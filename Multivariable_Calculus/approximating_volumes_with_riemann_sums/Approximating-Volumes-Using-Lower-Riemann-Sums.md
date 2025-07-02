## **Approximating Volumes Using Lower Riemann Sums**

---

### **1. Overview of Lower Riemann Sums**

The **Lower Riemann Sum** is a method for approximating the **volume under a surface** (or area under a curve in 2D) by using the **minimum value** of the function over each subinterval of the domain. 
It provides an underestimate (lower bound) of the total integral when the function is nonnegative.

In one variable:

$$
L_n = \sum_{i=1}^n m_i \Delta x_i
$$

* $`m_i = \inf_{x \in [x_{i-1}, x_i]} f(x)`$
* $`\Delta x_i = x_i - x_{i-1}`$

In two variables, over a rectangular region:

$$
L_{m,n} = \sum_{i=1}^m \sum_{j=1}^n m_{ij} \Delta x \Delta y
$$

* where $`m_{ij} = \inf_{(x,y) \in R_{ij}} f(x, y)`$ over subrectangles $`R_{ij}`$

---

### **2. Calculating an Expression for the Lower Bounds**

Let $`f(x)`$ be defined on an interval $`[a, b]`$, and divide the interval into $n$ equal parts:

* Width: $`\Delta x = \frac{b - a}{n}`$
* Subintervals: $`[x_{i-1}, x_i]`$ where $`x_i = a + i\Delta x`$

The **lower Riemann sum** is then:

$$
L_n = \sum_{i=1}^n \min_{x \in [x_{i-1}, x_i]} f(x) \cdot \Delta x
$$

In the 2D case, for a function $`f(x,y)`$ over a region $`R = [a, b] \times [c, d]`$, divide into $m$ subintervals in $x$, and $n$ in $y$:

$$
\Delta x = \frac{b - a}{m}, \quad \Delta y = \frac{d - c}{n}
$$

Then:

$$
L_{m,n} = \sum_{i=1}^m \sum_{j=1}^n \left[ \inf_{(x,y) \in R_{ij}} f(x,y) \right] \cdot \Delta x \Delta y
$$

---

### **3. Calculating a Lower Riemann Sum for a Strictly Decreasing Function**

If $`f(x)`$ is **strictly decreasing** over $`[a, b]`$, then in each subinterval $`[x_{i-1}, x_i]`$, the minimum occurs at the **right endpoint** $x_i$. Hence:

$$
L_n = \sum_{i=1}^n f(x_i) \cdot \Delta x
$$

Example:
Let $`f(x) = 1 - x`$ over $`[0, 1]`$, $`n = 4`$

* $`\Delta x = 0.25`$
* Right endpoints: $`x_i = 0.25, 0.5, 0.75, 1`$
* $`f(x_i) = 0.75, 0.5, 0.25, 0`$

Then:

$$
L_4 = (0.75 + 0.5 + 0.25 + 0)(0.25) = 1.5 \cdot 0.25 = 0.375
$$

---

### **4. Calculating a Lower Riemann Sum for a Strictly Increasing Function**

If $`f(x)`$ is **strictly increasing** over $`[a, b]`$, then the minimum over each interval $`[x_{i-1}, x_i]`$ occurs at the **left endpoint** $`x_{i-1}`$:

$$
L_n = \sum_{i=1}^n f(x_{i-1}) \cdot \Delta x
$$

Example:
Let $`f(x) = x^2`$ over $`[0, 2]`$, $`n = 4`$

* $`\Delta x = 0.5`$
* Left endpoints: $`x_0 = 0, x_1 = 0.5, x_2 = 1, x_3 = 1.5`$
* $`f(x_{i-1}) = 0, 0.25, 1, 2.25`$

Then:

$$
L_4 = (0 + 0.25 + 1 + 2.25)(0.5) = 3.5 \cdot 0.5 = 1.75
$$

---

### **Summary Table**

| Scenario                   | Minimum at     | Formula                               |
| -------------------------- | -------------- | ------------------------------------- |
| General Function           | Local minimum  | $`\sum m_i \Delta x_i`$                 |
| Strictly Decreasing $f(x)$ | Right endpoint | $`\sum f(x_i) \Delta x`$                |
| Strictly Increasing $f(x)$ | Left endpoint  | $`\sum f(x_{i-1}) \Delta x`$            |
| 2D Region                  | Over subrect.  | $`\sum_{i,j} m_{ij} \Delta x \Delta y`$ |

Lower Riemann sums are foundational in understanding integration as area under a curve or volume under a surface, especially in early numerical approximation or theoretical proofs of integrability.
