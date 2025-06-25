# **Level Curves**

A **level curve** (also called a *contour*) of a function

$`f:\mathbb R^2 \to \mathbb R`$ is the set of points in the $`xy`$-plane where the function attains a fixed value $c$:

$$
\boxed{\;f(x,y)=c\;}
$$

Thinking geometrically, each level curve is the “shadow’’ cast by the horizontal slice $`z=c`$ of the surface $`z=f(x,y)`$.

---

## 1 · Finding the Equation of a Level Curve

1. **Choose a value** $`c`$ (often several values are chosen to see a family of curves).

2. **Set the function equal to that value** and simplify.

> **Example**
> For $f(x,y)=\dfrac{x^2-y}{1+x^2}$, the level curve for $c=1$ is
>
> $$
> \frac{x^2-y}{1+x^2}=1
> \;\Longrightarrow\;
> y=-1.
> $$
>
> Thus the $c=1$ contour is the horizontal line $y=-1$.

---

## 2 · Determining the Shape of a Level Curve

After you have the implicit equation $`g(x,y)=0`$, classify it:

| Standard Form (after rearranging)        | Shape in $`xy`$-plane                                |
| ---------------------------------------- | -------------------------------------------------- |
| $`Ax+By=C`$                                | Line                                               |
| $`x^2+y^2=r^2`$                            | Circle                                             |
| $`\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}=1`$    | Ellipse                                            |
| $`xy = k`$                                 | Rectangular hyperbola                              |
| $`y = k x^n`$ (with $`n>0`$)                 | Power curve (parabola for $`n=2`$, cubic, …)         |
| $`y = \sin^{-1}(k)`$ or $`x = \cos^{-1}(k)`$ | Horizontal or vertical strip (from trig functions) |


> **Example**
> For $f(x,y)=x^2+4y^2$, setting $f=16$ gives
>
> $$
> \frac{x^2}{16} + \frac{y^2}{4}=1,
> $$
>
> an **ellipse** with semi-axes $4$ (in $x$) and $2$ (in $y$).

---

## 3 · Sketching Level Curves

1. **Pick several convenient $c$-values** (e.g., an arithmetic sequence).
2. **Solve $`f(x,y)=c`$** for each.
3. **Plot the curves** on a single set of axes.
4. **Label or shade** to indicate increasing or decreasing $f$.


### Quick Sketch Example

For $`f(x,y)=x\,e^{-y}`$:

| $c$        | Level-curve equation                  | Notes                    |
| ---------- | ------------------------------------- | ------------------------ |
| $1$        | $`x\,e^{-y}=1 \;\Rightarrow\; y=\ln x`$ | Right-branch logarithm   |
| $2$        | $`y = \ln(x/2)`$                        | Same shape, shifted down |
| $`\tfrac12`$ | $`y=\ln(2x)`$                           | Shifted up               |

All curves are **logarithmic**, stacked vertically.

---

### Practical Tips

* **Symmetry** in $`f`$ often means symmetry in level curves—exploit it.


* If $`f`$ is **independent of one variable** (e.g.\ $`f(x,y)=g(y)`$), then each contour is a horizontal line.


* Use **sign analysis**: where can $`f(x,y)=c`$ even be satisfied? (E.g.\ $`x^2+y^2=c<0`$ → no real curve.)

---

## ✏️ Check-List for Any Level-Curve Problem

1. **Set** $`f(x,y)=c`$.


2. **Rearrange** into a recognizable conic or other form.


3. **State** domain restrictions (if any).


4. **Classify** (line, ellipse, hyperbola, etc.).


5. **Draw** several curves, label axes, mark intercepts.

With these steps you can tackle virtually any level-curve question—whether for hand sketches, computer plots, 
or deeper analysis (e.g.\ gradient directions and critical points).
