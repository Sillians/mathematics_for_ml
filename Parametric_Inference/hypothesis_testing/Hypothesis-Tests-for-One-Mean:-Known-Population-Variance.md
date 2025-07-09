## **Hypothesis Tests for One Mean: Known Population Variance**

---

### **1. Overview: Hypothesis Testing for the Mean with Known Variance**

When the population standard deviation $`\sigma`$ is **known** and the population is **normally distributed** 
or the sample size is large, we use a **z-test** to test hypotheses about the population mean $`\mu`$.

#### **General Setup**

* **Null Hypothesis**: $`H_0: \mu = \mu_0`$
* **Alternative Hypothesis**:

  * One-tailed (right): $`H_1: \mu > \mu_0`$
  * One-tailed (left): $`H_1: \mu < \mu_0`$
  * Two-tailed: $`H_1: \mu \neq \mu_0`$

#### **Test Statistic**:

$$
z = \frac{\bar{x} - \mu_0}{\sigma / \sqrt{n}}
$$

Where:

* $`\bar{x}`$: sample mean


* $`\mu_0`$: hypothesized population mean


* $`\sigma`$: population standard deviation


* $n$: sample size

We compare the test statistic to the standard normal distribution $`\mathcal{N}(0,1)`$.

---

### **2. Testing a Hypothesis Given a Normal Population: One-Tailed Tests**

#### **Example (Right-Tailed Test)**:

A manufacturer claims that their energy drink increases alertness by **at least 80 minutes**. You suspect it might be **greater**. Population standard deviation is known to be $\sigma = 10$, and data from a **random sample of 25** shows a sample mean of $\bar{x} = 84$.

* $`H_0: \mu = 80`$


* $`H_1: \mu > 80`$ (right-tailed)


* $`\alpha = 0.05`$


* $`z = \frac{84 - 80}{10 / \sqrt{25}} = \frac{4}{2} = 2.0`$


**Critical value** from standard normal table: $`z_{0.05} = 1.645`$

Since $`z = 2.0 > 1.645`$, **reject $`H_0`$**

#### ✅ Conclusion: There is evidence at the 5% level that the mean alertness boost is **greater** than 80 minutes.

---

### **3. Testing a Hypothesis Given a Normal Population: Two-Tailed Tests**

#### **Example (Two-Tailed Test)**:

A tire company claims that their tires last **30,000 miles** on average. A skeptical consumer group tests 
40 tires and finds an average lifespan of $`\bar{x} = 29,200`$ miles. Assume $`\sigma = 2,000`$. 
Is this significantly different at $`\alpha = 0.01`$?

* $`H_0: \mu = 30,000`$


* $`H_1: \mu \neq 30,000`$ (two-tailed)


* $`z = \frac{29,200 - 30,000}{2000 / \sqrt{40}} = \frac{-800}{316.2} \approx -2.53`$

**Critical values**: $`\pm z_{0.005} = \pm 2.576`$

Since $`-2.53 > -2.576`$, **fail to reject $H_0$**

#### ✅ Conclusion: There is **not enough evidence** at the 1% level to conclude the tires last a different amount than claimed.

---

### **4. Testing a Hypothesis for a Large Sample (Central Limit Theorem)**

Even if the population is not normally distributed, the **Central Limit Theorem** allows hypothesis testing 
using the z-test when $`n \geq 30`$.

#### **Example (Large Sample)**:

A food inspector believes the average sodium content in canned soup is **more than** 500 mg. 
A random sample of 50 cans has mean sodium 510 mg. Assume $`\sigma = 15`$.

* $`H_0: \mu = 500`$, $`H_1: \mu > 500`$


* $`z = \frac{510 - 500}{15 / \sqrt{50}} = \frac{10}{2.12} \approx 4.72`$

Critical value at $`\alpha = 0.01`$: $`z_{0.01} = 2.33`$

Since $`4.72 > 2.33`$, **reject $H_0$**

#### ✅ Conclusion: Sodium content **significantly exceeds** 500 mg on average.

---

### **5. Applications of Hypothesis Testing**

| Field               | Example                                                                                 |
| ------------------- | --------------------------------------------------------------------------------------- |
| **Medicine**        | Testing if a new drug lowers blood pressure more than an old one (mean difference test) |
| **Manufacturing**   | Verifying machine calibration by checking if output matches target dimensions           |
| **Finance**         | Testing if average returns of a portfolio exceed a benchmark                            |
| **Marketing**       | Determining if a new campaign changes average sales                                     |
| **Quality Control** | Confirming if a production process meets specifications using sample means              |

Hypothesis testing is used **whenever decisions must be made under uncertainty**, using sample data to infer population behavior.

---

### **Summary Table**

| Component      | Description                                                      |
| -------------- | ---------------------------------------------------------------- |
| Known Variance | Use **z-test** if $`\sigma`$ is known                              |
| One-Tailed     | Directional claim (greater than or less than)                    |
| Two-Tailed     | Nondirectional (not equal)                                       |
| Large Sample   | Use z-test by CLT if $`n \geq 30`$ even if population isn’t normal |
| Test Statistic | $`z = \frac{\bar{x} - \mu_0}{\sigma / \sqrt{n}}`$                  |
| Decision Rule  | Compare $z$ to critical value from standard normal distribution  |
| Application    | Decision-making in business, science, tech, etc.                 |

---
