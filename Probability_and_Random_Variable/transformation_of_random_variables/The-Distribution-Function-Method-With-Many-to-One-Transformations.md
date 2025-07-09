## **The Distribution Function Method With Many-to-One Transformations**

---

### **1. Overview: Transformations of Random Variables**

Transforming random variables allows one to derive the distribution of a new variable $`Z = g(X, Y)`$, 
where $g$ is a **function** of one or more random variables. The goal is to find the probability distribution 
(PDF or CDF) of $Z$.


The **distribution function method** is a general and powerful approach that applies whether the transformation 
is one-to-one or many-to-one.

---

### **2. The Distribution Function Method**

To find the cumulative distribution function (CDF) of $`Z = g(X, Y)`$, use:

$$
F_Z(z) = P(Z \leq z) = P(g(X, Y) \leq z)
$$

This is a **geometric probability** over the region:

$$
A(z) = \{(x, y) \mid g(x, y) \leq z\}
$$

So,

$$
F_Z(z) = \iint_{A(z)} f_{X,Y}(x, y) \, dx\,dy
$$

To get the PDF $`f_Z(z)`$, differentiate:

$$
f_Z(z) = \frac{d}{dz} F_Z(z)
$$

---

### **3. One-to-One vs Many-to-One Transformations**

#### **One-to-One Transformation**

If $`Z = g(X, Y)`$ is **invertible**, and the inverse $`(X, Y) = g^{-1}(Z)`$ exists uniquely for each $z$, then:


* The **Jacobian method** is often preferred (change-of-variables).


* Direct integration using the distribution function method still works, though more computation-intensive.

#### **Many-to-One Transformation**

For **many-to-one** functions, multiple points in the domain map to the same value in the codomain.

* The **Jacobian method does not apply directly**.


* The **distribution function method** becomes essential:

  * It integrates the joint density over **all points** in the input space that map to values ≤ $z$.

---

### **4. Applying Two-to-One Transformations to Random Variables**

Let’s consider a **two-to-one transformation** such as:

$$
Z = X^2
$$

Suppose $X$ is standard normal: $X \sim \mathcal{N}(0,1)$

Then:

* $`Z = X^2`$ maps both $`X = \sqrt{z}`$ and $`X = -\sqrt{z}`$ to the same $Z$


* Hence, **two values** of $X$ correspond to each positive value of $Z$

Use:

$$
F_Z(z) = P(X^2 \leq z) = P(-\sqrt{z} \leq X \leq \sqrt{z})
$$

Then:

$$
f_Z(z) = \frac{d}{dz} F_Z(z) = \frac{d}{dz} \left[ \int_{-\sqrt{z}}^{\sqrt{z}} f_X(x) \, dx \right]
$$

Using the **fundamental theorem of calculus with Leibniz's rule** and chain rule, we get:

$$
f_Z(z) = \frac{1}{2\sqrt{z}} \left( f_X(\sqrt{z}) + f_X(-\sqrt{z}) \right)
= \frac{1}{\sqrt{2\pi z}} e^{-z/2},\quad z > 0
$$

This is the **PDF of a chi-squared distribution with 1 degree of freedom**.

---

### **5. Example: Distribution of the Maximum**

Let $`X, Y \sim \text{Uniform}(0, 1)`$, independent, and let $`Z = \max(X, Y)`$

This is a **many-to-one transformation**, because many $`(x, y)`$ pairs produce the same maximum.

#### **CDF method**:

$$
F_Z(z) = P(\max(X, Y) \leq z) = P(X \leq z,\ Y \leq z) = z^2,\quad 0 \leq z \leq 1
$$

Differentiate:

$$
f_Z(z) = \frac{d}{dz} z^2 = 2z,\quad 0 \leq z \leq 1
$$

---

### **6. Summary Table**

| Transformation Type | Method                                  | Key Feature                                                             |
| ------------------- |-----------------------------------------|-------------------------------------------------------------------------|
| One-to-One          | Change of Variables or CDF method       | Inverse exists uniquely                                                 |
| Many-to-One         | Distribution function method            | Multiple pre-images → must integrate over full region $`g(x,y) \leq z`$ |
| Two-to-One          | Distribution function method            | CDF is integral over symmetric domain                                   |
| Common Targets      | $`Z = X^2,\ Z = \max(X,Y),\ Z = X + Y`$ | Must analyze regions carefully                                          |

---

### **7. When to Use Distribution Function Method**

* When the transformation is **not invertible**


* When the region $`g(X, Y) \leq z`$ has a **geometrically simple** structure


* When the Jacobian method is undefined or complex due to singularities or overlapping images

---