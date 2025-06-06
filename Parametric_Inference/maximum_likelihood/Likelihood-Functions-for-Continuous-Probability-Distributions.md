## **Likelihood Functions for Continuous Probability Distributions**

---

### **1. Likelihood Functions for Continuous Random Variables**

For a **continuous random variable** $`X \sim f(x \mid \theta)`$, where $f$ is the **probability density function
(PDF)** parameterized by $`\theta`$, the **likelihood function** based on observed data $`\{x_1, x_2, \dots, x_n\}`$ is:

$$
L(\theta) = \prod_{i=1}^{n} f(x_i \mid \theta)
$$

The **log-likelihood function** is:

$$
\ell(\theta) = \sum_{i=1}^{n} \log f(x_i \mid \theta)
$$

Unlike the discrete case, the PDF does not directly give probabilities, but the **likelihood** still reflects how "plausible" the observed data are under a specific parameter $\theta$.

---

### **2. Likelihood Function for Exponential Random Variables**

Let $`X_1, \dots, X_n \sim \text{Exponential}(\lambda)`$, where $`\lambda > 0`$ is the rate parameter.

**PDF**:

$$
f(x \mid \lambda) = \lambda e^{-\lambda x}, \quad x \ge 0
$$

**Likelihood function**:

$$
L(\lambda) = \prod_{i=1}^{n} \lambda e^{-\lambda x_i} = \lambda^n e^{-\lambda \sum x_i}
$$

**Log-likelihood function**:

$$
\ell(\lambda) = n \log \lambda - \lambda \sum x_i
$$

This is a **concave** function in $`\lambda`$, and the MLE can be found easily by taking derivatives.

---

### **3. Likelihood Function for Normal Random Variables**

Let $`X_1, \dots, X_n \sim \mathcal{N}(\mu, \sigma^2)`$, with mean $`\mu \in \mathbb{R}`$ and variance $`\sigma^2 > 0`$.

**PDF**:

$$
f(x \mid \mu, \sigma^2) = \frac{1}{\sqrt{2\pi \sigma^2}} \exp\left( -\frac{(x - \mu)^2}{2\sigma^2} \right)
$$

**Likelihood function**:

$$
L(\mu, \sigma^2) = \prod_{i=1}^{n} \frac{1}{\sqrt{2\pi \sigma^2}} \exp\left( -\frac{(x_i - \mu)^2}{2\sigma^2} \right)
$$

$$
= (2\pi \sigma^2)^{-n/2} \exp\left( -\frac{1}{2\sigma^2} \sum_{i=1}^{n} (x_i - \mu)^2 \right)
$$

**Log-likelihood function**:

$$
\ell(\mu, \sigma^2) = -\frac{n}{2} \log(2\pi \sigma^2) - \frac{1}{2\sigma^2} \sum_{i=1}^{n} (x_i - \mu)^2
$$

Maximizing this function with respect to $`\mu`$ and $`\sigma^2`$ leads to:

* MLE of $`\mu`$: $`\hat{\mu} = \frac{1}{n} \sum x_i`$
* MLE of $`\sigma^2`$: $`\hat{\sigma}^2 = \frac{1}{n} \sum (x_i - \hat{\mu})^2`$

---

### **Summary Table**

| Distribution                                   | PDF                                                                            | Log-Likelihood Function                                                     |
| ---------------------------------------------- | ------------------------------------------------------------------------------ | --------------------------------------------------------------------------- |
| **Exponential** $`X \sim \text{Exp}(\lambda)`$   | $`\lambda e^{-\lambda x}`$                                                       | $`n \log \lambda - \lambda \sum x_i`$                                         |
| **Normal** $`X \sim \mathcal{N}(\mu, \sigma^2)`$ | $`\frac{1}{\sqrt{2\pi \sigma^2}} \exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right)`$ | $`-\frac{n}{2} \log(2\pi \sigma^2) - \frac{1}{2\sigma^2} \sum (x_i - \mu)^2`$ |

---

### **Key Takeaways**

* For **continuous distributions**, likelihood functions measure the relative plausibility of parameter values given observed data.
* **Log-likelihoods** simplify optimization and are foundational in estimation (MLE), model fitting, and statistical inference.
* **Exponential distributions** yield simple log-likelihoods linear in $`\lambda`$.
* **Normal distributions** have quadratic log-likelihoods in $`\mu`$, enabling closed-form MLEs.
* In multivariate and Bayesian contexts, these log-likelihoods are combined with priors or constraints to estimate parameters more robustly.
