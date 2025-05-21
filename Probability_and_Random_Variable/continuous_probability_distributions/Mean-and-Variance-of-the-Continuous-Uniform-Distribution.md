## **Mean and Variance of the Continuous Uniform Distribution**

The **continuous uniform distribution** models a random variable that is **equally likely to 
take on any value** within a specified interval. It's one of the simplest probability distributions 
and forms the foundation for understanding more complex models.

Let $`X \sim \text{Uniform}(a, b)`$, where $`a < b`$.
The PDF of $X$ is:

$$
f(x) =
\begin{cases}
\frac{1}{b - a}, & \text{for } a \leq x \leq b \\
0, & \text{otherwise}
\end{cases}
$$

---

### **1. Computing the Expected Value (Mean)**

The **expected value** (or **mean**) of a uniform distribution on $[a, b]$ is the midpoint of the interval:

$$
\mathbb{E}[X] = \mu = \frac{a + b}{2}
$$

#### ✅ Example:

For $`X \sim \text{Uniform}(2, 10)`$:

$$
\mathbb{E}[X] = \frac{2 + 10}{2} = 6
$$

---

###  **2. Computing the Variance**

The **variance** of $`X \sim \text{Uniform}(a, b)`$ is:

$$
\mathrm{Var}(X) = \frac{(b - a)^2}{12}
$$

#### ✅ Example:

For $`X \sim \text{Uniform}(2, 10)`$:

$$
\mathrm{Var}(X) = \frac{(10 - 2)^2}{12} = \frac{64}{12} = \frac{16}{3}
$$

---

###  **3. Computing the Standard Deviation**

The **standard deviation** is the square root of the variance:

$$
\sigma = \sqrt{\mathrm{Var}(X)} = \frac{b - a}{\sqrt{12}}
$$

#### ✅ Example:

$$
\sigma = \frac{10 - 2}{\sqrt{12}} = \frac{8}{\sqrt{12}} = \frac{8}{2\sqrt{3}} = \frac{4}{\sqrt{3}} \approx 2.309
$$

---

### ✅ **Summary Table**

| Statistic               | Formula                   |
| ----------------------- | ------------------------- |
| Mean $`\mu`$              | $`\frac{a + b}{2}`$         |
| Variance $`\sigma^2`$     | $`\frac{(b - a)^2}{12}`$    |
| Std. Deviation $`\sigma`$ | $`\frac{b - a}{\sqrt{12}}`$ |

---

### **Conclusion**

The **continuous uniform distribution** is defined by a constant probability across an interval. 
Its mean is the midpoint, and its spread is captured by a simple formula for variance and 
standard deviation—making it a fundamental concept in both theoretical and applied probability.
