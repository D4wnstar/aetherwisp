---
wiki-publish: true
---
The **exponential series** is the [[series]] that defines the exponential function $e^{x}$:
$$\sum\limits_{n=0}^{\infty} \frac{x^n}{n!}=e^x$$
It converges only for $x=1$. The first terms are
$$e^{x}=1+ x+ \frac{x^{2}}{2}+ \frac{x^{3}}{6}+\ldots$$
### Exponential of a matrix or operator  
This definition can also be used to extend the exponential to the exponential of a [[matrix]] or [[operator]]. For a matrix or linear operator $A$, its exponential is
$$e^{A}=\sum_{n=0}^{\infty} \frac{A^{n}}{n!}$$
which is computable by recalling that the power of an operator is simply the repeated application of that operator:
$$A^{2}=AA,\quad A^{n}=\underbrace{ AA\ldots A }_{ n\text{ volte} }$$
Then the first terms are
$$e^{A}=1+ A+ \frac{AA}{2}+ \frac{AAA}{6}+\ldots$$
As with all operators, the exponential of an operator (itself an operator) only makes sense when applied to something.