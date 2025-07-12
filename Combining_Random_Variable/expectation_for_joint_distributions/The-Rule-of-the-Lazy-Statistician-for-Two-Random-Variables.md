## **The Rule of the Lazy Statistician for Two Random Variables**

---

### **1. Overview: The Rule of the Lazy Statistician**

The **Rule of the Lazy Statistician** allows you to compute expectations (means) of functions of random variables **without first computing their marginal distributions**. 
This is especially useful when dealing with functions of two random variables, say $X$ and $Y$.

If $`g(X, Y)`$ is a function of two random variables, the rule says:

* **Discrete case:**

  $`\mathbb{E}[g(X, Y)] = \sum_x \sum_y g(x, y)\, P(X = x, Y = y)`$

* **Continuous case:**

  $`\mathbb{E}[g(X, Y)] = \iint g(x, y)\, f_{X,Y}(x, y)\,dx\,dy`$

This avoids the intermediate step of finding marginal distributions, hence the term “lazy.”

---

### **2. Applying the Rule to Discrete Random Variables**

Let $X$ and $Y$ be discrete random variables with joint probability mass function $`P(x, y) = P(X = x, Y = y)`$.

To compute $`\mathbb{E}[g(X, Y)]`$:

$$
\mathbb{E}[g(X, Y)] = \sum_{x} \sum_{y} g(x, y)\, P(x, y)
$$

#### **Example**

Let $X$ and $Y$ take values in $`{1, 2}`$ with joint PMF:

| $`Y \backslash X`$   | 1   | 2   |
|----------------------| --- | --- |
| 1                    | 0.2 | 0.3 |
| 2                    | 0.1 | 0.4 |

Compute $`E[XY]`$:

$$
\begin{aligned}
\mathbb{E}[XY] &= \sum_x \sum_y xy \cdot P(x, y) \\
&= 1\cdot1\cdot 0.2 + 2\cdot1\cdot 0.3 + 1\cdot2\cdot 0.1 + 2\cdot2\cdot 0.4 \\
&= 0.2 + 0.6 + 0.2 + 1.6 = 2.6
\end{aligned}
$$

---

### **3. Applying the Rule to Continuous Random Variables**

Let $X$ and $Y$ be continuous random variables with joint PDF $`f(x, y)`$. Then:

$$
\mathbb{E}[g(X, Y)] = \iint_{\mathbb{R}^2} g(x, y)\, f(x, y)\, dx\, dy
$$

This double integral can be computed over the **support of the joint PDF**.

#### **Example (Rectangular Domain)**

Let:

$$
f(x, y) = \begin{cases}
4xy, & 0 \le x \le 1,\; 0 \le y \le 1 \\
0, & \text{otherwise}
\end{cases}
$$

Compute $`\mathbb{E}[XY]`$:

$$
\mathbb{E}[XY] = \int_0^1 \int_0^1 xy \cdot 4xy\,dy\,dx = \int_0^1 \int_0^1 4x^2 y^2\,dy\,dx
$$

$$
= \int_0^1 4x^2 \left[\frac{y^3}{3}\right]_0^1 dx = \int_0^1 \frac{4x^2}{3}\,dx = \frac{4}{3} \cdot \left[\frac{x^3}{3}\right]_0^1 = \frac{4}{9}
$$

---

### **4. Applying the Rule to Continuous Random Variables: Non-Rectangular Domains**

When the domain is **non-rectangular**, set integration limits carefully based on the shape of the support.

#### **Example (Triangular Domain)**

Let:

$$
f(x, y) = \begin{cases}
2, & 0 < y < x < 1 \\
0, & \text{otherwise}
\end{cases}
$$

Compute $`\mathbb{E}[XY]`$:

1. Integration domain: $y$ goes from $0$ to $x$, and $x$ goes from $0$ to $1$.
2. Apply the rule:

$$
\mathbb{E}[XY] = \int_0^1 \int_0^x xy \cdot 2\,dy\,dx
= 2 \int_0^1 x \left[\frac{y^2}{2}\right]_0^x dx
= 2 \int_0^1 x \cdot \frac{x^2}{2}\,dx
= \int_0^1 x^3\,dx = \frac{1}{4}
$$

---

### **Summary Table**

| Case                         | Formula                                                                         | Notes                |
| ---------------------------- |---------------------------------------------------------------------------------| -------------------- |
| Discrete                     | $` \mathbb{E}[g(X, Y)] = \sum\_x \sum\_y g(x, y) P(x, y) `$                     | Use joint PMF        |
| Continuous (rectangular)     | $` \mathbb{E}[g(X, Y)] = \iint g(x, y) f(x, y),dx,dy `$                         | Limits are constants |
| Continuous (non-rectangular) | $` \mathbb{E}[g(X, Y)] = \int\_a^b \int\_{\text{inner}} g(x, y) f(x, y),dy,dx `$ | Set bounds carefully |

---

The **Rule of the Lazy Statistician** is a powerful shortcut: when asked for $`\mathbb{E}[g(X, Y)]`$, don’t marginalize—just integrate or sum over the joint distribution directly.
This is particularly efficient in multivariable statistical computations and probabilistic modeling.
