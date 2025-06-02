## **Sampling Distributions**

---

#### **Definition**

A **sampling distribution** is the probability distribution of a **statistic** (e.g., mean, variance, proportion) calculated from a random sample of a population.

Let $`\theta`$ be a population parameter (e.g., mean $`\mu`$), and let $`\hat{\theta}`$ be a statistic estimated 
from a sample. The distribution of $`\hat{\theta}`$, when repeatedly computed from different random samples, 
forms the **sampling distribution of $`\hat{\theta}`$**.

---

### **1. Identifying Statistics**

A **statistic** is any quantity computed from sample data without using unknown population parameters.

**Common examples:**

* **Sample mean:**

$$
\bar{X} = \frac{1}{n} \sum_{i=1}^n X_i
$$

* **Sample variance:**

$$
S^2 = \frac{1}{n-1} \sum_{i=1}^n (X_i - \bar{X})^2
$$

* **Sample proportion (for binary data):**

$$
\hat{p} = \frac{\text{Number of successes}}{n}
$$

These statistics are **random variables** because they vary across samples.

---

### **2. Calculating Statistics**

To compute a statistic:

* Collect a random sample $`\{X_1, X_2, ..., X_n\}`$
* Apply the statistic’s formula.

##### **Example – Sample Mean:**

Given data: $`X_1 = 5, X_2 = 7, X_3 = 8`$

$$
\bar{X} = \frac{5 + 7 + 8}{3} = \frac{20}{3} \approx 6.67
$$

##### **Example – Sample Variance:**

$$
S^2 = \frac{1}{3 - 1} [(5 - 6.67)^2 + (7 - 6.67)^2 + (8 - 6.67)^2]
$$

$$
= \frac{1}{2}[(2.78) + (0.11) + (1.78)] = \frac{4.67}{2} = 2.335
$$

---

### **Properties of Sampling Distributions**

#### **Sample Mean $`\bar{X}`$:**

If $`X_1, ..., X_n`$ are i.i.d. with mean $`\mu`$ and variance $`\sigma^2`$, then:

* **Mean of $`\bar{X}`$:**

$$
\mathbb{E}[\bar{X}] = \mu
$$

* **Variance of $`\bar{X}`$:**

$$
\text{Var}(\bar{X}) = \frac{\sigma^2}{n}
$$

* **Shape:** By the **Central Limit Theorem**, if $`n`$ is large, $`\bar{X}`$ is approximately normally distributed:

$$
\bar{X} \sim \mathcal{N}(\mu, \frac{\sigma^2}{n})
$$

---

### **Why Sampling Distributions Matter**

* Enable construction of **confidence intervals**
* Allow **hypothesis testing**
* Quantify the **uncertainty** of estimates

---

### **Key Takeaways**

* A statistic is a function of sample data (e.g., $`\bar{X}, S^2, \hat{p}`$).
* The sampling distribution tells how a statistic varies across samples.
* The **expected value** and **standard error** of statistics are crucial to inference.
* The **Central Limit Theorem** makes normal approximation possible even if the underlying population is not normal, for large $`n`$.
