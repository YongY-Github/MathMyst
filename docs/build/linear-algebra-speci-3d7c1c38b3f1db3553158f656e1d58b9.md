# Linear Algebra: Special Matrices and Applications

This chapter introduces **special matrices** that play a central role in
optimization, comparative statics, and economic modeling. These matrices
summarize how systems respond to changes and how curvature determines optimality.

The focus is on **interpretation** and **application**, rather than abstract theory.

---

## The Jacobian Matrix

Consider a vector-valued function:
$$
f(x) =
\begin{bmatrix}
f_1(x_1,\dots,x_n) \\
\vdots \\
f_m(x_1,\dots,x_n)
\end{bmatrix}.
$$

The **Jacobian matrix** of $f$ is the matrix of first-order partial derivatives:
$$
J(x) =
\begin{bmatrix}
\frac{\partial f_1}{\partial x_1} & \cdots & \frac{\partial f_1}{\partial x_n} \\
\vdots & \ddots & \vdots \\
\frac{\partial f_m}{\partial x_1} & \cdots & \frac{\partial f_m}{\partial x_n}
\end{bmatrix}.
$$

### Interpretation

- Each row shows how one equation responds to changes in variables.
- The Jacobian generalizes the derivative to multivariate settings.
- In economics, Jacobians appear in:
  - systems of equations,
  - equilibrium conditions,
  - comparative statics.

---

## The Hessian Matrix

For a scalar-valued function $f(x_1,\dots,x_n)$, the **Hessian matrix** collects
second-order partial derivatives:
$$
H(x) =
\begin{bmatrix}
\frac{\partial^2 f}{\partial x_1^2} & \cdots & \frac{\partial^2 f}{\partial x_1 \partial x_n} \\
\vdots & \ddots & \vdots \\
\frac{\partial^2 f}{\partial x_n \partial x_1} & \cdots & \frac{\partial^2 f}{\partial x_n^2}
\end{bmatrix}.
$$

### Properties

- Under mild regularity conditions, the Hessian is **symmetric**.
- The Hessian summarizes the **curvature** of a function.
- It plays a crucial role in second-order conditions for optimization.

---

## Quadratic Forms

Given a symmetric matrix $A$ and a vector $x$, the expression
$$
x' A x
$$
is called a **quadratic form**.

Quadratic forms arise naturally when:
- approximating functions locally,
- analyzing curvature,
- studying stability.

### Example

If
$$
A =
\begin{bmatrix}
a & b \\
b & c
\end{bmatrix},
\quad
x =
\begin{bmatrix}
x_1 \\
x_2
\end{bmatrix},
$$
then
$$
x'Ax = a x_1^2 + 2b x_1 x_2 + c x_2^2.
$$

---

## Definiteness of a Matrix

A symmetric matrix $A$ is:

- **Positive definite** if $x'Ax > 0$ for all $x \neq 0$
- **Negative definite** if $x'Ax < 0$ for all $x \neq 0$
- **Indefinite** if $x'Ax$ takes both positive and negative values

### Economic Meaning

- Positive definiteness corresponds to **convexity**.
- Negative definiteness corresponds to **concavity**.
- These properties determine whether a critical point is a minimum or maximum.

---

## Principal Minors and the Determinant Test

For a symmetric matrix, definiteness can be checked using **principal minors**.

### Example (2 × 2 case)

Let
$$
A =
\begin{bmatrix}
a & b \\
b & c
\end{pbatrix}.
$$

- $A$ is positive definite if:
  $$
  a > 0, \quad \det(A) = ac - b^2 > 0.
  $$

This test is especially useful in applied work, where symbolic eigenvalues
may be difficult to compute.

---

## Eigenvalues and Definiteness

An alternative characterization uses **eigenvalues**.

A symmetric matrix is:
- positive definite if all eigenvalues are positive,
- negative definite if all eigenvalues are negative.

Eigenvalues provide geometric intuition: they describe how a quadratic form
stretches space along principal directions.

---

## The Bordered Hessian

When optimizing a function subject to constraints, the **bordered Hessian**
is used to check second-order conditions.

### Structure

For a problem with one constraint, the bordered Hessian takes the form:
$$
H_B =
\begin{bmatrix}
0 & g_x' \\
g_x & H
\end{bmatrix},
$$
where:
- $g_x$ is the gradient of the constraint,
- $H$ is the Hessian of the Lagrangian.

### Interpretation

- The bordered Hessian incorporates both curvature and constraints.
- The sign pattern of its principal minors determines optimality.

---

## Input–Output Matrices in Economics

Linear algebra is central to **input–output analysis**.

Let $A$ be the matrix of technical coefficients, and let $x$ denote output.
The system:
$$
x = Ax + d
$$
can be rewritten as:
$$
(I - A)x = d.
$$

If $(I - A)$ is invertible, the solution is:
$$
x = (I - A)^{-1} d.
$$

### Economic Meaning

- $(I - A)^{-1}$ is the **Leontief inverse**.
- It captures direct and indirect production requirements.
- Invertibility reflects feasibility and stability of production systems.

---

## Why These Matrices Matter

Special matrices allow us to:
- characterize equilibrium behavior,
- determine optimality,
- analyze stability,
- understand economic structure.

They form the mathematical backbone of:
- constrained optimization,
- dynamic systems,
- general equilibrium models.

---

## What Comes Next

With these tools in place, we are ready to move beyond linear algebra and
introduce calculus-based methods, beginning with **multivariate calculus**
and optimization.
