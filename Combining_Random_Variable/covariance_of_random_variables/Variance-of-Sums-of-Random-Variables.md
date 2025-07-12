## **Variance of Sums of Random Variables**

---

### **1. Core Idea: Variance of a Sum**

For random variables $`X_1, X_2, \dots, X_n`$, the **variance of their sum** is not always the sum of their variances. It depends on whether the variables are **independent** and how they're **correlated**.

#### **General Formula:**

$$
\mathrm{Var}\left( \sum_{i=1}^n X_i \right) = (\sum_{i=1}^n \mathrm{Var}(X_i) + (2 \sum_{i<j} \mathrm{Cov}(X_i, X_j)
$$

If the $`X_i`$'s are **pairwise independent**, the covariances are zero:

$$
\mathrm{Var}\left( \sum X_i \right) = \sum \mathrm{Var}(X_i)
$$

---

### **2. Calculating the Variance of a Sum or Difference of Two Random Variables**

Let $X$ and $Y$ be two random variables.

#### **Sum:**

$$
\mathrm{Var}(X + Y) = \mathrm{Var}(X) + \mathrm{Var}(Y) + 2\mathrm{Cov}(X, Y)
$$

#### **Difference:**

$$
\mathrm{Var}(X - Y) = \mathrm{Var}(X) + \mathrm{Var}(Y) - 2\mathrm{Cov}(X, Y)
$$

> If $X$ and $Y$ are independent: $`\mathrm{Cov}(X, Y) = 0`$

#### **Example**:

If $`\mathrm{Var}(X) = 4`$, $`\mathrm{Var}(Y) = 9`$, $`\mathrm{Cov}(X, Y) = 3`$

* $`\mathrm{Var}(X + Y) = 4 + 9 + 2(3) = 19`$


* $`\mathrm{Var}(X - Y) = 4 + 9 - 2(3) = 7`$

---

### **3. Variance of a Sum of Scaled Random Variables**

Let $`Z = aX + bY`$. Then:

$$
\mathrm{Var}(Z) = a^2 \mathrm{Var}(X) + b^2 \mathrm{Var}(Y) + 2ab\, \mathrm{Cov}(X, Y)
$$


#### **Example**:

Let $`X, Y`$ be random variables with:

* $`\mathrm{Var}(X) = 1`$


* $`\mathrm{Var}(Y) = 4`$


* $`\mathrm{Cov}(X, Y) = -1`$


* Let $`Z = 2X - 3Y`$

Then:

$$
\mathrm{Var}(Z) = 4(1) + 9(4) + 2(2)(-3)(-1) = 4 + 36 + 12 = 52
$$

---

### **4. Calculating a Combined Variance Given Some Moments**

Given:

* $`\mathbb{E}[X] = 2`$, $`\mathbb{E}[Y] = 5`$


* $`\mathbb{E}[X^2] = 6`$, $`\mathbb{E}[Y^2] = 30`$


* $`\mathbb{E}[XY] = 15`$

Find: $`\mathrm{Var}(X + Y)`$

#### **Step 1**: Compute variances and covariance

$$
\mathrm{Var}(X) = 6 - 2^2 = 2,\quad
\mathrm{Var}(Y) = 30 - 5^2 = 5,\quad
\mathrm{Cov}(X, Y) = 15 - (2)(5) = 5
$$

#### **Step 2**: Plug into variance of a sum:

$$
\mathrm{Var}(X + Y) = 2 + 5 + 2(5) = 17
$$

---

### **5. Variance of a Sum of Three Random Variables**

Let $`S = X + Y + Z`$. Then:

$$
\mathrm{Var}(S) = \mathrm{Var}(X) + \mathrm{Var}(Y) + \mathrm{Var}(Z) + 2\mathrm{Cov}(X,Y) + 2\mathrm{Cov}(X,Z) + 2\mathrm{Cov}(Y,Z)
$$

#### **Example**:

Let:

* $`\mathrm{Var}(X) = 2`$, $`\mathrm{Var}(Y) = 3`$, $`\mathrm{Var}(Z) = 1`$


* $`\mathrm{Cov}(X, Y) = 1`$, $`\mathrm{Cov}(X, Z) = 0`$, $`\mathrm{Cov}(Y, Z) = -1`$

Then:

$$
\mathrm{Var}(X + Y + Z) = 2 + 3 + 1 + 2(1) + 2(0) + 2(-1) = 6 + 2 - 2 = 6
$$

---

### **6. Summary Table**

| Type                              | Formula                                                                              |
|-----------------------------------|--------------------------------------------------------------------------------------|
| $`\mathrm{Var}(X + Y)`$     | $`\mathrm{Var}(X) + \mathrm{Var}(Y) + 2\mathrm{Cov}(X, Y)`$        |
| $`\mathrm{Var}(aX + bY)`$   | $`a^2\mathrm{Var}(X) + b^2\mathrm{Var}(Y) + 2ab\mathrm{Cov}(X, Y)`$ |
| $`\mathrm{Var}(X - Y)`$     | $`\mathrm{Var}(X) + \mathrm{Var}(Y) - 2\mathrm{Cov}(X, Y)`$        |
| $`\mathrm{Var}(X + Y + Z)`$ | $`\sum \mathrm{Var}(X_i) + 2\sum_{i<j} \mathrm{Cov}(X_i, X_j)`$          |

---

### **7. Applications**

| Field           | Use Case                                  |
| --------------- | ----------------------------------------- |
| **Finance**     | Portfolio variance with correlated assets |
| **ML**          | Variance propagation in model uncertainty |
| **Simulation**  | Error analysis in Monte Carlo methods     |
| **Engineering** | Noise analysis in signal systems          |

---
