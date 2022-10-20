# Part 7 : **Non-linear** systems :
$\dot{x} = f(x)$
$f : \mathbb{R}^n \to \mathbb{R}^n$
**basic results about existence and uniqueness of solutions**

$$(1)
\begin{cases}
\dot{x_1} = f_1(x_1, \dots, x_n)\\
\vdots\\
\dot{x_n} = f_n(x_1, \dots, x_n)
\end{cases}
$$

Exemple :

$$
\begin{cases}
\dot{x_1} = x_1x_2 \\
\dot{x_2} = x_2
\end{cases}
$$

Let's solve it

$$
\begin{cases}
\dot{x_1} = x_1x_2 \\
\dot{x_2} = x_2
\end{cases}
\Rightarrow
\begin{cases}
\dot{x_1} = x_1x_2 \\
x_2 = Ce^{t}
\end{cases}
\Rightarrow
\begin{cases}
\dot{x_1} = x_1Ce^{t} \\
x_2 = Ce^{t}
\end{cases}
$$

We can solve it by integrating the first equation

$$
\begin{cases}
\frac{\dot{x_1}}{x_1} = Ce^{t} \\
x_2 = Ce^{t}
\end{cases}
$$
$$
\begin{cases}
\int \frac{\dot{x_1}}{x_1} = \int Ce^{t} \\
x_2 = Ce^{t}
\end{cases}
$$
...

Remark : if f is defined for all $x \in \mathbb{R}^n$ then, the solution may become unbounded at some finite point t.

Exemple :

$$
\begin{cases}
\dot{x} = x^2 \\
x(0) = 1
\end{cases}
$$

$x(t)=\frac{1}{1-t}$ is defined on $]1, \infty[$, 

Def : Jacobian matrix of f at x

$$
Df(x)=J_f(x) = \begin{pmatrix}
\frac{\partial f_1}{\partial x_1} & \dots & \frac{\partial f_1}{\partial x_n}\\
\vdots & \ddots & \vdots\\
\frac{\partial f_n}{\partial x_1} & \dots & \frac{\partial f_n}{\partial x_n}
\end{pmatrix}
$$

Exemple : 
$$f(x)=f(x_1, x_2)=\begin{pmatrix} x_1x_2 \\ x_2 \end{pmatrix}$$

$$Df(x)=\begin{pmatrix} x_2 & x_1 \\ 0 & 1 \end{pmatrix}$$

$$Df(0)=\begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix}$$

Theorem - The fundamental existence and uniqueness theorem

Let $f \in C^1| E$ Then $\forall x_0 \in E$ there exists a unique solution $x \in C^1([0, \infty), E)$

$$
\begin{cases}
\dot{x_1} = f(x) \; (2) \\
x(0) = x_0
\end{cases}
$$

has a unique solution on the interval [-a, a]

Sketch the proof :

$$
x_0 \in E \Rightarrow \text{ for some } b > 0, N={x | ||x-x_0|| \leq b} \subset E \\
f \in C^1|E \Rightarrow ||f(x) - f(y)|| \leq L .||x-y|| \; \forall x, y \in E \\
M = max ||f(x) ||
$$

Let us take a $a < min(\frac{b}{M},\frac{1}{L})$
(2) is equivalent to an integral equation $x(t) = x_0 + \int_0^t f(x(s)) ds$

Introduce the iterating procedure (successive approximations of the solution) :

$$
x_0(t) \equiv x_0 \\
x_{n+1}(t) = x_0 + \int_0^t f(x_n(s)) ds
$$

