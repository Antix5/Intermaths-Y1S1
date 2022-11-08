# [Stability and Lyapunov Theorem](https://en.wikipedia.org/wiki/Lyapunov_stability)

Def: x_0 equilibrium point of $\dot{x} = f(x)$ (*) is stable if for all $\epsilon > 0$, exists on $\delta_\epsilon > 0$ such that for all $x \in B(x_0, \delta_\epsilon)$ and$t \geq 0$, one has $\Phi_t(x) \in B(x_0, \epsilon)$

$x_0$ is said Asymptotically stable if it is stable and for all $x \in B_\delta(x_0)$, one has $\lim_{t \rightarrow \infty} \Phi_t(x) = x_0$

Remark : 
i) any sink for a linear system is asymptotically stable (and alos for a non linear system in regard of the Hartman-Grobman Theorem)

ii) any source and saddle equilibrium points are unstable

iii) x = Ax, x = $\begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}$ this is an exemple of a linear system which is stable but not asymptotically stable.

Theorem : if $x_0$ is a sink for $\dot{x} = f(x)$ and $Re(\lambda_j) \leq 0$ for all $\lambda_j$ of the eigenvalues 

$A = Df(x_0)$, then given epsilon >0, there exists delta_elpsilon such that for all x in ball $B(\delta_\epsilon, x_0)$, one has | pfi_t

=> Asymptotic stability (cannot follow)

Theroem: if x_0 is a stable equilibrium for $x' = f(x)$, the no eigenvalues of $Df(x_0)$ have positiove real parts

Lyapunov Theorem : 
$\Omega \subset \mathbb{R}^n$ is an open set
$\dot{V} = \frac{d}{dt} V(x(t))_{t=0} $,
 x(t) is a the solution
 $$
 \dot{x} = f(x) \quad, x(0) = x_0$$
 $$ \dot{V} = DV(x_0) . f(x_0)$$

 Theorem (Lyapunov)

 $Omega$ open set $x_0$ equilibirum point for $\dot{x} = f(x)$, $f \in C^1(\Omega)$
 Suppose that there exists on
 $$ V: \Omega \to \mathbb{R}$$ such that

 i) $v(x_0) = 0$
 ii) $V(x) >0$ for all x not equal to $x_0$

 iii) if V'(x) <= 0 for all , x in Omega
 
 b) if V'(x)<0 for all x in R, x!= x_0
 
 => x_0 is Asymptotically stable

 c) if V'(x) >0 for all x in R, x!= x_0

 Exemple of V in R^2

 V'(x,y) = C_1(x-x0) ^2  + C_2(y-y0) ^2

 alpha, beta are even and positive and C_1 and C_2 > 0

 (V satisfying i, ii) is called a Lyapunov function)

 Remark : if V'(x) = 0 => d/dt V( phi_t(x)) = 0

=> V( phi_t(x)) = C > 0

S = {x in Omega | V(x) = c}


Exemple :

x' = -2y + yz
y' = y -xz
z' = xy

non linear

0,0,0 is an equilibrium point

When we compute the jacobian, we have

$$
Df(0) =
\begin{pmatrix}
0 & -2 &0 \\
-1 & 0 & 0
\\ 0 & 0 & 0 \end{pmatrix}
$$

V(x,y,z)  C_1 x^2 + C_2 y^2 + C_3 z^2

long lyapunov dot product (to look online)



