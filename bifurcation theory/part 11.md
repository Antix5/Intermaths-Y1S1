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

Now we consider the case A not equal to 0

Assume that the Taylor exepansion of P and Q begin with m.th degree terms $P_m(x,y)$ and $Q_m(x,y)$
Consider
$$
g(\theta) = cos(\theta).Q_m(cos(\theta),sin(\theta)) - sin(\theta).P_m(cos(\theta),sin(\theta))
$$

Assume g diff from 0.Then, the equation $g(\theta) = 0$ has at most 2(m+1) roots $\theta = \theta_U$ which define derection along wich trajectories of (1) may appraoch $\bar{0}$.
Lines, corresponding to these directions divide neiborhood of $\bar{0}$ into finite number of regions called **sectors**.

Def: A sector which is topologically equivalent to

[image that I cannot drow in markdown]

it's called an hyperbolic sector.

[other image that I cannot draw]

parabolic sector

[other image that I cannot draw]

a) if m odd , am>0 , then 0 is unstable
b) if m odd, am<0, then 0 is stable
c) if m even, am>0, then 0 is a saddle node

$$
\begin{cases}
\dot{x} = y \\
\dot{y} = a_n x^k (1 + h(x)) + b_n x^n y (1 + g(y)) + y^2 R(x,y) 
\end{cases}
$$

$k \geq 2$, $a_k \ne 0$ and $n \geq 1$

Th. Let k= 2m, m>=1 Then 1) 0 is a casp if $b_n=0$ and also if $b_n \ne 0$ and $n \geq m$ 2) 0 is a saddle if $b_n \ne 0$ and $n < m$

Th Let k = 2m +& , m>=1 $\lambda := b_n^2 + 4(m+1) a_k$. Then if $a_k > 0$ then o is a saddle

If $a_k < 0$ then 0 is 1) focus or center if $b_n = 0$ and also if $b_n \ne 0$ and $n > m$ or if n=m and $\lambda <
 0$

 2) node if $b_n \ne 0$ , n is even and n < m and also if $b_n \ne 0$ , n is even and n = m and $\lambda \geq 0$

3) critical point with elliptic domain if b_n \ne 0 , n is odd and n < m and also if $b_n \ne 0$ , n is odd and n = m and $\lambda \geq 0$

Remark: If A=0 then the classification of possible phase portraits is sties (???) possible but too complicated

Central Manifold Theorem

A = Df(0) has c engivalues with real part $\lambda_1 = 0$, s engivalues with real part $\lambda_2 < 0$ 
(I missed it)

Too many things to write down, see the recording