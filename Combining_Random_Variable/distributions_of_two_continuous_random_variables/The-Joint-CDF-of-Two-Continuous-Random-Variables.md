## **The Joint CDF of Two Continuous Random Variables**

---

### **1. Overview: The Joint CDF**

The **joint cumulative distribution function (CDF)** of two continuous random variables $X$ and $Y$, 
denoted $`F(x, y)`$, gives the probability that $`X \leq x`$ and $`Y \leq y`$:

$$
F(x, y) = P(X \leq x, Y \leq y)
= \iint\limits_{(-\infty, x] \times (-\infty, y]} f(u, v)\,du\,dv
$$

Where:

* $`f(u, v)`$ is the **joint probability density function (PDF)** of $X$ and $Y$.


* $`F(x, y)`$ is **non-decreasing** in both variables, and:

  * $`\displaystyle \lim_{x \to \infty, y \to \infty} F(x, y) = 1`$

  * $`\displaystyle \lim_{x \to -\infty} F(x, y) = \lim_{y \to -\infty} F(x, y) = 0`$

---

### **2. Computing the Value of the Joint CDF at a Point**

To compute $`F(x_0, y_0)`$ from a given joint PDF $`f(x, y)`$:

#### **Procedure**

1. **Identify support** of $`f(x, y)`$: region $D$ where $`f > 0`$.


2. If $`(x_0, y_0)`$ lies outside $D$, the integral simplifies or vanishes.


3. Compute:

$$
F(x_0, y_0) = \iint\limits_{u = -\infty}^{x_0} \int_{v = -\infty}^{y_0} f(u, v)\, dv\, du
$$

#### **Example**

Given:

$$
f(x, y) = 
\begin{cases}
6y e^{-3x}, & x \geq 0,\ 0 \leq y \leq 1 \\
0, & \text{otherwise}
\end{cases}
$$

Find $F(1, 0.5)$:

$$
F(1, 0.5) = \int_0^1 \int_0^{0.5} 6y e^{-3x}\, dy\, dx
= \int_0^1 e^{-3x} \left[ 3y^2 \right]_0^{0.5}\, dx
= \int_0^1 e^{-3x} \cdot 0.75\, dx
= 0.75 \cdot \left[ \frac{-1}{3}e^{-3x} \right]_0^1
= 0.75 \cdot \left( \frac{1}{3}(1 - e^{-3}) \right)
$$

$$
= \frac{1}{4}(1 - e^{-3})
$$

---

### **3. Finding a Probability Geometrically Using a CDF**

The joint CDF can be used to compute probabilities over **rectangular regions**:

For example, if $`a < b`$, $`c < d`$, then:

$$
P(a < X \leq b,\ c < Y \leq d)
= F(b, d) - F(a, d) - F(b, c) + F(a, c)
$$

#### **Example**

To find $`P(X \in [0,1],\ Y \in [0, 0.5])`$:

$$
= F(1, 0.5) - F(0, 0.5) - F(1, 0) + F(0, 0)
$$

Assuming CDF values known, this gives probability over a **bounded rectangle** in the plane.

---

### **4. Finding Part of a Joint CDF from a Joint PDF: Simple Cases**

When the joint PDF is separable or defined over a simple rectangular region $`D = [a, b] \times [c, d]`$, 
and $`x, y`$ lie within those bounds, the CDF becomes:

$$
F(x, y) = \int_a^x \int_c^y f(u, v)\, dv\, du
$$

#### **Example**

If:

$$
f(x, y) = \frac{9}{2}x^2 y^2,\quad \text{for } -1 \leq x \leq 1,\ 0 \leq y \leq 1
$$

Then:

$$
F(1, 0.5) = \int_{-1}^{1} \int_{0}^{0.5} \frac{9}{2}x^2 y^2 \, dy\, dx
= \int_{-1}^{1} \left( \frac{3}{16}x^2 \right) dx = \frac{1}{8}
$$

(As seen in earlier examples)

---

### **5. Finding Part of a Joint CDF from a Joint PDF**

In **general cases**, especially when $`f(x, y)`$ is not separable or defined over irregular domains:

#### **Steps**

1. Determine the bounds of integration: $x$ from $`-\infty`$ to $`x_0`$, and $y$ from $`-\infty`$ to $`y_0`$, intersected with the domain $D$.


2. Set up the double integral with correct limits.


3. Evaluate the integral—possibly in parts—if the integration domain is not rectangular.

#### **General Formula** (on domain $D$):

$$
F(x_0, y_0) = \iint_{(u, v) \in D \cap ((-\infty, x_0] \times (-\infty, y_0])} f(u, v) \, dv \, du
$$

This approach ensures accuracy even when the evaluation point partially intersects the region where the PDF is defined.

---

### **Summary Table**

| Concept                        | Description                                                                |
| ------------------------------ | -------------------------------------------------------------------------- |
| Joint CDF                      | $`F(x, y) = P(X \leq x, Y \leq y) = \iint f(u,v) \,du\,dv`$                  |
| From PDF                       | Integrate the PDF over $`(-\infty, x] \times (-\infty, y]`$                  |
| Rectangular region probability | $`P(a < X \leq b, c < Y \leq d) = F(b,d) - F(a,d) - F(b,c) + F(a,c)`$        |
| From support $D$               | Restrict integration region to $`D \cap ((-\infty, x] \times (-\infty, y])`$ |
| Piecewise PDF                  | Split the integral over regions where $`f(x, y) \neq 0`$                     |

---
