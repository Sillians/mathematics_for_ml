## **Cumulative Distribution Functions (CDFs) for Continuous Random Variables**

The **Cumulative Distribution Function (CDF)** of a continuous random variable $X$ gives the 
probability that $X$ takes on a value less than or equal to $x$:

$$
F(x) = P(X \leq x) = \int_{-\infty}^{x} f(t) \, dt
$$

Where $`f(t)`$ is the **probability density function (PDF)** of $X$.

The CDF is:

* **Non-decreasing**
* $`\lim_{x \to -\infty} F(x) = 0`$
* $`\lim_{x \to \infty} F(x) = 1`$
* Continuous for continuous random variables

---

### **1. Finding a CDF Given a PDF With a Lower Bound**

If a PDF is nonzero only for $`x \geq a`$, then the CDF is defined as:

$$
F(x) =
\begin{cases}
0, & x < a \\
\int_a^x f(t)\, dt, & x \geq a
\end{cases}
$$

#### **Example:**

Let:

$$
f(x) =
\begin{cases}
\frac{1}{4} e^{-x/4}, & x \geq 0 \\
0, & x < 0
\end{cases}
$$

Then:

$$
F(x) = \int_0^x \frac{1}{4} e^{-t/4} \, dt = 1 - e^{-x/4} \quad \text{for } x \geq 0
$$

---

### **2. Computing a CDF Given a PDF That’s Nonzero Over All Real Numbers**

If the PDF is nonzero for all $`x \in (-\infty, \infty)`$, such as the **normal distribution**, then:

$$
F(x) = \int_{-\infty}^x f(t) \, dt
$$

This is often **not solvable by hand** and is typically computed **numerically** or via 
a **lookup table** (e.g., standard normal table).

#### **Example:**

Standard normal:

$$
f(x) = \frac{1}{\sqrt{2\pi}} e^{-x^2/2}
$$

Then:

$$
F(x) = \Phi(x) = \int_{-\infty}^{x} \frac{1}{\sqrt{2\pi}} e^{-t^2/2} \, dt
$$

---

### **3. Finding a CDF Given a PDF With Lower and Upper Bounds**

If $`f(x)`$ is defined over $`[a, b]`$, the CDF is:

$$
F(x) =
\begin{cases}
0, & x < a \\
\int_a^x f(t)\, dt, & a \leq x \leq b \\
1, & x > b
\end{cases}
$$

#### **Example:**

Let:

$$
f(x) =
\begin{cases}
\frac{1}{5}, & 2 \leq x \leq 7 \\
0, & \text{otherwise}
\end{cases}
$$

Then:

$$
F(x) =
\begin{cases}
0, & x < 2 \\
\frac{x - 2}{5}, & 2 \leq x \leq 7 \\
1, & x > 7
\end{cases}
$$

---

### **4. Computing a Probability Over an Interval Using a CDF**

Once you have the CDF $`F(x)`$, the probability that $X$ falls in an interval $`[a, b]`$ is:

$$
P(a \leq X \leq b) = F(b) - F(a)
$$

This is true **regardless of whether the interval is open or closed**, since the probability of a 
specific point in continuous distributions is `0`.

#### **Example:**

If $`F(x) = 1 - e^{-x/4}`$, find $`P(1 \leq X \leq 3)`$:

$$
P(1 \leq X \leq 3) = F(3) - F(1) = \left(1 - e^{-3/4}\right) - \left(1 - e^{-1/4}\right)
= e^{-1/4} - e^{-3/4}
$$

---

### ✅ **Summary Table**

| Scenario                     | Formula for $F(x)$                         |
| ---------------------------- | ------------------------------------------ |
| PDF with lower bound $`a`$     | $`F(x) = \int_a^x f(t)\, dt`$ for $`x \geq a`$ |
| PDF over all real numbers    | $`F(x) = \int_{-\infty}^x f(t)\, dt`$        |
| PDF over interval $`[a, b]`$   | Piecewise: 0, definite integral, or 1      |
| Compute $`P(a \leq X \leq b)`$ | $`F(b) - F(a)`$                              |

---

### **Conclusion**

The CDF is a foundational tool in probability that encodes **all distributional information** of a 
continuous random variable. It allows for easy computation of interval probabilities and helps
in defining related functions like percentiles and quantiles. Whether the PDF has a bounded or 
unbounded domain, mastering how to construct and apply the CDF is critical for analyzing continuous data.
