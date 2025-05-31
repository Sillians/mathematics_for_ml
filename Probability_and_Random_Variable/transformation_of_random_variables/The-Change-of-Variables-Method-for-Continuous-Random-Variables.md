## **The Change-of-Variables Method for Continuous Random Variables**

---

### **Overview:**

The **change-of-variables method** allows us to determine the probability density function (PDF) of a new random 
variable defined as a transformation of another. This is essential when dealing with transformed data or modeling 
distributions of nonlinear functions of a variable.

---

### **1. Identifying Transformations Where the Change-of-Variables Method Is Applicable**

The method is applicable when:

* The transformation is **monotonic** (strictly increasing or decreasing) on the domain of interest.
* The original variable has a known **continuous PDF**.
* The transformation is **differentiable**, and its inverse exists on the support of the transformed variable.

Let:

* $X$ be a continuous random variable with PDF $`f_X(x)`$,
* $`Y = g(X)`$ be a transformation of $X$, where $g$ is one-to-one and differentiable.

---

### **2. Computing the PDF of a Random Variable Under an Affine Transformation**

For affine transformation $`Y = aX + b`$ where $`a \neq 0`$:

$$
f_Y(y) = \frac{1}{|a|} f_X\left( \frac{y - b}{a} \right)
$$

**Explanation:**

* The absolute value $`|a|`$ accounts for scaling.
* The substitution $x = \frac{y - b}{a}$ adjusts the original density to the new variable.

**Example:**

If $`X \sim \text{Uniform}(0, 1)`$, and $`Y = 2X + 3`$, then:

$$
f_Y(y) = \frac{1}{2}, \quad \text{for } y \in [3, 5]
$$

---

### **3. Computing the PDF of a Random Variable Under a Nonlinear Transformation**

If $`Y = g(X)`$ is a **nonlinear**, one-to-one, differentiable transformation:

$$
f_Y(y) = f_X(g^{-1}(y)) \cdot \left| \frac{d}{dy} g^{-1}(y) \right|
$$

Where:

* $`g^{-1}`$ is the inverse function of $`g`$,
* The absolute derivative adjusts for local distortion introduced by $g$.

**Example:**

Let $`X \sim \text{Uniform}(0, 1)`$, and $`Y = \sqrt{X}`$, i.e., $`X = Y^2`$

Then:

$$
f_Y(y) = f_X(y^2) \cdot \left| \frac{d}{dy}(y^2) \right| = 1 \cdot 2y = 2y, \quad \text{for } y \in [0, 1]
$$

---

### **Key Insight:**

The transformation rule ensures that the **area under the PDF remains 1**, and it **preserves probabilities** under the change of variable.

---

### ✅ Summary:

| Transformation Type  | PDF Formula                             |                               |                                        |
| -------------------- | --------------------------------------- | ----------------------------- | -------------------------------------- |
| Affine $`Y = aX + b`$  | ( f\_Y(y) = \frac{1}{                   | a                             | } f\_X\left( \frac{y - b}{a} \right) ) |
| Nonlinear $`Y = g(X)`$ | ( f\_Y(y) = f\_X(g^{-1}(y)) \cdot \left | \frac{d}{dy} g^{-1}(y) \right | )                                      |

This method is foundational in probability, especially for distributions of derived statistics and simulations.
