# **Equality of Mixed Partial Derivatives**

---

## Overview

For a scalar function of multiple variables, **mixed partial derivatives** refer to second-order derivatives taken with respect to two variables in succession.

If all the **second-order mixed partials are continuous** in a neighborhood of a point, then **Clairaut’s Theorem** (or Schwarz's Theorem) guarantees:

$$
\frac{\partial^2 f}{\partial x \partial y} = \frac{\partial^2 f}{\partial y \partial x}
$$

This theorem underlies many results in multivariable calculus and is fundamental for verifying the consistency of computed derivatives.

---

## 1. Finding Missing Constants in First-Order Partial Derivative Expressions

Sometimes, partial derivative expressions are given with unknown constants. 
If these are known to be partials of the **same function**, equality of mixed partials can help solve for unknowns.

### **Example**

Suppose:

$$
f_x = 3x^2y + Ay, \quad f_y = x^3 + Ax + B
$$

Compute mixed partials:

* $`f\_{xy} = \frac{\partial}{\partial y}(f\_x) = 3x^2 + A`$


* $`f\_{yx} = \frac{\partial}{\partial x}(f\_y) = 3x^2 + A`$

Since $`f\_{xy} = f\_{yx}`$ automatically, this confirms any value of $A$ works. Now check $`f\_{yx}`$ again to verify \$B\$ has no effect on equality.

Thus, **matching mixed partials helps identify valid values for constants**.

---

## 2. Identifying Possible Pairs of First-Order Partial Derivatives

Given two functions $`p(x, y)`$ and $`q(x, y)`$, determine whether they can be the partial derivatives of the same scalar field $f$:

* Let $`p(x, y) = \frac{\partial f}{\partial x}`$


* Let $`q(x, y) = \frac{\partial f}{\partial y}`$

If the **cross partials** satisfy:

$$
\frac{\partial p}{\partial y} = \frac{\partial q}{\partial x}
$$

Then $f$ **may exist** with $`f\_x = p`$ and $`f\_y = q`$.

### **Example**

Let:

* $`p(x, y) = x^2 + 2y`$


* $`q(x, y) = 2x + y^2`$

Then:

* $`\partial p / \partial y = 2`$


* $`\partial q / \partial x = 2`$

Since they’re equal, there exists a function $`f(x, y)`$ such that $`f\_x = p`$ and $`f\_y = q`$.

---

## 3. Evaluating Expressions of Partial Derivatives at a Point

You can confirm the equality of mixed partials by computing them at a specific point.

### **Example**

Let:

$$
f(x, y) = x^2 y^3 + 5xy
$$

Compute at $`(1, 2)`$:

* $`f\_x = 2xy^3 + 5y`$


* $`f\_{xy} = 2y^3 + 5`$


* $`f\_y = 3x^2 y^2 + 5x`$


* $`f\_{yx} = 6xy^2 + 5`$

Now evaluate at $`(1, 2)`$:

* $`f\_{xy}(1, 2) = 2(8) + 5 = 21`$


* $`f\_{yx}(1, 2) = 6(1)(4) + 5 = 29`$

Mismatch! So we **must have made an error** — let’s recalculate $`f\_y`$ properly:

* $`f\_y = 3x^2 y^2 + 5x`$


* $`\Rightarrow f\_{yx} = \partial/\partial x(3x^2 y^2 + 5x) = 6x y^2 + 5`$

Now:

* $`f\_{yx}(1, 2) = 6(1)(4) + 5 = 29`$

Oops! Wait — this doesn't match $`f\_{xy} = 21`$.

So let’s recalculate $`f\_{xy}`$ again:


* $`f\_x = 2x y^3 + 5y`$


* $`f\_{xy} = 2x \cdot 3y^2 + 5 = 6x y^2 + 5`$


At $`(1, 2)`$:


* $`f\_{xy} = 6(1)(4) + 5 = 29`$

✅ Match with $`f\_{yx}`$!

---

## Summary Table

| Concept                             | Expression                                                                               |
| ----------------------------------- | ---------------------------------------------------------------------------------------- |
| Mixed partials (Clairaut's Theorem) | $`\frac{\partial^2 f}{\partial x \partial y} = \frac{\partial^2 f}{\partial y \partial x}`$ |
| Use in matching partials            | Check if $`\partial p/\partial y = \partial q/\partial x`$                               |
| Verifying equality at a point       | Compute both $`f\_{xy}`$ and $`f\_{yx}`$ at same point                                    |
| Finding unknown constants           | Match expressions via equal mixed partials                                               |

---
