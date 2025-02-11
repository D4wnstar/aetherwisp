---
aliases:
  - emf
  - motional emf
  - flux rule
---
The **electromotive force** (or **emf** for short) $\mathcal{E}$ is the transfer of energy per unit [[electric charge]] to a circuit, usually by a generator or battery. It is an [[electric potential]] difference, measured in volts, that can be thought of as "putting charges in motion" within a circuit. Despite the name, it is not a force. In the case of a closed circuit powered by a sole generator, the voltage of the circuit is equivalent to the electromotive force produced by the generator.

Given any non-[[conservative force]] per unit charge $\mathbf{f}$ inside of a generator, it is defined as
$$\mathcal{E}=\int_{A}^{B}\mathbf{f}\cdot d\mathbf{r}=\oint_{\gamma} \mathbf{f}\cdot d\mathbf{r}$$
where the first integral is calculated between the terminals $A$ and $B$ of the generator, whereas the second is over the entire [[curva|closed loop]] of the circuit $\gamma$. The two integrals are the same because $\mathbf{f}=0$ outside the generator anyway, so the extension to the whole circuit is free. Since $\mathbf{f}$ has to be non-conservative, it cannot be an [[Electric field|electrostatic field]].
### Flux rule
In the specific case of a loop of [[electric current]] moving through a static [[magnetic field]], an emf is produced by the work done by whatever is pulling the loop being converted into a push of the charges by the magnetic field. This form of emf is called **motional emf** and is the basis of generators, which transform mechanical energy into electrical one. The amount of motional emf can be found with a straightforward law called the **flux rule**:
$$\mathcal{E}=- \frac{d\Phi}{dt}$$
This tells us that the motional emf $\mathcal{E}$ is equal to the opposite of the change in the magnetic flux $\Phi$ through the loop. If you pull a loop out of a magnetic field, the flux reduces in time and the derivative is negative, which correctly yields a positive emf. It is the integral form of [[Faraday's law]].

In fact, by studying [[electromagnetic induction]], we can generalize the flux rule to state that whenever a magnetic field going through a loop changes (for *any* reason, be it movement of the loop, of the flux, variation in the generating current, etc.), a emf equal to
$$\mathcal{E}=- \frac{d\Phi}{dt}$$
will be found in the loop.
### Origin
Consider a closed circuit of any sort. We know that the electric field is [[conservative force|conservative]], so the circulation is always zero:
$$\oint_{\gamma} \mathbf{E}\cdot d\mathbf{r}=0$$
for any closed curve $\gamma$. Thus, for any closed circuit the potential difference for a full trip around the wire must itself be zero. This means that an electrostatic field alone cannot possibly account for the creation of an electric current[^1] and so the generators and batteries that power the circuit cannot produce the potential difference by way of electrostatics, opting instead to *convert* other kinds of energies (mechanical for generators, chemical for batteries) *into* electrical energy. The important difference is that the forces at play here are not conservative and therefore *do* produce a potential difference across a loop.[^2] The forces in question are associated with a field that produces them, which we call **electromotive field**. Don't let the name mislead you: it is emphatically not electrostatic in nature (else it defeat the entire point). It's called what it is because its purpose is to move electric charges around.

Say you have a generator attached to a circuit at points A and B keeping a potential difference $\Delta V$ between the two. Outside the generator, you only have the electrostatic field $\mathbf{E}_{s}$, but inside it you also have the electromotive field $\mathbf{E}_{m}$, leading to a total internal field of $\mathbf{E}=\mathbf{E}_{m}+\mathbf{E}_{s}$ (note that the electromotive field has the opposite direction of the electrostatic one). The circulation of the electrostatic field is zero, as seen above, so
$$\underset{ \text{inside} }{ \int_{A}^{B} }\mathbf{E}_{s}\cdot d\mathbf{r}=-\underset{ \text{outside} }{ \int_{B}^{A} }\mathbf{E}_{s}\cdot d\mathbf{r}$$
but this is not true when we add the electromotive field into the mix, as it is not conservative. The electromotive field is zero outside the generator, so what we get is
$$\oint \mathbf{E}\cdot d\mathbf{r}=\oint(\mathbf{E}_{m}+\mathbf{E}_{s})\cdot d\mathbf{r}=\underset{ \text{inside} }{ \int_{B}^{A} }\mathbf{E}_{m}\cdot d\mathbf{r}=\mathcal{E}$$
in which case the circulation of the total field is not zero and is entirely determined by the electromotive field. For this reason, we call this value the **electromotive force** that acts onto the charges of the wires and creates the current.

To see how this correlates to the voltage of the system, consider the case where the generator is not actually attached to anything (A and B are just "dangling" terminals). In this case, there is no current and the two fields cancel each other out: $\mathbf{E}=\mathbf{E}_{m}+\mathbf{E}_{s}=0$. This is because the electromotive field does actually move charges around *within* the generator, so that positive charges pile up on one terminal and negative ones on the other. But these charges are the ones that produce the electrostatic field, which opposes the electromotive one. Thus, in time, the difference between the charges across the terminals will be large enough that the electrostatic field will cancel it out completely, ending up in a state of equilibrium. If this sounds like the definition of a potential difference, it's because it is. If we calculate the emf inside we get
$$\mathcal{E}=\underset{ \text{inside} }{ \int_{B}^{A} }\mathbf{E}_{m}\cdot d\mathbf{r}=-\int_{B}^{A}\mathbf{E}_{s}\cdot d\mathbf{r}=V_{A}-V_{B}=\Delta V$$
Therefore, if we were to connect the two terminals with a wire, the voltage on that circuit would be precisely $\mathcal{ E}$, at least at the start when current has not yet started flowing. Once current $I$ does begin flowing, two things happen: one, the charges inside the generator begin moving, so they are subject to whatever internal [[electrical resistance]] $r$ the generator has, which produces a second potential difference opposite the emf; second, [[Ohm's law|Ohm's first law]] kicks in and a third potential different is produced dependent on the wire's resistance $R$. If we put this all together we get
$$\Delta V=RI$$
and also
$$\Delta V=\mathcal{E}-rI$$
so
$$\boxed{\mathcal{E}=RI+rI=(R+r)I\geq \Delta V}$$
The two resistances are in series, so the sum between the two is expected. What this means is that the emf, once in motion, is the sum of potential rises and falls across the entire length of the wire. In fact, $R$ could be any combination of resistances and $\mathcal{E}$ would be their combined effect, plus the internal resistance of the generator. Moreover, if $r$ is very small (at least compared to $R$), we might as well ignore it and what we are left with is, again, Ohm's first law. In fact, even if we do include it, our result is nothing more than a sensible application of that law. A generator whose internal resistance is (approximated as) zero is called a **perfect generator** and is shown in diagrams as

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}
\draw
(0,0) to[battery1] (2,0)
;
\end{circuitikz}
\end{document}
```

where the longer line is the positive end (i.e. higher potential) and the shorter one the negative end.
### Generators in series and parallel
Say you have an open circuit containing $n$ identical real generators producing an emf $\mathcal{E}$ each of which with internal resistance $r_{i}$.

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}
\draw
(0,0) to[battery1] (2,0)
(2,0) to[battery1] (4,0)
(4,0) to[battery1] (6,0)
(6,0) to[battery1] (8,0)
(8,0) to[battery1] (10,0)
;
\end{circuitikz}
\end{document}
```

If the circuit is open and the ends are not connected to anything else, the potential difference at the ends is the total electromotive force of the generators, which just is
$$\Delta V=\mathcal{E}'=n\mathcal{E}$$
so generators in series sum their emfs. The total resistance is of course $r=\sum r_{i}$.

Say now they are in parallel.

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}
\draw
(0,0) -- (2,0)
(2,0) -- (2,4)
(2,0) -- (2,-4)
(2,4) to[battery1] (4,4)
(2,2) to[battery1] (4,2)
(2,0) to[battery1] (4,0)
(2,-2) to[battery1] (4,-2)
(2,-4) to[battery1] (4,-4)
(4,4) -- (4,-4)
(4,0) -- (6,0)
;
\end{circuitikz}
\end{document}
```

The current gets split among all the generators, so the emf is
$$\Delta V=\mathcal{E}'=\mathcal{E}$$
but the resistance is also split and is
$$\frac{1}{r'}=\sum_{i=1}^{n} \frac{1}{r_{i}}\quad\Rightarrow \quad r'=\frac{r}{6}$$
which reduces the [[Joule effect]] and overall leads to a more efficient transfer of energy. On top of that, since the total energy is now $n$ times greater, this current can be maintained $n$ times longer, leading to a much more long lived system (if you plug two batteries in parallel, the thing you're powering will last twice as long).

To summarize, generators in series move $n$ times more energy but run out of energy in the same time as a single generator, but ones in parallel move the same amount of energy, but do so for $n$ times longer. Series allows for a greater burst of current, whereas parallel allows for a more long term application.

[^1]: As a matter of fact, this electrostatic field could very well be zero everywhere, as is the case with steady currents, and yet the current is clearly there.
[^2]: This is why it's impossible to create an everlasting battery. If the battery never lost any energy of its own, it could never produce a potential difference! The reason why battery technology does improve over time is because this energy transfer is inefficient and some of the energy gets "lost in transport", but the transfer itself must happen.