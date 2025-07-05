## **I.I.D. Normal Random Variables**

---

### **1. Definition and Setting**

Let $`X_1, X_2, \ldots, X_n`$ be **independent and identically distributed (i.i.d.)** normal random variables:

$$
X_i \sim \mathcal{N}(\mu, \sigma^2) \quad \text{for each } i = 1, 2, \dots, n.
$$

These satisfy:

* **Identical distributions**: All have the same mean $`\mu`$ and variance $`\sigma^2`$.
* **Independence**: Knowledge of one variable gives no information about the others.

---

### **2. Linear Combinations and the Sample Mean**

Let:

* **Sum**: $`S_n = \sum_{i=1}^n X_i`$
* **Sample Mean**: $`\overline{X}_n = \frac{1}{n} \sum_{i=1}^n X_i`$

#### 2.1 Distribution of the Sum

$$
S_n \sim \mathcal{N}(n\mu, n\sigma^2)
$$

#### 2.2 Distribution of the Sample Mean

$$
\overline{X}_n \sim \mathcal{N}\left(\mu, \frac{\sigma^2}{n}\right)
$$

> This reflects **concentration around the mean**: the larger the sample, the smaller the variance of the average.

---

### **3. Calculating Distributions and Probabilities With I.I.D. Normal Variables**

#### 3.1 Example: Probability Involving the Sample Mean

Let $`X_i \sim \mathcal{N}(10, 4)`$, and let $`\overline{X}_5`$ be the sample mean of 5 such variables.

Then:

$$
\overline{X}_5 \sim \mathcal{N}\left(10, \frac{4}{5} = 0.8\right)
$$

Find:

$$
P(9 < \overline{X}_5 < 11) = P\left( \frac{9 - 10}{\sqrt{0.8}} < Z < \frac{11 - 10}{\sqrt{0.8}} \right)
= P(-1.12 < Z < 1.12)
\approx 0.7314
$$

#### 3.2 Example: Probability Involving a Sum

Let $`X_i \sim \mathcal{N}(2, 9)`$, and find:

$$
P\left( \sum_{i=1}^{4} X_i > 10 \right)
$$

Then:

* $`S_4 \sim \mathcal{N}(8, 36)`$
* Standardize:

$$
P(S_4 > 10) = P\left(Z > \frac{10 - 8}{\sqrt{36}} \right) = P(Z > \tfrac{1}{\sqrt{9}}) = P(Z > \tfrac{1}{3}) \approx 0.3707
$$

---

### **4. Calculating Distributions and Probabilities In Context**

#### Context: Quality Control

Let each bottle of a beverage contain $`X_i \sim \mathcal{N}(500, 4)`$ ml.

**Question**: What’s the probability that a box of 10 bottles has average volume less than 498 ml?

Then:

* $`\overline{X}_{10} \sim \mathcal{N}(500, \tfrac{4}{10}=0.4)`$
* Compute:

$$
P(\overline{X}_{10} < 498) = P\left(Z < \frac{498 - 500}{\sqrt{0.4}} \right) = P(Z < -3.16) \approx 0.0008
$$

So it's **highly unlikely** under normal conditions — possibly indicates underfilling or a systematic error.

---

### **5. Key Takeaways**

| Concept                                         | Result                                                 |
|-------------------------------------------------| ------------------------------------------------------ |
| $`X_i \sim \mathcal{N}(\mu, \sigma^2)`$, i.i.d. | All $`X_i`$ independent and same distribution            |
| $`S_n = \sum X_i`$                              | $`\sim \mathcal{N}(n\mu, n\sigma^2)`$                    |
| $`\overline{X}_n = \frac{1}{n}S_n`$             | $`\sim \mathcal{N}\left(\mu, \frac{\sigma^2}{n}\right)`$ |
| Standardization                                 | $`Z = \frac{X - \mu}{\sigma} \sim \mathcal{N}(0, 1)`$    |

---

### **6. Applications**

* Statistical estimation: $`\overline{X}`$ as point estimator of $`\mu`$
* Hypothesis testing: Compare sample means to hypothesized values
* Quality control: Identify systematic errors using distribution tails
* Simulation: Normal samples generated using random generators in Monte Carlo studies

---

This framework underpins much of parametric statistics, due to the tractable and stable behavior of i.i.d. normal variables under addition and scaling.
