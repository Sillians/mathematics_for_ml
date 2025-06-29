## **THE MULTIVARIABLE CHAIN RULE**

---

### 1. OVERVIEW

The **multivariable chain rule** generalizes the single-variable chain rule to functions of several variables. 
It allows one to compute the derivative of a composition of functions when each intermediate variable depends on one or more independent variables.

It is especially useful when dealing with **composite functions** of the form:

* $`z = f(x, y)`$, with $`x = x(t), y = y(t)`$
* or more generally, $`z = f(u_1, u_2, ..., u_n)`$, where each $`u_i`$ is a function of one or more variables.

---

### 2. CALCULATING THE DERIVATIVE OF A MULTIVARIABLE FUNCTION WITH ONE INDEPENDENT VARIABLE

Given a function:

* $`z = f(x(t), y(t))`$

where $f$ is a function of two variables and both $x$ and $y$ are functions of a single variable $t$, then the chain rule says:

$$
\frac{dz}{dt} = \frac{\partial f}{\partial x} \cdot \frac{dx}{dt} + \frac{\partial f}{\partial y} \cdot \frac{dy}{dt}
$$

**Interpretation:**
The total derivative $`\frac{dz}{dt}`$ accounts for how $z$ changes with $t$ through both intermediate variables $`x(t)`$ and $`y(t)`$.

---

### 3. SPECIAL CASE: WHEN ONE VARIABLE IS CONSTANT

Suppose $y$ is a constant (i.e., $`\frac{dy}{dt} = 0`$), then the formula simplifies to:

$$
\frac{dz}{dt} = \frac{\partial f}{\partial x} \cdot \frac{dx}{dt}
$$

This is equivalent to treating $z$ as a function of $`x(t)`$ alone while holding $y$ fixed.

This special case appears often in physics and engineering when only one quantity is changing and others are held constant.

---

### 4. CALCULATING THE DERIVATIVE OF A MULTIVARIABLE FUNCTION WITH TWO INDEPENDENT VARIABLES

Now suppose:

* $`z = f(x(u, v), y(u, v))`$

Then the **partial derivatives** of $z$ with respect to $u$ and $v$ are:

$$
\frac{\partial z}{\partial u} = \frac{\partial f}{\partial x} \cdot \frac{\partial x}{\partial u} + \frac{\partial f}{\partial y} \cdot \frac{\partial y}{\partial u}
$$


$$
\frac{\partial z}{\partial v} = \frac{\partial f}{\partial x} \cdot \frac{\partial x}{\partial v} + \frac{\partial f}{\partial y} \cdot \frac{\partial y}{\partial v}
$$

This rule extends to higher dimensions. The idea is to sum over all intermediate paths from the independent variables to the dependent variable.

---

### 5. CALCULATING THE DERIVATIVE OF A FUNCTION OF THREE INTERMEDIATE VARIABLES AND TWO INDEPENDENT VARIABLES

Suppose:

* $`w = f(x, y, z)`$, where:

  * $`x = x(u, v)`$
  * $`y = y(u, v)`$
  * $`z = z(u, v)`$

Then the **partial derivatives** of $w$ are:

$$
\frac{\partial w}{\partial u} = \frac{\partial f}{\partial x} \cdot \frac{\partial x}{\partial u} + \frac{\partial f}{\partial y} \cdot \frac{\partial y}{\partial u} + \frac{\partial f}{\partial z} \cdot \frac{\partial z}{\partial u}
$$

$$
\frac{\partial w}{\partial v} = \frac{\partial f}{\partial x} \cdot \frac{\partial x}{\partial v} + \frac{\partial f}{\partial y} \cdot \frac{\partial y}{\partial v} + \frac{\partial f}{\partial z} \cdot \frac{\partial z}{\partial v}
$$

This captures the full contribution of each path through the variables $`x, y, z`$, which all depend on both $u$ and $v$.

---

### KEY PRINCIPLE

The general form of the multivariable chain rule is:

$$
\frac{\partial f}{\partial t_j} = \sum_i \frac{\partial f}{\partial x_i} \cdot \frac{\partial x_i}{\partial t_j}
$$

where:

* $f$ is a function of intermediate variables $`x_1, x_2, ..., x_m`$,
* each $`x_i`$ is a function of independent variables $`t_1, t_2, ..., t_n`$,
* and $`\frac{\partial f}{\partial t_j}`$ is the total rate of change of $f$ with respect to one of those independent variables.

---

**Summary Table:**

| Case                             | Expression                                                                                                                                                              |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| One independent variable         | $`\frac{dz}{dt} = \frac{\partial f}{\partial x} \cdot \frac{dx}{dt} + \frac{\partial f}{\partial y} \cdot \frac{dy}{dt}`$                                                 |
| Special case (constant variable) | $`\frac{dz}{dt} = \frac{\partial f}{\partial x} \cdot \frac{dx}{dt}`$                                                                                                     |
| Two independent variables        | $`\frac{\partial z}{\partial u} = \frac{\partial f}{\partial x} \cdot \frac{\partial x}{\partial u} + \frac{\partial f}{\partial y} \cdot \frac{\partial y}{\partial u}`$ |
| Three intermediate variables     | Add a term for each: $`\frac{\partial f}{\partial z} \cdot \frac{\partial z}{\partial u}`$, etc.                                                                          |

This rule is foundational in multivariable calculus, optimization, machine learning (backpropagation), and differential geometry.










































