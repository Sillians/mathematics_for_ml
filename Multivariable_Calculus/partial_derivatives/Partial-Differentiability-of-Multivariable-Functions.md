# **Partial Differentiability of Multivariable Functions**

Partial differentiability concerns whether the partial derivatives of a multivariable function exist at 
specific points or over a region. It is a foundational concept in multivariable calculus and a precursor 
to continuity, differentiability, and smoothness in higher dimensions.

---

## **1. Finding the Domain Where a Partial Derivative Exists**

To determine where a partial derivative exists, check:

* The function must be **defined** at the point.
* The limit used to define the partial derivative must exist.

### **Example**

Let

$$
f(x, y) = \frac{x^2 y}{x^2 + y^2}, \quad f(0, 0) = 0
$$

To find $`\frac{\partial f}{\partial x}`$ at $`(0, 0)`$:

* Define $`f(x, y)`$ along the path $`y = 0`$:


  $`f(x, 0) = 0`$ for $`x \ne 0`$ ⇒ $`\partial f / \partial x = 0`$ at $`(0, 0)`$ exists.


To determine the **domain where $`\partial f/\partial x`$ exists**, analyze the limit definition:

$$
\lim_{h \to 0} \frac{f(x + h, y) - f(x, y)}{h}
$$

for all $`(x, y)`$ where $f$ is defined and smooth.

---

## **2. Finding the Domain Where All Partial Derivatives Exist**

A function $`f(x, y)`$ has **all partial derivatives** if:

* $`\frac{\partial f}{\partial x}`$ and $`\frac{\partial f}{\partial y}`$ both exist at every point in a region.

### **Example**

Let

$$
f(x, y) = \ln(4 - x^2 - 4y^2)
$$

To find the domain where all partials exist:

* The logarithm is defined when the argument is **positive**:

  $`4 - x^2 - 4y^2 > 0`$
  ⇒ $`x^2 + 4y^2 < 4`$


* This is the **interior of an ellipse**, which is the domain of all partial derivatives.

---

## **3. Identifying Points Where Partial Derivatives Exist**

Sometimes, partial derivatives may exist **at a point**, but the function may not be differentiable there.

### **Example**

Let

$$
f(x, y) =
\begin{cases}
\frac{xy}{x^2 + y^2}, & (x, y) \ne (0, 0) \\
0, & (x, y) = (0, 0)
\end{cases}
$$

* At $`(0, 0)`$:

  * $`\frac{\partial f}{\partial x}(0, 0) = \lim\_{h \to 0} \frac{f(h, 0) - f(0, 0)}{h} = 0`$


  * $`\frac{\partial f}{\partial y}(0, 0) = \lim\_{h \to 0} \frac{f(0, h) - f(0, 0)}{h} = 0`$

  ⇒ Both partial derivatives exist at $`(0, 0)`$.

However:

* The function is **not continuous** at $`(0, 0)`$ since approaching along $`y = x`$ gives $`\frac{1}{2}`$.

---

## **Key Summary**

| Concept                         | Description                                                                             |
| ------------------------------- | --------------------------------------------------------------------------------------- |
| Partial derivative exists       | Limit defining the derivative exists at a point                                         |
| All partials exist in a domain  | $`\frac{\partial f}{\partial x}`$ and $`\frac{\partial f}{\partial y}`$ exist throughout |
| Pointwise existence of partials | Possible even if the function is not continuous or differentiable                       |

---