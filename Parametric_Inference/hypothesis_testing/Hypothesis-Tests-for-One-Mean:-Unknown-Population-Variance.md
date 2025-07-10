## **Hypothesis Tests for One Mean: Unknown Population Variance**

---

### **1. Core Concept**

When testing a hypothesis about a population mean $`\mu`$ and the **population standard deviation is unknown**, we use the **t-distribution** instead of the z-distribution. This is crucial when:

* Sample size is small ($`n < 30`$)


* Population standard deviation $`\sigma`$ is unknown


* Population is approximately normal (or large enough sample for CLT)

---

### **2. Test Statistic (t-test for One Mean)**

Given:

* Sample mean $`\bar{x}`$


* Hypothesized mean $`\mu_0`$


* Sample standard deviation $s$


* Sample size $n$

$$
t = \frac{\bar{x} - \mu_0}{s/\sqrt{n}}
$$

Degrees of freedom $`df = n - 1`$

---

### **3. One-Tailed Test Example**

#### **Scenario: Right-Tailed Test**

Suppose a nutritionist claims that a new diet plan increases the average weight loss beyond 5 kg.

* Hypotheses:

  * $`H_0: \mu = 5`$
  * $`H_1: \mu > 5`$


* Sample:

  * $`n = 16`$, $`\bar{x} = 5.8`$, $`s = 1.2`$


* Significance level: $`\alpha = 0.05`$

**Step 1**: Compute the test statistic:

$$
t = \frac{5.8 - 5}{1.2/\sqrt{16}} = \frac{0.8}{0.3} = 2.667
$$

**Step 2**: Critical value from t-table for $`df = 15`$ and one-tailed $`\alpha = 0.05`$:

$$
t_{0.05,15} \approx 1.753
$$

Since $`2.667 > 1.753`$, we **reject $`H_0`$**.

✅ **Conclusion**: There's significant evidence that the diet increases weight loss beyond 5 kg.

---

### **4. Two-Tailed Test Example**

#### **Scenario**

A manufacturer claims their batteries last **on average** 100 hours. A consumer protection group wants to verify if the average is **different**.

* Hypotheses:

  * $`H_0: \mu = 100`$
  * $`H_1: \mu \ne 100`$


* Sample:

  * $`n = 10`$, $`\bar{x} = 96.5`$, $`s = 4`$


* $`\alpha = 0.05`$

**Step 1**: Test statistic

$$
t = \frac{96.5 - 100}{4/\sqrt{10}} = \frac{-3.5}{1.2649} \approx -2.767
$$

**Step 2**: Critical values for $`df = 9`$, two-tailed $`\alpha = 0.05`$:

$$
\pm t_{0.025,9} = \pm 2.262
$$

Since $`-2.767 < -2.262`$, we **reject $`H_0`$**.

✅ **Conclusion**: The average battery life is significantly different from 100 hours.

---

### **5. Large Sample Case (CLT Applies)**

Even when $`\sigma`$ is unknown, for **large samples** ($`n \geq 30`$), the sample mean is approximately normal due to the **Central Limit Theorem**, and a **t-test** is still appropriate.

#### **Example**

A bottling company claims its machines fill bottles with 500 ml on average.

* Sample: $`n = 40`$, $`\bar{x} = 497`$, $`s = 5`$


* $`H_0: \mu = 500`$, $`H_1: \mu \ne 500`$, $`\alpha = 0.01`$

$$
t = \frac{497 - 500}{5/\sqrt{40}} = \frac{-3}{0.7906} \approx -3.794
$$

$`df = 39`$; two-tailed $`\alpha = 0.01`$ critical value: $`\pm 2.708`$

Since $`-3.794 < -2.708`$, **reject $H_0$**.

✅ **Conclusion**: The machine’s fill volume is significantly different from 500 ml.

---

### **6. Applications of This Test**

| Field             | Use Case                                                       |
| ----------------- | -------------------------------------------------------------- |
| **Medicine**      | Testing average recovery time for a new drug                   |
| **Manufacturing** | Verifying machine precision (e.g., part lengths)               |
| **Education**     | Assessing whether a new curriculum changes average test scores |
| **Business**      | Evaluating whether a new training improves productivity        |
| **Marketing**     | Testing if a campaign increased average sales per customer     |

---

### **7. Summary Table**

| Element            | Description                                 |
| ------------------ |---------------------------------------------|
| Distribution       | Student’s t (when $`\sigma`$ unknown)       |
| Test Statistic     | $`t = \frac{\bar{x} - \mu_0}{s/\sqrt{n}}`$  |
| Degrees of Freedom | $`n - 1`$                                   |
| One-Tailed Test    | Use when looking for increase/decrease      |
| Two-Tailed Test    | Use when checking for any difference        |
| Large Sample       | $`n \geq 30`$; t-test remains valid via CLT |

---
