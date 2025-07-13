# **The Inverse Function Theorem**

The Inverse Function Theorem is a fundamental result in multivariable calculus and differential geometry that provides conditions under which a function has a local inverse. 
It is particularly useful in understanding transformations and their invertibility in higher dimensions.

#### Overview of the Inverse Function Theorem
The Inverse Function Theorem states that if $`T: \mathbb{R}^n \to \mathbb{R}^n`$ is a continuously differentiable function (i.e., $`T \in C^1`$) and the Jacobian determinant $`\det(J_T(p)) \neq 0`$ at a point $p$ in the domain, 
then there exists an open neighborhood $U$ of $p$ and an open neighborhood $V$ of $T(p)$ such that $`T: U \to V`$ is a bijection, and the inverse function $`T^{-1}: V \to U`$ is also continuously differentiable. 
The Jacobian of the inverse at $`T(p)`$ is the inverse of the Jacobian of $T$ at $p$, i.e., $`J_{T^{-1}}(T(p)) = (J_T(p))^{-1}`$, provided the inverse exists.

**Key Condition:** The non-zero Jacobian determinant ensures the transformation is locally invertible, as it indicates the linear approximation (via the Jacobian) is non-singular.

---

#### Identifying True Statements Regarding the Inverse Function Theorem
To apply the theorem correctly, certain statements must hold. Let’s explore some potential statements and identify which are true.

**Example Problem 1: Evaluating Statements**

Consider the following statements about the Inverse Function Theorem:


1. If $`\det(J_T(p)) = 0`$, then $T$ has a local inverse at $p$.


2. The theorem guarantees a global inverse if $`\det(J_T) \neq 0`$ everywhere.


3. The inverse $T^{-1}$ is differentiable if $T$ is $`C^1`$ and $`\det(J_T) \neq 0`$ at the point of interest.


5. The theorem applies only to linear transformations.


**Solution:**
- **Statement 1:** False. If $`\det(J_T(p)) = 0`$, the Jacobian is singular, and the theorem does not guarantee a local inverse, as the transformation may collapse dimensions (critical point).


- **Statement 2:** False. The theorem ensures a *local* inverse in a neighborhood, not a global inverse, even if $`\det(J_T) \neq 0`$ everywhere (e.g., consider a spiral mapping).


- **Statement 3:** True. If $T$ is $C^1$ and $`\det(J_T) \neq 0`$ at $p$, the inverse $`T^{-1}`$ exists locally and is differentiable by the theorem.


- **Statement 4:** False. The theorem applies to any continuously differentiable (non-linear included) transformation, not just linear ones.


**True Statement:** Only statement 3 is true.

---


#### Determining the Critical Points of a Transformation
Critical points of a transformation $`T: \mathbb{R}^n \to \mathbb{R}^n`$ occur where the Jacobian determinant $`\det(J_T) = 0`$, 
indicating the transformation is not locally invertible at those points. 
These points are where the rank of the Jacobian drops, potentially causing the image to collapse to a lower-dimensional set.


**Example Problem 2: Finding Critical Points**
Consider $`T(u, v) = (u^2 - v^2, 2uv)`$. Find the critical points.


**Solution:**
- Compute the Jacobian matrix:
  - $`\frac{\partial x}{\partial u} = 2u`$, $`\frac{\partial x}{\partial v} = -2v`$


  - $`\frac{\partial y}{\partial u} = 2v`$, $`\frac{\partial y}{\partial v} = 2u`$


  - $`J_T = \begin{bmatrix} 2u & -2v \\ 2v & 2u \end{bmatrix}`$


- Determinant:
$`\det(J_T) = (2u \cdot 2u) - (-2v \cdot 2v) = 4u^2 + 4v^2`$


- Set $`\det(J_T) = 0`$:

$`4u^2 + 4v^2 = 0`$


  Since $`u^2 \geq 0`$ and $`v^2 \geq 0`$, the only solution is $u = 0$ and $v = 0$.
- **Critical Point:** $`(u, v) = (0, 0)`$.

---

#### Jacobian Determinants of Inverse Transformations
The Jacobian determinant of the inverse transformation $`T^{-1}`$ is related to the Jacobian determinant of $T$ by the reciprocal relationship. 
If $`T: U \to V`$ and $`T^{-1}: V \to U`$ are inverses, and $`\det(J_T(p)) \neq 0`$ at $`p \in U`$, then:


$$
\det(J_{T^{-1}}(T(p))) = \frac{1}{\det(J_T(p))}.
$$


**Example Problem 3: Jacobian of Inverse**
Given $`T(u, v) = (u + v, u - v)`$ and its inverse $`T^{-1}(x, y) = \left(\frac{x + y}{2}, \frac{x - y}{2}\right)`$, 
find the Jacobian determinant of $`T^{-1}`$ and verify the relationship.


**Solution:**

- Jacobian of $T$:
  - $$J_T = \begin{bmatrix} 1 & 1 \\ 1 & -1 \end{bmatrix}$$


  - $$\det(J_T) = (1 \cdot -1) - (1 \cdot 1) = -1 - 1 = -2$$


- Jacobian of $$T^{-1}$$:
  - $$u = \frac{x + y}{2}$$, $$v = \frac{x - y}{2}$$


  - $$\frac{\partial u}{\partial x} = \frac{1}{2}$$, $$\frac{\partial u}{\partial y} = \frac{1}{2}$$


  - $$\frac{\partial v}{\partial x} = \frac{1}{2}$$, $$\frac{\partial v}{\partial y} = -\frac{1}{2}$$


  - $$J_{T^{-1}} = \begin{bmatrix} \frac{1}{2} & \frac{1}{2} \\ \frac{1}{2} & -\frac{1}{2} \end{bmatrix}$$


  - $$\det(J_{T^{-1}}) = \left(\frac{1}{2} \cdot -\frac{1}{2}\right) - \left(\frac{1}{2} \cdot \frac{1}{2}\right) = -\frac{1}{4} - \frac{1}{4} = -\frac{1}{2}$$



Verify:
$$
\frac{1}{\det(J_T)} = \frac{1}{-2} = -\frac{1}{2}
$$
The determinants match, confirming the relationship.
