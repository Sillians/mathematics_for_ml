## **Computing the Singular Values of a Matrix**

---

### **1. What Are Singular Values?**

The **singular values** of a real or complex matrix $`A \in \mathbb{R}^{m \times n}`$ are 
the non-negative square roots of the eigenvalues of $`A^\top A`$ (or $`A A^\top`$). They are denoted by:

$$
\sigma_1 \ge \sigma_2 \ge \cdots \ge \sigma_r > 0,\quad \text{with } r = \text{rank}(A)
$$

These values tell us how the transformation defined by $A$ stretches or compresses vectors in different directions.

---

### **2. How to Compute the Singular Values of a Matrix**

Given $`A \in \mathbb{R}^{m \times n}`$:

1. Compute $`A^\top A`$ (if $`m \le n`$) or $`A A^\top`$ (if $`m > n`$).
2. Find the eigenvalues $`\lambda_1, \dots, \lambda_r`$ of this matrix.
3. Take square roots: $`\sigma_i = \sqrt{\lambda_i}`$
4. Sort the values in descending order.

The result is the **set of singular values** of $A$.

---

### **3. Finding the Singular Values of a Square Matrix**

If $`A \in \mathbb{R}^{n \times n}`$, then:

* Compute $`A^\top A \in \mathbb{R}^{n \times n}`$.


* Diagonalize $`A^\top A = Q \Lambda Q^\top`$, where $`\Lambda`$ has eigenvalues on the diagonal.


* Singular values are:

  $$
  \sigma_i = \sqrt{\lambda_i(A^\top A)}
  $$

**Example:**

$$
A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}
\quad \Rightarrow \quad
A^\top A = \begin{bmatrix} 10 & 14 \\ 14 & 20 \end{bmatrix}
\Rightarrow \text{eigenvalues: } \lambda_1, \lambda_2
\Rightarrow \sigma_i = \sqrt{\lambda_i}
$$

---

### **4. Finding the Singular Values of a Rectangular Matrix**

If $`A \in \mathbb{R}^{m \times n}`$ where $`m \ne n`$:

* If $`m < n`$: use $`A A^\top \in \mathbb{R}^{m \times m}`$


* If $`m > n`$: use $`A^\top A \in \mathbb{R}^{n \times n}`$

Then proceed as in the square case:

* Diagonalize the Gram matrix
* Take square roots of eigenvalues

**Example:**

$$
A = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 2 & 0 \end{bmatrix}
\quad \Rightarrow \quad
A A^\top = \begin{bmatrix} 1 & 0 \\ 0 & 4 \end{bmatrix}
\Rightarrow \sigma_1 = 2,\ \sigma_2 = 1
$$

---

### **5. Identifying True Statements About Singular Values**

| Statement                                                                    | True/False           | Reason                                                               |
| ---------------------------------------------------------------------------- | -------------------- | -------------------------------------------------------------------- |
| Singular values are always real and non-negative                             | **True**             | Eigenvalues of $`A^\top A`$ are real and ≥ 0                           |
| The number of non-zero singular values equals the rank of the matrix         | **True**             | Each non-zero singular value corresponds to an independent dimension |
| For symmetric matrices, singular values equal absolute values of eigenvalues | **True**             | Because $`A^\top = A`$, and eigenvalues may be negative                |
| $`\|A\|_2 = \sigma_1`$ (operator norm)                                         | **True**             | The largest singular value equals the maximum stretch                |
| Singular values depend on the eigenvalues of $A$                             | **False in general** | Only for special matrices (e.g., symmetric or normal matrices)       |

---

### **6. Summary of Key Properties**

| Concept                  | Description                                                                         |         |                                      |
| ------------------------ |-------------------------------------------------------------------------------------| ------- | ------------------------------------ |
| **Definition**           | $`\sigma_i = \sqrt{\lambda_i(A^\top A)}`$                                           |         |                                      |
| **Count**                | $`\min(m, n)`$ singular values, all $`\ge 0`$                                       |         |                                      |
| **Rank**                 | Number of non-zero $`\sigma_i`$ values                                              |         |                                      |
| **Norm**                 | $`\|A\|_2 = \sigma_1`$                                                              |         |                                      |
| **Determinant (square)** | $`(\det(A) = \prod \sigma\_i)`$ if $A$ is square                                    |
| **SVD**                  | $`A = U \Sigma V^\top`$, where $`\Sigma`$ contains the $`\sigma_i`$ on the diagonal |         |                                      |

---

### **Final Note**

Singular values are crucial in:

* Principal Component Analysis (PCA)
* Condition number computation
* Matrix approximation (e.g., low-rank SVD)
* Solving ill-posed linear systems

They provide deep geometric insight into how a matrix transforms space — capturing both scaling and rank information.
