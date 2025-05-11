## **Tangent Vectors and Tangent Lines to Curves**

Tangent vectors and tangent lines describe the **instantaneous direction and behavior** of a 
curve at a given point in space. They're essential in calculus, physics, and geometry for 
understanding motion, slope, and interaction between vector fields.

---

### **1. Finding a Tangent Vector**

Given a vector-valued function (curve):

$$
\mathbf{r}(t) = \langle x(t), y(t), z(t) \rangle
$$

The **tangent vector** at time $t$ is the **derivative**:

$$
\mathbf{r}'(t) = \left\langle x'(t), y'(t), z'(t) \right\rangle
$$

This vector points in the direction the curve is moving at that instant.

---

#### **Example:**

$$
\mathbf{r}(t) = \langle t^2, \sin t, e^t \rangle
\Rightarrow
\mathbf{r}'(t) = \langle 2t, \cos t, e^t \rangle
$$

---

### **2. Finding a Tangent Line to a Curve**

The **tangent line** to the curve at point $\mathbf{r}(t_0)$ is the line:

$$
\mathbf{L}(t) = \mathbf{r}(t_0) + s \cdot \mathbf{r}'(t_0)
$$

Where:

* $\mathbf{r}(t_0)$ is the **point on the curve**,
* $\mathbf{r}'(t_0)$ is the **tangent vector**,
* $s \in \mathbb{R}$ is a scalar parameter for the line.

---

#### **Example:**

If $\mathbf{r}(t) = \langle t, t^2 \rangle$, then at $t = 1$:

* $\mathbf{r}(1) = \langle 1, 1 \rangle$
* $\mathbf{r}'(t) = \langle 1, 2t \rangle \Rightarrow \mathbf{r}'(1) = \langle 1, 2 \rangle$

So the **tangent line** is:

$$
\mathbf{L}(s) = \langle 1, 1 \rangle + s \cdot \langle 1, 2 \rangle = \langle 1 + s, 1 + 2s \rangle
$$

---

### **3. Finding Points Where a Tangent Vector is Perpendicular to Another Vector**

Two vectors are **perpendicular** (orthogonal) if their **dot product is zero**:

$$
\mathbf{r}'(t) \cdot \mathbf{v} = 0
$$

Solve this equation to find the value(s) of $t$ where the tangent vector is perpendicular to $\mathbf{v}$.

---

#### **Example:**

Let $\mathbf{r}(t) = \langle t, t^2 \rangle$, and find when the tangent is perpendicular to $\mathbf{v} = \langle 1, 1 \rangle$

$$
\mathbf{r}'(t) = \langle 1, 2t \rangle
\Rightarrow \langle 1, 2t \rangle \cdot \langle 1, 1 \rangle = 1 + 2t = 0 \Rightarrow t = -\tfrac{1}{2}
$$

---

### **4. Finding Points Where a Tangent Vector is Parallel to Another Vector**

Two vectors are **parallel** if one is a **scalar multiple** of the other:

$$
\mathbf{r}'(t) = k \cdot \mathbf{v}
$$

This gives a system of equations to solve for $t$ and the scalar $k$.

---

#### **Example:**

Let $\mathbf{r}(t) = \langle t^2, 3t \rangle$, and find when the tangent is parallel to $\mathbf{v} = \langle 2, 3 \rangle$

* $\mathbf{r}'(t) = \langle 2t, 3 \rangle$
* Set $\langle 2t, 3 \rangle = k \cdot \langle 2, 3 \rangle = \langle 2k, 3k \rangle$

So:

$$
2t = 2k \Rightarrow k = t, \quad 3 = 3k \Rightarrow k = 1 \Rightarrow t = 1
$$

---

### ✅ **Summary Table**

| Concept                              | Method                                       |
| ------------------------------------ | -------------------------------------------- |
| **Tangent Vector**                   | Derivative: $\mathbf{r}'(t)$                 |
| **Tangent Line**                     | $\mathbf{r}(t_0) + s \cdot \mathbf{r}'(t_0)$ |
| **Tangent ⟂ to vector $\mathbf{v}$** | $\mathbf{r}'(t) \cdot \mathbf{v} = 0$        |
| **Tangent ∥ to vector $\mathbf{v}$** | $\mathbf{r}'(t) = k \cdot \mathbf{v}$        |

---

Understanding tangent vectors and lines is fundamental for describing motion, curvature, optimization, and directionality in multivariable calculus and vector calculus.
