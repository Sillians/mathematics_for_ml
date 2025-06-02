## **The Joint CDF of Two Discrete Random Variables**

---

#### **Definition**

Given two discrete random variables $X$ and $Y$, the **joint cumulative distribution function (CDF)** is defined as:

$$
F(x, y) = P(X \leq x, Y \leq y)
$$

This function gives the **cumulative probability** that $X$ is less than or equal to $x$, and simultaneously, $Y$ is less than or equal to $y$.

---

### **1. Evaluating a Joint CDF**

To evaluate the joint CDF at a point $`(x, y)`$, sum all the probabilities of outcomes where:

$$
x' \leq x \quad \text{and} \quad y' \leq y
$$

That is:

$$
F(x, y) = \sum_{x' \leq x} \sum_{y' \leq y} P(X = x', Y = y')
$$

##### **Example:**

If the joint PMF is known and given as a table:

| $`Y \backslash X`$ | 0   | 1    |
| ---------------- | --- | ---- |
| 1                | 0.1 | 0.15 |
| 2                | 0.2 | 0.05 |

Then:

$$
F(1,2) = P(X \leq 1, Y \leq 2) = 0.1 + 0.15 + 0.2 + 0.05 = 0.5
$$

---

### **2. Interpreting the Joint CDF Geometrically**

* Think of the joint CDF as a **surface** over the $`(x, y)`$-plane.
* At any point $`(x, y)`$, the height of the surface is the cumulative probability up to that point.
* It forms a **stepwise function** because both variables are discrete.
* The function is **non-decreasing** in both $`x`$ and $`y`$.

---

### **3. Finding Cumulative Probabilities Given Values From the Joint CDF**

To find a probability like:

$$
P(a < X \leq b, c < Y \leq d)
$$

Use the **inclusion-exclusion principle**:

$$
P(a < X \leq b, c < Y \leq d) = F(b, d) - F(a, d) - F(b, c) + F(a, c)
$$

This subtracts off unwanted rectangular cumulative areas and adds back the overlap.

---

### **4. Further Finding Cumulative Probabilities Given Values From the Joint CDF**

#### **Marginal Probabilities**

From the joint CDF, compute marginal CDFs:

* For $`X`$:

$$
F_X(x) = \lim_{y \to \infty} F(x, y)
$$

* For $Y$:

$$
F_Y(y) = \lim_{x \to \infty} F(x, y)
$$

If $`X \in \{0, 1\}`$, $`Y \in \{1,2,3,4,5,6\}`$, then:

$$
F_X(1) = F(1,6), \quad F_Y(6) = F(1,6)
$$

#### **Joint PMF Recovery**

You can recover joint PMF entries using finite differences:

$$
P(X = x, Y = y) = F(x, y) - F(x-1, y) - F(x, y-1) + F(x-1, y-1)
$$

---

### **Key Properties**

* $`F(x, y)`$ is **right-continuous**.
* $`\lim_{x \to \infty, y \to \infty} F(x, y) = 1`$
* $`\lim_{x \to -\infty \text{ or } y \to -\infty} F(x, y) = 0`$
* Non-decreasing in both $x$ and $y$

---

This framework is essential for analyzing joint distributions, dependence, and computing probabilities over multi-dimensional discrete spaces.
