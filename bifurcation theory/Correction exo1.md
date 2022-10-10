## Ex 1 : 

Solve $\dot{x} = Ax$ for

### a)

$$A =
\begin{pmatrix}
3 & 1 \\
1 & 3
\end{pmatrix}$$

Solution :

$$0=det(A-XI)=det
\begin{pmatrix}
3-X & 1 \\
1 & 3-X 
\end{pmatrix}\\
=(3-X)^2-1
\\
\\
1=(3-X)^2 \Rightarrow
\begin{cases}
1=3-X \Leftrightarrow X=2\\
-1=3-X \Leftrightarrow X=4
\end{cases}$$

therefore the solutions are $\lambda_1 = 2$ and $\lambda_2 = 4$

We now look for obvious eigenvectors :

$$\begin{cases}
v_1 = \begin{pmatrix} 1 \\ 1 \end{pmatrix} \\
v_2 = \begin{pmatrix} 1 \\ -1 \end{pmatrix}
\end{cases}$$

So P = $$\begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix}$$

$$det(P)=-1-1=-2$$

$$det(P^{-1})=-\frac{1}{2}$$

We look for the comatrix of P :

$$C(P) =
\begin{pmatrix}
-1 & -1 \\
-1 & 1
\end{pmatrix}$$

$$C(P)^T =
\begin{pmatrix}
-1 & -1 \\
-1 & 1
\end{pmatrix}$$


$$P^{-1} = \frac{1}{det(P)}C(P)^T = \frac{1}{2}\begin{pmatrix}
1 & 1 \\
1 & -1
\end{pmatrix}$$

We check that $P^{-1}P = I$ :

$$\begin{pmatrix}
1 & 1 \\
1 & -1
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & -1
\end{pmatrix}
=\begin{pmatrix}
2 & 0 \\
0 & 2
\end{pmatrix}
=2I$$

So we have found the eigenvectors and the eigenvalues of $A$.

$$e^{At} = P\begin{pmatrix}
e^{2t} & 0 \\
0 & e^{4t}
\end{pmatrix}P^{-1}$$

We but A back in its inital basis :

$$e^{At} = \begin{pmatrix}
1 & 1 \\
1 & -1
\end{pmatrix}
\begin{pmatrix}
e^{2t} & 0 \\
0 & e^{4t}
\end{pmatrix}
\frac{1}{2}
\begin{pmatrix}
1 & 1 \\
1 & -1
\end{pmatrix}$$

$$= \frac{1}{2} \begin{pmatrix}
e^{2t} & e^{4t} \\
e^{2t} & -e^{4t}
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & -1
\end{pmatrix}$$

$$= \frac{1}{2} \begin{pmatrix}
e^{2t}+e^{4t} & e^{2t}-e^{4t} \\
e^{2t}-e^{4t} & e^{2t}+e^{4t}
\end{pmatrix}$$

So the solution is :

$$x(t) = \frac{1}{2} \begin{pmatrix}
e^{2t}+e^{4t} & e^{2t}-e^{4t} \\
e^{2t}-e^{4t} & e^{2t}+e^{4t}
\end{pmatrix}
C_1
$$

### b)

$$A =
\begin{pmatrix}
2 & 4 \\
-1 & 2
\end{pmatrix}$$

Solution :

$$0=det(A-XI)=det\begin{pmatrix}
2-X & 4 \\
-1 & 2-X
\end{pmatrix}\\
=(2-X)(2-X)+4
\\ \Leftrightarrow \\
(2-X)^2=-4 \Rightarrow
\begin{cases}
2-X=2i \Leftrightarrow X=2-2i=2(1-i)\\
2-X=-2i \Leftrightarrow X=2+2i=2(1+i)
\end{cases}$$

therefore the solutions are $\lambda_1 = 2(1-i)$ and $\lambda_2 = 2(1+i)$

We can already say that they will be an element of rotation to the vector field due to the complex eigenvalues.

We now look for eigenvectors :

$$
Av_1 = \lambda_1 v_1 \Leftrightarrow
\begin{pmatrix}
2 & 4 \\
-1 & 2
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix}
=2(1-i)
\begin{pmatrix}
x \\
y
\end{pmatrix}
\Leftrightarrow
\begin{pmatrix}
2-2(1-i) & 4 \\
-1 & 2-2(1-i)
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix}
=0
\\
\Leftrightarrow
\begin{pmatrix}
2(1-1+i) & 4 \\
-1 & 2(1-1+i)
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix}
=0
\\
\Leftrightarrow
\begin{pmatrix}
2i & 4 \\
-1 & 2i
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix}
=0
\\
$$

