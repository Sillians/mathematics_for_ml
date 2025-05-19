## **Mean and Variance of the Binomial Distribution**

The **binomial distribution** models the number of successes in a fixed number of **independent** Bernoulli trials, 
each with the same probability of success. It’s commonly used when outcomes are **binary** (success/failure, yes/no).

---

### **Definition of a Binomial Random Variable**

A random variable $`X`$ is said to be binomially distributed if:

$$
X \sim \text{Binomial}(n, p)
$$

Where:

* $`n`$ is the number of trials
* $`p`$ is the probability of success on each trial
* $`q = 1 - p`$ is the probability of failure

---

###  **1. Finding the Mean of a Binomial Random Variable**

The **mean** (expected value) of a binomial distribution is:

$$
\mu = \mathbb{E}[X] = n \cdot p
$$

This gives the **expected number of successes** in $`n`$ trials.

#### Example:

If $`n = 20`$, $`p = 0.3`$:

$$
\mathbb{E}[X] = 20 \cdot 0.3 = \boxed{6}
$$

---

###  **2. Finding the Variance of a Binomial Random Variable**

The **variance** of a binomial random variable is:

$$
\text{Var}(X) = n \cdot p \cdot (1 - p) = n \cdot p \cdot q
$$

This measures the **spread** around the mean.

#### Example:

Using $`n = 20`$, $`p = 0.3`$, $`q = 0.7`$:

$$
\text{Var}(X) = 20 \cdot 0.3 \cdot 0.7 = \boxed{4.2}
$$

---

### 🔹 **3. Finding the Standard Deviation of a Binomial Random Variable**

The **standard deviation** is the square root of the variance:

$$
\sigma = \sqrt{\text{Var}(X)} = \sqrt{n \cdot p \cdot (1 - p)}
$$

#### Example:

Continuing with the values above:

$$
\sigma = \sqrt{4.2} \approx \boxed{2.05}
$$

---

### ✅ **Summary Table**

| Metric                | Formula                                   |
| --------------------- | ----------------------------------------- |
| Mean (Expected Value) | $`\mu = n \cdot p`$                         |
| Variance              | $`\sigma^2 = n \cdot p \cdot (1 - p)`$      |
| Standard Deviation    | $`\sigma = \sqrt{n \cdot p \cdot (1 - p)}`$ |

---

### **Conclusion**

The mean and variance of a binomial distribution provide insights into the **central tendency** and **spread** of outcomes 
in repeated binary trials. Understanding these parameters is crucial for estimating probabilities, constructing confidence intervals, 
and conducting hypothesis tests in discrete data scenarios.
