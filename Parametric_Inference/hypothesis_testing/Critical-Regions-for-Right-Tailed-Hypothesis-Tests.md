## **Critical Regions for Right-Tailed Hypothesis Tests**

---

### **1. Hypothesis Testing Overview**

In hypothesis testing, we assess:

* **Null hypothesis**: $`H_0`$ (e.g., population mean is $`\mu_0`$)
* **Alternative hypothesis**: $`H_1`$ (e.g., mean is **greater** than $`\mu_0`$)

A **right-tailed test** is used when we're testing for values significantly **greater** than expected under $H_0$:

$$
H_0: \theta = \theta_0 \quad \text{vs} \quad H_1: \theta > \theta_0
$$

We define a **critical region** (or rejection region) in the **right tail** of the sampling distribution.

---

### **2. Critical Region and Critical Value**

* The **critical region** is the set of test statistic values that lead to rejection of $H_0$.
* The **critical value** is the threshold value that separates the **non-rejection region** from the **rejection region**.

In a **right-tailed test**, the critical region is:

$$
\text{Critical region} = \{ x : x > c \}
$$

where $c$ is the **critical value** satisfying:

$$
P(X > c \mid H_0 \text{ true}) = \alpha
$$

with $`\alpha`$ being the **significance level** (e.g., 0.05).

---

### **3. Identifying Critical Regions Using CDFs (Continuous Case)**

For a continuous test statistic $`X \sim F`$, the **critical value $c$** satisfies:

$$
P(X > c) = \alpha \quad \Rightarrow \quad P(X \leq c) = 1 - \alpha
$$

Use the **cumulative distribution function (CDF)**:

$$
F(c) = 1 - \alpha \quad \Rightarrow \quad c = F^{-1}(1 - \alpha)
$$

#### Example:

Let $`X \sim \mathcal{N}(0, 1)`$, $`\alpha = 0.05`$:

$$
c = \Phi^{-1}(1 - 0.05) = \Phi^{-1}(0.95) \approx 1.645
$$

Critical region: $`\{ X > 1.645 \}`$

---

### **4. Identifying Critical Regions Using PMFs (Discrete Case)**

For a **discrete** test statistic $X$, the critical region may need adjustment to ensure:

$$
P(X \in R \mid H_0) \leq \alpha
$$

Use the **probability mass function (PMF)** to find the smallest $c$ such that:

$$
P(X \geq c) \leq \alpha
$$

#### Example:

Let $`X \sim \text{Binomial}(n = 10, p = 0.5)`$, $`\alpha = 0.05`$

Compute:

$$
P(X \geq 9) = P(X = 9) + P(X = 10) = \binom{10}{9}(0.5)^{9}(0.5)^1 + \binom{10}{10}(0.5)^{10} = 0.0107 + 0.00098 = 0.01168
$$

Still too small. Try $`X \geq 8`$:

$$
P(X \geq 8) = P(8) + P(9) + P(10) = 0.0439 + 0.0107 + 0.00098 = 0.0556 > 0.05
$$

→ Use $`X \geq 9`$ as the critical region to ensure $`\leq \alpha`$

---

### **5. Identifying Critical Values (Summary)**

| Distribution                    | Critical Value $c$ for Right Tail                      |
|---------------------------------|--------------------------------------------------------|
| Normal $`\mathcal{N}(0,1)`$     | $`\Phi^{-1}(1 - \alpha)`$                              |
| t‑distribution (df = $`n-1`$)   | $`t_{1 - \alpha, n-1}`$                                |
| Chi-square $`\chi^2_k`$         | $`\chi^2_{1 - \alpha, k}`$                             |
| F-distribution $`F_{d_1, d_2}`$ | $`F_{1 - \alpha; d_1, d_2}`$                           |
| Binomial / Poisson              | Find smallest $c$ such that $`P(X \geq c) \leq \alpha`$ |

---

### **6. Visual Summary**

```
  |
  |                     /\
  |                    /  \      ← right tail (critical region)
  |                   /    \      P(X > c) = α
  |------------------|-----|------------------> X
                   μ      c
```

---

### **7. Example in Context: Drug Efficacy**

A drug is effective if mean blood pressure reduction exceeds 10 mmHg. Under $H_0$: $`\mu = 10`$, under $`H_1`$: $`\mu > 10`$. Let:

* $`\overline{X} \sim \mathcal{N}(10, 4/25)`$
* $`\alpha = 0.05`$

Critical value:

$$
c = 10 + z_{0.95} \cdot \sqrt{4/25} = 10 + 1.645 \cdot 0.4 = 10.658
$$

Reject $H_0$ if $`\overline{X} > 10.658`$

---

### **8. Key Takeaways**

| Concept            | Right-Tailed Test                                                        |
| ------------------ | ------------------------------------------------------------------------ |
| Direction of test  | Large values → reject $H_0$                                              |
| Critical region    | $`\{ x : x > c \}`$                                                        |
| Critical value $c$ | Chosen so $`P(X > c \mid H_0) = \alpha`$                                   |
| Use CDF            | For continuous variables: $`F(c) = 1 - \alpha`$                            |
| Use PMF            | For discrete variables: find smallest $c$ s.t. $`P(X \geq c) \leq \alpha`$ |

---

This process is foundational to many **parametric hypothesis tests**, including z-tests, t-tests, and binomial proportion tests.
