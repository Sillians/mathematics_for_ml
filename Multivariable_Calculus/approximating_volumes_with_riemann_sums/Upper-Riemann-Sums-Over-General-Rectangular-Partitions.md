## **Upper Riemann Sums Over General Rectangular Partitions**

---

### **1. Introduction to Upper Riemann Sums**

An **Upper Riemann Sum** approximates the area under a function over a region by overestimating the function's value on each subrectangle. 
It’s particularly useful in determining whether a function is Riemann integrable over a domain.

Given a bounded function $`f(x, y)`$ defined on a closed rectangle $`R = [a, b] \times [c, d]`$, and a partition of $R$ into smaller rectangles:

* Divide $`[a, b]`$ into $m$ subintervals.
* Divide $`[c, d]`$ into $n$ subintervals.
* Let $`R_{ij}`$ denote the rectangle formed by the $i$-th subinterval in $x$ and $j$-th in $y$.

Then, the **Upper Riemann Sum** is defined as:

$$
U(f, P) = \sum_{i=1}^{m} \sum_{j=1}^{n} M_{ij} \cdot \Delta x_i \cdot \Delta y_j
$$

Where:

* $`M_{ij} = \sup \{ f(x, y) : (x, y) \in R_{ij} \}`$ is the **supremum (maximum)** of $f$ on the subrectangle $`R_{ij}`$,
* $`\Delta x_i = x_i - x_{i-1}`$, width of subinterval in $x$,
* $`\Delta y_j = y_j - y_{j-1}`$, height of subinterval in $y$.

---

### **2. Writing an Upper Riemann Sum for a Strictly Increasing Function**

Let $f(x)$ be strictly increasing on interval $`[a, b]`$, and suppose it is partitioned into subintervals $`x_0 < x_1 < \dots < x_n`$.

In each subinterval $`[x_{i-1}, x_i]`$, the maximum value of $f$ occurs at the **right endpoint**, so:

$$
U(f, P) = \sum_{i=1}^{n} f(x_i) \cdot \Delta x_i
$$

For multivariable functions $`f(x, y)`$ that are strictly increasing in both variables, the supremum on each subrectangle occurs at the **top-right corner**:

$$
U(f, P) = \sum_{i=1}^{m} \sum_{j=1}^{n} f(x_i, y_j) \cdot \Delta x_i \cdot \Delta y_j
$$

---

### **3. Writing an Upper Riemann Sum for a Strictly Decreasing Function**

Let $f(x)$ be strictly decreasing on $`[a, b]`$. Then, the maximum value on subinterval $`[x_{i-1}, x_i]`$ is at the **left endpoint**, so:

$$
U(f, P) = \sum_{i=1}^{n} f(x_{i-1}) \cdot \Delta x_i
$$

For functions $`f(x, y)`$ strictly decreasing in both $x$ and $y$, the supremum on each $R_{ij}$ is found at the **bottom-left corner**:

$$
U(f, P) = \sum_{i=1}^{m} \sum_{j=1}^{n} f(x_{i-1}, y_{j-1}) \cdot \Delta x_i \cdot \Delta y_j
$$

---

### **4. Writing an Upper Riemann Sum for a Function That’s Neither Strictly Increasing nor Decreasing**

If $`f(x, y)`$ has no strict monotonicity, the maximum on each subrectangle $`R_{ij}`$ must be **calculated or estimated directly**:

$$
U(f, P) = \sum_{i=1}^{m} \sum_{j=1}^{n} \left[ \sup_{(x, y) \in R_{ij}} f(x, y) \right] \cdot \Delta x_i \cdot \Delta y_j
$$

This supremum could occur at:

* An interior point,
* A boundary,
* Or a corner.

In such cases, numerical methods (sampling or symbolic maximization) may be used to estimate each $`M_{ij}`$.

---

### **5. Summary Table**

| **Function Type**               | **Location of Supremum $M_{ij}$**                | **Upper Sum Expression**                                            |
|---------------------------------|--------------------------------------------------|---------------------------------------------------------------------|
| Strictly Increasing in $`x, y`$ | Top-right corner of $`R_{ij}$: $(x_i, y_j)`$     | $`\sum f(x_i, y_j) \cdot \Delta x_i \cdot \Delta y_j`$              |
| Strictly Decreasing in $`x, y`$ | Bottom-left corner: $`(x_{i-1}, y_{j-1})`$       | $`\sum f(x_{i-1}, y_{j-1}) \cdot \Delta x_i \cdot \Delta y_j`$      |
| Neither Increasing nor Decreasing | Supremum over each $`R_{ij}$                     | $`\sum \sup_{R_{ij}} f(x, y) \cdot \Delta x_i \cdot \Delta y_j`$    |

---

### **6. Importance of Upper Riemann Sums**

Upper and Lower Riemann sums help verify **Riemann integrability**. If the difference between upper and lower sums can be made arbitrarily 
small as the partition is refined, then:


$$
\lim_{\|\mathcal{P}\| \to 0} U(f, \mathcal{P}) = \lim_{\|\mathcal{P}\| \to 0} L(f, \mathcal{P}) = \iint_R f(x, y)\,dx\,dy
$$

---
