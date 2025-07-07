## **Conditional Distributions for Continuous Random Variables**

---

### **1. Working With the Definition of a Conditional PDF**

Let $X$ and $Y$ be continuous random variables with a joint probability density function (PDF) $`f_{X,Y}(x,y)`$.
If the marginal PDF of $Y$, denoted $`f_Y(y)`$, is positive at a given point $y$, then the **conditional PDF** of $X$ given $`Y = y`$ is defined by:

$$
f_{X|Y}(x \mid y) = \frac{f_{X,Y}(x, y)}{f_Y(y)} \quad \text{for } f_Y(y) > 0
$$

Similarly,

$$
f_{Y|X}(y \mid x) = \frac{f_{X,Y}(x, y)}{f_X(x)} \quad \text{for } f_X(x) > 0
$$

Where:

* $`f_{X,Y}(x,y)`$ is the joint PDF,
* $`f_Y(y) = \int_{-\infty}^{\infty} f_{X,Y}(x,y)\,dx`$ is the marginal of $Y$,
* $`f_X(x) = \int_{-\infty}^{\infty} f_{X,Y}(x,y)\,dy`$ is the marginal of $X$.

---

### **2. Finding a Conditional PDF**

#### **Example:**

Let the joint PDF be:

$$
f_{X,Y}(x,y) = \begin{cases}
3(x + 2y)/2, & 0 \leq y \leq x \leq 1 \\
0, & \text{otherwise}
\end{cases}
$$

**Step 1: Find the marginal of $Y$:**

$$
f_Y(y) = \int_y^1 \frac{3(x + 2y)}{2} \, dx
= \frac{3}{2} \int_y^1 (x + 2y)\,dx
= \frac{3}{2} \left[ \frac{1}{2}(1^2 - y^2) + 2y(1 - y) \right]
$$

$$
f_Y(y) = \frac{3}{2} \left[ \frac{1 - y^2}{2} + 2y(1 - y) \right]
= \frac{3}{2} \left[ \frac{1 - y^2 + 4y - 4y^2}{2} \right]
= \frac{3}{2} \cdot \frac{1 + 4y - 5y^2}{2}
= \frac{3(1 + 4y - 5y^2)}{4}
$$

**Step 2: Conditional PDF $`f_{X|Y}(x \mid y)`$:**

$$
f_{X|Y}(x \mid y) = \frac{f_{X,Y}(x,y)}{f_Y(y)} = \frac{ \frac{3(x + 2y)}{2} }{ \frac{3(1 + 4y - 5y^2)}{4} }
= \frac{2(x + 2y)}{1 + 4y - 5y^2}
\quad \text{for } y \leq x \leq 1
$$

---

### **3. Computing a Conditional Probability**

Using the conditional PDF from above, to find:

$$
P\left( X < \frac{2}{5} \mid Y = \frac{1}{5} \right)
$$

**Step 1: Plug $`y = \frac{1}{5}`$ into the conditional PDF:**

$$
f_{X|Y}\left(x \mid \frac{1}{5}\right) = \frac{2(x + \frac{2}{5})}{1 + \frac{4}{5} - \frac{5}{25}} 
= \frac{2(x + \frac{2}{5})}{\frac{45 - 5}{25}} = \frac{2(x + \frac{2}{5})}{\frac{40}{25}} = \frac{5(x + \frac{2}{5})}{4}
$$

\*\*Step 2: Integrate from $`x = \frac{1}{5}`$ to $`x = \frac{2}{5}`$ (because $`y = 1/5 \leq x \leq 1`$):

$$
P = \int_{1/5}^{2/5} \frac{5(x + 2/5)}{4} \, dx
= \frac{5}{4} \int_{1/5}^{2/5} \left(x + \frac{2}{5} \right) dx
= \frac{5}{4} \left[ \frac{1}{2}x^2 + \frac{2}{5}x \right]_{1/5}^{2/5}
$$

$$
= \frac{5}{4} \left( \left[ \frac{1}{2}\left(\frac{4}{25}\right) + \frac{4}{25} \right] - \left[ \frac{1}{2}\left(\frac{1}{25}\right) + \frac{2}{25} \right] \right)
= \frac{5}{4} \left( \frac{2}{25} + \frac{4}{25} - \left( \frac{1}{50} + \frac{2}{25} \right) \right)
$$

$$
= \frac{5}{4} \left( \frac{6}{25} - \left( \frac{1}{50} + \frac{2}{25} \right) \right)
= \frac{5}{4} \left( \frac{6}{25} - \frac{5}{50} \right)
= \frac{5}{4} \cdot \left( \frac{12 - 5}{50} \right) = \frac{5}{4} \cdot \frac{7}{50} = \frac{35}{200} = \frac{7}{40}
$$

---

### **4. Summary Table**

| Concept                           | Formula                                                        |
|-----------------------------------|----------------------------------------------------------------|
| Conditional PDF                   | $`( f_{X\|Y}(x \mid y) = \dfrac{f_{X,Y}(x,y)}{f_Y(y)}`$        |
| Conditional Probability           | $`( P(a < X < b \mid Y = y) = \int_a^b f_{X\|Y}(x \mid y)\,dx`$ |
| Marginal PDF of \( Y \)           | $`( f_Y(y) = \int f_{X,Y}(x,y)\,dx`$                           |
| Law of Total Probability          | $`( f_X(x) = \int f_{X\|Y}(x \mid y)\,f_Y(y)\,dy`$             |

---


### **5. Applications**

* **Reliability:** Probability a device lasts $X$ hours, given temperature $Y$.
* **Bayesian Inference:** Posterior distributions rely on conditional PDFs.
* **Signal Processing:** Estimating signals given observed noise.
* **Economics:** Wages $X$ given education $Y$.
* **Environmental Modelling:** Rainfall $X$ conditioned on humidity $Y$.

This approach underlies much of conditional reasoning in probability and statistics.