(Also known as Picard's method)[https://en.wikipedia.org/wiki/Picard–Lindelöf_theorem]

Solution of (2) is unique : 
Indeed, if $x_1$ and $x_2$ are solution of (2) then

$$
x_1(t) - x_2(t) = \int_0^t (x_1(s) - x_2(s)) ds \\
|| x_1(t) - x_2(t) || \leq \int_0^t ||x_1(s) - x_2(s)|| ds \\
$$

and $\forall t \in [-a,a]$

$$
|| x_1(t) - x_2(t) || \leq L \int_0^t ||x_1(s) - x_2(s)|| ds
$$


$$ 1 \leq La \Rightarrow \text{contradiction}$$

Exemple (increasin of b does not imply an increase in a)
but the approximation converge to $\bar{x}=0\text{ only on }[-a,a]$

$$
\begin{cases}
\dot{x_1} = x_1x_2 ,\; x_1(0) = 0 ,\; x_1(t) = 0 \\
\dot{x_2} = x_2 ,\; x_2(0) = 0 ,\; x_2(t) = 0
\end{cases}
$$

Th (Dependence on initial Date)
Let $f \in C^1(E), x_0 \in E$ 
Then $ \exists a > 0, \exists \delta > 0$ such that $\forall \xi \in N_{\delta}(x_0) = \{x \in E | ||x-x_0|| \leq \delta \}$
The probelm 
$$
\begin{cases}
\dot{x_1} = f(x) \\
x(0) = x_0
\end{cases}
$$

has a unique solution $x = x(t,\xi)$ on $[-a,a]$, $ x \in c^1(G),$ where $G=[-a,a] \times N_{\delta}(x_0)$

moreover, the matrix

$$
\Psi(t,\xi) = \frac{\partial x(t,\xi)}{\partial \xi}
$$

satisfies the system

$$
\begin{cases}
\frac{d}{dt} \Psi(t,\xi) = Df(x(t,\xi)) \Psi(t,\xi) \\
\Psi(0,\xi) = I
\end{cases}
$$

where $I$ is the identity matrix

Remark : If $x_0$ is a, equilibrium point of (1), i.e, $f(x_0)=0$, then $x(t,x_0)=x_0$ for all t

So, $\Psi(t,x_0)= \frac{\partial x(t,x_0)}{\partial x_0}$

Exemple : 

$$
\begin{cases}
\dot{x} = Ax \\
x(0) = \xi
\end{cases}
\Rightarrow
x(t, \xi) = e^{At}\xi
\Rightarrow
\Psi(t, \xi) = e^{At}
$$

Exemple : 

$$
\begin{cases}
\dot{x_1} = x_1x_2 \\
\dot{x_2} = x_2 \\
x_1(0) = \xi_1 \\
x_2(0) = \xi_2
\end{cases}
\Rightarrow
x(t,\xi) = \text{(solution - figure too complicated to do in latex)} \\
$$

$$
\Psi(t,\xi) = \frac{\partial x(t,\xi)}{\partial \xi} = \begin{pmatrix} \frac{\partial x_1(t,\xi)}{\partial \xi_1} & \frac{\partial x_1(t,\xi)}{\partial \xi_2} \\ \frac{\partial x_2(t,\xi)}{\partial \xi_1} & \frac{\partial x_2(t,\xi)}{\partial \xi_2} \end{pmatrix}
$$

Let consider $\dot{x} = f(x)$, $x(0) = x_0$

Th (Dependence on parameters)
Let E be an open set in $R^{n+m}$, $(x_0, \mu_0) \in E$,

$$
f \in C^1(E), \text{then } \exists a > 0, \exists \delta > 0 \text{ such that } \forall \xi \in N_{\delta}(x_0) \text{ and }\\\forall \mu \in N_{\delta}(\mu_0) \text{ the problem }
$$

$$
\begin{cases}
\dot{x} = f(x,\mu) \\
x(0) = \xi
\end{cases}
$$

has a unique solution $x=x(t, \xi, \mu)$ on [-a, a], and $x \in \mathcal{C}^1(G)$, where $G=[-a,a] \times N_{\delta}(x_0) \times N_{\delta}(\mu_0)$

Th. Let $f \in C^1(E)$, $x_0 \in E$.

Then, there exits a maximum interval 
$I(x_0) = ]\alpha, \beta[$ of existence of the solution of the problem (2), i.E, if $y(t), t \in J$ is a solution of (2), then J is included in I(x_0) and $x(t) \equiv y(t)$ on J

Furthermore if $ \beta$ is finite and there exits $lim_{t\rightarrow\beta -} x(t) $

then $x_2 \in \partial E$

On the other hand, if there exists $lim_{t\rightarrow\beta -} x(t)$,
then $\beta$ is infinite

Gramwall Lemma :

Suppose that x(t) is a continuous function, $x(t) \leq 0$

$$ \forall t \in [0,T], x(t) \leq C + \int_0^t h(s)x(s) ds, \text{ where } 0 \leq h \text{ is given} \\
\text{then} \\
\forall t \in [0,T], x(t) \leq C e^{-\int_0^t h(s) ds}
$$

Proof :

$$
\text{Define } u(t)=C + \int_0^t h(s)x(s) ds.
\text{ Then } u \in C^1([0,T]), u(0)=C,\\
u'(t) = h(t)x(t) \leq h(t)u(t) | . e^{-\int_0^t h(s) ds} \\	
u(t) e^{-\int_0^t h(s) ds} - C e^{-\int_0^t h(s) ds} \leq \int_0^t h(s) x(s) e^{-\int_0^t h(s) ds} ds \\
$$

(check the proof)

Th. Global existance for syst. with right hand part of linear growth)

