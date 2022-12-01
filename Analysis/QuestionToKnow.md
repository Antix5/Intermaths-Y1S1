#  Possible BWQ questions

### First part

1. **Define the concept of metric, or distance, on a set X. Define the concept of norm on a linear space.**

Let $d: X \times X \rightarrow \mathbb{R}^+$
$d$ is called a distance if and only if the following conditions are satisfied:

   1. $d(x,y) = 0$ if and only if $x = y$ 
   2. $d(x,y) = d(y,x)$ (symetry)
   3. $d(x,z) \leq d(x,y) + d(y,z)$  (triangular inequality)

A space with a distance is called a metric space.
   

1. **Let $(X, || · ||)$ be a normed linear space.
Prove that $d(x, y) = ||x − y||$ is a distance on X.**

    1. Let's prove that $d(x,y) = 0$ if and only if $x = y$ :
    $$d(x,y) = ||x-y|| = 0 \Leftrightarrow x-y = 0 \Leftrightarrow x = y$$

    2. Let's prove that $d(x,y) = d(y,x)$ 

    $$d(x,y) = ||x-y|| = ||y-x|| = d(y,x)$$

    3. Let's prove that $d(x,z) \leq d(x,y) + d(y,z)$

    $$d(x,z) = ||x-z|| \leq ||x-y|| + ||y-z|| = d(x,y) + d(y,z)$$ 


1. **Define the concepts of convergent sequence and limit of a sequence on a metric space.**

For a sequence $(x_n)$ in a metric space $(X,d)$, we say that the sequence converges to $x$ if and only if for every $\epsilon > 0$ there exists a $N$ such that $d(x_n,x) < \epsilon$ for all $n \geq N$.

The point x is called the limit of the sequence $(x_n)$ and is denoted by $\lim_{n \rightarrow \infty} x_n = x$.


1. **Provide the definition of uniformly continuous function between two metric spaces at some given point.**

$$
 \forall \varepsilon >0\;\exists \delta >0\;\forall x\in X\;\forall y\in X:\,d_{1}(x,y)<\delta \,\Rightarrow \,d_{2}(f(x),f(y))<\varepsilon 
 $$


   
1. **Prove that a function f : X → Y between two metric spaces is continuous at x ∈ X if and only if it is sequentially continuous at x.**

__*Proof*__.
First, we show that if f is continuous, then it is sequentially continuous :

Suppose that f is continuous at x, and let $x_n \rightarrow x$. Let $e > 0$ be given.
By the continuity of f , we can choose $δ > 0$ such that $d(x_n, x) < δ$ implies
$d(f(x_n), f(x)) < e$. By the convergence or $(x_n)_n$, we can choose N so that
$n ≥ N$ implies d(x, x_n) < δ. Therefore, $n ≥ N$ implies $d(f(xn), f(x)) < e$, and
this means that $f(x_n) → f(x_n)$.


To prove the converse, we prove that if f is discontinuous, then it is not sequentially continuous. If f is discontinuous at x, then there is an $e > 0$ such that for every $n ∈ N$ there exists $x_n ∈ X$ with $d(x_n, x) < \frac{1}{n}$ and
$d(f(x_nn), f(x)) ≥ e$. The sequence $(x_n)$ constructed converges to x but $(f(x_n))$
does not converge to $f(x)$. Hence, f is not sequentially continuous


2. **Define the concept of topological space. Let $C \subset X$ be a subset of a topological space. Define the closure of C and the interior of C. When is C called a dense subset of X? Define the concept of separable metric space.**

Closure of C is the smallest closed subset of X containing C.

The interior of C is the largest open subset of X containing C.

A subset C is dense if its closure is the whole space X. A metric space is separable if it contains a countable dense subset.


3. **Prove that a subset of a topological space is closed if and only if it coincides with its closure.**

Proof by contradiction :
We are going to try to find a closed topological subset of X that is not equal to its closure.

Let $C \subset X$ be a closed topological subset of X : 

