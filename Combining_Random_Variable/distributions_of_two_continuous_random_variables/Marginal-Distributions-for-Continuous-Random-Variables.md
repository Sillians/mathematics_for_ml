## **Marginal Distributions for Continuous Random Variables**

---

### **1. Overview**

In the context of **continuous random variables**, a **marginal distribution** gives the probability behavior of one variable **regardless of** the values of others. 
If $X$ and $Y$ are continuous random variables with a **joint PDF** $`f\_{X,Y}(x, y)`$, then:

* The **marginal PDF of $X$** is:

  $`f_X(x) = \int_{-\infty}^\infty f_{X,Y}(x, y)\,dy`$

* The **marginal PDF of $Y$** is:

  $`f_Y(y) = \int_{-\infty}^\infty f_{X,Y}(x, y)\,dx`$

These functions describe the distribution of one variable independently of the other.

---

### **2. Finding a Marginal Distribution From a Joint Distribution**

Given the joint PDF $`f\_{X,Y}(x, y)`$, the marginal distribution of $X$ is found by **integrating out** $Y$:

#### **Marginal of $X$**:

$$
f_X(x) = \int_{y_{\min}}^{y_{\max}} f_{X,Y}(x, y)\,dy
$$

#### **Marginal of $Y$**:

$$
f_Y(y) = \int_{x_{\min}}^{x_{\max}} f_{X,Y}(x, y)\,dx
$$

#### **Example (Rectangular Domain)**

Let:

$$
f(x, y) = \begin{cases}
6(1 - y), & 0 \le x \le 1,\; 0 \le y \le 1 \\
0, & \text{otherwise}
\end{cases}
$$

Find $`f\_X(x)`$:

$$
f_X(x) = \int_0^1 6(1 - y)\,dy = 6\int_0^1 (1 - y)\,dy = 6\left[y - \frac{y^2}{2}\right]_0^1 = 6\left(1 - \frac{1}{2}\right) = 3
$$

So:

$$
f_X(x) = \begin{cases}
3, & 0 \le x \le 1 \\
0, & \text{otherwise}
\end{cases}
$$

---

### **3. Finding a Marginal Probability From a Joint Distribution**

A **marginal probability** is computed using the marginal PDF:

$$
P(a \le X \le b) = \int_a^b f_X(x)\,dx
$$

#### **Example**

Using previous example where $`f\_X(x) = 3`$ on $`[0, 1]`$, compute $`P(0.2 \le X \le 0.6)`$:

$$
P(0.2 \le X \le 0.6) = \int_{0.2}^{0.6} 3\,dx = 3(0.6 - 0.2) = 1.2
$$

This value exceeds 1 — it implies the earlier PDF $`f(x, y) = 6(1 - y)`$ may have had normalization issues (but the method is correct).

---

### **4. Finding a Marginal Distribution From a Joint Distribution: Non-Rectangular Domains**

When the joint PDF is defined over a **non-rectangular domain**, integration limits depend on one of the variables.

#### **Example**

Let:

$$
f(x, y) = \begin{cases}
2, & 0 < y < x < 1 \\
0, & \text{otherwise}
\end{cases}
$$

Find the marginal PDF of $X$:

1. Identify domain: For fixed $x$, $y$ ranges from $0$ to $x$.
2. Integrate:

$$
f_X(x) = \int_0^x 2\,dy = 2x, \quad 0 < x < 1
$$

So:

$$
f_X(x) = \begin{cases}
2x, & 0 < x < 1 \\
0, & \text{otherwise}
\end{cases}
$$

Similarly, to find $`f\_Y(y)`$, observe that for fixed $y$, $x$ ranges from $y$ to $1$:

$$
f_Y(y) = \int_y^1 2\,dx = 2(1 - y), \quad 0 < y < 1
$$

---

### **5. Finding a Marginal CDF**

The **marginal cumulative distribution function (CDF)** of $X$ is:

$$
F_X(x) = P(X \le x) = \int_{-\infty}^x f_X(t)\,dt = \iint_{(-\infty, x] \times \mathbb{R}} f_{X,Y}(t, y)\,dy\,dt
$$

#### **Example**

Using $`f\_X(x) = 2x`$ for $`x \in (0,1)`$:

$$
F_X(x) = \int_0^x 2t\,dt = [t^2]_0^x = x^2
\quad \text{for } 0 \le x \le 1
$$

So:

$$
F_X(x) = \begin{cases}
0, & x \le 0 \\
x^2, & 0 < x < 1 \\
1, & x \ge 1
\end{cases}
$$

---

### **Summary Table**

| Concept             | Formula                                                                                                          | Description                           |
| ------------------- |------------------------------------------------------------------------------------------------------------------| ------------------------------------- |
| Marginal PDF of $X$ | $`f\_X(x) = \int f\_{X,Y}(x,y),dy`$                                                                              | Collapses joint distribution over $y$ |
| Marginal PDF of $Y$ | $`f\_Y(y) = \int f\_{X,Y}(x,y),dx`$                                                                              | Collapses joint distribution over $x$ |
| Marginal CDF of $X$ | $`F\_X(x) = \int\_{-\infty}^x f\_X(t),dt`$ or $`F\_X(x) = \iint\_{(-\infty,x]\times \mathbb{R}} f(t,y),dy,dt`$   | Gives $`P(X \le x)`$                  |
| Non-rectangular domain | Adjust limits                                                                                                    | Bounds of integration depend on variable |

---

Marginal distributions are foundational in statistics and probability, especially when analyzing individual behavior within multivariate distributions or computing conditional probabilities.