Suppose that for $\dot{x} = f(x)$, $f \in C^1(\mathbb{R}^n)$,

$$
|| f(x) || \leq A + B||X||, \forall x \in \mathbb{R}^n, A>=0, B>=0
$$
Then every solution exits on (-\infty, \infty)

Proof:

Let $T>0$ be arbitrary.
For solution of $ \begin{cases} \dot{x} = f(x) \\ x(0) = x_0 \end{cases}$, we have :

$$
x(t) = x_0 + \int_0^t f(x(s)) ds
$$

Then

$$
||x(t)|| \leq ||x_0|| + \int_0^t ||f(x(s))|| ds \leq ||x_0|| + \int_0^t (A + B||x(s)||) ds \\
\leq ||x_0|| + A.T + \int_0^t B||x(s)|| ds
$$

Due to the Gramwall Lemma, we have :

$$
||x(t)|| (||x_0|| + A.T).e^{-B.T} 
$$

Ex:

$$
\begin{cases}
\dot{x_1} = sin(x_1^2 + x_2^2) \\
\dot{x_2} = x_1 + x_2 \\
\end{cases}
$$

every solution exits on (-\infty, \infty)

$$
f(x) =
\begin{pmatrix}
sin(x_1^2 + x_2^2) \\
x_1 + x_2
\end{pmatrix}
$$

$$
||f(x)|| = \sqrt{sin^2(x_1^2 + x_2^2) + (x_1 + x_2)^2} \leq 1 + \sqrt{2}\sqrt{x_1^2 + x_2^2}\\
= 1 + \sqrt{2}||x||
$$

Corollary, All solutions of the systm

$$
\dot{x} = \frac{f(x)}{1+||f(x)||}
$$

exists on $(-\infty, \infty)$

Proof:

$$
||\frac{f(x)}{1+||f(x)||}|| \leq 1
$$

Def : For solution $x(t,x_0), t \in I(x_0)$ the set of points $\{x(t,x_0) : t \in I(x_0)\}$ is called the trajectory of the solution through the point $x_0$


Ex: 

$$
\begin{cases}
\dot{x} = x^2 \\
x(0) = 1
\end{cases}, \;
x(t) = \frac{1}{1-t}, t \in (-\infty, 1)
$$

The phase space is in $\mathbb{R}$ 

$$
\begin{cases}
\dot{x} = \frac{x^2}{1+x^2} \\
x(0) = 1
\end{cases}, \;
x(t) = \frac{1}{2}(t+\sqrt{t^2+4}), t \in (-\infty, \infty)
$$
T
h. for $f \in C^1(\mathbb{R}^n)$, systems

$$
(1) \quad \dot{x} = f(x) \text{ and } (2) \quad \dot{x} = \frac{f(x)}{1+||f(x)||}
$$

have the same trajectories with the same direction along the trajectories ( (1) and (2) are topologically equivalent)

Sketch of the proof :

Let x(t) be the solution of (1), $ t \in I(x_0)=(\alpha, \beta)$

Let us introduce a new variable

$$
\tau = \int_0^t ( 1 + ||f(x(s))|| ) ds
$$

$\tau(0)=0$, $\tau(t) \neq 0$ $\tau:(\alpha, \beta) \rightarrow \mathbb{R} \Rightarrow \exists t = t(\tau) = 0$

$$
\frac{dy}{d\tau} = \frac{f(x(t))}{1+||f(x(t))||}
$$

(to check)

Once this rescaling has been made, it follows that 

$$\forall x_0 \in E ,I(x_0) = (-\infty, +\infty)
$$
So in the sequel, we assume that for the system

$$
\dot{x} = f{x} \quad (1)
$$

for every $x_0$ we have I(x_0) = (-\infty, +\infty)

