## **The Domain of a Multivariable Function**

---

### **1. What is the Domain?**

The **domain** of a multivariable function is the set of all points in ℝⁿ for which the function is **defined**. 
For a function of two variables, like

$$
f(x, y),
$$

the domain is the set of all points $`(x, y)`$ in ℝ² such that the expression for $`f(x, y)`$ is meaningful — i.e., 
it doesn't involve division by zero, negative inputs to even roots, or undefined logs.

---

### **2. Common Constraints Affecting the Domain**

| Expression Type | Condition for Validity                      | Example                          | Domain Description                     |
| --------------- | ------------------------------------------- |----------------------------------| -------------------------------------- |
| **Rational**    | Denominator ≠ 0                             | $`f(x, y) = \frac{x+y}{x - y}`$  | $`x \ne y`$                              |
| **Root**        | Even root: radicand ≥ 0                     | $`f(x, y) = \sqrt{x^2 - y}`$     | $`x^2 - y \ge 0`$                        |
| **Logarithmic** | Argument > 0                                | $`f(x, y) = \ln(y - x^2)`$       | $`y - x^2 > 0`$                          |
| **Trig**        | Often all ℝ, but can be undefined at points | $`f(x, y) = \tan(x + y)`$        | Exclude $`x + y = \frac{\pi}{2} + k\pi`$ |

---

### **3. How to Find the Domain**

#### **Step-by-step Process:**

1. **Identify the function expression**

   * Determine if it involves division, square roots, logarithms, etc.

2. **Write down all restrictions**

   * For denominators: ensure they are not 0.
   
   * For roots: ensure the radicand is non-negative (if even root).
   
   * For logs: ensure the argument is positive.

3. **Express the domain in set-builder or interval notation** (or graphically).

---

### **4. Examples**

#### **Example 1:**

$$
f(x, y) = \sqrt{9 - x^2 - y^2}
$$

* The square root requires:

  $9 - x^2 - y^2 \ge 0 \Rightarrow x^2 + y^2 \le 9$

✅ **Domain**:

$$
\{ (x, y) \in \mathbb{R}^2 \mid x^2 + y^2 \le 9 \}
$$

---

#### **Example 2:**

$$
f(x, y) = \frac{\ln(x + y)}{x - y}
$$

* Log requires: $x + y > 0$


* Denominator: $x \ne y$


✅ **Domain**:

$$
\{ (x, y) \in \mathbb{R}^2 \mid x + y > 0 \text{ and } x \ne y \}
$$

---

#### **Example 3:**

$$
f(x, y, z) = \frac{1}{\sqrt{x^2 + y^2 - z^2}}
$$

* The square root: $`x^2 + y^2 - z^2 > 0`$

✅ **Domain**:

$$
\{ (x, y, z) \in \mathbb{R}^3 \mid x^2 + y^2 > z^2 \}
$$

---

### **5. Visualizing Domains**

For 2D functions, the domain is a region in the $xy$-plane. For 3D, it's a volume in $`\mathbb{R}^3`$. 
Plotting inequalities or level curves can help visually understand where the function is defined.

---

### ✅ Summary

| Function Component | Domain Restriction Example             |
| ------------------ | -------------------------------------- |
| Division           | Denominator ≠ 0                        |
| Even Root          | Radicand ≥ 0                           |
| Logarithm          | Argument > 0                           |
| Trig Functions     | Avoid undefined angles (e.g. tan, sec) |

The domain of a multivariable function is found by identifying **all the points** where the function's formula is **valid and real-valued**.
