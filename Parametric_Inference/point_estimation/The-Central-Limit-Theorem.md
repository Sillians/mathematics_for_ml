## **The Central Limit Theorem (CLT)**

---

### **1. Central Limit Theorem: Statement**

Let $`X_1, X_2, \dots, X_n`$ be **i.i.d.** random variables with:

* Mean: $`\mu = \mathbb{E}[X_i]`$
* Variance: $`\sigma^2 = \text{Var}(X_i) < \infty`$

Define the sample mean:

$$
\overline{X}_n = \frac{1}{n} \sum_{i=1}^n X_i
$$

Then the **Central Limit Theorem** states:

$$
\frac{\overline{X}_n - \mu}{\sigma / \sqrt{n}} \;\xrightarrow{d}\; \mathcal{N}(0, 1) \quad \text{as } n \to \infty
$$

> This means that for **large enough** $n$, $`\overline{X}_n`$ is approximately normal—even if the original distribution of $`X_i`$ is **not normal**.

---

### **2. Why the CLT Matters**

* **Universality**: Works for any distribution (discrete or continuous) with finite mean and variance.
* **Approximation**: Allows normal approximation for sums/averages.
* **Basis for inference**: Used in confidence intervals, hypothesis tests, control charts, etc.

---

### **3. Finding an Approximate Probability Using the CLT**

**Procedure:**

1. Given: i.i.d. variables $`X_i \sim (\mu, \sigma^2)`$, sample size $n$


2. Want: $`P(a < \overline{X}_n < b)`$


3. Standardize:

   $$
   Z = \frac{\overline{X}_n - \mu}{\sigma / \sqrt{n}} \sim \mathcal{N}(0,1) \text{ approximately}
   $$


4. Use standard normal table (or CDF):

   $$
   P(a < \overline{X}_n < b) = P\left( \frac{a - \mu}{\sigma / \sqrt{n}} < Z < \frac{b - \mu}{\sigma / \sqrt{n}} \right)
   $$

---

#### **Example:**

Let $`X_i \sim \text{Exponential}(1)`$, so:

* $`\mu = 1`$, $`\sigma^2 = 1`$
* Let $`n = 30`$, find $`P(0.9 < \overline{X}_{30} < 1.1)`$

Standardize:

$$
Z_1 = \frac{0.9 - 1}{1 / \sqrt{30}} = -\sqrt{30} \cdot 0.1 \approx -0.5477
$$


$$
Z_2 = \frac{1.1 - 1}{1 / \sqrt{30}} = \sqrt{30} \cdot 0.1 \approx 0.5477
$$


Use normal table:


$$
P(-0.5477 < Z < 0.5477) \approx \Phi(0.5477) - \Phi(-0.5477) \approx 0.7088 - 0.2912 = 0.4176
$$

---

### **4. Using the CLT With a Discrete Population Distribution**

The CLT applies even if the underlying variable is **discrete**.

#### **Example:**

Let $`X_i \sim \text{Binomial}(n = 1, p = 0.3)`$, i.e., a **Bernoulli** random variable.

* Mean: $`\mu = 0.3`$


* Variance: $`\sigma^2 = 0.3 \cdot 0.7 = 0.21`$


* For large $n$, $`\overline{X}_n \sim \mathcal{N}(0.3, \frac{0.21}{n})`$

**Approximate probability**:

Find $`P(\overline{X}_{50} > 0.4)`$

Standardize:

$$
Z = \frac{0.4 - 0.3}{\sqrt{0.21/50}} = \frac{0.1}{\sqrt{0.0042}} \approx \frac{0.1}{0.0648} \approx 1.54
$$

$$
P(\overline{X}_{50} > 0.4) \approx P(Z > 1.54) \approx 0.0618
$$

---

### **5. Using the CLT With a Continuous Population Distribution**

If $`X_i \sim`$ continuous (e.g., Uniform, Exponential, Normal), the CLT still applies.

The only requirements:

* i.i.d. (or weakly dependent in extensions)
* Finite mean and variance

#### **Example:**

Let $`X_i \sim \text{Uniform}(2, 6)`$

* $`\mu = \frac{2+6}{2} = 4`$


* $`\sigma^2 = \frac{(6 - 2)^2}{12} = \frac{16}{12} = \frac{4}{3}`$


For $`n = 36`$, find $`P(\overline{X}_{36} < 3.8)`$

Standardize:

$$
Z = \frac{3.8 - 4}{\sqrt{(4/3)/36}} = \frac{-0.2}{\sqrt{1/27}} = -0.2 \cdot \sqrt{27} \approx -1.0392
$$

$$
P(\overline{X}_{36} < 3.8) \approx P(Z < -1.04) \approx 0.1492
$$

---

### **6. Summary Table**

| Population Type                         | Use CLT if…  | Sample Mean Distribution                                  |
| --------------------------------------- | ------------ | --------------------------------------------------------- |
| Discrete (e.g., Bernoulli, Binomial)    | $n$ is large | $`\overline{X}_n \approx \mathcal{N}(\mu, \sigma^2/n)`$     |
| Continuous (e.g., Uniform, Exponential) | $n$ is large | Same                                                      |
| Normal                                  | Any $n$      | Exact: $`\overline{X}_n \sim \mathcal{N}(\mu, \sigma^2/n)`$ |

---

### **7. Key Insights**

* The CLT is **distribution-agnostic**—it doesn't require the population to be normal.


* The **larger** the sample size $n$, the better the normal approximation.


* The CLT is the foundation for:

  * Estimating probabilities for averages/sums
  * Constructing confidence intervals
  * Performing z-tests for population means

---

This theorem is one of the most powerful tools in statistics—it justifies using normal approximations in 
real-world scenarios where the population distribution may be unknown, discrete, or skewed.
