## **Approximating Volumes Using Upper Riemann Sums**

---

### **1. Overview of Upper Riemann Sums**

The **Upper Riemann Sum** is a method for approximating the **volume under a surface** (or area under a curve 
in 2D) by using the **maximum value** of the function over each subinterval. It gives an **overestimate 
(upper bound)** for the total integral when the function is nonnegative.

In 1D:

$$
U_n = \sum_{i=1}^n M_i \Delta x_i
\quad \text{where} \quad M_i = \sup_{x \in [x_{i-1}, x_i]} f(x)
$$

In 2D:

$$
U_{m,n} = \sum_{i=1}^m \sum_{j=1}^n M_{ij} \Delta x \Delta y
\quad \text{where} \quad M_{ij} = \sup_{(x,y) \in R_{ij}} f(x,y)
$$

---

### **2. Calculating an Expression for the Upper Bound in Terms of Maximum Values**

Let $`f(x)`$ be continuous on $`[a, b]`$ and partitioned into $n$ subintervals of equal width:

* $`\Delta x = \frac{b - a}{n}`$
* Subintervals: $`[x_{i-1}, x_i]`$

Then the **Upper Riemann Sum** is:

$$
U_n = \sum_{i=1}^n \max_{x \in [x_{i-1}, x_i]} f(x) \cdot \Delta x
$$

For 2D functions over a rectangular region $`R = [a,b] \times [c,d]`$ partitioned into $m$ subintervals in $x$, and $n$ in $y$:

* $`\Delta x = \frac{b - a}{m}, \quad \Delta y = \frac{d - c}{n}`$

$$
U_{m,n} = \sum_{i=1}^m \sum_{j=1}^n \left[ \sup_{(x,y) \in R_{ij}} f(x,y) \right] \cdot \Delta x \Delta y
$$

---

### **3. Calculating an Upper Riemann Sum for a Strictly Decreasing Function**

If $`f(x)`$ is **strictly decreasing** over $`[a,b]`$, the maximum on $`[x_{i-1}, x_i]`$ occurs at the **left endpoint** $`x_{i-1}`$:

$$
U_n = \sum_{i=1}^n f(x_{i-1}) \cdot \Delta x
$$

**Example**:
Let $`f(x) = 1 - x`$ on $`[0,1]`$, divide into $`n = 4`$ equal parts.

* $`\Delta x = 0.25`$
* Left endpoints: $`x_{i-1} = 0, 0.25, 0.5, 0.75`$
* $`f(x_{i-1}) = 1, 0.75, 0.5, 0.25`$

Then:

$$
U_4 = (1 + 0.75 + 0.5 + 0.25)(0.25) = 2.5 \cdot 0.25 = 0.625
$$

---

### **4. Calculating an Upper Riemann Sum for a Strictly Increasing Function**

If $`f(x)`$ is **strictly increasing** on $`[a,b]`$, the maximum on each subinterval $`[x_{i-1}, x_i]`$ occurs at the **right endpoint** $x_i$:

$$
U_n = \sum_{i=1}^n f(x_i) \cdot \Delta x
$$

**Example**:
Let $`f(x) = x^2`$ on $`[0,2]`$, with $`n = 4`$ subintervals.

* $`\Delta x = 0.5`$
* Right endpoints: $`x_i = 0.5, 1, 1.5, 2`$
* $`f(x_i) = 0.25, 1, 2.25, 4`$

Then:

$$
U_4 = (0.25 + 1 + 2.25 + 4)(0.5) = 7.5 \cdot 0.5 = 3.75
$$

---

### **Summary Table**

| Function Type       | Maximum at     | Upper Riemann Sum Formula             |
| ------------------- | -------------- | ------------------------------------- |
| General Function    | Local max      | $`\sum M_i \Delta x_i`$                 |
| Strictly Decreasing | Left endpoint  | $`\sum f(x_{i-1}) \Delta x`$            |
| Strictly Increasing | Right endpoint | $`\sum f(x_i) \Delta x`$                |
| 2D Region           | Subrectangle   | $`\sum_{i,j} M_{ij} \Delta x \Delta y`$ |

---

Upper Riemann sums serve as overestimates for definite integrals and are critical in numerical approximation,
bounding errors, and establishing integrability in Riemann theory.
