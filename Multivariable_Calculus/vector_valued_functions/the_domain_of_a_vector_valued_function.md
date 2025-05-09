## **The Domain of a Vector-Valued Function**

A **vector-valued function** maps real numbers to vectors. For example, in $\mathbb{R}^3$:

$$
\mathbf{r}(t) = \begin{bmatrix} f(t) \\ g(t) \\ h(t) \end{bmatrix}
$$

The **domain** of $\mathbf{r}(t)$ is the set of all real numbers $t$ for which **all component functions** $f(t), g(t), h(t)$ are defined.

To determine the domain, analyze the components **individually**, then take the **intersection** of their domains.

---

### **1. Domains With Reciprocal and Radical Components**

#### **Reciprocals (e.g., $\frac{1}{t - a}$)**

* Undefined when the denominator is 0.
* **Exclude** any value where the denominator vanishes.

**Example:**

$$
\mathbf{r}(t) = \begin{bmatrix}
\frac{1}{t-2} \\
t^2 \\
\sqrt{t+1}
\end{bmatrix}
$$

* $\frac{1}{t-2}$: undefined at $t = 2$
* $t^2$: defined for all $t$
* $\sqrt{t+1}$: defined when $t + 1 \geq 0 \Rightarrow t \geq -1$

**Domain:**

$$
\boxed{[-1, 2) \cup (2, \infty)}
$$

---

### **2. Domains With Exponential and Logarithmic Components**

#### **Exponential Functions (e.g., $e^t, 2^t$)**

* **Defined for all real numbers.**

#### **Logarithmic Functions (e.g., $\ln(t), \log_b(t)$)**

* Defined only when the **argument is positive**: $t > 0$

**Example:**

$$
\mathbf{r}(t) = \begin{bmatrix}
\ln(t - 1) \\
e^t \\
\log(t^2 - 4)
\end{bmatrix}
$$

* $\ln(t - 1)$: $t > 1$
* $e^t$: all $t$
* $\log(t^2 - 4)$: $t^2 - 4 > 0 \Rightarrow t < -2$ or $t > 2$

**Domain:**

$$
\boxed{(2, \infty)}
$$

(Intersection of $t > 1$ and $t > 2$)

---

### **3. Domains With Trigonometric Components**

#### **Sine and Cosine ($\sin t, \cos t$)**

* Defined for **all real numbers**

#### **Tangent and Secant**

* Undefined where cosine is zero:

  * $\tan t, \sec t$: undefined at $t = \frac{\pi}{2} + n\pi$

#### **Cotangent and Cosecant**

* Undefined where sine is zero:

  * $\cot t, \csc t$: undefined at $t = n\pi$

**Example:**

$$
\mathbf{r}(t) = \begin{bmatrix}
\sin t \\
\cot t \\
\ln(\cos t)
\end{bmatrix}
$$

* $\sin t$: all $t$
* $\cot t$: undefined at $t = n\pi$
* $\ln(\cos t)$: only defined when $\cos t > 0$

**Domain:**

* Find intervals where $\cos t > 0$ and $t \ne n\pi$

On $(0, \frac{\pi}{2})$, $\cos t > 0$ and $\cot t$ is defined.

So, one possible valid domain interval:

$$
\boxed{(0, \frac{\pi}{2})}
$$

(Other valid intervals can be found periodically.)

---

### **4. Summary**

To find the **domain of a vector-valued function**:

* Analyze each component:

  * **Rational**: exclude values that make the denominator zero.
  * **Radical**: ensure expression under root is ≥ 0 (for even roots).
  * **Logarithmic**: argument must be > 0.
  * **Trigonometric**: check where functions are undefined.
* **Intersect** the valid domains of all components.

Mastering domain analysis is essential for ensuring vector-valued functions are well-defined and for understanding their behavior across intervals.