Therefore :

   1. $C$ is closed
      $C \subset X$

We now assume there is a smaller closed subset of X that contains C, let's call it $C'$

Therefore, $C' \subset C$ , but $C'$ is smaller than $C$, which is a contradiction.

Therefore, $C$ is equal to its closure.


1. **Define the open sets of a metric space (X, d). Prove they define a topology.**

B is an open set of X if :

$$ \forall x \in B, \; \exists \epsilon > 0, \; \forall y \in X : d(x,y) < \epsilon \Rightarrow y \in B $$

equivalently :

$$ \forall x \in B, \; \exists \epsilon > 0, \; \forall y \in \mathcal{B_\epsilon(x)} \text{ s.t } y \in B $$


Let S be a set.
Let X be a set of subsets of X.
Then X is a topology on S if and only if:

(1): Any intersection of arbitrarily many open sets of $S$ under $X$ is an open set of $S$ under $X$

(2): The union of any finite number of open sets of $S$ under $X$ is an open set of $S$ under $X$

(3):$S$ and $∅$ are both opened sets of $S$ under $X$
where a open set $V$ of $S$ under $X$ is defined as a subset of S such that $S∖V ∈ X$.


1. **Prove that a subset F of a metric space is closed if and only if it contains all the limits of convergent sequences $x_n ∈ F$.**

We can rewrite that in the following way :

In a metric space:

A set F is closed $\Leftrightarrow$ $\forall (x_n) \in F, lim_{n\rightarrow \infty}(x_n) = x \in F $

We therefore have to prove 2 things :

a) F is closed $\Rightarrow$ $\forall (x_n) \in F, lim_{n\rightarrow \infty}(x_n) = x \in F $

b) $\forall (x_n) \in F, lim_{n\rightarrow \infty}(x_n) = x \in F $ $\Rightarrow$ F is closed

Let's prove **a)** :

We are going to do a proof by contradiction.

Let's assume that F is closed but that $\exists (x_n) \in F, lim_{n\rightarrow \infty}(x_n) = x \notin F $

F is closed if it's complement is open,so $lim_{n\rightarrow \infty}(x_n) = x \in F^c $

$F^c$ is open, so $\exist \epsilon > 0$ such that $\mathcal{B_\epsilon(x)} \subset F^c $

The definition of a limit is that for every $\epsilon > 0$, there exists a $N$ such that $d(x_n,x) < \epsilon$ for all $n \geq N$.

That would imply that $x_n$ would be at one moment in both $F$ and $F^c$ (if we want to satify both conditions), which is a contradiction.

The closeness of F therefore implies that $\forall (x_n) \in F, lim_{n\rightarrow \infty}(x_n) = x \in F $

Let's prove **b)** :

That all sequence from a set converging to a point in the said set is closed.

We will once against do a proof by contradiction.

Let's assume that all sequence converge in a set but the set is not closed, we can write this in the following way :

$\forall (x_n) \in F, lim_{n\rightarrow \infty}(x_n) = x \in F $ $\Rightarrow$ F is not closed

The contraposition of that statement is :

$$\overline{\forall (x_n) \in F, lim_{n\rightarrow \infty}(x_n) = x \in F} \Rightarrow \text{ F is closed } $$

$$\Leftrightarrow$$

$$\exists (x_n) \in F, lim_{n\rightarrow \infty}(x_n) = x \notin F \Rightarrow \text{F is closed}$$

If F is closed , all sequence should converge in F, therefore, there is not sequence in F that does not converge in F, therefore

If all sequence in F converge in F, then F is closed.

We therefore proved that :

A subset F of a metric space is closed if and only if it contains all the limits of convergent sequences $x_n \in F$.


1. **Define the discrete distance on R. Find a suitable equivalent condition for the convergence of a sequence in this topology. Find a sequence that converges in the standard sense in R, but not with respect to the discrete distance.**

The discrete distance on R is defined as :

$$d(x,y) = \begin{cases} 0 & \text{if } x = y \\ 1 & \text{if } x \neq y \end{cases}$$

