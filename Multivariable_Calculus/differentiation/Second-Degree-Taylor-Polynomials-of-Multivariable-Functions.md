## **Second‑Degree Taylor Polynomials of Multivariable Functions**

---

### **1. Conceptual Framework**

| Notation                              | Meaning                                      |
|---------------------------------------|----------------------------------------------|
| $`f:\mathbb{R}^{n}\!\to\!\mathbb{R}`$ | Twice continuously differentiable scalar field |
| $`\mathbf{a}\in\mathbb{R}^{n}`$       | Expansion (anchor) point                     |
| $`\mathbf{x}\in\mathbb{R}^{n}`$       | Evaluation point                             |
| $`\mathbf{h}=\mathbf{x}-\mathbf{a}`$  | Displacement vector                          |
| $`\nabla f(\mathbf{a})`$              | Gradient at $`\mathbf{a}`$                   |
| $`H_f(\mathbf{a})`$                   | Hessian (symmetric) at $`\mathbf{a}`$        |

The **quadratic (second‑degree) Taylor polynomial** provides the best local quadratic approximation:

$$
T_2f(\mathbf{x};\mathbf{a}) \;=\;
f(\mathbf{a}) \;+\; \nabla f(\mathbf{a})^{\!\top}\mathbf{h}
\;+\;
\frac{1}{2}\,\mathbf{h}^{\!\top} H_f(\mathbf{a})\,\mathbf{h}.
$$

---

### **2. Deriving the Quadratic Taylor Polynomial (Matrix Form)**

1. **Start with one‑dimensional Taylor’s theorem**:
   $`f(t)\approx f(0)+f'(0)t+\tfrac12f''(0)t^{2}`$.


2. **Generalise via multivariable chain rule** using
   $`g(t)=f(\mathbf{a}+t\mathbf{h})$ with $g(0)=f(\mathbf{a})`$.
   Compute $`g'(0)=\nabla f(\mathbf{a})^{\!\top}\mathbf{h}`$ and
   $`g''(0)=\mathbf{h}^{\!\top}H_f(\mathbf{a})\mathbf{h}`$.


3. **Insert into 1‑D formula** with $`t=1`$ ⇒ matrix expression above.


4. **Error term**: $`f(\mathbf{x}) = T_2f(\mathbf{x};\mathbf{a}) + o(\lVert\mathbf{h}\rVert^{2})`$.

---

### **3. Building the Quadratic Taylor Polynomial (Component Form)**

For $`n=2`$ with $`(x,y)`$ near $`(a,b)`$:

$$
\begin{aligned}
T_2f(x,y)
&= f(a,b) + f_x(a,b)(x-a) + f_y(a,b)(y-b) \\
&\quad + \frac12 f_{xx}(a,b)(x-a)^2 + f_{xy}(a,b)(x-a)(y-b) + \frac12 f_{yy}(a,b)(y-b)^2.
\end{aligned}
$$

Mixed term coefficient equals $`f_{xy}=f_{yx}`$ thanks to Clairaut’s theorem.

---

### **4. Constructing a Quadratic Taylor Polynomial – Worked Example**

Given data at $`\mathbf{a}=(1,1)`$:

| Quantity        | Value                                    |
| --------------- |------------------------------------------|
| $`f(1,1)`$        | $3$                                      |
| $`\nabla f(1,1)`$ | $`\begin{bmatrix}2\\-1\end{bmatrix}`$    |
| $`H_f(1,1)`$      | $`\begin{bmatrix}4&1\\1&2\end{bmatrix}`$ |

**Polynomial**

$$
T_2f(x,y)=
3+
\begin{bmatrix}2&-1\end{bmatrix}
\begin{bmatrix}x-1\y-1\end{bmatrix}
+\tfrac12
\begin{bmatrix}x-1&y-1\end{bmatrix}
\!\begin{bmatrix}4&1\1&2\end{bmatrix}\!
\begin{bmatrix}x-1\y-1\end{bmatrix}.
$$

Simplified form (expand if desired).

---

### **5. Approximating a Function Value via the Quadratic Polynomial**

**Task**: estimate $`f(1.1,0.9)`$ using the polynomial above.

1. **Displacement**: $`\mathbf{h}=(0.1,-0.1)`$.


2. **Linear term**: $`\nabla f^{\!\top}\mathbf{h}=2(0.1)+(-1)(-0.1)=0.30`$.


3. **Quadratic term**:


$$
\tfrac12\,\mathbf{h}^{\!\top}H\mathbf{h}
=\tfrac12\begin{bmatrix}0.1&-0.1\end{bmatrix}
\begin{bmatrix}0.3\\-0.1\end{bmatrix}
=\tfrac12(0.04)=0.02.
$$


4. **Approximation**: $`T_2f(1.1,0.9)=3+0.30+0.02=3.32`$.

---

### **6. Summary Table**

| Step                                                     | Action                                                |
|----------------------------------------------------------| ----------------------------------------------------- |
| Evaluate $`f,\nabla f,H_f`$ at base point $`\mathbf{a}`$ | Gather constants                                      |
| Form $`\mathbf{h}=\mathbf{x}-\mathbf{a}`$                | Displacement                                          |
| Compute linear term                                      | $`\nabla f(\mathbf{a})^{\!\top}\mathbf{h}`$             |
| Compute quadratic term                                   | $`\frac12\mathbf{h}^{\!\top}H_f(\mathbf{a})\mathbf{h}`$ |
| Sum with $`f(\mathbf{a})`$                               | Quadratic approximation                               |

---

### **Key Insights**

* The **matrix form** $`f(\mathbf{a})+\nabla f^{\!\top}\mathbf{h}+\frac12\mathbf{h}^{\!\top}H\mathbf{h}`$ is dimension‑independent and computationally efficient.


* Second‑degree terms capture **curvature**, delivering markedly better local accuracy than the linear (first‑degree) model.


* In optimisation, the Hessian within the Taylor polynomial aids **Newton‑type methods** and **critical‑point classification**.
