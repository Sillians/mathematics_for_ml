## **The Discrete Uniform Distribution**

---

### **1. Definition**

A **discrete uniform distribution** assigns **equal probability** to all values in a finite set of distinct outcomes.

If a random variable $X$ takes values in the set $`\{x_1, x_2, \dots, x_n\}`$, and all are equally likely, then:

$$
P(X = x_i) = \frac{1}{n}, \quad \text{for } i = 1, 2, \dots, n
$$

---

### **2. Properties**

* All outcomes are equally likely.
* The support set is finite and discrete.
* Mean:

$$
\mu = \frac{a + b}{2}
$$

* Variance:

$$
\sigma^2 = \frac{(b - a + 1)^2 - 1}{12}
$$

where $`X \in \{a, a+1, \dots, b\}`$

---

### **3. Computing a Probability at a Single Point**

Since each value has equal likelihood:

$$
P(X = x) = \frac{1}{n}
$$

**Example:**
If $`X \sim \text{Uniform}(\{1, 2, 3, 4, 5\})`$, then:

$$
P(X = 3) = \frac{1}{5}
$$

---

### **4. Computing a Probability on a Bounded Interval**

For an interval $`[a, b] \subseteq \{x_1, x_2, \dots, x_n\}`$:

$$
P(a \leq X \leq b) = \frac{\text{Number of values from } a \text{ to } b}{n}
$$

**Example:**
If $`X \sim \text{Uniform}(1, 10)`$, then:

$$
P(3 \leq X \leq 6) = \frac{6 - 3 + 1}{10} = \frac{4}{10} = 0.4
$$

---

### **5. Computing a Probability on an Unbounded Interval**

For intervals like $`X > k`$ or $`X < k`$:

* $`P(X > k) = \frac{\text{Number of values greater than } k}{n}`$
* $`P(X < k) = \frac{\text{Number of values less than } k}{n}`$

**Example:**
If $`X \sim \text{Uniform}(1, 5)`$, then:

$$
P(X > 2) = \frac{3}{5} \quad \text{(i.e., values 3, 4, 5)}
$$

---

### ✅ **Summary**

| Task                           | Formula / Approach                         |
| ------------------------------ | ------------------------------------------ |
| **Single Point**               | $`P(X = x) = \frac{1}{n}`$                   |
| **Bounded Interval** $`[a, b]`$  | $`P(a \leq X \leq b) = \frac{b - a + 1}{n}`$ |
| **Unbounded Interval** $`X > k`$ | $`P(X > k) = \frac{\#\text{values > }k}{n}`$ |

The discrete uniform distribution is foundational in modeling equally likely outcomes, such as dice rolls, lottery draws, and randomized selections.
