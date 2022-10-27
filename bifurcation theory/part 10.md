# [Stability and Lyapunov Theorem](https://en.wikipedia.org/wiki/Lyapunov_stability)

Def: x_0 equilibrium point of $\dot{x} = f(x)$ (*) is stable if for all $\epsilon > 0$, exists on $\delta_\epsilon > 0$ such that for all $x \in B(x_0, \delta_\epsilon)$ and$t \geq 0$, one has $\Phi_t(x) \in B(x_0, \epsilon)$

$x_0$ is said Asymptotically stable if it is stable and for all $x \in B_\delta(x_0)$, one has $\lim_{t \rightarrow \infty} \Phi_t(x) = x_0$

Remark : 
i) any sink for a linear system is asymptotically stable (and alos for a non linear system in regard of the Hartman-Grobman Theorem)

ii) any source and saddle equilibrium points are unstable

iii) x = Ax, x = $\begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}$ this is an exemple of a linear system which is stable but not asymptotically stable.

