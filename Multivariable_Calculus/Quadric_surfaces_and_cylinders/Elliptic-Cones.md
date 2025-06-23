# **Elliptic Cones**

An **elliptic cone** is a **quadric surface** defined by a **second-degree equation** in three variables where the origin is a **singularity (vertex)** and the cross-sections (traces) are ellipses or hyperbolas depending on the plane of intersection.

---

## **Definition and General Equation**

The standard form of an elliptic cone is:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{z^2}{c^2} = 0
$$

where $`a, b, c \in \mathbb{R}^{+}`$.
This equation represents a **cone with elliptical cross-sections**.

* The **vertex** is at the origin $`(0, 0, 0)`$
* The cone is **symmetric** about the $`z`$-axis
* The surface is **double-napped**, meaning it extends in both the positive and negative directions of the axis of symmetry

---

## **Identifying Properties of Elliptic Cones**

| **Property**                 | **Description**                                              |
| ---------------------------- | ------------------------------------------------------------ |
| **Vertex**                   | The origin (0, 0, 0)                                         |
| **Axes of symmetry**         | Aligned with the coordinate axes (usually the z-axis)        |
| **Cross-section in $z = k$** | Ellipse if $`k \neq 0`$, point or singularity if $`k = 0`$       |
| **Homogeneity**              | Homogeneous quadratic equation (no linear or constant terms) |
| **Non-degenerate**           | Forms a genuine 3D surface, not a degenerate point or line   |
| **Double Napped**            | Has upper and lower sheets (cones) extending from the vertex |

---

## **Finding Traces of Elliptic Cones**

Traces are found by slicing the cone with a plane and analyzing the resulting cross-section:

---

### **1. Trace in a Horizontal Plane ($`z = k`$)**

Substitute $`z = k`$ into the equation:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{k^2}{c^2} = 0
\Rightarrow
\frac{x^2}{a^2} + \frac{y^2}{b^2} = \frac{k^2}{c^2}
$$

This is the equation of an **ellipse** for all $`k \neq 0`$.

---

### **2. Trace in the $`xz`$-plane ($`y = 0`$)**

$$
\frac{x^2}{a^2} - \frac{z^2}{c^2} = 0
\Rightarrow
\frac{x^2}{a^2} = \frac{z^2}{c^2}
\Rightarrow
z = \pm \frac{c}{a} x
$$

This is a pair of lines through the origin — a **conic section (degenerate hyperbola)**.

---

### **3. Trace in the $`yz`$-plane ($`x = 0`$)**

$$
\frac{y^2}{b^2} - \frac{z^2}{c^2} = 0
\Rightarrow
z = \pm \frac{c}{b} y
$$

Another **pair of intersecting lines**.

---

### **Summary of Traces**

| **Plane**      | **Resulting Trace**          |
| -------------- | ---------------------------- |
| $`z = k \neq 0`$ | Ellipse centered at origin   |
| $`z = 0`$        | Point (the vertex at origin) |
| $`x = 0`$        | Two lines through the origin |
| $`y = 0`$        | Two lines through the origin |

---

## **🔚 Summary**

* An **elliptic cone** is a symmetric, double-napped surface defined by a homogeneous quadratic equation.
* It exhibits **elliptical traces in horizontal planes** and **linear traces in vertical planes**.
* Its structure and symmetry make it important in geometry, physics, and optics (e.g., wavefronts and light cones).

---