$$\begin{pmatrix}
2i\\
1
\end{pmatrix}
= v_1
$$

$$
Av_2 = \lambda_2 v_2 \Leftrightarrow
\begin{pmatrix}
2 & 4 \\
-1 & 2
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix}
=2(1+i)
\begin{pmatrix}
x \\
y
\end{pmatrix}
\Leftrightarrow
\begin{pmatrix}
2-2(1+i) & 4 \\
-1 & 2-2(1+i)
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix}
=0
\\
\Leftrightarrow
\begin{pmatrix}
2(1-1-i) & 4 \\
-1 & 2(1-1-i)
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix}
=0
\\
\Leftrightarrow
\begin{pmatrix}
-2i & 4 \\
-1 & -2i
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix}
=0
\\
$$

$$\begin{pmatrix}
-2i\\
1
\end{pmatrix}
= v_2
$$

We now have two eigenvectors and two eigenvalues. We can now find the matrix $P$ :

$$P = \begin{pmatrix}
2i & -2i \\
1 & 1
\end{pmatrix}$$

We compute det(P) :

$$det(P) = 2i+2i = 4i$$

so $P$ is invertible. We can now compute $P^{-1}$ :

$$P^{-1} = \frac{-i}{4}com(P)^T$$

$$com(P) = \begin{pmatrix}
1 & -1 \\
2i & 2i
\end{pmatrix}$$

$$P^{-1} = \frac{-i}{4}
\begin{pmatrix}
1 & 2i \\
-1 & 2i
\end{pmatrix}=
\frac{1}{4}
\begin{pmatrix}
-i & 2 \\
i & 2
\end{pmatrix}$$

We can now compute $e^{At}$ :

$$e^{At} = P e^{\Lambda t} P^{-1}$$

$$e^{\Lambda t} = \begin{pmatrix}
e^{2t-2it} & 0 \\
0 & e^{2t+2it}
\end{pmatrix}$$


$$=e^{2t}
\begin{pmatrix}
e^{-2it} & 0 \\
0 & e^{2it}
\end{pmatrix}$$

$$e^{At} = \frac{e^{2t}}{4}
\begin{pmatrix}
2i & -2i \\
1 & 1
\end{pmatrix}
\begin{pmatrix}
e^{-2it} & 0 \\
0 & e^{2it}
\end{pmatrix}
\begin{pmatrix}
-i & 2 \\
i & 2
\end{pmatrix}$$

$$= \frac{e^{2t}}{4}
\begin{pmatrix}
2ie^{-2it} & -2ie^{2it} \\
e^{-2it} & e^{2it}
\end{pmatrix}
\begin{pmatrix}
-i & 2 \\
i & 2
\end{pmatrix}$$

$$= \frac{e^{2t}}{4}
\begin{pmatrix}
2e^{-2it} + 2e^{2it} & -4ie^{-2it} -4ie^{2it} \\
-ie^{-2it} + ie^{2it} & 2e^{-2it} + 2e^{2it}
\end{pmatrix}$$

$$=\frac{e^{2t}}{4}
\begin{pmatrix}
4cos(2t) & 8sin(2t) \\
2sin(2t) & 4cos(2t)
\end{pmatrix}$$

$$=\begin{pmatrix}
e^{2t}cos(2t) & 2e^{2t}sin(2t) \\
\frac{e^{2t}}{2}sin(2t) & e^{2t}cos(2t)
\end{pmatrix}$$

We can now compute the solution:

$$x(t) = \begin{pmatrix}
e^{2t}cos(2t) & 2e^{2t}sin(2t) \\
\frac{e^{2t}}{2}sin(2t) & e^{2t}cos(2t)
\end{pmatrix}
C
$$

### c)

$$
A = 
\begin{pmatrix}
1 & 0 & 0 \\
1 & 2 & 0 \\
1 & 0 & -1
\end{pmatrix}
$$

We have here a lower triangular matrix, so the eigenvalues are the diagonal elements. We have:

$$\lambda_1 = 1 \\
\lambda_2 = 2 \\
\lambda_3 = -1$$

We can now compute the eigenvectors:

For $v_1$ :

$$
\begin{pmatrix}
0 & 0 & 0 \\
1 & 1 & 0 \\
1 & 0 & -2
\end{pmatrix}
v_1 = 0
$$

In that case 

$$v_1 = \begin{pmatrix}
2 \\
-2 \\
1
\end{pmatrix}$$

For $v_2$ :

$$
\begin{pmatrix}
-1 & 0 & 0 \\
1 & 0 & 0 \\
1 & 0 & -3
\end{pmatrix}
v_2 = 0
$$

