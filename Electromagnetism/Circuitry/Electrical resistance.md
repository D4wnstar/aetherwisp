---
hl-publish: true
aliases:
  - resistor
  - resistance
---
The **electrical resistance** $R$ of a material is the amount of [[electric current]] running through it per unit [[electric potential]]. For metals, it can be calculated with [[Ohm's law|Ohm's first law]]. It is measured in ohms, $\Omega$, which are volts per ampere. The resistance of a material is also dependent on its temperature.

Mechanically, resistance is added to a circuit by adding a component with very high resistance called a **resistor** or **resistance**.
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

The difference caused by the first one is given by [[Ohm's law|Ohm's first law]] as $\Delta V_{1}=R_{1}I$ and the second is $\Delta V_{2}=R_{2}I$. It must be that $\Delta V=\Delta V_{1}+\Delta V_{2}$ so
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
$$I_{1}=\frac{\Delta V}{R_{1}},\qquad I_{2}=\frac{\Delta V}{R_{2}}$$
so
$$I=I_{1}+I_{2}=\Delta V\left( \frac{1}{R_{1}} + \frac{1}{R_{2}} \right)$$
The *reciprocal* of resistance therefore *sum* in parallel. More generally, for $n$ resistances:
$$\boxed{\frac{1}{R}=\sum_{i=1}^{n} \frac{1}{R_{i}}}$$
### Experimental measurement
Typically, resistors are manufactured with a known electrical resistance. If you need to find the effective resistance of multiple resistors in series or parallel, you use the laws above. But what if you don't know the resistance values to begin with? Then you need to measure them experimentally using the component itself. Measuring them directly is not that easy, though. There exist tools called [[ohmmeter|ohmmeters]] that provide measurements of resistance through [[Ohm's law]], but they are in general not high-precision instruments, especially since Ohm's law itself is only an approximation.

A technique that does not involve a bespoke ohmmeter but still uses Ohm's law goes as follows. Consider a circuit made of an [[electrical generator]], the resistor to measure, a [[voltmeter]] hooked up parallel at the ends of the resistor and an [[ammeter]] in series with the circuit. The voltmeter and ammeter provide measurements of $\Delta V$ and $I$, which in turn provide the resistance through Ohm's law $R=\Delta V/I$. By taking measurements of multiple pairs of $(\Delta V,I)$, it is possible to find $R$ through, say, a [[Minimum squares method|linear minimum squares]], since $R$ ends up being the (inverse of the) slope in an $\Delta V\text{-}I$ plot. A few words of warning:
- You might expect the predicted line to always cross the origin (i.e., have zero intercept). In principle, that should always be true, but in practice, electrical wiring is noisy and there's always some background noise that causes issues with fine-grained measurements. Expect a small but nonzero intercept.
- It's important to not go too high with the currents, as then you risk going outside of ohmic regime, Ohm's law no longer applies and the relation is no longer linear. Also, you risk melting the resistance if the [[Joule effect]] becomes more intense than what the resistance is built to sustain.

For a more precise technique, you should use a [[Wheatstone bridge]].