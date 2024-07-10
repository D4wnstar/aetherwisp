---
aliases:
  - insulator
---
A **dielectric** or **insulator** is a material in which all [[Electric charge|electric charges]] are attached to a specific [[Atomo|atom]] or [[molecule]] and cannot move far from it. There are no free charges.
### Behavior under an electric field
#### Atoms
The simplest possible dielectric is a single atom, with a positively charged [[Nucleo atomico|atomic nucleus]] and a negatively charged [[Elettrone|electron]] cloud surrounding it. When subject to an [[electric field]], the nucleus and electron cloud move in opposite direction, as one is attracted by the field and the other is repelled. With a strong enough field, the electrons can be ripped from the nucleus, thus [[ionizzazione|ionizing]] the atom, but for milder fields, a state of equilibrium is reached.

The force keeping the nucleus and cloud together balances the one applied by the external field. In this state, the geometric center of the electron cloud, which acts as a sort of charge equivalent of the [[center of mass]], does not coincide with the (approximately point-like) nucleus. As such, the positive and negative charges of the atom are not superimposed and this turns the atom into an [[electric dipole]], with a (tiny) [[electric dipole moment]] that is typically proportional to the strength of the external field. Such an atom (or molecule) is said to be **polarized** and the dipole moment is modeled as
$$\mathbf{p}=\alpha \mathbf{E}$$
where $\mathbf{E}$ is the field and $\alpha$ is an atom-specific constant called the [[atomic polarizability]].
#### Molecules
In the case of molecules, the situation is more complicated, as the geometry of a molecule makes more easily polarized from a certain direction. In the case of a linear molecule, such as $\text{CO}_{2}$, the polarizability is highest on the molecule's axis. This complicates the induced moment's formula due to having to consider the components parallel and perpendicular to the axis:
$$\mathbf{p}=\alpha_{\perp}\mathbf{E}_{\perp}+\alpha_{\parallel}\mathbf{E}_{\parallel}$$
This may make the moment not even in the same direction of the field. For completely asymmetrical molecules, the polarizability splits in nine different components, one for every combination of axes. The object containing these components is called the **polarizability tensor** and is applied to the electric field:
$$\begin{pmatrix}
p_{x} \\
p_{y} \\
p_{z}
\end{pmatrix}=\begin{pmatrix}
\alpha_{xx} & \alpha_{xy} & \alpha_{xz} \\
\alpha_{yx} & \alpha_{yy} & \alpha_{yz} \\
\alpha_{zx} & \alpha_{zy} & \alpha_{zz}
\end{pmatrix}\begin{pmatrix}
E_{x} \\
E_{y} \\
E_{z}
\end{pmatrix}$$

Some molecules are permanently polarized due to their geometry. These are called **polar molecules**. If a uniform field is applied, the force on the positive end of the molecule is $\mathbf{F}_{+}=q\mathbf{E}$ and cancels out the force of the negative end $\mathbf{F}_{-}=-q\mathbf{E}$ exactly. However, a moment of force is applied:
$$\mathbf{N}=(\mathbf{r}_{+}\times \mathbf{F}_{+})+(\mathbf{r}_{-}\times \mathbf{F}_{-})=\left( \frac{\mathbf{d}}{2}\times q\mathbf{E} \right)+\left( - \frac{\mathbf{d}}{2}\times (-q\mathbf{E}) \right)=q\mathbf{d}\times \mathbf{E}$$
where $\mathbf{d}$ is the distance from the center of the molecule. Clearly then, a dipole $\mathbf{p}$ in a uniform field experiences a moment of force
$$\mathbf{N}=\mathbf{p}\times \mathbf{E}$$
Notably, $\mathbf{N}$ is in such a direction as to make $\mathbf{p}$ line up *parallel* to $\mathbf{E}$, as for $\mathbf{N}$ to be zero, and hence stop the rotation, $\mathbf{p}$ must be parallel to $\mathbf{E}$. This means that the dipole will rotate until it points in the direction of the field.

If the field is nonuniform, $\mathbf{F}_{+}$ does not balance $\mathbf{F}_{-}$ and there will be a net force on the molecule (on top of the moment of force). This is uncommon, as since molecules are tiny, the variation of the field needs to be very important such that we can't ignore the variation even in the space of a molecule. That said, the formula is
$$\mathbf{F}=\Delta \mathbf{F}_{\pm}=q(\mathbf{E}_{+}-\mathbf{E}_{-})=q\Delta \mathbf{E}$$
If the dipole is tiny, we can approximate this for each axis as
$$\Delta E_{i}\equiv(\nabla E_{i})\cdot \mathbf{d}$$
where $i=x,y,z$. In vector terms
$$\Delta \mathbf{E}=(\mathbf{d}\cdot \nabla)\mathbf{E}$$
and therefore
$$\mathbf{F}=(\mathbf{p}\cdot \nabla)\mathbf{E}$$
and the moment of force therefore sums to the previous one to get
$$\mathbf{N}=\mathbf{p}\times \mathbf{E}+\mathbf{r}\times \mathbf{F}$$