In that case $v_2$ is:

$$v_2 = \begin{pmatrix}
0 \\
1 \\
0
\end{pmatrix}$$

For $v_3$ :

$$
\begin{pmatrix}
2 & 0 & 0 \\
1 & 3 & 0 \\
1 & 0 & 0
\end{pmatrix}
v_3 = 0
$$

In that case $v_3$ is:

$$v_3 = \begin{pmatrix}
0 \\
0 \\
1
\end{pmatrix}$$

We now have three eigenvectors and three eigenvalues. We can now find the matrix $P$ :

$$P = \begin{pmatrix}
2 & 0 & 0 \\
-2 & 1 & 0 \\
1 & 0 & 1
\end{pmatrix}$$

The determinant of a diagonal matrix is the product of the diagonal elements. We compute det(P) :

$$det(P) = 2$$

so $P$ is invertible. We can now compute $P^{-1}$ :

I compute the comatrix of P:

$$com(P) = \begin{pmatrix}
1 & 2 & -1 \\
0 & 2 & 0 \\
0 & 0 & 2
\end{pmatrix}$$

so $P^{-1}$ is:

$$P^{-1} = \frac{1}{2}
\begin{pmatrix}
1 & 0 & 0 \\
2 & 2 & 0 \\
-1 & 0 & 2
\end{pmatrix}$$

We check that $P^{-1}P = I$ :

$$P^{-1}P = \frac{1}{2}
\begin{pmatrix}
1 & 0 & 0 \\
2 & 2 & 0 \\
-1 & 0 & 2
\end{pmatrix}
\begin{pmatrix}
2 & 0 & 0 \\
-2 & 1 & 0 \\
1 & 0 & 1
\end{pmatrix} =
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} = I$$

We can now compute $e^{At}$ :

$$e^{At} = P e^{\Lambda t} P^{-1}$$

$$e^{\Lambda t} = \begin{pmatrix}
e^{t} & 0 & 0 \\
0 & e^{2t} & 0 \\
0 & 0 & e^{-t}
\end{pmatrix}$$

$$e^{At} = \begin{pmatrix}
2 & 0 & 0 \\
-2 & 1 & 0 \\
1 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
e^{t} & 0 & 0 \\
0 & e^{2t} & 0 \\
0 & 0 & e^{-t}
\end{pmatrix}
\frac{1}{2}
\begin{pmatrix}
1 & 0 & 0 \\
2 & 2 & 0 \\
-1 & 0 & 2
\end{pmatrix}$$

$$e^{At} = \begin{pmatrix}
2e^{t} & 0 & 0 \\
-2e^{t} & e^{2t} & 0 \\
e^{t} & 0 & e^{-t}
\end{pmatrix}
\frac{1}{2}
\begin{pmatrix}
1 & 0 & 0 \\
2 & 2 & 0 \\
-1 & 0 & 2
\end{pmatrix}$$

$$e^{At} = \frac{1}{2}
\begin{pmatrix}
2e^{t} & 0 & 0 \\
-2e^t + 2e^{2t} & 2e^{2t} & 0 \\
e^t-e^{-t} & 0 & 2e^{-t}
\end{pmatrix}$$

$$x(t) =
\frac{1}{2}
\begin{pmatrix}
2e^{t} & 0 & 0 \\
-2e^t + 2e^{2t} & 2e^{2t} & 0 \\
e^t-e^{-t} & 0 & 2e^{-t}
\end{pmatrix}
C
$$

### d)

$$
A =
\begin{pmatrix}
0 & -2 & 0 \\
1 & 2 & 0 \\
0 & 0 & -2
\end{pmatrix}
$$

$$
det(A-XI) = (-2-X)(-X(2-X)+2) = 0
\Leftrightarrow
\begin{cases}
-2-X = 0 \\
-X(2-X)+2 = 0 \Leftrightarrow X^2-2X+2 = 0
\end{cases}
$$

$$
X^2-2X+2 = 0 \\
\Delta = 4-4(1)(2) = 4-8 = -4 \\
X_{1,2} = \frac{2\pm i\sqrt{4}}{2} = 1 \pm i
$$

We have 3 eigenvalues: -2, 1+i and 1-i

We can now compute the eigenvectors:

For $v_1$ :

$$
\begin{pmatrix}
-2 & -2 & 0 \\
1 & 0 & 0 \\
0 & 0 & -4
\end{pmatrix}
v_1 = 0
$$

In that case, it's impossible to find a solution for $v_1$ as a standard eigenvector but we can try to find a generalized eigenvector:



















