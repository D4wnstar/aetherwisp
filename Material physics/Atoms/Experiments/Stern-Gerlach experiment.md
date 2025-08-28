---
wiki-publish: true
---
The **Stern-Gerlach experiment** is an experiment that almost accidentally discovered the [[spin]] of the [[electron]]. The true purpose of the experiment was to measure whether [[Particle|particles]] have an intrinsic [[angular momentum]] or not.
### Theory
The idea behind the Stern-Gerlach experiment starts from the [[Bohr model]] of the [[hydrogen atom]], which suggests that, since electrons orbit the [[Atomic nucleus|nucleus]], and rotating [[Electric charge|electric charges]] produce a [[magnetic field]], then hydrogen atoms should, at least in principle, be a naturally occurring [[magnetic dipole]] with [[magnetic dipole moment]] determined exactly by the motion of the electron.

To analyze the situation, consider a circular loop of radius $R$ and area $A=\pi R^{2}$ traversed by an [[electric current]] $I$. This will be our "toy hydrogen atom".

![[Spira con momento di dipolo|40%|center]]

This loop has a magnetic dipole moment perpendicular to the loop given by $\boldsymbol{\mu}=IA \hat{\mathbf{n}}$, where $\hat{\mathbf{n}}$ is the outgoing normal vector from the surface. For a single charge $q$ moving circularly at a velocity $v$ on that radius, we have a current
$$I=\lambda v=\frac{q}{2\pi R} v$$
where $\lambda$ is the linear charge density due to the charge particle. Of course, this density is highly variable in time, following the position of the particle. However, if we take the rotation of the particle to be very fast compared to the characteristic time of our system of interest[^1], we can consider $\lambda$ to be the [[mean]] value over an entire rotation, so $\lambda=q/2\pi R$. If we plug this in the dipole moment formula we get
$$\mu=IA=\frac{q}{2\pi R}v\pi R^{2}=\frac{1}{2}qvR$$
If the rotating charge has [[mass]] $M$, then it must have angular momentum $L=MvR$. We can invert this to find the velocity $v=L/MR$ and by plugging this into the formula above
$$\mu=\frac{q}{2M}L$$
This is a general relationship between magnetic dipole moment and angular momentum of a rotating charge. As it stands, we haven't used anything specific to atomic physics at all. This is just run of the mill electromagnetism. To make the connection to the hydrogen atom, we set the mass $M$ to be that of the electron $m_{e}$ and the charge to the [[Elementary charge]] $e$[^2], but more importantly, we invoke the Bohr model. According to the third postulate of that model, the electron's angular momentum is discrete, so $L$ can't be any real number. We're "stuck" with a set of choices determined by an integer as $L=n\hbar$, where $\hbar$ is the [[Planck constant|reduced Planck constant]]. Substituting this in $\mu$ leads to
$$\mu=\frac{e}{2m}n\hbar$$
This leads to the natural conclusion that all possible dipole moments of the hydrogen atom are in units of
$$\boxed{\mu_{B}=\frac{e\hbar}{2m}}$$
This quantity is known as the **[[Bohr magneton]]**, and it allows us to find the magnetic dipole moment of a hydrogen atom as its multiples.

So far so good. What Stern and Gerlach instead asked is this: we know that an orbiting charged particle creates a magnetic dipole, but does a particle *alone* create a magnetic dipole? In other words, they asked if the spinning of a particle also created a dipole through the same mechanism.

In principle, the request makes sense. Any spinning charged object of nonzero radius will cause a charge density to move, thus triggering [[Ampere's law]] and creating a magnetic dipole. What wasn't known was *which* dipole moments could be created. Bohr showed that angular momentum appeared to be quantized, so "any real dipole moment" was no longer a safe bet. Their experiment wanted to answer this question.
### Experiment
The experiment consisted of a source of silver atoms, which are then aimed and fired at through collimators to align the atoms into a thin beam. These atoms are then made to pass through two magnets (one with an exposed north pole, the other a south pole) irregularly shaped such that they create an inhomogeneous magnetic field $\mathbf{B}$. The inhomogeneity produces a net force $\mathbf{F}=\nabla(\boldsymbol{\mu}\cdot \mathbf{B})$ on the atoms passing through[^3]. The atoms then hit a [[Rivelatore|detector]] that reveals their where they hit.

:::image
![[Stern-Gerlach_experiment.svg]]
1 is the atom source. 2 are the collimators. 3 are the magnets. 4 is the expected distribution, 5 is the measured one. By Tatoute - Own work, CC BY-SA 4.0, from [Wikipedia](https://commons.wikimedia.org/w/index.php?curid=34095239).
:::

In the old way of thinking, there's no reason to think that we would see anything other than a smooth distribution of measured hits across the entire surface of the detector (see 4 in the figure). In the simple case of a hydrogen atom in the ground state, anything between $\mu_{B}$ and $-\mu_{B}$ would be fine, as it depends on how fast the atom is spinning. However, Bohr noted that this isn't the case. *Only* $\mu_{B}$ and $-\mu_{B}$ are allowed, but nothing in between. It's either spinning at a set (angular) speed in one direction, or at the same speed in the other. No in-between.

In fact, the observed distribution (see 5 in the figure) was only peaked around two points, at the two extremes, with near zero measurements everywhere else. Some atoms were being pushed up, other were being pushed down, but all of them with the same force, as they all landed near the same point. This confirmed Bohr's vision: there can only be discrete angular momenta. This behavior matched what would would expect out of a spinning particle and more. Not only did the atoms possess some sort of *intrinsic* magnetic dipole (and thus angular momentum), it was also *quantized*, just as Bohr had predicted. This intrinsic angular momentum was, in reference to the classical counterpart, named [[spin]].
### A correction
The formula we derived for $\mu$ works well enough for orbital momentum, but displays issues for spin. In reality, for spin specifically, this relationship is not quite correct, but the proof is not within the scope or historical context of this article. Quantum mechanics tells us that there is a factor, called the (electron spin) **[[g-factor]]** $g$, that rescales this equation, such that
$$\mu_{e}=g\frac{eS_{e}}{2m_{e}}$$
This is the actually correct form of the equation, shown for the electron, where we replaced $n\hbar$ with the more general spin $S_{e}$. It is found that this number is *approximately* $g=2$ (a couple thousandths more than 2, actually).

A more general form involving the total angular momentum $\mathbf{J}$ (not the current density!) gives us the total magnetic dipole moment of the system:
$$\boldsymbol{\mu}=-g\mu_{B} \frac{\mathbf{J}}{\hbar}$$

[^1]: In the context of electrons, this is a fair approximation. Even in classical descriptions, electrons move at [[Lorentz transformation|relativistic]] speeds around the nucleus.

[^2]: Technically it should be $-e$, but the sign doesn't matter: we can just make the electron orbit the other way and the sign disappears anyway, so we might as well ignoring from the start.

[^3]: Note that the inhomogeneity is obligatory, as since we assume that $\nabla \boldsymbol{\mu}=0$ ($\boldsymbol{\mu}$ is a constant of the atom), the only term that can produce a nonzero force is $\nabla \mathbf{B}$. A uniform field as zero [[gradient]] everywhere, so no force would be felt.
