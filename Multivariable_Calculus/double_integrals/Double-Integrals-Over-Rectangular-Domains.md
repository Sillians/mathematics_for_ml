# **Double Integrals Over Rectangular Domains**

Double integrals allow us to compute **volume under a surface**, **mass of a region**, and more, over a 2D domain.

---

## Overview

Let $`f(x, y)`$ be continuous over a rectangle $`R = [a, b] \times [c, d]`$ in the $`xy`$-plane. 
Then the **double integral** over $`R`$ is:

$$
\iint_R f(x, y) \, dA = \int_c^d \int_a^b f(x, y) \, dx\,dy
$$

This is often computed as an **iterated integral** or **repeated integral**.

---

## Evaluating a Repeated Integral

To evaluate:

$$
\int_c^d \left( \int_a^b f(x, y)\, dx \right) dy
$$

1. **Integrate inner integral** (with respect to $x$, treat $y$ as constant)
2. **Plug result into outer integral**
3. **Integrate outer integral** (with respect to $y$)

### Example

Let:

$$
f(x, y) = xy, \quad R = [0, 1] \times [0, 2]
$$

Then:

$$
\iint_R xy \, dA = \int_0^2 \left( \int_0^1 xy \, dx \right) dy
$$

Compute inner integral:

$$
\int_0^1 xy \, dx = y \int_0^1 x \, dx = y \cdot \left[ \frac{x^2}{2} \right]_0^1 = \frac{y}{2}
$$

Then outer integral:

$$
\int_0^2 \frac{y}{2} \, dy = \frac{1}{2} \int_0^2 y \, dy = \frac{1}{2} \cdot \left[ \frac{y^2}{2} \right]_0^2 = \frac{1}{2} \cdot 2 = 1
$$

✅ Final result: **1**

---

## Evaluating a Double Integral Over a Rectangular Domain

Use when:

* Region is **rectangular**
* Function is continuous or easily integrable

**Example**:

$$
f(x, y) = x^2 + y^2, \quad R = [0, 1] \times [1, 2]
$$

Then:

$$
\iint_R f(x, y) \, dA = \int_1^2 \int_0^1 (x^2 + y^2)\, dx\,dy
$$

* Inner: $`\int\_0^1 (x^2 + y^2) dx = [\frac{x^3}{3} + x y^2]\_0^1 = \frac{1}{3} + y^2`$


* Outer: $`\int\_1^2 (\frac{1}{3} + y^2) dy = \frac{1}{3}(2 - 1) + [\frac{y^3}{3}]\_1^2 = \frac{1}{3} + \frac{8 - 1}{3} = \frac{1 + 7}{3} = \frac{8}{3}`$

✅ Final result: **$\frac{8}{3}$**

---

## Changing the Order of Integration

Sometimes it's easier to switch the order of integration:

$$
\int_c^d \int_a^b f(x, y) \, dx\,dy \quad \longleftrightarrow \quad \int_a^b \int_c^d f(x, y) \, dy\,dx
$$

You can switch **if the region is rectangular**, or more generally if bounds are properly adjusted.

### Example

Let:

$$
\iint_R x + y \, dx\,dy, \quad R = [0, 1] \times [0, 2]
$$

Can be written as:

* $`\int\_0^2 \int\_0^1 (x + y), dx,dy`$
* Or: $`\int\_0^1 \int\_0^2 (x + y), dy,dx`$

Both will yield the same result:
$`\boxed{3}`$

---

## Summary Table

| Concept            | Description                                                               |
| ------------------ | ------------------------------------------------------------------------- |
| Double Integral    | $`\iint\_R f(x, y) , dA`$ gives volume under surface over region $R$      |
| Repeated Integral  | Evaluate inner first, then outer                                          |
| Rectangular Domain | Bounds are constants; integration is straightforward                      |
| Changing Order     | Valid if integrand and region allow switching; often simplifies computation |

---