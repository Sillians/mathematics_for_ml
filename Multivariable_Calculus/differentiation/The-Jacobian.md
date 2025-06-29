## **The Jacobian**

### **Finding the Jacobian Determinant of a Transformation**
The Jacobian determinant quantifies how a transformation $T$ distorts area or volume in a given space. 
For a transformation $$T: \mathbb{R}^2 \to \mathbb{R}^2$$ defined by $$T(u, v) = (x(u, v), y(u, v))$$, 
the Jacobian matrix is the matrix of partial derivatives:

$$
J = \begin{bmatrix}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\
\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}
\end{bmatrix}.
$$

The Jacobian determinant, $$\det(J)$$, is the determinant of this matrix. For a transformation from $$\mathbb{R}^3 \to \mathbb{R}^3$$, 
the Jacobian is a 3x3 matrix, and its determinant scales volumes accordingly.

**Example Problem 1: Finding the Jacobian Determinant**
Consider the transformation $$T(u, v) = (u^2 + v, e^u v)$$. Find the Jacobian determinant.

**Solution:**
- Compute the partial derivatives:
  - $$\frac{\partial x}{\partial u} = \frac{\partial}{\partial u} (u^2 + v) = 2u$$
  - $$\frac{\partial x}{\partial v} = \frac{\partial}{\partial v} (u^2 + v) = 1$$
  - $$\frac{\partial y}{\partial u} = \frac{\partial}{\partial u} (e^u v) = e^u v$$
  - $$\frac{\partial y}{\partial v} = \frac{\partial}{\partial v} (e^u v) = e^u$$
  

- Jacobian matrix:
$$
J = \begin{bmatrix} 2u & 1 \\ e^u v & e^u \end{bmatrix}
$$


- Determinant:
$$
\det(J) = (2u \cdot e^u) - (1 \cdot e^u v) = 2u e^u - e^u v
$$

#### Evaluating a Jacobian Determinant
Evaluating the Jacobian determinant involves substituting specific values of $$u$$ and $$v$$ into the 
determinant expression to assess the transformation's effect at those points.

**Example Problem 2: Evaluating the Jacobian Determinant**
Using the transformation from Example 1, evaluate the Jacobian determinant at $$(u, v) = (0, 1)$$.

**Solution:**
- Substitute $$u = 0$$, $$v = 1$$ into $$\det(J) = 2u e^u - e^u v$$:

$$
\det(J) = 2(0) e^0 - e^0 (1) = 0 - 1 = -1
$$
- At this point, the Jacobian determinant is $$-1$$, indicating a non-degenerate transformation with orientation reversal.

#### Identifying the Local Area Scale Factor of a Transformation
The local area scale factor is given by the absolute value of the Jacobian determinant, $$|\det(J)|$$. 
This value indicates how much the area is magnified or reduced by the transformation locally. 
A value of 0 implies the transformation collapses the area to a lower dimension.

**Example Problem 3: Identifying the Local Area Scale Factor**
For $$T(u, v) = (u v, u^2 - v)$$, find the local area scale factor at $$(u, v) = (2, 1)$$.

**Solution:**
- Compute partial derivatives:
  - $$\frac{\partial x}{\partial u} = v$$, $$\frac{\partial x}{\partial v} = u$$
  - $$\frac{\partial y}{\partial u} = 2u$$, $$\frac{\partial y}{\partial v} = -1$$

- Jacobian matrix:
$$
J = \begin{bmatrix} v & u \\ 2u & -1 \end{bmatrix}
$$

- Determinant:
$$
\det(J) = (v \cdot -1) - (u \cdot 2u) = -v - 2u^2
$$

- At $$ (u, v) = (2, 1) $$:
$$
\det(J) = -(1) - 2(2)^2 = -1 - 8 = -9
$$

- Local area scale factor: $$|\det(J)| = |-9| = 9$$, meaning the area is scaled by a factor of 9.

#### Finding Regions Where a Transformation is Orientation-Preserving or Reversing
The sign of the Jacobian determinant determines the orientation:
- $$\det(J) > 0$$: The transformation is orientation-preserving (e.g., a rotation).
- $$\det(J) < 0$$: The transformation is orientation-reversing (e.g., a reflection).
- $$\det(J) = 0$$: The transformation is degenerate at that point.

**Example Problem 4: Finding Orientation Regions**
Determine the regions where $$T(u, v) = (u^2 - v^2, 2uv)$$ is orientation-preserving or reversing.

**Solution:**
- Compute partial derivatives:
  - $$\frac{\partial x}{\partial u} = 2u$$, $$\frac{\partial x}{\partial v} = -2v$$
  - $$\frac{\partial y}{\partial u} = 2v$$, $$\frac{\partial y}{\partial v} = 2u$$
- Jacobian matrix:
$$
J = \begin{bmatrix} 2u & -2v \\ 2v & 2u \end{bmatrix}
$$
- Determinant:
$$
\det(J) = (2u \cdot 2u) - (-2v \cdot 2v) = 4u^2 + 4v^2
$$


- Orientation analysis:
  - Since $$4u^2 + 4v^2 \geq 0$$ and equals 0 only at $$(u, v) = (0, 0)$$, the determinant is positive except at the origin.
  - $$4u^2 + 4v^2 > 0$$ (i.e., $$(u, v) \neq (0, 0)$$): Orientation-preserving.
  - At $$(u, v) = (0, 0)$$: $$\det(J) = 0$$, indicating a critical point.
  
- Regions: The entire plane except the origin is orientation-preserving; the origin is a degenerate point.

