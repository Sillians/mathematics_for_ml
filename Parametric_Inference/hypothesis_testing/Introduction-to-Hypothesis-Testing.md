## **Introduction to Hypothesis Testing**

---

### **1. What is Hypothesis Testing?**

Hypothesis testing is a formal statistical method for making inferences or decisions about population parameters 
using sample data. It involves:

* **Proposing hypotheses** about a population.
* **Collecting and analyzing data**.
* **Making a decision** based on the results.

The goal is to test a **claim** or **assumption** (often called a *hypothesis*) about a population parameter (e.g., mean, proportion, variance).

---

### **2. Identifying Null and Alternative Hypothesis**

There are always two competing hypotheses:

* **Null Hypothesis** $`H_0`$: The default or original claim, usually indicating **no effect**, **no difference**, or **status quo**.
* **Alternative Hypothesis** $`H_1`$ or $`H_a`$: The rival claim, representing a **new effect**, **difference**, or **change**.

**Examples:**

* Testing a mean:

* $`H_0: \mu = 10`$
* $`H_a: \mu \ne 10`$ (two-tailed)
* $`H_a: \mu > 10`$ (right-tailed)
* $`H_a: \mu < 10`$ (left-tailed)

The **form of $H_a$** determines the direction of the test.

---

### **3. Identifying the Significance Level and Test Statistic**

#### **Significance Level $`\alpha`$**

* The probability of rejecting $`H_0`$ when it is actually true (**Type I error**).
* Common choices: 0.05, 0.01, 0.10.

#### **Test Statistic**

A quantity calculated from the sample that summarizes how far the sample result is from what is expected under $`H_0`$.

Examples:

* **Z-test (known population variance):**

$$
z = \frac{\bar{x} - \mu_0}{\sigma / \sqrt{n}}
$$

* **t-test (unknown population variance):**

$$
t = \frac{\bar{x} - \mu_0}{s / \sqrt{n}}, \quad \text{df} = n - 1
$$

The test statistic is compared to **critical values** or used to compute a **p-value**.

---

### **4. Conducting Left-Tailed Tests**

Use when the **alternative hypothesis** is:

$$
H_a: \mu < \mu_0
$$

#### **Steps**:

1. State $`H_0`$ and $`H_a`$.
2. Choose $`\alpha`$ (e.g., 0.05).
3. Compute the test statistic (z or t).
4. Find the **critical value** $`z_\alpha`$ or $`t_\alpha`$.
5. **Decision Rule**: Reject $`H_0`$ if:

$$
\text{test statistic} < -z_\alpha \quad \text{(or } -t_\alpha \text{)}
$$

Or compare **p-value** to $\alpha$:

* Reject $`H_0`$ if $`\text{p-value} < \alpha`$

---

### **5. Conducting Right-Tailed Tests**

Use when the **alternative hypothesis** is:

$$
H_a: \mu > \mu_0
$$

#### **Steps**:

1. State $`H_0`$ and $`H_a`$.
2. Choose $`\alpha`$.
3. Compute the test statistic.
4. Find the **critical value** $`z_\alpha`$ or $`t_\alpha`$.
5. **Decision Rule**: Reject $`H_0`$ if:

$$
\text{test statistic} > z_\alpha \quad \text{(or } t_\alpha \text{)}
$$

Or using the p-value:

* Reject $`H_0`$ if $`\text{p-value} < \alpha`$

---

### **6. Summary Table**

| **Component**               | **Description**                                                 |
| --------------------------- | --------------------------------------------------------------- |
| Null Hypothesis $`H_0`$       | Default assumption (e.g., $`\mu = 0`$)                            |
| Alt. Hypothesis $`H_a`$       | Claim to be tested (e.g., $`\mu \ne 0`$, $`\mu > 0`$, or $`\mu < 0`$) |
| Significance Level $`\alpha`$ | Probability threshold for rejecting $`H_0`$                       |
| Test Statistic              | Z or t score, measures distance from hypothesized mean          |
| Critical Region             | Region of rejection determined by $`\alpha`$ and type of test     |
| p-value                     | Probability of observing result as extreme under $`H_0`$          |

---

### **Key Notes**

* Always define hypotheses **before** seeing the data.
* Ensure correct **direction of test** matches the research question.
* Use **left-tailed** for "less than", **right-tailed** for "greater than", and **two-tailed** for "not equal to".
* A small $`\alpha`$ reduces the chance of a **Type I error** but increases the chance of a **Type II error** (failing to reject a false $H_0$).

Hypothesis testing provides a **framework** for statistical decision-making and is foundational in inferential statistics.
