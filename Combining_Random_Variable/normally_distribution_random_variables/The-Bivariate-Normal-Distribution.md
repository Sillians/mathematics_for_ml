## **The Bivariate Normal Distribution**

---

### **1. Introduction**

The **bivariate normal distribution** generalizes the univariate normal distribution to two variables. 
It models two **jointly normally distributed** random variables $X$ and $Y$, capturing not just their 
individual behavior but also the **linear relationship** (correlation) between them.



$$
(X, Y) \sim \mathcal{N}_2\left(
\begin{bmatrix}
\mu_X \\
\mu_Y
\end{bmatrix},
\begin{bmatrix}
\sigma_X^2 & \rho \sigma_X \sigma_Y \\
\rho \sigma_X \sigma_Y & \sigma_Y^2
\end{bmatrix}
\right)
$$


Where:

* $`\mu_X, \mu_Y`$ are means,


* $`\sigma_X, \sigma_Y`$ are standard deviations,


* $`\rho \in [-1, 1]`$ is the **correlation coefficient** between $X$ and $Y$.

---




### **2. The Joint PDF of a Bivariate Normal Random Variable**



Let $X$ and $Y$ have means $`\mu_X, \mu_Y`$, standard deviations $`\sigma_X, \sigma_Y`$, and correlation coefficient $`\rho`$. 
Then their **joint probability density function** is:




$` f(x, y) = \frac{1}{2\pi \sigma_X \sigma_Y \sqrt{1 - \rho^2}} \exp\left( -\frac{1}{2(1 - \rho^2)}  \left[ \left( \frac{x - \mu_X}{\sigma_X} \right)^2 - 2\rho \left( \frac{x - \mu_X}{\sigma_X} \right)\left( \frac{y - \mu_Y}{\sigma_Y} \right) + \left( \frac{y - \mu_Y}{\sigma_Y} \right)^2 \right] \right)`$




#### **Key Properties:**

* If $`\rho = 0`$, then $X$ and $Y$ are **independent**.


* If $`\rho \ne 0`$, the distribution reflects linear **dependence**.


* Contours of constant density are **ellipses** centered at $`(\mu_X, \mu_Y)`$.

---

### **3. Linear Combinations of Bivariate Normal Variables**

Suppose $`X, Y \sim \mathcal{N}_2(\mu, \Sigma)`$. Let:

$$
Z = aX + bY
$$

Then $`Z \sim \mathcal{N}(\mu_Z, \sigma_Z^2)`$, where:

* **Mean:**

  $$
  \mu_Z = a\mu_X + b\mu_Y
  $$


* **Variance:**

  $$
  \sigma_Z^2 = a^2\sigma_X^2 + b^2\sigma_Y^2 + 2ab\rho\sigma_X\sigma_Y
  $$

#### **Example:**

Let:

* $`\mu_X = 1, \mu_Y = 2`$


* $`\sigma_X = 1, \sigma_Y = 2, \rho = 0.5`$


* Let $`Z = 3X - 2Y`$

Then:

* $`\mu_Z = 3(1) - 2(2) = -1`$


* $`\sigma_Z^2 = 9(1^2) + 4(2^2) + 2(3)(-2)(0.5)(1)(2) = 9 + 16 - 12 = 13`$


So $`Z \sim \mathcal{N}(-1, 13)`$

---

### **4. Linear Combinations of Elements From a Multivariate Normal Random Variable**

Let $`\mathbf{X} \sim \mathcal{N}_n({\mu}, {\Sigma})`$, and let $`\mathbf{a} \in \mathbb{R}^n`$. Define:

$$
Z = \mathbf{a}^\top \mathbf{X}
$$


Then:

* $`Z \sim \mathcal{N}(\mathbf{a}^\top {\mu},\ \mathbf{a}^\top {\Sigma} \mathbf{a})`$

#### **Example:**

Let:

$$
\mathbf{X} =
\begin{bmatrix}
X_1 \\
X_2 \\
X_3
\end{bmatrix}
\sim \mathcal{N}_3
\left(
\begin{bmatrix}
0 \\
1 \\
2
\end{bmatrix},
\begin{bmatrix}
1 & 0.5 & 0 \\
0.5 & 2 & 1 \\
0 & 1 & 3
\end{bmatrix}
\right)
$$

and $`\mathbf{a} = [1,\ -1,\ 1]^\top`$

Then:

* $`\mathbb{E}[Z] = 1(0) -1(1) + 1(2) = 1`$


* $`\text{Var}(Z) = \mathbf{a}^\top \Sigma \mathbf{a} = 1(1) + 1(2) + 1(3) - 2(0.5) - 2(1) + 0 = 6 - 1 - 2 = 3`$


So $`Z \sim \mathcal{N}(1, 3)`$

---


### **5. Summary Table**

| Feature                      | Formula                                                                                                     |        |
|------------------------------|-------------------------------------------------------------------------------------------------------------|--------|
| Joint PDF                    | See Section 2                                                                                               |        |
| Marginal of $X$              | $`X \sim \mathcal{N}(\mu_X, \sigma_X^2)`$                                                                   |        |
| Conditional of $`(Y ∥ X=x )`$ | $`\mathcal{N}\left(\mu_Y + \rho \frac{\sigma_Y}{\sigma_X}(x - \mu_X),\ \sigma_Y^2(1 - \rho^2)\right)`$       |
| Linear Combination           | $`aX + bY \sim \mathcal{N}(a\mu_X + b\mu_Y,\ a^2\sigma_X^2 + b^2\sigma_Y^2 + 2ab\rho\sigma_X\sigma_Y)`$     |        |
| Multivariate Linear          | $`\mathbf{a}^\top \mathbf{X} \sim \mathcal{N}(\mathbf{a}^\top {\mu},\ \mathbf{a}^\top {\Sigma} \mathbf{a})`$ |        |

---

### **6. Applications**

| Field             | Application                                  |
| ----------------- | -------------------------------------------- |
| Machine Learning  | Gaussian mixture models, generative models   |
| Finance           | Joint modeling of asset returns              |
| Signal Processing | Noise modeling                               |
| Statistics        | Hypothesis testing and multivariate analysis |

---
