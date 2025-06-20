# **Ellipsoids**

---

## **1. Definition of an Ellipsoid**

An **ellipsoid** is a 3D surface represented by the equation:

$$
\frac{(x - h)^2}{a^2} + \frac{(y - k)^2}{b^2} + \frac{(z - l)^2}{c^2} = 1
$$

* Center: $`(h, k, l)`$
* Axes lengths: $`2a`$, $`2b`$, and $`2c`$
* If $`a = b = c`$, the ellipsoid becomes a **sphere**

---

## **2. Identifying the Center and Radius of a Sphere**

A **sphere** is a special ellipsoid where all axes are equal. It has the form:

$$
(x - h)^2 + (y - k)^2 + (z - l)^2 = r^2
$$

* Center: $`(h, k, l)`$
* Radius: $`r`$

### **Example:**

Given:

$$
(x + 2)^2 + (y - 1)^2 + (z - 3)^2 = 25
$$

* Center: $`(-2, 1, 3)`$
* Radius: $`\sqrt{25} = 5`$

---

## **3. Calculating Intercepts of Spheres and Ellipsoids**

To find **intercepts**, set two variables to 0 and solve for the third:

For ellipsoid:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1
$$

### **x-intercepts** (set $`y = 0`$, $`z = 0`$):

$$
\frac{x^2}{a^2} = 1 \Rightarrow x = \pm a
$$

### **y-intercepts**: $`y = \pm b`$

### **z-intercepts**: $`z = \pm c`$

These points are where the ellipsoid intersects the axes.

---

## **4. The Domain of a Sphere or Ellipsoid**

The **domain** consists of all real points $`(x, y, z)`$ that satisfy the ellipsoid inequality:

$$
\frac{(x - h)^2}{a^2} + \frac{(y - k)^2}{b^2} + \frac{(z - l)^2}{c^2} \leq 1
$$

For the function:

$$
f(x, y, z) = \sqrt{1 - \frac{(x - h)^2}{a^2} - \frac{(y - k)^2}{b^2} - \frac{(z - l)^2}{c^2}}
$$

Domain:

$$
\frac{(x - h)^2}{a^2} + \frac{(y - k)^2}{b^2} + \frac{(z - l)^2}{c^2} \leq 1
$$

---

## **5. Describing Traces of Ellipsoids**

To find **traces**, set one variable constant.

### **Trace in the $`xy`$-plane** (set $`z = z\_0`$):

From:

$$
\frac{(x - h)^2}{a^2} + \frac{(y - k)^2}{b^2} + \frac{(z - l)^2}{c^2} = 1
$$

Substitute $`z = z\_0`$:

$$
\frac{(x - h)^2}{a^2} + \frac{(y - k)^2}{b^2} = 1 - \frac{(z_0 - l)^2}{c^2}
$$

* If the right-hand side is **positive**, the trace is an **ellipse**.
* If it's **zero**, the trace is a **point**.
* If it's **negative**, the trace is **empty** (no intersection).

---

## **Summary Table**

| Feature          | Ellipsoid                                                           | Sphere                                    |
| ---------------- | ------------------------------------------------------------------- | ----------------------------------------- |
| General Equation | $`\frac{(x-h)^2}{a^2} + \frac{(y-k)^2}{b^2} + \frac{(z-l)^2}{c^2} = 1`$ | $`(x - h)^2 + (y - k)^2 + (z - l)^2 = r^2`$ |
| Center           | $`(h, k, l)`$                                                        | $`(h, k, l)`$                              |
| Axes Lengths     | $`2a, 2b, 2c`$                                                       | $`2r`$                                     |
| Traces           | Usually ellipses                                                    | Circles or points                         |
| Domain           | 3D region enclosed by ellipsoid                                     | Solid sphere                              |

---
