# **Hypothesis Tests for the Rate of a Poisson Distribution**

---

## **1. Overview**

The **Poisson distribution** is used to model the number of events occurring in a fixed interval of time or space when those events occur **independently**
and at a **constant average rate** $`\lambda`$.

The hypothesis test determines whether the **observed event count** is consistent with a claimed Poisson rate.

---

## **2. Poisson Distribution Recap**

A random variable $`X`$ follows a Poisson distribution with rate $`\lambda`$ if:

$$
P(X = k) = \frac{e^{-\lambda} \lambda^k}{k!}, \quad k = 0, 1, 2, \dots
$$

Where:

* $`\lambda > 0`$ is the **mean number of occurrences** in the interval.

---

## **3. Setting Up a Hypothesis Test**

We are testing:

* **Null Hypothesis**: $`H_0: \lambda = \lambda_0`$
* **Alternative Hypothesis**:

  * Left-tailed: $`H_1: \lambda < \lambda_0`$
  * Right-tailed: $`H_1: \lambda > \lambda_0`$
  * Two-tailed: $`H_1: \lambda \ne \lambda_0`$

Let:

* $`X`$ be the **observed number of events**
* $`\alpha`$ be the **significance level** (e.g., 0.05)

Under $`H_0`$, $`X \sim \text{Poisson}(\lambda_0)`$

---

## **4. Test Statistic**

Since $`X`$ is discrete, we compute the **exact probability** under the null hypothesis.

---

## **5. Conducting a Left-Tailed Test**

### **Hypotheses**:

$$
H_0: \lambda = \lambda_0 \quad \text{vs.} \quad H_1: \lambda < \lambda_0
$$

### **Steps**:

1. Compute:

$$
p\text{-value} = P(X \le x_{\text{obs}} \mid \lambda = \lambda_0) = \sum_{k=0}^{x_{\text{obs}}} \frac{e^{-\lambda_0} \lambda_0^k}{k!}
$$

2. Compare to significance level:

* Reject $`H_0`$ if $`p\text{-value} < \alpha`$

---

## **6. Conducting a Right-Tailed Test**

### **Hypotheses**:

$$
H_0: \lambda = \lambda_0 \quad \text{vs.} \quad H_1: \lambda > \lambda_0
$$

### **Steps**:

1. Compute:

$$
p\text{-value} = P(X \ge x_{\text{obs}} \mid \lambda = \lambda_0) = 1 - \sum_{k=0}^{x_{\text{obs}} - 1} \frac{e^{-\lambda_0} \lambda_0^k}{k!}
$$

2. Compare to $\alpha$:

* Reject $`H_0`$ if $`p\text{-value} < \alpha`$

---

## **7. Two-Tailed Test (Optional)**

### **Hypotheses**:

$$
H_0: \lambda = \lambda_0 \quad \text{vs.} \quad H_1: \lambda \ne \lambda_0
$$

* Requires computing the **two-tailed** p-value:

$$
p\text{-value} = 2 \cdot \min \left( P(X \le x_{\text{obs}}),\ P(X \ge x_{\text{obs}}) \right)
$$

* Reject $`H_0`$ if $`p\text{-value} < \alpha`$

---

## **8. Example (Right-Tailed)**

Suppose:

* $`X = 12`$ observed events
* Claimed $`\lambda_0 = 8`$
* Significance level $`\alpha = 0.05`$

Compute:

$$
p\text{-value} = P(X \ge 12 \mid \lambda = 8)
= 1 - P(X \le 11 \mid \lambda = 8)
$$

Use tables/software to compute:

* If $`p\text{-value} = 0.045 < 0.05`$ → Reject $`H_0`$
* Conclude: Evidence suggests $`\lambda > 8`$

---

##  Summary Table

| Test Type    | Null Hypothesis       | Alternative Hypothesis  | p-value Expression                                          | Reject if    |
| ------------ | --------------------- | ----------------------- | ----------------------------------------------------------- | ------------ |
| Left-tailed  | $`\lambda = \lambda_0`$ | $`\lambda < \lambda_0`$   | $`P(X \le x_{\text{obs}})`$                                   | $`p < \alpha`$ |
| Right-tailed | $`\lambda = \lambda_0`$ | $`\lambda > \lambda_0`$   | $`P(X \ge x_{\text{obs}}) = 1 - P(X \le x_{\text{obs}} - 1)`$ | $`p < \alpha`$ |
| Two-tailed   | $`\lambda = \lambda_0`$ | $`\lambda \ne \lambda_0`$ | $`2 \cdot \min(P(X \le x), P(X \ge x))`$                      | $`p < \alpha`$ |

---
