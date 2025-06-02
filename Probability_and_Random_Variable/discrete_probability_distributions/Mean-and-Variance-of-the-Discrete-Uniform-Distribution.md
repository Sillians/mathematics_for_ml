## **Mean and Variance of the Discrete Uniform Distribution**

---

### **1. Definition**

A **Discrete Uniform Distribution** assigns equal probability to each value in a finite set of integers.
If a random variable $`X`$ takes values in the set

$$
\{a, a+1, a+2, \dots, b\}
$$

where $`a, b \in \mathbb{Z}`$ and $`a < b`$, then the total number of values is

$$
n = b - a + 1
$$

and for each $`x \in \{a, a+1, \dots, b\}`$,

$$
P(X = x) = \frac{1}{n}
$$

---

### **2. Mean (Expected Value)**

The mean of a discrete uniform distribution is:

$$
\mathbb{E}[X] = \mu = \frac{a + b}{2}
$$

This is simply the **arithmetic average** of the smallest and largest values.

---

### **3. Variance**

The variance of $`X \sim \text{Uniform}(a, b)`$ is:

$$
\text{Var}(X) = \frac{(b - a + 1)^2 - 1}{12}
$$

This formula arises from computing the second moment and subtracting the square of the mean:

$$
\text{Var}(X) = \mathbb{E}[X^2] - \mu^2
$$

---

### **4. Computing Mean Values in Context**

#### **Example 1:**

Suppose $`X \sim \text{Uniform}(1, 10)`$. Then:

* $`a = 1`$, $`b = 10`$
* $`\mu = \frac{1 + 10}{2} = 5.5`$

Interpretation: On average, the expected value of a fair draw from 1 to 10 is 5.5.

---

### **5. Computing Variances in Context**

#### **Example 2:**

Using the same $`X \sim \text{Uniform}(1, 10)`$:

* $`b - a + 1 = 10`$
* Variance:

$$
\text{Var}(X) = \frac{10^2 - 1}{12} = \frac{99}{12} = 8.25
$$

Interpretation: The average squared deviation from the mean in this uniform range is 8.25.

---

### **6. Summary**

| Property | Formula                                   |
| -------- | ----------------------------------------- |
| Mean     | $`\mu = \frac{a + b}{2}`$                   |
| Variance | $`\sigma^2 = \frac{(b - a + 1)^2 - 1}{12}`$ |

These properties help characterize symmetric discrete distributions with finite support and equal probabilities.
