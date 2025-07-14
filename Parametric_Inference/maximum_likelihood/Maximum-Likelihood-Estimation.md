## **Maximum Likelihood Estimation (MLE)**

---

### **1. Introduction to Maximum Likelihood Estimation**

**Maximum Likelihood Estimation** is a fundamental method in statistics for estimating the parameters of a 
probability distribution based on observed data. It selects the parameter values that 
**maximize the likelihood** that the observed data came from the assumed model.

Given a dataset $`x_1, x_2, \dots, x_n`$ drawn independently from a distribution with PDF or 
PMF $`f(x \mid \theta)`$, the **likelihood function** is:


$$
\mathcal{L}(\theta) = \prod_{i=1}^{n} f(x_i \mid \theta)
$$


And the **log-likelihood function** is:


$$
\ell(\theta) = \log \mathcal{L}(\theta) = \sum_{i=1}^{n} \log f(x_i \mid \theta)
$$


The **Maximum Likelihood Estimator (MLE)** is the value of $`\theta`$ that maximizes this function:


$$
\hat{\theta}_{\text{MLE}} = \underset{\theta}{\arg\max} \; \ell(\theta)
$$

---

### **2. MLE for Discrete Probability Distributions**

#### **Bernoulli Distribution**

If $`X_i \sim \text{Bernoulli}(p)`$, then:

* Likelihood: $`\mathcal{L}(p) = \prod_{i=1}^{n} p^{x_i} (1 - p)^{1 - x_i}`$


* Log-likelihood: $`\ell(p) = \sum_{i=1}^{n} x_i \log p + (1 - x_i) \log(1 - p)`$


* Maximize:

$$
\hat{p} = \frac{1}{n} \sum_{i=1}^{n} x_i
$$

#### **Binomial Distribution**

If $`X_i \sim \text{Bin}(n, p)`$, and $`k = \sum x_i`$, then:

$$
\hat{p} = \frac{k}{n \cdot m}
$$

where $m$ is the number of observations (number of trials).

#### **Poisson Distribution**

If $`X_i \sim \text{Poisson}(\lambda)`$, then:

* Likelihood: $`\mathcal{L}(\lambda) = \prod_{i=1}^{n} \frac{\lambda^{x_i} e^{-\lambda}}{x_i!}`$


* Log-likelihood:

$$
\ell(\lambda) = \sum x_i \log \lambda - n \lambda + \text{const}
$$


* Maximize:

$$
\hat{\lambda} = \bar{x}
$$

---

### **3. MLE for Continuous Probability Distributions**

#### **Normal Distribution** $`\mathcal{N}(\mu, \sigma^2)`$

Given data $`x_1, x_2, \dots, x_n \sim \mathcal{N}(\mu, \sigma^2)`$:


* Log-likelihood:

$$
\ell(\mu, \sigma^2) = -\frac{n}{2} \log(2\pi \sigma^2) - \frac{1}{2\sigma^2} \sum_{i=1}^{n} (x_i - \mu)^2
$$


* MLE estimates:

$$
\hat{\mu} = \bar{x}, \quad \hat{\sigma}^2 = \frac{1}{n} \sum (x_i - \bar{x})^2
$$

  > **Note:** This differs from the unbiased estimator, which divides by $`n - 1`$.


#### **Exponential Distribution** $`f(x \mid \lambda) = \lambda e^{-\lambda x}`$

* Log-likelihood:

$$
\ell(\lambda) = n \log \lambda - \lambda \sum x_i
$$


* MLE:

$$
\hat{\lambda} = \frac{1}{\bar{x}}
$$

#### **Uniform Distribution** $`U(0, \theta)`$

* PDF: $`f(x \mid \theta) = \frac{1}{\theta}`$ for $`0 \le x \le \theta`$


* Likelihood: $`\mathcal{L}(\theta) = \theta^{-n} \mathbf{1}_{\theta \ge \max(x_i)}`$


* MLE:

$$
\hat{\theta} = \max(x_1, \dots, x_n)
$$

---

### **4. General Strategy for MLE**

1. **Write the likelihood function** $`\mathcal{L}(\theta)`$


2. **Take log** to simplify: $`\ell(\theta) = \log \mathcal{L}(\theta)`$


3. **Differentiate**: $`\frac{d\ell}{d\theta} = 0`$


4. **Solve for $`\hat{\theta}`$** to find the MLE

---

### **5. List of Common Maximum Likelihood Estimators**

| Distribution                          | Parameter(s)      | MLE                                                                         |
|---------------------------------------|-------------------| --------------------------------------------------------------------------- |
| Bernoulli $`\text{Bern}(p)`$          | $p$               | $`\hat{p} = \frac{1}{n} \sum x_i`$                                            |
| Binomial $`\text{Bin}(n, p)`$         | $p$               | $`\hat{p} = \frac{k}{n \cdot m}`$                                             |
| Poisson $`\text{Pois}(\lambda)`$      | $`\lambda`$       | $`\hat{\lambda} = \bar{x}`$                                                   |
| Normal $`\mathcal{N}(\mu, \sigma^2)`$ | $`\mu, \sigma^2`$ | $`\hat{\mu} = \bar{x},\; \hat{\sigma}^2 = \frac{1}{n}\sum (x_i - \bar{x})^2`$ |
| Exponential $`\text{Exp}(\lambda)`$   | $`\lambda`$       | $`\hat{\lambda} = \frac{1}{\bar{x}}`$                                         |
| Uniform $`U(0,\theta)`$               | $`\theta`$        | $`\hat{\theta} = \max(x_i)`$                                                  |

---

### **6. Key Properties of MLE**

| Property                 | Description                                                                                        |
| ------------------------ |----------------------------------------------------------------------------------------------------|
| **Consistency**          | $`\hat{\theta}_{\text{MLE}} \to \theta`$ as $`n \to \infty`$                                       |
| **Asymptotic Normality** | $`\hat{\theta} \sim \mathcal{N}(\theta, I^{-1}(\theta))`$ for large $n$                            |
| **Efficiency**           | Achieves the Cramér–Rao lower bound under regularity                                               |
| **Invariance**           | If $`\hat{\theta}`$ is the MLE of $`\theta`$, then $`g(\hat{\theta})`$ is the MLE of $`g(\theta)`$ |

---

### **Conclusion**

MLE is a versatile and powerful technique used across statistics and machine learning. 
It enables parameter estimation for both discrete and continuous models, supports asymptotic theory, 
and connects directly to model likelihood and information-theoretic principles like `AIC`.
