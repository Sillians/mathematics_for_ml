## **Sample Means From Normal Populations**

---

### **1. Introduction: Why Sample Means Matter**

In statistical inference, we often collect a sample from a population to estimate a parameter 
(like the population mean). When the underlying population is **normally distributed**, 
the behavior of the **sample mean** is particularly well-understood and useful.

Let:

* $`X_1, X_2, \dots, X_n \sim \mathcal{N}(\mu, \sigma^2)`$ be i.i.d. normal random variables.
* The **sample mean** is $`\overline{X}_n = \dfrac{1}{n} \sum_{i=1}^n X_i`$.

---

### **2. Stating the Distribution of the Sample Mean**

If the population is normal, i.e. $`X_i \sim \mathcal{N}(\mu, \sigma^2)`$, then the sample mean $`\overline{X}_n`$ is **also normally distributed**, regardless of the sample size:

$$
\overline{X}_n \sim \mathcal{N}\left(\mu, \frac{\sigma^2}{n} \right)
$$

| Quantity | Value                 |
| -------- |-----------------------|
| Mean     | $`\mu`$               |
| Variance | $`\sigma^2 / n`$      |
| Std. Dev | $`\sigma / \sqrt{n}`$ |

> This result is exact when sampling from a normal population (no need to invoke the Central Limit Theorem).

---

### **3. Calculating a Probability Involving a Sample Mean**

We use the standardization process:

$$
Z = \frac{\overline{X}_n - \mu}{\sigma / \sqrt{n}} \sim \mathcal{N}(0,1)
$$

#### **Example:**

Suppose:

* $`X_i \sim \mathcal{N}(50, 25)`$
* $`n = 16 \Rightarrow \overline{X}_{16} \sim \mathcal{N}(50, \tfrac{25}{16})`$
* Find: $`P(\overline{X}_{16} > 52)`$

**Step 1:** Compute standard deviation:

$$
\sigma_{\overline{X}} = \frac{5}{\sqrt{16}} = 1.25
$$

**Step 2:** Standardize:

$$
Z = \frac{52 - 50}{1.25} = 1.6
$$

**Step 3:** Use standard normal table:

$$
P(Z > 1.6) = 1 - \Phi(1.6) \approx 1 - 0.9452 = 0.0548
$$

**Answer:** $`P(\overline{X}_{16} > 52) \approx 0.0548`$

---

### **4. Calculating a Probability Involving a Sample Mean in Context**

#### **Contextual Example: Manufacturing Batteries**

A factory claims battery lifespans follow a normal distribution with:

* Mean $`\mu = 1000`$ hours
* Std. dev. $`\sigma = 80`$ hours

A quality inspector selects a **sample of 25 batteries**. What's the probability that the **average** lifespan is **less than 970 hours**?

---

**Step 1:**

$$
\overline{X}_{25} \sim \mathcal{N}\left(1000, \frac{80^2}{25} = 256\right)
\quad \Rightarrow \quad \sigma_{\overline{X}} = 16
$$

**Step 2:**

$$
Z = \frac{970 - 1000}{16} = -1.875
$$

**Step 3:**

$$
P(\overline{X} < 970) = \Phi(-1.875) \approx 0.0304
$$

**Interpretation:** There's about a **3.04%** chance the average lifespan of 25 randomly
chosen batteries is under 970 hours — low enough to potentially trigger concern in quality control.

---

### **5. Summary Table**

| Concept                                | Formula                                                          |
|----------------------------------------| ---------------------------------------------------------------- |
| Sample mean $`\overline{X}_n`$         | $`\dfrac{1}{n} \sum X_i`$                                          |
| Distribution (from normal population)  | $`\mathcal{N}\left(\mu, \dfrac{\sigma^2}{n} \right)`$              |
| Standardization                        | $`Z = \dfrac{\overline{X}_n - \mu}{\sigma / \sqrt{n}}`$            |
| Use case                               | Estimating probabilities, confidence intervals, hypothesis tests |

---

### **6. Applications in Practice**

* **Quality control**: Is a process mean shifting?
* **Medical trials**: Are average effects of treatment significant?
* **Agriculture**: Is average crop yield above a threshold?
* **Finance**: Is average daily return greater than expected?

---

### **7. Key Insights**

* When sampling from a **normal distribution**, the sample mean is also normal, regardless of sample size.
* The **variance of the sample mean decreases** with increasing sample size, improving estimate precision.
* Probabilities involving sample means are computed using the **standard normal distribution** via standardization.

---

This framework underpins confidence interval construction, z-tests for means, and central limit intuition in practical data-driven decisions.
