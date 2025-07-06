## **Confidence Intervals for Two Means: Known and Unequal Population Variances**

---

### **1. Overview**

When comparing the means of two populations with **known and unequal variances**, and either:

* both populations are **normally distributed**, or


* both samples are **large (typically n ≥ 30)**,

we construct a **confidence interval for the difference in means**:

$$
(\mu_1 - \mu_2) \in \left[(\bar{x}_1 - \bar{x}_2) \pm z_{\alpha/2} \cdot \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}} \right]
$$

Where:

* $`\bar{x}_1, \bar{x}_2`$: sample means


* $`\sigma_1^2, \sigma_2^2`$: **known** population variances


* $`n_1, n_2`$: sample sizes


* $`z_{\alpha/2}`$: z-value for the desired confidence level

---

### **2. Finding Confidence Intervals Given Two Normal Populations**

If both populations are **normally distributed** and variances are known:

#### **Formula:**

$$
CI = (\bar{x}_1 - \bar{x}_2) \pm z_{\alpha/2} \cdot \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}
$$

#### **Example:**

* Population 1: $`\bar{x}_1 = 100`$, $`\sigma_1 = 10`$, $`n_1 = 25`$


* Population 2: $`\bar{x}_2 = 95`$, $`\sigma_2 = 8`$, $`n_2 = 30`$


* 95% Confidence → $`z_{\alpha/2} = 1.96`$

$$
SE = \sqrt{\frac{10^2}{25} + \frac{8^2}{30}} = \sqrt{4 + 2.133} = \sqrt{6.133} \approx 2.476
$$

$$
CI = 5 \pm 1.96 \cdot 2.476 \Rightarrow 5 \pm 4.85 \Rightarrow (0.15,\ 9.85)
$$

---

### **3. Finding Confidence Intervals Given Two Large Samples**

Even if the underlying distributions are not normal, **by the Central Limit Theorem**, large samples make the sample means approximately normal.

Same formula applies:

$$
CI = (\bar{x}_1 - \bar{x}_2) \pm z_{\alpha/2} \cdot \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}
$$

This allows inference on population mean differences without assuming normality of the population.

---

### **4. Applications of Confidence Intervals**

#### **a. Product Comparison**

A company compares the lifespans of two battery brands to decide if there's a significant performance difference.


#### **b. Medical Studies**

Researchers test whether a new drug reduces recovery time more than the standard treatment.


#### **c. Manufacturing Quality**

An engineer assesses whether a new machine produces parts more consistently than an older one.

---

### **5. Interpretation**

* If the **entire CI lies above 0**, it suggests $`\mu_1 > \mu_2`$


* If it **includes 0**, the difference is **not statistically significant** at the given confidence level


* If it lies **below 0**, it suggests $`\mu_1 < \mu_2`$

---

### **Summary Table**

| Component           | Formula / Description                                    |
| ------------------- | -------------------------------------------------------- |
| Standard Error (SE) | $`\sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}`$ |
| Z-score             | From normal table for confidence level                   |
| Confidence Interval | $`(\bar{x}_1 - \bar{x}_2) \pm z_{\alpha/2} \cdot SE`$      |
| Assumptions         | Known variances, normal populations or large samples     |

---
