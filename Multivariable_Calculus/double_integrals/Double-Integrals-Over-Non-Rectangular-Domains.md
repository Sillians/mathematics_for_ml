# **Double Integrals Over Non-Rectangular Domains**

---

## **Overview**

In multivariable calculus, **double integrals** allow us to compute the volume under a surface defined over
a **2D region**. While rectangular regions are easy to handle, many real-world applications involve
**non-rectangular domains** bounded by curves or other functions.

---

## **1. Determining a Valid Region to Define a Double Integral Over a Non-Rectangular Domain**

A **non-rectangular domain** can be:

* **Type I (vertical slices):**

  $$
  D = \{(x, y) \in \mathbb{R}^2 \mid a \leq x \leq b,\; g_1(x) \leq y \leq g_2(x) \}
  $$

  Evaluate as:

  $$
  \iint_D f(x, y)\, dA = \int_a^b \int_{g_1(x)}^{g_2(x)} f(x, y)\, dy\, dx
  $$

* **Type II (horizontal slices):**

  $$
  D = \{(x, y) \in \mathbb{R}^2 \mid c \leq y \leq d,\; h_1(y) \leq x \leq h_2(y) \}
  $$

  Evaluate as:

  $$
  \iint_D f(x, y)\, dA = \int_c^d \int_{h_1(y)}^{h_2(y)} f(x, y)\, dx\, dy
  $$

> ✅ **A valid region** must be described clearly using continuous boundary functions and appropriate limits.

---

## **2. Identifying True Statements About Double Integrals Over Non-Rectangular Domains**

Here are true key properties:

| Statement                                                                                              | Truth                                                  |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------ |
| A double integral over a curved domain can be evaluated using iterated integrals with variable limits. | ✅ True                                                 |
| The limits of integration must match the bounds of the region.                                         | ✅ True                                                 |
| The order of integration can be switched, provided the limits are adjusted accordingly.                | ✅ True                                                 |
| A double integral over a non-rectangular domain can always be split into rectangular subregions.       | ❌ Not always; many curves can't be subdivided cleanly. |

---

## **3. Determining a Correct Function Used to Define a Double Integral Over a Non-Rectangular Domain**

Suppose we’re given a region $D$ bounded by $`y = x^2`$ and $`y = 4`$. This is a Type I region:

$$
D = \{(x, y) \mid -2 \leq x \leq 2,\; x^2 \leq y \leq 4 \}
$$

A correct double integral setup for \$f(x, y) = x + y\$:

$$
\iint_D (x + y)\, dA = \int_{-2}^{2} \int_{x^2}^{4} (x + y)\, dy\, dx
$$

> ✅ The **function used** must match the **variable limits of the domain**.

---

## **Sketching Non-Rectangular Domains**

To better visualize integration:

1. **Graph both boundary curves**
2. **Shade the region between the curves**
3. **Draw arrows in the direction of integration (vertical/horizontal slices)**

This helps determine whether it’s better to treat the domain as Type I or II.

---

## **Summary Table**

| Concept              | Key Idea                                            |
| -------------------- | --------------------------------------------------- |
| Valid Region         | Must be well-defined using continuous bounds        |
| Type I               | $`a \leq x \leq b`$, $`g\_1(x) \leq y \leq g\_2(x)`$ |
| Type II              | $`c \leq y \leq d`$, $`h\_1(y) \leq x \leq h\_2(y)`$ |
| Order of Integration | Can be changed if bounds are adjusted               |
| Function Setup       | Function and bounds must align correctly            |

---
