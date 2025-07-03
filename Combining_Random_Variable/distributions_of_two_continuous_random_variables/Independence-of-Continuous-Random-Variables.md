## **Independence of Continuous Random Variables**

---

### **1. Overview**

Two continuous random variables $X$ and $Y$ are **independent** if the occurrence of one does not influence the probability distribution of the other. 
Mathematically, this means the joint probability density function (PDF) **factors** into the product of the marginal PDFs:

$$
f_{X,Y}(x, y) = f_X(x) \cdot f_Y(y) \quad \text{for all } x, y
$$

This factorization is both **necessary and sufficient** for independence.

---

### **2. Finding the Joint PDF of Two Independent Random Variables Using Marginal PDFs**

If $`X`$ and $`Y`$ are **independent**, and their marginal PDFs are known as:

* $`f_X(x)`$: the PDF of $`X`$
* $`f_Y(y)`$: the PDF of $`Y`$

Then their joint PDF is:

$$
f(x, y) = f_X(x) \cdot f_Y(y)
$$

#### **Example**

Let:

* $`f_X(x) = e^{-x}`$ for $`x \ge 0`$ (Exponential)
* $`f_Y(y) = 2y`$ for $`0 \le y \le 1`$ (Beta(2,1))

Then the joint PDF is:

$$
f(x, y) = f_X(x) \cdot f_Y(y) = e^{-x} \cdot 2y, \quad x \ge 0,\; 0 \le y \le 1
$$

---

### **3. Finding a Joint Probability for Independent Random Variables Using Marginals**

If $`X`$ and $`Y`$ are independent, then for any region $`A \times B \subset \mathbb{R}^2`$, the probability is:

$$
P(X \in A,\ Y \in B) = P(X \in A) \cdot P(Y \in B)
$$

#### **Example**

Using the same marginals:

* $`P(X > 1) = \int_1^{\infty} e^{-x}\,dx = e^{-1}`$
* $`P(0 \le Y \le 0.5) = \int_0^{0.5} 2y\,dy = y^2\Big|_0^{0.5} = 0.25`$

So:

$$
P(X > 1,\ 0 \le Y \le 0.5) = P(X > 1) \cdot P(0 \le Y \le 0.5) = e^{-1} \cdot 0.25
$$

---

### **4. Determining Whether Two Continuous Random Variables Are Independent**

Given a joint PDF $`f(x, y)`$, check independence by:

#### **Step 1: Compute Marginal PDFs**

$$
f_X(x) = \int_{-\infty}^{\infty} f(x, y)\,dy,\quad
f_Y(y) = \int_{-\infty}^{\infty} f(x, y)\,dx
$$

#### **Step 2: Multiply the Marginals**

$$
f_X(x) \cdot f_Y(y)
$$

#### **Step 3: Compare With $`f(x, y)`$**

If:

$$
f(x, y) = f_X(x) \cdot f_Y(y) \quad \text{for all } x, y
$$

then $`X`$ and $`Y`$ are independent.

---

#### **Example**

Given:

$$
f(x, y) = \begin{cases}
4xy, & 0 \le x \le 1,\ 0 \le y \le 1 \\
0, & \text{otherwise}
\end{cases}
$$

* $`f_X(x) = \int_0^1 4xy\,dy = 4x \cdot \int_0^1 y\,dy = 4x \cdot \frac{1}{2} = 2x`$
* $`f_Y(y) = \int_0^1 4xy\,dx = 4y \cdot \int_0^1 x\,dx = 4y \cdot \frac{1}{2} = 2y`$

Then:

$$
f_X(x) \cdot f_Y(y) = 2x \cdot 2y = 4xy = f(x, y)
$$

✅ $X$ and $Y$ are **independent**

---

### **5. Summary Table**

| Task                        | Expression                                            | Condition                      |
| --------------------------- |-------------------------------------------------------|--------------------------------|
| **Joint PDF (independent)** | $`f(x, y) = f_X(x) \cdot f_Y(y)`$                     | If independent                 |
| **Joint probability**       | $`P(X \in A, Y \in B) = P(X \in A) \cdot P(Y \in B)`$ | If independent                 |
| **Check independence**      | Compare $`f(x, y)`$ with $`f_X(x) \cdot f_Y(y)`$      | Must be equal for all $`x, y`$ |

---

### **Key Insight**

Independence in continuous random variables simplifies computation and model analysis. 
It guarantees that knowledge of one variable gives no information about the other, making them completely separable in probabilistic modeling.
