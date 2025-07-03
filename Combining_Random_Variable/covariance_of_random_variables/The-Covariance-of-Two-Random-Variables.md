## **The Covariance of Two Random Variables**

---

### **1. What Is Covariance?**

Covariance measures the **linear relationship** between two random variables $X$ and $Y$:

* **Positive covariance**: $X$ and $Y$ tend to increase together.
* **Negative covariance**: One increases while the other decreases.
* **Zero covariance**: No linear relationship.

---

### **2. Covariance — Formal Definition**

$$
\text{Cov}(X, Y) = \mathbb{E}\left[(X - \mathbb{E}[X])(Y - \mathbb{E}[Y])\right]
$$

This definition captures how deviations from each variable’s mean interact on average.

---

### **3. Shortcut Formula for Covariance**

Using linearity of expectation:

$$
\text{Cov}(X, Y) = \mathbb{E}[XY] - \mathbb{E}[X]\,\mathbb{E}[Y]
$$

This is often easier to compute directly and is valid for both discrete and continuous variables.

---

### **4. Calculating Covariance (Discrete Case)**

Given joint PMF $`p(x, y)`$, we compute:

* $`\mathbb{E}[X] = \sum_x \sum_y x\,p(x, y)`$


* $`\mathbb{E}[Y] = \sum_x \sum_y y\,p(x, y)`$


* $`\mathbb{E}[XY] = \sum_x \sum_y x y\,p(x, y)`$


* Then plug into the shortcut formula.

#### **Example**

Let the joint PMF be:

| $`X \backslash Y`$ | 1   | 2   |
| ---------------- | --- | --- |
| 1                | 0.1 | 0.2 |
| 2                | 0.3 | 0.4 |

Compute:

* $`\mathbb{E}[X] = 1(0.1 + 0.2) + 2(0.3 + 0.4) = 0.3 + 1.4 = 1.7`$


* $`\mathbb{E}[Y] = 1(0.1 + 0.3) + 2(0.2 + 0.4) = 0.4 + 1.2 = 1.6`$


* $`\mathbb{E}[XY] = 1(1)(0.1) + 1(2)(0.2) + 2(1)(0.3) + 2(2)(0.4) = 0.1 + 0.4 + 0.6 + 1.6 = 2.7`$

So:

$$
\text{Cov}(X, Y) = 2.7 - (1.7)(1.6) = 2.7 - 2.72 = -0.02
$$

---

### **5. Calculating Covariance (Continuous Case)**

Given joint PDF $`f(x, y)`$:

$$
\text{Cov}(X, Y) = \mathbb{E}[XY] - \mathbb{E}[X]\,\mathbb{E}[Y]
$$

Where:

* $`\mathbb{E}[X] = \int\!\int x\,f(x, y)\,dx\,dy`$


* $`\mathbb{E}[Y] = \int\!\int y\,f(x, y)\,dx\,dy`$


* $`\mathbb{E}[XY] = \int\!\int xy\,f(x, y)\,dx\,dy`$

---

#### **Example**

Let:

$$
f(x, y) = \begin{cases}
4xy, & 0 \le x \le 1,\; 0 \le y \le 1 \\
0, & \text{otherwise}
\end{cases}
$$

Then:

* $`\mathbb{E}[X] = \int_0^1 \int_0^1 x \cdot 4xy\,dy\,dx = 4 \int_0^1 x^2 \left[\int_0^1 y\,dy\right] dx = 4 \int_0^1 x^2 \cdot \frac{1}{2}\,dx = 2 \int_0^1 x^2\,dx = \frac{2}{3}`$


* Similarly, $`\mathbb{E}[Y] = \frac{2}{3}`$


* $`\mathbb{E}[XY] = \int_0^1 \int_0^1 xy \cdot 4xy\,dy\,dx = 4 \int_0^1 x^2\,dx \int_0^1 y^2\,dy = 4 \cdot \frac{1}{3} \cdot \frac{1}{3} = \frac{4}{9}`$

Now compute covariance:

$$
\text{Cov}(X, Y) = \frac{4}{9} - \left(\frac{2}{3}\right)^2 = \frac{4}{9} - \frac{4}{9} = 0
$$

✅ **Covariance is zero**, but this does **not imply independence** unless the joint PDF also factorizes.

---

### **6. Summary Table**

| Formula                                                                   | Description           |
|---------------------------------------------------------------------------| --------------------- |
| $`\text{Cov}(X, Y) = \mathbb{E}[(X - \mathbb{E}[X])(Y - \mathbb{E}[Y])]`$ | Definition            |
| $`\text{Cov}(X, Y) = \mathbb{E}[XY] - \mathbb{E}[X]\mathbb{E}[Y]`$        | Shortcut              |
| $`\text{Cov}(X, X) = \text{Var}(X)`$                                      | Variance special case |
| $`\text{Cov}(aX + b, cY + d) = ac\,\text{Cov}(X, Y)`$                     | Linear scaling rule   |

---

### **Key Insight**

Covariance provides a **directional measure** of how two random variables move together. 
While zero covariance means **no linear association**, only factorization of the joint PDF/PMF guarantees **independence**.
