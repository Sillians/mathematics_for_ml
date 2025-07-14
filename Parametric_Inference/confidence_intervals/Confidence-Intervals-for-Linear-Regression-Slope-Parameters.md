## **Confidence Intervals for Linear Regression Slope Parameters**

---

### **1. Overview: Linear Regression and Confidence Intervals**

In simple linear regression, we model the relationship between a response variable $Y$ and a predictor variable $X$ as:

$$
Y_i = \beta_0 + \beta_1 X_i + \varepsilon_i,\quad \varepsilon_i \sim \mathcal{N}(0, \sigma^2)
$$

Here:

* $`\beta_1`$: true slope of the regression line (rate of change of $Y$ with respect to $X$)


* $`\hat{\beta}_1`$: sample estimate of the slope


* A **confidence interval** for $`\beta_1`$ gives a range of plausible values for the slope based on observed data.

---

### **2. Finding Confidence Intervals for Slope Parameters**

#### **Formula**

The **$`(1 - \alpha)\times100\%`$ confidence interval** for the slope parameter $`\beta_1`$ is:

$$
\boxed{
\hat{\beta}_1 \pm t_{n-2,\alpha/2} \cdot \mathrm{SE}(\hat{\beta}_1)
}
$$

Where:

* $`\hat{\beta}_1`$ is the estimated slope


* $`\mathrm{SE}(\hat{\beta}_1) = \dfrac{s}{\sqrt{\sum (x_i - \bar{x})^2}}`$


* $`s^2 = \dfrac{1}{n-2} \sum (y_i - \hat{y}_i)^2`$ is the unbiased estimate of the error variance


* $`t_{n-2,\alpha/2}`$ is the critical value from the t-distribution with $`n - 2`$ degrees of freedom

---

### **3. Finding Confidence Intervals in Context**

#### **Example**

Suppose from a dataset of size $`n = 10`$, the following are computed:

* $`\hat{\beta}_1 = 1.8`$


* $`\sum (x_i - \bar{x})^2 = 20`$


* Residual sum of squares (RSS) = 18

Then:

* $`s^2 = \frac{18}{10 - 2} = 2.25`$


* $`s = \sqrt{2.25} = 1.5`$


* $`\mathrm{SE}(\hat{\beta}_1) = \frac{1.5}{\sqrt{20}} \approx 0.335`$

Using $`t_{8,0.025} \approx 2.306`$, the 95% confidence interval is:

$$
1.8 \pm 2.306 \times 0.335 \quad \Rightarrow \quad (1.027, 2.573)
$$

---

### **4. Deriving an Expression for the Confidence Interval**

The derivation begins by noting:

$$
\hat{\beta}_1 = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sum (x_i - \bar{x})^2}
$$

Since 

$`\hat{\beta}_1 \sim \mathcal{N}(\beta_1, \mathrm{Var}(\hat{\beta}_1))`$ 

and 

$`\mathrm{Var}(\hat{\beta}_1) = \frac{\sigma^2}{\sum (x_i - \bar{x})^2}`$, 


the sample-based estimate replaces $`\sigma^2`$ with $`s^2`$, leading to:


$$
\frac{\hat{\beta}_1 - \beta_1}{\mathrm{SE}(\hat{\beta}_1)} \sim t_{n-2}
$$


Rearranging gives the confidence interval formula:


$`\hat{\beta}_1 \pm t_{n-2,\alpha/2} \cdot \mathrm{SE}(\hat{\beta}_1)`$

---

### **5. Interpretation & Applications**

* **If 0 is not in the interval:** Suggests statistically significant relationship between $X$ and $Y$.


* **Wider intervals** imply less certainty about the slope estimate (possibly due to smaller sample size or high variance).


* **Used in forecasting, diagnostics, and hypothesis testing** in both academic and applied regression settings.

---

### **6. Summary Table**

| Concept           | Formula                                                                              |
| ----------------- | ------------------------------------------------------------------------------------ |
| Slope estimate    | $`\hat{\beta}_1 = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sum (x_i - \bar{x})^2}`$ |
| Residual variance | $`s^2 = \frac{1}{n-2} \sum (y_i - \hat{y}_i)^2`$                                       |
| Standard error    | $`\mathrm{SE}(\hat{\beta}_1) = \frac{s}{\sqrt{\sum (x_i - \bar{x})^2}}`$               |
| CI for slope      | $`\hat{\beta}_1 \pm t_{n-2,\alpha/2} \cdot \mathrm{SE}(\hat{\beta}_1)`$                |

This approach generalizes to multiple regression and enables inference on the strength and direction of linear relationships.
