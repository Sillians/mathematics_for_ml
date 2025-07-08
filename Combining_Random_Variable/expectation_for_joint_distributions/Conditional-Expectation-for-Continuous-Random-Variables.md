## **Conditional Expectation for Continuous Random Variables**

---

## 1 | What Is Conditional Expectation?

For two continuous random variables $X$ and $Y$ with joint PDF $`f_{X,Y}(x,y)`$, the **conditional expectation of $`X`$ given $`Y=y`$** is

$$
\boxed{ \;E[X \mid Y = y] \;=\;\int_{-\infty}^{\infty} x \, f_{X|Y}(x\mid y)\,dx \;}
$$

where $`f_{X|Y}(x\mid y)=\dfrac{f_{X,Y}(x,y)}{f_Y(y)}`$ and $`f_Y(y)=\int_{-\infty}^{\infty}f_{X,Y}(x,y)\,dx`$.

Think of $`E[X\mid Y]`$ as the **best mean‑squared predictor** of $X$ when $Y$ is known.

---

## 2 | Calculating a Conditional Expectation From a Conditional PDF

### Example 1

Let

$$
f_{X|Y}(x\mid y)=\begin{cases}
2x,&0\le x\le1\\
0,&\text{otherwise}
\end{cases}
\quad(\text{for every fixed }y).
$$

Then

$$
E[X\mid Y=y]=\int_{0}^{1}x\,(2x)\,dx
             =2\int_{0}^{1}x^{2}\,dx
             =\frac23.
$$

Although the conditional PDF does not depend on $y$, writing $`E[X\mid Y]=\frac23`$ emphasises it is *a random variable that equals $`\tfrac23`$ for all $y$*.

---

## 3 | Calculating Conditional Expectations Given Joint and Marginal PDFs

### Example 2

Joint PDF

$$
f_{X,Y}(x,y)=\begin{cases}
4xy,&0\le x\le1,\;0\le y\le1\\
0,&\text{otherwise}.
\end{cases}
$$

**Step 1 — Marginal of $Y$**
$`f_Y(y)=\int_0^1 4xy\,dx=2y,\;0\le y\le1.`$

**Step 2 — Conditional PDF**
$`f_{X|Y}(x\mid y)=\dfrac{4xy}{2y}=2x,\;0\le x\le1.`$

**Step 3 — Conditional Expectation**
$`E[X\mid Y=y]=\int_0^1 x(2x)\,dx=\tfrac23.`$

Again, the result does not depend on $y$; the conditional mean is the constant $`2/3`$.

---

## 4 | Conditional Expectation as a Function

Formally, the mapping

$$
g(y)=E[X\mid Y=y]
$$

defines a **function of the conditioning variable**.
Thus the random variable $`E[X\mid Y]`$ is $`g(Y)`$.

### Properties

1. **Law of Iterated Expectation**
   $`E\!\bigl[E[X\mid Y]\bigr]=E[X]`$.


2. **Best Mean‑Squared Predictor**
   $`E[X\mid Y]`$ minimizes $`E[(X-h(Y))^{2}]`$ over all measurable functions $h$.


3. **Linearity**
   $`E[aX+bZ\mid Y]=aE[X\mid Y]+bE[Z\mid Y]`$.

---

## 5 | Another Worked Example

Let

$$
f_{X,Y}(x,y)=\begin{cases}
6(1-y),&0\le y\le x\le1\\
0,&\text{otherwise}.
\end{cases}
$$

### Marginal of $`Y`$

$$
f_Y(y)=\int_{y}^{1}6(1-y)\,dx=6(1-y)(1-y)=6(1-y)^{2},\quad0\le y\le1.
$$

### Conditional PDF $`f_{X|Y}`$

$$
f_{X|Y}(x\mid y)=\frac{6(1-y)}{6(1-y)^{2}}=\frac{1}{1-y},\quad y\le x\le1.
$$

### Conditional Expectation

$$
E[X\mid Y=y]=\int_{y}^{1}x\cdot\frac{1}{1-y}\,dx
            =\frac{1}{1-y}\bigl[\tfrac12(1^{2}-y^{2})\bigr]
            =\frac{1+y}{2}.
$$

Hence $`E[X\mid Y]=(1+Y)/2`$ — a **linear function** of $Y$.

---

## 6 | Key Takeaways

| Concept                     | Formula / Insight                                     | Notes                            |
|-----------------------------|-------------------------------------------------------|----------------------------------|
| Conditional PDF             | $`f_{X\|Y}(x \mid y) = \dfrac{f_{X,Y}(x,y)}{f_Y(y)}`$ | Ratio of joint to marginal density |
| Conditional Mean            | $`E[X \mid Y=y] = \int x f_{X\|Y}(x \mid y) \, dx`$   | Expectation under conditional dist. |
| Random-variable View        | $`E[X \mid Y] = g(Y)`$ where $`g(y) = E[X \mid Y=y]`$ | Function of the `RV` $Y$           |
| Law of Iterated Expectation | $`E[E[X \mid Y]] = E[X]`$                             | Tower property of expectations   |
| Predictor Property          | Minimizes mean-squared error among all \( h(Y) \)     | Best $L^2$ predictor             |


Mastering conditional expectation equips you for advanced topics such as regression, martingales, Bayesian inference, and optimal filtering.
