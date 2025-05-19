## **The Exponential Distribution**

The **Exponential distribution** is a continuous probability distribution that models the time 
between independent events occurring at a **constant average rate**. It is widely used 
in **queueing theory**, **reliability engineering**, and **Poisson processes**.

---

### **Definition**

A continuous random variable $`X \sim \text{Exponential}(\lambda)`$ has:

* **PDF**:

$$
f(x) = 
\begin{cases}
\lambda e^{-\lambda x}, & x \geq 0 \\
0, & x < 0
\end{cases}
$$

* **CDF**:

$$
F(x) = P(X \leq x) = 1 - e^{-\lambda x}, \quad x \geq 0
$$

* **Mean**: $`\frac{1}{\lambda}`$

* **Memoryless Property**:

$$
P(X > s + t \mid X > s) = P(X > t)
$$

---

### **1. Computing a "Less Than" Probability**

To compute $`P(X < a)`$:

$$
P(X < a) = F(a) = 1 - e^{-\lambda a}
$$

#### **Example:**

If $`X \sim \text{Exponential}(2)`$, find $`P(X < 1)`$:

$$
P(X < 1) = 1 - e^{-2(1)} = 1 - e^{-2} \approx \boxed{0.8647}
$$

---

### **2. Computing a "Greater Than" Probability**

To compute $`P(X > a)`$:

$$
P(X > a) = 1 - F(a) = e^{-\lambda a}
$$

#### **Example:**

For $`X \sim \text{Exponential}(3)`$, find $`P(X > 2)`$:

$$
P(X > 2) = e^{-3(2)} = e^{-6} \approx \boxed{0.0025}
$$

---

### **3. Computing a Probability on a Bounded Interval**

To find $`P(a \leq X \leq b)`$:

$$
P(a \leq X \leq b) = F(b) - F(a) = \left(1 - e^{-\lambda b}\right) - \left(1 - e^{-\lambda a}\right)
= e^{-\lambda a} - e^{-\lambda b}
$$

#### **Example:**

Let $`X \sim \text{Exponential}(1.5)`$, find $`P(1 \leq X \leq 3)`$:

$$
P(1 \leq X \leq 3) = e^{-1.5(1)} - e^{-1.5(3)} = e^{-1.5} - e^{-4.5} \approx 0.2231 - 0.0111 = \boxed{0.212}
$$

---

### **4. Calculating Probabilities Using the Memoryless Property**

The Exponential distribution is **memoryless**, meaning:

$$
P(X > s + t \mid X > s) = P(X > t)
$$

This implies that **future waiting time is independent of how long you've already waited**.

#### **Example:**

If a component has an exponential lifetime with $`\lambda = 0.1`$, and it has already lasted 5 hours,
the probability it lasts another 3 hours is:

$$
P(X > 8 \mid X > 5) = P(X > 3) = e^{-0.1 \cdot 3} = \boxed{e^{-0.3} \approx 0.7408}
$$

---

### ✅ **Summary Table**

| Type                 | Formula                              |
| -------------------- | ------------------------------------ |
| $`P(X < a)`$           | $`1 - e^{-\lambda a}`$                 |
| $`P(X > a)`$           | $`e^{-\lambda a}`$                     |
| $`P(a \leq X \leq b)`$ | $`e^{-\lambda a} - e^{-\lambda b}`$    |
| **Memoryless**       | $`P(X > s + t \mid X > s) = P(X > t)`$ |

---

### **Conclusion**

The **Exponential distribution** is essential for modeling **time-to-event** problems where the 
event rate is constant. It's elegant PDF, straightforward probabilities, and **memoryless property** 
make it one of the most powerful tools in probability and applied statistics.
