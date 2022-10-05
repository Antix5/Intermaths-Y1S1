### Methods of the characterisitcs - Part 1 (1st order)

The goal of this method is to **transform a PDE** into a **system of ODEs**. This is done by finding the **characteristics of the PDE**. The characteristics are the curves that are tangent to the solution of the PDE.

Detailed explanation with the example of the transport equation:

$$
\begin{cases}
u_t + c u_x = 0 ; (x,t) \in \Reals \times \Reals^+ \\
u(x, 0) = u_0(x) ; x \in \Reals
\end{cases}
$$

To understand this method for the first order we need to study the general case. We are looking for the function $u(x,t)$ that satisfies the PDE.

$$
\dfrac{du}{ds}(x(s), t(s)) = \dfrac{\partial u}{\partial t}\dfrac{dx}{ds} + \dfrac{\partial u}{\partial x}\dfrac{dt}{ds} = 0
$$

($\dfrac{dx}{ds}$, $\dfrac{dt}{ds}$) is the tangent vectors to the curve $u(x(s), t(s))$

This is clearly visible if we consider the above equation as a dot product between the **tangent vectors** and the **gradient of $u$**.

$$
\dfrac{dx}{ds} = \xi_x ; 
\dfrac{dt}{ds} = \xi_t
$$

$$
\begin{bmatrix}
\xi_x \\
\xi_t
\end{bmatrix}
\cdot
\begin{bmatrix}
\dfrac{\partial u}{\partial x} \\
\dfrac{\partial u}{\partial t}
\end{bmatrix}
= 0
$$

#### Defintion of the characteristic vector: 
**A characteristic vector is a vector that is tangent to the solution curve of the PDE.**

We can identify now identify $\xi_x$ and $\xi_t$ in the transport equation.


$$
\xi_x = \dfrac{\partial u}{\partial x} = c \\
\xi_t = \dfrac{\partial u}{\partial t} = 1
$$

We now have 3 ODEs that we can solve.

$$
\begin{cases}
\dfrac{dx}{ds} = c \\
\dfrac{dt}{ds} = 1 \\
\dfrac{du}{ds} = 0
\end{cases}
$$

$$
\Leftrightarrow
$$

$$\begin{cases}
x(s) = c s + x_0 \\
t(s) = s + t_0 \\
u(s) = u(0) = u_0(x_0)
\end{cases} $$

We now need to do some algebra to get the solution of the PDE.

$$
t_0 = 0 \\
therefore \; \\
t(s) = s \; and \; x(s) = c t + x_0
$$

We isolate $x_0$ to reinject it in the solution of the PDE.

$$
x_0 = x - ct
$$

We now have the solution of the PDE.

$$
u(x,t) = u_0(x - ct)
$$





