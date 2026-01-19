# 2. Linear Algebra

## Matrix Basics

[cite_start]**Matrix addition and subtraction**: If $A=(a_{ij})$ and $B=(b_{ij})$ are two $m\times n$ matrices of same dimension, then $A+B$ is defined as $(a_{ij}+b_{ij})$[cite: 28]. [cite_start]That is, we add element by element the two matrices[cite: 29]. [cite_start]Clearly $A+B=B+A$[cite: 29]. [cite_start]The rule applies to matrix subtraction[cite: 29].

[cite_start]**Transpose of a matrix**: If A is a $m\times n$ matrix, the $A'$ is the $n\times m$ matrix whose rows are the columns of A[cite: 30]. [cite_start]So $A^{\prime}=(a_{ji})$[cite: 30]. For example:
* [cite_start]$[\begin{matrix}2&-3\\ -4&5\end{matrix}]^{\prime}=[\begin{matrix}2&-4\\ -3&5\end{matrix}]$ [cite: 32]
* [cite_start]**Note**: $(A+B)^{\prime}=A^{\prime}+B^{\prime}$ [cite: 31]
* [cite_start]**Note**: $(AB)^{\prime}=B^{\prime}A^{\prime}$ [cite: 33]

[cite_start]**Null matrix**: Has all elements as 0[cite: 34]. [cite_start]Clearly $A+O_{m,n}=0_{m,n}+A=A$ for all $m\times n$ matrices[cite: 34].

[cite_start]**Scalar multiplication**: If $A=(a_{ij})$ then for any constant $k$ define $kA=(ka_{ij})$[cite: 35]. [cite_start]That is, multiply each element in A by $k$[cite: 35].

[cite_start]**Matrix multiplication**: Say A is $m\times n$ and B is $n\times p$ then the $m\times p$ matrix AB is the product of A and B[cite: 36]. For example:
* [cite_start]$[\begin{matrix}1&2\\ 4&0\end{matrix}][\begin{matrix}3&-1\\ 4&3\end{matrix}]=[\begin{matrix}11&5\\ 12&-4\end{matrix}]$ [cite: 37]
* [cite_start]The matrices A and B are **comformable**[cite: 38].

[cite_start]**Diagonal matrix**: A square $n\times n$ matrix A is diagonal if all entries off the 'main diagonal' are zero[cite: 39].
[cite_start]$A=[\begin{matrix}a_{11}&0&...&0\\ 0&a_{22}&...&0\\ \vdots&\vdots&\vdots&\vdots\\ 0&0&...&a_{nn}\end{matrix}]$ [cite: 40]
* [cite_start]**Note**: The elements in the diagonal of A are the same as those in $A'$[cite: 41].

[cite_start]**Trace of a square matrix**: If A is a square, the trace of A, denoted $tr(A)$, is the sum of the elements on the main/leading diagonal of A[cite: 42, 43].

[cite_start]**Identity matrix**: Denoted by $I_{n}$, the $n\times n$ diagonal matrix with $a_{ij}=1$ for all $i$[cite: 44, 46].
[cite_start]$A=[\begin{matrix}1&0&...&0\\ 0&1&...&0\\ \vdots&\vdots&\vdots&\vdots\\ 0&0&...&1\end{matrix}]$ [cite: 45]

[cite_start]**Symmetric matrix**: A square matrix A is symmetric if $A=A^{\prime}$[cite: 47]. [cite_start]The identity matrix and the square null matrix are symmetric[cite: 47].

---

[cite_start]**Idempotent matrix**: A square matrix is said to be idempotent if $A^{2}=A$[cite: 48]. 
[cite_start]Example: $A=[\begin{matrix}2&-2&-4\\ -1&3&4\\ 1&-2&-3\end{matrix}]$ [cite: 49]

[cite_start]**Singular Matrix**: A matrix that is linearly dependent (in the columns or rows) is singular and has a determinant of zero[cite: 50]. 
* [cite_start]Any two (or three) vectors $x$ and $y$ (and $z$) are linearly dependent iff one can be written as a scalar multiple of the other[cite: 51].
* [cite_start]Two vectors $x\ne0$ and $y\ne0$ are **linearly independent** iff the only solution to $ax+by=0$ is $a=0$ and $b=0$[cite: 52].
* [cite_start]$x$ and $y$ are said to be **orthogonal**[cite: 53].

