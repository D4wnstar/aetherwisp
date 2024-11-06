In information theory, the **source code** is the collection of strings expressed in a predetermined set of symbols called an alphabet that encode some or all of the possible outcomes of a random event.
### Definitions
Let's define a [[random variable]] $X$ in a [[sample space]] $\mathcal{X}$ which defines a sequence of variables $\underline{X}=(X_{1},X_{2},\ldots,X_{n})$. Another function $w:\mathcal{X}\to D^{*}$ converts the outcomes of the variable into an **alphabet** $D$, where $D$ is a set of known values used to encode the outcomes. Typically, this is the binary set $D=\{ 0,1 \}$. The asterisk $D^{*}$ denotes that the output of $w$ is a finite sequence of elements of $D$. An element of $D^{*}$ is called a **string**, and $D^{*}$ is the set of all possible strings. If the element is given by $w$ specifically, it is called a **codeword**. For instance, if $D$ is the binary set, a code in $D^{*}$ might be $01010011$. The collection of all possible strings (one for each outcome) is the **source code**, or just **code**.

A code is said to be **non-singular** if every element of $\mathcal{X}$ maps to a different string in $D^{*}$. In symbols, $x\neq x' \Rightarrow w(x)\neq w(x')\ \forall\ x,x'$.

The **extent** $w^{*}$ of a code is the mapping between finite strings of $\mathcal{X}$ to finite strings of $D^{*}$. The codeword function $w$ is a special case of $w^{*}$.

A code is **uniquely decodable** if its extent is non-singular.

A code is said to be **instantaneous** if no codeword is the prefix of any other codeword. For instance, the word $w_{1}=01$ would be the prefix of the codeword $w_{2}=010$. This property is useful because it makes signals resilient to miscommunication. A non-instantaneous signal can only be decoded if the full signal is received. An instantaneous code can be decoded piecemeal even if only bits and pieces are received since each codeword can be uniquely isolated in the sequence.
### Properties
The product of outcomes in the codeword function $w$ results in the concatenation of the codewords:
$$w(x_{1}x_{2}\ldots x_{n})=w(x_{1})w(x_{2})\ldots w(x_{n})$$
For instance, if $w(x_{1})=00$ and $w(x_{2})=11$, we have $w(x_{1}x_{2})=0011$.
### Examples
> [!example] Four possibilities
> Consider an event $X$ with four possible outcomes. Let's analyze some ways of encoding them.
> $$\begin{array}{c|c|c|c|c}
> x & w_{1}(x) & w_{2}(x) & w_{3}(x) & w_{4}(x) \\
> 1 & 0 & 0 & 10 & 0 \\
> 2 & 0 & 110 & 00 & 10 \\
> 3 & 0 & 01 & 11 & 110 \\
> 4 & 0 & 10 & 110 & 111
> \end{array}$$
> 1. Encoding 1 is clearly singular as all codewords are the same.
> 2. Encoding 2 is non-singular, but it is not uniquely decodable.
> 3. Encoding 3 is both non-singular and uniquely decodable, but it isn't instantaneous because 11 is the prefix of 110. For instance, the communication snippet $110000$ can either be 4, 2 and the start of another 2 or 3, 2 and 2. Without knowing the start and end, we can't be sure.
> 4. Encoding 4 is non-singular, uniquely decodable and instantaneous.
