**Conditional execution** or **branching** is the process whereby some machine instruction are only executed under certain circumstances. At a high level, this typically maps to logical branches like `if-else` statements. At an [[assembly]] level, certain instructions are conditional by definition. For example, `je` and `jne` are both conditional instructions.

Conditional execution requires a way to altering the execution flow: this is done through the **jump instruction** `jmp`, which causes control to be passed to a different code section. `jmp` may be itself conditional. Conditional instructions access the values stored in the bits of the flag register, a special register where the CPU stores some information on the last arithmetic or logical operation.

Let's see an example: consider the following C code:

```c
for (int i=0; i<10; i++)
	array[i] = 0;
```

where `array` is some valid variable. This code implicitly contains a condition: is the loop finished? The [[compiler]] could, depending on optimization level[^1], translate this to

```asm
.L2:
	mov    DWORD PTR [rax], 0
	add    rax, 4
	cmp    rax, rbp
	jne    .L2
```

In order:
1. `DWORD` does direct memory access to the $i$-th element of the array. `rax` is the [[register]] that contains the address of `array` and uses it to set `array[i]` to 0.
2. The index $i$ is increased by one: specifically, the memory address `rax` is increased by one `int` worth of bytes (4) so that it points to the next `int` in the array (which is contiguous is memory).
3. The new index is compared to the ending bound of the loop ($i=10$) to check whether to loop should end. *This is the condition.* `cmp` sets the `ZF` flag (*zero flag*) if the loop is over; this flag can then be checked by conditional instructions. Specifically, `cmp` checks if `rax - rbp <= 0`, which means checking that the memory address of the current element (`rax`) is within the termination value of the array (`rbp`).
4. `jne` jumps back to `.L2` if the `ZF` flag is not set (i.e., continues the loop), otherwise does nothing (i.e., goes on with the rest of the program after the loop).

### Performance
Conditional branching can be *expensive*. Modern CPUs modern processors achieve great performance thanks to [[pipeline|pipelines]] and [[out-of-order execution]], that is, by decomposing complex instructions in simpler steps and mixing the execution of those sub-steps for different instructions.[^2] However, in order to fill these pipelines, the CPU needs to know what to place in them in advance. With unconditional execution, this is largely trivial: just dump the next $N$ instructions into the pipelines, since you know for a fact that they will happen. With conditional execution, by definition the CPU does not know what will happen until the condition is checked, so it can't fill the pipelines. Or rather, not confidently: modern CPUs tackle this problem by implementing a very sophisticated feature called a **branch predictor**, which is an internal unit of the CPU that tries to predict the result of a future condition before it happens. By using these, the CPU can prefill the pipelines using the instructions that it predicts will happen and preserve much of its optimizations, even under conditional branching, with little to no programmer action required.

Predictors aren't perfect though, but they can be very accurate: their accuracy depends on the *regularity of the data and the code*. On regular code that exhibits clear patterns, the predictor than reach more than 99% accuracy. On complex code with unpredictable patterns (or none at all), this figure can lower to 90-95% or even much lower in pathological cases (e.g., with completely [[random]], [[Uniform distribution|uniform]] data). This is significant as misprediction can incur considerable performance penalties in the order of 10-30 [[CPU cycle|CPU cycles]]. This is where code structure becomes significant. There a several ways one can help the branch predictor do its job well, some compiler-specific, some universal. One universal best-practice is to take conditions outside of loops (in practice: take `if-else` statements outside of `for`/`while` loops). The presence of a condition inside a loop makes it hard for the compiler to optimize it, as the predictor needs to be right for every single loop cycle. If you make the *entire* loop conditional remove all inner condition, then the loop can be optimized much more efficiently as it is now entirely unconditional. As a rule of thumb, the code pattern you should follow looks a little like this:

```c
// Branch predictor has trouble
for (int i=0; i<10; i++)
{
	if ( /* condition here */ )
	{
		// conditional loop code...
	}
}

// Branch predictor has fewer issues
if ( /* condition here */ )
{
	for (int i=0; i<10; i++)
	{
		// unconditional loop code...
	}
}
```

If you have multiple `if` branches per loop, it is likely worth writing smaller, more specialized loops, one per branch. So, for instance, if your loop has three `if` branches, you may be better off extracting the `if`s out of the loop, then writing three separate, smaller loops, one for each `if`.

```c
// This...
for (int i=0; i<10; i++)
{
	if ( /* condition 1 */ ) { /* branch 1 */ }
	if ( /* condition 2 */ ) { /* branch 2 */ }
	if ( /* condition 3 */ ) { /* branch 3 */ }
}

// ...should become this.
if ( /* condition 1 */ )
{
	for (int i=0; i<10; i++) { /* loop 1 */ }
}
if ( /* condition 2 */ )
{
	for (int i=0; i<10; i++) { /* loop 2 */ }
}
if ( /* condition 3 */ )
{
	for (int i=0; i<10; i++) { /* loop 3 */ }
}
```

It can be more verbose, but it makes the compiler happier as the loops are now unconditional. Of course, this isn't always possible. If a condition depends on the loop index/element, then you can't bring the condition outside and you'll need other

[^1]: Compiling with high optimization might very well delete this entire loop, since it's just a trivial assignment of a compile-time constant.

[^2]: Up to hundreds of instructions at the same time may be "on-the-fly" in modern CPUs. For example, AMD Zen 4 CPUs have a **Reorder Buffer** size of 320.
