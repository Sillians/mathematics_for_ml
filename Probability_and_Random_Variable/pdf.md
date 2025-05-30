## **Probability Density Function**

A **Probability Density Function (PDF)** is a function that describes the **likelihood** of a **continuous random variable** taking on a particular value within a given range.

---

### **Key Characteristics:**

1. **Non-Negative:**
   For all $x$,

$$
f(x) \geq 0
$$

2. **Total Area = 1:**
   The total probability over the entire domain must equal 1:

$$
\int_{-\infty}^{\infty} f(x) \, dx = 1
$$

3. **Probability Over an Interval:**
   The probability that the variable falls between two values $a$ and $b$ is:

$$
P(a \leq X \leq b) = \int_a^b f(x) \, dx
$$

---

### **Important Notes:**

* For continuous variables, $`P(X = a) = 0`$. Probabilities are only defined over intervals.
* The PDF represents **density**, not probability at a point.

---

### **Example:**

Let

$$
f(x) = \begin{cases}
2x, & 0 \leq x \leq 1 \\
0, & \text{otherwise}
\end{cases}
$$

* Check if it's a valid PDF:

$$
\int_0^1 2x \, dx = \left[ x^2 \right]_0^1 = 1
$$

✅ Valid.

* Probability $`0.2 \leq X \leq 0.4`$:

$$
\int_{0.2}^{0.4} 2x \, dx = [x^2]_{0.2}^{0.4} = 0.16 - 0.04 = 0.12
$$

---

In essence, a PDF lets you model and compute probabilities for **continuous random variables** over ranges, using integration.
