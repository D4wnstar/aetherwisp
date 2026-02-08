---
wiki-publish: true
---
A **Wheatstone bridge** is a [[bridge circuit]] designed to measure [[Electrical resistance|electrical resistances]]. It is composed of two parallel branches each containing two resistors in series. The branches are connected by an [[ammeter]] or [[galvanometer]] at the midpoints between the resistors. A [[voltmeter]] may also be used instead. Three of the four resistors have known resistance, while the fourth is unknown and to be measured.

:::image
![[Wheatstonebridge.svg]]
Circuit diagram of a Wheatstone bridge. $R_{1}$, $R_{2}$ and $R_{3}$ are known resistances, while $R_{X}$ is unknown. $V_{G}$ is a galvanometer.
By Rhdv - Own work, CC BY-SA 3.0, from [Wikipedia](https://commons.wikimedia.org/w/index.php?curid=2888809)
:::

### Usage
Wheatstone bridges are intended for measuring the resistance of an electrical component by finding the specific combination of other resistances such that the branches are balanced. Referring to the figure above, $R_{1}$, $R_{2}$ and $R_{3}$ are known resistors whereas $R_{X}$ is the one to be measured. $V_{G}$ is a galvanometer, but could also be an ammeter or voltmeter. The idea of the bridge is to find a set of $R_{1}$, $R_{2}$ and $R_{3}$ for which the galvanometer detects nothing:
$$\text{find }R_{1},R_{2},R_{3}\text{ such that }I_{BD}=0$$
(or $\Delta V_{BD}=0$ if using an voltmeter). The benefit of this kind of technique over measuring, say, $(\Delta V,I)$ pairs and using [[Ohm's law]] directly is that precisely detecting a zero-point for current can be done to excellent precision and also doesn't stress the resistor's material, since you're using tiny $I$ instead of progressively larger ones. This avoids issues with the [[Joule effect]] and non-ohmic regimes.

If we call $I_{1}$, $I_{2}$, $I_{3}$ and $I_{X}$ the current corresponding to the resistances, according to [[Kirchhoff's laws]], when there is no current going through the bridge ($I_{BD}=0$) we need to have
$$\begin{cases}
I_{1}=I_{2} \\
I_{3}=I_{X}
\end{cases}\tag{1}$$
Assuming the resistors all abide by Ohm's law, they require
$$\begin{cases}
\Delta V_{1}=R_{1}I_{1} \\
\Delta V_{2}=R_{2}I_{2} \\
\Delta V_{3}=R_{3}I_{3} \\
\Delta V_{X}=R_{X}I_{X}
\end{cases}\tag{2}$$
Potential is the same across parallel branches so $\Delta V_{1}=\Delta V_{3}$ and if there's no current flow between the branches ($I_{BD}=0$) then also $\Delta V_{2}=\Delta V_{X}$. Combining this fact with $(2)$ yields
$$\begin{cases}
R_{1}I_{1}=R_{3}I_{3} \\
R_{2}I_{2}=R_{X}I_{X}
\end{cases}$$
and using $(1)$
$$\begin{cases}
R_{1}I_{1}=R_{3}I_{3} \\
R_{2}I_{1}=R_{X}I_{3}
\end{cases}$$
Dividing row by row yields
$$\frac{R_{1}}{R_{2}}=\frac{R_{3}}{R_{X}}\quad\Rightarrow \quad R_{X}=\frac{R_{3}}{R_{1}}R_{2}\quad\text{when }I_{BD}= 0$$
This is our formula for the unknown resistance. Since the three resistances are arbitrary, a common practical trick is to choose $R_{1}$ and $R_{3}$ to be intermediate (neither high nor low) and equal, so that they vanish from the equation leaving simply:
$$\boxed{R_{X}=R_{2}\quad\text{when }R_{1}=R_{3}\text{ and }I_{BD}= 0}$$
The practical work then simply involves swapping out $R_{2}$ for different resistors until you find one where the voltmeter/ammeter detects no potential/current: when you do, you've found $R_{X}$.