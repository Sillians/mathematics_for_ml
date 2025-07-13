## **Directional Derivatives**

---

### **1. What Is a Directional Derivative?**

The **directional derivative** of a scalar-valued multivariable function measures the rate of change of the function at a point in a specified direction.

If $`f: \mathbb{R}^n \to \mathbb{R}`$, and $`\vec{u} \in \mathbb{R}^n`$ is a **unit vector**, 
then the **directional derivative** of $f$ at point $`\vec{a}`$ in the direction of $`\vec{u}`$ is:


$$
D_{\vec{u}} f(\vec{a}) = \nabla f(\vec{a}) \cdot \vec{u}
$$


Where:

* $`\nabla f(\vec{a})`$ is the **gradient** of $f$ at $`\vec{a}`$


* $`\vec{u}`$ is the **unit vector** in the desired direction


* $`\cdot`$ denotes the **dot product**

---

### **2. Calculating a Directional Derivative**

**Step-by-Step:**

1. Compute the **gradient vector** of $f$:

$$
\nabla f(x, y) = \left\langle \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right\rangle
$$


2. Evaluate the gradient at the point $`\vec{a}`$.


3. Normalize the direction vector $`\vec{v}`$ to get unit vector $`\vec{u} = \frac{\vec{v}}{\|\vec{v}\|}`$.


4. Compute the dot product:


$$
D_{\vec{u}} f(\vec{a}) = \nabla f(\vec{a}) \cdot \vec{u}
$$

**Example:**

Let $`f(x, y) = x^2 y + y^2`$, find $`D_{\vec{v}} f(1, 2)`$ in direction $`\vec{v} = \langle 3, 4 \rangle`$:


* $`\nabla f = \langle 2xy, x^2 + 2y \rangle \Rightarrow \nabla f(1,2) = \langle 4, 5 \rangle`$


* Unit vector: $`\vec{u} = \frac{1}{5} \langle 3, 4 \rangle`$


* Dot product: $`D_{\vec{u}} f(1,2) = \langle 4, 5 \rangle \cdot \frac{1}{5} \langle 3, 4 \rangle = \frac{1}{5}(12 + 20) = \frac{32}{5}`$

---

### **3. Direction of Maximum Increase or Decrease**

* The **direction of maximum increase** of a function at a point is the direction of the **gradient vector** $`\nabla f`$ at that point.


* The **magnitude** of the gradient $`\| \nabla f \|`$ gives the **maximum rate of increase**.


* The **direction of maximum decrease** is **opposite** the gradient, i.e., $`-\nabla f`$.


$$
\text{Maximum increase: } \vec{u} = \frac{\nabla f}{\|\nabla f\|}, \quad D_{\vec{u}} f = \|\nabla f\|
$$

$$
\text{Maximum decrease: } \vec{u} = -\frac{\nabla f}{\|\nabla f\|}, \quad D_{\vec{u}} f = -\|\nabla f\|
$$

---

### **4. Finding the Rate of Change of a Function in a Given Direction**

Let $` f: \mathbb{R}^n \to \mathbb{R} `$, and $`   \vec{v} \in \mathbb{R}^n   `$ be **any** direction vector (not necessarily unit length). Then:

$$
\text{Rate of change of } f \text{ at } \vec{a} \text{ in direction } \vec{v} =
\boxed{
\nabla f(\vec{a}) \cdot \frac{\vec{v}}{\|\vec{v}\|}
}
$$

Or equivalently:

$$
\text{Rate of change } = \|\nabla f(\vec{a})\| \cdot \cos \theta
$$

where $`\theta`$ is the angle between $`\nabla f(\vec{a})`$ and $`\vec{v}`$.

---

### **5. Summary**

| Concept                   | Formula                                                                                                    |
| ------------------------- | ---------------------------------------------------------------------------------------------------------- |
| Gradient                  | $`\nabla f(x, y) = \left\langle \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right\rangle`$ |
| Directional Derivative    | $`D_{\vec{u}} f(\vec{a}) = \nabla f(\vec{a}) \cdot \vec{u}`$                                                 |
| Max Rate of Increase      | $`\|\nabla f(\vec{a})\|`$                                                                                    |
| Direction of Max Increase | $`\frac{\nabla f(\vec{a})}{\|\nabla f(\vec{a})\|}`$                                                          |
| Direction of Max Decrease | $`-\frac{\nabla f(\vec{a})}{\|\nabla f(\vec{a})\|}`$                                                         |

The directional derivative reveals how a multivariable function changes in any chosen direction 
and connects tightly to gradients, which encode the function's most sensitive direction of change.
