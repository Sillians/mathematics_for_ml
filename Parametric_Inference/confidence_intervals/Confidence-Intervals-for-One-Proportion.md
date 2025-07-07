## **Confidence Intervals for One Proportion**

---

### **1. Overview**

When estimating an unknown **population proportion** $p$, a **confidence interval** gives a range of 
plausible values for $p$, based on the sample proportion $`\hat{p}`$. 
The construction of this interval depends on the assumption that the sampling distribution 
of $`\hat{p}`$ is approximately normal (justified by the Central Limit Theorem).

---

### **2. Conditions for Validity**

Before constructing a confidence interval for a proportion, ensure:

* The sample is **random** and **independent**.
* The sample size is large enough such that:

  $$
  n\hat{p} \geq 10 \quad \text{and} \quad n(1 - \hat{p}) \geq 10
  $$

---

### **3. Formula for the Confidence Interval**

For a sample of size $n$ with sample proportion $`\hat{p}`$, the **(1−α)% confidence interval** is:

$$
\hat{p} \pm z_{\alpha/2} \cdot \sqrt{\frac{\hat{p}(1 - \hat{p})}{n}}
$$

Where:

* $`\hat{p} = \frac{x}{n}`$: sample proportion
* $`z_{\alpha/2}`$: critical value from standard normal distribution

---

### **4. Finding Confidence Intervals for Population Proportions**

#### **Example:**

Suppose a survey finds that **120 out of 200** people prefer a new product. 
Construct a 95% confidence interval for the true population proportion.

**Step 1: Compute $`\hat{p}`$**

$$
\hat{p} = \frac{120}{200} = 0.60
$$

**Step 2: Compute Standard Error**

$$
SE = \sqrt{\frac{0.6(1 - 0.6)}{200}} = \sqrt{\frac{0.24}{200}} \approx 0.0346
$$

**Step 3: Determine z-value for 95% confidence**

$$
z_{0.025} = 1.96
$$

**Step 4: Construct Interval**

$$
0.6 \pm 1.96 \cdot 0.0346 = 0.6 \pm 0.0678
\Rightarrow (0.5322,\ 0.6678)
$$

**Interpretation**: We are 95% confident that between 53.2% and 66.8% of the population prefer the product.

---

### **5. Finding Confidence Intervals for Population Proportions in Context**

#### **a. Elections**

A poll finds 48% of voters support Candidate A from a sample of 1,000. A 99% confidence interval is constructed to determine if Candidate A is statistically favored.

#### **b. Health Studies**

In a vaccine trial, 95 out of 100 people showed immunity. A 90% CI on the population proportion helps assess overall effectiveness.

#### **c. Quality Control**

A factory finds that 4 out of 200 parts are defective. A CI helps determine the true defect rate and guides quality assurance thresholds.

---

### **6. Summary Table**

| Component           | Description                                      |
|---------------------|--------------------------------------------------|
| $`\hat{p}`$         | Sample proportion                                |
| $`z_{\alpha/2}`$    | z-score corresponding to the confidence level    |
| SE                  | $`\sqrt{\frac{\hat{p}(1 - \hat{p})}{n}}`$        |
| Confidence Interval | $`\hat{p} \pm z_{\alpha/2} \cdot SE`$            |
| Validity Check      | $`n\hat{p} \geq 10`$ and $`n(1-\hat{p}) \geq 10`$ |

---

### **Conclusion**

Confidence intervals for one proportion provide a statistically sound method for estimating population 
proportions from sample data, provided the sample size is large enough. They are widely applicable in polling,
manufacturing, public health, and social science.
