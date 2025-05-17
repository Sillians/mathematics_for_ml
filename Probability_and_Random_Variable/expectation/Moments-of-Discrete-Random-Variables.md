## **Moments of Discrete Random Variables**

**Moments** are numerical measures that describe various aspects of the **shape** 
and **distribution** of a random variable. The *k-th moment* of a discrete random 
variable $X$ gives insight into quantities like **spread**, **skewness**, and **kurtosis**. 
Moments are centered around either the origin or the mean.

---

### **Definition: k-th Moment About the Origin**

The **k-th moment** about the origin is defined as:

$$
\mu'_k = \mathbb{E}[X^k] = \sum_{x \in \text{Support}(X)} x^k \cdot P(X = x)
$$

---

### **1. Calculating the Second Moment of a Random Variable**

The **second moment** about the origin is:

$$
\mu'_2 = \mathbb{E}[X^2]
$$

This is used in the formula for variance:

$$
\text{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2
$$

#### **Example:**

Let $`X \in \{1, 2, 3\}`$ with
$`P(X = 1) = 0.2, \, P(X = 2) = 0.5, \, P(X = 3) = 0.3`$

Then:

$$
\mathbb{E}[X^2] = 1^2(0.2) + 2^2(0.5) + 3^2(0.3) = 0.2 + 2.0 + 2.7 = \boxed{4.9}
$$

---

### **2. Calculating Higher Moments of a Random Variable**

Higher-order moments (e.g., third, fourth) are computed similarly:

$$
\mu'_k = \mathbb{E}[X^k] = \sum x^k P(X = x)
$$

They are used to analyze:

* **3rd moment**: skewness (asymmetry)
* **4th moment**: kurtosis (tail heaviness)

#### **Example (Third Moment):**

$$
\mathbb{E}[X^3] = 1^3(0.2) + 2^3(0.5) + 3^3(0.3) = 0.2 + 4.0 + 8.1 = \boxed{12.3}
$$

---

### **3. Simplifying Expressions Using Properties of Expected Value**

Key properties of expectation help simplify moments:

* **Linearity**:

$$
\mathbb{E}[aX + b] = a \mathbb{E}[X] + b
$$

* **Expectation of a constant**:

$$
\mathbb{E}[c] = c
$$

* **Expectation of scaled variable**:

$$
\mathbb{E}[aX^k] = a \mathbb{E}[X^k]
$$

#### **Example:**

Let $`Y = 2X + 3`$, then:

$$
\mathbb{E}[Y] = 2\mathbb{E}[X] + 3
$$

$$
\mathbb{E}[Y^2] \ne 2\mathbb{E}[X^2] + 3^2 \quad \text{(nonlinear!)}
$$

Instead, compute $`\mathbb{E}[(2X + 3)^2]`$ carefully by expanding and applying linearity to each term.

---

### ✅ **Summary Table**

| Moment     | Formula           | Interpretation            |
| ---------- | ----------------- | ------------------------- |
| 1st moment | $`\mathbb{E}[X]`$   | Mean                      |
| 2nd moment | $`\mathbb{E}[X^2]`$ | Spread (used in variance) |
| 3rd moment | $`\mathbb{E}[X^3]`$ | Skewness                  |
| 4th moment | $`\mathbb{E}[X^4]`$ | Kurtosis                  |

---

### **Conclusion**

Moments give deep insight into the **shape and behavior** of a discrete random variable's 
distribution. Starting from the mean and variance and extending to higher-order moments, 
these values are essential for summarizing, comparing, and modeling distributions in probability and statistics.
