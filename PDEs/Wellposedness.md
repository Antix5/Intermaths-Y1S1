### Well-posedness

let $\begin{cases} a(x,t)u_t(x,t) + b(x,t)u_x(x,t) + c(x,t)u(x,t) = f(x,t) \\ a,b,c \in \mathcal{C}^1(\Omega), \quad f \in \mathcal{C}^1(\Omega) , \quad \Omega \subset \mathbb{R}, \quad (x,t) \in \Omega \end{cases}$ $\quad (I)$

$C_0 = (\bar{x}(\sigma),\bar{y}(\sigma)) \in C^1(I)$ a curve in $\Omega$ for some Interval I such that

$$
u(\bar{x}(\sigma),\bar{y}(\sigma)) = \bar{u}(\sigma) \quad \text{ for some } \bar{u} \in \mathcal{C}^1(I)
$$

Assume
 $a^2 + b^2 \neq 0 \forall (x,y) \in \Omega$ 

Let $(x_0,y_0) = (\bar{x}(0),\bar{y}(0)) \in C_0$ such that

$$
a(x,t) \frac{dt}{ds} |_{s=s_0} - b(x,t) \frac{dx}{ds} |_{s=s_0} \neq 0 \quad (II)
$$

Then on $\mathcal{U}$ neighbourhood of $(x_0, t_0) \exists!$ solution of the PDE $(I)$ that satifies the initial condition $\forall x \in C$


#### Exemple of use :

 $\quad \begin{cases} u_t + xu_x = 2u+x  \\ u(x,1) = x-4 \end{cases} \quad (1)$

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

 $\Rightarrow \frac{dx}{ds} |_{s=s_0} = 1 \quad \frac{dt}{ds} |_{s=s_0} = 0$

Therefore,

$$
1 \frac{dt}{ds} |_{s=s_0} - x \frac{dx}{ds} |_{s=s_0} = 1 \times 0 - x \times 1 = -x \neq 0 \quad
$$

This condition is also verified, the problem is therefore well-posed.

