## **Conditional Variance for Continuous Random Variables**

---

### **1. Core Concept: Conditional Variance**

For continuous random variables $X$ and $Y$, the **conditional variance** of $Y$ given $`X = x`$, denoted as:

$$
\operatorname{Var}(Y \mid X = x)
$$

measures the spread of $Y$ assuming that $`X = x`$ is known. This is a **function of $x$** and captures how the variability of $Y$ changes as $X$ varies.

---

### **2. Formula for Conditional Variance**

Given the **conditional probability density function** $`f_{Y|X}(y|x)`$, the conditional variance is computed as:

$$
\operatorname{Var}(Y \mid X = x) = \mathbb{E}[Y^2 \mid X = x] - \left( \mathbb{E}[Y \mid X = x] \right)^2
$$

Where:

* $`\mathbb{E}[Y \mid X = x] = \int_{-\infty}^{\infty} y \cdot f_{Y|X}(y|x) \, dy`$


* $`\mathbb{E}[Y^2 \mid X = x] = \int_{-\infty}^{\infty} y^2 \cdot f_{Y|X}(y|x) \, dy`$

---

### **3. Calculating Conditional Variance Given a Conditional PDF**

#### **Example**:

Let the conditional PDF of $`Y \mid X = x`$ be:

$$
f_{Y|X}(y|x) = 
\begin{cases}
2y, & 0 < y < 1, \\
0, & \text{otherwise}
\end{cases}
$$


**Step 1: Compute** $`\mathbb{E}[Y \mid X = x]`$:

$$
\mathbb{E}[Y \mid X = x] = \int_0^1 y \cdot 2y \, dy = \int_0^1 2y^2 \, dy = \frac{2}{3}
$$


**Step 2: Compute** $`\mathbb{E}[Y^2 \mid X = x]`$:

$$
\mathbb{E}[Y^2 \mid X = x] = \int_0^1 y^2 \cdot 2y \, dy = \int_0^1 2y^3 \, dy = \frac{1}{2}
$$


**Step 3: Apply the formula**:

$$
\operatorname{Var}(Y \mid X = x) = \frac{1}{2} - \left( \frac{2}{3} \right)^2 = \frac{1}{2} - \frac{4}{9} = \frac{1}{18}
$$

---

### **4. Using Improper Integrals**

Improper integrals arise when the support of the conditional PDF is unbounded (e.g., infinite limits).


#### **Example**:

Let the conditional PDF be:

$$
f_{Y|X}(y|x) = 
\begin{cases}
\lambda e^{-\lambda y}, & y \ge 0 \\
0, & \text{otherwise}
\end{cases}
$$


This is the **Exponential(λ)** distribution. Then:

* $`\mathbb{E}[Y \mid X = x] = \int_0^{\infty} y \cdot \lambda e^{-\lambda y} \, dy = \frac{1}{\lambda}`$


* $`\mathbb{E}[Y^2 \mid X = x] = \int_0^{\infty} y^2 \cdot \lambda e^{-\lambda y} \, dy = \frac{2}{\lambda^2}`$

So the conditional variance:

$$
\operatorname{Var}(Y \mid X = x) = \frac{2}{\lambda^2} - \left( \frac{1}{\lambda} \right)^2 = \frac{1}{\lambda^2}
$$

---


### **5. Calculating Conditional Variance Using Joint and Marginal PDFs**

If the **joint PDF** $`f_{X,Y}(x, y)`$ is known, and the **marginal** $`f_X(x)`$ is computable:

$$
f_{Y|X}(y|x) = \frac{f_{X,Y}(x, y)}{f_X(x)}
$$

Once $`f_{Y|X}(y|x)`$ is computed, apply the conditional variance formula.

#### **Example**:

Let:

$$
f_{X,Y}(x, y) = 
\begin{cases}
8xy, & 0 < x < 1,\ 0 < y < 1 \\
0, & \text{otherwise}
\end{cases}
$$

**Step 1: Compute** $`f_X(x)`$:

$$
f_X(x) = \int_0^1 8xy \, dy = 4x
$$

**Step 2: Compute** $`f_{Y|X}(y|x)`$:

$$
f_{Y|X}(y|x) = \frac{8xy}{4x} = 2y, \quad 0 < y < 1
$$

This is the same conditional distribution from earlier, so:

$$
\operatorname{Var}(Y \mid X = x) = \frac{1}{18}
$$

---

### **6. Applications**

| Domain                | Example                                                    |
| --------------------- | ---------------------------------------------------------- |
| **Econometrics**      | Conditional variance of income given education level       |
| **Signal processing** | Variance of noise given signal strength                    |
| **Machine learning**  | Uncertainty estimates in heteroskedastic models            |
| **Finance**           | Conditional volatility of asset returns given past returns |

---

### **7. Summary**

| Step | Action                                                                                                           |             |      |
| ---- |------------------------------------------------------------------------------------------------------------------|-------------| ---- |
| 1    | Obtain the conditional PDF $`( f\_{Y  X}(y x) )`$                                                                |  |  |
| 2    | Compute $`\mathbb{E}[Y \mid X = x]`$                                                                             |             |      |
| 3    | Compute $`\mathbb{E}[Y^2 \mid X = x]`$                                                                           |             |      |
| 4    | Use $`\operatorname{Var}(Y \mid X = x) = \mathbb{E}[Y^2 \mid X = x] - \left( \mathbb{E}[Y \mid X = x] \right)^2`$ |             |      |
| 5    | Apply improper integration if the domain is unbounded                                                            |             |      |

---
