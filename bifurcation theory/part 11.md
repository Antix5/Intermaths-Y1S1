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

Th.
Suppose that 0 is a center for linear systems with A=Df(0).

Then 0 is either center, focus or center focus for the non linear system (1).

(see proof on the recording)

Remark!!: A center focus cannot accure in analytic systems.
So if f is analytic, 0 is acenter for a linear sysyte
then 0 is other center or focus for non linear system

### How to distinguis a center from focus
The first way: Lyaupunov functions approach

Exercices on the video

The second way: Write the system in polar coordinate and try to investigate the behavior of r and $\theta$ as $t \rightarrow \infty$

The third way: Look for symetric properties in respect to axies or 1 axis

Th: Let $f \in C^1(E)$, $\bar{0} \in E$ f(0) = 0, 
symetric wrt one of the axis 

Exemple:

$$
\begin{cases}
\dot{x} = -xy-y \\
\dot{y} = x^2+x
\end{cases}
$$

After change of variable, the system is symetric (wrt x axis) 