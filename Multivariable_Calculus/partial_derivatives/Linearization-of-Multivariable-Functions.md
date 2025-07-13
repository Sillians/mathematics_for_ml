# **Linearization of Multivariable Functions**

Linear approximation is a fundamental tool in multivariable calculus that allows us to approximate nonlinear functions using linear ones near a specific point. 
This technique is especially useful in physics, engineering, and optimization problems where exact solutions are difficult to obtain.

---

## **1. Linearization of a Two-Variable Function**
Given a differentiable function $`f(x,y)`$, its **linear approximation (or tangent plane approximation)** near a point $`(a,b)`$ is:

$$
L(x,y) = f(a,b) + f_x(a,b)(x - a) + f_y(a,b)(y - b)
$$

where:
- $f_x$ and $f_y$ are the partial derivatives of $f$ with respect to $x$ and $y$, respectively.


- $L(x,y)$ is the linearization of $f$ at $(a,b)$.


### **Example: Approximating $`f(x,y) = \sqrt{x^2 + y^2}`$ near $`(3,4)`$**

1. **Compute $`f(3,4)`$:**
   
$$
f(3,4) = \sqrt{3^2 + 4^2} = 5
$$



2. **Compute partial derivatives:**

$$
f_x = \frac{x}{\sqrt{x^2 + y^2}} \implies f_x(3,4) = \frac{3}{5}
$$

$$
f_y = \frac{y}{\sqrt{x^2 + y^2}} \implies f_y(3,4) = \frac{4}{5}
$$



3. **Write the linear approximation:**

$$
L(x,y) = 5 + \frac{3}{5}(x - 3) + \frac{4}{5}(y - 4)
$$



4. **Use it to estimate $f(3.1, 3.9)$:**

$$
L(3.1, 3.9) \approx 5 + \frac{3}{5}(0.1) + \frac{4}{5}(-0.1) = 5 - 0.02 = 4.98
$$

(The exact value is $`\approx 4.9802`$, so the approximation is good.)

---

## **2. Linearization of a Three-Variable Function**
For a function $`f(x,y,z)`$, the linear approximation at $`(a,b,c)`$ is:

$$
L(x,y,z) = f(a,b,c) + f_x(a,b,c)(x - a) + f_y(a,b,c)(y - b) + f_z(a,b,c)(z - c)
$$


### **Example: Approximating $`f(x,y,z) = x e^{y z}`$ near $`(1,0,2)`$**
1. **Compute $`f(1,0,2)`$:**

$$
f(1,0,2) = 1 \cdot e^{0} = 1
$$


2. **Compute partial derivatives:**

$$
f_x = e^{y z} \implies f_x(1,0,2) = 1
$$

$$
f_y = x z e^{y z} \implies f_y(1,0,2) = 2
$$

$$
f_z = x y e^{y z} \implies f_z(1,0,2) = 0
$$


3. **Write the linear approximation:**

$$
L(x,y,z) = 1 + (1)(x - 1) + (2)(y - 0) + (0)(z - 2) = x + 2y
$$


4. **Use it to estimate \( f(1.1, -0.1, 2.05) \):**

$$
L(1.1, -0.1, 2.05) \approx 1.1 + 2(-0.1) = 0.9
$$

(The exact value is $\approx 0.904$, so the approximation is reasonable.)

---

## **3. Best Linear Approximation**
The **best linear approximation** of a function $f$ at a point $`\mathbf{a}`$ is simply its **first-order Taylor expansion**:

$$
L(\mathbf{x}) = f(\mathbf{a}) + \nabla f(\mathbf{a}) \cdot (\mathbf{x} - \mathbf{a})
$$

where:
- $`\nabla f`$ is the gradient of $f$.

- The approximation is best in the sense that the error $`|f(\mathbf{x}) - L(\mathbf{x})|`$ tends to zero faster than $`\|\mathbf{x} - \mathbf{a}\|`$ as $`\mathbf{x} \to \mathbf{a}`$.


### **Example: Best Linear Approximation of $f(x,y) = \sin(xy)$ at $`(0,0)`$**
1. **Compute $`f(0,0) = 0`$.**


2. **Compute the gradient:**

$$
\nabla f = (y \cos(xy), x \cos(xy)) \implies \nabla f(0,0) = (0, 0)
$$


3. **The best linear approximation is:**

$$
L(x,y) = 0 + 0 \cdot x + 0 \cdot y = 0
$$

(This makes sense because $`\sin(xy) \approx xy`$ near $`(0,0)`$, but the best **linear** approximation is just $0$.)

---

## **Key Takeaways**
1. **Linearization** replaces a nonlinear function with a linear one near a point.


2. **For two variables**, it gives a tangent plane.


3. **For three variables**, it gives a hyperplane.


4. **Best linear approximation** is the first-order Taylor expansion.


5. **Applications** include:
   - Estimating values of functions near known points.
   - Simplifying optimization problems.
   - Error analysis in numerical methods.
