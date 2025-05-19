## **The Rule of the Lazy Statistician**

The **Rule of the Lazy Statistician** is a clever, time-saving principle in probability and statistics that lets you **bypass 
computing the full distribution of a random variable** to directly compute its **expected value**.

---

### **What Is the Rule of the Lazy Statistician?**

If a random variable $Y$ is defined as a **function of another random variable** $X$, i.e.,

$$
Y = g(X)
$$

then the expected value of $Y$ is given by:

* **Discrete case**:

$$
\mathbb{E}[Y] = \mathbb{E}[g(X)] = \sum_{x} g(x) \cdot P(X = x)
$$

* **Continuous case**:

$$
\mathbb{E}[Y] = \mathbb{E}[g(X)] = \int_{-\infty}^{\infty} g(x) \cdot f(x) \, dx
$$

Where:

* $`f(x)`$ is the **PDF** of $`X`$ in the continuous case
* $`P(X = x)`$ is the **PMF** of $`X`$ in the discrete case

This avoids the need to find the full **distribution of $Y$**.

---

##  **1. Applying the Rule for Discrete Random Variables**

Let’s say $`X`$ is a discrete random variable with a known PMF, and we define a transformation $`Y = g(X)`$. To compute $`\mathbb{E}[Y]`$, we simply evaluate:

$$
\mathbb{E}[g(X)] = \sum_{x} g(x) \cdot P(X = x)
$$

---

### **Example:**

Let $`X \in \{1, 2, 3\}`$ with $`P(X = x) = \frac{1}{3}`$, and let $`Y = X^2`$

Then:

$$
\mathbb{E}[Y] = \sum_{x} x^2 \cdot \frac{1}{3}
= \frac{1^2 + 2^2 + 3^2}{3} = \frac{1 + 4 + 9}{3} = \boxed{4.67}
$$

---

## **2. Applying the Rule for Continuous Random Variables**

If $X$ is a continuous random variable with PDF $`f(x)`$, and $`Y = g(X)`$, then:

$$
\mathbb{E}[g(X)] = \int_{-\infty}^{\infty} g(x) \cdot f(x) \, dx
$$

---

### **Example:**

Let $`X \sim \text{Uniform}(0, 2)`$, so $`f(x) = \frac{1}{2}`$ for $`x \in [0, 2]`$, and define $`Y = X^2`$

Then:

$$
\mathbb{E}[Y] = \int_0^2 x^2 \cdot \frac{1}{2} \, dx = \frac{1}{2} \int_0^2 x^2 \, dx = \frac{1}{2} \cdot \left[ \frac{x^3}{3} \right]_0^2 = \frac{1}{2} \cdot \frac{8}{3} = \boxed{\frac{4}{3}}
$$

---

### ✅ **Summary Table**

| Case       | Expected Value via Lazy Statistician           |
| ---------- | ---------------------------------------------- |
| Discrete   | $`\mathbb{E}[g(X)] = \sum g(x) \cdot P(X = x)`$  |
| Continuous | $`\mathbb{E}[g(X)] = \int g(x) \cdot f(x)\, dx`$ |

---

### **Why It’s Called “Lazy”**

It avoids:

* Computing the **distribution** of $`Y`$
* Re-deriving the **PMF or PDF** for a transformed variable

Instead, it uses the **known distribution of $X$** and the **transformation function $g$** to go straight to the expected value.

---

### **Conclusion**

The **Rule of the Lazy Statistician** is a practical shortcut for computing expected values of transformed variables — whether discrete 
or continuous — without doing unnecessary algebra. It's a vital tool for simplifying expectation calculations in both theoretical and applied statistics.
