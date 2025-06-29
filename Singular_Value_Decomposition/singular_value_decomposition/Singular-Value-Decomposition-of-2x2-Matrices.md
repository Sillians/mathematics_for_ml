## **Singular Value Decomposition of 2×2 Matrices**

---

### **What Is Singular Value Decomposition (SVD)?**

Singular Value Decomposition expresses any real matrix \$A\$ (not necessarily square) as:

$$
A = U \Sigma V^{\mathsf T}
$$

Where:

* $A$ is a real $`m \times n`$ matrix.
* $U$ is an $`m \times m`$ orthogonal matrix (columns are orthonormal eigenvectors of $`AA^{\mathsf T}`$).
* $V$ is an $`n \times n`$ orthogonal matrix (columns are orthonormal eigenvectors of $`A^{\mathsf T}A`$).
* $`\Sigma`$ is an $`m \times n`$ diagonal matrix with non-negative real numbers on the diagonal (the **singular values**).

In the **2×2 case**, $A$ is a $`2 \times 2`$ matrix, so:

* $`U, V`$ are $`2 \times 2`$ orthogonal matrices,
* $`\Sigma = \begin{bmatrix} \sigma\_1 & 0 \ 0 & \sigma\_2 \end{bmatrix}`$, with $`\sigma\_1 \ge \sigma\_2 \ge 0`$.

---

### **Identifying True Statements Regarding Singular Value Decomposition**

| Statement                                                                               | True?       | Reason                                      |        |                                          |
|-----------------------------------------------------------------------------------------|-------------|---------------------------------------------| ------ | ---------------------------------------- |
| The singular values of $A$ are the square roots of the eigenvalues of $`A^{\mathsf T}A`$ | ✅ True      | Definition                                  |        |                                          |
| $U$ and $V$ are always orthogonal                                                       | ✅ True      | Guaranteed by SVD                           |        |                                          |
| If $A$ is symmetric, $`U = V`$                                                          | ✅ Sometimes | When $A$ is symmetric and positive semi-definite |        |                                          |
| Singular values can be negative                                                         | ❌ False     | Always non-negative                         |        |                                          |
| $`\det(A) = \sigma\_1  \sigma\_2`$                                                      | ✅ True      | Determinant of orthogonal matrices is ±1 |

---

### **Finding the Columns of the Third Matrix Given Part of an SVD**

Given:

* $`A = U \Sigma V^{\mathsf T}`$
* Suppose $U$, $`\Sigma`$ are known.

To find **$V$**:

1. Rearrange: $`AV = U \Sigma`$
   Multiply both sides on the right by $V$:

   $$
   A = U \Sigma V^{\mathsf T} \Rightarrow AV = U\Sigma
   $$

2. Solve for columns: if \$v\_1\$ is a column of \$V\$, then:

   $$
   Av_1 = \sigma_1 u_1 \quad \text{and} \quad Av_2 = \sigma_2 u_2
   $$

   So:

   $$
   v_1 = A^{-1}(\sigma_1 u_1), \text{ normalized}
   $$

If $A$ has rank 1, then $`v\_2`$ can be any orthonormal vector orthogonal to $`v\_1`$.

---

### **Determining the Columns of the First Matrix Given Part of an SVD**

Given:

* $`A = U \Sigma V^{\mathsf T}`$
* Suppose $`V`$, $`\Sigma`$ are known.

To find **$U$**:

1. Rearrange: $`A V = U \Sigma`$
2. Use:

   $$
   u_i = \frac{1}{\sigma_i} A v_i
   $$

   Then normalize to ensure unit length.

If $A$ has rank 1, then the second column of $U$ can be any orthonormal vector perpendicular to the first.

---

### **The Singular Value Decomposition of a 2×2 Matrix: Step-by-Step**

Given a real $`2 \times 2`$ matrix $A$, here’s how to compute its SVD:

#### **Step 1: Compute $`A^{\mathsf T}A`$**

$$
A^{\mathsf T}A \text{ is symmetric and positive semi-definite}
$$

#### **Step 2: Find Eigenvalues and Eigenvectors of $`A^{\mathsf T}A`$**

* The eigenvalues are $`λ\_1, λ\_2`$ with $`λ\_1 \ge λ\_2 \ge 0`$
* The singular values are:

$$
\sigma_1 = \sqrt{\lambda_1}, \quad \sigma_2 = \sqrt{\lambda_2}
$$

#### **Step 3: Construct $V$**

* $V$ has orthonormal eigenvectors of $`A^{\mathsf T}A`$ as its columns

#### **Step 4: Construct $U$**

* Use $`u\_i = \frac{1}{\sigma\_i} A v\_i`$
* Normalize $`u\_i`$

#### **Step 5: Construct $`\Sigma`$**

$$
\Sigma = \begin{bmatrix} \sigma_1 & 0 \\ 0 & \sigma_2 \end{bmatrix}
$$

#### **Final Assembly**

$$
A = U \Sigma V^{\mathsf T}
$$

---

### **Example**

Let:

$$
A = \begin{bmatrix} 3 & 1 \\ 0 & 2 \end{bmatrix}
$$

1. Compute $`A^{\mathsf T}A`$:

$$
A^{\mathsf T}A = \begin{bmatrix} 3 & 0 \\ 1 & 2 \end{bmatrix} \begin{bmatrix} 3 & 1 \\ 0 & 2 \end{bmatrix} = \begin{bmatrix} 9 & 3 \\ 3 & 5 \end{bmatrix}
$$

2. Find eigenvalues of $`A^{\mathsf T}A`$:
   Solve: $`\det(A^{\mathsf T}A - \lambda I) = 0`$

$$
\lambda^2 - 14\lambda + 36 = 0 \Rightarrow \lambda_1 = 12, \lambda_2 = 2
\Rightarrow \sigma_1 = \sqrt{12},\; \sigma_2 = \sqrt{2}
$$

3. Eigenvectors → $V$, compute $`U = \frac{1}{\sigma\_i}Av\_i`$, and then assemble the full SVD.

---

### **Summary**

| Matrix        | Role in SVD                                        |
|---------------| -------------------------------------------------- |
| $U$           | Orthonormal basis for the output space             |
| $`\Sigma`$    | Diagonal scaling matrix (with singular values)     |
| $V$           | Orthonormal basis for the input space              |
| $`\sigma\_1`$ | Largest stretch direction                          |
| $`\sigma\_2`$ | Second largest stretch (or zero if rank deficient) |


SVD provides a geometric view: **rotate → scale → rotate**. 
For $`2 \times 2`$ matrices, it enables easy analysis of transformation behavior, compressibility, and stability.
