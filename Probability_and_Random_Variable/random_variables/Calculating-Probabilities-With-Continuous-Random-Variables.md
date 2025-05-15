## **Calculating Probabilities with Continuous Random Variables**

For **continuous random variables**, probabilities are computed **over intervals** using 
the **probability density function (PDF)**. Since the probability of a continuous random 
variable taking any single value is zero, all meaningful probability calculations 
involve **integrals over intervals**.

---

### **1. Computing the Probability That a Random Variable Lies Within a Bounded Interval**

Given a continuous random variable $X$ with PDF $f(x)$, the probability that $X$ lies in the interval $[a, b]$ is:

$$
\boxed{P(a \leq X \leq b) = \int_a^b f(x) \, dx}
$$

Because for continuous variables, inequalities like $<$, $`\leq`$, etc., give the **same result**:

$$
P(a < X \leq b) = P(a \leq X < b) = P(a < X < b) = P(a \leq X \leq b)
$$

#### **Example:**

Let $`f(x) = 2x`$ for $`x \in [0, 1]`$.
Then:

$$
P(0.2 \leq X \leq 0.6) = \int_{0.2}^{0.6} 2x \, dx = \left[x^2\right]_{0.2}^{0.6} = 0.36 - 0.04 = \boxed{0.32}
$$

---

### **2. Computing the Probability That a Random Variable Lies Within an Unbounded Interval**

When an interval is **unbounded**, such as $`(-\infty, b]`$ or $`[a, \infty)`$, use a **definite integral** that runs to or from infinity:

$$
\boxed{
P(X > a) = \int_a^{\infty} f(x)\,dx, \quad
P(X < b) = \int_{-\infty}^{b} f(x)\,dx
}
$$

#### **Example:**

Let $`f(x) = e^{-x}`$ for $`x \geq 0`$ (PDF of an exponential distribution).
Then:

$$
P(X > 2) = \int_2^{\infty} e^{-x} \, dx = \left[ -e^{-x} \right]_2^{\infty} = 0 - (-e^{-2}) = \boxed{e^{-2}}
$$

---

### **3. Calculating Probabilities with Piecewise PDFs**

For piecewise-defined PDFs, compute the integral over each **relevant piece** of the interval and **add them** together.

#### **Example:**

Let:

$$
f(x) = 
\begin{cases}
2x & 0 \leq x < 0.5 \\
2(1 - x) & 0.5 \leq x \leq 1 \\
0 & \text{otherwise}
\end{cases}
$$

To find $`P(0.3 \leq X \leq 0.8)`$:

Break into two parts:

* $`[0.3, 0.5)`$ uses $`f(x) = 2x`$
* $`[0.5, 0.8]`$ uses $`f(x) = 2(1 - x)`$


$$
P = \int_{0.3}^{0.5} 2x \, dx + \int_{0.5}^{0.8} 2(1 - x) \, dx
= [x^2]_{0.3}^{0.5} + [2x - x^2]_{0.5}^{0.8}
= (0.25 - 0.09) + [(1.6 - 0.64) - (1.0 - 0.25)]
= 0.16 + (0.96 - 0.75) = \boxed{0.37}
$$

---

### ✅ **Summary Table**

| Task                   | Method                                                      |
| ---------------------- | ----------------------------------------------------------- |
| **Bounded interval**   | $`\int_a^b f(x)\, dx`$                                        |
| **Unbounded interval** | $`\int_a^{\infty} f(x)\, dx`$ or $`\int_{-\infty}^b f(x)\, dx`$ |
| **Piecewise PDF**      | Break integral across relevant cases, sum results           |

---

### **Conclusion**

For continuous random variables, probability is area under the curve of the PDF. Whether bounded,
unbounded, or piecewise-defined, integration is the essential tool for computing these probabilities 
accurately — forming the core of inferential and applied probability in continuous domains.
