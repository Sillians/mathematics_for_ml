# **The Domain of a Multivariable Function**

In multivariable calculus, the **domain** of a function describes the set of input values $`(x, y)`$ (or more variables) for which the function is **defined**. 
It depends on the algebraic structure of the function — specifically, whether it includes **fractions**, **square roots**, **logarithms**, or **other special functions**.

---

## **Definition**

For a function $`f : \mathbb{R}^n \rightarrow \mathbb{R}`$, the **domain** is:

$$
\text{dom}(f) = \left\{ \mathbf{x} \in \mathbb{R}^n \mid f(\mathbf{x}) \text{ is defined} \right\}
$$

This means identifying where **no undefined operations** (like division by zero or taking the log of a negative number) occur.

---

## **Evaluating a Two-Variable Function**

Given a function like:

$$
f(x, y) = x^2 + y^2 + 3
$$

This is defined for **all** $`(x, y) \in \mathbb{R}^2`$, so the domain is:

$$
\boxed{ \mathbb{R}^2 }
$$

---

##  **Domain of a Function Involving Reciprocals and Radicals**

Example:

$$
f(x, y) = \frac{1}{\sqrt{x^2 + y^2 - 4}}
$$

### ➤ Constraints:

1. **Radical (square root)**: the expression inside must be **≥ 0**:

   $$
   x^2 + y^2 - 4 > 0
   $$

2. **Denominator**: must not be **zero**, so:

   $$
   x^2 + y^2 - 4 \ne 0
   $$

### ➤ Combine:

$$
x^2 + y^2 > 4
$$

### Domain:

$$
\boxed{ \left\{ (x, y) \in \mathbb{R}^2 \mid x^2 + y^2 > 4 \right\} }
$$

---

## **Domain of a Function Containing Exponential, Logarithmic, and Trigonometric Functions**

Example:

$$
f(x, y) = \ln(4 - x^2 - y^2) + \frac{\sin(x)}{y}
$$

### ➤ Constraints:

1. **Logarithmic term**: \$4 - x^2 - y^2 > 0\$

   $$
   x^2 + y^2 < 4
   $$

2. **Denominator**: \$y \ne 0\$

### Domain:

$$
\boxed{ \left\{ (x, y) \in \mathbb{R}^2 \mid x^2 + y^2 < 4 \text{ and } y \ne 0 \right\} }
$$

---

##  **Sketching the Domain of a Multivariable Function**

### Example:

Let:

$$
f(x, y) = \sqrt{9 - x^2 - y^2}
$$

### ➤ Constraint:

The radicand must be non-negative:

$$
x^2 + y^2 \leq 9
$$

This is a **disk of radius 3** centered at the origin.

---

### Visual Guide:

* Graphically, sketch a **filled circle** of radius 3:

  * Includes boundary: $`\leq`$
  * Excludes points outside the circle

If the constraint was **strict** ($`<`$), draw a **dashed** boundary and exclude it.

---

## **Summary Table**

| Function Type       | Condition                       | Domain Form                |
| ------------------- | ------------------------------- | -------------------------- |
| Polynomial          | Always defined                  | $`\mathbb{R}^n`$            |
| Rational            | Denominator $`\ne 0`$           | Remove zeros of denominator |
| Radical (even root) | Radicand $`\ge 0`$              | Solve inequality           |
| Logarithmic         | Argument $`> 0`$                 | Solve strict inequality    |
| Trigonometric       | Domain of underlying trig function | Exclude where undefined    |

---
