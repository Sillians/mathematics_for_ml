# **Tangent Planes & Hyperplanes**

A **tangent plane** is the 2-D plane that best approximates a 3-D surface at a point.
For an \$n\$-variable scalar field \$F(x\_1,\dots,x\_{,n})=0\$, the **tangent hyperplane** is the \$(n-1)\$-dimensional affine space that best approximates the level set through the point.

---

## 1 · Calculating the Equation of a Tangent Plane

### Surface given **explicitly**

If \$z=f(x,y)\$ is differentiable at \$(x\_0,y\_0)\$, then

$$
z \;=\; f(x_0,y_0) \;+\; f_x(x_0,y_0)\,(x-x_0) \;+\; f_y(x_0,y_0)\,(y-y_0)
$$

### Surface given as a **level set**

If \$F(x,y,z)=0\$ and \$\nabla F(P)\neq\mathbf 0\$, the tangent plane at \$P(x\_0,y\_0,z\_0)\$ is

$$
\nabla F(x_0,y_0,z_0)\;\cdot\;\bigl\langle x-x_0,\; y-y_0,\; z-z_0 \bigr\rangle \;=\;0 ,
\qquad\text{where } \nabla F=\bigl\langle F_x,F_y,F_z\bigr\rangle.
$$

---

### **Example**

Surface: \$z= x^2y - 3y^2\$ at \$(1,,1)\$.


Gradient of \$f\$: \$f\_x = 2xy,; f\_y = x^2 - 6y\$.


At \$(1,1)\$: \$f\_x=2,; f\_y=-5,; f(1,1)=1^2\cdot1-3= -2\$.


Tangent plane:

$$
z + 2 \;=\; 2(x-1) \;-\; 5(y-1).
$$


---

## 2 · Calculating the Equation of a Tangent **Hyperplane**

For \$F(x\_1,\dots,x\_n)=0\$ with non-zero gradient at a point \$P\$:

$$
\nabla F(P)\cdot\bigl\langle x_1-x_{1,0},\dots,x_n-x_{n,0}\bigr\rangle = 0 .
$$

### **Example in \$\mathbb R^4\$**

Level set of

$$
F(x,y,z,w)=x^2+y^2+z^2+w^2-9 =0
$$

is the 3-sphere of radius 3.

At $`P(1,2,2,2)`$ 

($`\lVert P\rVert^2=13!\not=9`$ 

so pick point $`(1,2,2,2)`$ 

on radius-3 scaled to


$`(\frac{1}{\sqrt{3}}, \frac{2}{\sqrt{3}}, \frac{2}{\sqrt{3}}, \frac{2}{\sqrt{3}})`$  etc.  

Illustration skipped.)

Gradient $`\nabla F = \langle 2x,2y,2z,2w\rangle`$ → at $`P`$ it is $`\langle2,4,4,4\rangle`$.

Tangent hyperplane:

$$
2(x-1)+4(y-2)+4(z-2)+4(w-2)=0 .
$$

---


## 3 · Finding Points Where Tangent Planes Have Particular Properties

### 3.1 · **Horizontal (parallel to \$xy\$-plane)**

For $`z=f(x,y)`$, the plane is horizontal when $`f\_x=f\_y=0`$.
Solve **critical-point** system $`f\_x=f\_y=0`$.



### 3.2 · **Containing a given line or normal**

If required normal $`\mathbf n`$ is known, ensure

$$
\mathbf n \parallel \nabla F(x_0,y_0,z_0).
$$

Solve for points where gradients are colinear.



### **Example**

Find points on $`z=x^2+y^2`$ whose tangent plane passes through origin $`(0,0,0)`$.

Plane at $`(a,b,a^2+b^2)`$:

$`z - (a^2+b^2)=2a(x-a)+2b(y-b)`$.


Plug $`(0,0,0)`$:

$`-(a^2+b^2) = -2a^2 -2b^2 ;\Longrightarrow; a^2+b^2=0;`$ ⇒ only point $`(0,0,0)`$.

---

## 🔑 Properties of the Gradient

| Property                                                | Consequence for tangent planes                     |
|---------------------------------------------------------|----------------------------------------------------|
| $`\nabla f`$ points in direction of **steepest ascent** | Tangent plane normal = $`\nabla f`$                |
| $`\nabla f = \mathbf0`$ at a point                      | Tangent plane is horizontal for graphs $`z=f(x,y)`$ |
| For level set $`F=c`$, $`\nabla F`$ ⟂ surface           | Used directly for hyperplane equation              |

---

### Quick Checklist

1. **Choose representation**: explicit graph or implicit level set.


2. **Compute gradient** at desired point.


3. **Write plane/hyperplane** using point–normal form.


4. **Impose special conditions** (horizontal, passes through a fixed point, etc.) to locate specific points.

---
