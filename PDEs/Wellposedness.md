### Well-posedness

$
\begin{cases}
a(x,t)u_t(x,t) + b(x,t)u_x(x,t) + c(x,t)u(x,t) = f(x,t) \\
a,b,c \in \mathcal{C}^1(\Omega), \quad f \in \mathcal{C}^1(\Omega) , \quad \Omega \subset \mathbb{R}, \quad (x,t) \in \Omega 
\end{cases}
$ $\quad (I)$

Let $a^2 + b^2 \neq 0$ 

Let C be a curve in $\Omega$ parametrized by $\begin{cases} t(s) = s \\ x(s) = s \end{cases} \quad$, $\quad s \in I \subset R$

Tangent vector $\frac{d t(s)}{d s} , \frac{d x(s)}{d s}$ $\quad (I)$

$u = \Phi \in C \text{ s.t }, u(x_0(s),t_0(s)) = \Phi(s)$

Then  

$$
a(x,t) \frac{dt}{ds} |_{s=s_0} - b(x,t) \frac{dx}{ds} |_{s=s_0} \neq 0 \quad (II)
$$

Then $\mathcal{U}$ nbd of $(x_0, t_0) \exists!$ solution of the PDE $(I)$ satifying the initial condition $\forall x \in C$ for $\mathcal{U}$


#### Exemple of use :

$\quad
\begin{cases}
u_t + xu_x = 2u+x  \\
u(x,1) = x-4
\end{cases}
\quad (1)$

- Also in view of point (1), above, discuss the well-posedness of the problem (1)

In this case $a(x,t) = 1, \quad b(x,t) = x$

$$
a^2 + b^2 = 1 + x^2 \neq 0 \quad
$$

This condition is indeed verified

$$
a(x,t) \frac{dt}{ds} |_{s=s_0} - b(x,t) \frac{dx}{ds} |_{s=s_0} =$$ $$
1 \frac{dt}{ds} |_{s=s_0} - x \frac{dx}{ds} |_{s=s_0}
$$

We know that $u(x,1) = x-4 = u(s,1) = s-4$ due to the parametrisation.

and $x(s) = s$ and $t(s) = 1$

$ \Rightarrow \frac{dx}{ds} |_{s=s_0} = 1 \quad \frac{dt}{ds} |_{s=s_0} = 0$

Therefore,

$$
1 \frac{dt}{ds} |_{s=s_0} - x \frac{dx}{ds} |_{s=s_0} = 1 \times 0 - x \times 1 = -x \neq 0 \quad
$$

This condition is also verified, the problem is therefore well-posed.