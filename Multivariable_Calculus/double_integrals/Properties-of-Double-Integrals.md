## **PROPERTIES OF DOUBLE INTEGRALS**

---

### **1. OVERVIEW**

A **double integral** is used to compute the accumulated value of a function over a two-dimensional region — often representing **area**, **volume under a surface**, **mass**, or **total density**.

For a continuous function $`f(x, y)`$ over a region $R$, the double integral is denoted as:

$$
\iint_R f(x, y)\, dA
$$

where $`dA`$ typically represents an infinitesimal area element $`dx\,dy`$ or $`dy\,dx`$ in rectangular coordinates.

---

### **2. EVALUATING A DOUBLE INTEGRAL USING THE MULTIPLICATIVE PROPERTY**

If the integrand is **separable**, i.e.,

$$
f(x, y) = g(x) \cdot h(y)
$$

and the domain $R$ is a **rectangle**:

$$
R = [a, b] \times [c, d]
$$

then:

$$
\iint_R f(x, y)\, dA = \left( \int_a^b g(x)\, dx \right) \cdot \left( \int_c^d h(y)\, dy \right)
$$

**Example:**

$$
\iint_{[0,1] \times [0,2]} (x^2)(\sin y)\, dA = \left( \int_0^1 x^2\, dx \right) \cdot \left( \int_0^2 \sin y\, dy \right)
$$

---

### **3. EVALUATING A DOUBLE INTEGRAL WHEN THE INTEGRAND CONTAINS ONLY ONE VARIABLE**

If $`f(x, y) = f(x)`$ only (no $y$-dependence), then the integration over $y$ becomes a **constant multiplier**:

$$
\iint_R f(x)\, dA = \int_a^b f(x) \left( \int_c^d dy \right) dx = \int_a^b f(x) (d - c)\, dx
$$

**Analogously**, if $`f(x, y) = f(y)`$, then:

$$
\iint_R f(y)\, dA = \int_c^d f(y) (b - a)\, dy
$$

**Example:**

$$
\iint_{[0,2] \times [0,3]} e^x\, dA = \int_0^2 e^x (3 - 0)\, dx = 3 \int_0^2 e^x\, dx
$$

---

### **4. USING ADDITIVITY OF DOUBLE INTEGRALS**

The double integral is **additive over regions**:
If $`R = R_1 \cup R_2`$, and $`R_1, R_2`$ are **non-overlapping**, then:

$$
\iint_R f(x, y)\, dA = \iint_{R_1} f(x, y)\, dA + \iint_{R_2} f(x, y)\, dA
$$

This property allows:

* Splitting complex domains into simpler ones.
* Computing integrals piecewise over adjacent regions.

**Important:** The regions must be **non-overlapping (disjoint interiors)**.

---

### **5. EVALUATING A DOUBLE INTEGRAL USING ADDITIVITY OVER A RECTANGULAR DOMAIN**

If a rectangle $R$ is subdivided into subrectangles $`R_1, R_2, ..., R_n`$, then:

$$
\iint_R f(x, y)\, dA = \sum_{i=1}^n \iint_{R_i} f(x, y)\, dA
$$

This is commonly used in:

* Numerical integration (Riemann sum approximation)
* Piecewise-defined functions over partitioned rectangles

**Example:**

Let $`R = [0, 2] \times [0, 2]`$ be split into two rectangles:

* $`R_1 = [0, 1] \times [0, 2]`$
* $`R_2 = [1, 2] \times [0, 2]`$

Then:

$$
\iint_R f(x, y)\, dA = \iint_{R_1} f(x, y)\, dA + \iint_{R_2} f(x, y)\, dA
$$

---

### **KEY PROPERTIES — SUMMARY TABLE**

| Property                      | Description                              | Formula                                             |
| ----------------------------- | ---------------------------------------- | --------------------------------------------------- |
| **Multiplicative**            | For separable integrands over rectangles | $`\iint f(x, y) = \int g(x)\,dx \cdot \int h(y)\,dy`$ |
| **Single-variable Integrand** | Pulls out constant from one integral     | $`\iint f(x)\,dx\,dy = (d - c)\int f(x)\,dx`$         |
| **Additivity Over Regions**   | Add over non-overlapping regions         | $`\iint_{R} = \iint_{R_1} + \iint_{R_2}`$             |
| **Additivity in Rectangles**  | Add over rectangular partitions          | $`\iint_{R} = \sum \iint_{R_i}`$                      |

---

These foundational properties simplify evaluating double integrals and are essential tools in multivariable calculus, physics, and applied math.
