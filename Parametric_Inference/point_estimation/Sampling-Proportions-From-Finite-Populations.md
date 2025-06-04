## **Sampling Proportions From Finite Populations**

---

## 1. Introduction: Sampling Proportions

When sampling from a finite population **without replacement**, the **sample proportion** is the fraction of 
sampled items that possess a particular characteristic.

Let:

* $`N`$: population size
* $`n`$: sample size
* $`M`$: number of population elements with the trait
* $`p = M / N`$: population proportion
* $`X`$: number in the sample with the trait
* $`\hat{p} = X / n`$: sample proportion

---

## 2. Finding a Conditional Probability Given a Population Proportion

If sampling is **without replacement**, then `X` (number of items with the trait in the sample) follows a **hypergeometric distribution**:

$$
P(X = k) = \frac{\binom{M}{k} \binom{N - M}{n - k}}{\binom{N}{n}}
$$

**Example**:
From a population of 100 items, where 40 are defective (`M = 40`), what’s the probability of finding exactly 4 defective items in a sample of 10?

$$
P(X = 4) = \frac{\binom{40}{4} \binom{60}{6}}{\binom{100}{10}}
$$

---

## 3. Properties of Sums of Bernoulli Random Variables

If sampling is **with replacement**, or from an **infinite population**, `X` follows a **Binomial distribution**:

$$
X \sim \text{Binomial}(n, p)
$$

Each Bernoulli trial has:

* Mean: $`\mathbb{E}[X_i] = p`$
* Variance: $`\mathrm{Var}(X_i) = p(1 - p)`$

For the sum $`X = \sum X_i`$:

* Mean: $`\mathbb{E}[X] = np`$
* Variance: $`\mathrm{Var}(X) = np(1 - p)`$

---

## 4. Mean and Variance of Sample Proportions

### a. **With Replacement** or from an **Infinite Population**:

$$
\mathbb{E}[\hat{p}] = p
$$

$$
\mathrm{Var}(\hat{p}) = \frac{p(1 - p)}{n}
$$

### b. **Without Replacement** from a **Finite Population**:

Apply the **finite population correction (FPC)**:

$$
\mathbb{E}[\hat{p}] = p
$$

$$
\mathrm{Var}(\hat{p}) = \frac{p(1 - p)}{n} \cdot \frac{N - n}{N - 1}
$$

---

## Summary Table

| Sampling Scenario                       | Mean of $`\hat{p}`$ | Variance of $`\hat{p}`$                                                              |
| --------------------------------------- | ----------------- | ---------------------------------------------------------------------------------- |
| Infinite population / With replacement  | $`p`$               | $`\frac{p(1 - p)}{n}`$                                                               |
| Finite population / Without replacement | $`p`$               | $`\frac{p(1 - p)}{n} \cdot \frac{N - n}{N - 1}`$ (with finite population correction) |


