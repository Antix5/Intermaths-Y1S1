### Uniqueness of the heat equation proven by the energy method

$$
\begin{cases}
u_t - u_{xx} = 0 \\
u(x,0) = f(x) \\
u(0,t) = u(1,t) = 0
\end{cases}
$$

Let $u$ be a solution of the heat equation

$$
u_t - u_{xx} = 0 \\
\Leftrightarrow u_t = u_{xx}
$$

We now multiply by u on both sides and integrate over the domain $\Omega = (0,1)$

$$(A) \quad \int_0^1 u_t u dx = \int_0^1 u_{xx} u dx$$

$$\Leftrightarrow \frac{1}{2} \int_0^1 \frac{d}{dt} (u^2) dx = \int_0^1 u_{xx} u dx$$


$$\Leftrightarrow \frac{1}{2} \frac{d}{dt} \int_0^1 u^2 dx = \int_0^1 u_{xx} u dx$$

We now concentrate on the right hand side

$$\int_0^1 u_{xx} u dx = [u_x u]_0^1 - \int_0^1 u_x^2 dx$$

$$[u_x u]_0^1 = 0 - 0 = 0$$

$$- \int_0^1 u_x^2 dx = \int_0^1 u_{xx} u dx$$

$$\Rightarrow \frac{1}{2} \frac{d}{dt} \int_0^1 u^2 dx = - \int_0^1 u_{x}^2 dx$$

$$E'(t) = - \int_0^1 u_{x}^2 dx = \text{negative consant or null} $$

$$\Rightarrow E(0) \geq E(t) \quad \forall t \geq 0$$

Now let's assume that the equation has 2 solutions that we will name $v$ and $q$ (using the principle of superposition)

$w = v - q$ should also be a solution of the equation

$$\frac{1}{2} \frac{d}{dt} \int_0^1 w(x,0)^2 dx = 0$$

because $w^2$ cannot be negative therefore $w$ is null
and we have $v = q$

So, uniqueness of solutions






