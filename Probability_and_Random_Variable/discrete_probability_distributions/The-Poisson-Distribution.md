## **The Poisson Distribution**

The **Poisson distribution** models the number of times an event occurs in a **fixed interval** 
of time or space when events happen **independently** and at a **constant average rate**.

---

### **1. Definition and Formula**

If a random variable $X$ follows a **Poisson distribution** with mean (or rate) $\lambda$, then:

$$
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}, \quad \text{where } k = 0, 1, 2, \dots
$$

* $`\lambda`$: average number of occurrences in the interval
* $`k`$: number of actual occurrences
* $`e`$: Euler’s number ($\approx 2.718$)

---

### **2. Computing a Probability at a Point**

To find the probability of **exactly** $k$ occurrences:

$$
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}
$$

#### **Example:**

If $`\lambda = 4`$, compute $`P(X = 2)`$:

$$
P(X = 2) = \frac{4^2 e^{-4}}{2!} = \frac{16 e^{-4}}{2} = 8e^{-4}
$$

---

### **3. Computing a Probability Over a Bounded Interval: Lower Bound is Zero**

To find the probability that $X$ is **less than or equal to $k$**:

$$
P(X \leq k) = \sum_{i=0}^{k} \frac{\lambda^i e^{-\lambda}}{i!}
$$

#### **Example:**

$`P(X \leq 3)`$ when $`\lambda = 2`$:

$$
P(X \leq 3) = P(0) + P(1) + P(2) + P(3)
$$

---

### **4. Computing a Probability Over a Bounded Interval: Lower Bound is Not Zero**

To find $`P(a \leq X \leq b)`$, compute:

$$
P(a \leq X \leq b) = \sum_{k=a}^{b} \frac{\lambda^k e^{-\lambda}}{k!}
$$

#### **Example:**

For $`\lambda = 3`$, find $`P(2 \leq X \leq 4)`$:

$$
P(2 \leq X \leq 4) = P(2) + P(3) + P(4)
$$

---

### **5. Computing a Probability Over an Unbounded Interval Using the Complement**

For probabilities like $`P(X > k)`$, use the complement:

$$
P(X > k) = 1 - P(X \leq k) = 1 - \sum_{i=0}^{k} \frac{\lambda^i e^{-\lambda}}{i!}
$$

#### **Example:**

Find $`P(X > 5)`$ when $`\lambda = 2`$:

$$
P(X > 5) = 1 - \sum_{i=0}^{5} \frac{2^i e^{-2}}{i!}
$$

---

### ✅ **Summary Table**

| Task                 | Formula                                                |
| -------------------- | ------------------------------------------------------ |
| Point probability    | $P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}$         |
| $P(X \leq k)$        | $\sum_{i=0}^{k} \frac{\lambda^i e^{-\lambda}}{i!}$     |
| $P(a \leq X \leq b)$ | $\sum_{i=a}^{b} \frac{\lambda^i e^{-\lambda}}{i!}$     |
| $P(X > k)$           | $1 - \sum_{i=0}^{k} \frac{\lambda^i e^{-\lambda}}{i!}$ |

---

### **Conclusion**

The Poisson distribution is a powerful model for **discrete events** in fixed intervals. 
Understanding how to compute probabilities over different intervals—especially using complements 
and summations—is essential in fields like queuing theory, reliability engineering, and machine learning.
