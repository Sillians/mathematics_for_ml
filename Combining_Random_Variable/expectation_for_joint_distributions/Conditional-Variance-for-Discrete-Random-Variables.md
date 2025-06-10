# **Conditional Variance for Discrete Random Variables**

Conditional variance measures how a random variable $X$ varies when another variable $Y$ is fixed at a certain value. 
It helps quantify the uncertainty in $X$ **given** that $`Y = y`$.

---

## **1. Definition**

The **conditional variance** of $X$ given $`Y = y`$, denoted $`\operatorname{Var}(X \mid Y = y)`$, is defined as:

$$
\operatorname{Var}(X \mid Y = y) = \mathbb{E}\left[(X - \mathbb{E}[X \mid Y = y])^2 \mid Y = y\right]
$$

Equivalently, using the shortcut formula:

$$
\operatorname{Var}(X \mid Y = y) = \mathbb{E}[X^2 \mid Y = y] - (\mathbb{E}[X \mid Y = y])^2
$$

---

## **2. Calculating Conditional Variance Given a Conditional Mass Function**

### **Given:**

A conditional PMF of $`X \mid Y = y`$, i.e., $`P(X = x_i \mid Y = y)`$

### **Steps:**

1. Compute $`\mathbb{E}[X \mid Y = y] = \sum_{i} x_i \cdot P(X = x_i \mid Y = y)`$
2. Compute $`\mathbb{E}[X^2 \mid Y = y] = \sum_{i} x_i^2 \cdot P(X = x_i \mid Y = y)`$
3. Apply the formula:

$$
\operatorname{Var}(X \mid Y = y) = \mathbb{E}[X^2 \mid Y = y] - (\mathbb{E}[X \mid Y = y])^2
$$

---

## **3. Calculating Conditional Variance Using Row Totals**

This method uses **row-wise conditional distributions** when a joint probability table is given.

### **Steps:**

1. For each fixed value $y$, extract the conditional PMF $`P(X = x_i \mid Y = y) = \frac{P(X = x_i, Y = y)}{P(Y = y)}`$
2. Use the conditional PMF as in section 2 to compute the conditional variance.

---

## **4. Calculating Conditional Variance Using Column Totals**

This method is similar but conditions on $`X = x`$ to compute $`\operatorname{Var}(Y \mid X = x)`$.

### **Steps:**

1. Fix a value $x$, and calculate $`P(Y = y_j \mid X = x) = \frac{P(X = x, Y = y_j)}{P(X = x)}`$
2. Find:

$$
\mathbb{E}[Y \mid X = x] = \sum_j y_j \cdot P(Y = y_j \mid X = x)
$$

$$
\mathbb{E}[Y^2 \mid X = x] = \sum_j y_j^2 \cdot P(Y = y_j \mid X = x)
$$

$$
\operatorname{Var}(Y \mid X = x) = \mathbb{E}[Y^2 \mid X = x] - (\mathbb{E}[Y \mid X = x])^2
$$

---

## **Summary Table**

| Task                      | Formula                                                                                        |
| ------------------------- | ---------------------------------------------------------------------------------------------- |
| Conditional Expectation   | $`\mathbb{E}[X \mid Y = y] = \sum x_i P(X = x_i \mid Y = y)`$                                    |
| Conditional Second Moment | $`\mathbb{E}[X^2 \mid Y = y] = \sum x_i^2 P(X = x_i \mid Y = y)`$                                |
| Conditional Variance      | $`\operatorname{Var}(X \mid Y = y) = \mathbb{E}[X^2 \mid Y = y] - (\mathbb{E}[X \mid Y = y])^2`$ |
| Joint to Conditional PMF  | $`P(X = x \mid Y = y) = \frac{P(X = x, Y = y)}{P(Y = y)}`$                                       |

---

This guide allows systematic calculation of conditional variances using either direct conditional PMFs or joint distributions via rows or columns of a probability table.
