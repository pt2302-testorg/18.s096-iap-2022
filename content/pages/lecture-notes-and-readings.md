---
content_type: page
description: This page includes lecture notes and readings for each lecture.
draft: false
title: Lecture Notes and Readings
uid: d37b3aa2-ff0c-4286-b7ce-b7e4f3fbb2ea
---
## Lecture 1

### Lecture Notes

- Part 1: {{% resource_link "563ca6c0-9f9e-4974-8994-6ad8ce50438d" "Introduction (PDF)" %}}
- Part 2: Derivatives as Linear Operators \[notes not available\]

### Further Readings:

- [matrixcalculus.org](http://www.matrixcalculus.org/) is a fun site to play with derivatives of matrix and vector functions. 
- [*The Matrix Cookbook* (PDF)](https://www.math.uwaterloo.ca/~hwolkowi/matrixcookbook.pdf) has a lot of formulas for these derivatives, but no derivations.
- Notes on [Vector and Matrix Differentiation (PDF)](https://cdn-uploads.piazza.com/paste/j779e63owl53k6/04b2cb8c2f300212d723bea822a6b856085b28e28ca9debc75a05761a436499c/6.S087_Lecture_2.pdf) are helpful.
- **Fancier math**: The perspective of derivatives as linear operators is sometimes called a [Fréchet derivative](https://en.wikipedia.org/wiki/Fr%C3%A9chet_derivative) and you can find lots of very abstract (what I'm calling "fancy") presentations of this online, chock full of weird terminology whose purpose is basically to generalize the concept to weird types of vector spaces. The "little-o notation" o(δx) we're using here for "infinitesimal asymptotics" is closely related to the [Big *O* notation](https://en.wikipedia.org/wiki/Big_O_notation) used in computer science, but in computer science people are typically taking the limit as the argument (often called "n") becomes very *large* instead of very small. A fancy name for a row vector is a "covector" or [linear form](https://en.wikipedia.org/wiki/Linear_form), and the fancy version of the relationship between row and column vectors is the [Riesz representation theorem](https://en.wikipedia.org/wiki/Riesz_representation_theorem), but until you get to non-Euclidean geometry you may be happier thinking of a row vector as the transpose of a column vector.

## Lecture 2

### Lecture Notes

- Part 1: Derivatives as Linear Operators (cont.) \[notes not available\]
- Part 2: [Two by Two Matrix Jacobians (html)](https://rawcdn.githack.com/mitmath/matrixcalc/7340d2a7d40e6548a5ca0945ecae96cbac659929/2x2Jacobians.jl.html) ({{% resource_link "5f00501e-fb3c-48f9-a50d-d0c93bb377dc" "download the zip file" %}}) ([pluto notebook source code](https://github.com/mitmath/matrixcalc/blob/main/notes/2x2Jacobians.jl)) ({{% resource_link "0c0bb241-5d3f-4acb-a96d-6630947a841d" "download the source code zip file" %}})

### Further Readings:

- The terms "forward-mode" and "reverse-mode" differentiation are most prevalent in [automatic differentiation](https://en.wikipedia.org/wiki/Automatic_differentiation) (AD), which we will cover later in this course. 
- You can find many, many articles online about [backpropagation](https://en.wikipedia.org/wiki/Backpropagation) in neural networks. 
- There are many other versions of this, e.g. in differential geometry the derivative linear operator (multiplying Jacobians and perturbations dx right-to-left) is called a [pushforward](https://en.wikipedia.org/wiki/Pushforward_(differential)), whereas multiplying a gradient row vector (covector) by a Jacobian left-to-right is called a [pullback](https://en.wikipedia.org/wiki/Pullback_(differential_geometry)). 
- This video on "[Understanding Automatic Differentiation](https://www.youtube.com/watch?v=UqymrMG-Qi4)" by [Dr. Mohamed Tarek](https://github.com/mohamed82008) also starts with a similar left-to-right (reverse) vs right-to-left (forward) viewpoint and goes into how it translates to Julia code, and how you define custom chain-rule steps for Julia AD.

## Lecture 3

### Lecture Notes

- Part 1: {{% resource_link "e8eecb54-8a16-42ef-a24d-745cbf9451e3" "The Gradient of a Scalar Function of a Vector: Column Vector or Row Vector? (PDF)" %}}
- Part 2: [Finite Difference (Jupyter notebook)](https://nbviewer.org/urls/ocw.mit.edu/courses/18-s096-matrix-calculus-for-machine-learning-and-beyond-january-iap-2022/fd_checks.ipynb) ({{% resource_link "d9e83bd3-6b99-44b8-98c4-7ad59ffb2f4c" "download \"Finite Difference\" zip file" %}})

### Further Readings:

- Wikipedia has a useful list of [properties of the matrix trace](https://en.wikipedia.org/wiki/Trace_(linear_algebra)#Properties). 
- The "matrix dot product" introduced today is also called the [Frobenius inner product](https://en.wikipedia.org/wiki/Frobenius_inner_product), and the corresponding norm ("length" of the matrix viewed as a vector) is the [Frobenius norm](https://mathworld.wolfram.com/FrobeniusNorm.html). 
- When you "flatten" a matrix A by stacking its columns into a single vector, the result is called [vec(A)](https://en.wikipedia.org/wiki/Vectorization_(mathematics)), and many important linear operations on matrices can be expressed as [Kronecker products](https://en.wikipedia.org/wiki/Kronecker_product). 
- [*The Matrix Cookbook* (PDF)](https://www.math.uwaterloo.ca/~hwolkowi/matrixcookbook.pdf) has lots of formulas for derivatives of matrix functions. 
- There is a lot of information online on [finite difference](https://en.wikipedia.org/wiki/Finite_difference), [18.303 Notes on Finite Differences (PDF)](https://github.com/mitmath/18303/blob/fall16/difference-approx.pdf), or [Section 5.7 of Numerical Derivatives (PDF)](http://www.it.uom.gr/teaching/linearalgebra/NumericalRecipiesInC/c5-7.pdf). 
- The Julia [FiniteDifferences.jl](https://github.com/JuliaDiff/FiniteDifferences.jl) package provides lots of algorithms to compute finite-difference approximations; a particularly robust and powerful way to obtain high accuracy is to employ [Richardson extrapolation](https://github.com/JuliaDiff/FiniteDifferences.jl#richardson-extrapolation) to smaller and smaller δx. If you make δx too small, the finite precision (#digits) of [floating-point arithmetic](https://en.wikipedia.org/wiki/Floating-point_arithmetic) leads to [catastrophic cancellation](https://en.wikipedia.org/wiki/Catastrophic_cancellation) errors.

## Lecture 4

### Lecture Notes

- Part 1: [The Gradient of the Determinant (html)](https://rawcdn.githack.com/mitmath/matrixcalc/c97512521a9ff63802454ee258f1759c45f7d8b6/determinant_and_inverse.html) ({{% resource_link "5153711d-d113-46cb-8df6-e7e20a7f78a2" "download the zip file" %}}) ([Julia source](https://github.com/mitmath/matrixcalc/blob/iap2022/symeig.jl)) ({{% resource_link "6cd714af-b338-40c7-a3a0-7d570503a662" "download Julia source zip file" %}})
- Part 2: {{% resource_link "ed4afe03-6d76-495e-872b-cf5c194f3d03" "Nonlinear Root-Finding, Optimization, and Adjoint-Method Differentiation (PDF)" %}}

### Further Readings (Part 1):

- There are lots of discussions of the [derivative of a determinant](https://en.wikipedia.org/wiki/Jacobi%27s_formula) online, involving the ["adjugate" matrix](https://en.wikipedia.org/wiki/Adjugate_matrix) det(A)A⁻¹. Not as well documented is that the gradient of the determinant is the cofactor matrix widely used for the [Laplace expansion](https://en.wikipedia.org/wiki/Laplace_expansion) of a determinant. 
- The formula for the [derivative of log(det X)](https://statisticaloddsandends.wordpress.com/2018/05/24/derivative-of-log-det-x/) is also nice, and logs of determinants appear in surprisingly many applications (from statistics to quantum field theory). 
- [*The Matrix Cookbook* (PDF)](https://www.math.uwaterloo.ca/~hwolkowi/matrixcookbook.pdf) contains many of these formulas, but no derivations. 
- A nice application of d(det(A)) is solving for eigenvalues λ by applying Newton's method to det(A-λI)=0, and more generally one can solve det(M(λ))=0 for any function Μ(λ) — the resulting roots λ are called [nonlinear eigenvalues](https://en.wikipedia.org/wiki/Nonlinear_eigenproblem) (if M is nonlinear in λ), and one can apply Newton's method in ["The Nonlinear Eigenvalue Problem: Part II (PDF - 1.2 MB)"](https://www.maths.manchester.ac.uk/~ftisseur/talks/FT_talk2.pdf) using the determinant-derivative formula here.

### Further Readings (Part 2):

- There are many textbooks on [*Nonlinear Programming*](http://www.athenasc.com/nonlinbook.html) (by Bertsekas), including specialized books on [*Convex Optimization*](http://web.stanford.edu/~boyd/cvxbook/) (by Boyd and Vandenberghe), [*Introduction to Derivative-Free Optimization*](http://bookstore.siam.org/mp08/) (by Conn, Scheinberg, and Vicente), etcetera. 
- A useful review of topology-optimization methods can be found in Sigmund and Maute's "[Topology Optimization Approaches](https://link.springer.com/article/10.1007/s00158-013-0978-6)." 
- See the [Notes on Adjoint Methods (PDF)](https://github.com/mitmath/18335/blob/spring21/notes/adjoint/adjoint.pdf) and [The Adjoint Method for Differentiating Complex Computations (PDF)](https://github.com/mitmath/18335/blob/spring21/notes/adjoint/adjoint-intro.pdf) from *18.335 Introduction to Numerical Methods*.

## Lecture 5

### Lecture Notes

- [Forward and Reverse Automatic Differentiation in a Nutshell](https://rawcdn.githack.com/mitmath/matrixcalc/e90417f46a20bec6d9c743c6b7bf5b178e77913a/automatic_differentiation_done_quick.html) (guest lecture by [Dr. Chris Rackauckas](https://chrisrackauckas.com/)) ({{% resource_link "16c346e3-c441-411e-b9a5-a3bbb8bf71d1" "download the zip file" %}})

### Further Readings:

- Googling "automatic differentiation" will turn up many, many resources—this is a huge practical field these days. [ForwardDiff.jl](https://github.com/JuliaDiff/ForwardDiff.jl) (described in detail by "[Forward-Mode Automatic Differentiation in Julia](https://arxiv.org/abs/1607.07892)") uses [dual number](https://en.wikipedia.org/wiki/Dual_number) arithmetic similar to lecture to compute derivatives.
- See also the article "[How to Differentiate with a Computer](http://www.ams.org/publicoutreach/feature-column/fc-2017-12)," or google "dual number automatic differentiation" for many other reviews. 
- Implementing automatic reverse-mode AD is much more complicated than defining a new number type, unfortunately, and involves a lot more intricacies of compiler technology. See also Chris's blog post on [Engineering Trade-Offs in Automatic Differentiation](https://www.stochasticlifestyle.com/engineering-trade-offs-in-automatic-differentiation-from-tensorflow-and-pytorch-to-jax-and-julia/), and Chris Rackauckas's discussion post on [AD limitations](https://discourse.julialang.org/t/open-discussion-on-the-state-of-differentiable-physics-in-julia/72900/2).

## Lecture 6

### Lecture Notes

- Part 1: [Derivatives of Eigenproblems (html)](https://rawcdn.githack.com/mitmath/matrixcalc/61a7b3e0cbebd0ccdc126fbe831d1398154e272b/symeig.jl.html) ({{% resource_link "4c0529a7-9649-4d68-9617-399fce0743dc" "download the zip file" %}}) ([Julia source](https://github.com/mitmath/matrixcalc/blob/iap2022/symeig.jl)) ({{% resource_link "4b3b3a58-f350-4ec8-a621-49d634341796" "download Julia source zip file" %}})
- Part 2: Second Derivatives, Bilinear Forms, and Hessian Matrices \[notes not available\]

### Further Readings (Part 1):

- Computing derivatives on curved surfaces ("manifolds") is closely related to [tangent spaces](https://en.wikipedia.org/wiki/Tangent_space) in differential geometry. The effect of constraints can also be expressed in terms of [Lagrange multipliers](https://en.wikipedia.org/wiki/Lagrange_multiplier), which are useful in expressing optimization problems with constraints (see also Chapter 5 of [*Convex Optimization*](https://web.stanford.edu/~boyd/cvxbook/) by Boyd and Vandenberghe). 
- In physics, first and second derivatives of eigenvalues and first derivatives of eigenvectors are often presented as part of ["time-independent" perturbation theory](https://en.wikipedia.org/wiki/Perturbation_theory_(quantum_mechanics)#Time-independent_perturbation_theory) in quantum mechanics, or as the [Hellmann-Feynmann theorem](https://en.wikipedia.org/wiki/Hellmann%E2%80%93Feynman_theorem) for the case of dλ. 
- The derivative of an eigenvector involves *all* of the other eigenvectors, but a much simpler "vector-Jacobian product" (involving only a single eigenvector and eigenvalue) can be obtained from left-to-right differentiation of a *scalar function* of an eigenvector, as reviewed in the [18.335 Notes on Adjoint Methods (PDF)](https://github.com/mitmath/18335/blob/spring21/notes/adjoint/adjoint.pdf).

### Further Readings (Part 2):

- [Bilinear forms](https://en.wikipedia.org/wiki/Bilinear_form) are an important generalization of quadratic operations to arbitrary vector spaces, and we saw that the second derivative can be viewed as a [symmetric bilinear form](https://en.wikipedia.org/wiki/Symmetric_bilinear_form). This is closely related to a [quadratic form](https://en.wikipedia.org/wiki/Quadratic_form), which is just what we get by plugging in the same vector twice, e.g. the f''(x)\[δx,δx\]/2 that appears in quadratic approximations for f(x+δx) is a quadratic form. 
- The most familar multivariate version of f''(x) is the [Hessian matrix](https://en.wikipedia.org/wiki/Hessian_matrix). 
- Khan Academy has an introduction to [quadratic approximation](https://www.khanacademy.org/math/multivariable-calculus/applications-of-multivariable-derivatives/quadratic-approximations/a/quadratic-approximation).

## Lecture 7

### Lecture Notes

- Part 1: Hessian Matrices (cont.) \[notes not available\]
- Part 2: [Backpropagation through Back Substitution with a Backslash (PDF)](https://github.com/mitmath/matrixcalc/blob/iap2022/backprop_poster.pdf)

### Further Readings (Part 1):

- [Positive-definite](https://en.wikipedia.org/wiki/Definite_matrix) Hessian matrices, or more generally [definite quadratic forms](https://en.wikipedia.org/wiki/Definite_quadratic_form) f″, appear at extrema (f′=0) of scalar-valued functions f(x) that are local minima; there are a lot more formal treatments of the same idea—[Unconstrained Optimization (PDF)](http://www.columbia.edu/~md3405/Unconstrained_Optimization.pdf), and conversely Khan academy has the [simple 2-variable version](https://www.khanacademy.org/math/multivariable-calculus/applications-of-multivariable-derivatives/optimizing-multivariable-functions/a/second-partial-derivative-test) where you can check the sign of the 2×2 eigenvalues just by looking at the determinant and a single entry (or the trace). 
- There's a nice [stackexchange discussion](https://math.stackexchange.com/questions/2285282/relating-condition-number-of-hessian-to-the-rate-of-convergence) on why an [ill-conditioned](https://nhigham.com/2020/03/19/what-is-a-condition-number/) Hessian tends to make steepest descent converge slowly.
- University of Toronto's [Course Notes on Optimization (PDF - 3.3 MB)](https://www.cs.toronto.edu/~rgrosse/courses/csc421_2019/slides/lec07.pdf) may also be helpful.

### Further Readings (Part 2):

- See this blog post on [Calculus on Computational Graphs](https://colah.github.io/posts/2015-08-Backprop/) for a gentle review.
- See Columbia University's [Course Notes on Computational Graphs, and Backpropagation (PDF)](http://www.cs.columbia.edu/~mcollins/ff2.pdf) for a more formal approach.

## Lecture 8

### Lecture Notes

- Part 1: Hessian Matrices (cont.) \[notes not available\]
- Part 2: [Differentiable Programming and Neural Differential Equations](https://rawcdn.githack.com/mitmath/18337/7b0e890e1211bfa253782f7862389aeaa321e8d7/lecture11/adjoints.html) (guest lecture by [Dr. Chris Rackauckas](https://chrisrackauckas.com/))

### Further Readings (Part 1):

- See e.g. these Stanford University's notes on [Sequential Convex Programming (PDF)](https://web.stanford.edu/class/ee364b/lectures/seq_notes.pdf) using trust regions (sec. 2.2). 
- See 18.335 notes on [Quasi-Newton Optimization: Origin of the BFGS Update (PDF)](https://github.com/mitmath/18335/blob/spring21/notes/BFGS.pdf). 
- The fact that a quadratic optimization problem in a sphere has [strong duality](https://en.wikipedia.org/wiki/Strong_duality) and hence is efficiently solvable as discussed in section 5.2.4 of the [*Convex Optimization*](https://web.stanford.edu/~boyd/cvxbook/) by Boyd and Vandenberghe. 
- There has been a lot of work on [Hessian automatic computation](https://en.wikipedia.org/wiki/Hessian_automatic_differentiation), but for large-scale problems you can ultimately only compute Hessian-vector products efficiently in general, which are equivalent to a directional derivative of the gradient, and can be used e.g. for [Newton-Krylov methods](https://en.wikipedia.org/wiki/Newton%E2%80%93Krylov_method).

### Further Readings (Part 2):

- A very general reference on adjoint-method (reverse-mode/backpropagation) differentiation of ODEs (and generalizations thereof), using notation similar to that of Chris R. today, is "[Adjoint Sensitivity Analysis for Differential-Algebraic Equations: The Adjoint DAE System and Its Numerical Solution](https://epubs.siam.org/doi/10.1137/S1064827501380630)".
- See also the [adjoint sensitivity analysis](https://docs.sciml.ai/SciMLSensitivity/stable/) section of Chris's amazing [DifferentialEquations.jl software suite](https://diffeq.sciml.ai/stable/) for numerical solution of ODEs in Julia. 
- There is a nice YouTube lecture on [Adjoint State Method for an ODE](https://www.youtube.com/watch?v=k6s2G5MZv-I), again using a similar notation.