# **Introduction to Partial Derivatives**

## **Overview**

Partial derivatives measure the rate at which a multivariable function changes as **only one variable changes**, keeping the others constant. 
This is foundational for multivariable calculus, optimization, and differential equations.

Given a function $`f(x, y)`$, its partial derivatives with respect to $x$ and $y$ are denoted as:

* $`\frac{\partial f}{\partial x}\$ or \$f\_x`$
* $`\frac{\partial f}{\partial y}\$ or \$f\_y`$

---

##  Partial Derivatives as Limits of Difference Quotients

Just like single-variable derivatives, partial derivatives can be defined using a limit:

### Partial with respect to $x$:

$$
\frac{\partial f}{\partial x}(x_0, y_0) = \lim_{h \to 0} \frac{f(x_0 + h, y_0) - f(x_0, y_0)}{h}
$$

### Partial with respect to $y$:

$$
\frac{\partial f}{\partial y}(x_0, y_0) = \lim_{h \to 0} \frac{f(x_0, y_0 + h) - f(x_0, y_0)}{h}
$$

Only one variable is allowed to change; the other is held constant.

---

## Finding Partial Derivatives of Two-Variable Functions

To find partial derivatives:

* **Treat other variables as constants**
* Differentiate **only** with respect to the specified variable

### Example:

Let $`f(x, y) = x^2y + 3xy^2`$

**Partial with respect to $x$:**

$$
f_x = \frac{\partial}{\partial x}(x^2y + 3xy^2) = 2xy + 3y^2
$$

**Partial with respect to $y$:**

$$
f_y = \frac{\partial}{\partial y}(x^2y + 3xy^2) = x^2 + 6xy
$$

---

## Evaluating a Partial Derivative at a Point

After finding a general partial derivative, plug in the values of the point $`(x\_0, y\_0)`$.

### Example:

Let $`f(x, y) = x^2y + 3xy^2`$

Already found: $`f\_x = 2xy + 3y^2`$

Now evaluate at $`(x, y) = (1, 2)`$:

$$
f_x(1, 2) = 2 \cdot 1 \cdot 2 + 3 \cdot 2^2 = 4 + 12 = 16
$$

---

## Summary Table

| Function $`f(x, y)`$ | $`\frac{\partial f}{\partial x}`$ | $`\frac{\partial f}{\partial y}`$ |
| -------------- | -------------------------- | -------------------------- |
| $`x^2y + 3xy^2`$ | $`2xy + 3y^2`$              | $`x^2 + 6xy`$               |
| $`e^{xy}`$      | $`y e^{xy}`$                | $`x e^{xy}`$                |
| $`\ln(x^2 + y^2)`$ | $`\frac{2x}{x^2 + y^2}`$    | $`\frac{2y}{x^2 + y^2}`$    |
| $`\sin(xy)`$    | $`y \cos(xy)`$              | $`x \cos(xy)`$              |

---
