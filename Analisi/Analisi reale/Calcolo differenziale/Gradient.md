The **gradient** $\nabla f$ of a [[Differenziabilità|differentiable]] function $f$ is the [[Campo vettoriale|vector field]] whose values describe the direction and magnitude of fastest increase at any given point in $f$'s domain. In a generic coordinate system with [[base|basis]] vectors $(x_{1},x_{2},\ldots,x_{n})$, the gradient can be written as the column vector whose components are the partial derivatives in that component:
$$\nabla f=\begin{pmatrix}
\frac{ \partial f }{ \partial x_{1} } \\
\frac{ \partial f }{ \partial x_{2} } \\
\vdots \\
\frac{ \partial f }{ \partial x_{n} } \\
\end{pmatrix}$$
This is related to the [[total differential]] $df$, as they are [[transposition|transpose]] (and thus [[spazio duale|dual]]) to each other:
$$df=(\nabla f)^{T}$$
In [[Notazione braket|braket notation]], they are the ket and bra of the same vector:
$$\nabla f=\ket{\partial_{x} f},\quad df=\bra{\partial_{x}f} $$
### In curvilinear coordinates
The most generic form of the gradient is given in curvilinear coordinates. Consider a three-dimensional system with coordinates $u$, $v$ and $w$. If you move an object from point $(u,v,w)$ to point $(u+du,v+dv,w+dw)$ in an infinitesimal motion, a scalar function $t(u,v,w)$ changes by an amount
$$dt=\nabla t\cdot d\mathbf{r}=(\nabla t)_{u}f\ du+(\nabla t)_{v}g\ dv+(\nabla t)_{w}h\ dw$$
so long as we define
$$(\nabla t)_{u}\equiv \frac{1}{f}\frac{ \partial t }{ \partial u } ,\quad (\nabla t)_{v}\equiv \frac{1}{g}\frac{ \partial t }{ \partial v } ,\quad(\nabla t)_{w}\equiv \frac{1}{h}\frac{ \partial t }{ \partial w } $$
where $f$, $g$ and $h$ are functions of position that are specific to a given coordinate system. The gradient of $t$ then is
$$\nabla t\equiv \frac{1}{f}\frac{ \partial t }{ \partial u } \mathbf{\hat{u}}+ \frac{1}{g}\frac{ \partial t }{ \partial v } \mathbf{\hat{v}}+ \frac{1}{h}\frac{ \partial t }{ \partial w } \mathbf{\hat{w}}$$
