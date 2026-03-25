**Message passing** is a memory sharing paradigm. It involves connecting separate nodes of a compute cluster by passing structured messages between, which may be used to request access to non-local memory owned by different nodes. It is primarily intended for distributed computing, but also works in a shared memory paradigm.

In distributed parallelization, the program to run is distributed into separate processes for each node, each with its own memory address space. Each node has access to its local memory, but not to that of other nodes. This allows each node to act independently of all others without having to worry about memory conflicts: this is known as the **shared nothing** approach. Then, the choice of where data resides rests on the programmer, who chooses which process to assign a certain piece of memory to. This data may then be accessed by other processes by sending it with a **message** from one node to another with contains the request data. Messages are also defined by the programmer. This means that in the message passing paradigm, the programmer is responsible for two things: data locality (where do we put the data?) and message distribution (how do we move the data?).

The benefits of message passing is that it makes memory scaling easy at a hardware level. Since each processor (or node) manages its own memory, to add more memory you just add more processors and wire them up together. The downside is that communication between nodes is entirely the responsibility of the programmer. Since data is divided across multiple address spaces, the programmer needs to decide all of the details about how the processors communicate and how to keep the entire program synchronized across all nodes at all times. The other aspect to worry about is [[non-uniform memory access]] (NUMA). Since data is physically distant (not just logically), accessing memory in a different node takes longer than local memory because it needs to travel across the cluster network. Data transfer speeds are limited by the wiring technology and the [[speed of light]].
## MPI
Message passing is typically implemented through the **Message Passing Interface** (**MPI**), which is a 1994 standard[^1] for writing message passing code. MPI itself has no canonical implementation and several libraries for it exist; these involve working with the network drivers to handle node-to-node communication. Relevant implementations are **MPICH** (the oldest, original MPI implementation), **OpenMPI** and **IntelMPI**. Compiling a program that includes MPI instructions also requires a compiler with bespoke support for it, usually specified by additional flags. For example, `gcc` provides MPI support for C/C++. Compiler wrappers like `mpicc` exist to make the compilation process more convenient, as do runners like `mpirun` to handle the actual runtime usage of MPI code.
### Introduction to MPI programming
In MPI, library functions can be roughly divided in four categories:
- Calls used to initialize, manage, and terminate communications.
- Calls used to communicate between pairs of processors (**pair communication**).
- Calls used to communicate among groups of processors (**collective communication**).
- Calls to create custom data types.

To start, you'll want to know six functions:
- `MPI_INIT`. This initializes MPI for the program.
- `MPI_COMM_SIZE`. This tells the program how many processors are available for communication.
- `MPI_COMM_RANK`. This returns the identifier of a processor.
- `MPI_SEND`. This sends data to a processor.
- `MPI_RECV`. This receives data sent with `MPI_SEND`.
- `MPI_FINALIZE`. This shuts MPI down.

The general structure of an MPI program looks like this (in C):

```c
#include<mpi.h>

int main(int argc, char **argv)
{
	MPI_Init(&argc, &argv);
	
	// parallel code here...
	
	MPI_Finalize();
	return 0;
}
```

Then compile with `mpicc your_code_here.c -o compiled` and run with `mpirun -np 8 ./compiled`.[^2]

In MPI, communications are handled by one or more **communicators**. A communicator is a variable identifying a **group** of processes that are allowed to communicate with each other, alongside additional context. A group is a collection of processes (tasks) that are related in some way. A task may be in multiple groups simultaneously. In MPI, there is a default communicator that is automatically defined and encompasses all tasks called `MPI_COMM_WORLD`, but as a programmer you are allowed to define more specific communicators. Every single MPI function that deals with communication takes a communicator as an argument. The **size** of a communicator is the number of processors associated with a communicator. The **rank** of a processor in a communicator is its index within the communicator, which spans between `0` and `size - 1`, and is used to select what processor to send a message to inside the communicator.

> [!tip] Communicator isolation
> It is best practice to avoid using `MPI_COMM_WORLD` directly to avoid conflicts with other applications running on the same machine at the same time. For example, if you use a library that internally employs MPI, it could conflict with your own code due to using the same global communicator. Instead, always create a custom communicator at the start of your program by duplicating the world into a separate `my_comm_world` variable with `MPI_Comm_dup(MPI_COMM_WORLD, &my_comm_world)`. Then, use `my_comm_world` wherever you'd use `MPI_COMM_WORLD`. Since `my_comm_world` is owned by your application only, it has its own isolated context that won't conflict with other processes.

