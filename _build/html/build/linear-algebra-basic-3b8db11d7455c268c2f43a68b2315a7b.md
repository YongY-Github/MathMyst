# Linear Algebra: Basic Concepts

Linear algebra provides the language and tools for representing and solving
systems of equations, analyzing economic models, and studying optimization
problems. This chapter introduces the basic objects and operations that will
be used throughout the rest of these notes.

The emphasis is on **intuition**, **structure**, and **economic relevance**,
rather than formal proofs.

---

## Scalars, Vectors, and Matrices

A **scalar** is a single number, such as income, price, or an interest rate.

A **vector** is an ordered collection of numbers. For example, a vector of
outputs from different sectors can be written as
$$
x =
\begin{bmatrix}
x_1 \\
x_2 \\
\vdots \\
x_n
\end{bmatrix}.
$$

A **matrix** is a rectangular array of numbers. For example,
$$
A =
\begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{bmatrix}.
$$

Matrices are used to represent:
- systems of linear equations,
- technological relationships,
- linear transformations.

---

## Matrix Operations

### Matrix Addition and Scalar Multiplication

Two matrices of the same dimension can be added element by element:
$$
A + B = [a_{ij} + b_{ij}].
$$

A matrix can be multiplied by a scalar $c$:
$$
cA = [c a_{ij}].
$$

These operations behave much like addition and multiplication of numbers.

---

### Matrix Multiplication

Matrix multiplication is defined so that dimensions must be compatible.
If $A$ is an $m \times n$ matrix and $B$ is an $n \times k$ matrix, then
$AB$ is an $m \times k$ matrix.

The $(i,j)$ element of $AB$ is given by
$$
(AB)_{ij} = \sum_{k} a_{ik} b_{kj}.
$$

Matrix multiplication is **not commutative** in general:
$$
AB \neq BA.
$$

This non-commutativity is economically important: the *order* of
transformations matters.

---

## Transpose of a Matrix

The **transpose** of a matrix $A$, denoted $A'$, is obtained by swapping rows
and columns:
$$
(A')_{ij} = a_{ji}.
$$

For example,
$$
A =
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix},
\qquad
A' =
\begin{bmatrix}
1 & 3 \\
2 & 4
\end{bmatrix}.
$$

### Symmetric Matrices

A matrix is **symmetric** if
$$
A = A'.
$$

Symmetric matrices arise naturally in:
- quadratic forms,
- Hessian matrices,
- second-order conditions in optimization.

---

## Identity and Zero Matrices

The **identity matrix** $I$ satisfies
$$
AI = IA = A.
$$

For example,
$$
I =
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}.
$$

The **zero matrix** has all elements equal to zero and acts as the additive
identity.

---

## Inverse of a Matrix

A square matrix $A$ is **invertible** if there exists a matrix $A^{-1}$ such
that
$$
AA^{-1} = A^{-1}A = I.
$$

### Interpretation

If $Ax = b$, then multiplying both sides by $A^{-1}$ yields
$$
x = A^{-1} b.
$$

Thus, the inverse matrix allows us to solve systems of linear equations.

Not all matrices are invertible. Non-invertibility typically reflects:
- redundancy,
- linear dependence,
- the absence of a unique solution.

---

## Determinant of a Matrix

The **determinant** of a square matrix is a scalar value that summarizes key
properties of the matrix.

For a $2 \times 2$ matrix,
$$
A =
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix},
$$
the determinant is given by
$$
\det(A) = ad - bc.
$$

### Key Properties

- If $\det(A) = 0$, the matrix is **singular** (not invertible).
- If $\det(A) \neq 0$, the matrix is invertible.
- The determinant reflects the *volume-scaling* effect of a linear
  transformation.

---

## Cramer’s Rule

Cramer’s Rule provides an explicit solution to a system of linear equations
$$
Ax = b,
$$
when $A$ is invertible.

For each component $x_i$, the solution is
$$
x_i = \frac{\det(A_i)}{\det(A)},
$$
where $A_i$ is obtained by replacing the $i$-th column of $A$ with $b$.

### Remarks

- Cramer’s Rule is mainly of **theoretical interest**.
- It shows how solutions depend on determinants.
- It is inefficient for large systems but conceptually illuminating.

---

## Linear Dependence and Rank (Intuition)

The columns of a matrix are **linearly dependent** if one column can be
expressed as a linear combination of the others.

Linear dependence implies:
- loss of information,
- non-invertibility,
- multiple or no solutions.

The **rank** of a matrix measures the number of linearly independent rows or
columns.

---

## Why Linear Algebra Matters in Economics

Linear algebra underpins:
- equilibrium analysis,
- comparative statics,
- input–output models,
- optimization problems,
- dynamic systems.

Later chapters will show how these basic tools are used to analyze:
- stability,
- convexity,
- optimality conditions.

---

## What Comes Next

In the next chapter, we extend these ideas to **special matrices** that play a
central role in optimization and economic modeling, including:
- Jacobian matrices,
- Hessian matrices,
- quadratic forms and definiteness.
