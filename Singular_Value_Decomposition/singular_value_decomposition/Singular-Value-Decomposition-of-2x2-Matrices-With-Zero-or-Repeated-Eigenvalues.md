## **Singular Value Decomposition of 2×2 Matrices With Zero or Repeated Eigenvalues**

---

### **1. Overview of SVD for 2×2 Matrices**

For any real $`2 \times 2`$ matrix $A$, the **Singular Value Decomposition (SVD)** expresses $A$ as:

$$
A = U \Sigma V^T
$$

where:

* $U$ and $V$ are $`2 \times 2`$ orthogonal matrices (i.e., $`U^T U = V^T V = I`$),


* $`\Sigma = \begin{bmatrix} \sigma\_1 & 0 \ 0 & \sigma\_2 \end{bmatrix}`$, with singular values $`\sigma\_1 \geq \sigma\_2 \geq 0`$,


* The singular values are defined as:

$$
\sigma_i = \sqrt{\lambda_i(A^T A)}
$$

  where $`\lambda\_i`$ are the eigenvalues of $`A^T A`$.

---

### **2. The Singular Value Decomposition of a 2×2 Matrix With a Zero Eigenvalue**

When $`\sigma\_2 = 0`$, $A$ is **rank-deficient** (rank 1), and one eigenvalue of $`A^T A`$ is zero.

#### **Example:**

Let

$$
A = \begin{bmatrix} 2 & 4 \\ 1 & 2 \end{bmatrix}
$$

* Compute $`A^T A`$:

$$
A^T A = \begin{bmatrix} 2 & 1 \\ 4 & 2 \end{bmatrix}
       \begin{bmatrix} 2 & 4 \\ 1 & 2 \end{bmatrix}
     = \begin{bmatrix} 5 & 10 \\ 10 & 20 \end{bmatrix}
$$

* Eigenvalues: $`25`$, $`0`$ ⇒ $`\sigma\_1 = 5`$, $`\sigma\_2 = 0`$

* Corresponding orthonormal eigenvectors form $`V = [v\_1 \ v\_2]`$

* Compute $`u\_1 = \dfrac{A v\_1}{\sigma\_1}`$

* Choose $`u\_2`$ such that $`U = [u\_1 \ u\_2]`$ is orthogonal

Then:

$$
A = U \begin{bmatrix} 5 & 0 \\ 0 & 0 \end{bmatrix} V^T
$$

---

### **3. Finding the Columns of the First Matrix Given Part of an SVD With a Zero Eigenvalue**

Suppose we are given:

* $`\Sigma = \begin{bmatrix} \sigma\_1 & 0 \ 0 & 0 \end{bmatrix}`$


* $`V = [v\_1 \ v\_2]`$, with $`v\_1`$ known and $`\sigma\_1 \neq 0`$


**Steps to recover $`U = [u\_1\ u\_2]`$:**

1. Compute $`u\_1 = \dfrac{A v\_1}{\sigma\_1}`$


2. Choose $`u\_2`$ as any unit vector orthogonal to $`u\_1`$


3. Ensure $`U`$ is orthogonal: $`U^T U = I`$


This process completes the first matrix $U$ from partial SVD information.

---

### **4. The Singular Value Decomposition of a 2×2 Matrix With Repeated Eigenvalues**

If $`A^T A`$ has two **equal** eigenvalues, then $`\sigma\_1 = \sigma\_2`$.

This happens when:

* $`A^T A = \lambda I`$ for some $`\lambda > 0`$


* Then $`\Sigma = \sqrt{\lambda} I`$ and $A$ acts like an **isotropic scaling + rotation/reflection**

#### **Example:**

Let

$$
A = \sqrt{2} \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}
$$

This is a rotation matrix scaled by $`\sqrt{2}`$

Then:

* $`A^T A = 2 I`$


* $`\sigma\_1 = \sigma\_2 = \sqrt{2}`$


* Any orthonormal pair of vectors can be used for $V$; set $`V = I`$


* Then $`U = A V \Sigma^{-1} = A \cdot \dfrac{1}{\sqrt{2}} I`$

So:

$$
A = U \Sigma V^T = \left(\dfrac{A}{\sqrt{2}}\right) \cdot \sqrt{2} I \cdot I^T = A
$$

---

### **5. Summary Table**

| Case                          | Eigenvalues of \$A^T A\$        | Singular Values               | Rank | Notes                               |
| ----------------------------- | ------------------------------- | ----------------------------- | ---- | ----------------------------------- |
| One zero eigenvalue           | $`\lambda\_1 > 0,\ \lambda\_2 = 0`$ | $`\sigma\_1 > 0,\ \sigma\_2 = 0`$ | 1    | Rank-deficient                      |
| Repeated positive eigenvalues | $`\lambda\_1 = \lambda\_2 > 0`$  | $`\sigma\_1 = \sigma\_2 > 0`$  | 2    | Rotation or reflection times scalar |
| Zero matrix                   | $`\lambda\_1 = \lambda\_2 = 0`$  | $`\sigma\_1 = \sigma\_2 = 0`$  | 0    | Trivial case                        |

---

### **Conclusion**

SVD remains well-defined and interpretable even when the matrix has zero or repeated eigenvalues.

* In the **zero eigenvalue** case, SVD reveals the collapse along one direction (rank 1).
* In the **repeated eigenvalue** case, the action is uniform in all directions, and SVD reflects rotational symmetry.

Understanding these special cases is crucial for interpreting structure and behavior in dimensionality reduction, compression, and data representation.
