## **Lower Riemann Sums Over General Rectangular Partitions**

---

### **1. Overview: Riemann Sums in Two Dimensions**

In two-variable integration, a **Riemann sum** approximates the double integral of a function $`f(x, y)`$ 
over a rectangular region $`R = [a, b] \times [c, d]`$. A **lower Riemann sum** underestimates the integral
by using the **minimum value** of $f$ over each subrectangle.

---

### **2. Partitioning the Rectangle**

Let:

* Divide $`[a, b]`$ into $m$ subintervals with $x$-coordinates $`a = x_0 < x_1 < \dots < x_m = b`$
* Divide $`[c, d]`$ into $n$ subintervals with $y$-coordinates $`c = y_0 < y_1 < \dots < y_n = d`$

Then $R$ is partitioned into $`m \times n`$ **rectangles**:

$$
R_{ij} = [x_{i-1}, x_i] \times [y_{j-1}, y_j]
\quad \text{for } 1 \le i \le m,\ 1 \le j \le n
$$

Let the **area** of each rectangle be:

$$
\Delta A_{ij} = (x_i - x_{i-1})(y_j - y_{j-1})
$$

---

### **3. General Formula for the Lower Riemann Sum**

Let:

* $`m_{ij} = \inf\{ f(x, y) : (x, y) \in R_{ij} \}`$

Then the **lower Riemann sum** is:

$$
L(f, \mathcal{P}) = \sum_{i=1}^{m} \sum_{j=1}^{n} m_{ij} \cdot \Delta A_{ij}
$$

This is a weighted sum of **infimum values** times **area elements**, giving an **underestimate** of the exact double integral:

$$
L(f, \mathcal{P}) \leq \iint_R f(x, y)\,dA
$$

---

### **4. Writing the Lower Riemann Sum for Different Behaviors**

---

#### **A. Strictly Increasing Function**

Assume $`f(x, y)`$ increases in both $x$ and $y$.

Then over rectangle $`R_{ij}`$, the **minimum value** occurs at the **lower-left corner**:

$$
m_{ij} = f(x_{i-1}, y_{j-1})
$$

So the lower sum becomes:

$$
L(f, \mathcal{P}) = \sum_{i=1}^{m} \sum_{j=1}^{n} f(x_{i-1}, y_{j-1}) \cdot \Delta A_{ij}
$$

---

#### **B. Strictly Decreasing Function**

Assume $`f(x, y)`$ decreases in both $x$ and $y$.

Then the **minimum** on each rectangle occurs at the **upper-right corner**:

$$
m_{ij} = f(x_i, y_j)
$$

So the lower sum becomes:

$$
L(f, \mathcal{P}) = \sum_{i=1}^{m} \sum_{j=1}^{n} f(x_i, y_j) \cdot \Delta A_{ij}
$$

---

#### **C. Function Neither Increasing Nor Decreasing**

If $`f(x, y)`$ varies irregularly, then:

$$
m_{ij} = \min \{ f(x, y) \mid (x, y) \in R_{ij} \}
$$

We typically:

* Pick sample points $`(x^*_{ij}, y^*_{ij}) \in R_{ij}`$
* Estimate $`m_{ij} \approx f(x^*_{ij}, y^*_{ij})`$, where $`f(x^*_{ij}, y^*_{ij})`$ is the **minimum** value among corners or sampled points within each subrectangle

Hence:

$$
L(f, \mathcal{P}) \approx \sum_{i=1}^{m} \sum_{j=1}^{n} f(x^*_{ij}, y^*_{ij}) \cdot \Delta A_{ij}
$$

This form must be **adapted** based on available knowledge about $f$ in each region.

---

### **5. Visual Intuition**

* Each term in the sum represents a "box" with height equal to the **smallest** value of $f$ over the rectangle.
* For increasing functions, the "boxes" hug the **lower-left** of each subrectangle.
* For decreasing functions, they hug the **upper-right**.

This results in a **"stepped surface"** under the actual graph of $f(x, y)$, underestimating the volume.

---

### **6. Summary Table**

| Function Behavior                   | Minimum Point                        | Lower Riemann Sum Term                               |
|-------------------------------------|--------------------------------------| ---------------------------------------------------- |
| Strictly increasing in $`x, y`$     | $`(x_{i-1}, y_{j-1})`$               | $`f(x_{i-1}, y_{j-1}) \cdot \Delta A_{ij}`$            |
| Strictly decreasing in $`x, y`$     | $`(x_i, y_j)`$                       | $`f(x_i, y_j) \cdot \Delta A_{ij}`$                    |
| Neither increasing nor decreasing   | Unknown (choose minimum over region) | $`m_{ij} \cdot \Delta A_{ij}`$, estimated via sampling |

---

### **7. Applications and Importance**

* **Lower Riemann sums** give underapproximations useful for **bounds** in numerical integration.
* Essential in defining **Riemann integrability**: if lower and upper sums converge as partition gets finer.
* Used in early stages of **integration theory** and **computational geometry**.

---

The **lower Riemann sum** framework builds foundational intuition for surface area under multivariable 
functions and is a stepping stone to more advanced integration techniques like iterated integrals, 
Fubini’s theorem, and measure theory.
