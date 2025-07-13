## **The Derivative of a Multivariable Function**

---

### **1. Overview**

In multivariable calculus, the derivative generalizes the concept of a slope to higher dimensions. 
The derivative of a multivariable function describes the best linear approximation to the function at a point. 
Depending on the output dimension of the function, the derivative takes the form of either a **gradient vector** or a **Jacobian matrix**.

Let:

* Scalar function: $`f:\mathbb{R}^n \to \mathbb{R}`$
* Vector function: $`\mathbf{F}:\mathbb{R}^n \to \mathbb{R}^m`$

---

### **2. Finding the Derivative of a Scalar Function**

Given a function $`f:\mathbb{R}^n \to \mathbb{R}`$, the derivative at point $`x \in \mathbb{R}^n`$ is the **gradient**:

#### **Gradient Vector**

$$
\nabla f(x) = \begin{bmatrix}
\frac{\partial f}{\partial x_1}(x) \\
\frac{\partial f}{\partial x_2}(x) \\
\vdots \\
\frac{\partial f}{\partial x_n}(x)
\end{bmatrix}
$$

This gradient points in the direction of the **steepest ascent** of the function at that point.

#### **Example**

Let $`f(x, y) = x^2y + \sin(xy)`$.

Then:

$$
\frac{\partial f}{\partial x} = 2xy + y\cos(xy), \quad
\frac{\partial f}{\partial y} = x^2 + x\cos(xy)
$$

$$
\Rightarrow \nabla f(x, y) = \begin{bmatrix}
2xy + y\cos(xy) \\
x^2 + x\cos(xy)
\end{bmatrix}
$$

---

### **3. Finding the Derivative of a Vector Function**

Given $`\mathbf{F}:\mathbb{R}^n \to \mathbb{R}^m`$ where $`\mathbf{F}(x) = (F_1(x), F_2(x), \dots, F_m(x))`$, the derivative is the **Jacobian matrix**:

#### **Jacobian Matrix**

$$
J_{\mathbf{F}}(x) =
\begin{bmatrix}
\frac{\partial F_1}{\partial x_1} & \cdots & \frac{\partial F_1}{\partial x_n} \\
\vdots & \ddots & \vdots \\
\frac{\partial F_m}{\partial x_1} & \cdots & \frac{\partial F_m}{\partial x_n}
\end{bmatrix}
\in \mathbb{R}^{m \times n}
$$

Each row is the gradient of a scalar component $`F_i`$.

#### **Example**

Let $`\mathbf{F}(x, y, z) = (xy, e^{xz}, x + y + z)`$.

Then:

$$
J_{\mathbf{F}}(x, y, z) = \begin{bmatrix}
y & x & 0 \\
ze^{xz} & 0 & xe^{xz} \\
1 & 1 & 1
\end{bmatrix}
$$

---

### **4. Finding the Tangent Plane to the Graph of a Scalar Function (Matrix Form)**

Let $`f:\mathbb{R}^n \to \mathbb{R}`$ be differentiable, and let $`x_0 \in \mathbb{R}^n`$. The **graph** of $`f`$ is the set:

$$
\text{Graph}(f) = \left\{\begin{bmatrix} x \\ f(x) \end{bmatrix} \in \mathbb{R}^{n+1} \right\}
$$


$$
\text{Graph}(f) = \left\{\begin{bmatrix} x \\ f(x) \end{bmatrix} \in \mathbb{R}^{n+1} \right\}
$$


Define an augmented function:

$$
\tilde{f}(x) = \begin{bmatrix} x \\ f(x) \end{bmatrix}
$$

Then, the Jacobian of $`\tilde{f}`$ is:

$$
J_{\tilde{f}}(x_0) = \begin{bmatrix}
I_n \\
\nabla f(x_0)^\top
\end{bmatrix}
\in \mathbb{R}^{(n+1) \times n}
$$

The **tangent plane** at point $`(x_0, f(x_0))`$ is the image of:

$$
\tilde{f}(x_0) + J_{\tilde{f}}(x_0)h \quad \text{for} \quad h \in \mathbb{R}^n
$$

Which gives:

$$
\text{Tangent plane:} \quad 
\left\{ 
\left(x_0 + h,\; f(x_0) + \nabla f(x_0)^\top h\right) 
\;\middle|\; 
h \in \mathbb{R}^n 
\right\}
$$


---

### **5. Finding an Affine Approximation of a Vector Function**

Given a differentiable vector-valued function $`\mathbf{F}:\mathbb{R}^n \to \mathbb{R}^m`$, we can approximate $`\mathbf{F}(x)`$ near a point $`x_0`$ by its **first-order Taylor expansion**:

$$
\mathbf{F}(x_0 + h) \approx \mathbf{F}(x_0) + J_{\mathbf{F}}(x_0) \cdot h
$$

This is the **best affine (linear) approximation** of $`\mathbf{F}`$ near $`x_0`$, where:

* $`\mathbf{F}(x_0)`$ is the constant offset
* $`J_{\mathbf{F}}(x_0)`$ is the linear part (Jacobian)

#### **Affine Approximation Form**

$$
\mathbf{F}(x) \approx \mathbf{F}(x_0) + J_{\mathbf{F}}(x_0)(x - x_0)
$$

#### **Interpretation**:

This gives a local linear model of $`\mathbf{F}`$, accurate up to first order. The error in this approximation goes to zero faster than $`\|x - x_0\|`$ as $`x \to x_0`$:

$$
\lim_{x \to x_0} \frac{\|\mathbf{F}(x) - \mathbf{F}(x_0) - J_{\mathbf{F}}(x_0)(x - x_0)\|}{\|x - x_0\|} = 0
$$

---

### **Summary Table**

| Concept                                 | Object              | Notation                                       | Description                            |
| --------------------------------------- | ------------------- | ---------------------------------------------- | -------------------------------------- |
| Derivative of scalar function           | Gradient            | $`\nabla f(x)`$                                | Column vector of partial derivatives   |
| Derivative of vector function           | Jacobian            | $`J_{\mathbf{F}}(x)`$                          | Matrix of partial derivatives          |
| Tangent plane to scalar function        | $`\text{Graph}(f)`$ | $`\{(x, f(x))\}`$                              | Linear surface approximating the graph |
| Affine approximation of vector function | Linear + constant   | $`\mathbf{F}(x_0) + J_{\mathbf{F}}(x_0)(x - x_0)`$ | First-order Taylor expansion           |

---

This framework generalizes the idea of derivatives and tangent lines to high-dimensional and multivariable settings, providing the foundation for optimization, 
approximation, and analysis in vector calculus and differential geometry.
