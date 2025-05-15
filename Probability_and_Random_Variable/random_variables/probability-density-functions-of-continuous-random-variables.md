## **Probability Density Functions (PDFs) of Continuous Random Variables**

In probability theory, a **Probability Density Function (PDF)** describes the **likelihood** of 
a **continuous random variable** taking on a specific range of values. Unlike discrete variables, 
for a continuous random variable $X$, the probability of taking any exact value is **zero** — only 
ranges matter.

---

### **1. Identifying Continuous Random Variables Given in Context**

A **continuous random variable** is one that can take **any value within an interval** 
(finite or infinite). It’s used when outcomes are measured rather than counted.

#### ✅ **Examples of Continuous Random Variables:**

* The **time** a customer waits in line
* The **temperature** in a city at a given time
* The **height** of a randomly chosen person
* The **proportion** of defective items in a batch

These variables can take on an **uncountably infinite** number of values and are modeled using **PDFs**.

---

### **2. Determining Whether a Function Is a Valid PDF**

A function $f(x)$ is a **valid PDF** of a continuous random variable $X$ if it satisfies **two conditions**:

1. **Non-negativity**:

$$
f(x) \geq 0 \quad \text{for all } x
$$

2. **Total Area Under the Curve Equals 1**:

$$
\int_{-\infty}^{\infty} f(x) \, dx = 1
$$

These ensure that $`f(x)`$ represents a **true probability distribution** over $`x`$.

#### **Example:**

$$
f(x) = \begin{cases}
2x & \text{for } 0 \leq x \leq 1 \\
0 & \text{otherwise}
\end{cases}
$$

Check total probability:

$$
\int_0^1 2x \, dx = \left[ x^2 \right]_0^1 = 1^2 - 0 = 1
$$

✅ Valid PDF

---

### **3. Determining the Value of an Unknown Constant Given a PDF**

When a PDF is defined with an unknown constant $c$, you solve for $c$ by enforcing the total area rule:

$$
\int_{a}^{b} c \cdot f(x) \, dx = 1
$$

#### **Example:**

Let:

$$
f(x) = \begin{cases}
c(1 - x^2) & \text{for } -1 \leq x \leq 1 \\
0 & \text{otherwise}
\end{cases}
$$

Find $`c`$ such that $`f(x)`$ is a valid PDF:

$$
\int_{-1}^{1} c(1 - x^2) \, dx = c \int_{-1}^{1} (1 - x^2) \, dx
= c\left[ x - \frac{x^3}{3} \right]_{-1}^{1}
= c \left( \left(1 - \frac{1}{3}\right) - \left(-1 + \frac{1}{3} \right) \right)
= c \left( \frac{2}{3} + \frac{2}{3} \right) = c \cdot \frac{4}{3}
$$

Set equal to 1:

$$
c \cdot \frac{4}{3} = 1 \Rightarrow c = \frac{3}{4}
$$

---

### ✅ **Summary Table**

| Task                   | Key Formula or Rule                         |
| ---------------------- | ------------------------------------------- |
| Identify continuous RV | Values over intervals (not countable)       |
| Valid PDF condition 1  | $`f(x) \geq 0`$ for all $`x`$                   |
| Valid PDF condition 2  | $`\int_{-\infty}^{\infty} f(x)\, dx = 1`$     |
| Find constant $`c`$      | Solve $`\int f(x)\, dx = 1`$ over the support |

---

### **Conclusion**

Understanding **PDFs for continuous random variables** is fundamental to probability and statistics. 
The key is recognizing how density functions **describe probability over intervals**, 
ensuring **non-negativity and total probability of 1**, and solving for unknown parameters 
through **integration**. PDFs lay the groundwork for computing expectations, variances, 
and modeling real-world continuous data.
