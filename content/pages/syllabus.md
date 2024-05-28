---
content_type: page
description: This page includes course meeting times, prerequisites, course description,
  topics, and calendar.
draft: false
title: Syllabus
uid: 3edca454-764e-40e4-a81b-0504c739b7f5
---
## Course Meeting Times

Lectures: 3 sessions / week, 2 hours / session

## Prerequisites

Courses in linear algebra (such as [*18.06 Linear Algebra*](https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/)) and multivariate calculus (such as [*18.02 Multivariable Calculus*](https://ocw.mit.edu/courses/18-02sc-multivariable-calculus-fall-2010/))

## Course Description

We all know that calculus courses such as [*18.01 Single Variable Calculus*](https://ocw.mit.edu/courses/18-01sc-single-variable-calculus-fall-2010/) and [*18.02 Multivariable Calculus*](https://ocw.mit.edu/courses/18-02sc-multivariable-calculus-fall-2010/) cover univariate and vector calculus, respectively. Modern applications such as machine learning require the next big step, matrix calculus.

This class covers a coherent approach to matrix calculus showing techniques that allow you to think of a matrix holistically (not just as an array of scalars), compute derivatives of important matrix factorizations, and really understand forward and reverse modes of differentiation. We will discuss adjoint methods, custom Jacobian matrix vector products, and how modern automatic differentiation is more computer science than mathematics in that it is neither symbolic nor based on finite differences. 

## Topics

Here are some of the topics covered:

- Derivatives as linear operators and linear approximation on arbitrary vector spaces: beyond gradients and Jacobians.
- Derivatives of functions with matrix inputs and/or outputs (e.g. matrix inverses and determinants). Kronecker products and matrix "vectorization."
- Derivatives of matrix factorizations (e.g. eigenvalues/SVD) and derivatives with constraints (e.g. orthogonal matrices).
- Multidimensional chain rules, and the signifance of right-to-left ("forward") vs. left-to-right ("reverse") composition. Chain rules on computational graphs (e.g. neural networks).
- Forward- and reverse-mode manual and automatic multivariate differentiation.
- Adjoint methods (vJp/pullback rules) for derivatives of solutions of linear, nonlinear, and differential equations.
- Application to nonlinear root-finding and optimization. Multidimensional Newton and steepest–descent methods.
- Applications in engineering/scientific optimization and machine learning.
- Second derivatives, Hessian matrices, quadratic approximations, and quasi-Newton methods.

## Calendar

{{< tableopen >}}{{< theadopen >}}{{< tropen >}}{{< thopen >}}
Lecture # and Topics
{{< thclose >}}{{< thopen >}}
Key Dates
{{< thclose >}}{{< trclose >}}{{< theadclose >}}{{< tbodyopen >}}{{< tropen >}}{{< tdopen >}}
Lecture 1 Part 1: Introduction            
Lecture 1 Part 2: Derivatives as Linear Operators
{{< tdclose >}}{{< tdopen >}}
 
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Lecture 2 Part 1: Derivatives as Linear Operators (cont.)           
Lecture 2 Part 2: Two by Two Matrix Jacobians
{{< tdclose >}}{{< tdopen >}}
Problem Set 1 out
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Lecture 3 Part 1: The Gradient of a Scalar Function of a Vector: Column Vector or Row Vector?         
Lecture 3 Part 2: Finite Difference
{{< tdclose >}}{{< tdopen >}}
 
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Lecture 4 Part 1: The Gradient of the Determinant         
Lecture 4 Part 2: Nonlinear Root-Finding, Optimization, and Adjoint-Method Differentiation
{{< tdclose >}}{{< tdopen >}}
Problem Set 1 due            
Problem Set 2 out
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Lecture 5: Forward and Reverse Automatic Differentiation in a Nutshell
{{< tdclose >}}{{< tdopen >}}
 
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Lecture 6 Part 1: Derivatives of Eigenproblems         
Lecture 6 Part 2: Second Derivatives, Bilinear Forms, and Hessian Matrices
{{< tdclose >}}{{< tdopen >}}
 
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Lecture 7 Part 1: Hessian Matrices (cont.)         
Lecture 7 Part 2: Backpropagation through Back Substitution with a Backslash
{{< tdclose >}}{{< tdopen >}}
Problem Set 2 due
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Lecture 8 Part 1: Hessian Matrices (cont.)         
Lecture 8 Part 2: Differentiable Programming and Neural Differential Equations
{{< tdclose >}}{{< tdopen >}}
 
{{< tdclose >}}{{< trclose >}}{{< tbodyclose >}}{{< tableclose >}}