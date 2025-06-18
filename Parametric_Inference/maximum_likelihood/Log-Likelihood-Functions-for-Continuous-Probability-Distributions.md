##  **Log-Likelihood Functions for Continuous Probability Distributions**

---

##  Overview: What Is a Log-Likelihood?

For a continuous random variable $X$ with probability density function (PDF) $`f(x \mid \theta)`$ and 
a set of observations $`{x\_1, x\_2, \dots, x\_n}`$, the **likelihood function** is:

$$
L(\theta) = \prod_{i=1}^n f(x_i \mid \theta)
$$

The **log-likelihood function** is the natural logarithm of the likelihood:

$$
\ell(\theta) = \log L(\theta) = \sum_{i=1}^n \log f(x_i \mid \theta)
$$

Using log-likelihood simplifies product-based likelihoods into sum-based expressions, which are easier to optimize.

---

##  Log-Likelihood for Continuous Random Variables

The general form for the log-likelihood function for a continuous distribution is:

$$
\ell(\theta) = \sum_{i=1}^n \log f(x_i \mid \theta)
$$

Where:

* $`f(x\_i \mid \theta)`$ is the PDF of the distribution
* $`\theta`$ represents one or more parameters (e.g., mean, variance)

---

## ⚡ Example: Exponential Distribution

**PDF** of the exponential distribution with rate $`\lambda > 0`$:

$$
f(x \mid \lambda) = \lambda e^{-\lambda x}, \quad x \geq 0
$$

For a sample $`{x\_1, x\_2, \dots, x\_n}`$, the **log-likelihood function** is:

###  Step-by-step:

1. Write the likelihood:

$$
L(\lambda) = \prod_{i=1}^n \lambda e^{-\lambda x_i} = \lambda^n e^{-\lambda \sum x_i}
$$

2. Take the log:

$$
\ell(\lambda) = n \log \lambda - \lambda \sum_{i=1}^n x_i
$$

This is the expression to maximize when estimating $`\lambda`$ (via MLE).

---

##  Example: Normal Distribution

**PDF** of $`\mathcal{N}(\mu, \sigma^2)`$:

$$
f(x \mid \mu, \sigma^2) = \frac{1}{\sqrt{2\pi\sigma^2}} \exp\left( -\frac{(x - \mu)^2}{2\sigma^2} \right)
$$

For observations $`{x\_1, \dots, x\_n}`$:

###  Step-by-step:

1. Likelihood:

$$
L(\mu, \sigma^2) = \prod_{i=1}^n \frac{1}{\sqrt{2\pi\sigma^2}} \exp\left( -\frac{(x_i - \mu)^2}{2\sigma^2} \right)
$$

2. Log-likelihood:

$$
\ell(\mu, \sigma^2) = -\frac{n}{2} \log(2\pi\sigma^2) - \frac{1}{2\sigma^2} \sum_{i=1}^n (x_i - \mu)^2
$$

This form is used to derive maximum likelihood estimates for $`\mu`$ and $`\sigma^2`$.

---

## 📈 Summary Table

| **Distribution** | **PDF**                                                                                 | **Log-Likelihood $`\ell(\theta)`$**                                          |
| ---------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| Exponential      | $`f(x) = \lambda e^{-\lambda x}`$                                                       | $`n \log \lambda - \lambda \sum x\_i`$                                      |
| Normal           | $`f(x) = \frac{1}{\sqrt{2\pi\sigma^2}} \exp\left(-\frac{(x - \mu)^2}{2\sigma^2}\right)`$ | $`-\frac{n}{2} \log(2\pi\sigma^2) - \frac{1}{2\sigma^2} \sum (x\_i - \mu)^2`$ |

---

##  Final Insight

> Log-likelihood functions transform complex probability products into more manageable summations, providing a cornerstone for parameter estimation (e.g., Maximum Likelihood Estimation) in statistics and machine learning.

---