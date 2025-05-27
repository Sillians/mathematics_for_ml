## **Partitions of Intervals**

---

### **1. What Is a Partition of an Interval?**

A **partition** of an interval is a way to divide a closed interval on the real number line into smaller subintervals.

Let $`[a, b]`$ be a closed interval. A **partition** $P$ of $`[a, b]`$ is a finite ordered set:

$$
P = \{ x_0, x_1, x_2, \ldots, x_n \}
$$

such that:

* $`a = x_0 < x_1 < x_2 < \ldots < x_n = b`$
* Each $`[x_{i-1}, x_i]`$ is a **subinterval** of $`[a, b]`$

These subintervals form the basis for **Riemann sums** and other analytical computations.

---

### **2. Identifying Partitions of the Real Line**

In theory, you **cannot partition the entire real line** $`\mathbb{R}`$ into a finite number of subintervals, but you *can*:

* Partition **bounded intervals** like $[a, b]$
* Or use **countable partitions** to divide $`\mathbb{R}`$ into infinite pieces like $`(-\infty, -1], (-1, 0], (0, 1], (1, \infty)`$

**Examples**:

* Partition of $`[0, 1]`$: $`\{0, \frac{1}{3}, \frac{2}{3}, 1\}`$
* Partition of $`\mathbb{R}`$: $`\{\ldots, [-2, -1], [-1, 0], [0, 1], [1, 2], \ldots \}`$

---

### **3. Computing Simple Sums Over Partitions**

Given a partition $`P = \{x_0, x_1, \ldots, x_n\}`$ of $`[a, b]`$ and a function $f$, 
we can compute **simple sums** such as:

* **Right-endpoint sum**:

$$
\sum_{i=1}^n f(x_i) \Delta x_i, \quad \text{where } \Delta x_i = x_i - x_{i-1}
$$

* **Left-endpoint sum**:

$$
\sum_{i=1}^n f(x_{i-1}) \Delta x_i
$$

* **Midpoint sum**:

$$
\sum_{i=1}^n f\left( \frac{x_{i-1} + x_i}{2} \right) \Delta x_i
$$

These are the basis for approximating integrals.

---

### **4. Computing Sums Over Partitions of the Real Line**

If we break up a function over the **entire real line**, we use **infinite partitions**. For example:

Let $`f(x) = \frac{1}{1 + x^2}`$, and partition $`\mathbb{R}`$ into unit intervals:

$$
\sum_{k = -\infty}^\infty \int_k^{k+1} \frac{1}{1 + x^2} dx
$$

This sum converges due to the decay of $`\frac{1}{1 + x^2}`$, and its total integral is:

$$
\int_{-\infty}^\infty \frac{1}{1 + x^2} dx = \pi
$$

---

### **Summary**

| Concept                   | Key Idea                                                  |
| ------------------------- | --------------------------------------------------------- |
| Partition of $`[a, b]`$     | Divide into finite subintervals with increasing endpoints |
| Partition of $`\mathbb{R}`$ | Use countable or infinite intervals                       |
| Simple sum                | Finite sum over subintervals using function values        |
| Real line sum             | Infinite sum of integrals over countable partitions       |

These tools are foundational in real analysis, numerical integration, and measure theory.
