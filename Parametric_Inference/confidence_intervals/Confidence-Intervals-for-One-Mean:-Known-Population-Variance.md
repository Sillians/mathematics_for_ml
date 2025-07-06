## **Confidence Intervals for One Mean: Known Population Variance**

### **1. Overview**

A **confidence interval (CI)** provides a range of plausible values for an unknown population mean $`\mu`$, 
based on sample data. When the **population variance $`\sigma^2`$ is known**, and either the population is normal or the sample size is large, 
the **standard normal distribution** is used to construct the interval.

---

### **2. Formula for the Confidence Interval**

Given:

* $`\bar{X}`$: sample mean
* $`\sigma`$: known population standard deviation
* $`n`$: sample size
* $`z_{\alpha/2}`$: critical value from the standard normal distribution for confidence level $`1 - \alpha`$

The **confidence interval** for the population mean $`\mu`$ is:

$$
\bar{X} \pm z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}}
$$

---

### **3. Finding Confidence Intervals from Normal Populations**

If the population is **normally distributed**, the confidence interval is **exact** for any sample size $n$.

#### **Steps**:

1. Identify $`\bar{X}, \sigma, n`$
2. Choose confidence level (e.g., 90%, 95%, 99%)
3. Find corresponding $`z_{\alpha/2}`$ (e.g., 1.645, 1.96, 2.576)
4. Plug into the formula

#### **Example**:

* Population is normal
* $`\bar{X} = 100`$, $`\sigma = 10`$, $`n = 25`$, 95% confidence
* $`z_{0.025} = 1.96`$

$$
CI = 100 \pm 1.96 \cdot \frac{10}{\sqrt{25}} = 100 \pm 3.92 = (96.08,\; 103.92)
$$

---

### **4. Finding Confidence Intervals from Large Samples**

If the population is **not normal**, but the sample size is **large** (typically $`n \geq 30`$), 
the **Central Limit Theorem** ensures the sampling distribution of $`\bar{X}`$ is approximately normal.

The **same formula** applies:

$$
\bar{X} \pm z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}}
$$

#### **Example**:

* Non-normal population
* $`\bar{X} = 78`$, $`\sigma = 12`$, $`n = 64`$, 90% confidence
* $`z_{0.05} = 1.645`$

$$
CI = 78 \pm 1.645 \cdot \frac{12}{\sqrt{64}} = 78 \pm 2.47 = (75.53,\; 80.47)
$$

---

### **5. Finding Confidence Intervals: Applications**

| **Field**         | **Application**                                                            |
| ----------------- | -------------------------------------------------------------------------- |
| **Healthcare**    | Estimating average systolic blood pressure in a population                 |
| **Manufacturing** | Estimating the mean weight of a packaged product to meet quality standards |
| **Education**     | Estimating the average test score of students in a large district          |
| **Finance**       | Estimating the average return of a stock over a certain period             |
| **Marketing**     | Estimating the average time users spend on a website after a UI change     |

These intervals provide decision-makers with a **range of plausible values** for the true population mean, reflecting **sampling uncertainty**.

---

### **6. Key Points to Remember**

* Use **z-distribution** only when **population variance is known**.
* Use **t-distribution** when $`\sigma`$ is **unknown**.
* Confidence level determines the **width** of the interval: higher confidence ⇒ wider interval.
* The larger the sample size $n$, the **narrower** the interval.

---

This method is foundational for statistical inference, especially when you have **prior knowledge of 
population variability** and want precise estimates of the population mean.
