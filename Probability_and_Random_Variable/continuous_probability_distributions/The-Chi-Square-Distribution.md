## **The Chi-Square Distribution**

---

### **1. Overview of the Chi-Square Distribution**

The **chi-square distribution** (denoted $`\chi^2_k`$) is a continuous probability distribution commonly used in statistical inference, 
especially in hypothesis testing and confidence interval estimation.

A chi-square random variable arises as the **sum of squares of independent standard normal variables**.

If $`Z_1, Z_2, \dots, Z_k \sim N(0, 1)`$, then:

$$
X = Z_1^2 + Z_2^2 + \dots + Z_k^2 \sim \chi^2_k
$$

* $`k`$ is called the **degrees of freedom** (df)
* The distribution is **skewed right**, but approaches normality as $`k`$ increases

---

###  **2. Computing a Probability Using the Chi-Square PDF**

The probability density function (PDF) for the chi-square distribution with $`k`$ degrees of freedom is:

$$
f(x; k) = \frac{1}{2^{k/2} \Gamma(k/2)} x^{(k/2) - 1} e^{-x/2}, \quad x > 0
$$

To compute a probability:

$$
P(a \leq X \leq b) = \int_a^b f(x; k) \, dx
$$

However, this integral is not elementary, so numerical methods or software (like Python, R, or statistical tables) are typically used.

---

###  **3. Using a Percentage Points Table to Find a Chi-Square Probability**

Chi-square **percentage points tables** (also called **critical value tables**) give the value $x$ such that:

$$
P(X \leq x) = p
$$

for various $p$ values (like 0.95, 0.99) and degrees of freedom $k$.

**Example**:
From the table, if $`k = 5`$, the 95th percentile is approximately 11.07:

$$
P(X \leq 11.07) = 0.95
$$

This means there's a 5% chance that a chi-square variable with 5 df exceeds 11.07.

---

### **4. Computing a Chi-Square Probability Using the Complement**

Often we use the **complement rule**:

$$
P(X > x) = 1 - P(X \leq x)
$$

This is useful for finding upper-tail probabilities, such as in goodness-of-fit tests or test statistics.

**Example**:
If $P(X \leq 11.07) = 0.95$, then:

$$
P(X > 11.07) = 1 - 0.95 = 0.05
$$

---

###  **5. Finding a Probability Involving Sums of Squared Standard Normal Variables**

Given $`Z_i \sim N(0,1)`$, the sum $`S = Z_1^2 + Z_2^2 + \cdots + Z_k^2`$ follows:

$$
S \sim \chi^2_k
$$

This directly leads to applications such as:

* Estimating **sample variance**
* Performing **chi-square goodness-of-fit tests**
* Constructing **confidence intervals** for variance
* Performing **independence tests** in contingency tables

**Example**:
If you compute $`Z_1^2 + Z_2^2 + Z_3^2`$, then $`S \sim \chi^2_3`$
To find $`P(S > 7.8)`$, use the chi-square table or software for $`\chi^2_3`$.

---

### ✅ **Summary Table**

| **Feature**        | **Chi-Square Distribution**                                 |
| ------------------ | ----------------------------------------------------------- |
| PDF                | $`\frac{1}{2^{k/2} \Gamma(k/2)} x^{(k/2)-1} e^{-x/2}`$        |
| Support            | $`x > 0`$                                                     |
| Degrees of Freedom | $`k \in \mathbb{N}`$                                          |
| Mean               | $`\mu = k`$                                                   |
| Variance           | $`\sigma^2 = 2k`$                                             |
| Application        | Variance analysis, hypothesis testing, confidence intervals |

---

The **chi-square distribution** is central to inferential statistics. It bridges the gap between raw data (through squared standard normal variables) 
and critical decision-making through hypothesis testing and interval estimation.
