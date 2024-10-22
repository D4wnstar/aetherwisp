The **Bernoulli entropy** or **binary entropy function** is a function for the [[Entropy (information theory)|information-theoretical entropy]] of a binary process, with [[probability]] $p$. It is defined as
$$H(p)=-p\log_{2}p-(1-p)\log_{2}(1-p)$$
It can be used to describe any process with two possible outcomes. As with entropy, the base of the logarithm is arbitrary. Base two and base $e$ are the most common. Below is with base $e$:

```mathpad
%$1:=-(-p+1)*log(-p+1)-log(p)*p
H(p):=-p*log(p)-(1-p)*log(1-p)
plot(H(p), [0,1], [0,1])==?
```


