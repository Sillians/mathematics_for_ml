## **Hypothesis Tests for Two Means: Known Population Variances**

---

### **1. Overview: Comparing Two Population Means**

When comparing two population means $`\mu_1`$ and $`\mu_2`$, and **both population variances $`\sigma_1^2`$ 
and $`\sigma_2^2`$ are known**, we use a **two-sample z-test**. This test assesses whether the observed difference in sample means is statistically significant.

#### **General Setup**

Let:

* $`\bar{X}_1 \sim N(\mu_1, \sigma_1^2/n_1)`$


* $`\bar{X}_2 \sim N(\mu_2, \sigma_2^2/n_2)`$

We test:

$$
H_0: \mu_1 = \mu_2 \quad \text{or} \quad H_0: \mu_1 - \mu_2 = \Delta_0
$$

Usually $`\Delta_0 = 0`$, unless specified otherwise.

#### **Test Statistic**:

$$
z = \frac{(\bar{x}_1 - \bar{x}_2) - \Delta_0}{\sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}}
$$

---

### **2. One-Tailed Test (Given Two Normal Populations)**

#### **Example (Right-Tailed Test)**:

A researcher tests whether a new teaching method improves scores compared to the standard method.

* Standard method: $`\bar{x}_1 = 78`$, $`\sigma_1 = 10`$, $`n_1 = 40`$


* New method: $`\bar{x}_2 = 82`$, $`\sigma_2 = 12`$, $`n_2 = 35`$


* Claim: New method **improves scores** ⇒ $`H_1: \mu_2 > \mu_1`$

**Step 1**: Set hypotheses

* $`H_0: \mu_1 = \mu_2`$
* $`H_1: \mu_2 > \mu_1`$

**Step 2**: Compute test statistic

$$
z = \frac{82 - 78}{\sqrt{\frac{10^2}{40} + \frac{12^2}{35}}}
= \frac{4}{\sqrt{2.5 + 4.114}} \approx \frac{4}{2.537} \approx 1.577
$$

**Step 3**: Critical value at $`\alpha = 0.05`$: $`z_{0.05} = 1.645`$

Since $`1.577 < 1.645`$, **fail to reject $H_0$**

#### ✅ Conclusion: No significant evidence at 5% to support the claim that the new method is better.

---

### **3. Two-Tailed Test (Given Two Normal Populations)**

#### **Example (Two-Tailed Test)**:

An analyst compares two machines' mean production times. Data:

* Machine A: $`\bar{x}_1 = 45`$, $`\sigma_1 = 5`$, $`n_1 = 50`$


* Machine B: $`\bar{x}_2 = 47`$, $`\sigma_2 = 6`$, $`n_2 = 60`$

Test if the machines perform **differently**.

**Hypotheses**:

* $`H_0: \mu_1 = \mu_2`$


* $`H_1: \mu_1 \ne \mu_2`$

**Test statistic**:

$$
z = \frac{45 - 47}{\sqrt{\frac{25}{50} + \frac{36}{60}}}
= \frac{-2}{\sqrt{0.5 + 0.6}} = \frac{-2}{1.049} \approx -1.907
$$

**Critical values** for $`\alpha = 0.05`$: $`\pm 1.96`$

Since $-1.907 \in (-1.96, 1.96)$, **fail to reject $H_0$**

#### ✅ Conclusion: No significant difference in mean production time at the 5% level.

---

### **4. Hypothesis Testing with Two Large Samples (CLT)**

If the population variances are **known** and the **sample sizes are large** (typically $`n \geq 30`$), 
the z-test remains valid **even if the populations are not normal**, due to the Central Limit Theorem.


#### **Example**:

* Group A: $`\bar{x}_1 = 100`$, $`\sigma_1 = 20`$, $`n_1 = 100`$


* Group B: $`\bar{x}_2 = 104`$, $`\sigma_2 = 25`$, $`n_2 = 120`$

Test if the means are different at $\alpha = 0.01$

$$
z = \frac{100 - 104}{\sqrt{400/100 + 625/120}} = \frac{-4}{\sqrt{4 + 5.208}} = \frac{-4}{3.059} \approx -1.308
$$

**Critical values** at $`\alpha = 0.01`$: $`\pm 2.576`$

Since $`-1.308 > -2.576`$, **fail to reject $`H_0`$**

#### ✅ Conclusion: No significant difference at the 1% level.

---

### **5. Applications of Two-Sample Hypothesis Testing**

| Field             | Use Case                                                      |
| ----------------- | ------------------------------------------------------------- |
| **Medicine**      | Compare average effectiveness of two drugs or treatments      |
| **Marketing**     | Compare average conversion rates of two ad campaigns          |
| **Education**     | Compare mean scores under two teaching methods                |
| **Manufacturing** | Assess if two machines or processes produce different results |
| **Economics**     | Compare income levels or spending behavior between groups     |

These tests help make **data-driven decisions** by quantifying whether observed differences are **statistically significant** rather than due to random variation.

---

### **6. Summary Table**

| Component       | Description                                                                               |
| --------------- |-------------------------------------------------------------------------------------------|
| Known Variances | Use **z-test** for two means                                                              |
| Assumptions     | Independent samples, normal population or large $n$                                       |
| One-Tailed      | Tests if $`\mu_1 > \mu_2`$ or $`\mu_1 < \mu_2`$                                           |
| Two-Tailed      | Tests if $`\mu_1 \ne \mu_2`$                                                              |
| Test Statistic  | $`z = \frac{(\bar{x}_1 - \bar{x}_2) - \Delta_0}{\sqrt{\sigma_1^2/n_1 + \sigma_2^2/n_2}}`$ |
| Decision Rule   | Compare $z$ to critical z-values from standard normal                                     |

---
