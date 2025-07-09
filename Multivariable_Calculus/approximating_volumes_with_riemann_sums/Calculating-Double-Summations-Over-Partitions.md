## **Calculating Double Summations Over Partitions**

---

### **1. Overview: Double Summations and Partitions**

In multivariable calculus, a **double summation** is used to approximate or compute values over a two-dimensional region, 
often in preparation for evaluating a **double integral**. A **partition** divides a domain 
(usually rectangular) into smaller subregions where the function can be approximated or analyzed.


If a function is defined over a rectangle $`R = [a, b] \times [c, d]`$, we partition it into smaller 
rectangles using subdivisions in the $x$ and $y$ directions and compute the sum over all subrectangles.

---

### **2. Double Summation Over a Rectangular Partition**

#### **Setup**

Let:

* $m$: number of subintervals in the $x$-direction


* $n$: number of subintervals in the $y$-direction


* $`\Delta x = \frac{b - a}{m}`$, $`\Delta y = \frac{d - c}{n}`$: widths of subintervals


* $`x_i = a + i\Delta x`$, $`y_j = c + j\Delta y`$


* $`f(x_i, y_j)`$: function evaluated at sample point in each rectangle

Then the **double sum** is:

$$
\sum_{i=1}^{m} \sum_{j=1}^{n} f(x_i, y_j) \Delta x \Delta y
$$

This gives a Riemann sum approximation of the double integral:

$$
\iint_R f(x, y) \, dx \, dy
$$

---

### **3. Computing a Double Sum Over a Rectangular Partition**

#### **Example**

Let $`f(x, y) = x + y`$, over the region $`R = [0, 1] \times [0, 1]`$ with 2 partitions in each direction ($`m = n = 2`$).

Then:

* $`\Delta x = \Delta y = \frac{1}{2}`$


* Sample points (use upper-right corner):
  $`(x_i, y_j) \in \{(0.5, 0.5), (0.5, 1), (1, 0.5), (1, 1)\}`$

Now compute:

$$
\sum_{i=1}^{2} \sum_{j=1}^{2} f(x_i, y_j) \Delta x \Delta y = \frac{1}{4} \sum f(x_i, y_j)
$$

$$
= \frac{1}{4} \left[ f(0.5, 0.5) + f(0.5, 1) + f(1, 0.5) + f(1, 1) \right]
= \frac{1}{4}(1 + 1.5 + 1.5 + 2) = \frac{1}{4}(6) = 1.5
$$

---

### **4. Computing a Double Sum Over a Rectangular Partition Using a Difference of Squares**

This typically arises when the function has the form:

$$
f(x, y) = x^2 - y^2 \quad \text{(a difference of squares)}
$$

#### **Example**

Let $`f(x, y) = x^2 - y^2`$, over $`R = [0, 1] \times [0, 1]`$, with $`m = n = 2`$

* $`\Delta x = \Delta y = \frac{1}{2}`$


* Sample points: $`(0.5, 0.5), (0.5, 1), (1, 0.5), (1, 1)`$

Now compute:

$$
\sum_{i=1}^{2} \sum_{j=1}^{2} (x_i^2 - y_j^2) \Delta x \Delta y
= \frac{1}{4} \sum (x_i^2 - y_j^2)
$$

List each term:

* $`f(0.5, 0.5) = 0.25 - 0.25 = 0`$


* $`f(0.5, 1) = 0.25 - 1 = -0.75`$


* $`f(1, 0.5) = 1 - 0.25 = 0.75`$


* $`f(1, 1) = 1 - 1 = 0`$

So the double sum is:

$$
\frac{1}{4}(0 - 0.75 + 0.75 + 0) = \frac{1}{4}(0) = 0
$$

#### **Interpretation**

When integrating (or summing) a **symmetric function like $`x^2 - y^2`$** over a symmetric domain $`[0,1]\times[0,1]`$, cancellation can occur. 
The positive and negative contributions balance, and the result may be zero.

---

### **5. Summary Table**

| Concept               | Formula / Description                                                 |
| --------------------- |-----------------------------------------------------------------------|
| Rectangular Partition | $`[a,b] \times [c,d]`$ divided into $`m \times n`$ grid               |
| Subintervals          | $`\Delta x = \frac{b-a}{m}, \Delta y = \frac{d-c}{n}`$                |
| Double Sum            | $`\sum_{i=1}^m \sum_{j=1}^n f(x_i, y_j) \Delta x \Delta y`$           |
| Example Function      | $`f(x, y) = x^2 - y^2`$: leads to cancellation over symmetric domains |
| Usage                 | Approximating double integrals; analyzing behavior over regions       |

---

