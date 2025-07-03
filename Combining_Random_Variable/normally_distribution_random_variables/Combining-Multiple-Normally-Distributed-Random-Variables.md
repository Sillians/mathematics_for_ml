## **Combining Multiple Normally Distributed Random Variables**

---

### **1. Overview**

If $`X_1, X_2, \dots, X_n`$ are **jointly normally distributed** random variables, then any **linear combination** of them is also normally distributed.

Let:

$$
Z = a_1 X_1 + a_2 X_2 + \dots + a_n X_n = \sum_{i=1}^{n} a_i X_i
$$

Then:

$$
Z \sim \mathcal{N}\left(\sum_{i=1}^n a_i \mu_i,\; \sum_{i=1}^n a_i^2 \sigma_i^2 + \sum_{i \ne j} a_i a_j \,\text{Cov}(X_i, X_j)\right)
$$


If the variables are **independent**, then $`\text{Cov}(X_i, X_j) = 0`$ for $`i \ne j`$, and the variance simplifies to:


$$
\text{Var}(Z) = \sum_{i=1}^{n} a_i^2 \sigma_i^2
$$

---

### **2. Distribution of a Sum of Normal Random Variables**

If $`X_i \sim \mathcal{N}(\mu_i, \sigma_i^2)`$ and they are **independent**, then the sum


$$
S_n = X_1 + X_2 + \dots + X_n
$$


has the distribution:


$$
S_n \sim \mathcal{N}\left(\sum_{i=1}^n \mu_i,\; \sum_{i=1}^n \sigma_i^2\right)
$$

---

### **3. Distribution of a Linear Combination of Normals**

Let:

$$
Z = a_1 X_1 + a_2 X_2 + \dots + a_n X_n
$$

Then:

$$
Z \sim \mathcal{N}\left(\sum_{i=1}^n a_i \mu_i,\; \sum_{i=1}^n a_i^2 \sigma_i^2 + \sum_{i \ne j} a_i a_j \,\text{Cov}(X_i, X_j)\right)
$$

If **independent**, then only diagonal terms contribute:

$$
Z \sim \mathcal{N}\left(\sum_{i=1}^n a_i \mu_i,\; \sum_{i=1}^n a_i^2 \sigma_i^2\right)
$$

#### **Example**

Let:

* $`X_1 \sim \mathcal{N}(2, 1)`$, $`X_2 \sim \mathcal{N}(5, 4)`$, $`X_3 \sim \mathcal{N}(1, 9)`$, all independent.

Find the distribution of:

$$
Z = 3X_1 - 2X_2 + 0.5X_3
$$

**Mean**:

$$
\mu_Z = 3(2) - 2(5) + 0.5(1) = 6 - 10 + 0.5 = -3.5
$$

**Variance**:

$$
\sigma_Z^2 = 3^2(1) + (-2)^2(4) + (0.5)^2(9) = 9 + 16 + 2.25 = 27.25
$$

So:

$$
Z \sim \mathcal{N}(-3.5, 27.25)
$$

---

### **4. Calculating Probabilities Involving Linear Combinations**

To compute $`\mathbb{P}(Z \le z_0)`$, standardize:

$$
Z^* = \frac{z_0 - \mu_Z}{\sigma_Z}
$$

Then use standard normal distribution tables or software:

$$
\mathbb{P}(Z \le z_0) = \Phi\left(\frac{z_0 - \mu_Z}{\sigma_Z}\right)
$$

#### **Example**

Using previous result: $`Z \sim \mathcal{N}(-3.5, 27.25)`$

Find $`\mathbb{P}(Z \le 0)`$:


$$
Z^* = \frac{0 - (-3.5)}{\sqrt{27.25}} \approx \frac{3.5}{5.22} \approx 0.67
\Rightarrow \mathbb{P}(Z \le 0) \approx \Phi(0.67) \approx 0.7486
$$

---

### **5. Contextual Example: Portfolio Returns**

Let:

* Asset A: $`R_A \sim \mathcal{N}(0.06, 0.02^2)`$
* Asset B: $`R_B \sim \mathcal{N}(0.08, 0.03^2)`$
* Asset C: $`R_C \sim \mathcal{N}(0.05, 0.01^2)`$

Weights: $`w_A = 0.5,\; w_B = 0.3,\; w_C = 0.2`$, independent returns.

Then portfolio return:

$$
R_P = 0.5R_A + 0.3R_B + 0.2R_C
$$

**Expected return**:

$$
\mu_P = 0.5(0.06) + 0.3(0.08) + 0.2(0.05) = 0.030 + 0.024 + 0.010 = 0.064
$$

**Variance**:

$$
\sigma_P^2 = 0.5^2(0.02)^2 + 0.3^2(0.03)^2 + 0.2^2(0.01)^2 = 0.0001 + 0.000081 + 0.000004 = 0.000185
\Rightarrow \sigma_P \approx 0.0136
$$

Probability portfolio return below 5%:

$$
Z^* = \frac{0.05 - 0.064}{0.0136} \approx -1.03
\Rightarrow \mathbb{P}(R_P < 0.05) \approx \Phi(-1.03) \approx 0.1515
$$

So there's a **15.15% chance** of underperformance.

---

### **6. Summary Table**

| Expression                            | Distribution                                                  |
|---------------------------------------| ------------------------------------------------------------- |
| $`S_n = X_1 + \dots + X_n`$ (indep.)  | $`\mathcal{N}(\sum \mu_i,\; \sum \sigma_i^2)`$                  |
| $`Z = \sum a_i X_i`$ (indep.)         | $`\mathcal{N}(\sum a_i \mu_i,\; \sum a_i^2 \sigma_i^2)`$        |
| $`Z = \sum a_i X_i`$ (correlated)     | Add $`\sum_{i \ne j} a_i a_j \text{Cov}(X_i, X_j)`$ to variance |

---

### **Key Insight**

Any **linear combination** of jointly normal variables is again **normally distributed**. 
This powerful closure property simplifies modeling in finance, control systems, Bayesian statistics, 
and signal processing, where weighted combinations of uncertain inputs arise frequently.
