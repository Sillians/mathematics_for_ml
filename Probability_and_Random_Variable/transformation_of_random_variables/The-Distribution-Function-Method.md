## **The Distribution Function Method**

The **distribution function method** is a technique used to find the **probability density function (PDF)** of a **transformed random variable**. 
Instead of transforming the PDF directly, we first compute the **cumulative distribution function (CDF)** 
of the transformed variable and then differentiate it to obtain the new PDF.

---

### **1. General Steps of the Distribution Function Method**

Let $X$ be a continuous random variable with known PDF $`f_X(x)`$ and CDF $`F_X(x)`$, 
and let $`Y = g(X)`$ be a transformation of $X$. Then:

1. Compute the CDF of $Y$:

$$
F_Y(y) = P(Y \le y) = P(g(X) \le y)
$$

2. Express this probability in terms of $X$.

3. Differentiate $`F_Y(y)`$ to obtain the PDF of $Y$:

$$
f_Y(y) = \frac{d}{dy} F_Y(y)
$$

---

### **2. Computing the PDF Under an Affine Transformation**

Let $`Y = aX + b`$, where $`a \ne 0`$. This is a linear (affine) transformation.

#### ✅ **Step-by-step:**

If $`X \sim f_X(x)`$, then the PDF of $`Y = aX + b`$ is:

$$
f_Y(y) = \frac{1}{|a|} f_X\left( \frac{y - b}{a} \right)
$$

This formula adjusts the shape of the original distribution and rescales it.

---

#### ✅ **Example:**

If $`X \sim U(0, 1)`$, then $`f_X(x) = 1`$ for $`0 \le x \le 1`$

Let $`Y = 2X + 3`$. Then:

$$
f_Y(y) = \frac{1}{2} \cdot f_X\left(\frac{y - 3}{2}\right)
$$

* Support of $Y$: $`y \in [3, 5]`$
* So:

$$
f_Y(y) =
\begin{cases}
\frac{1}{2}, & 3 \le y \le 5 \\
0, & \text{otherwise}
\end{cases}
$$

---

### **3. Computing the PDF Under a Nonlinear Transformation**

Let $`Y = g(X)`$, where $`g`$ is **monotonic and nonlinear**.

#### ✅ General Rule (Using CDF and Derivative):

If $g$ is differentiable and **strictly increasing**:

$$
f_Y(y) = f_X\left(g^{-1}(y)\right) \cdot \left| \frac{d}{dy} g^{-1}(y) \right|
$$

If $g$ is **strictly decreasing**, the formula still holds because of the absolute value.

---

#### ✅ **Example:**

Let $`X \sim U(0, 1)`$, and $`Y = \sqrt{X}`$.
We want to find $`f_Y(y)`$.

1. CDF of $Y$:

$$
F_Y(y) = P(Y \le y) = P(\sqrt{X} \le y) = P(X \le y^2) = F_X(y^2)
$$

Since $`X \sim U(0, 1)`$, $`F_X(x) = x`$ for $`0 \le x \le 1`$, so:

$$
F_Y(y) = y^2 \quad \text{for } 0 \le y \le 1
$$

2. Differentiate:

$$
f_Y(y) = \frac{d}{dy} F_Y(y) = \frac{d}{dy} (y^2) = 2y
$$

So:

$$
f_Y(y) =
\begin{cases}
2y, & 0 \le y \le 1 \\
0, & \text{otherwise}
\end{cases}
$$

---

### ✅ **Summary Table**

| Transformation Type              | PDF Formula                             |                               |                                        |
|----------------------------------| --------------------------------------- | ----------------------------- | -------------------------------------- |
| Affine $`Y = aX + b`$            | ( f\_Y(y) = \frac{1}{                   | a                             | } f\_X\left( \frac{y - b}{a} \right) ) |
| Monotonic Nonlinear $`Y = g(X)`$ | ( f\_Y(y) = f\_X(g^{-1}(y)) \cdot \left | \frac{d}{dy} g^{-1}(y) \right | )                                      |

---

### **Conclusion**

The **distribution function method** provides a reliable technique for deriving the PDF of a transformed variable, 
particularly when direct substitution is difficult. It is especially valuable in transformations 
involving **nonlinear** or **piecewise** functions where algebraic inverses and domain adjustments are required.
