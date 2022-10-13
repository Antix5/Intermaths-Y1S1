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
but the approximation converge to $\bar{x}=0 only on [-a,a]$

$$
\begin{cases}
\dot{x_1} = x_1x_2 ,\; x_1(0) = 0 ,\; x_1(t) = 0 \\
\dot{x_2} = x_2 ,\; x_2(0) = 0 ,\; x_2(t) = 0
\end{cases}
$$


