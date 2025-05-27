## **Modeling With Continuous Uniform Distributions**

---

### **1. Overview of the Continuous Uniform Distribution**

A **continuous uniform distribution** models a situation where all outcomes in a given interval $`[a, b]`$ 
are equally likely. Its probability density function (PDF) is:

$$
f(x) = \begin{cases}
\frac{1}{b - a}, & a \le x \le b \\
0, & \text{otherwise}
\end{cases}
$$

---

### **2. Calculating a Probability in Context**

To find the probability that a value lies between $`x_1`$ and $`x_2`$ within the interval $`[a, b]`$, use:

$$
P(x_1 \le X \le x_2) = \frac{x_2 - x_1}{b - a}
$$

**Example**:
If the time a bus arrives is uniformly distributed between 8:00 and 8:30 (i.e., $`a = 0`$, $`b = 30`$ minutes), the probability it arrives between 8:10 and 8:20:

$$
P(10 \le X \le 20) = \frac{20 - 10}{30 - 0} = \frac{10}{30} = \frac{1}{3}
$$

---

### **3. Calculating an Expected Value in Context**

The **expected value** (mean) for a continuous uniform distribution is:

$$
\mathbb{E}[X] = \frac{a + b}{2}
$$

**Example**:
If a uniform variable models wait times between 0 and 10 minutes:

$$
\mathbb{E}[X] = \frac{0 + 10}{2} = 5 \text{ minutes}
$$

---

### **4. Calculating a Variance in Context**

The **variance** is given by:

$$
\text{Var}(X) = \frac{(b - a)^2}{12}
$$

And the **standard deviation**:

$$
\sigma = \sqrt{\text{Var}(X)} = \frac{b - a}{\sqrt{12}}
$$

**Example**:
For $`X \sim \text{Uniform}(0, 6)`$:

$$
\text{Var}(X) = \frac{(6 - 0)^2}{12} = \frac{36}{12} = 3
$$

---

### **Summary**

| **Quantity**                       | **Formula**                          |
| ---------------------------------- | ------------------------------------ |
| PDF $`f(x)`$                         | $`\frac{1}{b - a}`$ for $`x \in [a, b]`$ |
| Probability $`P(x_1 \le X \le x_2)`$ | $`\frac{x_2 - x_1}{b - a}`$            |
| Expected Value $`\mathbb{E}[X]`$     | $`\frac{a + b}{2}`$                    |
| Variance $`\text{Var}(X)`$           | $`\frac{(b - a)^2}{12}`$               |

The uniform model is especially useful in estimating probabilities when no preference or weighting is assumed across outcomes.
