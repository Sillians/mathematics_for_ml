## **Properties of Expectation for Discrete Random Variables**

The **expected value** (or **expectation**, **mean**) of a discrete random variable represents 
its **long-run average** value over many repetitions of the experiment. It is one of the most 
fundamental concepts in probability theory, summarizing a distribution's central tendency.

If $X$ is a discrete random variable with probability mass function (PMF) $`P(X = x_i) = p_i`$, then:

$$
\mathbb{E}[X] = \sum_i x_i \cdot p_i
$$

---

### **1. Computing the Expected Value of a Constant**

If $`X = c`$, where $c$ is a constant (i.e. $X$ always takes on value $c$):

$$
\mathbb{E}[c] = c
$$

No matter the distribution or sample space, the expectation of a constant is just the constant itself.

---

### **2. Computing the Expected Value of a Scaled Random Variable**

If $a$ is a constant and $X$ is a discrete random variable, then:

$$
\mathbb{E}[aX] = a \cdot \mathbb{E}[X]
$$

This **linearity of expectation** means scaling a random variable scales its expectation by the same factor.

#### **Example:**

If $`\mathbb{E}[X] = 4`$, then:

$$
\mathbb{E}[3X] = 3 \cdot 4 = \boxed{12}
$$

---

### **3. Computing the Expected Value of a Transformed Random Variable**

If $`Y = g(X)`$ is a transformation of $X$, then:

$$
\mathbb{E}[g(X)] = \sum_{x \in \text{Support}(X)} g(x) \cdot P(X = x)
$$

This is used for computing expectations of nonlinear functions like $X^2$, $|X|$, $\ln(X)$, etc.

#### **Example:**

Let $`X \in \{1, 2, 3\}`$ with:

$$
P(X = 1) = 0.2,\quad P(X = 2) = 0.5,\quad P(X = 3) = 0.3
$$

Find $`\mathbb{E}[X^2]`$:

$$
\mathbb{E}[X^2] = (1^2)(0.2) + (2^2)(0.5) + (3^2)(0.3) = 0.2 + 2.0 + 2.7 = \boxed{4.9}
$$

---

### ✅ **Summary Table of Properties**

| Property                      | Formula                                          |
| ----------------------------- | ------------------------------------------------ |
| **Expectation of a constant** | $`\mathbb{E}[c] = c`$                              |
| **Scaling**                   | $`\mathbb{E}[aX] = a \cdot \mathbb{E}[X]`$         |
| **Transformed variable**      | $`\mathbb{E}[g(X)] = \sum_x g(x) \cdot P(X = x)`$  |
| **Linearity (general)**       | $`\mathbb{E}[aX + b] = a \cdot \mathbb{E}[X] + b`$ |

---

### **Conclusion**

Expectation is a **linear** operator and retains its behavior even under transformations and scaling. 
Understanding how to compute expectations for constants, scaled variables, and transformed functions 
is fundamental to analysis in statistics, economics, data science, and theoretical probability.
