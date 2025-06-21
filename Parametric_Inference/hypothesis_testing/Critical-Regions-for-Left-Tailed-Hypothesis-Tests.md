# **Critical Regions for Left-Tailed Hypothesis Tests**

---

## **1. Overview of Left-Tailed Tests**

A **left-tailed hypothesis test** is used when the alternative hypothesis states that the population parameter is **less than** a specified value:

* Null Hypothesis: $`H_0: \mu = \mu_0`$
* Alternative Hypothesis: $`H_a: \mu < \mu_0`$

The **critical region** (or rejection region) lies in the **left tail** of the sampling distribution.

---

## **2. Identifying Critical Regions Using CDFs**

To determine the critical region using the **Cumulative Distribution Function (CDF)**:

* Choose a significance level $`\alpha`$
* Determine the critical value $`x_c`$ such that:

$$
P(X \leq x_c) = \alpha
$$

This $`x_c`$ is found using the inverse CDF (quantile function) of the distribution.

### **Example (Normal Distribution)**

For $`\alpha = 0.05`$:

$$
P(Z \leq z_c) = 0.05 \Rightarrow z_c \approx -1.645
$$

So, **reject** $`H_0`$ if the standardized test statistic $`z \leq -1.645`$.

---

## **3. Identifying Critical Regions Using PMFs**

When dealing with **discrete distributions**, such as the **Binomial** or **Poisson**, use the **Probability Mass Function (PMF)** and cumulative sums:

* The critical region includes the smallest values of the test statistic such that:

$$
P(X \leq x_c) \leq \alpha
$$

You typically iterate through values of $`X`$ until the cumulative probability crosses $`\alpha`$.

### **Example (Poisson with $`\lambda = 3`$, $`\alpha = 0.05`$)**

Using the CDF:

* $`P(X \leq 0) = e^{-3} \approx 0.0498`$ → Critical value $`x_c = 0`$
* Reject $`H_0`$ if $`X \leq 0`$

---

## **4. Identifying Critical Values**

The **critical value** separates the **non-rejection region** from the **rejection region**.

* For **left-tailed tests**, the critical value $`x_c`$ satisfies:

$$
P(X \leq x_c) = \alpha
$$

* It is found using:

  * **Z-tables** (for standard normal)
  * **T-tables** (for small sample sizes with unknown variance)
  * **Quantile functions** (for Poisson, Binomial, etc.)

### **Key Notes:**

* For **normal** or **t-distributions**, negative values are typical in left-tailed tests.
* The **critical region** is the set of all values **less than or equal to** the critical value.

---

## **Summary Table**

| Distribution Type            | Method                 | Rejection Condition                      |
| ---------------------------- | ---------------------- | ---------------------------------------- |
| Continuous (Normal, t)       | Inverse CDF (quantile) | $`z \leq z_\alpha`$                        |
| Discrete (Poisson, Binomial) | CDF or cumulative PMF  | $`X \leq x_c`$                             |
| General                      | Use tables or software | Compare with significance level $`\alpha`$ |

---

## **Example Wrap-Up**

If:

* $`H_0: \mu = 50`$
* $`H_a: \mu < 50`$
* Sample mean $`\bar{x} = 47.5`$, $`\sigma = 5`$, $`n = 25`$
* Then:

$$
z = \frac{\bar{x} - \mu_0}{\sigma / \sqrt{n}} = \frac{47.5 - 50}{5 / \sqrt{25}} = -2.5
$$

Compare to critical value:

* At $`\alpha = 0.05`$: $`z_c = -1.645`$

Since $`-2.5 < -1.645`$, **reject** $`H_0`$.

---
