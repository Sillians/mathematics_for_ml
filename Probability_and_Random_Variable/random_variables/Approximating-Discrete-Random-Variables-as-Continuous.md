## **Approximating Discrete Random Variables as Continuous**

In practice, **discrete distributions** (like the Binomial or Poisson) are sometimes approximated using **continuous distributions** 
(like the Normal) for ease of computation, especially when dealing with large samples or when exact probabilities are difficult to compute.

This approach is known as the **continuity correction** and often involves the **Normal approximation** to a discrete distribution.

---

### **When to Approximate**

A discrete random variable $X$ (e.g., Binomial or Poisson) can be approximated by a continuous distribution when:

* The sample size is **large**, and
* The distribution of $`X`$ is **approximately symmetric**

#### Common Example:

* $`X \sim \text{Binomial}(n, p)`$ can be approximated by $`Y \sim \mathcal{N}(np, np(1 - p))`$

Use a **continuity correction** by adding or subtracting **0.5** when translating between discrete and continuous forms.

---

### **1. Approximating a Probability at a Single Point**

To approximate $`P(X = k)`$, use:

$$
P(X = k) \approx P(k - 0.5 < Y < k + 0.5)
$$

Where $`Y`$ is the continuous approximation of $`X`$ (typically Normal).

#### **Example:**

If $`X \sim \text{Binomial}(100, 0.5)`$, approximate $`P(X = 50)`$:

* Mean: $`\mu = 50`$, Standard deviation: $`\sigma = 5`$
* Use $`Y \sim \mathcal{N}(50, 5^2)`$

Then:

$$
P(X = 50) \approx P(49.5 < Y < 50.5) = \Phi\left(\frac{50.5 - 50}{5}\right) - \Phi\left(\frac{49.5 - 50}{5}\right)
= \Phi(0.1) - \Phi(-0.1) \approx 0.5398 - 0.4602 = \boxed{0.0796}
$$

---

### **2. Approximating a Probability Over an Interval**

To approximate $`P(a \leq X \leq b)`$, apply the continuity correction:

$$
P(a \leq X \leq b) \approx P(a - 0.5 < Y < b + 0.5)
$$

#### **Example:**

Approximate $`P(45 \leq X \leq 55)`$ for the same $`X \sim \text{Binomial}(100, 0.5)`$:

$$
P(45 \leq X \leq 55) \approx P(44.5 < Y < 55.5)
$$

$$
= \Phi\left(\frac{55.5 - 50}{5}\right) - \Phi\left(\frac{44.5 - 50}{5}\right)
= \Phi(1.1) - \Phi(-1.1) \approx 0.8643 - 0.1357 = \boxed{0.7286}
$$

---

### **3. Approximating a Probability Over an Unbounded Interval**

For $`P(X > k)`$, approximate using:

$$
P(X > k) \approx P(Y > k + 0.5)
$$

Similarly, for $`P(X < k)`$:

$$
P(X < k) \approx P(Y < k - 0.5)
$$

#### **Example:**

Approximate $`P(X > 60)`$ for $`X \sim \text{Binomial}(100, 0.5)`$:

$$
P(X > 60) \approx P(Y > 60.5) = 1 - \Phi\left(\frac{60.5 - 50}{5}\right)
= 1 - \Phi(2.1) \approx 1 - 0.9821 = \boxed{0.0179}
$$

---

### ✅ Summary Table

| Discrete Probability | Continuous Approximation with Correction |
| -------------------- | ---------------------------------------- |
| $`P(X = k)`$           | $`P(k - 0.5 < Y < k + 0.5)`$               |
| $`P(a \leq X \leq b)`$ | $`P(a - 0.5 < Y < b + 0.5)`$               |
| $`P(X > k)`$           | $`P(Y > k + 0.5)`$                         |
| $`P(X < k)`$           | $`P(Y < k - 0.5)`$                         |

---

### **Conclusion**

Approximating discrete distributions with continuous ones (especially the Normal) provides a powerful tool for estimating probabilities when exact 
methods are cumbersome. By applying a **continuity correction**, the approximation becomes more accurate, preserving the integrity of the discrete 
outcomes within the continuous framework.
