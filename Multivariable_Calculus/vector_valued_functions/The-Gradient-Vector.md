# **The Gradient Vector**

The **gradient vector** generalizes the idea of a derivative to multivariable functions. 
It points in the direction of the **steepest increase** of a function and is orthogonal 
to **level curves** (or surfaces in 3D).

Given a scalar function $`f(x, y, z, \dots)`$, the **gradient** is denoted:

$$
\nabla f = \left\langle \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial z}, \dots \right\rangle
$$

---

## 1. **Calculating the Gradient of a Function of Two Variables**

If $`f(x, y)`$ is differentiable, then:


$$
\nabla f(x, y) = \left\langle \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right\rangle
$$

### **Example**

Let

$$
f(x, y) = x^2 y + y^3
$$

Then:

* $`\frac{\partial f}{\partial x} = 2xy`$


* $`\frac{\partial f}{\partial y} = x^2 + 3y^2`$

So:

$$
\nabla f(x, y) = \left\langle 2xy,\ x^2 + 3y^2 \right\rangle
$$

---

## 2. **Calculating the Gradient of a Function of Three Variables**

If $`f(x, y, z)`$ is differentiable, then:

$$
\nabla f(x, y, z) = \left\langle \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial z} \right\rangle
$$

### **Example**

Let

$$
f(x, y, z) = xye^z + z^2
$$

Then:

* $`\frac{\partial f}{\partial x} = y e^z`$


* $`\frac{\partial f}{\partial y} = x e^z`$


* $`\frac{\partial f}{\partial z} = xy e^z + 2z`$

So:

$$
\nabla f(x, y, z) = \left\langle y e^z,\ x e^z,\ xy e^z + 2z \right\rangle
$$

---

## 3. **Finding the Points Where a Gradient Vanishes**

The gradient **vanishes** at points where:

$$
\nabla f = \vec{0}
$$

These points are critical in optimization — potential **local extrema** or **saddle points**.

### **Example**

Let

$$
f(x, y) = x^2 + y^2 - 4x - 6y
$$

Then:

* $`\nabla f = \left\langle 2x - 4,\ 2y - 6 \right\rangle`$

Set gradient to zero:

$$
2x - 4 = 0 \quad \Rightarrow \quad x = 2 \\
2y - 6 = 0 \quad \Rightarrow \quad y = 3
$$

So the gradient vanishes at **(2, 3)**.

---

## 4. **Calculating the Gradient Using Properties of the Gradient**

**Useful Properties:**

* **Linearity**:

  $$
  \nabla(af + bg) = a \nabla f + b \nabla g
  $$

* **Product Rule**:

  $$
  \nabla(fg) = f \nabla g + g \nabla f
  $$

* **Quotient Rule**:

  $$
  \nabla\left(\frac{f}{g}\right) = \frac{g \nabla f - f \nabla g}{g^2}
  $$

### **Example (Product Rule)**

Let $`f(x, y) = x^2`$, $`g(x, y) = \sin y`$

Then:

$$
\nabla(fg) = x^2 \cdot \left\langle 0, \cos y \right\rangle + \sin y \cdot \left\langle 2x, 0 \right\rangle = \left\langle 2x \sin y,\ x^2 \cos y \right\rangle
$$

---

## **Summary Table**

| Topic                     | Formula / Description                                 |
| ------------------------- | ----------------------------------------------------- |
| Gradient (2D)             | $`\nabla f(x, y) = \langle f\_x, f\_y \rangle`$       |
| Gradient (3D)             | $`\nabla f(x, y, z) = \langle f\_x, f\_y, f\_z \rangle`$ |
| Vanishing Gradient        | Solve $`\nabla f = \vec{0}`$                          |
| Product Rule for Gradient | $`\nabla(fg) = f \nabla g + g \nabla f`$               |
| Gradient Direction        | Points in direction of **steepest ascent**            |

---
