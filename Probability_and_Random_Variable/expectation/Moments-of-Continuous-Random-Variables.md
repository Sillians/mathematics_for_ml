## **Moments of Continuous Random Variables**

**Moments** of a random variable give a detailed description of the shape and distribution of a probability distribution. 
For **continuous random variables**, moments are calculated using integrals involving the probability density function (PDF).

---

###  **1. Definition of Moments**

For a continuous random variable $X$ with probability density function $`f(x)`$, the **$n$th moment about the origin** is:

$$
\mu'_n = \mathbb{E}[X^n] = \int_{-\infty}^{\infty} x^n f(x)\,dx
$$

The **mean** (or first moment) is:

$$
\mu = \mathbb{E}[X] = \int_{-\infty}^{\infty} x f(x)\,dx
$$

---

### **2. Calculating the Second Moment of a Random Variable**

The **second moment** about the origin is:

$$
\mathbb{E}[X^2] = \int_{-\infty}^{\infty} x^2 f(x)\,dx
$$

This is used to compute **variance**:

$$
\mathrm{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2
$$

#### ✅ Example:

If $`f(x) = 2x`$ on $`[0,1]`$, then:

$$
\mathbb{E}[X^2] = \int_0^1 x^2 \cdot 2x\, dx = \int_0^1 2x^3\, dx = \left[\frac{2x^4}{4}\right]_0^1 = \frac{1}{2}
$$

---

### **3. Calculating a Higher Moment of a Random Variable**

To compute the **$n$th moment**:

$$
\mathbb{E}[X^n] = \int_{-\infty}^{\infty} x^n f(x)\, dx
$$

#### ✅ Example:

For the same $f(x) = 2x$ on $[0,1]$, the 4th moment:

$$
\mathbb{E}[X^4] = \int_0^1 x^4 \cdot 2x\, dx = \int_0^1 2x^5\, dx = \left[\frac{2x^6}{6}\right]_0^1 = \frac{1}{3}
$$

---

### **4. Computing the Mean of a Transformed Random Variable**

Let $`Y = g(X)`$. Then:

$$
\mathbb{E}[Y] = \mathbb{E}[g(X)] = \int_{-\infty}^{\infty} g(x) f(x)\,dx
$$

This is especially useful when analyzing functions of random variables such as $`X^2`$, $`\ln X`$, or $`e^X`$.

#### ✅ Example:

Let $`f(x) = e^{-x}`$ for $`x \geq 0`$. Then:

$$
\mathbb{E}[e^x] = \int_0^\infty e^x \cdot e^{-x} dx = \int_0^\infty 1\, dx \rightarrow \infty
$$

So $`\mathbb{E}[e^X]`$ is not defined (diverges).

---

### ✅ **Summary Table**

| Moment Type                    | Formula                                |
| ------------------------------ | -------------------------------------- |
| First Moment (Mean)            | $`\mathbb{E}[X] = \int x f(x)\,dx`$      |
| Second Moment                  | $`\mathbb{E}[X^2] = \int x^2 f(x)\,dx`$  |
| $n$th Moment                   | $`\mathbb{E}[X^n] = \int x^n f(x)\,dx`$  |
| Mean of a Transformed Variable | $`\mathbb{E}[g(X)] = \int g(x)f(x)\,dx`$ |

---

### **Conclusion**

Moments help describe the **center**, **spread**, and **shape** of a continuous distribution. 
Calculating them through integration allows for a deeper understanding and modeling of random behavior,
especially when working with transformations or analyzing variance and higher-order behaviors.
