## **Double Integrals Over Type II Regions**

---

### **1. Understanding Type II Regions**

A **Type II region** is one where the region is bounded:

* **Horizontally** between two curves/functions of $y$: $`x = g_1(y)`$ to $`x = g_2(y)`$,
* And **vertically** from $`y = c`$ to $`y = d`$.

Thus, the region $R$ is described as:

$$
R = \{ (x, y) \in \mathbb{R}^2 \mid c \leq y \leq d,\; g_1(y) \leq x \leq g_2(y) \}
$$

The double integral over $R$ becomes:

$$
\iint_R f(x, y) \, dA = \int_{y=c}^{d} \int_{x=g_1(y)}^{g_2(y)} f(x, y) \, dx \, dy
$$

---

### **2. Representing a Double Integral as a Repeated Integral When the Limits Are Given**

If limits are provided:

* For $`y \in [c, d]`$, and
* For each fixed $y$, $`x \in [g_1(y), g_2(y)]`$,

Then directly write:

$$
\iint_R f(x, y) \, dA = \int_{y=c}^{d} \int_{x=g_1(y)}^{g_2(y)} f(x, y) \, dx \, dy
$$

**Example:**

Given:

$$
R = \{(x, y) \mid 0 \leq y \leq 2,\; y^2 \leq x \leq 4\}
$$

Then:

$$
\iint_R f(x, y) \, dA = \int_{y=0}^{2} \int_{x=y^2}^{4} f(x, y) \, dx \, dy
$$

---

### **3. Representing a Double Integral as a Repeated Integral When the Limits Are Not Given**

**Step-by-step:**

1. Sketch or visualize the region.
2. For Type II:

   * Fix $y$ and determine how $x$ varies with it.
3. Express the horizontal bounds as functions of $y$:

   * Find $`x = g_1(y)`$ (left)
   * $`x = g_2(y)`$ (right)
4. Determine $y$-bounds $`c \leq y \leq d`$ for which region exists.

**Example:**

Given region bounded by:

* $`x = y^2`$ (left)
* $`x = y + 2`$ (right)

To find limits:

* Set $`y^2 = y + 2 \Rightarrow y^2 - y - 2 = 0 \Rightarrow y = -1, 2`$

Then:

$$
\iint_R f(x, y) \, dA = \int_{y=-1}^{2} \int_{x=y^2}^{y+2} f(x, y) \, dx \, dy
$$

---

### **4. Evaluating a Repeated Integral Defined Over a Type II Region**

Once limits are known:

$$
\int_{y=c}^{d} \left( \int_{x=g_1(y)}^{g_2(y)} f(x, y) \, dx \right) dy
$$

Evaluate the inner integral with respect to $x$, treating $y$ as constant, then the outer with respect to $y$.

**Example:**

Evaluate:

$$
\int_{y=0}^{1} \int_{x=y}^{\sqrt{y}} x^2 \, dx \, dy
$$

(Here bounds are invalid unless flipped; ensure $`g_1(y) < g_2(y)`$.)

---

### **5. Calculating a Double Integral Defined Over a Type II Region**

**Example Problem:**

Evaluate:

$$
\iint_R x \, dA
$$

where $`R`$ is bounded by:

* $`x = y^2`$, $`x = 4`$, and $`y \in [-2, 2]`$

→ Type II form: $`x \in [y^2, 4]`$, $`y \in [-2, 2]`$

Then:

$`\iint_R x \, dA = \int_{y=-2}^{2} \int_{x=y^2}^{4} x \, dx \, dy  = \int_{y=-2}^{2} \left[ \frac{x^2}{2} \right]_{x=y^2}^{4} dy  = \int_{y=-2}^{2} \left( \frac{16}{2} - \frac{y^4}{2} \right) dy  = \int_{-2}^{2} \left( 8 - \frac{y^4}{2} \right) dy`$

Now compute:

$$
= \int_{-2}^{2} 8 \, dy - \int_{-2}^{2} \frac{y^4}{2} \, dy = 8(4) - \frac{1}{2} \cdot \frac{2^5}{5} = 32 - \frac{32}{5} = \frac{160 - 32}{5} = \frac{128}{5}
$$

---

### **Summary Table**

| **Task**                    | **Approach**                                                      |
| --------------------------- | ----------------------------------------------------------------- |
| Represent with limits given | Use $`\int_{y=c}^{d} \int_{x=g_1(y)}^{g_2(y)} f(x, y) \, dx \, dy`$ |
| Without limits              | Sketch → find horizontal bounds as functions of $`y`$               |
| Evaluate repeated integral  | Inner: integrate w\.r.t. $`x`$; Outer: w\.r.t. $`y`$                 |
| Calculate over region       | Reduce to definite integral using correct bounds                  |

---

