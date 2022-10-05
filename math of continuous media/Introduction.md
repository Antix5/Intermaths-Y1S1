# Mathematics of Continuous Mediums

### What is a continuous medium?

**Continuous medium**, is a region defined in space where various properties, such as temperature, pressure, density, and velocity, may vary in a continuous manner. This is a macroscopic description of a medium, and is in contrast to a microscopic description, where the medium is described as a collection of particles. The macroscopic description is often sufficient for many applications, but in some cases, the microscopic description is required.

### Notation and conventions

We will use the following notation and conventions:

*   $\nabla$ is the gradient operator
*   The divergence operator is denoted by $\operatorname{div}$ or can be noted by $\nabla \cdot$ for convenience reasons.
*   The curl operator is denoted by $\operatorname{curl}$ or can be noted by $\nabla \wedge$ for convenience reasons.
*   Jacobian matrices are denoted by $J$.
*   Tensor products are denoted by $\otimes$.

The divergence theorem is the following:

$$\int_{\partial V} \vec{F} \cdot \vec{n} dS = \int_V \operatorname{div} \vec{F} dV$$

### Transport formula

The transport formula, allows to move the derivative in respect to time to the left

$$\frac{d}{dt} \int_{A(t)} g(x,t) dx = \int_{A(t)} (\frac{D}{Dt}g + g\nabla \cdot u) dx$$

(demo later)

#### Particular case (used most of the time)

if $g(x,t) = \rho(x,t)\psi(x,t)$, then

$$\frac{d}{dt} \int_{A(t)} \rho(x,t)\psi(x,t) dx = \int_{A(t)} (\frac{D}{Dt}\rho\psi + \rho\psi\nabla \cdot u) dx\\
= \int_{A(t)} (\rho\frac{D}{Dt}\psi + \psi \frac{D\rho}{Dt} + \rho\psi\nabla \cdot u) dx\\$$

$$= \int_{A(t)} (\rho\frac{D\psi}{Dt} + \psi(\frac{D \rho}{Dt} + \rho\nabla \cdot u)) dx\\$$

Because of conservation law 

$$\frac{D\rho}{Dt} + \rho\nabla \cdot u = 0$$

and therefore

$$\frac{d}{dt} \int_{A(t)} \rho \psi dx = \int_{A(t)} \rho \frac{D\psi}{Dt} dx$$

