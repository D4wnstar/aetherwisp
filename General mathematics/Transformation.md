---
wiki-publish: true
aliases:
  - transform
---
A **transformation** or **transform** is a function $f$ that maps a [[set]] to itself. These functions are often seen in geometry and linear algebra or have geometric interpretations. For instance, a [[rotation]] is a transform. More generally, they can also be [[operator|operators]].
### Properties
Since transformations are functions, they inherit all the properties of functions. A particularly important case is continuous transformations. An example of a continuous transformation $\varphi$ is the [[rotation]]
$$\begin{pmatrix}
q_{1} \\
q_{2}
\end{pmatrix}\to \begin{pmatrix}
\cos \alpha & -\sin \alpha \\
\sin \alpha & \cos \alpha
\end{pmatrix}\begin{pmatrix}
q_{1} \\
q_{2}
\end{pmatrix}=\begin{pmatrix}
\varphi_{1}(q,\alpha) \\
\varphi_{2}(q,\alpha)
\end{pmatrix}$$
where $\alpha \in[-\pi,\pi[$. The derivative transformation $\psi$ is
$$\begin{pmatrix}
\dot{q}_{1} \\
\dot{q}_{2}
\end{pmatrix}\to\begin{pmatrix}
\cos \alpha & -\sin \alpha \\
\sin \alpha & \cos \alpha
\end{pmatrix}\begin{pmatrix}
\dot{q}_{1} \\
\dot{q}_{2}
\end{pmatrix}=\begin{pmatrix}
\psi_{1}(q,\dot{q},\alpha) \\
\psi_{2}(q,\dot{q},\alpha)
\end{pmatrix}$$

An example of a non-continuous transformation (called a discrete transformation) is
$$\begin{pmatrix}
q_{1} \\
q_{2}
\end{pmatrix}\to \begin{pmatrix}
\alpha q_{1} \\
\alpha q_{2}
\end{pmatrix}$$
where $\alpha=\pm 1$.