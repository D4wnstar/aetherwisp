---
wiki-publish: true
---
**Numerical integration** is a broad category of methods and algorithms designed to calculate the numerical value of a definite [[integral]]. In general, the end goal of a numerical integration method is, given some function $f(x)$, to calculate its definite integral over a known range $[a,b]$
$$\int_{a}^{b}f(x)dx$$
to a desired degree of accuracy.

Numerical integration is commonly used to solve [[Ordinary differential equation|ordinary differential equations]]. A first-order autonomous ODE has, in general, the form
$$\dot{x}=f(x)$$
and in principle, finding $x$ in a given interval means taking the integral of $f(x,t)$ over $dt$. Since any ODE can be expressed as a system of first-order ODEs, and any non-autonomous system can be made to be autonomous by making the independent variable into an additional first-order ODE, any individual ODE can be solved in this manner. This is particularly useful for nonlinear ODEs, which are typically extremely difficult or impossible to solve analytically.