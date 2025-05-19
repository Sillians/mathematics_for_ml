## **Expected Values of Continuous Random Variables**

The **expected value** (or **mean**) of a continuous random variable provides a measure of its **central tendency**—essentially, the "balance point" of its probability distribution.

---

### 🔹 **Definition of Expected Value (Mean)**

Let $X$ be a continuous random variable with **probability density function (PDF)** $f(x)$. The **expected value** of $X$ is defined as:

$$
\mathbb{E}[X] = \int_{-\infty}^{\infty} x f(x)\, dx
$$

If the domain of $X$ is restricted (e.g., from $a$ to $b$), then:

$$
\mathbb{E}[X] = \int_{a}^{b} x f(x)\, dx
$$

---

###  **1. Computing the Mean of a Continuous Random Variable**

#### Example:

Let $`f(x) = 2x`$, for $`x \in [0, 1]`$

This is a valid PDF because:

* $`f(x) \ge 0`$
* $`\int_0^1 2x\, dx = 1`$

Compute the expected value:

$$
\mathbb{E}[X] = \int_0^1 x \cdot 2x\, dx = \int_0^1 2x^2\, dx = \left[\frac{2x^3}{3}\right]_0^1 = \frac{2}{3}
$$

✅ **Mean**: $`\mathbb{E}[X] = \frac{2}{3}`$

---

### 🔹 **2. Computing the Mean With a Piecewise PDF**

Suppose:

$$
f(x) =
\begin{cases}
x, & 0 \le x \le 1 \\
2 - x, & 1 < x \le 2 \\
0, & \text{otherwise}
\end{cases}
$$

Compute:

$$
\mathbb{E}[X] = \int_0^1 x \cdot x \, dx + \int_1^2 x(2 - x) \, dx
$$

First part:

$$
\int_0^1 x^2 \, dx = \left[\frac{x^3}{3}\right]_0^1 = \frac{1}{3}
$$

Second part:

$$
\int_1^2 (2x - x^2) \, dx = \left[x^2 - \frac{x^3}{3}\right]_1^2 = (4 - \frac{8}{3}) - (1 - \frac{1}{3}) = \frac{4}{3}
$$

So:

$$
\mathbb{E}[X] = \frac{1}{3} + \frac{4}{3} = \boxed{\frac{5}{3}}
$$

---

### 🔹 **3. Computing the Mean of a Transformed Continuous Random Variable**

If $`Y = g(X)`$, then:

$$
\mathbb{E}[g(X)] = \int_{-\infty}^{\infty} g(x) f(x)\, dx
$$

#### Example:

Let $`X \sim U(0, 2)`$, so $`f(x) = \frac{1}{2}`$ for $`x \in [0, 2]`$

Find $`\mathbb{E}[X^2]`$:

$$
\mathbb{E}[X^2] = \int_0^2 x^2 \cdot \frac{1}{2} \, dx = \frac{1}{2} \int_0^2 x^2\, dx = \frac{1}{2} \left[\frac{x^3}{3}\right]_0^2 = \frac{1}{2} \cdot \frac{8}{3} = \frac{4}{3}
$$

✅ **Mean of Transformed Variable** $`\mathbb{E}[X^2] = \frac{4}{3}`$

---

### ✅ **Summary Table**

| Task                       | Formula                                  |
| -------------------------- | ---------------------------------------- |
| Mean of $X$                | $`\mathbb{E}[X] = \int x f(x)\, dx`$       |
| Mean with piecewise $`f(x)`$ | Sum of integrals over each interval      |
| Mean of $`g(X)`$             | $`\mathbb{E}[g(X)] = \int g(x) f(x)\, dx`$ |

---

### **Conclusion**

The expected value of a continuous random variable provides the long-run average or center of mass of its distribution. 
Whether you're working with a simple function, a piecewise PDF, or a transformed variable, integration is the key tool for calculating expected values in the continuous case.
