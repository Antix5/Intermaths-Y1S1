# Partial differential equations

Notation : 

$u_x$ is the derivative of $u$ with respect to $x$.

## First order equations

### Linear, semi-linear and quasi-linear equations

#### Main parts

The main part of a differential equation is the part with the highest order derivative. For example, in the equation $u_{xx} = f(x)$, the main part is $u_{xx}$.

#### Linear equations

A linear equation is an equation of the form:

$$\sum_{i=1}^n a_i u_{x_i} = f$$

A semi-linear equation is similar to a linear equation but can be differentiated due to the fact that the lower order derivatives are not linear. For example, the equation $u_{xx} + u_x^2 = f$ is semi-linear.

A quasi-linear equation is similar to a linear equation but can contain cross terms:

$$\sum_{i=1}^n a_i u_{x_i} + \sum_{i=1}^n \sum_{j=1}^n b_{ij} u_{x_i} u_{x_j} = f$$

Other non linearity exist but those are very well studied.

### Well-posedness

For a PDE to be well-posed, it must have the following properties:

  * A solution exists
  * The solution is unique
  * The solution's behavior changes continuously with the initial conditions


