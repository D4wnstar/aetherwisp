The **electrical resistance** $R$ of a material is the amount of [[electric current]] running through it per unit [[electric potential]]. For metals, it can be calculated with [[Ohm's laws|Ohm's first law]]. It is measured in Ohms, $\Omega$. The resistance of a material is also dependent on its temperature.
### Behavior in series and parallel
Consider two resistances $R_{1}$ and $R_{2}$ in a circuit of total potential difference $\Delta V$ and traversed by a current $I$. Say they are placed in series one after another.

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}[scale=2]
\draw
(0,0) to[R, o-o, l=$R_1$] (1,0)
(1,0) -- (2,0)
(2,0) to[R, o-o, l=$R_2$] (3,0)
;
\end{circuitikz}
\end{document}
```

The difference caused by the first one is $\Delta V_{1}=R_{1}I$ and the second is $\Delta V_{2}=R_{2}I$. It must be that $\Delta V=\Delta V_{1}+\Delta V_{2}$ so
$$\Delta V=R_{1}I+R_{2}I=(R_{1}+R_{2})I$$
Resistances therefore *sum* in series. More generally, for $n$ resistances:
$$\boxed{R=\sum_{i=1}^{n}R_{i}}$$

Say now they are in parallel.

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}
\draw
(0,0) -- node[currarrow]{} (1,0)
(1,0) -- (1,1)
(1,0) -- (1,-1)
(1,1) to[R, o-o, l=$R_1$] (3,1)
(1,-1) to[R, o-o, l=$R_2$] (3,-1)
(3,1) -- (3,0)
(3,-1) -- (3,0)
(3,0) -- node[currarrow] {} (4,0)
;
\end{circuitikz}
\end{document}
```

The current intensity now is $I=I_{1}+I_{2}$, split between the branches of the circuit. We can express them through Ohm's law
$$I_{1}=\frac{\Delta V}{R_{1}},\qquad I=\frac{\Delta V}{R_{2}}$$
so
$$I=I_{1}+I_{2}=\Delta V\left( \frac{1}{R_{1}} + \frac{1}{R_{2}} \right)$$
The *reciprocal* of resistance therefore *sum* in parallel. More generally, for $n$ resistances:
$$\boxed{\frac{1}{R}=\sum_{i=1}^{n} \frac{1}{R_{i}}}$$
