# 2. Linear Algebra

## Matrix Basics

**Matrix addition and subtraction**: If $A=(a_{ij})$ and $B=(b_{ij})$ are two $m\times n$ matrices of same dimension, then $A+B$ is defined as $(a_{ij}+b_{ij})$. That is, we add element by element the two matrices. Clearly $A+B=B+A$. The rule applies to matrix subtraction.

**Transpose of a matrix**: If A is a $m\times n$ matrix, then $A'$ is the $n\times m$ matrix whose rows are the columns of A. So $A^{\prime}=(a_{ji})$. 

**Example and Notes**:
* $[\begin{matrix}2&-3\\ -4&5\end{matrix}]^{\prime}=[\begin{matrix}2&-4\\ -3&5\end{matrix}]$
* $(A+B)^{\prime}=A^{\prime}+B^{\prime}$
* $(AB)^{\prime}=B^{\prime}A^{\prime}$

**Null matrix**: Has all elements as 0. Clearly $A+O_{m,n}=0_{m,n}+A=A$ for all $m\times n$ matrices.

**Scalar multiplication**: If $A=(a_{ij})$ then for any constant $k$ define $kA=(ka_{ij})$. That is, multiply each element in A by $k$.

**Matrix multiplication**: Say A is $m\times n$ and B is $n\times p$ then the $m\times p$ matrix AB is the product of A and B. For example:
* $[\begin{matrix}1&2\\ 4&0\end{matrix}][\begin{matrix}3&-1\\ 4&3\end{string}]=[\begin{matrix}11&5\\ 12&-4\end{matrix}]$
* The matrices A and B are **comformable**.

**Diagonal matrix**: A square $n\times n$ matrix A is diagonal if all entries off the 'main diagonal' are zero, i.e.
$A=[\begin{matrix}a_{11}&0&...&0\\ 0&a_{22}&...&0\\ \vdots&\vdots&\vdots&\vdots\\ 0&0&...&a_{nn}\end{matrix}]$
Note: The elements in the diagonal of A are the same as those in $A'$.

**Trace of a square matrix**: If A is a square, the trace of A, denoted $tr(A)$, is the sum of the elements on the main/leading diagonal of A.

**Identity matrix**: Denoted by $I_{n}$, the $n\times n$ diagonal matrix with $a_{ij}=1$ for all $i$. That is:
$A=[\begin{matrix}1&0&...&0\\ 0&1&...&0\\ \vdots&\vdots&\vdots&\vdots\\ 0&0&...&1\end{matrix}]$

**Symmetric matrix**: A square matrix A is symmetric if $A=A^{\prime}$. The identity matrix and the square null matrix are symmetric.

---

**Idempotent matrix**: A square matrix is said to be idempotent if $A^{2}=A$. 
Example: $A=[\begin{matrix}2&-2&-4\\ -1&3&4\\ 1&-2&-3\end{matrix}]$

**Singular Matrix**: A matrix that is linearly dependent (in the columns or rows) is singular and has a determinant of zero. 
* Note that any two (or three) vectors $x$ and $y$ (and $z$) are said to be linearly dependent iff one can be written as a scalar multiple of the other.
* Two vectors $x\ne0$ and $y\ne0$ are said to be **LINEARLY INDEPENDENT** iff the ONLY solution to $ax+by=0$ is $a=0$ AND $b=0$. And $x$ and $y$ are said to be **ORTHOGONAL**.

### Some Notes on Matrices
1. Usually $AB\ne BA$.
2. We can have $AB=0$ even if A or B are not zero. 
3. We find that $AB=AC$ even though $B\ne C$.
4. Say A and B are singular matrices. Then $AB$ will not be zero, although the product will be a singular matrix.

---

## Systems of Equations in Matrix Form
One of the uses of linear algebra in economics is to represent and then solve systems of equations. For instance, consider the system:
$3x_{1}+4x_{2}=5$
$7x_{1}-2x_{2}=2$

This is equivalent to the matrix form $Ax=b$ where:
$A = [\begin{matrix}3&4\\ 7&-2\end{matrix}]$, $x=[\begin{matrix}x_{1}\\ x_{2}\end{matrix}]$, and $b=[\begin{matrix}5\\ 2\end{matrix}]$

---

## Matrix Inversion
In fact, $A^{-1}A=AA^{-1}=I$. To find the inverse of $A=[\begin{matrix}1&-2\\ 3&4\end{matrix}]$:
1. Think of another matrix such that $[\begin{matrix}1&-2\\ 3&4\end{matrix}][\begin{matrix}a&b\\ c&d\end{matrix}]=[\begin{matrix}10&0\\ 0&10\end{matrix}]$.
2. The 10 comes from the determinant of A.
3. The matrix $\frac{1}{10}[\begin{matrix}4&2\\ -3&1\end{matrix}]$ is the inverse of A.

### Properties of the Inverse
* **Property 1**: For any nonsingular matrix A, $(A^{-1})^{-1}=A$.
* **Property 2**: The determinant of the inverse is the reciprocal of the determinant: $|A^{-1}|=\frac{1}{|A|}$.
* **Property 3**: The inverse of matrix A is unique.
* **Property 4**: The inverse of the transpose is equal to the transpose of the inverse: $(A^{\prime})^{-1}=(A^{-1})^{\prime}$.
* **Property 5**: If A and B are nonsingular, AB is also nonsingular.
* **Property 6**: The inverse of the product of two matrices: $(AB)^{-1}=B^{-1}A^{-1}$.

---

## The Determinant of a Matrix
The determinant is a scalar-value uniquely associated with a square non-singular matrix, denoted as $|A|$.
* For a $2\times2$ matrix $A=[\begin{matrix}a_{11}&a_{12}\\ a_{21}&a_{22}\end{matrix}]$, the determinant is defined as $|A|=a_{11}a_{22}-a_{12}a_{21}$.
* For a $3\times3$ matrix, the Laplace expansion is often used.

### Notes on Determinants
1. $|A|=|A^{\prime}|$ and $|A|\cdot|B|=|B|\cdot|A|$.
2. Interchanging any two rows or columns changes the sign of the determinant.
3. Multiplying a single row or column by a scalar multiplies the determinant by that scalar.
4. Addition or subtraction of a nonzero multiple of a row/column to another does not change the determinant.
5. The determinant of a triangular matrix is the product of the diagonal elements.
6. If any rows or columns equal zero, the determinant is zero.
7. If two rows or columns are linearly dependent, the determinant is zero.

---

## Finding the Inverse of Matrix
Defined as: $A^{-1}=\frac{1}{|A|}adjA$.

**Step 1**: The minor $|M_{ij}|$ is the determinant of the submatrix formed by deleting the $i$th row and $j$th column.
**Step 2**: The cofactor $|C_{ij}|=(-1)^{i+j}|M_{ij}|$.
**Step 3**: The adjoint matrix is the transpose of the cofactor matrix.

---

## Cramer's Rule
A simplified method for solving $Ax=b$ through determinants.
$x_{i}=\frac{|\Delta_{i}|}{|\Delta|}$
Where $\Delta_{i}$ is the matrix A with the $i$th column replaced by the $b$ vector.