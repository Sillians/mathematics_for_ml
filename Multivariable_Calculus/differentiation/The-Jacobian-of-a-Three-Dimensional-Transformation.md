## **The Jacobian of a Three-Dimensional Transformation**

---

### **1. The Jacobian in 3D: Overview**

In multivariable calculus, the **Jacobian matrix** generalizes the concept of a derivative to functions from $`\mathbb{R}^n \to \mathbb{R}^m`$. 
For a **three-dimensional transformation**:

$$
\mathbf{T}(u, v, w) = \left( x(u, v, w),\; y(u, v, w),\; z(u, v, w) \right)
$$

the **Jacobian matrix** is the 3×3 matrix of all first-order partial derivatives:

$$
J_{\mathbf{T}}(u, v, w) =
\begin{bmatrix}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} & \frac{\partial x}{\partial w} \\
\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v} & \frac{\partial y}{\partial w} \\
\frac{\partial z}{\partial u} & \frac{\partial z}{\partial v} & \frac{\partial z}{\partial w}
\end{bmatrix}
$$

The **Jacobian determinant**:

$$
\det(J_{\mathbf{T}}(u, v, w))
$$

gives the **local volume scale factor** of the transformation at a point. It also tells whether the transformation preserves or reverses orientation.

---

### **2. Finding the Jacobian of a Three-Dimensional Transformation**

**Steps:**

1. Let $`\mathbf{T}(u, v, w) = (x(u, v, w), y(u, v, w), z(u, v, w))`$
2. Compute all 9 partial derivatives: $`\partial x/\partial u`$, $`\partial y/\partial v`$, etc.
3. Form the 3×3 Jacobian matrix.
4. Compute its determinant.

**Example:**

Let

$$
x = uv,\quad y = vw,\quad z = wu
$$

Then the Jacobian matrix is:

$`J = \begin{bmatrix} \frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} & \frac{\partial x}{\partial w} \\ \frac{\partial y}{\partial u} & \frac{\partial y}{\partial v} & \frac{\partial y}{\partial w} \\ \frac{\partial z}{\partial u} & \frac{\partial z}{\partial v} & \frac{\partial z}{\partial w} \end{bmatrix} = \begin{bmatrix} v & u & 0 \\ 0 & w & v \\ w & 0 & u \end{bmatrix}`$


$$
\det(J) = v(wu - 0) - u(0 \cdot u - v \cdot w) + 0 = vwu + uvw = 2uvw
$$

---

### **3. Determining the Critical Points of a Transformation**

A **critical point** of a transformation $`\mathbf{T}(u, v, w)`$ is where the **Jacobian determinant vanishes**:

$$
\det(J_{\mathbf{T}}(u, v, w)) = 0
$$

At critical points:

* The transformation **fails to be locally invertible**.
* The mapping may collapse volume (like folding or projection).

**Example:**

In the previous example with $`\det(J) = 2uvw`$, the critical points are where any of $`u = 0`$, $`v = 0`$, or $`w = 0`$. 
At these points, the transformation flattens (loses dimension).

---

### **4. Finding the Jacobian of an Inverse Transformation**

Let $`\mathbf{T}: \mathbb{R}^3 \to \mathbb{R}^3`$ be a **smooth and invertible** transformation with inverse $`\mathbf{T}^{-1}`$. Then:

$$
J_{\mathbf{T}^{-1}}(x, y, z) = \left[J_{\mathbf{T}}(u, v, w)\right]^{-1}
\quad \text{and} \quad
\det(J_{\mathbf{T}^{-1}}) = \frac{1}{\det(J_{\mathbf{T}})}
$$

**Important:** To compute this, you must:

* Find the inverse transformation explicitly.
* Substitute the inverse expressions into the Jacobian of the inverse.

**Example:**

Let

$$
x = u + v + w,\quad y = u - v + w,\quad z = u + v - w
$$

Solving for $`u, v, w`$, you can compute the inverse transformation $`\mathbf{T}^{-1}(x, y, z)`$, then calculate the Jacobian matrix of this inverse transformation.

---

### **Summary Table**

| Concept                      | Expression or Condition                                                       |                  
| ---------------------------- |-------------------------------------------------------------------------------|
| Jacobian Matrix              | $`J_{\mathbf{T}} = \left[\frac{\partial(x, y, z)}{\partial(u, v, w)}\right]`$ |                                                 
| Jacobian Determinant         | $`\det(J_{\mathbf{T}})`$                                                      |                                                 
| Local Volume Scale Factor    | Absolute value: ($`\det(J\_{\mathbf{T})}`$ )                                  |   
| Critical Points              | $`\det(J_{\mathbf{T}}) = 0`$                                                  |                                               
| Inverse Jacobian Determinant | $`\det(J_{\mathbf{T}^{-1}}) = 1/\det(J_{\mathbf{T}})`$                        |                                                 

This framework is essential for changing variables in triple integrals,
analyzing nonlinear maps, and solving PDEs involving coordinate transformations.