Let us denote $\phi_t(x_0) = \phi(t, x_0) = x(t, x_0)$ solution of (1) with $x(0) = x_0$

(He switched the page, could not copy 😡)

Th (proprieties of the flow)

1) $\phi \in C^1(\mathbb{R} \times E)$
2) $\forall t,x \quad \forall x_0 \quad \phi_{t+s} (x_0 = \phi_t(\phi_s(x_0))$
   
Proof:

1) We know that $(t, \xi) \rightarrow X|(t, \xi)$ belongs to $C^1 \Rightarrow \Phi \in C^1(R \times E)$
2) let us fix s > 0 and x(t) = x(t, x_0)
consider $x_s(0) = x(s)$

$$
\frac{d}{dt} x_s(t) = f(x_s(t)) = f(x(s+t)) = f(X_s(t))
$$

Due to the uniqueness, we get :

$$
x_s(t) = \phi_t(x(s))
$$

(really need to be check, he jumpted to the next page)

Def: A set $S \subset E$ is said to be invariant with respect to $\Phi_t$

it

$$
\Phi_t(S) \subset S , \forall t \in \mathbb{R} ( \Rightarrow \Phi_t(S) = S \text{ for all } t \in \mathbb{R})
$$

S is called positively (negatively) invariant with tespect to $\Phi_t$ if

$$
\Phi_t(S) \subset S , \forall t >= 0 ( \Phi_t(S) \subset S, \forall t \leq 0)
$$

Exemple

$$
\begin{cases}
\dot{x_1} = -x_1 \\
\dot{x_2} = x_1^2 + x_2
\end{cases}
$$

$$
x_1 = x_1^0 e^{-t} \;, \\
\dot{x_2}=x_2 + (x_1^0)^2 e^{-2t}
$$

Variation of the constant

$$
x_2(t)= x_2^0 e^{t} + e^t \int_0^t e^{-s} (x_1^0)^2 e^{-2s} ds \\
x_2(t)=x_2^0 e^{t} + \frac{(x_1^0)^2}{3} (e^t - e^{-2t})
$$

So, for every $c = \begin{pmatrix} c_1 \\ c_2 \end{pmatrix}$

$$
\Phi(t,x) = \begin{pmatrix} c_1 e^{-t} \\ c_2 e^{t} + \frac{(c_1)^2}{3} (e^t - e^{-2t}) \end{pmatrix}
$$

Consider the set $$S= \{x \in R^2 | x_2 = \frac{x_1^2}{3} \}$$

(missing some part, look at the lecture to get it, just simplifications)


$$
\Phi_t = \begin{pmatrix} c_1 e^{-t} \\ \frac{(c_1)^2}{3} (e^t - e^{-2t}) \end{pmatrix}
$$

So, for $\forall t, \forall x \in S \; \Phi(t,x) \in S \Rightarrow S \text{ is invariant}$

Consider U = $\{x \in R^2 | x_1 = 0\}$

$$
\forall c = \begin{pmatrix} c_1 \\ c_2 \end{pmatrix} \; \Phi_t = \begin{pmatrix} 0 \\ c_2 e^{t} \end{pmatrix} \in U \Rightarrow U \text{ isinvariant}
$$

It is easy to see that :
$$
\forall c \in S \; \Phi_t(c) \rightarrow \bar{0} \text{ as } t \rightarrow \infty ( \Rightarrow S \text{ is a stable manifold})\\
\forall c \in U \; \Phi_t(c) \rightarrow \bar{0} \text{ as } t \rightarrow -\infty ( \Rightarrow U \text{ is an unstable manifold})
$$

<p style="text-align: center; text-decoration: underline;">Linearisation</p>

$$
\dot{x}=f(x) \quad (1)
$$

Def: A point $x_0$ is cammed an equilibrium point (or critical point) if f(x_0)=0
For the corresponding flow $\Phi_t$ we have $\Phi_t(x_0) = x_0$ for all t, so $x_0$ is a fixed point for $\Phi_t$

Let is denote $A=Df(x_0)$

The linear system

$$
\dot{x} = Ax \quad (2)
$$
is called the linearisation (or linearised system) for (1)

Def : An equilibrium point x_0 is called hyperbolic if for all eigenvalues of A $\lambda(A)$ we have : $Re(\lambda) \neq 0$

Remark

