## **Conditional Expectation for Discrete Random Variables**

---

### **1. What Is Conditional Expectation?**

The **conditional expectation** of a discrete random variable $X$ given another random variable $`Y = y`$ is 
the **expected value of $X$** computed using the **conditional probability mass function** of $X$ given $`Y = y`$.

It is denoted as:

$$
\mathbb{E}[X \mid Y = y] = \sum_{x} x \cdot P(X = x \mid Y = y)
$$

---

### **2. Calculating a Conditional Expected Value Given a Conditional Mass Function**

If you already have the **conditional PMF** $`f_{X|Y}(x \mid y)`$, the conditional expectation is:

$$
\mathbb{E}[X \mid Y = y] = \sum_{x} x \cdot f_{X|Y}(x \mid y)
$$

**Example:**

Suppose:

$$
f_{X|Y}(x \mid 1) = \begin{cases}
0.2 & x = 0 \\
0.5 & x = 1 \\
0.3 & x = 2
\end{cases}
$$

Then:

$$
\mathbb{E}[X \mid Y = 1] = 0 \cdot 0.2 + 1 \cdot 0.5 + 2 \cdot 0.3 = 0 + 0.5 + 0.6 = 1.1
$$

---

### **3. Calculating a Conditional Expectation Using Row Totals (Fix $Y = y$)**

If you are given a **joint distribution table**:

* Fix $`Y = y`$ (i.e., a **row**),
* Compute the marginal total $`P(Y = y)`$,
* For each value $x$, compute $`f(x, y)/P(Y = y)`$ → this gives the conditional PMF,
* Use it to compute $`\mathbb{E}[X \mid Y = y]`$ via:

$$
\mathbb{E}[X \mid Y = y] = \sum_x x \cdot \frac{f(x, y)}{P(Y = y)}
$$

---

### **4. Calculating a Conditional Expectation Using Column Totals (Fix $X = x$)**

Similarly, if you fix $`X = x`$ (a **column** in the table):

$$
\mathbb{E}[Y \mid X = x] = \sum_y y \cdot \frac{f(x, y)}{P(X = x)}
$$

* Compute the **column total** $`P(X = x)`$,
* Normalize each $`f(x, y)`$ over that column,
* Multiply each $`y`$ by its corresponding conditional probability and sum.

---

### ✅ **Summary**

| **Task**                                               | **Method**                                                 |
| ------------------------------------------------------ | ---------------------------------------------------------- |
| **Conditional Expectation** $`\mathbb{E}[X \mid Y = y]`$ | $`\sum_x x \cdot P(X = x \mid Y = y)`$                       |
| **Using Row Totals** (Fixed $`Y = y`$)                   | Normalize row $`f(x, y)`$, then sum $`x \cdot f(x \mid y)`$    |
| **Using Column Totals** (Fixed $`X = x`$)                | Normalize column $`f(x, y)`$, then sum $`y \cdot f(y \mid x)`$ |

Conditional expectation is a key tool in **Bayesian reasoning**, **sequential decision making**, and **regression**. 
It allows you to understand the average behavior of one variable when another is known.
