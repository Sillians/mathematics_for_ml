## **The Covariance Matrix**

---

### **1. What Is the Covariance Matrix?**

The **covariance matrix** generalizes the concept of variance and covariance to **higher-dimensional** random vectors.

Let $`\mathbf{X} = \begin{bmatrix} X_1 \\ X_2 \\ \cdots \\ X_n \end{bmatrix}`$ be an $n$-dimensional random vector. 

The **covariance matrix** is:

$`\Sigma = \mathrm{Cov}(\mathbf{X}) = \mathbb{E}\left[(\mathbf{X} - \mathbb{E}[\mathbf{X}])(\mathbf{X} - \mathbb{E}[\mathbf{X}])^T\right]`$

---

### **2. Structure of the Covariance Matrix**

For $`\mathbf{X} = [X_1, X_2, \dots, X_n]^T`$, the $`(i,j)`$-th entry is:


$$
\Sigma_{ij} = \operatorname{Cov}(X_i, X_j) = \mathbb{E}[(X_i - \mu_i)(X_j - \mu_j)]
$$


So:

* Diagonal entries: $`\mathrm{Var}(X_i)`$


* Off-diagonal entries: $`\mathrm{Cov}(X_i, X_j)`$

The matrix is:

* **Symmetric**: $`\Sigma_{ij} = \Sigma_{ji}`$


* **Positive semi-definite**

---

### **3. Determining Elements of a Covariance Matrix**

To compute elements:

* Use marginal expectations: $`\mu_i = \mathbb{E}[X_i]`$


* Then compute: $`\Sigma_{ij} = \mathbb{E}[X_i X_j] - \mu_i \mu_j`$

#### **Example**:

Let $`\mathbb{E}[X] = 2`$, $`\mathbb{E}[Y] = 3`$, $`\mathbb{E}[X^2] = 5`$, $`\mathbb{E}[Y^2] = 10`$, $`\mathbb{E}[XY] = 6`$

Then:

* $`\mathrm{Var}(X) = 5 - 2^2 = 1`$


* $`\mathrm{Var}(Y) = 10 - 3^2 = 1`$


* $`\mathrm{Cov}(X, Y) = 6 - (2)(3) = 0`$

So:

$$
\Sigma =
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
$$

---

### **4. Finding a Covariance Matrix Given Some Moments**

If you’re given first and second-order moments like:

* $`\mathbb{E}[X]`$, $`\mathbb{E}[Y]`$


* $`\mathbb{E}[X^2]`$, $`\mathbb{E}[Y^2]`$


* $`\mathbb{E}[XY]`$

Then:

$$
\begin{aligned}
\mathrm{Var}(X) &= \mathbb{E}[X^2] - \mathbb{E}[X]^2 \\
\mathrm{Var}(Y) &= \mathbb{E}[Y^2] - \mathbb{E}[Y]^2 \\
\mathrm{Cov}(X, Y) &= \mathbb{E}[XY] - \mathbb{E}[X] \mathbb{E}[Y]
\end{aligned}
$$

Fill the symmetric matrix accordingly.

---

### **5. Finding a Covariance Matrix Given a Discrete Bivariate Distribution**

Given a discrete joint distribution of $X$ and $Y$:

| $`X \backslash Y`$ | 1   | 2   |
|--------------------| --- | --- |
| 1                  | 0.1 | 0.2 |
| 2                  | 0.3 | 0.4 |

#### **Step 1: Compute expectations**


$$
\mathbb{E}[X] = \sum_x x \cdot P(X = x) = 1 \cdot (0.1 + 0.2) + 2 \cdot (0.3 + 0.4) = 1(0.3) + 2(0.7) = 1.7
$$


$$
\mathbb{E}[Y] = 1 \cdot (0.1 + 0.3) + 2 \cdot (0.2 + 0.4) = 1(0.4) + 2(0.6) = 1.6
$$


$$
\mathbb{E}[XY] = \sum_{x,y} x y \cdot P(X = x, Y = y) = 1(1)(0.1) + 1(2)(0.2) + 2(1)(0.3) + 2(2)(0.4) = 0.1 + 0.4 + 0.6 + 1.6 = 2.7
$$


#### **Step 2: Compute elements**

$$
\mathrm{Var}(X) = \mathbb{E}[X^2] - \mathbb{E}[X]^2 = (1^2)(0.3) + (2^2)(0.7) - 1.7^2 = (0.3 + 2.8) - 2.89 = 3.1 - 2.89 = 0.21
$$


$$
\mathrm{Var}(Y) = \text{(similar steps)} = 0.24,\quad
\mathrm{Cov}(X, Y) = 2.7 - 1.7 \cdot 1.6 = 2.7 - 2.72 = -0.02
$$

Final matrix:

$$
\Sigma =
\begin{bmatrix}
0.21 & -0.02 \\
-0.02 & 0.24
\end{bmatrix}
$$

---

### **6. Finding a Covariance Matrix Given a Continuous Bivariate Distribution**

Let $`f_{X,Y}(x, y) = 4xy`$, defined over $`0 < x < 1, 0 < y < 1`$

**Step 1: Compute Expectations**

$$
\mathbb{E}[X] = \int_0^1 \int_0^1 x \cdot 4xy \, dxdy = 4 \int_0^1 \int_0^1 x^2 y \, dxdy = \frac{1}{2}
$$


$$
\mathbb{E}[Y] = \frac{1}{2},\quad
\mathbb{E}[XY] = \int_0^1 \int_0^1 xy \cdot 4xy \, dxdy = \frac{4}{9}
$$


$$
\mathbb{E}[X^2] = \int_0^1 \int_0^1 x^2 \cdot 4xy \, dxdy = \frac{1}{3},\quad \mathbb{E}[Y^2] = \frac{1}{3}
$$


**Step 2: Compute Matrix Elements**

$$
\mathrm{Var}(X) = \frac{1}{3} - \left(\frac{1}{2}\right)^2 = \frac{1}{12},\quad
\mathrm{Var}(Y) = \frac{1}{12}
$$


$$
\mathrm{Cov}(X, Y) = \frac{4}{9} - \frac{1}{4} = \frac{7}{36}
$$

Final matrix:

$$
\Sigma =
\begin{bmatrix}
\frac{1}{12} & \frac{7}{36} \\
\frac{7}{36} & \frac{1}{12}
\end{bmatrix}
$$

---

### **7. Summary Table**

| Task                         | Formula                                                       |
|------------------------------|---------------------------------------------------------------|
| $`\Sigma_{ii}`$ (Variance)   | $`\mathbb{E}[X_i^2] - \mu_i^2`$                               |
| $`\Sigma_{ij}`$ (Covariance) | $`\mathbb{E}[X_i X_j] - \mu_i \mu_j`$                         |
| Covariance Matrix            | $`\Sigma = \mathbb{E}[(\mathbf{X} - \mu)(\mathbf{X} - \mu)^T]`$ |
| Discrete case                | Sum over all $x, y$ values                                    |
| Continuous case              | Double integrals over domain                                  |

---

### **Applications of the Covariance Matrix**

| Field               | Use                                                    |
| ------------------- | ------------------------------------------------------ |
| **ML/AI**           | Principal Component Analysis (PCA), Gaussian Processes |
| **Statistics**      | Multivariate analysis, hypothesis testing              |
| **Finance**         | Portfolio risk modeling, asset correlations            |
| **Control systems** | Kalman filters                                         |

---
