## **The Sample Mean**

---

## **1. Definition: Sample Mean**

Given a sample of size $n$:

$$
X_1, X_2, \dots, X_n
$$

The **sample mean** $`\bar{X}`$ is defined as:

$$
\bar{X} = \frac{1}{n} \sum_{i=1}^{n} X_i
$$

It serves as an estimator of the **population mean** $`\mu`$ when the full population is not accessible.

---

## **2. Estimating a Population Mean From the Sample Mean**

The sample mean $`\bar{X}`$ is a **point estimator** of the population mean $`\mu`$:

$$
\bar{X} \approx \mu
$$

This estimation becomes more accurate as:

* The sample size $n$ increases (by the **Law of Large Numbers**),
* The sample is representative of the population (i.e., random and unbiased).

**Example**:
If a researcher collects the heights of 100 randomly selected individuals and finds $`\bar{X} = 170 \text{ cm}`$, they estimate:

$$
\mu \approx 170 \text{ cm}
$$

---

## **3. The Expected Value of the Sample Mean**

Assume $`X_1, X_2, \dots, X_n`$ are **i.i.d.** (independent and identically distributed) with mean $`\mu`$ and variance $`\sigma^2`$. Then:

### **Expected Value**:

$$
\mathbb{E}[\bar{X}] = \mu
$$

This shows that the sample mean is an **unbiased estimator** of the population mean.

### **Variance**:

$$
\text{Var}(\bar{X}) = \frac{\sigma^2}{n}
$$

This decreases as the sample size increases, improving the precision of $`\bar{X}`$.

---

## **4. Key Properties of the Sample Mean**

| Property              | Formula / Explanation                                                |
| --------------------- | -------------------------------------------------------------------- |
| Linearity             | $`\mathbb{E}[a\bar{X} + b] = a \mathbb{E}[\bar{X}] + b`$               |
| Unbiased Estimator    | $`\mathbb{E}[\bar{X}] = \mu`$                                          |
| Variance              | $`\text{Var}(\bar{X}) = \frac{\sigma^2}{n}`$                           |
| Law of Large Numbers  | $`\bar{X} \xrightarrow{P} \mu$ as $n \to \infty`$                      |
| Central Limit Theorem | $`\bar{X} \approx \mathcal{N}(\mu, \frac{\sigma^2}{n})`$ for large $`n`$ |

---

## **5. Example: Estimating Population Mean From Sample**

**Scenario**:
A random sample of 5 observations:

$$
X = \{10, 12, 14, 11, 13\}
$$

Then:

$$
\bar{X} = \frac{10 + 12 + 14 + 11 + 13}{5} = \frac{60}{5} = 12
$$

Interpretation:
The estimated population mean is $`\mu \approx 12`$.

---

## **6. Visual Summary**

* **Sample mean** aggregates the data into a single central tendency.
* **Expected value** of the sample mean equals the population mean if the sample is random and i.i.d.
* **Precision** increases as $n$ increases due to shrinking variance.

---

This provides a comprehensive and properly formatted markdown deep dive into the sample mean and its role in statistical inference.
