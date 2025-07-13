## **Defining Double Integrals Using Lower and Upper Riemann Sums**

---

### **1. Overview: Double Integrals and Riemann Sums**

A **double integral** over a region $`R \subset \mathbb{R}^2`$ gives the **signed volume** under a surface $`f(x, y)`$ above $R$. 
It is formally defined as the **limit of Riemann sums**, which approximate this volume using finite rectangular partitions.


#### **Double Integral Definition**:

$`\iint_R f(x, y)\, dA = \lim_{\|P\| \to 0} \sum_{i,j} f(x_{ij}^*, y_{ij}^*) \Delta A_{ij}`$

Where:

* $P$ is a partition of $R$ into subrectangles.


* $`\Delta A_{ij} = \Delta x_i \cdot \Delta y_j`$


* $`(x_{ij}^*, y_{ij}^*) \in R_{ij}`$ is a **sample point** in the subrectangle.


* $`\|P\| \to 0`$: the maximum diagonal length of the subrectangles goes to 0.

---

### **2. Lower and Upper Riemann Sums**

Given a bounded function $`f(x, y)`$ on a rectangle $`R = [a, b] \times [c, d]`$, partitioned into $`m \times n`$ subrectangles:

* Let $`m_{ij} = \inf f(x, y)`$ on $`R_{ij}`$


* Let $`M_{ij} = \sup f(x, y)`$ on $`R_{ij}`$


#### **Lower Riemann Sum**:

$$
L(f, P) = \sum_{i=1}^m \sum_{j=1}^n m_{ij} \Delta A_{ij}
$$

#### **Upper Riemann Sum**:

$$
U(f, P) = \sum_{i=1}^m \sum_{j=1}^n M_{ij} \Delta A_{ij}
$$

If:

$$
\lim_{\|P\| \to 0} L(f, P) = \lim_{\|P\| \to 0} U(f, P)
$$

Then $f$ is **Riemann integrable**, and the common value is the **double integral**.

---

### **3. Applying the Definition Using Lower and Upper Riemann Sums**

To apply this definition practically:

#### Step-by-Step:

1. Partition the rectangle $`R = [a, b] \times [c, d]`$ into small rectangles.


2. For each subrectangle:

   * Compute $`m_{ij} = \inf f(x, y)`$
   * Compute $`M_{ij} = \sup f(x, y)`$


3. Multiply by area $`\Delta A_{ij}`$ and sum:

   * Lower sum: sum of $`m_{ij} \Delta A_{ij}`$
   * Upper sum: sum of $`M_{ij} \Delta A_{ij}`$


4. Refine the partition (make rectangles smaller) and observe convergence.

---

### **4. Calculating a Double Integral Using Lower and Upper Riemann Sums**

#### **Example**:

Let $`f(x, y) = x + y`$ over $`R = [0, 1] \times [0, 1]`$, divide into 2 × 2 subrectangles.

Subrectangles:

| Subregion    | $`R_{ij}`$                     | $`m_{ij}`$ | $`M_{ij}`$ |
|--------------|--------------------------------|------------|-----------|
| $`R_{11}`$   | $`[0, 0.5] \times [0, 0.5]`$   | $`0`$      | $`1`$     |
| $`R_{12}`$   | $`[0.5, 1] \times [0, 0.5]`$   | $`0.5`$    | $`1.5`$   |
| $`R_{21}`$   | $`[0, 0.5] \times [0.5, 1]`$   | $`0.5`$    | $`1.5`$   |
| $`R_{22}`$   | $`[0.5, 1] \times [0.5, 1]`$   | $`1`$      | $`2`$     |

Each $`\Delta A = 0.25`$

* Lower sum:

$$
L = (0 + 0.5 + 0.5 + 1) \cdot 0.25 = 0.5
$$

* Upper sum:

$$
U = (1 + 1.5 + 1.5 + 2) \cdot 0.25 = 1.5
$$

So:

$$
0.5 \leq \iint_R (x + y)\,dA \leq 1.5
$$

The **exact value** is:

$$
\iint_R (x + y)\,dA = \int_0^1 \int_0^1 (x + y)\,dy\,dx = 1
$$

---

### **5. Calculating a Double Integral Using the Mean Value of X and Y**

The **mean value approximation** (midpoint rule) estimates the double integral by sampling at the center of each subrectangle:

Let:

* $`(x_{ij}, y_{ij})`$ be the midpoint of $`R_{ij}`$


* Then:

$$
\iint_R f(x, y)\,dA \approx \sum f(x_{ij}, y_{ij}) \cdot \Delta A
$$

#### **Example**:

Same region $`R = [0,1]^2`$, with midpoint of each 0.5 × 0.5 square:

$$
f(0.25, 0.25) + f(0.75, 0.25) + f(0.25, 0.75) + f(0.75, 0.75)
= (0.5 + 1 + 1 + 1.5)
$$

Average value:

$$
\frac{4}{4} = 1,\quad \text{so } \text{approximate integral} = 1 \cdot 1 = 1
$$

Perfect estimate.

---

### **Summary Table**

| Method                    | Definition                             | Accuracy            | Use                            |
| ------------------------- | -------------------------------------- | ------------------- | ------------------------------ |
| **Lower Riemann Sum**     | Sum of minimum values in subrectangles | Underestimates      | Theoretical lower bound        |
| **Upper Riemann Sum**     | Sum of maximum values in subrectangles | Overestimates       | Theoretical upper bound        |
| **Midpoint Rule**         | Sample at center of subrectangle       | Often very accurate | Practical numerical estimate   |
| **Exact Double Integral** | Limit of Riemann sums                  | True value          | Calculus / symbolic evaluation |

---