The equivalent condition for the convergence of a sequence in this topology is :

$$\exists N \in \mathbb{N} \text{ s.t } \forall n \geq N, d(x_n,y) = 0$$

A sequence that converges in the standard sense in R, but not with respect to the discrete distance is :

$x_n = 1/n$ converges to 0 in R, but not with respect to the discrete distance (because it's in infinite time)


2. **Define the concept of sequentially compact subset of a metric space.**

A topological space X is sequentially compact if every sequence of points in X has a convergent subsequence converging to a point in X.

3. **Define the concept of compactness for a subset K of a topological space. Define the concept of total boundedness for a subset K of a metric space.**

Compactness of subsets
A subset K of a topological space X is said to be compact if it is compact as a subspace (in the subspace topology). That is, K is compact if for every arbitrary collection C of open subsets of X such that

${\displaystyle K\subseteq \bigcup _{c\in C}c\ ,}{\displaystyle K\subseteq \bigcup _{c\in C}c\ ,}$
there is a finite subcollection F ⊆ C such that

${\displaystyle K\subseteq \bigcup _{c\in F}c\ .}{\displaystyle K\subseteq \bigcup _{c\in F}c\ .}$
Compactness is a "topological" property. That is, if ${\displaystyle K\subset Z\subset Y}{\displaystyle K\subset Z\subset Y}$, with subset Z equipped with the subspace topology, then K is compact in Z if and only if K is compact in Y.


4.   Let (X, d) be a metric space and A ⊂ X. Prove that A is dense in X if and
only if for all x ∈ X and for all ε > 0 there exists a ∈ A with d(a, x) < ε.

1.   Prove that a sequentially compact metric space is separable.


15.  Prove that every compact subset of a metric space is closed and bounded.


16.  Define the concept of equivalent norms on a linear space. Let X be an
n-dimensional linear space with a given basis. Define the k · k1-norm
with respect to that basis. Prove that all norms X are equivalent to the
k · k1-norm.

17.  Define the `
p norms and the `
p
spaces for p ∈ [1, +∞].


18.  State and prove Young’s inequality.


19.  State and prove the discrete Hoelder inequality.


20.  State and prove the discrete Minkowski inequality.


21.  Let X be a metric space and fn : X → R be a sequence of functions.
Define the concepts of pointwise and uniform convergence for fn. Prove
that uniform convergence implies pointwise convergence. Define the
uniform norm, or infinity norm, of function f : X → R.


22.  Let fn : X → R be a sequence of continuous functions. Assume fn → f
uniformly for some f : X → R. Prove that f is continuous.


23.  Let X be a metric space. Define the spaces Cb
(X), Cc(X), and C0(X) with
their standard norm. Prove that in general these spaces are all distinct.
Prove they all coincide with C(X) in case X is compact.


24.  Let X be a metric space. For a family F ⊂ C(X), define the concept of
equicontinuity. Let K be a compact metric space and let F ⊂ C(K) be
closed, bounded, and equicontinuous. Then prove that K is compact in
C(K) with the standard infinity norm.


25.  Find an example of a bounded set in C([0, 1]) which is not relatively
compact.


26.  Define the concept of Lipschitz continuous function f : X → R. Define the
Lipschitz constant of f . Prove that every Lipschitz continuous function
f : [0, 1] → R is continuous. Find an example showing the vice-versa is,
in general, false.


27.  Prove that the set of Lipschitz continuous functions f : X → R with
Lipschitz constant bounded by a given constant M is closed in C(X)
with the infinity norm.


28.  Define the linear space C
1
([0, 1]). Prove that C
1
([0, 1]) is not closed in
C([0, 1]) equipped with the infinity norm.


29.  Define the linear space X = C
1
([0, 1]) and the C
1 norm on X. Prove that
C
1
([0, 1]) equipped with the C
1 norm is a Banach space.


30.  Define the concept of contraction mapping on a metric space. State and
prove the contraction mapping theorem.

