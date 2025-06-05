## **Likelihood Functions for Discrete Probability Distributions**

A **likelihood function** measures the plausibility of a parameter value given observed data. 
For discrete distributions, the likelihood is the joint probability of observed outcomes, 
viewed as a function of the distribution parameter(s).

Given data $`x_1, x_2, \ldots, x_n`$ from a discrete distribution with parameter $`\theta`$, the **likelihood function** is:

$$
L(\theta) = \prod_{i=1}^{n} P(X = x_i \mid \theta)
$$

---

## **1. Likelihood Functions for Bernoulli Random Variables**

A **Bernoulli random variable** takes values 0 and 1 with success probability $p$.

### PMF:

$$
P(X = x) = p^x (1 - p)^{1 - x}, \quad x \in \{0, 1\}
$$

### Likelihood Function:

Given $n$ i.i.d. observations $`x_1, x_2, \dots, x_n \in \{0, 1\}`$, let $`S = \sum_{i=1}^{n} x_i`$ be the number of successes.

$$
L(p) = \prod_{i=1}^{n} p^{x_i} (1 - p)^{1 - x_i} = p^S (1 - p)^{n - S}
$$

---

## **2. Likelihood Functions for Binomial Random Variables**

A **Binomial random variable** with parameters $n$ and $p$ gives the number of successes in $n$ independent Bernoulli trials.

### PMF:

$$
P(X = x) = \binom{n}{x} p^x (1 - p)^{n - x}, \quad x \in \{0, 1, \dots, n\}
$$

### Likelihood Function:

Given $m$ i.i.d. binomial observations $`x_1, x_2, \dots, x_m`$, each from a $`\text{Binomial}(n, p)`$ distribution:

$$
L(p) = \prod_{i=1}^{m} \binom{n}{x_i} p^{x_i} (1 - p)^{n - x_i}
$$

This simplifies to:

$$
L(p) = \left[ \prod_{i=1}^{m} \binom{n}{x_i} \right] p^{\sum x_i} (1 - p)^{mn - \sum x_i}
$$

---

## **3. Likelihood Functions for Poisson Random Variables**

A **Poisson random variable** counts the number of events in a fixed interval, with average rate $`\lambda`$.

### PMF:

$$
P(X = x) = \frac{\lambda^x e^{-\lambda}}{x!}, \quad x \in \{0, 1, 2, \dots\}
$$

### Likelihood Function:

Given $n$ i.i.d. Poisson observations $`x_1, x_2, \dots, x_n`$, define $`S = \sum x_i`$:

$$
L(\lambda) = \prod_{i=1}^{n} \frac{\lambda^{x_i} e^{-\lambda}}{x_i!}
= \left( \prod_{i=1}^{n} \frac{1}{x_i!} \right) \lambda^S e^{-n\lambda}
$$

---

## **Summary Table**

| Distribution | PMF                                 | Likelihood Function $`L(\theta)`$                                   |
| ------------ | ----------------------------------- | ----------------------------------------------------------------- |
| Bernoulli    | $`p^x (1-p)^{1-x}`$                   | $`p^S (1 - p)^{n - S}`$                                             |
| Binomial     | $`\binom{n}{x} p^x (1-p)^{n-x}`$      | $`\prod \binom{n}{x_i} \cdot p^{\sum x_i} (1 - p)^{mn - \sum x_i}`$ |
| Poisson      | $`\frac{\lambda^x e^{-\lambda}}{x!}`$ | $`\left( \prod \frac{1}{x_i!} \right) \lambda^S e^{-n\lambda}`$     |

---

Likelihood functions are foundational for **maximum likelihood estimation (MLE)**, where parameter estimates maximize $`L(\theta)`$ or its log.
