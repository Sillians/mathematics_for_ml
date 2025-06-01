## **Conditional Distributions for Discrete Random Variables**

---

### **1. What Is a Conditional Distribution?**

A **conditional distribution** describes the probability of one variable given that the other has taken a specific value. It answers the question:

> *"What is the probability distribution of $X$ given that $Y = y$?"*

---

### **2. Computing a Conditional Probability**

The conditional probability of $`X = x`$ given $`Y = y`$ is:

$$
P(X = x \mid Y = y) = \frac{P(X = x, Y = y)}{P(Y = y)}
$$

You need:

* The **joint probability** $`P(X = x, Y = y)`$
* The **marginal probability** $`P(Y = y)`$

**Example:**

If

* $`P(X = 2, Y = 1) = 0.1`$
* $`P(Y = 1) = 0.25`$

Then:

$$
P(X = 2 \mid Y = 1) = \frac{0.1}{0.25} = 0.4
$$

---

### **3. Computing a Conditional Probability Over an Interval**

To compute something like:

$$
P(X \leq 2 \mid Y = 1)
$$

Sum all conditional probabilities for $`X = 0, 1, 2`$ given $`Y = 1`$:

$$
P(X \leq 2 \mid Y = 1) = P(X = 0 \mid Y = 1) + P(X = 1 \mid Y = 1) + P(X = 2 \mid Y = 1)
$$

Each term is computed using:

$$
P(X = x \mid Y = 1) = \frac{P(X = x, Y = 1)}{P(Y = 1)}
$$

---

### **4. Computing the Value of a Conditional Probability Mass Function at a Point**

To compute the **value of a conditional PMF** $`f_{X|Y}(x \mid y)`$, use:

$$
f_{X|Y}(x \mid y) = \frac{f(x, y)}{f_Y(y)}
$$

* $`f(x, y)`$ is the joint PMF
* $`f_Y(y) = \sum_x f(x, y)`$ is the marginal PMF of $Y$

**Example:**

If:

* $`f(1, 2) = 0.1`$,
* $`f_Y(2) = 0.25`$

Then:

$$
f_{X|Y}(1 \mid 2) = \frac{0.1}{0.25} = 0.4
$$

---

### **5. Computing the Entire Conditional Probability Mass Function**

To compute the full **conditional distribution** of $X$ given $`Y = y`$:

1. **Fix $`Y = y`$**
2. For each $x$, compute:

$$
f_{X|Y}(x \mid y) = \frac{f(x, y)}{\sum_x f(x, y)}
$$

This gives a new **probability distribution** over $X$, **conditioned on** a particular value of $Y$.

---

### ✅ Summary Table

| **Task**                                      | **Method**                                       |                                                    |
| --------------------------------------------- | ------------------------------------------------ | -------------------------------------------------- |
| Conditional Probability $`P(X = x \mid Y = y)`$ | $`\frac{P(X = x, Y = y)}{P(Y = y)}`$               |                                                    |
| Conditional Probability Over Interval         | Sum $`P(X = x \mid Y = y)`$ for values in interval |                                                    |
| Conditional PMF at a Point                    | ( f\_{X                                          | Y}(x \mid y) = \frac{f(x, y)}{f\_Y(y)} )           |
| Full Conditional PMF                          | Compute ( f\_{X                                  | Y}(x \mid y) ) for all $x$, normalize over $`Y = y`$ |

Conditional distributions are fundamental for understanding **dependency**, **Bayesian inference**, and **predictive modeling** in probability and statistics.
