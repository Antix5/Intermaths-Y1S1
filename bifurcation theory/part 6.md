# Part 6 : Non-homogeneous linear systems (variation of constant formula)

What does that mean to have a non-homogeneous linear system ? It means that the right hand side of the differential equation is not zero :

$$
\dot{x} = Ax + b
$$

#### Def : 
Fondamental matrix of:
$$
\dot{x} = Ax + b
$$

is any non-singular matrix $\Phi$ such that:

$$
\frac{d}{dt}\Phi=  A \Phi
$$

Remark : if $\Phi$ is a fundamental matrix and C. $det(C) \neq 0$, then $\Phi C$ is a also fundamental
$\Phi(t)=e^{At}$ is fundamental, $e^{At} \text{ at time 0} = I$

$\Phi(t)\Phi(t)^{-1} = e^{At}e^{-At} = I$

This method is called the variation of the constant.

Let $\Phi(t)$ be any fundamental matrix of (2).
Then $\forall x_0 \in \mathbb{R}^n$ $\forall$ continuous f(t) the problem 

$$
\begin{cases}
\dot{x} = Ax + b \; (3)\\
x(0) = x_0 
\end{cases}
$$

has a unique solution given by

$$
x(t) = \Phi(t)\Phi(t)^{-1}x_0 + \Phi(t)\int_0^t \Phi(s)^{-1}b(s)ds
$$

Remark : If $\Phi(t) = e^{At}$, then

$$
x(t) = e^{At}x_0 + e^{At}\int_0^t e^{-As}b(s)ds \\
= e^{At} (x_0 + \int_0^t e^{-As}b(s)ds)
$$


uniqueness : let $x_1$ and $x_2$ be two solutions of (3). Then for $x=x_1-x_2$ we got $\dot{x}=Ax$, $x(0)=0 \Rightarrow x(t) = 0$

$$
\frac{d}{dt}x(t) = \Phi(t)\Phi(t)^{-1}x_0 + \Phi(t)\int_0^t \Phi(s)^{-1}b(s)ds + \Phi(t)\Phi(t)^{-1}b(t) \\
= A(\Phi(t)\Phi(t)^{-1}x_0+\Phi(t)\int_0^t \Phi(s)^{-1}b(s)ds)
$$

Exemple (forced harmonic oscillator)

$$
\ddot{x} + x = f(t) \\
$$

Introduce now the variables :

$$
\begin{cases}
y_1 = x \\
y_2 = \dot{x}
\end{cases}
\Rightarrow
\begin{cases}
\dot{y_1} = y_2 \\
\dot{y_2} = -y_1 + f(t)
\end{cases}
$$

We rewrite the system in matrix form :

$$
\dot{y} = Ay + b
$$

where
$$
A = \begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix}
\text{ and }
b =
\begin{pmatrix}
0 \\ f(t)
\end{pmatrix}
$$

it's a simple rotation matrix so : 

$$
e^{At} = \begin{pmatrix}
cos(t) & sin(t) \\
-sin(t) & cos(t)
\end{pmatrix}
$$

$$
e^{-A\tau} = \begin{pmatrix}
cos(\tau) & -sin(\tau) \\
sin(\tau) & cos(\tau)
\end{pmatrix}
$$

$$
\begin{pmatrix}
y_1(t) \\
y_2(t)
\end{pmatrix}
$$ 

$$
= e^{At} \begin{pmatrix}
y_1(0) \\
y_2(0)
\end{pmatrix}+e^{At} \int_0^t e^{-A(\tau)} b(\tau) d\tau
$$

$$
= \begin{pmatrix}
cos(t) & sin(t) \\
-sin(t) & cos(t)
\end{pmatrix}
$$

$$
\begin{pmatrix}
y_1(0) \\
y_2(0)
\end{pmatrix}
$$
$$+\begin{pmatrix}
cos(t) & sin(t) \\
-sin(t) & cos(t)
\end{pmatrix}
$$

$$\int_0^t \begin{pmatrix}
cos(\tau) & -sin(\tau) \\
sin(\tau) & cos(\tau)
\end{pmatrix}
$$
$$
\begin{pmatrix}
0 \\ f(\tau)
\end{pmatrix}
$$

$$ d\tau \\
= \begin{pmatrix}
y_1(0)cos(t) + y_2(0)sin(t) \\
-y_1(0)sin(t) + y_2(0)cos(t)
\end{pmatrix}
$$

$$+\begin{pmatrix}
\int_0^t cos(\tau) f(\tau) d\tau \\
\int_0^t sin(\tau) f(\tau) d\tau
\end{pmatrix}
$$

(to recheck)