Assume that $x_0 = 0, f(0)=0$. Then, by Taylor's theorem, we have : 

$$
f(x) = Df(0) x + \frac{1}{2}D^2f(0)(x,x) + \dots
$$

Def: An equilibrium point $x_0$ is called a sink if for all eigenvalues of A $\lambda(A)$ we have : $Re(\lambda) < 0$

Def: An equilibrium point $x_0$ is called a source if for all eigenvalues of A $\lambda(A)$ we have : $Re(\lambda) > 0$

Def: An equilibrium point $x_0$ is called a saddle if $x_0$ is hyperbolic and not a sink or a source

Example:

$$
\begin{cases}
\dot{x_1} = -x_1 \\
\dot{x_2} = x_1^2 + x_2
\end{cases}
f(x) = \begin{pmatrix} -x_1 \\ x_1^2 + x_2 \end{pmatrix}\\
Df(x) = \begin{pmatrix} -1 & 0 \\ 2x_1 & 1 \end{pmatrix}\\
A = Df(0) = \begin{pmatrix} -1 & 0 \\ 0 & 1 \end{pmatrix}
$$

The eigenvalues of A are $\lambda_1 = -1$ and $\lambda_2 = 1$ we therefore have a saddle point at $x_0 = \bar{0}$

Example:

$$
\begin{cases}
\dot{x_1} = x_1^2 - x_2^2 - 1 \\
\dot{x_2} = 2x_2
\end{cases}
\text{ Eg. points: }
\begin{cases}
x_1^2 - x_2^2 - 1 = 0 \\
2x_2 = 0
\end{cases}
$$

$$
x_0^{(1)} = \begin{pmatrix} 1 \\ 0 \end{pmatrix} \text{ and } x_0^{(2)} = \begin{pmatrix} -1 \\ 0 \end{pmatrix}
$$

$$
Df(x_0^{(1)}) = \begin{pmatrix} 2 & 0 \\ 0 & 2 \end{pmatrix} \text{ and } Df(x_0^{(2)}) = \begin{pmatrix} -2 & 0 \\ 0 & 2 \end{pmatrix}
$$

So the first one isa source and the second one a saddle point.

Remark : We'll see later (the Hartman-Grobman theorem) that is $x_0$ is a hyperbolic equilibrium point, then the local behaviour of (1) is topologically equivalent to the local behaviour of (2), i.e., $ \exists \text{ a neighbourhood } N(x_0) \text{ and } N(\bar{0})$
There exists a continuous one to one mapping $H : N(x_0) \rightarrow N(\bar{0})$ which transforms trajectories of (1) into trajectories of (2) and vice versa.

Example : 

$$
\begin{cases}
\dot{x_1} = -x_1 \\
\dot{x_2} = x_1^2 + x_2
\end{cases}
A = Df(0) = \begin{pmatrix} -1 & 0 \\ 0 & 1 \end{pmatrix}
$$ \dot{x} = Ax
$$

Consider the map $H : R^2 \rightarrow R^2$ defined by $H(x) = \begin{pmatrix} x_1 \\ x_2 + \frac{x_1^2}{3}\end{pmatrix}$

$$
H: R^2 \rightarrow R^2 \text{ is a bijection}\\
\Leftrightarrow \\
\forall y \in R^2 \; \exists! x \in R^2 : H(x)=y
$$

$$
y=\begin{pmatrix} y_1 \\ y_2 \end{pmatrix} \Rightarrow x = \begin{pmatrix} x_1 \\ x_2 + \frac{x_1^2}{3}\end{pmatrix}
$$

For $y=H(x)$, where $x=x|H = \begin{pmatrix} x_1|H \\ x_2|H \end{pmatrix}$ we have :

$$
\dot{y}=\begin{pmatrix}
\dot{x_1} \\
\dot{x_2} + \frac{2}{3}x_1 \dot{x_1}
\end{pmatrix} = \begin{pmatrix}
-x_1 \\
x_1^2 + x_2 - \frac{2}{3}x_1^2
\end{pmatrix} = \begin{pmatrix}
-x_1 \\
x_1^2 + x_2 - \frac{2}{3}x_1^2
\end{pmatrix} = \begin{pmatrix}
-y_1 \\
y_2
\end{pmatrix}
=A \begin{pmatrix}
y_1 \\
y_2
\end{pmatrix}
$$

A linear system















