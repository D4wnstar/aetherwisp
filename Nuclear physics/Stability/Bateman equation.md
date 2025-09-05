---
wiki-publish: true
---
The **Bateman equation** determines the [[activity]] of the $n$-th step of an arbitrarily long [[Radioactive decay law|decay chain]] at some point in time:
$$A_{n}=N_{0}\sum\limits_{i=0}^{n}c_{i}e^{-\lambda_{i}t}=N_{0}(c_{1}e^{-\lambda_{1}t}+c_{2}e^{-\lambda_{2}t}+\ldots+c_{n}e^{-\lambda_{n}t})$$
where $c_{i}$ is
$$c_{i}=\frac{\prod\limits_{j=1,\ j\neq i}^{n}\lambda_{j}}{\prod\limits_{j=1,\ j\neq i}^{n}(\lambda_{j}-\lambda_{i})}=\frac{\lambda_{1}\lambda_{2}\lambda_{3}\ldots\lambda_{n}}{(\lambda_{1}-\lambda_{i})(\lambda_{2}-\lambda_{i})\ldots(\lambda_{n}-\lambda_{i})}$$
The Bateman equation is the solution to the [[ordinary differential equation]]
$$\frac{dN_{n}}{dt}=\lambda_{n-1}N_{n-1}-\lambda_{n}N_{n}$$
for the decay rate of the $n$-th nuclear species.