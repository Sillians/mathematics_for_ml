## **Many-to-One Transformations of Discrete Random Variables**

A **many-to-one transformation** of a discrete random variable maps **multiple input values** to 
the **same output**. This often occurs with **non-injective functions** like squaring, absolute value,
or rounding, where different original values result in the **same transformed value**.

When a transformation is **many-to-one**, the probabilities of input values must be **added** 
when they produce the same output value.

---

### **1. Finding Distributions of Squared Random Variables: One-to-One Transformations**

If $X$ is a **non-negative** discrete random variable and the transformation $`Y = X^2`$ is **one-to-one** over its support, then:

$$
P(Y = y) = P(X = \sqrt{y}) \quad \text{if } \sqrt{y} \in \text{Support}(X)
$$

#### **Example:**

Let $`X \in \{1, 2, 3\}`$ with:

$$
P(X = 1) = 0.2,\quad P(X = 2) = 0.3,\quad P(X = 3) = 0.5
$$

Then $`Y = X^2 \in \{1, 4, 9\}`$, and the distribution of $`Y`$ is:

$$
\begin{aligned}
P(Y = 1) &= P(X = 1) = 0.2 \\
P(Y = 4) &= P(X = 2) = 0.3 \\
P(Y = 9) &= P(X = 3) = 0.5 \\
\end{aligned}
$$

Since $`X \geq 0`$, squaring is one-to-one here.

---

### **2. Finding Distributions of Squared Random Variables: Many-to-One Transformations**

If $X$ includes both positive and negative values, then $`Y = X^2`$ is **many-to-one** because both $x$ and $-x$ map to the same $y$. 
To find $`P(Y = y)`$, **add probabilities of all values of $X$** that satisfy $`x^2 = y`$.

$$
P(Y = y) = \sum_{x: x^2 = y} P(X = x)
$$

#### **Example:**

Let $`X \in \{-2, -1, 0, 1, 2\}`$ with:

$$
P(X = -2) = 0.1,\quad P(X = -1) = 0.2,\quad P(X = 0) = 0.4,\quad P(X = 1) = 0.2,\quad P(X = 2) = 0.1
$$

Then $`Y = X^2 \in \{0, 1, 4\}`$:

$$
\begin{aligned}
P(Y = 0) &= P(X = 0) = 0.4 \\
P(Y = 1) &= P(X = -1) + P(X = 1) = 0.2 + 0.2 = 0.4 \\
P(Y = 4) &= P(X = -2) + P(X = 2) = 0.1 + 0.1 = 0.2 \\
\end{aligned}
$$

So the distribution of $`Y`$ is:

$$
\boxed{
\begin{aligned}
P(Y = 0) &= 0.4 \\
P(Y = 1) &= 0.4 \\
P(Y = 4) &= 0.2 \\
\end{aligned}
}
$$

---

### **3. Calculating a Probability Involving a Squared Random Variable**

To compute $`P(Y \in A)`$, where $`Y = X^2`$, identify all $`x \in \text{Support}(X)`$ such 
that $`x^2 \in A`$, then sum:

$$
P(Y \in A) = \sum_{x: x^2 \in A} P(X = x)
$$

#### **Example:**

Using the same $X$ above, find $`P(Y \geq 1)`$:

* $`Y = 1`$ from $`X = \pm1`$
* $`Y = 4`$ from $`X = \pm2`$

$$
P(Y \geq 1) = P(X = -2) + P(X = -1) + P(X = 1) + P(X = 2)
= 0.1 + 0.2 + 0.2 + 0.1 = \boxed{0.6}
$$

---

### ✅ **Summary Table**

| Task                            | Method                                                               |
| ------------------------------- | -------------------------------------------------------------------- |
| **One-to-one transformations**  | Directly map and assign $`P(Y = y) = P(X = x)`$                        |
| **Many-to-one transformations** | Sum all $`P(X = x)`$ such that $`x^2 = y`$                               |
| **Probability of event in $`Y`$** | Identify all $`x`$ such that $`x^2 \in A`$, then sum their probabilities |

---

### **Conclusion**

Many-to-one transformations, such as squaring, require **grouping multiple input values** 
that result in the **same output**. Accurately transforming and summing probabilities is 
key to understanding how functions of discrete random variables behave—especially in probability 
modeling, random processes, and statistical computation.
