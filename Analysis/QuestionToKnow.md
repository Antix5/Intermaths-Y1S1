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

For a sequence $(x_n)$ in a metric space $(X,d)$, we say that the sequence converges to $x$ if and only if $d(x_n,x) \rightarrow 0$ as $n \rightarrow \infty$.


2. Provide the definition of uniformly continuous function between two metric spaces at some given point.
   
3. Prove that a function f : X → Y between two metric spaces is continuous
at x ∈ X if and only if it is sequentially continuous at x.

1. Define the concept of topological space. Let C ⊂ X be a subset of a topological space. Define the closure of C and the interior of C. When is C
called a dense subset of X? Define the concept of separable metric space.


7. Prove that a subset of a topological space is closed if and only if it coincides with its closure.


8. Define the open sets of a metric space (X, d). Prove they define a topology.


9. Prove that a subset F of a metric space is closed if and only if it contains
all the limits of convergent sequences xn ∈ F.


10.  Define the discrete distance on R. Find a suitable equivalent condition
for the convergence of a sequence in this topology. Find a sequence that
converges in the standard sense in R, but not with respect to the discrete
distance.


11.  Define the concept of sequentially compact subset of a metric space.


12.  Define the concept of compactness for a subset K of a topological space.
Define the concept of total boundedness for a subset K of a metric space.


13.  Let (X, d) be a metric space and A ⊂ X. Prove that A is dense in X if and
only if for all x ∈ X and for all ε > 0 there exists a ∈ A with d(a, x) < ε.

14.  Prove that a sequentially compact metric space is separable.


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

