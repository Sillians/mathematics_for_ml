# **Hyperboloids**

---

## **1. Definition of Hyperboloids**

A **hyperboloid** is a type of quadric surface. There are two main types:

* **Hyperboloid of One Sheet:**

$$
\frac{(x - h)^2}{a^2} + \frac{(y - k)^2}{b^2} - \frac{(z - l)^2}{c^2} = 1
$$

* **Hyperboloid of Two Sheets:**

$$
\frac{(z - l)^2}{c^2} - \frac{(x - h)^2}{a^2} - \frac{(y - k)^2}{b^2} = 1
$$

Where:

* $`(h, k, l)`$ is the **center**
* $`a\`$, $`b`$, and $c$ are constants defining the shape

---

## **2. Identifying the Intercepts of a Hyperboloid**

To find the **intercepts**, set two variables to zero and solve for the third.

### **Example:**

For the one-sheet hyperboloid:

$$
\frac{x^2}{9} + \frac{y^2}{4} - \frac{z^2}{16} = 1
$$

### **x-intercepts**: Set $`y = 0`$, $`z = 0`$

$$
\frac{x^2}{9} = 1 \Rightarrow x = \pm 3
$$

### **y-intercepts**: Set $`x = 0`$, $`z = 0`$

$$
\frac{y^2}{4} = 1 \Rightarrow y = \pm 2
$$

### **z-intercepts**: Set $`x = 0`$, $`y = 0`$

$$
-\frac{z^2}{16} = 1 \Rightarrow \text{No real solution}
$$

So, no $`z`$-intercepts exist in this example.

---

## **3. Identifying the Domain of a Hyperboloid**

The **domain** of a hyperboloid typically refers to the **set of valid $`(x, y, z)`$ values** that satisfy the surface equation.

For **explicitly defined functions**, solve for the variable and identify constraints.

### **Example** (solve for $z$):

Given:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{z^2}{c^2} = 1
$$

Then,

$$
z = \pm c \sqrt{\frac{x^2}{a^2} + \frac{y^2}{b^2} - 1}
$$

Domain of $z$ exists when:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} \geq 1
$$

For the **two-sheet** case, the domain is typically defined **only where the RHS stays positive**, so the **radical is real**.

---

## **4. Finding Traces of Hyperboloids**

A **trace** is the curve obtained by intersecting the surface with a plane (e.g., $`x = k`$, $`y = k`$, or $`z = k`$).

---

### **Hyperboloid of One Sheet**

#### **Trace in the $`xy`$-plane** ($`z = 0`$):

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1 \quad \Rightarrow \text{Ellipse}
$$

#### **Trace in $`xz`$- or $`yz`$-plane**:

$$
\frac{x^2}{a^2} - \frac{z^2}{c^2} = 1 \quad \Rightarrow \text{Hyperbola}
$$

---

### **Hyperboloid of Two Sheets**

#### **Trace in the $`xy`$-plane** ($`z = 0`$):

$$
-\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1 \Rightarrow \text{No Real Points}
$$

#### **Trace in $`xz`$ or $`yz`$ plane**:

$$
\frac{z^2}{c^2} - \frac{x^2}{a^2} = 1 \Rightarrow \text{Hyperbola}
$$

The **plane that includes the positive term** generally yields a **hyperbola**.

---

## **Summary Table**

| Property                | One-Sheet Hyperboloid                                     | Two-Sheet Hyperboloid                                     |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| General Form            | $`\frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{z^2}{c^2} = 1`$ | $`\frac{z^2}{c^2} - \frac{x^2}{a^2} - \frac{y^2}{b^2} = 1`$ |
| Trace in $xy$-plane     | Ellipse                                                   | Empty                                                     |
| Trace in $xz$ or $yz$   | Hyperbola                                                 | Hyperbola                                                 |
| Domain (if solving for $z$) | $`\frac{x^2}{a^2} + \frac{y^2}{b^2} \geq 1`$               | $`\frac{z^2}{c^2} \geq 1`$                                 |
| Intercepts              | May be partial (not all axes)                             | Depends on configuration                                  |

---
