# **Limits and Continuity of Multivariable Functions**

## **Overview**

Multivariable functions involve more than one independent variable, typically written as $`f(x, y)`$ or $`f(x, y, z)`$. 
Understanding limits and continuity in this context requires analyzing behavior from multiple paths and directions.

---

## Calculating Limits of Multivariable Functions at Points of Continuity

A multivariable function $`f(x, y)`$ is **continuous at a point** $`(a, b)`$ if:

$$
\lim_{(x, y) \to (a, b)} f(x, y) = f(a, b)
$$

**Example**:

Let $`f(x, y) = x^2 + y^2`$.
Since this is a polynomial, it's continuous **everywhere**, and:

$$
\lim_{(x, y) \to (1, 2)} f(x, y) = 1^2 + 2^2 = 5
$$

---

## Calculating Limits of Multivariable Rational Functions by Factoring

If direct substitution gives an indeterminate form like $`\frac{0}{0}`$, **algebraic factoring** may help.

**Example**:

Let:

$$
f(x, y) = \frac{x^2 - y^2}{x - y}
$$

Factor numerator:

$$
\frac{(x - y)(x + y)}{x - y} = x + y \quad \text{(for } x \ne y \text{)}
$$

So:

$$
\lim_{(x, y) \to (a, a)} \frac{x^2 - y^2}{x - y} = 2a
$$

---

## Calculating Limits Using Conjugate Multiplication

Useful when the expression involves radicals.

**Example**:

$$
f(x, y) = \frac{\sqrt{x^2 + y^2 + 1} - 1}{x^2 + y^2}
$$

Multiply numerator and denominator by the **conjugate**:

$$
\frac{\sqrt{x^2 + y^2 + 1} - 1}{x^2 + y^2} \cdot \frac{\sqrt{x^2 + y^2 + 1} + 1}{\sqrt{x^2 + y^2 + 1} + 1}
= \frac{x^2 + y^2}{(x^2 + y^2)(\sqrt{x^2 + y^2 + 1} + 1)}
$$

Cancel terms:

$$
= \frac{1}{\sqrt{x^2 + y^2 + 1} + 1}
$$

As $`(x, y) \to (0, 0)`$:

$$
\lim_{(x, y) \to (0, 0)} f(x, y) = \frac{1}{\sqrt{1} + 1} = \frac{1}{2}
$$

---

## Calculating Limits Along Different Paths

When a limit **depends on the path** of approach, the limit **does not exist**.

**Example**:

$$
f(x, y) = \frac{xy}{x^2 + y^2}
$$

Approach along $`y = x`$:

$$
f(x, x) = \frac{x \cdot x}{x^2 + x^2} = \frac{x^2}{2x^2} = \frac{1}{2}
$$

Approach along $`y = -x`$:

$$
f(x, -x) = \frac{-x^2}{x^2 + x^2} = \frac{-1}{2}
$$

Since the limits differ, the limit **does not exist** at $`(0, 0)`$.

---

## Continuity Criteria Summary

A function $`f(x, y)`$ is continuous at $`(a, b)`$ if:

1. $`f(a, b)`$ is defined
2. $`\lim\_{(x, y) \to (a, b)} f(x, y)`$ exists
3. The limit equals the function value

---

