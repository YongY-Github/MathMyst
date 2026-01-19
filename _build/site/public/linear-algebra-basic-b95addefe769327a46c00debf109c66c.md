# 2. Linear Algebra

## Matrix Basics

If $\mathbf{A} = (a_{ij})$ and $\mathbf{B} = (b_{ij})$ are two $m \times n$ matrices of same dimension, then $\mathbf{A} + \mathbf{B}$ is defined as $(a_{ij} + b_{ij})$. That is, we add element by element the two matrices.
Clearly $\mathbf{A} + \mathbf{B} = \mathbf{B} + \mathbf{A}$. The rule applies to matrix subtraction.

**Transpose of a matrix:** If \( \mathbf{A} \) is an \( m \times n \) matrix, then \( \mathbf{A}' \) is the \( n \times m \) matrix whose rows are the columns of \( \mathbf{A} \). So \( \mathbf{A}' = (a_{ji}) \). For example:

\[
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}' = \begin{bmatrix}
a & c \\
b & d
\end{bmatrix}
\]

Note: \( (\mathbf{A} + \mathbf{B})' = \mathbf{A}' + \mathbf{B}' \), however \( (\mathbf{A}\mathbf{B})' = \mathbf{B}'\mathbf{A}' \).

**Null matrix:** Has all elements as 0. Clearly \( \mathbf{A} + \mathbf{0}_{m,n} = \mathbf{0}_{m,n} + \mathbf{A} = \mathbf{A} \) for all \( m \times n \) matrices.

**Scalar multiplication:** If \( \mathbf{A} = (a_{ij}) \) then for any constant \( k \), define \( k\mathbf{A} = (k a_{ij}) \). That is, multiply each element in \( \mathbf{A} \) by \( k \).

**Matrix multiplication:** Say \( \mathbf{A} \) is \( m \times n \), and \( \mathbf{B} \) is \( n \times p \), then the \( m \times p \) matrix \( \mathbf{A}\mathbf{B} \) is the product of \( \mathbf{A} \) and \( \mathbf{B} \). For example:

\[
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
\begin{bmatrix}
e & f \\
g & h
\end{bmatrix}
= \begin{bmatrix}
ae + bg & af + bh \\
ce + dg & cf + dh
\end{bmatrix}
\]

and the matrices \( \mathbf{A} \) and \( \mathbf{B} \) are conformable.

**Diagonal matrix:** A square \( n \times n \) matrix \( \mathbf{A} \) is diagonal if all entries off the 'main diagonal' are zero, i.e.

\[
\mathbf{A} = \begin{bmatrix}
a_{11} & 0 & \cdots & 0 \\
0 & a_{22} & \cdots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \cdots & a_{nn}
\end{bmatrix}
\]

Note: The elements in the diagonal of \( \mathbf{A} \) are the same as those in \( \mathbf{A}' \).

**Trace of a square matrix:** If \( \mathbf{A} \) is a square matrix, the trace of \( \mathbf{A} \), denoted \( \operatorname{tr}(\mathbf{A}) \), is the sum of the elements on the main/leading diagonal of \( \mathbf{A} \).

**Identity matrix:** Denoted by \( \mathbf{I}_n \), the \( n \times n \) diagonal matrix with \( a_{ii} = 1 \) for all \( i \). That is:

\[
\mathbf{I}_n = \begin{bmatrix}
1 & 0 & \cdots & 0 \\
0 & 1 & \cdots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \cdots & 1
\end{bmatrix}
\]

**Symmetric matrix:** A square matrix \( \mathbf{A} \) is symmetric if \( \mathbf{A} = \mathbf{A}' \). The identity matrix and the square null matrix are symmetric.

## Idempotent matrix

A square matrix is said to be idempotent if \( \mathbf{A}^2 = \mathbf{A} \). Below is an example (try squaring the matrix and see what you get).

\[
\begin{bmatrix}
1 & 0 \\
0 & 0
\end{bmatrix}
\]

**Singular Matrix:** A matrix that is linearly dependent (in the columns or rows) is singular and has determinant of zero. Note that any two (or three) vectors \( \mathbf{x} \) and \( \mathbf{y} \) (and \( \mathbf{z} \)) are said to be linearly dependent iff one can be written as a scalar multiple of the other. Two vectors \( \mathbf{x} \neq \mathbf{0} \) and \( \mathbf{y} \neq \mathbf{0} \) are said to be **linearly independent** iff the ONLY solution to \( a\mathbf{x} + b\mathbf{y} = \mathbf{0} \) is \( a = 0 \) AND \( b = 0 \). And \( \mathbf{x} \) and \( \mathbf{y} \) are said to be **orthogonal**.

## Some Notes on Matrices

1. Usually \( \mathbf{A}\mathbf{B} \neq \mathbf{B}\mathbf{A} \). For example, try \( \mathbf{A} = \begin{bmatrix}2 & 0 \\ 3 & 1\end{bmatrix} \) and \( \mathbf{B} = \begin{bmatrix}0 & 1 \\ 0 & 0\end{bmatrix} \).

2. We can have \( \mathbf{A}\mathbf{B} = \mathbf{0} \) even if \( \mathbf{A} \) or \( \mathbf{B} \) are not zero. For example, try \( \mathbf{A} = \begin{bmatrix}6 & -12 \\ -3 & 6\end{bmatrix} \) and \( \mathbf{B} = \begin{bmatrix}12 & 6 \\ 6 & 3\end{bmatrix} \).

3. Say, \( \mathbf{A} = \begin{bmatrix}4 & 8 \\ 1 & 2\end{bmatrix} \), \( \mathbf{B} = \begin{bmatrix}2 & 1 \\ 2 & 2\end{bmatrix} \), and \( \mathbf{C} = \begin{bmatrix}-2 & 1 \\ 4 & 2\end{bmatrix} \). We find that \( \mathbf{A}\mathbf{B} = \mathbf{A}\mathbf{C} \) even though \( \mathbf{B} \neq \mathbf{C} \).

4. Say \( \mathbf{A} \) and \( \mathbf{B} \) are singular matrices. Then \( \mathbf{A}\mathbf{B} \) will not be zero, although the product will be a singular matrix.

## Systems of Equations in Matrix Form

One of the uses of linear algebra in economics is to represent and then solve systems of equations. For instance, consider the system of two equations:

\[
3x_1 + 4x_2 = 5 \\
7x_1 - 2x_2 = 2
\]

Here, we can define:

\[
\mathbf{A} = \begin{pmatrix} 3 & 4 \\ 7 & -2 \end{pmatrix}, \quad \mathbf{x} = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}, \quad \mathbf{b} = \begin{pmatrix} 5 \\ 2 \end{pmatrix}
\]

Then we see that:

\[
\mathbf{A}\mathbf{x} = \begin{pmatrix} 3 & 4 \\ 7 & -2 \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \end{pmatrix} = \begin{pmatrix} 3x_1 + 4x_2 \\ 7x_1 - 2x_2 \end{pmatrix}
\]

The original system is in fact equivalent to the matrix form:

\[
\mathbf{A}\mathbf{x} = \mathbf{b}