# Poles, zeros and system's behaviours

## Introduction

In this section, we will learn about the poles and zeros of a transfer function. We will also learn about the system's behaviours depending on the poles and zeros.

## Poles and zeros

### Definition

A pole is a root of the denominator of a transfer function. A zero is a root of the numerator of a transfer function.

### Example

Let's take the following transfer function:

$$G(s)=\frac{1}{s^2+2s+3}$$

The denominator of this transfer function is $s^2+4s+3$. The roots of this polynomial are $s_1=-1$ and $s_2=-3$. Therefore, the poles of this transfer function are $s_1=-1$ and $s_2=-3$.

The numerator is $1$, therefore, this transfer function has no zero.

### Computation tips - Partial fraction expansion

All polynomials can be written as a product of 1st order polynomials in the complex plane

$$p(s)=a_0+a_1s+a_2s^2+\dots+a_ns^n$$
$$\Leftrightarrow$$
$$p(s)=(x-\beta_1)(x-\beta_2)\dots(x-\beta_n)$$

where $\beta_1,\beta_2,\dots,\beta_n$ are the roots of the polynomial $p(s)$

The transfer function can therefore always be rewritten in the following form:

$$T(s)=\frac{Q(s)}{(s-\beta_1)(s-\beta_2)\dots(s-\beta_n)}$$

where $Q(s)$ is a polynomial of lower order than the denominator

#### Partial fraction expansion - Reminder

The partial fraction expansion is the process of rewriting a fraction as a sum of simpler fractions.
It is used to solve differential equations using Laplace transform.

Let's take the following transfer function:

$$T(s)=\frac{1}{s^2+4s+3}$$

The denominator of this transfer function is $s^2+4s+3$. The roots of this polynomial are $s_1=-1$ and $s_2=-3$. Therefore, the poles of this transfer function are $s_1=-1$ and $s_2=-3$.

We can rewrite this transfer function as:

$$T(s)=\frac{1}{(s+1)(s+3)}$$

##### Now, let's do that partial fraction expansion

$$T(s)=\frac{\lambda_1}{(s+1)} + \frac{\lambda_2}{(s+3)}$$

where $\lambda_1$ and $\lambda_2$ are constants

$$\frac{1}{(s+1)(s+3)}=\frac{\lambda_1}{(s+1)} + \frac{\lambda_2}{(s+3)}$$

$$\Leftrightarrow$$

$$\frac{1}{s+3} = \lambda_1 + \frac{\lambda_2 (s+1)}{s+3}$$

We input $s=-1$

$$\lambda_1 = 1/2$$

We do the same thing for the other root and get $\lambda_2 = -1/2$

$$T(s)=\frac{1}{2(s+1)} - \frac{1}{2(s+3)}$$

We apply the inverse Laplace transform to get the time domain response

$$\tau(t)=\frac{1}{2}e^{-t} - \frac{1}{2}e^{-3t}$$

Here is a simple example of the study of a transfer function using partial fraction expansion (with Laplace transform, for more complicated examples, we work with the state space representation)

### Important note regarding the behaviour of the system depending of the poles.

If the poles are real, the system is non oscillatory. If the poles are complex, the system is oscillatory.

If the real part of the poles is positive, the system is unstable because we observe an exponential growth of the output. If the real part of the poles is negative, the system is stable because we observe an exponential decay of the output.

If the real part of the poles is zero and the imaginary part is not zero, the system is oscillatory without damping.




