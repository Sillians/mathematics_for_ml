## **The Student's t-Distribution**

### **1. What Is the Student’s t-Distribution?**

The **Student's t-distribution** is a family of distributions that arise when estimating 
the **population mean** $\mu$ of a **normally distributed population** in situations where 
the **sample size is small** and the **population standard deviation is unknown**.

It is used in place of the standard normal distribution when replacing the unknown $`\sigma`$ with 
the sample standard deviation $s$, introducing **extra uncertainty** accounted for by the t-distribution’s heavier tails.

---

### **2. Definition**

Let $`X_1, X_2, \dots, X_n`$ be a random sample from a normal distribution with **unknown** mean $`\mu`$ 
and **unknown** standard deviation $`\sigma`$. The **t-statistic** is:

$$
t = \frac{\bar{X} - \mu}{s/\sqrt{n}}
$$

Where:

* $`\bar{X}`$: sample mean


* $s$: sample standard deviation


* $n$: sample size

This follows a **Student’s t-distribution** with $`\nu = n - 1`$ **degrees of freedom (df)**.

---

### **3. Properties of the t-Distribution**

| Property           | Description                                                |
| ------------------ | ---------------------------------------------------------- |
| Symmetry           | Symmetric around 0 (like the standard normal distribution) |
| Shape              | Bell-shaped but with **heavier tails**                     |
| Degrees of Freedom | More degrees of freedom → closer to normal distribution    |
| Limiting Case      | As $`\nu \to \infty`$, $t$-distribution → standard normal    |

---

### **4. Using a Percentage Points Table To Find a t-Score**

A **t-table** (percentage points table) gives the **critical value** $`t_{\alpha,\nu}`$ such that:

$$
P(T > t_{\alpha,\nu}) = \alpha \quad \text{for } T \sim t_{\nu}
$$

#### **Example**:

* Find the t-score for a **95% confidence level** with $`\nu = 10`$ degrees of freedom.


* Since 95% leaves 2.5% in each tail, use $`\alpha = 0.025`$


* Look up $`t_{0.025,10}`$ in the table:

  $$
  t_{0.025,10} \approx 2.228
  $$

This is the value such that:

$$
P(T > 2.228) = 0.025 \quad \text{and} \quad P(-2.228 < T < 2.228) = 0.95
$$

---

### **5. Computing a t-Score Using the Complement**

If the table gives $`t_{\alpha, \nu}`$ such that $`P(T > t_{\alpha, \nu}) = \alpha`$, you can use:

$$
P(T < t_{\alpha, \nu}) = 1 - \alpha
$$

#### **Example**:

To find $t$ such that $`P(T < t) = 0.90`$ with $`\nu = 15`$:

* Use $`\alpha = 0.10`$, so $`P(T > t) = 0.10`$


* Find $`t_{0.10,15} \approx 1.341`$


* Then $`t = t_{0.10,15}`$, and:

  $$
  P(T < 1.341) = 0.90
  $$

---

### **6. Computing a t-Score Using Symmetry**

Because the t-distribution is symmetric:

$$
t_{1 - \alpha, \nu} = -t_{\alpha, \nu}
$$

#### **Example**:

If $`t_{0.025,20} = 2.086`$, then:

$$
t_{0.975,20} = -2.086
$$

This is useful for:

* **Two-tailed tests**, where you split $`\alpha`$ across both tails


* Converting right-tail critical values to left-tail equivalents

---

### **7. Comparison to Standard Normal**

| Feature     | t-Distribution                | Standard Normal           |
| ----------- |-------------------------------|---------------------------|
| Mean        | 0                             | 0                         |
| Shape       | Bell-shaped                   | Bell-shaped               |
| Tails       | Heavier                       | Lighter                   |
| Variability | Depends on $n$                | Fixed                     |
| Use When    | $`\sigma`$ unknown, small $n$ | $`\sigma`$ known, any $n$ |

---

### **8. Summary Table**

| Component          | Formula or Use                                          |
| ------------------ | ------------------------------------------------------- |
| t-statistic        | $`\displaystyle t = \frac{\bar{X} - \mu}{s/\sqrt{n}}`$    |
| Degrees of freedom | $`\nu = n - 1`$                                           |
| Symmetry           | $`t_{\alpha,\nu} = -t_{1-\alpha,\nu}`$                    |
| Table usage        | $`P(T > t_{\alpha,\nu}) = \alpha`$                        |
| CI endpoints       | $`\bar{X} \pm t_{\alpha/2,\nu} \cdot \frac{s}{\sqrt{n}}`$ |

---

The t-distribution is essential for **inference about a mean** when variability is estimated from the data. 
It's most powerful in small-sample contexts and remains widely used in confidence intervals and hypothesis testing.
