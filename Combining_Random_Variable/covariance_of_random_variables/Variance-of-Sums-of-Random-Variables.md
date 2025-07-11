## **Variance of Sums of Random Variables**

---

### **1. Core Idea: Variance of a Sum**

For random variables $`X_1, X_2, \dots, X_n`$, the **variance of their sum** is not always the sum of their variances. It depends on whether the variables are **independent** and how they're **correlated**.

#### **General Formula:**

$$
\operatorname{Var}\left( \sum_{i=1}^n X_i \right) = \sum_{i=1}^n \operatorname{Var}(X_i) + 2 \sum_{i<j} \operatorname{Cov}(X_i, X_j)
$$

If the $`X_i`$'s are **pairwise independent**, the covariances are zero:

$$
\operatorname{Var}\left( \sum X_i \right) = \sum \operatorname{Var}(X_i)
$$

---

### **2. Calculating the Variance of a Sum or Difference of Two Random Variables**

Let $X$ and $Y$ be two random variables.

#### **Sum:**

$$
\operatorname{Var}(X + Y) = \operatorname{Var}(X) + \operatorname{Var}(Y) + 2\operatorname{Cov}(X, Y)
$$

#### **Difference:**

$$
\operatorname{Var}(X - Y) = \operatorname{Var}(X) + \operatorname{Var}(Y) - 2\operatorname{Cov}(X, Y)
$$

> If $X$ and $Y$ are independent: $`\operatorname{Cov}(X, Y) = 0`$

#### **Example**:

If $`\operatorname{Var}(X) = 4`$, $`\operatorname{Var}(Y) = 9`$, $`\operatorname{Cov}(X, Y) = 3`$

* $`\operatorname{Var}(X + Y) = 4 + 9 + 2(3) = 19`$


* $`\operatorname{Var}(X - Y) = 4 + 9 - 2(3) = 7`$

---

### **3. Variance of a Sum of Scaled Random Variables**

Let $`Z = aX + bY`$. Then:

$$
\operatorname{Var}(Z) = a^2 \operatorname{Var}(X) + b^2 \operatorname{Var}(Y) + 2ab\, \operatorname{Cov}(X, Y)
$$


#### **Example**:

Let $`X, Y`$ be random variables with:

* $`\operatorname{Var}(X) = 1`$


* $`\operatorname{Var}(Y) = 4`$


* $`\operatorname{Cov}(X, Y) = -1`$


* Let $`Z = 2X - 3Y`$

Then:

$$
\operatorname{Var}(Z) = 4(1) + 9(4) + 2(2)(-3)(-1) = 4 + 36 + 12 = 52
$$

---

### **4. Calculating a Combined Variance Given Some Moments**

Given:

* $`\mathbb{E}[X] = 2`$, $`\mathbb{E}[Y] = 5`$


* $`\mathbb{E}[X^2] = 6`$, $`\mathbb{E}[Y^2] = 30`$


* $`\mathbb{E}[XY] = 15`$

Find: $`\operatorname{Var}(X + Y)`$

#### **Step 1**: Compute variances and covariance

$$
\operatorname{Var}(X) = 6 - 2^2 = 2,\quad
\operatorname{Var}(Y) = 30 - 5^2 = 5,\quad
\operatorname{Cov}(X, Y) = 15 - (2)(5) = 5
$$

#### **Step 2**: Plug into variance of a sum:

$$
\operatorname{Var}(X + Y) = 2 + 5 + 2(5) = 17
$$

---

### **5. Variance of a Sum of Three Random Variables**

Let $`S = X + Y + Z`$. Then:

$$
\operatorname{Var}(S) = \operatorname{Var}(X) + \operatorname{Var}(Y) + \operatorname{Var}(Z) + 2\operatorname{Cov}(X,Y) + 2\operatorname{Cov}(X,Z) + 2\operatorname{Cov}(Y,Z)
$$

#### **Example**:

Let:

* $`\operatorname{Var}(X) = 2`$, $`\operatorname{Var}(Y) = 3`$, $`\operatorname{Var}(Z) = 1`$


* $`\operatorname{Cov}(X, Y) = 1`$, $`\operatorname{Cov}(X, Z) = 0`$, $`\operatorname{Cov}(Y, Z) = -1`$

Then:

$$
\operatorname{Var}(X + Y + Z) = 2 + 3 + 1 + 2(1) + 2(0) + 2(-1) = 6 + 2 - 2 = 6
$$

---

### **6. Summary Table**

| Type                              | Formula                                                                              |
|-----------------------------------|--------------------------------------------------------------------------------------|
| $`\operatorname{Var}(X + Y)`$     | $`\operatorname{Var}(X) + \operatorname{Var}(Y) + 2\operatorname{Cov}(X, Y)`$        |
| $`\operatorname{Var}(aX + bY)`$   | $`a^2\operatorname{Var}(X) + b^2\operatorname{Var}(Y) + 2ab\operatorname{Cov}(X, Y)`$ |
| $`\operatorname{Var}(X - Y)`$     | $`\operatorname{Var}(X) + \operatorname{Var}(Y) - 2\operatorname{Cov}(X, Y)`$        |
| $`\operatorname{Var}(X + Y + Z)`$ | $`\sum \operatorname{Var}(X_i) + 2\sum_{i<j} \operatorname{Cov}(X_i, X_j)`$          |

---

### **7. Applications**

| Field           | Use Case                                  |
| --------------- | ----------------------------------------- |
| **Finance**     | Portfolio variance with correlated assets |
| **ML**          | Variance propagation in model uncertainty |
| **Simulation**  | Error analysis in Monte Carlo methods     |
| **Engineering** | Noise analysis in signal systems          |

---
