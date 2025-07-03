## **The Second Derivative of a Multivariable Function**

---

### **1. Overview**

In multivariable calculus, the **second derivative** of a scalar-valued function provides information 
about the **curvature**, **concavity**, and **local behavior** of the function. 
It generalizes the second derivative in single-variable calculus to higher dimensions using the **Hessian matrix**.

Let $`f:\mathbb{R}^n \to \mathbb{R}`$ be a scalar-valued function.

* The **gradient** is a vector of first-order partials:

  $$
  \nabla f(x) = \begin{bmatrix}
  \frac{\partial f}{\partial x_1} \\
  \vdots \\
  \frac{\partial f}{\partial x_n}
  \end{bmatrix}
  $$

* The **second derivative** is the **Hessian matrix**, denoted:

  $$
  H_f(x) = \left[ \frac{\partial^2 f}{\partial x_i \partial x_j} \right]_{i,j=1}^{n}
  $$

---

### **2. Finding the Second Derivative Given the First Derivative**

Suppose the gradient $`f'(x) = \nabla f(x)`$ is known.

To obtain the second derivative:

1. Compute partial derivatives of each component of the gradient.
2. The result is a symmetric matrix of second-order partial derivatives.

#### **Example**

Given:

$$
f'(x, y) = \nabla f(x, y) = \begin{bmatrix}
y \cos(xy) \\
x \cos(xy)
\end{bmatrix}
$$

Then the Hessian matrix is:

$$
H_f(x, y) = \begin{bmatrix}
\frac{\partial^2 f}{\partial x^2} & \frac{\partial^2 f}{\partial x \partial y} \\
\frac{\partial^2 f}{\partial y \partial x} & \frac{\partial^2 f}{\partial y^2}
\end{bmatrix}
= \begin{bmatrix}
f_{xx} & f_{xy} \\
f_{yx} & f_{yy}
\end{bmatrix}
$$

Each entry is computed by differentiating the appropriate gradient component.

---

### **3. Finding the Second Derivative of a Function**

Let $`f:\mathbb{R}^2 \to \mathbb{R}`$. The second-order partial derivatives are:

* $`f\_{xx} = \dfrac{\partial^2 f}{\partial x^2}`$
* $`f\_{yy} = \dfrac{\partial^2 f}{\partial y^2}`$
* $`f\_{xy} = \dfrac{\partial^2 f}{\partial x \partial y} = f\_{yx}`$ (under mild smoothness conditions)

The Hessian matrix is:

$$
H_f(x, y) =
\begin{bmatrix}
f_{xx} & f_{xy} \\
f_{yx} & f_{yy}
\end{bmatrix}
$$

#### **Example**

Let $`f(x, y) = x^2 y + \sin(xy)`$.

First derivatives:

$$
f_x = 2xy + y \cos(xy), \quad
f_y = x^2 + x \cos(xy)
$$

Second derivatives:

$$
f_{xx} = 2y - y^2 \sin(xy), \quad
f_{yy} = -x^2 \sin(xy), \quad
f_{xy} = 2x + \cos(xy) - xy \sin(xy)
$$

So:

$$
H_f(x, y) =
\begin{bmatrix}
2y - y^2 \sin(xy) & 2x + \cos(xy) - xy \sin(xy) \\
2x + \cos(xy) - xy \sin(xy) & -x^2 \sin(xy)
\end{bmatrix}
$$

---

### **4. Evaluating a Hessian Determinant**

The **Hessian determinant** (for functions of 2 variables) is:

$$
\det(H_f(x, y)) = f_{xx} f_{yy} - (f_{xy})^2
$$

This determinant helps in **second derivative tests** for local extrema:

| Condition                      | Interpretation    |
|--------------------------------| ----------------- |
| $`D > 0`$ and $`f\_{xx} > 0`$  | Local **minimum** |
| $`D > 0`$ and $`f\_{xx} < 0`$  | Local **maximum** |
| $`D < 0`$                      | **Saddle point**  |
| $`D = 0`$                      | Inconclusive      |

#### **Example**

From earlier:

$$
H_f(x, y) = \begin{bmatrix}
0 & -1 \\
-1 & 0
\end{bmatrix}
\quad \Rightarrow \quad
\det(H_f) = 0 \cdot 0 - (-1)^2 = -1
\quad \text{(saddle point)}
$$

---

### **Summary Table**

| Concept             | Object                      | Description                                        |
| ------------------- |-----------------------------| -------------------------------------------------- |
| First derivative    | Gradient $`\nabla f`$       | Vector of partial derivatives                      |
| Second derivative   | Hessian $`H_f`$             | Matrix of second-order partials                    |
| Hessian entry       | $`f_{ij}`$                  | $`\frac{\partial^2 f}{\partial x_i \partial x_j}`$ |
| Hessian determinant | $`f_{xx}f_{yy} - f_{xy}^2`$ | Used for classifying critical points               |

---

The second derivative in multivariable calculus provides a matrix-based framework for understanding 
curvature and local behavior. It plays a crucial role in optimization, especially for identifying 
and classifying local extrema and saddle points.
