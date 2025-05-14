## **The Cumulative Distribution Function (CDF) of the Poisson Distribution**

The **Cumulative Distribution Function (CDF)** of a Poisson distribution gives the **probability that the number of events is 
less than or equal to a specific value**. It is particularly useful when calculating probabilities over **intervals** or 
when using **Poisson tables** to avoid summing individual probabilities manually.

---

### **1. Definition: CDF of the Poisson Distribution**

If $`X \sim \text{Poisson}(\lambda)`$, then the **CDF** is:

$$
\boxed{P(X \leq k) = F(k; \lambda) = \sum_{i=0}^{k} \frac{\lambda^i e^{-\lambda}}{i!}}
$$

This gives the **accumulated probability** up to and including $k$ events.

---

### **2. Constructing a Poisson CDF Table**

A **Poisson CDF table** provides precomputed values of $`P(X \leq k)`$ for various values of:

* $`\lambda`$: the mean rate of occurrence
* $`k`$: number of events

The table allows quick lookup without manual computation. Here's an example snippet (values approximated):

| $k$ | $\lambda = 2$ | $\lambda = 3$ |
| --- | ------------- | ------------- |
| 0   | 0.1353        | 0.0498        |
| 1   | 0.4060        | 0.1991        |
| 2   | 0.6767        | 0.4232        |
| 3   | 0.8571        | 0.6472        |
| 4   | 0.9473        | 0.8153        |
| 5   | 0.9834        | 0.9161        |

---

### **3. Computing a Poisson Probability Using a CDF Table**

To compute $`P(X \leq k)`$, **look up** $k$ and $`\lambda`$ in the table.

#### **Example:**

If $`X \sim \text{Poisson}(3)`$, find $`P(X \leq 4)`$:

From the table:

$$
P(X \leq 4) = \boxed{0.8153}
$$

---

### **4. Computing a Poisson Probability Over an Interval Using a CDF Table**

To compute $`P(a \leq X \leq b)`$, use:

$$
\boxed{P(a \leq X \leq b) = P(X \leq b) - P(X < a) = F(b; \lambda) - F(a - 1; \lambda)}
$$

#### **Example:**

Find $`P(2 \leq X \leq 4)`$ for $`\lambda = 3`$:

$$
P(2 \leq X \leq 4) = P(X \leq 4) - P(X \leq 1)
= 0.8153 - 0.1991 = \boxed{0.6162}
$$

---

### **5. Computing a Probability Over an Interval Containing a "Greater Than" Symbol**

For probabilities like $`P(X > k)`$, use the complement:

$$
\boxed{P(X > k) = 1 - P(X \leq k)}
$$

#### **Example:**

Find $`P(X > 3)`$ when $`\lambda = 2`$:

$$
P(X > 3) = 1 - P(X \leq 3) = 1 - 0.8571 = \boxed{0.1429}
$$

---

### ✅ **Summary Table**

| Task               | Formula                                                          |
| ------------------ | ---------------------------------------------------------------- |
| **CDF definition** | $`P(X \leq k) = \sum_{i=0}^{k} \frac{\lambda^i e^{-\lambda}}{i!}`$ |
| **Interval**       | $`P(a \leq X \leq b) = P(X \leq b) - P(X \leq a - 1)`$             |
| **Greater than**   | $`P(X > k) = 1 - P(X \leq k)`$                                     |
| **Using table**    | Look up $`F(k; \lambda)`$                                          |

---

### **Conclusion**

Using the **Poisson CDF** simplifies probability calculations over intervals, especially when combined with CDF tables. 
Whether you're analyzing call volumes, system failures, or rare events, the CDF enables efficient, accurate evaluation 
of **cumulative probabilities** in the Poisson framework.