Creating communicators for different parts of your program allows you to manage different tasks for different purposes. This is useful to reason about the program, to isolate data to avoid conflicts and also to express different levels of parallelism.

Once you have a communicator, you're ready to send and receive messages. A message contains some data, of course, alongside some additional information on what to do with it. The data itself is defined as a triple of: memory address, count of elements sent and data type. Memory address and element count are needed to read the data from the correct address in memory, whereas data type tells the receiver what the data is. Data types in MPI can be a bit complicated, as they aren't the regular data types of the language you're working with. Instead, MPI libraries define custom data types corresponding to basic language primitives, like `MPI_INT` or `MPI_DOUBLE` in a C implementation. When passing a data type for a message, you actually have quite a bit of freedom on what you pass. Namely, the data type field of a message accepts:
- A single data type, like `MPI_INT`.
- A contiguous array of data types.
- A strided block of data types.
- An indexed array of blocks of data types.
- An arbitrary structure of data types.

The first option is the simplest: the data is just one or more instances of that type. For example, setting count to 10 and data type to `MPI_INT` tells the receiver that the sent memory buffer contains 10 integers. To avoid sending unnecessary messages, you may also send heterogeneous data (e.g., sending integers and floats at the same time). The other four data type options allow you to send mixed data by specifying what exactly is inside the byte stream you sent. The MPI standard also defines ways to build custom data types.

Beyond data, messages carry a **tag**, which is a simple user-defined integer. This tag has no predefined meaning and it can be freely used to create custom identifiers for messages. Receivers can then filter incoming messages by tag, such as saying "I only care about messages with `tag == 42`". Alternatively, `MPI_any_tag` may be used to not filter at all.

Knowing this, a call to send a message generally looks like this:

```c
MPI_Send(buffer, count, data_type, destination, tag, communicator)
```

The `buffer`, `count` and `data_type` are the data triple, and `tag` has already been explained. `destination` is the rank of the processor to send the message to, and `communicator` is the communicator to route the message through. Meanwhile, receiving a message looks like this:

```c
MPI_Recv(buffer, count, data_type, source, tag, communicator, status)
```

The function signature is similar to send (after all, the message is still the same), with a few differences. `source` is the rank of the sender. You can use this to filter messages like you would with tags, such as "I only want messages from processor 6", and you can use `MPI_any_source` to not filter. `status` is a struct that contains the status code of the message, as in whether it succeeded or not, and information of what happened if it didn't. `MPI_Recv` modifies in-place, so the arguments are all pointers to variables.

These send and receive functions are **blocking**. They stop the program until the entire operation completes: for send, the operation is done when it is safe to change the data that we sent; for receive, it is done when it is safe to access the data we received. This is easy to reason about, but may be a serious performance bottleneck. If you know [[asynchronous programming]], you may already know what we're about to do: **non-blocking calls**. A non-blocking call, in this context, refers to starting a communication and then immediately returning control to the main program instead of waiting for it to complete. By doing so, we can let the communication happen in the background while the program keeps doing what it's supposed to without wasting precious computation time. However, blocking operations are *safe*: they only let the program move on when everything's done. Non-blocking operations are *unsafe*: you have to manually access or modify the data at some point after the communication started without the certainty of the program giving you the OK to do so. If you access or modify it before the communication is done, you'll get broken, corrupt data and risk all sorts of memory problems and [[undefined behavior]]. Because of this, using non-blocking communications, although performant, requires the programmer to *always* manually check the completion of a communication before doing anything with it, on pain of data corruption. Most communication functions in MPI have both a blocking and non-blocking variant; the latter is denoted by an `I` before the function name. The non-blocking variants of send and receive are `MPI_ISEND` and `MPI_IRECV` and have the same function signature.[^3]

[^1]: Technically only a "standard by consensus". It isn't the work of a single entity, but was rather originally designed collectively in a forum through the collaboration of many institutions, researchers and hardware vendors. It is not ratified by a standard agency like ISO or ANSI. The standard has changed much over the years. The most recent major version at the time of writing (March 2026) is MPI Version 5.

[^2]: The `-np <int>` option in `mpirun` is used to set the number of available processors.

[^3]: To continue the async analogy, this is similar to a library having both sync and async variants of the same function. For instance, in NodeJS, the `fs` module does this for I/O functions, like `write` and `writeSync`.