### Some Notes on Matrices
1. [cite_start]Usually $AB\ne BA$[cite: 55].
2. [cite_start]We can have $AB=0$ even if A or B are not zero[cite: 56]. 
3. [cite_start]We can find that $AB=AC$ even though $B\ne C$[cite: 58].
4. [cite_start]If A and B are singular matrices, $AB$ will not be zero, although the product will be a singular matrix[cite: 59].

---

## Systems of Equations in Matrix Form
[cite_start]One of the uses of linear algebra in economics is to represent and then solve systems of equations[cite: 61]. For instance:
[cite_start]$3x_{1}+4x_{2}=5$ [cite: 68]
[cite_start]$7x_{1}-2x_{2}=2$ [cite: 68]

[cite_start]This can be defined as $Ax=b$[cite: 76], where:
[cite_start]$A = [\begin{matrix}3&4\\ 7&-2\end{matrix}]$, $x=[\begin{matrix}x_{1}\\ x_{2}\end{matrix}]$, and $b=[\begin{matrix}5\\ 2\end{matrix}]$ [cite: 71, 73, 136]

---

## Matrix Inversion
[cite_start]In fact, $A^{-1}A=AA^{-1}=I$[cite: 94]. [cite_start]To find the inverse of $A=[\begin{matrix}1&-2\\ 3&4\end{matrix}]$[cite: 79]:
1. [cite_start]Find a matrix such that $[\begin{matrix}1&-2\\ 3&4\end{matrix}][\begin{matrix}a&b\\ c&d\end{matrix}]=[\begin{matrix}10&0\\ 0&10\end{matrix}]$[cite: 81].
2. [cite_start]The value 10 is the determinant of A[cite: 85].
3. [cite_start]The resulting matrix is $\frac{1}{10}[\begin{matrix}4&2\\ -3&1\end{matrix}]$[cite: 90].

### Properties of the Inverse
* [cite_start]**Property 1**: $(A^{-1})^{-1}=A$ for any nonsingular matrix A[cite: 96, 97].
* [cite_start]**Property 2**: $|A^{-1}|=\frac{1}{|A|}$[cite: 101].
* [cite_start]**Property 3**: The inverse of matrix A is unique[cite: 100].
* [cite_start]**Property 4**: $(A^{\prime})^{-1}=(A^{-1})^{\prime}$[cite: 103].
* [cite_start]**Property 5**: If A and B are nonsingular, AB is also nonsingular[cite: 104].
* [cite_start]**Property 6**: $(AB)^{-1}=B^{-1}A^{-1}$[cite: 106].

---

## The Determinant of a Matrix
[cite_start]The determinant is a scalar-value associated with a square non-singular matrix, denoted as $|A|$[cite: 108].
* [cite_start]For a $2\times2$ matrix $A=[\begin{matrix}a_{11}&a_{12}\\ a_{21}&a_{22}\end{matrix}]$, $|A|=a_{11}a_{22}-a_{12}a_{21}$[cite: 113].
* [cite_start]The **Laplace expansion** is often used for higher orders[cite: 116].

### Notes on Determinants
1. [cite_start]$|A|=|A^{\prime}|$ and $|A|\cdot|B|=|B|\cdot|A|$[cite: 122].
2. [cite_start]Interchanging any two rows or columns changes the sign[cite: 123].
3. [cite_start]Multiplying a single row/column by a scalar $k$ multiplies the determinant by $k$[cite: 124].
4. [cite_start]Adding a multiple of one row/column to another does not change the determinant[cite: 125].
5. [cite_start]The determinant of a triangular matrix is the product of the principal diagonal elements[cite: 126].
6. [cite_start]If any row or column equals zero, the determinant is zero[cite: 127].
7. [cite_start]If two rows or columns are linearly dependent, the determinant is zero[cite: 128].

---

## Finding the Inverse of Matrix
[cite_start]The inverse is defined as: $A^{-1}=\frac{1}{|A|}adjA$[cite: 132].
1. [cite_start]**Step 1**: Find the minor $|M_{ij}|$, the determinant of the submatrix after deleting the $i$th row and $j$th column[cite: 138].
2. [cite_start]**Step 2**: The cofactor $|C_{ij}|=(-1)^{i+j}|M_{ij}|$[cite: 141, 143].
3. [cite_start]**Step 3**: The adjoint matrix is the transpose of the cofactor matrix[cite: 144].

---

## Cramer's Rule
[cite_start]A simplified method for solving $Ax=b$ using determinants[cite: 151, 152].
[cite_start]$x_{i}=\frac{|\Delta_{i}|}{|\Delta|}$ [cite: 158]
[cite_start]Where $\Delta_{i}$ is the matrix A with the $i$th column replaced by vector $b$[cite: 157].