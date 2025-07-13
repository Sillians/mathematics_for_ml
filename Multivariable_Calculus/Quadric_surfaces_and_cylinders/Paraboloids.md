# **Paraboloids**

A **paraboloid** is a **quadric surface** that looks like a 3D parabola. There are two main types:

1. **Elliptic Paraboloid**: Bowl-shaped
2. **Hyperbolic Paraboloid**: Saddle-shaped

---

## **1. Elliptic Paraboloid**

### **Standard Equation**

$$
z = \frac{x^2}{a^2} + \frac{y^2}{b^2}
$$

* Opens **upward** if coefficients are positive.
* Opens **downward** if the equation is negated:

$$
z = -\left( \frac{x^2}{a^2} + \frac{y^2}{b^2} \right)
$$

### **Identifying Properties**

| Property           | Description                                             |
| ------------------ | ------------------------------------------------------- |
| **Shape**          | Bowl (convex or concave)                                |
| **Vertex**         | Minimum or maximum point (usually at origin)            |
| **Symmetry**       | Symmetric about all coordinate axes                     |
| **Cross Sections** | Ellipses in planes $`z = k`$; parabolas in $`xz`$, $`yz`$     |
| **Domain**         | All real values of $`x, y`$; $`z \in \mathbb{R}`$ as output |

---

## **2. Hyperbolic Paraboloid**

### **Standard Equation**

$$
z = \frac{x^2}{a^2} - \frac{y^2}{b^2}
$$

This is a **saddle surface** — it curves upward in one direction and downward in another.

### **Identifying Properties**

| Property           | Description                                           |
| ------------------ | ----------------------------------------------------- |
| **Shape**          | Saddle                                                |
| **Vertex**         | Saddle point (neither max nor min)                    |
| **Symmetry**       | Symmetric about the origin and coordinate planes      |
| **Cross Sections** | Hyperbolas in planes $`z = k`$; parabolas in $`xz`$, $`yz`$ |
| **Domain**         | All $`x, y \in \mathbb{R}`$; $`z \in \mathbb{R}`$         |

---

## **3. Traces of Paraboloids**

### **Elliptic Paraboloid:**

**Equation**:

$$
z = \frac{x^2}{a^2} + \frac{y^2}{b^2}
$$

| Plane   | Trace Equation                          | Shape                 |
| ------- | --------------------------------------- | --------------------- |
| $`z = k`$ | $`\frac{x^2}{a^2} + \frac{y^2}{b^2} = k`$ | Ellipse (for $`k > 0`$) |
| $`y = 0`$ | $`z = \frac{x^2}{a^2}`$                   | Parabola              |
| $`x = 0`$ | $`z = \frac{y^2}{b^2}`$                   | Parabola              |

---

### **Hyperbolic Paraboloid:**

**Equation**:

$$
z = \frac{x^2}{a^2} - \frac{y^2}{b^2}
$$

| Plane   | Trace Equation                          | Shape                      |
| ------- | --------------------------------------- | -------------------------- |
| $`z = k`$ | $`\frac{x^2}{a^2} - \frac{y^2}{b^2} = k`$ | Hyperbola (for $`k \neq 0`$) |
| $`y = 0`$ | $`z = \frac{x^2}{a^2}`$                   | Parabola                   |
| $`x = 0`$ | $`z = -\frac{y^2}{b^2}`$                 | Parabola (flipped)         |

---

## **4. Summary Table**

| Type                      | Equation                                | Shape  | Cross-Sections (Traces)         |
| ------------------------- | --------------------------------------- | ------ | ------------------------------- |
| **Elliptic Paraboloid**   | $`z = \frac{x^2}{a^2} + \frac{y^2}{b^2}`$ | Bowl   | Ellipses ($`z = k`$), parabolas   |
| **Hyperbolic Paraboloid** | $`z = \frac{x^2}{a^2} - \frac{y^2}{b^2}`$ | Saddle | Hyperbolas ($`z = k`$), parabolas |

---
