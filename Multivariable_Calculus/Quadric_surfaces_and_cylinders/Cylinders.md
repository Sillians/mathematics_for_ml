# **Cylinders**

## **Definition**

A **cylinder** in multivariable calculus is a surface that is invariant in one direction (i.e., it "extends infinitely" along a line). 
It is typically formed when a plane curve is translated along a line not in the plane of the curve.

For example:

* The surface defined by

$$
x^2 + y^2 = 1
$$

is a **cylinder** in 3D space extending along the $z$-axis. The base is a circle in the $xy$-plane.

---

## **The Domain of a Cylinder**

When working with cylinders, particularly when dealing with their algebraic representations, identifying the domain means determining for which values the equation makes sense.

### **Example:**

Let

$$
x^2 + y^2 = 4
$$

This describes a **cylinder** parallel to the \$z\$-axis.

* The **domain** is all $`(x, y, z) \in \mathbb{R}^3`$ such that $`x^2 + y^2 = 4`$.
* Since there is **no restriction on $z$**, the domain can be considered **all real values of $z$**:

$$
\text{Domain: } \{(x, y, z) \in \mathbb{R}^3 \mid x^2 + y^2 = 4, \ z \in \mathbb{R} \}
$$

---

## **Traces of Cylinders**

The **trace** of a surface is its intersection with a coordinate plane.

### **For a Cylinder Defined by:**

$$
x^2 + y^2 = 4
$$

* **$`xy`$-plane trace**:
  Set $`z = 0`$. The equation becomes:

$$
x^2 + y^2 = 4 \Rightarrow \text{a circle in the } xy\text{-plane}.
$$

* **$`xz`$-plane trace**:
  Set $`y = 0`$. The equation becomes:

$$
x^2 = 4 \Rightarrow x = \pm 2 \text{ (two vertical lines in the } xz\text{-plane)}.
$$

* **$`yz`$-plane trace**:
  Set $`x = 0`$. The equation becomes:

$$
y^2 = 4 \Rightarrow y = \pm 2 \text{ (two vertical lines in the } yz\text{-plane)}.
$$

---

## **Common Forms of Cylinders**

1. **Elliptic Cylinder:**

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
$$

   Extends in $z$, forms an **elliptical cross-section**.

2. **Parabolic Cylinder:**

$$
y = x^2
$$

   Cross-section is a **parabola**, extended in $z$.

3. **Hyperbolic Cylinder:**

$$
x^2 - y^2 = 1
$$

   Cross-section is a **hyperbola**, extends in $z$.

---

## **Summary Table**

| **Cylinder Type**   | **General Equation**                 | **Cross-section Shape** | **Direction of Extension** |
| ------------------- | ------------------------------------ | ----------------------- | ---------------------- |
| Circular Cylinder   | $`x^2 + y^2 = r^2`$                   | Circle                  | Along $`z`$            |
| Elliptic Cylinder   | $`\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1`$ | Ellipse                 | Along $`z`$            |
| Parabolic Cylinder  | $`y = x^2`$                           | Parabola                | Along $`z`$            |
| Hyperbolic Cylinder | $`x^2 - y^2 = 1`$                     | Hyperbola               | Along $`z`$             |

---
