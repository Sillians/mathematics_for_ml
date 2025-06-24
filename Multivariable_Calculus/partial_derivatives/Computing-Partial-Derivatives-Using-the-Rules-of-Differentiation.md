# **Computing Partial Derivatives Using the Rules of Differentiation**

Partial derivatives extend standard differentiation rules to functions of multiple variables. 
The primary tools — **product rule**, **quotient rule**, and **chain rule** — are adapted to differentiate 
with respect to one variable while treating others as constants.

---

## **1. Applying the Chain Rule**

The **chain rule** is used when a function depends on intermediate variables that are themselves functions of other variables.

### **Form**:

If

$$
z = f(u, v), \quad \text{where} \quad u = g(x, y), \quad v = h(x, y),
$$

then:

$$
\frac{\partial z}{\partial x} = \frac{\partial f}{\partial u} \cdot \frac{\partial u}{\partial x} + \frac{\partial f}{\partial v} \cdot \frac{\partial v}{\partial x}
$$

### **Example**:

Let

$$
z = \sin(x^2 + y^2)
$$

Then:

$$
\frac{\partial z}{\partial x} = \cos(x^2 + y^2) \cdot 2x
$$

and

$$
\frac{\partial z}{\partial y} = \cos(x^2 + y^2) \cdot 2y
$$

---

## **2. Applying the Product Rule**

If

$$
f(x, y) = u(x, y) \cdot v(x, y),
$$

then:

$$
\frac{\partial f}{\partial x} = \frac{\partial u}{\partial x} \cdot v + u \cdot \frac{\partial v}{\partial x}
$$

### **Example**:

Let

$$
f(x, y) = x^2 \cdot \sin(y),
$$

then:

* With respect to $x$:

$$
\frac{\partial f}{\partial x} = 2x \cdot \sin(y)
$$

* With respect to $y$:

$$
\frac{\partial f}{\partial y} = x^2 \cdot \cos(y)
$$

---

## **3. Applying the Quotient Rule**

If

$$
f(x, y) = \frac{u(x, y)}{v(x, y)},
$$

then:

$$
\frac{\partial f}{\partial x} = \frac{v \cdot \frac{\partial u}{\partial x} - u \cdot \frac{\partial v}{\partial x}}{v^2}
$$

### **Example**:

Let

$$
f(x, y) = \frac{x}{1 + y^2}
$$

Then:

* With respect to $x$:

$$
\frac{\partial f}{\partial x} = \frac{1}{1 + y^2}
$$

* With respect to $y$:

$$
\frac{\partial f}{\partial y} = \frac{-2xy}{(1 + y^2)^2}
$$

---

## **4. Finding Partial Derivatives of Three-Variable Functions**

Given

$$
f(x, y, z),
$$

partial derivatives are computed by treating all but one variable as constants.

### **Example**:

Let

$$
f(x, y, z) = x^2 y + yz \sin(x)
$$

Then:

* With respect to $x$:

$$
\frac{\partial f}{\partial x} = 2xy + yz \cos(x)
$$

* With respect to $y$:

$$
\frac{\partial f}{\partial y} = x^2 + z \sin(x)
$$

* With respect to $z$:

$$
\frac{\partial f}{\partial z} = y \sin(x)
$$

---

## **Summary Table of Rules**

| Rule          | Formula                                                                                                                             |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| Chain Rule    | $`\frac{\partial z}{\partial x} = \frac{\partial z}{\partial u} \cdot \frac{\partial u}{\partial x}`$                                |
| Product Rule  | $`\frac{\partial}{\partial x}(uv) = \frac{\partial u}{\partial x}v + u\frac{\partial v}{\partial x}`$                                |
| Quotient Rule | $`\frac{\partial}{\partial x} \left( \frac{u}{v} \right) = \frac{v \cdot \partial u/\partial x - u \cdot \partial v/\partial x}{v^2}`$ |

---
