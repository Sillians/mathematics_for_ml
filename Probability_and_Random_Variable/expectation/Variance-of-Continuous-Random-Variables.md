## **Variance of Continuous Random Variables**

The **variance** of a continuous random variable quantifies the **spread** of its values 
around the mean. For a variable $X$ with a given probability density function (PDF), 
variance is defined using integral calculus.

---

### **1. Definition of Variance for Continuous Random Variables**

Let $X$ be a continuous random variable with probability density function $f(x)$. 
The **variance** of $X$ is:

$$
\mathrm{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2
$$

Where:

* $`\mathbb{E}[X] = \int_{-\infty}^{\infty} x f(x)\, dx`$
* $`\mathbb{E}[X^2] = \int_{-\infty}^{\infty} x^2 f(x)\, dx`$

---

###  **2. Computing the Variance Given a Two-Branch PDF**

Suppose $`f(x)`$ is defined piecewise over two intervals:

$$
f(x) =
\begin{cases}
f_1(x), & a \le x < c \\
f_2(x), & c \le x \le b
\end{cases}
$$

Then:

* Compute $`\mathbb{E}[X]`$:

$$
\mathbb{E}[X] = \int_a^c x f_1(x)\, dx + \int_c^b x f_2(x)\, dx
$$

* Compute $`\mathbb{E}[X^2]`$:

$$
\mathbb{E}[X^2] = \int_a^c x^2 f_1(x)\, dx + \int_c^b x^2 f_2(x)\, dx
$$

* Then:

$$
\mathrm{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2
$$

---

#### ✅ **Example (Two-Branch PDF):**

$$
f(x) =
\begin{cases}
x, & 0 \le x \le 1 \\
2 - x, & 1 < x \le 2
\end{cases}
$$

Verify it’s a valid PDF and then compute:

* $`\mathbb{E}[X] = \int_0^1 x^2 dx + \int_1^2 x(2 - x) dx`$
* $`\mathbb{E}[X^2] = \int_0^1 x^3 dx + \int_1^2 x^2(2 - x) dx`$
* Compute variance with:

$$
\mathrm{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2
$$

---

### **3. Computing the Variance Given a Three-Branch PDF**

Suppose:

$$
f(x) =
\begin{cases}
f_1(x), & a \le x < d \\
f_2(x), & d \le x < e \\
f_3(x), & e \le x \le b
\end{cases}
$$

Then:

* $`\mathbb{E}[X] = \int_a^d x f_1(x)\, dx + \int_d^e x f_2(x)\, dx + \int_e^b x f_3(x)\, dx`$

* $`\mathbb{E}[X^2] = \int_a^d x^2 f_1(x)\, dx + \int_d^e x^2 f_2(x)\, dx + \int_e^b x^2 f_3(x)\, dx`$

* Then again:

$$
\mathrm{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2
$$

---

#### ✅ **Example (Three-Branch Structure)**

$$
f(x) =
\begin{cases}
k, & 0 \le x < 1 \\
2k, & 1 \le x < 2 \\
k, & 2 \le x \le 3
\end{cases}
$$

1. Determine $k$ by solving:

$$
\int_0^1 k dx + \int_1^2 2k dx + \int_2^3 k dx = 1
\Rightarrow k = \frac{1}{4}
$$

2. Use this to compute:

* $`\mathbb{E}[X] = \int_0^1 x \cdot \frac{1}{4} dx + \int_1^2 x \cdot \frac{2}{4} dx + \int_2^3 x \cdot \frac{1}{4} dx`$
* $`\mathbb{E}[X^2] = \int_0^1 x^2 \cdot \frac{1}{4} dx + \int_1^2 x^2 \cdot \frac{2}{4} dx + \int_2^3 x^2 \cdot \frac{1}{4} dx`$
* Then compute variance.

---

### ✅ **Summary Table**

| Step                         | Formula                                               |
| ---------------------------- | ----------------------------------------------------- |
| Mean                         | $`\mathbb{E}[X] = \int x f(x)\, dx`$                    |
| Second Moment                | $`\mathbb{E}[X^2] = \int x^2 f(x)\, dx`$                |
| Variance                     | $`\text{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2`$ |
| Multi-branch PDF integration | Sum integrals over each branch                        |

---

### **Conclusion**

Computing variance for continuous random variables—especially from piecewise PDFs—relies on 
calculating both the **first and second moments** using integrals over defined intervals. 
Whether the PDF is one-part or multi-branch, variance always reflects how widely values of 
the random variable spread around their expected value.
