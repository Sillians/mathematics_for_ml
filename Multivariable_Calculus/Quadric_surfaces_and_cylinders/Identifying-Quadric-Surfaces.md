# **Identifying Quadric Surfaces**

---

## **1. What Are Quadric Surfaces?**

A **quadric surface** is the 3D analog of conic sections, defined by a second-degree polynomial in three variables:

$$
Ax^2 + By^2 + Cz^2 + Dxy + Eyz + Fxz + Gx + Hy + Iz + J = 0
$$

Common quadric surfaces include:

* **Ellipsoids**

* **Hyperboloids (1-sheet or 2-sheets)**

* **Elliptic and Hyperbolic Paraboloids**

* **Cones**

* **Cylinders**

---

## **2. Identifying Quadric Surfaces and Cylinders**

### **Key Standard Forms and Identification**

| Surface Type                  | Standard Equation                                        | Cross Sections                | Notes                  |
| ----------------------------- | -------------------------------------------------------- | ----------------------------- | ---------------------- |
| **Ellipsoid**                 | $` \frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1 `$ | All ellipses                  | Closed surface         |
| **Hyperboloid of One Sheet**  | $` \frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{z^2}{c^2} = 1 `$ | Ellipses, hyperbolas          | Connected              |
| **Hyperboloid of Two Sheets** | $` -\frac{x^2}{a^2} - \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1 `$ | Hyperbolas, no xy-plane trace | Two disconnected parts |
| **Elliptic Paraboloid**       | $` z = \frac{x^2}{a^2} + \frac{y^2}{b^2} `$              | Parabolas & ellipses          | Bowl-shaped            |
| **Hyperbolic Paraboloid**     | $` z = \frac{x^2}{a^2} - \frac{y^2}{b^2} `$               | Hyperbolas & parabolas        | Saddle                 |
| **Elliptic Cone**             | $` \frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{z^2}{c^2} = 0 `$ | Intersects origin             | Like a double cone     |
| **Cylinders**                 | $` \frac{x^2}{a^2} + \frac{y^2}{b^2} = 1 `$               | No z-term                     | Extends infinitely     |

---

## **3. Identifying Quadric Surfaces and Cylinders With Alternative Orientations**

Quadric surfaces can be **rotated** or **shifted** from their standard positions.

### **Tips to Identify Orientation**:

* If $`z`$ is missing: the surface extends **along** the $`z`$-axis → **cylinder**.

* If only one variable is linear: think **paraboloid**.

* If two squares have opposite signs: **hyperboloid**.

* If all terms are squared and positive: **ellipsoid**.

* If $`= 0`$ rather than $`= 1`$: likely a **cone**.

**Example**:

* $`y^2 + z^2 = 1`$ → **cylinder along x-axis**


* $`x^2 + z^2 - y = 0`$ → **elliptic paraboloid, opens along y-axis**

---

## **4. Identifying Quadric Surfaces by Completing the Square**

For non-standard equations, **complete the square** to bring into recognizable form.

### **Example**:

Given:

$$
x^2 + y^2 - 4z + 1 = 0
$$

Rewriting:

$$
x^2 + y^2 = 4z - 1 \Rightarrow z = \frac{1}{4}x^2 + \frac{1}{4}y^2 + \frac{1}{4}
$$

This is an **elliptic paraboloid** opening along the $`z`$-axis.

---

## **5. Summary Table of Surface Features**

| Surface               | Signs                   | Degree                | Example Form              | Traces               |
| --------------------- | ----------------------- |-----------------------|---------------------------|----------------------|
| Ellipsoid             | All positive            | All squared           | $`x^2 + y^2 + z^2 = r^2`$ | Ellipses             |
| Hyperboloid (1-sheet) | One negative            | All squared           | $`x^2 + y^2 - z^2 = 1`$   | Hyperbolas, ellipses |
| Hyperboloid (2-sheet) | Two negative            | All squared           | $`-x^2 - y^2 + z^2 = 1`$  | Hyperbolas           |
| Cone                  | Mixed signs             | All squared, equals 0 | $`x^2 + y^2 - z^2 = 0`$   | Intersects origin    |
| Elliptic paraboloid   | Two squares, one linear | $`z = x^2 + y^2`$     | Parabolas, ellipses       |                      |
| Hyperbolic paraboloid | Opposite signs          | $`z = x^2 - y^2`$     | Saddle                    |                      |
| Cylinder              | Two variables squared   | $`x^2 + y^2 = 1`$     | Infinite length           |                      |

---
