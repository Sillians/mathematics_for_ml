## **Two-Tailed Hypothesis Tests**

---

### **1. Overview of Two-Tailed Tests**

A **two-tailed hypothesis test** checks whether a sample statistic is **significantly different** (either higher or lower) from a hypothesized population value.

This is in contrast to **one-tailed tests**, which only test for directionality (greater than or less than).

---

### **2. Identifying Two-Tailed Alternative Hypotheses**

| **Component**         | **Null Hypothesis**            | **Alternative Hypothesis (Two-Tailed)** |
| --------------------- |--------------------------------| --------------------------------------- |
| Population mean       | $`H_0: \mu = \mu_0`$           | $`H_1: \mu \ne \mu_0`$                    |
| Population proportion | $`H_0: p = p_0`$               | $`H_1: p \ne p_0`$                        |
| Population variance   | $`H_0: \sigma^2 = \sigma_0^2`$ | $`H_1: \sigma^2 \ne \sigma_0^2`$          |

**Key Indicator:**
The alternative hypothesis uses **"≠"**, meaning deviations in **both directions** (above or below) are significant.

---

### **3. Identifying Critical Regions**

For a two-tailed test:

* The **total significance level** $`\alpha`$ is split **equally** between the **two tails** of the distribution.


* Each tail contains $`\alpha/2`$.

#### **Normal distribution (Z-test):**

| **Confidence Level** | **Significance Level (α)** | **Each Tail (α/2)** | **Critical Z-Values** |
| -------------------- | -------------------------- | ------------------- | --------------------- |
| 90%                  | 0.10                       | 0.05                | ±1.645                |
| 95%                  | 0.05                       | 0.025               | ±1.960                |
| 99%                  | 0.01                       | 0.005               | ±2.576                |

#### **Chi-squared, t-distribution, etc.:**

Use **separate tables** and degrees of freedom to find corresponding critical values.

---

### **4. Identifying Critical Values**

**Definition:**
A **critical value** is the cutoff point that separates the **rejection region** from the **non-rejection region**.

For two-tailed tests:

* Lower Critical Value = Quantile at $`\alpha/2`$


* Upper Critical Value = Quantile at $`1 - \alpha/2`$

#### **Example (Z-distribution):**

If $`\alpha = 0.05`$, the critical values are:

* $`z_{\alpha/2} = z_{0.025} = 1.960`$


* Reject $H_0$ if:
                       $|z| > 1.960$

---

### **5. Decision Rule**

| **Test Statistic**               | **Decision**         |
| -------------------------------- | -------------------- |
| Lies **outside** critical values | Reject $`H_0`$         |
| Lies **within** critical values  | Fail to reject $`H_0`$ |

---

### **6. Applications**

| **Scenario**                                                   | **Hypotheses**                                    | **Why Two-Tailed?**                        |
| -------------------------------------------------------------- |---------------------------------------------------| ------------------------------------------ |
| Testing if a new drug has a different effect than the standard | $`H_0: \mu = \mu_0`$, $`H_1: \mu \ne \mu_0`$      | Difference matters in **either direction** |
| Comparing two manufacturing methods                            | $`H_0: \mu_1 = \mu_2`$, $`H_1: \mu_1 \ne \mu_2`$  | Concerned about **any** difference         |
| Checking if average wait time has changed                      | $`H_0: \mu = 5`$, $`H_1: \mu \ne 5`$              | **Any change**, shorter or longer, matters |

---

### **Summary Table**

| **Element**            | **Two-Tailed Test**                                 |
|------------------------| --------------------------------------------------- |
| Alternative Hypothesis | $`H_1: \text{parameter} \ne \text{value}`$            |
| Critical Regions       | Both tails of the distribution                      |
| Significance split     | $`\alpha/2`$ in each tail                             |
| Reject $`H_0`$ when    | Test statistic lies beyond **both** critical values |

---
