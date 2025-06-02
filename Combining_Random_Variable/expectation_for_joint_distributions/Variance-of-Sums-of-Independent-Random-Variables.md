## **Variance of Sums of Independent Random Variables**

---

### **1. Core Principle**

For **independent** random variables $`X`$ and $`Y`$:

$$
\text{Var}(X + Y) = \text{Var}(X) + \text{Var}(Y)
$$

If **dependent**, you must also include the covariance term:

$$
\text{Var}(X + Y) = \text{Var}(X) + \text{Var}(Y) + 2\text{Cov}(X, Y)
$$

But when **independent**, $`\text{Cov}(X, Y) = 0`$.

---

### **2. Calculating the Variance of a Sum or Difference of Independent Random Variables**

Let $`X`$ and $`Y`$ be independent.

* **Sum**:

$$
\text{Var}(X + Y) = \text{Var}(X) + \text{Var}(Y)
$$

* **Difference**:

$$
\text{Var}(X - Y) = \text{Var}(X) + \text{Var}(Y)
$$

**Note**: The **sign doesn’t matter** because variance is based on squares.

---

### **3. Calculating the Variance of a Sum of Scaled Random Variables**

Let $`a`$ and $`b`$ be constants. For independent $`X`$ and $`Y`$:

$$
\text{Var}(aX + bY) = a^2 \text{Var}(X) + b^2 \text{Var}(Y)
$$

This extends to any number of scaled independent random variables:

$$
\text{Var}\left(\sum_{i=1}^n a_i X_i\right) = \sum_{i=1}^n a_i^2 \text{Var}(X_i)
$$

---

### **4. Calculating a Combined Variance Given Some Raw Moments**

Sometimes you're given **raw moments**:

* $`\mathbb{E}[X]`$, $`\mathbb{E}[X^2]`$
* Then:

$$
\text{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2
$$

Once you compute the variances of the individual random variables, apply the rules above to get the total variance of their sum or difference.

---

### ✅ **Summary**

| Task                      | Formula                                               |
| ------------------------- | ----------------------------------------------------- |
| Variance of $`X + Y`$       | $`\text{Var}(X) + \text{Var}(Y)`$                       |
| Variance of $`aX + bY`$     | $`a^2 \text{Var}(X) + b^2 \text{Var}(Y)`$               |
| Variance from raw moments | $`\text{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2`$ |

Understanding these rules is crucial for modeling uncertainty and variability in systems with multiple 
independent random components—common in statistics, engineering, and machine learning.
