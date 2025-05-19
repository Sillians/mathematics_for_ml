## **Properties of Variance for Discrete Random Variables**

**Variance** measures how much a random variable deviates from its mean. For discrete random variables, variance has several key properties that allow us to compute or simplify it when constants or transformations are involved.

---

### 🔹 **1. Variance of a Discrete Random Variable**

Let $X$ be a discrete random variable with probability mass function $`P(X = x_i) = p_i`$. Then:

$$
\text{Var}(X) = \mathbb{E}[(X - \mu)^2] = \sum (x_i - \mu)^2 p_i
$$

Or, using the shortcut formula:

$$
\text{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2
$$

Where:

* $`\mathbb{E}[X] = \mu`$
* $`\mathbb{E}[X^2] = \sum x_i^2 p_i`$

---

### 🔹 **2. Computing the Variance of a Constant**

If $`c`$ is a constant (i.e., a random variable that always takes the same value), then:

$$
\text{Var}(c) = 0
$$

#### ✅ Example:

Let $`Y = 5`$, then:

$$
\text{Var}(Y) = 0
$$

Because there's no variability — the value never changes.

---

### 🔹 **3. Computing the Variance of a Scaled Random Variable**

If $`Y = aX`$, where $a$ is a constant, then:

$$
\text{Var}(aX) = a^2 \cdot \text{Var}(X)
$$

Scaling a variable **scales the variance by the square of the constant**.

#### ✅ Example:

If $`\text{Var}(X) = 4`$ and $`Y = 3X`$, then:

$$
\text{Var}(Y) = 3^2 \cdot 4 = 9 \cdot 4 = \boxed{36}
$$

---

### 🔹 **4. Computing the Variance of a Transformed Random Variable**

If $`Y = aX + b`$, where $a$ and $b$ are constants:

$$
\text{Var}(aX + b) = a^2 \cdot \text{Var}(X)
$$

The **constant shift $b$** does **not** affect the variance — only the **scaling $a$** does.

#### ✅ Example:

Let $X$ have $`\text{Var}(X) = 5`$, and let $`Y = -2X + 7`$, then:

$$
\text{Var}(Y) = (-2)^2 \cdot 5 = 4 \cdot 5 = \boxed{20}
$$

---

### 🔹 **5. Additional Properties of Variance**

* **Variance is always non-negative**:

$$
\text{Var}(X) \geq 0
$$

* **If $X$ and $Y$ are independent**:

$$
\text{Var}(X \pm Y) = \text{Var}(X) + \text{Var}(Y)
$$

* **For any constant $c$**:

$$
\text{Var}(X + c) = \text{Var}(X)
$$

---

### ✅ Summary Table

| Transformation                      | Variance Rule                   |
| ----------------------------------- | ------------------------------- |
| $`\text{Var}(c)`$                     | $0$                             |
| $`\text{Var}(aX)`$                    | $`a^2 \cdot \text{Var}(X)`$       |
| $`\text{Var}(aX + b)`$                | $`a^2 \cdot \text{Var}(X)`$       |
| $`\text{Var}(X + Y)`$, if independent | $`\text{Var}(X) + \text{Var}(Y)`$ |

---

### **Conclusion**

Understanding the properties of variance helps simplify calculations and predict how transformations 
(like scaling or shifting) affect data variability. These principles are widely used in probability, 
statistics, data analysis, and machine learning to quantify and control uncertainty.
