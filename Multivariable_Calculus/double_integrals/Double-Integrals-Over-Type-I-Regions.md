## **Double Integrals Over Type I Regions**

---

### **1. Definition of a Type I Region**

A planar region $`D`$ is **Type I** if it can be swept out by vertical segments:


$$
D = \lbrace{(x,y) \mid a \leq x \leq b,\; g_1(x) \leq y \leq g_2(x)\rbrace}
$$


with continuous bounds $`g_1,g_2`$ on $`[a,b]`$ and $`g_1(x)\le g_2(x)`$.


For an integrable function $`f(x,y)`$,

$$
\iint_{D} f(x,y)\,dA
=\int_{a}^{b}\!\Bigl[\int_{g_1(x)}^{g_2(x)} f(x,y)\,dy\Bigr]dx.
$$

The inner integral accumulates along each vertical slice; the outer integral sums these slices along the $x$‑axis.

---

### **2. Representing a Double Integral as a Repeated Integral**

#### **2.1 When the Limits Are Given**

If $`D`$ is already expressed in Type I form, substitute limits directly:

$$
\boxed{
\iint_D f(x,y)\,dA
=\int_{a}^{b}\!\int_{g_1(x)}^{g_2(x)} f(x,y)\,dy\,dx.}
$$

*Example*
$`D=\{(x,y)\mid 0\le x\le1,\;x^2\le y\le x+1\}`$

$$
\iint_D f\,dA=\int_0^1\!\int_{x^{2}}^{x+1} f(x,y)\,dy\,dx.
$$



#### **2.2 When the Limits Are Not Given**

1. **Sketch or visualize** the region.


2. **Project onto the $x$‑axis** to find $`a\le x\le b`$.


3. For each $`x`$ in $[a,b]$, identify


   $`g_1(x)=\text{lower }y`$ and $`g_2(x)=\text{upper }y`$.


4. Write the repeated integral in the same form.



*Example*
Region bounded by $`y=x^2`$ (below) and $`y=2`$ (above) for $`x\ge0`$:

* Projection → $`0\le x\le\sqrt2`$.


* Bounds → $`g_1(x)=x^2,\; g_2(x)=2`$.

$$
\iint_D f\,dA=\int_{0}^{\sqrt2}\!\int_{x^{2}}^{2} f(x,y)\,dy\,dx.
$$

---

### **3. Evaluating a Repeated Integral Over a Type I Region**

1. **Inner integral** (first with respect to $`y`$):

$$
F(x)=\int_{g_1(x)}^{g_2(x)} f(x,y)\,dy.
$$

2. **Outer integral** (with respect to $`x`$):

$$
\iint_D f\,dA=\int_{a}^{b} F(x)\,dx.
$$

*Worked example*


Evaluate $`\displaystyle \iint_D (x+y)\,dA`$ for
$`D=\{(x,y)\mid 0\le x\le1,\;x\le y\le x+1\}`$.


$`\begin{aligned} \text{Inner: }&\int_{y=x}^{x+1} (x+y)\,dy =\bigl[x\,y+\tfrac12 y^{2}\bigr]_{x}^{x+1} =x(1)+\tfrac12[(x+1)^2-x^{2}] =x+\tfrac12(2x+1).\\[4pt] \text{Outer: }&\int_{0}^{1} \!\bigl(2x+\tfrac12\bigr)\,dx =\Bigl[x^{2}+\tfrac12x\Bigr]_{0}^{1} =\tfrac32. \end{aligned}`$


---

### **4. Calculating a Double Integral (Area or Mass) Over a Type I Region**

* **Area** ($`f\equiv1`$):

$$
\text{Area}(D)=\int_{a}^{b}\!\bigl[g_2(x)-g_1(x)\bigr]\,dx.
$$

* **Mass** with density $`\rho(x,y)`$: use the same integral with $`\rho`$ in place of 1.

*Example (area of upper half‑circle of radius $r$)*
$`D=\{(x,y)\mid -r\le x\le r,\;0\le y\le\sqrt{r^{2}-x^{2}}\}`$

$$
\text{Area}(D)=\int_{-r}^{r}\!\int_{0}^{\sqrt{r^{2}-x^{2}}}1\,dy\,dx
               =\int_{-r}^{r}\sqrt{r^{2}-x^{2}}\,dx
               =\tfrac{\pi r^{2}}{2}.
$$

---

### **Summary**

| Task                       | Core Idea                                    |
|----------------------------|----------------------------------------------|
| Identify Type I limits | $`a\le x\le b`$, $`g_1(x)\le y\le g_2(x)`$.  |
| **Given** limits           | Insert directly into $`\int\int f\,dy\,dx`$. |
| **Not given** limits    | Sketch → project onto $x$ → read $`g_1, g_2`$. |
| Evaluate                   | Integrate in $y$ first, then $x$.            |
| Constant $f$               | Integral equals geometric area of $D$.       |

Mastery of Type I regions streamlines setup and evaluation of double integrals, turning geometric descriptions into precise analytic results.
