## **Normal Approximations of Binomial Distributions**

The **normal approximation** to the **binomial distribution** is a powerful technique used to simplify binomial probability calculations when the number of
trials is large. Instead of working directly with discrete probabilities, we use a **continuous normal distribution** to estimate binomial probabilities.

---

###  1. **Identifying Situations Where a Normal Approximation is Appropriate**

A normal approximation to a binomial distribution is appropriate when:

* The number of trials $`n`$ is **large**
* The probability $`p`$ is **not too close to 0 or 1**

✅ **Rule of Thumb**:

$$
np \geq 5 \quad \text{and} \quad n(1 - p) \geq 5
$$

If both conditions are met, the binomial distribution is roughly symmetric, and the normal approximation is generally accurate.

---

###  2. **Using a Normal Approximation to Approximate a Binomial Probability**

Let $`X \sim \text{Binomial}(n, p)`$. Then:

* Mean: $`\mu = np`$
* Standard deviation: $`\sigma = \sqrt{np(1 - p)}`$

We approximate $`X`$ with a **normal distribution**:

$$
X \approx \mathcal{N}(np, np(1 - p))
$$

Since binomial is **discrete** and normal is **continuous**, we apply a **continuity correction** by adjusting the value by **±0.5**.

---

#### ✅ **Example**:

Find $`P(X = k)`$ using the normal approximation:

$$
P(X = k) \approx P(k - 0.5 < Y < k + 0.5)
$$

Where $`Y \sim \mathcal{N}(np, np(1 - p))`$

---

### 3. **Using a Normal Approximation to Approximate a Binomial Probability Over an Interval**

To approximate a binomial probability over an interval $`a \leq X \leq b`$:

$$
P(a \leq X \leq b) \approx P(a - 0.5 < Y < b + 0.5)
$$

Convert to standard normal:

$$
z_1 = \frac{a - 0.5 - \mu}{\sigma}, \quad z_2 = \frac{b + 0.5 - \mu}{\sigma}
$$

Then:

$$
P(a \leq X \leq b) \approx P(z_1 < Z < z_2)
$$

Use the **standard normal table** to compute this.

---

### ✅ **Summary Table**

| Type                 | Binomial Expression | Normal Approximation       |
| -------------------- | ------------------- | -------------------------- |
| $`P(X = k)`$           | Discrete point      | $`P(k - 0.5 < Y < k + 0.5)`$ |
| $`P(X \leq k)`$        | Cumulative          | $`P(Y < k + 0.5)`$           |
| $`P(X \geq k)`$        | Upper tail          | $`P(Y > k - 0.5)`$           |
| $`P(a \leq X \leq b)`$ | Interval            | $`P(a - 0.5 < Y < b + 0.5)`$ |

---

### **Conclusion**

Normal approximation allows you to simplify binomial probability problems when the sample size is large and the binomial distribution is symmetric enough. 
Always remember to check for conditions and apply **continuity correction** for best accuracy.
