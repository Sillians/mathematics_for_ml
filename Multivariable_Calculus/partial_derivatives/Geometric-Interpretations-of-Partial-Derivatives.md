# **Geometric Interpretations of Partial Derivatives**

Partial derivatives measure the **rate of change** of a multivariable function in the direction of one variable while holding others constant. 
Geometrically, they describe the **slope of the surface** in a given direction and help define **tangent lines and vectors** on surfaces and curves.

---

## 1. **Finding the Slope of the Tangent Line to a Curve at a Point**

If $`f(x, y)`$ is a surface and we consider a **trace** (intersection with a plane like $`y = y\_0`$), then:

* $`\frac{\partial f}{\partial x}(x\_0, y\_0)`$ gives the **slope** of the tangent line to the curve $`f(x, y\_0)\$ at \$x = x\_0`$


* Similarly, $`\frac{\partial f}{\partial y}(x\_0, y\_0)`$ gives the slope along $y$ when $x$ is fixed.


### **Example**

Let:

$$
f(x, y) = x^2 + y^2, \quad \text{at point } (1, 2)
$$

Then:

* $`\frac{\partial f}{\partial x}(1, 2) = 2x = 2(1) = 2`$ → slope along $x$
* $`\frac{\partial f}{\partial y}(1, 2) = 2y = 2(2) = 4`$ → slope along $y$

These represent slopes of **tangent lines** in the $x$ and $y$ traces of the surface.

---

## 2. **Finding the Equation of the Tangent Line to a Curve at a Point**

Suppose we fix $`y = y\_0`$ and define:

$$
g(x) = f(x, y_0)
$$

Then the tangent line at $`x = x\_0`$ is:

$$
L(x) = f(x_0, y_0) + \frac{\partial f}{\partial x}(x_0, y_0) \cdot (x - x_0)
$$

### **Example**

Let:

$$
f(x, y) = xy^2, \quad \text{at } (1, 2)
$$

Fix $`y = 2`$:

Then $`g(x) = 4x`$, so:

* $`\frac{\partial f}{\partial x}(x, y) = y^2`$


* At $`(1, 2)`$: slope = $4$, and $`f(1, 2) = 4`$

Tangent line:

$$
L(x) = 4 + 4(x - 1)
$$

---

## 3. **Finding the Tangent Vector to a Curve at a Point**

For a parameterized curve $`\vec{r}(t) = \langle x(t), y(t), z(t) \rangle`$, the **tangent vector** at $`t = t\_0`$ is:

$$
\vec{r}\,'(t_0) = \left\langle \frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt} \right\rangle\bigg|_{t = t_0}
$$

In the context of a surface $`z = f(x, y)`$, consider a curve on the surface with $`x = x(t), y = y(t)`$:

Then $`z(t) = f(x(t), y(t))`$ and:

$$
\frac{dz}{dt} = \frac{\partial f}{\partial x} \cdot \frac{dx}{dt} + \frac{\partial f}{\partial y} \cdot \frac{dy}{dt}
$$

So the tangent vector is:

$$
\vec{T}(t) = \left\langle \frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt} \right\rangle
$$

---

## ✅ Summary Table

| Concept                                | Expression                                                          |
| -------------------------------------- | ------------------------------------------------------------------- |
| Slope along $`x`$ at $`(x\_0, y\_0)`$   | $`\frac{\partial f}{\partial x}(x\_0, y\_0)`$                       |
| Slope along $`y`$ at $`(x\_0, y\_0)`$   | $`\frac{\partial f}{\partial y}(x\_0, y\_0)`$                       |
| Tangent line to $`f(x, y\_0)`$ at $`x\_0`$ | $`f(x\_0, y\_0) + \frac{\partial f}{\partial x}(x\_0, y\_0)(x - x\_0)`$ |
| Tangent vector on surface              | $`\langle x'(t), y'(t), \frac{dz}{dt} \rangle`$                      |

---
