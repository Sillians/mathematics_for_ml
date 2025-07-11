## **Confidence Intervals for Linear Regression Intercept Parameters**

---

### **1. Overview**

In simple linear regression:

$$
Y = \beta_0 + \beta_1 X + \varepsilon
$$

* $`\beta_0`$: **Intercept**


* $`\beta_1`$: **Slope**


* $`\varepsilon`$: random error, assumed to be normally distributed with mean 0 and variance $`\sigma^2`$


A **confidence interval for the intercept $`\beta_0`$** estimates the range in which the true 
population intercept lies with a certain level of confidence (typically 95%).

---

### **2. Confidence Interval for Intercept**

Given:

* Estimated intercept: $`\hat{\beta}_0`$


* Standard error of intercept: $`SE_{\hat{\beta}_0}`$


* Degrees of freedom: $`n - 2`$


* Critical value from the t-distribution: $`t_{\alpha/2,\, n-2}`$


Then the confidence interval is:

$$
\hat{\beta}_0 \pm t_{\alpha/2,\, n-2} \cdot SE_{\hat{\beta}_0}
$$

---

### **3. How to Compute the Standard Error of the Intercept**

$$
SE_{\hat{\beta}_0} = s \sqrt{ \frac{1}{n} + \frac{\bar{X}^2}{\sum (X_i - \bar{X})^2} }
$$

Where:

* $s^2$: estimator of error variance, $`s^2 = \frac{1}{n-2} \sum (Y_i - \hat{Y}_i)^2`$


* $`\bar{X}`$: sample mean of $X$


* $n$: number of data points

---

### **4. Example: Finding Confidence Intervals for Intercept Parameters**

#### **Given:**

* Regression equation: $`\hat{Y} = 2.5 + 0.7X`$


* $`SE_{\hat{\beta}_0} = 0.4`$


* $`n = 30`$


* 95% confidence level → $`\alpha = 0.05`$, $`df = 28`$


* From the t-table: $`t_{0.025, 28} \approx 2.048`$


#### **Then:**

$$
CI = 2.5 \pm 2.048 \cdot 0.4 = 2.5 \pm 0.8192
\Rightarrow (1.6808,\ 3.3192)
$$

> Interpretation: We are 95% confident that the true intercept $\beta_0$ lies between 1.68 and 3.32.

---

### **5. Confidence Intervals in Context**

Suppose we’re predicting the starting salary $Y$ (in thousands of dollars) based on years of education $X$. 
The model:

$$
\hat{Y} = 20 + 4X
$$

If the 95% confidence interval for the intercept is $`(17.8,\ 22.2)`$, then:

* **Interpretation**: For someone with 0 years of education (theoretically), their expected starting salary lies between \$17,800 and \$22,200 with 95% confidence.


* **Caution**: This interpretation is only valid **if 0 years of education is within the scope of the data**. Otherwise, it may not be meaningful.

---

### **6. Summary Table**

| Term                    | Meaning                                         |
|-------------------------|-------------------------------------------------|
| $`\hat{\beta}_0`$       | Estimated intercept                             |
| $`SE_{\hat{\beta}_0}`$  | Standard error of the intercept                 |
| $`t_{\alpha/2, n-2}`$   | t-critical value for CI                         |
| CI Formula              | $`\hat{\beta}_0 \pm t \cdot SE_{\hat{\beta}_0}`$ |

---

### **7. Applications**

| Area            | Use                                    |
| --------------- | -------------------------------------- |
| **Economics**   | Predicting baseline consumption/income |
| **Education**   | Estimating default test scores         |
| **Healthcare**  | Predicting baseline risk               |
| **Engineering** | Estimating initial system performance  |

---

