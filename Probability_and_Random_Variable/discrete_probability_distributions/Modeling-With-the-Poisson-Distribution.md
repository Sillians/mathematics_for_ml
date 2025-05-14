## **Modeling with the Poisson Distribution**

The **Poisson distribution** is a powerful tool used to model the number of times an event occurs in a **fixed interval** of time, 
area, volume, or any other continuous domain, under the assumptions that events occur:

1. **Independently** of each other
2. At a **constant average rate**
3. Not simultaneously (i.e., events happen one at a time)

---

### **1. Identifying Random Variables That Follow a Poisson Distribution**

A random variable $X$ follows a **Poisson distribution** if it models the **number of occurrences** of an event in a fixed interval and satisfies the assumptions above.

#### **Typical examples:**

* Number of emails received per hour
* Number of decay events per second in radioactive material
* Number of phone calls to a call center per minute
* Number of typos on a page of a book

If the **average rate $`\lambda`$** of occurrence is known, and the variance roughly matches the mean, it likely follows a Poisson distribution.

---

### **2. Computing the Probability of a Poisson Random Variable at Some Value**

Given $`X \sim \text{Poisson}(\lambda)`$, the **probability of observing exactly $k$ events** is given by:

$$
\boxed{P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}}, \quad k = 0, 1, 2, \dots
$$

#### **Example:**

If a store receives 4 customers per hour on average ($\lambda = 4$), what is the probability exactly 2 customers arrive in an hour?

$$
P(X = 2) = \frac{4^2 e^{-4}}{2!} = \frac{16 e^{-4}}{2} = 8e^{-4}
\approx 0.1465
$$

---

### **3. Computing the Probability of a Poisson Random Variable on a Bounded Interval**

For a range $`[a, b]`$, compute:

$$
\boxed{P(a \leq X \leq b) = \sum_{k=a}^{b} \frac{\lambda^k e^{-\lambda}}{k!}}
$$

#### **Example:**

Find the probability of receiving between 2 and 4 emails in an hour, when $`\lambda = 3`$:

$$
P(2 \leq X \leq 4) = P(2) + P(3) + P(4)
= \sum_{k=2}^{4} \frac{3^k e^{-3}}{k!}
$$

---

### **4. Computing the Probability of a Poisson Random Variable on an Unbounded Interval**

To compute a probability over an **unbounded range**, such as $P(X > k)$, use the **complement rule**:

$$
\boxed{P(X > k) = 1 - \sum_{i=0}^{k} \frac{\lambda^i e^{-\lambda}}{i!}}
$$

#### **Example:**

If $`\lambda = 5`$, find $`P(X > 7)`$:

$$
P(X > 7) = 1 - P(X \leq 7) = 1 - \sum_{i=0}^{7} \frac{5^i e^{-5}}{i!}
$$

This is easier to compute using cumulative distribution tables or software (e.g., Python, R, calculator).

---

### ✅ **Summary Table**

| Task                               | Formula                                                                |
| ---------------------------------- | ---------------------------------------------------------------------- |
| **Point probability**              | $`P(X = k) = \dfrac{\lambda^k e^{-\lambda}}{k!}`$                        |
| **Bounded interval**               | $`\sum_{k=a}^{b} \dfrac{\lambda^k e^{-\lambda}}{k!}`$                    |
| **Unbounded interval**             | $`P(X > k) = 1 - \sum_{i=0}^{k} \dfrac{\lambda^i e^{-\lambda}}{i!}`$     |
| **Random variable identification** | Matches Poisson conditions: constant rate, independence, one-at-a-time |

---

### **Conclusion**

The Poisson distribution is ideal for **modeling discrete events** in continuous settings when the average rate is constant.
Whether calculating the probability of a specific count or modeling rare events across time or space, mastering its 
structure is essential in statistics, machine learning, and operational research.
