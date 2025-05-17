## **Continuous Random Variables Over Infinite Domains**

A **continuous random variable** defined over an **infinite domain** (such as $(-\infty, \infty)$, $[0, \infty)$, or $(-\infty, b]$) 
can still have a **valid probability density function (PDF)**—as long as the total area under the curve equals 1.

These types of random variables are common in real-world scenarios, such as **exponential**, **normal**, or **Cauchy** distributions.

---

### **1. Checking Whether a Given Function Is a Valid PDF**

To verify that a function $f(x)$ is a valid PDF over an infinite domain, it must satisfy:

#### **Conditions for a Valid PDF:**

1. **Non-negativity**:

$$
f(x) \geq 0 \quad \text{for all } x
$$

2. **Total Probability = 1**:

$$
\int_{-\infty}^{\infty} f(x)\, dx = 1
$$

or over the appropriate domain (e.g., $\int_0^\infty f(x)\, dx = 1$)

---

### **2. Solving for a Constant Given a PDF**

If a PDF includes an unknown constant $c$, determine its value by solving:

$$
\int_{a}^{b} c \cdot f(x) \, dx = 1
\quad \text{(where the limits may be infinite)}
$$

---

#### **Example:**

Let

$$
f(x) = \begin{cases}
ce^{-x}, & x \geq 0 \\
0, & x < 0
\end{cases}
$$

Find $`c`$ such that $`f(x)`$ is a valid PDF.

$$
\int_0^\infty ce^{-x} \, dx = c \cdot \int_0^\infty e^{-x} dx = c \cdot [ -e^{-x} ]_0^\infty = c(0 - (-1)) = c
$$

Set equal to 1:

$$
c = \boxed{1}
$$

So the valid PDF is $`f(x) = e^{-x}`$ for $`x \geq 0`$.

---

### **3. Computing a Probability Over an Unbounded Interval**

For infinite intervals like $`P(X > a)`$, integrate from the bound to infinity:

$$
P(X > a) = \int_a^\infty f(x) \, dx
$$

#### **Example:**

Let $`f(x) = e^{-x}`$ for $`x \geq 0`$.
Find $`P(X > 2)`$:

$$
P(X > 2) = \int_2^\infty e^{-x} dx = [-e^{-x}]_2^\infty = 0 - (-e^{-2}) = \boxed{e^{-2}}
$$

This is approximately $`0.1353`$.

---

### ✅ **Summary Table**

| Task                               | Rule or Formula                                                                   |
| ---------------------------------- | --------------------------------------------------------------------------------- |
| **Valid PDF over infinite domain** | $`\int f(x)\, dx = 1`$ and $`f(x) \geq 0`$                                            |
| **Solve for constant**             | Set $`\int f(x)\, dx = 1`$, solve for unknown                                       |
| **Unbounded probability**          | $`P(X > a) = \int_a^{\infty} f(x)\, dx`$ or $`P(X < b) = \int_{-\infty}^b f(x)\, dx`$ |

---

### **Conclusion**

Continuous random variables over infinite domains are handled through **improper integrals**. 
Despite the infinite support, valid PDFs can be defined as long as the **total area equals 1**. 
Mastering these concepts is essential for working with exponential, normal, and other real-world
probability models.
