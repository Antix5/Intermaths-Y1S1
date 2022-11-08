Th (Bendixon) either every neiborhood of $\bar{0}$ contians a closed curve or $\exists$ trajectories approching $\bar{0}$ as $t \rightarrow \pm \infty$

Th. Suppose that P, Q are analytic, Taylor expensions of P and Q begin with unic-degree terms $P_m(x,y)$ and $Q_m(x,y)$, $m\geq1$.

Then any trajectories of (1) which approach $\bar{0}$ as $t \rightarrow \pm \infty$ or it tends to $\bar{0}$ in a definite direction $\theta = \theta_0$ as $t \rightarrow \pm \infty$.

If $x.Q_m(x,y) - y.P_m(x,y) \ne 0$ then all such $\theta_0$ satisfies $cos(\theta).Q_m(cos(\theta),sin(\theta)) - sin(\theta).P_m(cos(\theta),sin(\theta)) = 0$ (4)
Furthermore, if our trajectories spirals towards $\bar{0}$ as $t \rightarrow + \infty$ then all trajectoirs spirals towards $\bar{0}$ as $t \rightarrow + \infty$.

Corollary, If $P_1(x,y) = ax + by$ and $Q_1(x,y) = cx + dy$ then (4)

$$
cos(\theta)(c cos(\theta) + d sin(\theta)) - sin(\theta)(a cos(\theta) + b sin(\theta)) = 0\\
f.sin^2(\theta) + (a-d).sin(\theta)cos(\theta) - c.cos^2(\theta) = 0
$$

for $cos(\theta) \ne 0$:

$$
f.tan^2(\theta) + (a-d).tan(\theta) - c = 0 \quad (5)
$$

$\exists$ at most 2 solutions $\theta \in (-\frac{\pi}{2},\frac{\pi}{2})$.

Finding solutions of (5) is equivalent to finding eigenvalues
of the matrix :

$$A=
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$

Th suppose that $t\in \mathcal{C}^1(E)$, $\bar{0} \in E$, $t(0)=0$. If $\bar{0}$ is hyperbolic at point then  $\bar{0}$ is saddle $\Leftrightarrow$  $\bar{0}$ is saddle for the linear system with $A=Df( \bar{0})$

moreover, direction $\theta_j$ along wich the supermatrices $\Gamma_j$ approach $\bar{0}$ are solution of (5) 

Exemple :

$$
\begin{cases}
\dot{x} = x + 2y + x^2 - y^2 \\
\dot{y} = 5x +4y - 2xy
\end{cases}
$$

$$
A = Df(\bar{0}) =
\begin{pmatrix}
1 & 2 \\
5 & 4
\end{pmatrix}
$$

The eigenvalues of $A$ are $\lambda_1 = -1$ and $\lambda_2 = 6$ and eigenvectors are $v_1 = \begin{pmatrix} 1 \\ -1 \end{pmatrix}$ and $v_2 = \begin{pmatrix} 2 \\ 5 \end{pmatrix}$







