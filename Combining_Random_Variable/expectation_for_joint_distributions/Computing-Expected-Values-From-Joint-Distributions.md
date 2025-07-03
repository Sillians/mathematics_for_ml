## **Computing Expected Values From Joint Distributions**

---

### **1. Overview**

When two or more random variables have a **joint distribution**, we can compute the **expected value** 
of a single variable or a function of variables directly from the joint distribution, *without first computing the marginal distributions*. 
This is a direct application of the **Rule of the Lazy Statistician**.

Let $X$ and $Y$ be random variables defined on the same probability space with joint distribution:

* **Discrete case**: joint PMF $`p(x, y) = P(X = x, Y = y)`$
* **Continuous case**: joint PDF $`f(x, y) = f\_{X,Y}(x, y)`$

---

### **2. Finding the Expected Value of a Discrete Random Variable From a Joint Distribution**

For a discrete random variable $X$ with joint PMF $p(x, y)$:

$$
\mathbb{E}[X] = \sum_x \sum_y x \cdot p(x, y)
$$

Similarly, for $Y$:

$$
\mathbb{E}[Y] = \sum_x \sum_y y \cdot p(x, y)
$$

#### **Example**

Let $`X, Y`$ be defined with the following joint PMF:

| $`Y \backslash X`$  | 0   | 1   |
|---------------------| --- | --- |
| 0                   | 0.1 | 0.2 |
| 1                   | 0.3 | 0.4 |

**Compute** $`\mathbb{E}[X]`$:

$$
\mathbb{E}[X] = \sum_x \sum_y x \cdot p(x, y)
= 0 \cdot (0.1 + 0.3) + 1 \cdot (0.2 + 0.4) = 0 + 0.6 = \boxed{0.6}
$$

**Compute** $`\mathbb{E}[Y]`$:

$$
\mathbb{E}[Y] = \sum_x \sum_y y \cdot p(x, y)
= 0 \cdot (0.1 + 0.2) + 1 \cdot (0.3 + 0.4) = 0 + 0.7 = \boxed{0.7}
$$

---

### **3. Finding the Expected Value of a Continuous Random Variable From a Joint Distribution**

For continuous random variables $X$ and $Y$ with joint PDF $`f(x, y)`$:

$$
\mathbb{E}[X] = \iint_{\mathbb{R}^2} x \cdot f(x, y)\,dx\,dy
$$

$$
\mathbb{E}[Y] = \iint_{\mathbb{R}^2} y \cdot f(x, y)\,dx\,dy
$$

You integrate $`x \cdot f(x, y)`$ or $`y \cdot f(x, y)`$ over the entire **support** of the joint PDF.

#### **Example (Rectangular Domain)**

Let:

$$
f(x, y) = \begin{cases}
4xy, & 0 \le x \le 1,\; 0 \le y \le 1 \\
0, & \text{otherwise}
\end{cases}
$$

**Compute** $`\mathbb{E}[X]`$:

$$
\mathbb{E}[X] = \int_0^1 \int_0^1 x \cdot 4xy\,dy\,dx
= \int_0^1 4x^2 \int_0^1 y\,dy\,dx
= \int_0^1 4x^2 \cdot \frac{1}{2}\,dx
= 2 \int_0^1 x^2\,dx = 2 \cdot \frac{1}{3} = \boxed{\frac{2}{3}}
$$

**Compute** $`\mathbb{E}[Y]`$:

$$
\mathbb{E}[Y] = \int_0^1 \int_0^1 y \cdot 4xy\,dx\,dy
= \int_0^1 4y^2 \int_0^1 x\,dx\,dy
= \int_0^1 4y^2 \cdot \frac{1}{2}\,dy
= 2 \int_0^1 y^2\,dy = 2 \cdot \frac{1}{3} = \boxed{\frac{2}{3}}
$$

---

### **4. Summary Table**

| Case           | Formula for $`\mathbb{E}[X]`$    | Notes                                |
| -------------- | -------------------------------- | ------------------------------------ |
| **Discrete**   | $`\sum\_x \sum\_y x \cdot p(x, y)`$ | Directly sum over joint PMF          |
| **Continuous** | $`\iint x \cdot f(x, y),dx,dy`$   | Integrate over the joint PDF support |

---

### **5. Key Insights**

* **Do not** marginalize unless needed — compute expectations directly from the joint.
* Expectations reflect **weighted averages** over all $`(x, y)`$ values, using the joint distribution as weights.
* This technique is widely used in **multivariate statistics**, **machine learning**, and **econometrics**.

---

This approach ensures efficient and elegant computation of expected values in both discrete and continuous multivariate probability models.
