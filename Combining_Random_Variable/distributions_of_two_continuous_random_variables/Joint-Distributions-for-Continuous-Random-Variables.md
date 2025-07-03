## **Joint Distributions for Continuous Random Variables**

---

### **1. Overview: Joint Distributions**

For two continuous random variables $X$ and $Y$, the **joint distribution** describes the probability structure of both variables together. 
This is defined by the **joint probability density function (PDF)**:

$$
f_{X,Y}(x,y)
$$

This function satisfies:

* $`f\_{X,Y}(x,y) \geq 0`$ for all $`(x,y)`$
* $`\displaystyle \iint\_{\mathbb{R}^2} f\_{X,Y}(x,y),dx,dy = 1`$

The probability that $`(X,Y)`$ lies in a region $`A \subseteq \mathbb{R}^2`$ is:

$$
P\big((X,Y) \in A\big) = \iint_A f_{X,Y}(x,y)\,dx\,dy
$$

---

### **2. Joint PDFs: Rectangular Domains**

A **rectangular domain** has constant lower and upper bounds for $x$ and $y$:

$$
a \leq x \leq b,\quad c \leq y \leq d
$$

#### **Example**

Let:

$$
f(x,y) = \begin{cases}
6xy & \text{if } 0 \leq x \leq 1,\; 0 \leq y \leq 1 \\
0 & \text{otherwise}
\end{cases}
$$

Verify it's a valid PDF:

$$
\int_0^1 \int_0^1 6xy\,dy\,dx
= \int_0^1 \left[3xy^2\right]_0^1 dx
= \int_0^1 3x\,dx = \frac{3}{2}
\quad \text{(Not valid PDF — must normalize)}
$$

To normalize:

$$
f(x,y) = \frac{6xy}{\int_0^1\int_0^1 6xy\,dy\,dx} = \frac{6xy}{3/2} = 4xy
$$

Then:

$$
\int_0^1\int_0^1 4xy\,dy\,dx = 1
\quad \text{✓}
$$

---

### **3. Joint PDFs: Non-Rectangular Domains**

**Non-rectangular domains** arise when bounds of $x$ or $y$ depend on the other variable. 
These require care in setting limits of integration.

#### **Example**

Let:

$$
f(x,y) = \begin{cases}
2 & \text{if } 0 < y < x < 1 \\
0 & \text{otherwise}
\end{cases}
$$

This is a **triangular domain** bounded by $`y = 0`$, $`y = x`$, and $`x = 1`$.

Check normalization:

$$
\int_0^1 \int_0^x 2\,dy\,dx = \int_0^1 2x\,dx = [x^2]_0^1 = 1
\quad \text{✓}
$$

This domain can also be written as $`0 < x < 1`$, $`0 < y < x`$.

---

### **4. Computing a Probability Using a Joint PDF**

To compute $`P((X,Y) \in A)`$, integrate the joint PDF over region $A$:

$$
P((X,Y) \in A) = \iint_A f(x,y)\,dx\,dy
$$

#### **Example (Rectangular Domain)**

Suppose $`f(x,y) = 4xy`$ over $`[0,1] \times [0,1]`$. Find:

$$
P(X \leq 0.5,\; Y \leq 0.25)
$$

$$
\int_0^{0.5} \int_0^{0.25} 4xy\,dy\,dx = \int_0^{0.5} \left[2xy^2\right]_0^{0.25} dx = \int_0^{0.5} 2x(0.25)^2\,dx = \int_0^{0.5} 2x(1/16)\,dx
$$

$$
= \frac{1}{8} \int_0^{0.5} x\,dx = \frac{1}{8} \cdot \frac{1}{4} = \frac{1}{32}
$$

#### **Example (Non-Rectangular Domain)**

Let $`f(x,y) = 2`$ over $`0 < y < x < 1`$. Compute $`P(Y < 0.5)`$.

Set bounds: $y$ ranges from $0$ to $0.5$, but $x$ must satisfy $`y < x < 1`$.

$$
\int_0^{0.5} \int_y^1 2\,dx\,dy = \int_0^{0.5} 2(1 - y)\,dy
= \left[2y - y^2\right]_0^{0.5} = 1 - \frac{1}{4} = \frac{3}{4}
$$

---

### **5. Marginal Densities**

From the joint PDF $`f(x,y)`$, the **marginal PDFs** are:

* For $X$:

  $$
  f_X(x) = \int_{-\infty}^{\infty} f(x,y)\,dy
  $$

* For $Y$:

  $$
  f_Y(y) = \int_{-\infty}^{\infty} f(x,y)\,dx
  $$

Used to compute distributions of individual variables.

---

### **6. Independence**

$X$ and $Y$ are **independent** if:

$$
f(x,y) = f_X(x) \cdot f_Y(y)
\quad \text{for all } x,y
$$

Otherwise, they are **dependent**.

---

### **Summary Table**

| Topic                  | Key Idea                      | Formula/Description                        |
| ---------------------- |-------------------------------|--------------------------------------------|
| Joint PDF              | Density over $`\mathbb{R}^2`$ | $`f(x,y) \geq 0`$, $`\iint f(x,y) = 1`$    |
| Rectangular domain     | Constant bounds               | $`\iint\_{[a,b]\times[c,d]} f(x,y),dy,dx`$ |
| Non-rectangular domain | Bounds depend on $x$ or $y$   | Set integration limits carefully           |
| Probability            | Area under PDF                | $`P((X,Y) \in A) = \iint\_A f(x,y),dx,dy`$ |
| Marginal PDFs          | Integrate out other variable  | $`f\_X(x) = \int f(x,y),dy`$               |
| Independence           | Factorization of PDF          | $`f(x,y) = f\_X(x)f\_Y(y)`$                |

---

This deep dive forms the basis for multivariable probability, especially in applications such as statistics, machine learning, and Bayesian inference.
