Def: A closed invariant set $A \subset \Omega$ is called attracting if there is some neiborhood U of A such that $\forall x \in U, \Phi(t,x) \in U \forall t \geq 0$.

An attractor of $\dot{x} = f(x)$ is an attracting set which contains a dense (in A) orbit

Remarks : 

1) Any equilibrium point $x_0$ is his own $\alpha-$ and $\omega-$limit set.

2) If a trajectory $\Gamma$ has a unique $\omega-$limit point $x_0$, then $x_0$ is an equilibrium point of $\dot{x} = f(x)$.

3) a stable node or a stable focus are the $\omega-$limit sets of all trajectories in some neighborhood of the equilibrium point.

Furthermore, a stable node or a stable focus are attractors for $\dot{x} = f(x)$.

4) A saddle point $x_0$ of a planar system is the $\omega-$limit set of a separatrics and of $x_0$ itself in a neighborhood of $x_0$.

A cycle $\Gamma$ is stable if $\forall \epsilon >0$ there exits a neiborhood of $\Gamma \;, U(\Gamma)$ such that , $\forall x \in U(\Gamma)$ we have

$d(\Gamma^+_x, \Gamma) < \epsilon$

A cycle is called unstable if it is not stable.
A cycle $\Gamma$ is called asymptotically stable if it is stable and $\forall x \in U(\Gamma)$ we have 

$$\lim_{t \to \infty} d(\Gamma^+_x, \Gamma) = 0$$ (to check)

PERIOD :
$$ \dot{x} = f(x) $$
cycles of this system correspond to periodic solutions.

$\Phi(t,x)$defines closes solution curves

$$\Leftrightarrow$$

The minimal T for which thsi equlity holds is called the PERIOD of the periodic orbit.

$$T = 2\pi \rightarrow \text{period}$$

Example : Hamiltonian sysytem

$$
\begin{cases}
\dot{x} = y \\
\dot{y} = x+x^2
\end{cases} \quad \text{(Newtonian System)}
$$

$$
\text{Hamiltonian} = H(x,y) = \frac{1}{2}y^2 - \frac{1}{2}x^2 - \frac{1}{3}x^3
$$

The equilibrium points are $(0,0)$ and $(-1,0)$

$$Df(x,y) = \begin{pmatrix}
0 & 1 \\
1+2x & 0
\end{pmatrix}$$

$$Df(0,0) = \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix} \quad \text{it's a saddle}$$

$$Df(-1,0) = \begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix} \quad \text{it's a center (because it's an hamiltonian)}$$