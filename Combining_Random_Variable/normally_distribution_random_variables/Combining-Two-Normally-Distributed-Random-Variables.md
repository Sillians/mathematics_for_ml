## **Combining Two Normally Distributed Random Variables**

---

### **1. Fundamentals**

If $`X \sim \mathcal{N}(\mu_X, \sigma_X^2)`$ and $`Y \sim \mathcal{N}(\mu_Y, \sigma_Y^2)`$, and they are **jointly normally distributed**, then any **linear combination** of them is also normally distributed:

$$
Z = aX + bY \sim \mathcal{N}(a\mu_X + b\mu_Y,\; a^2\sigma_X^2 + b^2\sigma_Y^2 + 2ab\,\text{Cov}(X, Y))
$$

If $X$ and $Y$ are **independent**, then $`\text{Cov}(X, Y) = 0`$.

---

### **2. Distribution of a Sum or Difference of Normal Random Variables**

For $`Z = X + Y`$ or $`Z = X - Y`$:

#### **If independent**:

* **Sum**:

  $$
  Z = X + Y \sim \mathcal{N}(\mu_X + \mu_Y,\; \sigma_X^2 + \sigma_Y^2)
  $$

* **Difference**:

  $$
  Z = X - Y \sim \mathcal{N}(\mu_X - \mu_Y,\; \sigma_X^2 + \sigma_Y^2)
  $$

#### **If dependent** (known correlation $`\rho`$):

$$
\text{Var}(aX + bY) = a^2\sigma_X^2 + b^2\sigma_Y^2 + 2ab\,\rho\sigma_X\sigma_Y
$$

---

### **3. Distribution of a Scaled Sum or Difference**

Let $`Z = aX + bY`$, where $`a, b \in \mathbb{R}`$.

Then:

$$
Z \sim \mathcal{N}(a\mu_X + b\mu_Y,\; a^2\sigma_X^2 + b^2\sigma_Y^2 + 2ab\,\text{Cov}(X, Y))
$$

If $X$ and $Y$ are independent:

$$
Z \sim \mathcal{N}(a\mu_X + b\mu_Y,\; a^2\sigma_X^2 + b^2\sigma_Y^2)
$$

#### **Example**

Let $`X \sim \mathcal{N}(3, 1)`$, $`Y \sim \mathcal{N}(5, 4)`$, independent.

Then:

* $`Z = 2X - 3Y \sim \mathcal{N}(2(3) - 3(5), 4(1)^2 + 9(4)^2) = \mathcal{N}(-9,\; 4 + 144 = 148)`$

---

### **4. Calculating a Probability: Sum/Difference of Normals**

**Procedure**:

1. Determine $`\mu_Z`$ and $`\sigma_Z^2`$
2. Standardize:

   $$
   Z^* = \frac{Z - \mu_Z}{\sigma_Z}
   $$

3. Use standard normal tables (or software) to compute $`\mathbb{P}(Z \le z)`$

---

#### **Example**

Let $`X \sim \mathcal{N}(100, 10^2)`$, $`Y \sim \mathcal{N}(80, 5^2)`$, independent.

Find $`\mathbb{P}(X + Y \le 190)`$:

* $`\mu = 100 + 80 = 180`$
* $`\sigma^2 = 10^2 + 5^2 = 125`$, $`\sigma = \sqrt{125} \approx 11.18`$

$$
Z = \frac{190 - 180}{11.18} \approx 0.894
\Rightarrow \mathbb{P}(X + Y \le 190) = \Phi(0.894) \approx 0.813
$$

---

### **5. Contextual Example**

**Scenario**: Two machines independently fill jars with weights $`X \sim \mathcal{N}(250, 2^2)`$ and $`Y \sim \mathcal{N}(300, 3^2)`$. 
The final product is a sealed package of both jars.

#### **a) Distribution of total weight**

$$
W = X + Y \sim \mathcal{N}(550, 13)
$$

* $`\mu = 250 + 300 = 550`$
* $`\sigma^2 = 4 + 9 = 13`$

---

#### **b) Probability that the package weighs less than 540g**

$$
Z = \frac{540 - 550}{\sqrt{13}} \approx -2.77
\Rightarrow \mathbb{P}(W < 540) = \Phi(-2.77) \approx 0.0028
$$

So there's a **0.28% chance** of underweight.

---

### **6. Summary Table**

| Expression    | Distribution                                                                              |
|---------------| ----------------------------------------------------------------------------------------- |
| $`X + Y`$     | $`\mathcal{N}(\mu_X + \mu_Y, \sigma_X^2 + \sigma_Y^2)`$ (if independent)                    |
| $`X - Y`$     | $`\mathcal{N}(\mu_X - \mu_Y, \sigma_X^2 + \sigma_Y^2)`$ (if independent)                    |
| $`aX + bY`$   | $`\mathcal{N}(a\mu_X + b\mu_Y,\; a^2\sigma_X^2 + b^2\sigma_Y^2 + 2ab\rho\sigma_X\sigma_Y)`$ |

---

### **Key Insight**

The linear combination of normal variables remains normal — enabling efficient computation of new distributions, probabilities, and risk estimates in statistics, finance, engineering, and more.
