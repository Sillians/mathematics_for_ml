# **Higher-Order Partial Derivatives**

Higher-order partial derivatives extend the concept of first-order derivatives to capture curvature 
and more detailed local behavior of multivariable functions. These include **second-order** and beyond, 
as well as **mixed** partials.

---

## 1. **Finding Mixed Second-Order Partial Derivatives**

Given a function $`f(x, y)`$, the **mixed partial derivatives** are:

* $`f\_{xy} = \frac{\partial}{\partial y} \left( \frac{\partial f}{\partial x} \right)`$
* $`f\_{yx} = \frac{\partial}{\partial x} \left( \frac{\partial f}{\partial y} \right)`$

If \$f\$ has continuous second-order partial derivatives near a point, **Clairaut’s Theorem** guarantees:

$$
f_{xy} = f_{yx}
$$

### **Example**

Let

$$
f(x, y) = x^2 y + 3xy^2
$$

Then:

* $`f\_x = 2xy + 3y^2`$
* $`f\_{xy} = \frac{\partial}{\partial y}(2xy + 3y^2) = 2x + 6y`$
* $`f\_y = x^2 + 6xy`$
* $`f\_{yx} = \frac{\partial}{\partial x}(x^2 + 6xy) = 2x + 6y`$
  ⇒ $`f\_{xy} = f\_{yx}`$ ✅

---

##  2. **Computing Expressions Involving Second-Order Partial Derivatives**

These expressions often appear in applications such as the Laplacian:

$$
\nabla^2 f = f_{xx} + f_{yy}
$$

### **Example**

Let

$$
f(x, y) = \ln(x^2 + y^2)
$$

Compute $`f\_{xx}`$ and $`f\_{yy}`$:

* $`f\_x = \frac{2x}{x^2 + y^2}`$
* $`f\_{xx} = \frac{2(y^2 - x^2)}{(x^2 + y^2)^2}`$
* $`f\_y = \frac{2y}{x^2 + y^2}`$
* $`f\_{yy} = \frac{2(x^2 - y^2)}{(x^2 + y^2)^2}`$

Then:

$$
f_{xx} + f_{yy} = \frac{2(y^2 - x^2 + x^2 - y^2)}{(x^2 + y^2)^2} = 0
$$

---

##  3. **Finding Higher-Order Derivatives**

For functions of more than one variable (e.g., $`f(x, y, z)`$), higher-order derivatives may 
involve repeated application of partial derivatives:

### **Example**

Let

$$
f(x, y, z) = xyz + e^{xz}
$$

Find some second-order partials:

* $`f\_{x} = yz + z e^{xz}`$
* $`f\_{xz} = \frac{\partial}{\partial z}(yz + z e^{xz}) = y + e^{xz} + xz e^{xz}`$
* $`f\_{zz} = \frac{\partial}{\partial z}(x e^{xz}) = x^2 e^{xz}`$

You can continue this process to get third-order or higher derivatives, keeping track of variable order.

---

## **Summary Table**

| Derivative Type         | Notation            | Interpretation                           |
| ----------------------- | ------------------- | ---------------------------------------- |
| Second-order partial    | $`f\_{xx}, f\_{yy}`$ | Curvature in the direction of $x$ or $y$ |
| Mixed partial           | $`f\_{xy}, f\_{yx}`$ | Rate of change of slope across variables |
| Higher-order (3rd, 4th) | $`f\_{xyz}, f\_{zzz}`$ | Repeated change in multiple directions   |

---
