## **Point Estimates of Population Proportions**

### **1. Introduction to Point Estimation for Proportions**

In statistics, a **point estimate** for a population proportion $p$ is calculated using sample data. 
If we take a random sample of size $n$ from a population and observe $X$ "successes," the **sample proportion**:

$$
\hat{p} = \frac{X}{n}
$$

serves as a **point estimate** of the unknown **population proportion** $p$. This estimate is the **most likely value** of $p$ based on the observed sample.

---

### **2. Properties of the Point Estimator $`\hat{p}`$**

If sampling is random and independent:

* **Expected value**:

  $$
  \mathbb{E}[\hat{p}] = p
  $$


* **Standard deviation (standard error)**:

  $$
  \text{SE}(\hat{p}) = \sqrt{ \frac{p(1 - p)}{n} }
  $$


* $\hat{p}$ is **unbiased** and **consistent**.

---

### **3. Identifying Situations When the CLT for Proportions is Appropriate**

The **Central Limit Theorem (CLT)** can be used to approximate the sampling distribution of $`\hat{p}`$ by a **normal distribution** when the following **conditions** are met:

$$
n p \geq 10 \quad \text{and} \quad n(1 - p) \geq 10
$$

Since $p$ is usually unknown, we substitute $`\hat{p}`$ to verify:

$$
n \hat{p} \geq 10 \quad \text{and} \quad n(1 - \hat{p}) \geq 10
$$

When these conditions hold:

$$
\hat{p} \sim \mathcal{N} \left( p,\; \sqrt{ \frac{p(1 - p)}{n} } \right)
$$

---

### **4. Finding an Approximate Probability Using the CLT for Proportions**

If the sample size is large enough for CLT to apply, we can **approximate probabilities** about $`\hat{p}`$ using the normal distribution.

#### **Steps**:

1. Identify $p$, $n$, and target range for $`\hat{p}`$


2. Compute the standard error:

   $$
   \text{SE} = \sqrt{ \frac{p(1 - p)}{n} }
   $$


3. Use the normal approximation:

   $$
   P\left(a \leq \hat{p} \leq b\right) \approx P\left(\frac{a - p}{\text{SE}} \leq Z \leq \frac{b - p}{\text{SE}} \right)
   $$

   where $`Z \sim \mathcal{N}(0, 1)`$

---

### **5. Example: Approximate Probability**

> Suppose 55% of a population supports a policy. What is the probability that in a sample of 200 people, the sample proportion is between 0.50 and 0.60?

* $`p = 0.55`$, $`n = 200`$


* $`\text{SE} = \sqrt{ \frac{0.55 \cdot 0.45}{200} } \approx 0.0351`$


* $`P(0.50 \leq \hat{p} \leq 0.60) = P\left( \frac{0.50 - 0.55}{0.0351} \leq Z \leq \frac{0.60 - 0.55}{0.0351} \right)`$


* $`= P(-1.42 \leq Z \leq 1.42) \approx 0.844`$

---

### **6. Finding an Approximate Probability Using the CLT for Proportions: Applications**

| **Field**           | **Application**                                       | **Interpretation**                                                    |
| ------------------- | ----------------------------------------------------- | --------------------------------------------------------------------- |
| **Public Policy**   | Estimating support for a new law from a random sample | CI and probability estimates inform public opinion reports            |
| **Elections**       | Forecasting voting outcomes using polls               | Determines likelihood of observed support exceeding threshold         |
| **Healthcare**      | Estimating vaccination coverage from sampled patients | Assess probability that coverage meets herd immunity requirements     |
| **Quality Control** | Estimating defect rate in a factory sample            | Find the probability that observed defect rate exceeds quality limits |
| **Marketing**       | Estimating click-through rate in ad campaigns         | Model likelihood that sample `CTR` falls within or above expectations   |

---

### **7. Summary**

| Concept                          | Formula                                         |
| -------------------------------- |-------------------------------------------------|
| **Point estimate of proportion** | $`\hat{p} = \frac{X}{n}`$                       |
| **Standard error**               | $`\sqrt{ \frac{p(1 - p)}{n} }`$                 |
| **Normal approximation (CLT)**   | $`\hat{p} \approx \mathcal{N}(p,\; \text{SE})`$ |
| **Conditions for CLT**           | $`np \geq 10,\; n(1 - p) \geq 10`$              |

---

This framework allows approximate inference for proportions using familiar normal probability tools, enabling rapid analysis in a wide variety of real-world applications.
