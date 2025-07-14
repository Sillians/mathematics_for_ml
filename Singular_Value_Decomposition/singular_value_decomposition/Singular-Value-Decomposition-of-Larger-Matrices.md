## **Singular Value Decomposition (SVD) of Larger Matrices**

---

### **I. Overview of Singular Value Decomposition**

Let $A$ be a real $`m \times n`$ matrix ($`m \ge n`$ without loss of generality). Then the **Singular Value Decomposition** of $A$ is:

$$
A = U \Sigma V^\mathsf{T}
$$

* $`U \in \mathbb{R}^{m \times m}`$: orthogonal matrix whose columns are **left singular vectors**.


* $`V \in \mathbb{R}^{n \times n}`$: orthogonal matrix whose columns are **right singular vectors**.


* $`\Sigma \in \mathbb{R}^{m \times n}`$: diagonal matrix with nonnegative entries $`\sigma\_1 \ge \sigma\_2 \ge \dots \ge \sigma\_r > 0`$ on the diagonal (called **singular values**), where $`r = \text{rank}(A)`$.

In the **reduced SVD**, we write:

$$
A = U_r \Sigma_r V_r^\mathsf{T}
$$

with:

* $`U\_r \in \mathbb{R}^{m \times r}`$


* $`\Sigma\_r \in \mathbb{R}^{r \times r}`$


* $`V\_r \in \mathbb{R}^{n \times r}`$

---

### **II. Finding the Third Factor in the SVD of a Rectangular Matrix**

(*Finding $V$ — the matrix of right singular vectors*)

1. Compute the symmetric matrix:

$$
A^\mathsf{T}A = V \Lambda V^\mathsf{T}
$$



* $`A^\mathsf{T}A`$ is positive semi-definite.


* The eigenvalues of $`A^\mathsf{T}A`$ are $`\lambda\_i = \sigma\_i^2`$.


* The columns of $V$ are orthonormal eigenvectors of $`A^\mathsf{T}A`$.

2. Then,

$$
\sigma_i = \sqrt{\lambda_i}, \quad \text{and} \quad v_i = \text{eigenvectors of } A^\mathsf{T}A
$$

The matrix $V$ is constructed by stacking the $`v\_i`$.

---

### **III. Finding the First Factor in the SVD of a Rectangular Matrix**

(*Finding $U$ — the matrix of left singular vectors*)

Once $V$ and the singular values $`\sigma\_i`$ are known:

$$
u_i = \frac{1}{\sigma_i} A v_i, \quad i = 1, \dots, r
$$

* These vectors $`u\_i`$ are orthonormal if $`A v\_i \neq 0`$.


* The $`u\_i`$ form the first $r$ columns of $`U\_r`$.


* If $`m > r`$, then $U$ can be completed with orthonormal vectors spanning the null space of $`A^\mathsf{T}`$.

---

### **IV. Finding the First Factor: Advanced Cases**

#### **Case 1: Zero Singular Values**

* If $`\sigma\_i = 0`$, then $`A v\_i = 0`$, and $`v\_i`$ lies in $`\ker(A)`$.


* Such $`v\_i`$ do not contribute to the image of $A$.



* The corresponding $`u\_i`$ are not defined by $`u\_i = \frac{1}{\sigma\_i} A v\_i`$, so we only use $`r = \text{rank}(A)`$ nonzero singular values to define the image.

#### **Case 2: Multiple or Repeated Singular Values**

* If $`\sigma\_i = \sigma\_j`$ (e.g., $`\sigma\_i = \sigma\_j = 5`$), then the subspace spanned by $`{u\_i, u\_j}`$ must be orthonormal, but $`A v\_i`$ and $`A v\_j`$ may not be.


* In this case, we **orthonormalize** the vectors $`{A v\_i}`$ using **Gram-Schmidt** or QR **decomposition** to maintain **orthogonality**.

---

### **V. Finding the First Factor: Cases Requiring Orthogonalization**

Numerical or geometric situations might require explicit orthogonalization:

#### **Scenario:**

* The computed vectors $`A v\_i`$ are linearly dependent or numerically unstable.


* This occurs especially when singular values are close or when working with large ill-conditioned matrices.


#### **Solution:**

Let $`W = [A v\_1, A v\_2, \dots, A v\_r]`$

1. Apply **QR Decomposition** to $W$:

$$
W = Q R, \quad \text{where } Q \in \mathbb{R}^{m \times r}, \ R \in \mathbb{R}^{r \times r}
$$

2. Use $Q$ as the orthonormalized matrix of left singular vectors:

$$
U_r = Q
$$

This ensures $`U\_r^\mathsf{T} U\_r = I\_r`$.

---

### **VI. Summary Table**

| Task                      | Matrix     | Computation                                       |
| ------------------------- |------------| ------------------------------------------------- |
| Right singular vectors    | $V$        | Eigenvectors of $`A^\mathsf{T}A`$                 |
| Singular values           | $`\Sigma`$ | Square roots of eigenvalues of $`A^\mathsf{T}A`$   |
| Left singular vectors     | $U$        | $`u\_i = \frac{1}{\sigma\_i} A v\_i`$              |
| Orthonormalizing \$u\_i\$ | $U$        | Apply QR on $`[A v\_1, \dots, A v\_r]`$ if necessary |

---

### **VII. Applications of Larger SVD**

* **Low-rank approximation**: Keep top-$k$ singular values/vectors for compression.


* **Principal Component Analysis (PCA)**: Use $V$ from SVD of centered data matrix.


* **Latent Semantic Analysis** in NLP.


* **Pseudoinverse computation**:

  $$
  A^+ = V \Sigma^+ U^\mathsf{T}
  $$

  where $`\Sigma^+`$ is formed by inverting the non-zero singular values.

---