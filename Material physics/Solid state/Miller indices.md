---
wiki-publish: true
---
**Miller indices** are a conventional notation to describe [[plane|planes]] in a three-dimensional [[Bravais lattice]]. It is based off of the geometric principle that three points in space uniquely identify a plane.

There are two ways of defining Miller indices.

Given a lattice with primitive vectors $\mathbf{a}_{1},\mathbf{a}_{2},\mathbf{a}_{3}$, one can define three integers $h$, $k$ and $l$. Now $\mathbf{a}_{1}/h$, $\mathbf{a}_{2}/k$ and $\mathbf{a}_{3}/l$ identify three lattice points, which in turn identify a plane, called a **crystal plane**. These numbers are known as the Miller indices, and are conventionally denoted $(hkl)$. If any index is zero, then the point is "at infinity", which means that the plane never intersects the axis of the correlated primitive vector. That's the same as saying that the plane is parallel to that axis. For instance, if $h=0$, then the crystal plane would be parallel to $\mathbf{a}_{1}$.

Alternatively, we can use the [[reciprocal lattice]] vectors $\mathbf{b}_{1},\mathbf{b}_{2},\mathbf{b}_{3}$. In this case, the plane is defined by the *reciprocal* lattice points $h\mathbf{b}_{1}$, $k\mathbf{b}_{2}$ and $l\mathbf{b}_{3}$.

By convention, negative indices are written with a bar over the number instead. For instance, the indices $h=0$, $k=1$, $l=-1$ would be written $(01\bar{1})$ and not $(01-1)$.

Using the same indices, we can define a [[Vector space|vector]] $h\mathbf{a}_{1}+k\mathbf{a}_{2}+l\mathbf{a}_{3}$. This is known as a **crystal direction** and is denoted as $[hkl]$. It is, in general, not the normal vector to the plane's [[surface]] (the exception is for a cubic lattice).

:::image
![[Miller indices.svg]]
A collection of planes defined by Miller indices on a cubic lattice cell. By Felix Kling - Own work, CC BY 3.0, from [Wikipedia](https://commons.wikimedia.org/w/index.php?curid=12123337).
:::