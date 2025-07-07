## **Confidence Intervals for One Mean: Unknown Population Variance**

---

When the population variance $`\sigma^2`$ is **unknown**, we cannot use the normal distribution directly to compute a confidence interval 
for the population mean $`\mu`$. Instead, we use the **Student’s t-distribution**, which accounts for the uncertainty introduced by 
estimating the standard deviation from the sample.

---

### **1. Core Idea**

For a random sample $`X_1, X_2, \dots, X_n`$ from a population with **unknown variance**, the **(1 − α) confidence interval** for the **population mean** $`\mu`$ is:

$$
\boxed{
\bar{x} \pm t_{\alpha/2,\, n-1} \cdot \frac{s}{\sqrt{n}}
}
$$

Where:

* $`\bar{x}`$: sample mean
* $s$: sample standard deviation
* $n$: sample size
* $`t_{\alpha/2,\, n-1}`$: critical value from the **t-distribution** with $`n - 1`$ degrees of freedom
* The interval has a **wider margin** than the normal case to reflect more uncertainty.

---

### **2. Finding Confidence Intervals From Normal Populations**

If the population is known to be **normally distributed**, the t-distribution-based interval is valid **for any sample size** $`n \geq 2`$.

#### **Example:**

Suppose a sample of 12 yields:

* $`\bar{x} = 45`$
* $`s = 5.2`$
* Confidence level: 95%

Degrees of freedom: $`df = 11`$
From the t-table: $`t_{0.025,\,11} \approx 2.201`$

$$
\text{CI} = 45 \pm 2.201 \cdot \frac{5.2}{\sqrt{12}} = 45 \pm 3.3
\Rightarrow (41.7,\ 48.3)
$$

---

### **3. Finding Confidence Intervals From Large Samples**

When the sample size $`n \geq 30`$, the **Central Limit Theorem** ensures that the sampling distribution of the sample mean is approximately normal, **regardless of population shape**.
Even though the population variance is unknown, we **still use the t-distribution**, but it **closely resembles** the normal distribution.

#### **Example:**

A sample of $`n = 60`$ gives:

* $`\bar{x} = 102`$, $`s = 15`$

At 90% confidence: $`t_{0.05,\,59} \approx 1.671`$

$$
\text{CI} = 102 \pm 1.671 \cdot \frac{15}{\sqrt{60}} \approx 102 \pm 3.24 \Rightarrow (98.76,\ 105.24)
$$

---

### **4. Finding Confidence Intervals: Applications**

#### **a. Scientific Research**

Estimate mean drug effectiveness from trial data, accounting for patient-to-patient variability.

#### **b. Manufacturing**

Determine average machine output (e.g., bolt length), with variability from sample batches.

#### **c. Education**

Estimate average test scores or GPA of a population based on a sample.

#### **d. Environmental Monitoring**

Estimate the mean pollutant level in a river or atmosphere using periodic measurements.

---

### **5. Summary Table**

| Element                       | Description                                         |
|-------------------------------| --------------------------------------------------- |
| $`\bar{x}`$                   | Sample mean                                         |
| $s$                           | Sample standard deviation                           |
| $`t_{\alpha/2,\,n-1}`$        | t-critical value with $`n-1`$ degrees of freedom      |
| Confidence Interval Formula   | $`\bar{x} \pm t_{\alpha/2} \cdot \frac{s}{\sqrt{n}}`$ |
| Assumptions                   | Sample from a normal population or large $n$        |

---

### ✅ Final Notes

* Use **t-distribution** when $`\sigma`$ is unknown.
* For small samples: normality of the population is **essential**.
* For large samples: the **CLT** makes the t-method robust.
* Degrees of freedom $df = n - 1$ **matters** for precision.

This method is foundational for inferential statistics, used across disciplines to draw conclusions from limited, noisy data.
