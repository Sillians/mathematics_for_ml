## **The Continuous Uniform Distribution**

The **continuous uniform distribution** models a random variable that is equally likely to 
take **any value within a specific interval**. It is defined over a **closed interval** $[a, b]$, 
where the probability is spread evenly.

If $`X \sim \text{Uniform}(a, b)`$, then the probability density function (PDF) is:

$$
f(x) = 
\begin{cases}
\frac{1}{b - a}, & a \leq x \leq b \\
0, & \text{otherwise}
\end{cases}
$$

---

### **1. Computing a "Less Than" Probability**

To compute the probability that $X$ is **less than a value $c$**, where $a \leq c \leq b$:

$$
P(X < c) = \int_a^c \frac{1}{b - a} \, dx = \frac{c - a}{b - a}
$$

#### **Example:**

If $`X \sim \text{Uniform}(2, 10)`$, find $`P(X < 5)`$:

$$
P(X < 5) = \frac{5 - 2}{10 - 2} = \frac{3}{8}
$$

---

### **2. Computing the Probability Over an Interval**

To compute the probability that $X$ falls within an interval $`[c, d]`$, where $`a \leq c < d \leq b`$:

$$
P(c \leq X \leq d) = \int_c^d \frac{1}{b - a} \, dx = \frac{d - c}{b - a}
$$

#### **Example:**

If $`X \sim \text{Uniform}(0, 6)`$, find $`P(2 \leq X \leq 4)`$:

$$
P(2 \leq X \leq 4) = \frac{4 - 2}{6 - 0} = \frac{2}{6} = \frac{1}{3}
$$

---

### **3. Computing a "Greater Than" Probability**

To compute the probability that $X$ is **greater than a value $c$**, where $a \leq c \leq b$:

$$
P(X > c) = \int_c^b \frac{1}{b - a} \, dx = \frac{b - c}{b - a}
$$

#### **Example:**

If $`X \sim \text{Uniform}(1, 5)`$, find $`P(X > 3)`$:

$$
P(X > 3) = \frac{5 - 3}{5 - 1} = \frac{2}{4} = \frac{1}{2}
$$

---

### ✅ **Summary Table**

| Probability Type     | Formula               |
| -------------------- | --------------------- |
| $`P(X < c)`$           | $`\frac{c - a}{b - a}`$ |
| $`P(c \leq X \leq d)`$ | $`\frac{d - c}{b - a}`$ |
| $`P(X > c)`$           | $`\frac{b - c}{b - a}`$ |

---

### **Conclusion**

The continuous uniform distribution offers a straightforward model for equally likely outcomes 
over a range. All probability computations reduce to **linear proportions** of the interval, 
making it one of the most intuitive continuous distributions.
