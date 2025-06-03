## **Variance of Sample Means**

---

### **1. Understanding the Variance of Sample Means**

The **sample mean** is a random variable when sampling from a population, and it has its own **distribution** 
known as the **sampling distribution of the sample mean**.

If:

* The population has a mean $`\mu`$
* The population has variance $`\sigma^2`$
* The sample size is $n$

Then:

* The **mean** of the sampling distribution of the sample mean $`\bar{X}`$ is $`\mu`$
* The **variance** of the sample mean is:

$$
\text{Var}(\bar{X}) = \frac{\sigma^2}{n}
$$

This result follows from the **additivity and scaling rules** of variance for independent random variables.

---

### **2. Finding the Variance of a Sample Mean**

Let $`X_1, X_2, \dots, X_n`$ be a random sample of size $n$ from a population with variance $`\sigma^2$`. The sample mean is:

$$
\bar{X} = \frac{1}{n} \sum_{i=1}^n X_i
$$

Since each $`X_i`$ is independent and identically distributed (i.i.d.), the variance of the sample mean is:

$$
\text{Var}(\bar{X}) = \text{Var} \left( \frac{1}{n} \sum_{i=1}^n X_i \right) = \frac{1}{n^2} \sum_{i=1}^n \text{Var}(X_i) = \frac{1}{n^2} \cdot n \cdot \sigma^2 = \frac{\sigma^2}{n}
$$

---

### **3. Finding the Standard Error**

The **standard error** (SE) of the sample mean is the **standard deviation** of its sampling distribution:

$$
\text{SE}(\bar{X}) = \sqrt{\text{Var}(\bar{X})} = \sqrt{\frac{\sigma^2}{n}} = \frac{\sigma}{\sqrt{n}}
$$

If $`\sigma`$ is unknown, it is estimated using the sample standard deviation $s$:

$$
\text{SE}(\bar{X}) \approx \frac{s}{\sqrt{n}}
$$

This estimation is commonly used in confidence intervals and hypothesis testing.

---

### **4. Calculating an Appropriate Sample Size**

To achieve a desired **margin of error (ME)** at a specific **confidence level**, use the formula derived from the normal approximation:

$$
n = \left( \frac{z_{\alpha/2} \cdot \sigma}{\text{ME}} \right)^2
$$

Where:

* $`z_{\alpha/2}`$ is the z-score corresponding to the confidence level
* $`\sigma`$ is the population standard deviation
* $`\text{ME}`$ is the desired margin of error

If $\sigma$ is unknown, a preliminary estimate $s$ or a prior study estimate is used.

**Example:**
To estimate a population mean within ±2 units with 95% confidence and $`\sigma = 6`$:

$$
n = \left( \frac{1.96 \cdot 6}{2} \right)^2 = \left(5.88\right)^2 \approx 34.6 \Rightarrow n = 35
$$

---

### **5. Summary Table**

| **Quantity**             | **Formula**                                                    | **Description**                |
| ------------------------ | -------------------------------------------------------------- | ------------------------------ |
| Sample mean              | $`\bar{X} = \frac{1}{n} \sum X_i`$                               | Average of sample values       |
| Variance of sample mean  | $`\text{Var}(\bar{X}) = \frac{\sigma^2}{n}`$                     | Dispersion of sample mean      |
| Standard error (SE)      | $`\frac{\sigma}{\sqrt{n}}$ or $\frac{s}{\sqrt{n}}`$              | Spread of sample mean estimate |
| Required sample size $n$ | $`\left( \frac{z_{\alpha/2} \cdot \sigma}{\text{ME}} \right)^2`$ | For specified margin of error  |

---

### **Key Insights**

* **Larger samples** yield **lower variance** and **smaller standard error**, making estimates more precise.
* **Standard error** is critical in constructing **confidence intervals**.
* Knowing or estimating population **standard deviation** is essential when determining sample size.

This foundation supports reliable statistical estimation and hypothesis testing in real-world studies.
