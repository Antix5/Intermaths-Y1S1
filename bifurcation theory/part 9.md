### [Hartman - Grobman Theorem](https://en.wikipedia.org/wiki/Hartman–Grobman_theorem)

Homeomorphism ?
$\rightarrow$ A continuous function $f: X \rightarrow Y$ is a homeomorphism if $f$ is bijective and $f^{-1}$ is continuous


$$i) \quad \dot{x} = f(x) \text{ and   ii) } \quad \dot{y} = f(y)$$

$t \in I \subset \mathbb{R}$, $x \in U, y \in V$


The flow of i) is $\mathcal{C}_t(x)$
The flow of ii) is $\mathcal{Y}_t(y)$

Def: We say tht the topologycal systems i) and ii) are topologically conjugate if there exitsts an homeomorphism $H:U \rightarrow V$ such that 

$$H(\mathcal{C}_t(x)) = \mathcal{\Psi}_t(H(x))$$

for all $x \in U$ and $t \in I$

Complicated graph , will write it after

Def: The flows $\phi_t: U \rightarrow U$ and $\psi_t: V \rightarrow V$ are topologically equivalent if there exists a homeomorphism $H: U \rightarrow V$ that maps orbits of $\phi$ onto orbits of $\psi$ __and__ preserves the direction by time , meaning that ther eis a map $\Tau: U \times I \rightarrow \mathbb{R}$ increasing with respect to the time t fpr each x, such that : 

$$H(\phi_{\tau (x,t)}(x)) = \phi_\tau(H(x))$$

Example : 

$$\dot{x} = -x \quad, \quad \dot{y} = -2y$$

$$ \phi_t(x) = e^{-t}x \quad, \quad \psi_t(y) = e^{-2t}y$$

We can show that these two linear systems are topologically conjugate by showing that there exists a homeomorphism $H: \mathbb{R} \rightarrow \mathbb{R}$ such that H is an homeomorphism and satisfies :

$$H(x e^{-t}) = e^{-2t}H(x)$$

$$H(x) = \begin{cases}
x^2 & \text{if } x \geq 0 \\
-x^2 & \text{if } x < 0 \end{cases}
$$

$$H^{-1}(x) = \begin{cases}
\sqrt{x} & \text{if } x \geq 0 \\
-\sqrt{-x} & \text{if } x < 0 \end{cases}
$$

for x > 0 : 

$$H(x e^{-t}) = x^2 e^{-2t} \\
H(x)e^{-2t} = x^2 e^{-2t} \\
$$

Topologically conjugate

Pictures I cannot do 

Hartman-Grobman Theorem
(Perco : author of the book)

$$ \dot{x} = f(x) \quad, 0 \in \Omega, f(0)=0$$

$f \in \mathcal{C}^1(\Omega)$, $ \Phi_t$ is the flow of $\dot{x} = f(x)$

Assume that o is an hyperbolic equilibrium point.

$$A = Df(0)$$

Then there exists an homeomorphism $H: \Omega \rightarrow \Omega$ such that :

$$H(\Phi_t(x)) = e^{At}H(x_0)$$

for all $t \in I(x_0) \text{ with } x_0 \in \Omega$ \\
$\dot{x} = f(x)$ and $\dot{x} = Ax$ are topologically conjugate

Remark : if $A=Df(0)$ and 0 is a saddle for 
$$ \dot{x} = Ax$$

then is a saddle for $$\dot{x} = f(x)$$

if 0 is a sink for $$\dot{x} = Ax$$

then is a sink for $$\dot{x} = f(x)$$

Theorem (Hartman 1960)

Def : [diffeomorphism](https://en.wikipedia.org/wiki/Diffeomorphism#:~:text=In%20mathematics%2C%20a%20diffeomorphism%20is,and%20its%20inverse%20are%20differentiable.)

$\Omega \subset \mathbb{R}^n$ is an open set
$\dot{x} = f(x)$, $f \in \mathcal{C}^1(\Omega)$, $f(0)=0$
and o is an hyperbolic equilibrium point. 

We'll suppose that A = Df(0) has all eigenvalues with negative real parts.

Then ther is a C^1-diffeomorphism $H: \Omega \rightarrow \Omega$ from the neiborhood of U of o to V open set contianing the origin such that for each $x \in U$ :


There is an open interval $I(x_0) \subset \mathbb{R}$ with $o \in I(x)$ such that

$$H(\Phi_t(x)) = e^{At}H(x_0)$$

for all $t \in I(x_0)$







