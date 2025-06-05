## **Log-Likelihood Functions for Discrete Probability Distributions**

---

### **1. Log-Likelihood Functions – Overview**

For a discrete random variable with a probability mass function (PMF) $`P(X = x \mid \theta)`$, 
the **likelihood function** for observed data $`\{x_1, x_2, \dots, x_n\}`$ is:

$$
L(\theta) = \prod_{i=1}^{n} P(x_i \mid \theta)
$$

The **log-likelihood function** is the natural logarithm of the likelihood:

$$
\ell(\theta) = \log L(\theta) = \sum_{i=1}^{n} \log P(x_i \mid \theta)
$$

This transformation:

* Simplifies calculations (especially differentiation for MLE)
* Converts products into sums
* Maintains the same maximizer as the likelihood

---

### **2. Log-Likelihood Function for Bernoulli Random Variables**

Let $`X_1, \dots, X_n \sim \text{Bernoulli}(p)`$, where $`X_i \in \{0, 1\}`$, and $`p \in (0,1)`$ is the probability of success.

**PMF**:

$$
P(X = x) = p^x (1 - p)^{1 - x}
$$

**Log-likelihood function**:

$$
\ell(p) = \sum_{i=1}^{n} \left[ x_i \log p + (1 - x_i) \log(1 - p) \right]
$$

Or, defining $`S = \sum x_i`$, the number of successes:

$$
\ell(p) = S \log p + (n - S) \log(1 - p)
$$

---

### **3. Log-Likelihood Function for Binomial Random Variables**

Let $`X_1, \dots, X_n \sim \text{Binomial}(m, p)`$, where each trial has $`m`$ attempts and success probability $p$.

**PMF**:

$$
P(X = x) = \binom{m}{x} p^x (1 - p)^{m - x}
$$

**Log-likelihood function** for observed data $`x_1, \dots, x_n`$:

$$
\ell(p) = \sum_{i=1}^{n} \left[ \log \binom{m}{x_i} + x_i \log p + (m - x_i) \log(1 - p) \right]
$$

$$
\ell(p) = \sum_{i=1}^{n} \log \binom{m}{x_i} + \left(\sum x_i\right) \log p + \left(nm - \sum x_i\right) \log(1 - p)
$$

The term $`\sum \log \binom{m}{x_i}`$ is constant w\.r.t. $p$, so often omitted when maximizing.

---

### **4. Log-Likelihood Function for Poisson Random Variables**

Let $`X_1, \dots, X_n \sim \text{Poisson}(\lambda)`$, where $`\lambda > 0`$ is the average event rate.

**PMF**:

$$
P(X = x) = \frac{e^{-\lambda} \lambda^x}{x!}
$$

**Log-likelihood function**:

$$
\ell(\lambda) = \sum_{i=1}^{n} \left[ -\lambda + x_i \log \lambda - \log(x_i!) \right]
$$

$$
\ell(\lambda) = -n\lambda + \left(\sum x_i\right) \log \lambda - \sum \log(x_i!)
$$

Again, $`\sum \log(x_i!)`$ is constant with respect to $`\lambda`$, so often ignored in optimization.

---

### **Summary Table**

| Distribution                                 | PMF                                 | Log-Likelihood Function                                           |
| -------------------------------------------- | ----------------------------------- | ----------------------------------------------------------------- |
| **Bernoulli** $`X \sim \text{Bern}(p)`$        | $`p^x (1-p)^{1-x}`$                  | $`\sum [x_i \log p + (1 - x_i) \log(1 - p)]`$                      |
| **Binomial** $`X \sim \text{Bin}(m, p)`$       | $`\binom{m}{x} p^x (1-p)^{m-x}`$     | $`\sum [\log \binom{m}{x_i} + x_i \log p + (m - x_i) \log(1 - p)]`$ |
| **Poisson** $`X \sim \text{Poisson}(\lambda)`$ | $`\frac{e^{-\lambda} \lambda^x}{x!}`$ | $`-n\lambda + (\sum x_i) \log \lambda - \sum \log(x_i!)`$           |

---

### **Key Insights**

* Log-likelihoods provide a foundation for **maximum likelihood estimation (MLE)**.
* Constant terms (not involving parameters) can be safely omitted for estimation.
* Each log-likelihood reflects the structure of the corresponding distribution’s PMF.
* The **score function** (gradient of log-likelihood) and **Hessian** are used to derive estimators and their properties.

This foundation is critical in statistical modeling, inference, and machine learning.
