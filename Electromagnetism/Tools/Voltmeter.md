---
wiki-publish: true
---
A **voltmeter** is a tool used to measure [[electric potential]] differences within a circuit. It is attached in parallel at the ends of an [[electrical resistance]] (or some other combination of components) whose potential drop needs to be measured and is specifically designed to have an extremely high internal resistance to avoid causing a significant split in the current passing through the node where the voltmeter is attached.
## Mechanism
A voltmeter is actually built from an [[ammeter]]. A voltmeter is essentially just an ammeter in series with a really large[^1] additional resistance $R_\text{add}$. In such a circuit, we have
$$R_\text{volt}=R_\text{amm}+R_\text{add}$$
here $R_\text{amm}$ is the resistance of the ammeter (probably tiny). The voltmeter is applied in parallel to the actual resistance $R$ we are trying to measure the drop of, so there are two branches. In parallel circuits, the potential is identical in both branches, but the current is split, as per [[Kirchhoff's laws]]. Call $I$ the total current and $I_\text{volt}$ the one going through the voltmeter branch. Then
$$\Delta V=(I-I_\text{volt})R,\qquad \Delta V_\text{volt}=I_\text{volt}R_\text{volt}\tag{1}$$
but as we said, the potential is the same across branches, so $\Delta V=\Delta V_\text{volt}$ when taking the measurement. *However*, this is a key detail. These two are the same only when the voltmeter is attached to measure, but because attaching the voltmeter splits the current, the measured $\Delta V$ will *not* be the true $\Delta V$, as the voltmeter "steals" some current from the main circuit, thus reducing the potential drop. Therefore, the voltmeter's measured potential is guaranteed to be an underestimate of the real potential drop that occurs when the voltmeter is not present.

This difference can be quantified. The true potential drop is given by
$$\Delta V_\text{true}=IR$$
which differs from the measured one
$$\Delta V_\text{meas}=(I-I_\text{volt})R$$
due to the voltmeter taking away some of the current. They are equal only when
$$\Delta V_\text{true}=IR=(I-I_\text{volt}+I_\text{volt})R=\left( \frac{\Delta V_\text{meas}}{R}+ \frac{\Delta V_\text{meas}}{R_\text{volt}} \right)R$$
by using $(1)$, so
$$\boxed{\Delta V_\text{true}=\Delta V_\text{meas}\left( 1+ \frac{R}{R_\text{volt}} \right)}$$
$R_\text{volt}$ is chosen during manufacturing, so as long as $R$ is known, $\Delta V_\text{meas}$ is the only necessary measurement to recover the real voltage drop. In turn, this means measuring $I_\text{volt}$ as per usual with the ammeter. Note how when $R/R_\text{volt}\to 0$, $\Delta V_\text{true}=\Delta V_\text{meas}$. Thus, we want our voltmeter resistance to be as high as possible compared to the circuit we're measuring.

[^1]: By large we mean with respect to the resistance causing the voltage drop we are measuring.
