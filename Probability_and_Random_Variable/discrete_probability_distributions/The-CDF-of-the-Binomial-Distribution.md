## **The Cumulative Distribution Function (CDF) of the Binomial Distribution**

The **Binomial Distribution** models the number of successes in a fixed number of independent 
Bernoulli trials, each with the same probability of success. The **Cumulative Distribution Function (CDF)** 
helps compute probabilities **up to a given number of successes**, which is especially useful when 
dealing with intervals or complements.

---

### **1. Definition: CDF of the Binomial Distribution**

Let $`X \sim \text{Bin}(n, p)`$, where:

* $`n`$ is the number of trials,
* $`p`$ is the probability of success in each trial,
* $`X`$ counts the number of successes.

The **CDF** is:

$$
\boxed{P(X \leq k) = F(k; n, p) = \sum_{x=0}^{k} \binom{n}{x} p^x (1 - p)^{n - x}}
$$

This represents the probability of obtaining **at most** $k$ successes.

---

### **2. Constructing a Binomial CDF Table**

A **Binomial CDF table** lists cumulative probabilities for given values of:

* $`n`$: number of trials,
* $`p`$: probability of success,
* $`k`$: number of successes.

#### **Example (excerpt)**

For $`n = 5`$, $`p = 0.4`$:

| $k$ | $P(X \leq k)$ |
| --- | ------------- |
| 0   | 0.07776       |
| 1   | 0.31744       |
| 2   | 0.68256       |
| 3   | 0.92224       |
| 4   | 0.98944       |
| 5   | 1.00000       |

These values save time by **accumulating binomial probabilities**.

---

### **3. Computing a Binomial Probability Using the CDF**

To find the probability of **at most** $k$ successes:

$$
P(X \leq k) = \text{Look up or calculate directly using the CDF formula.}
$$

#### **Example:**

For $`X \sim \text{Bin}(n=5, p=0.4)`$, find $`P(X \leq 2)`$:

From the table:

$$
\boxed{P(X \leq 2) = 0.68256}
$$

---

### **4. Computing a Binomial Probability Over an Interval Using the CDF**

To compute $`P(a \leq X \leq b)`$, use:

$$
\boxed{P(a \leq X \leq b) = P(X \leq b) - P(X < a) = F(b; n, p) - F(a - 1; n, p)}
$$

#### **Example:**

Find $`P(2 \leq X \leq 4)`$ for $`n = 5`$, $`p = 0.4`$:

$$
P(2 \leq X \leq 4) = P(X \leq 4) - P(X \leq 1) = 0.98944 - 0.31744 = \boxed{0.672}
$$

---

### **5. Computing a Binomial Probability Over an Interval Containing a "Greater Than" Symbol**

Use the **complement rule**:

$$
\boxed{P(X > k) = 1 - P(X \leq k)}
$$

#### **Example:**

Find $`P(X > 3)`$ for $`X \sim \text{Bin}(n=5, p=0.4)`$:

$$
P(X > 3) = 1 - P(X \leq 3) = 1 - 0.92224 = \boxed{0.07776}
$$

---

### ✅ **Summary Table**

| Task               | Formula                                                     |
| ------------------ | ----------------------------------------------------------- |
| **CDF definition** | $`P(X \leq k) = \sum_{x=0}^{k} \binom{n}{x} p^x (1-p)^{n-x}`$ |
| **Interval**       | $`P(a \leq X \leq b) = P(X \leq b) - P(X \leq a - 1)`$        |
| **Greater than**   | $`P(X > k) = 1 - P(X \leq k)`$                                |
| **Using table**    | Lookup $`F(k; n, p)`$ in CDF table                            |

---

### **Conclusion**

The **Binomial CDF** is essential for efficiently computing cumulative probabilities, particularly 
over intervals or when determining tail probabilities. Whether used through formulas or CDF tables, 
it simplifies calculations in probability, statistics, and real-world decision models involving 
binary outcomes.
