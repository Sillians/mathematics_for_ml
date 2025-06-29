## **The Multivariable Chain Rule in Vector Form**

---

### **1. Overview: Vector Form of the Chain Rule**

The **multivariable chain rule** in vector form provides a way to differentiate composite functions where the inner 
function maps from $`\mathbb{R}`$ (or higher dimensions) into $`\mathbb{R}^n`$, 
and the outer function maps from $`\mathbb{R}^n`$ into $`\mathbb{R}`$. If:

* $`\vec{r}(t) = \langle x(t), y(t), z(t) \rangle`$ is a vector-valued function


* $`f(x, y, z)`$ is a scalar-valued function

Then the chain rule in vector form is:

$$
\frac{d}{dt} f(\vec{r}(t)) = \nabla f(\vec{r}(t)) \cdot \vec{r}'(t)
$$

This expression generalizes to functions with more variables and higher dimensions.

---

### **2. Applying the Vector Form of the Chain Rule to a Function of Two Variables**

Let $`f(x, y)`$ be a scalar-valued function and $`\vec{r}(t) = \langle x(t), y(t) \rangle`$, then:

$$
\frac{d}{dt} f(x(t), y(t)) = \nabla f(x(t), y(t)) \cdot \vec{r}'(t)
$$

Where:

* $`\nabla f(x, y) = \left\langle \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right\rangle`$


* $`\vec{r}'(t) = \left\langle \frac{dx}{dt}, \frac{dy}{dt} \right\rangle`$

**Example:**

If $`f(x, y) = x^2 + y^2`$, and $`\vec{r}(t) = \langle \cos t, \sin t \rangle`$, then:

$$
\nabla f = \langle 2x, 2y \rangle, \quad \vec{r}'(t) = \langle -\sin t, \cos t \rangle
$$


$$
\frac{d}{dt} f(\vec{r}(t)) = \langle 2\cos t, 2\sin t \rangle \cdot \langle -\sin t, \cos t \rangle = -2\cos t \sin t + 2\sin t \cos t = 0
$$

---

### **3. Applying the Vector Form of the Chain Rule to a Function of Three Variables**

For a function $`f(x, y, z)`$ and $`\vec{r}(t) = \langle x(t), y(t), z(t) \rangle`$, the chain rule becomes:

$$
\frac{d}{dt} f(\vec{r}(t)) = \frac{\partial f}{\partial x} \frac{dx}{dt} + \frac{\partial f}{\partial y} \frac{dy}{dt} + \frac{\partial f}{\partial z} \frac{dz}{dt}
= \nabla f \cdot \vec{r}'(t)
$$

**Example:**

Let $`f(x, y, z) = \ln(xyz)`$, and $`\vec{r}(t) = \langle t, e^{t^{-1}}, e^t \rangle`$

* $`\nabla f = \left\langle \frac{1}{x}, \frac{1}{y}, \frac{1}{z} \right\rangle`$


* At $`\vec{r}(t)`$: $`\nabla f = \left\langle \frac{1}{t}, e^{-t^{-1}}, e^{-t} \right\rangle`$


* $`\vec{r}'(t) = \left\langle 1, -t^{-2}e^{t^{-1}}, e^t \right\rangle`$

Then:

$$
\frac{d}{dt} f(\vec{r}(t)) = \frac{1}{t}(1) + e^{-t^{-1}} (-t^{-2} e^{t^{-1}}) + e^{-t}(e^t) = \frac{1}{t} - t^{-2} + 1
$$

---

### **4. Evaluating the Derivative at a Point Using the Chain Rule**

To evaluate the derivative at a specific point:

1. Compute $`\nabla f`$ at that point.


2. Compute $`\vec{r}'(t)`$ at that point.


3. Take their dot product.

**Example:**

Given $`f(x, y) = x^2 + y^2`$, $`\vec{r}(t) = \langle t, t^2 \rangle`$. Then at $`t = 1`$:

* $`\nabla f = \langle 2x, 2y \rangle \Rightarrow \langle 2t, 2t^2 \rangle = \langle 2, 2 \rangle`$


* $`\vec{r}'(t) = \langle 1, 2t \rangle = \langle 1, 2 \rangle`$


* Derivative: $`\langle 2, 2 \rangle \cdot \langle 1, 2 \rangle = 2 + 4 = 6`$

---

### **5. Computing the Rate of Change of a Multivariable Function at a Point Using the Chain Rule**

The chain rule provides the **rate of change** of a scalar field $f$ along a path $`\vec{r}(t)`$, 
capturing how fast $f$ changes as we move through space along that path.

This is useful in physics and engineering to:

* Measure temperature change along a curve


* Track pressure change along a flight path


* Analyze concentration gradients along streamlines

---

### **Summary Table**

| Concept                  | Formula                                                                                                      |
| ------------------------ | ------------------------------------------------------------------------------------------------------------ |
| Chain Rule (Vector Form) | $`\frac{d}{dt} f(\vec{r}(t)) = \nabla f(\vec{r}(t)) \cdot \vec{r}'(t)`$                                        |
| Gradient                 | $`\nabla f = \left\langle \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \cdots \right\rangle`$ |
| Derivative at a Point    | Evaluate $`\nabla f`$ and $\vec{r}'$ at the point, then compute dot product                                    |
| Rate of Change           | Interpreted as how fast $f$ changes along the curve $`\vec{r}(t)`$                                             |

This vector form unifies partial derivatives and paths into a concise and powerful tool for differentiation in multivariable calculus.
