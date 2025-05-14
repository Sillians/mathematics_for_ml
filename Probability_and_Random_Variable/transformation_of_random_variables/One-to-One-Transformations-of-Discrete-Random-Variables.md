## **One-to-One Transformations of Discrete Random Variables**

A **one-to-one transformation** (or injective transformation) of a **discrete random variable** 
maps each outcome of the original variable to a **unique** value in the transformed space. 
This means **no two values in the original sample space map to the same value** in the 
transformed variable.

---

### **1. Understanding One-to-One Transformations**

Let $`X`$ be a discrete random variable, and let $`Y = g(X)`$ be a transformation of $`X`$, 
where $g$ is a **one-to-one function**.

* If $`g`$ is **injective**, then each value of $`Y`$ corresponds to exactly one value of $`X`$, and vice versa.
* The distribution of $`Y`$ can be derived directly from the distribution of $`X`$.

---

### **2. Finding the Distribution of a Transformed Random Variable**

To find the **probability distribution of $`Y = g(X)`$**:

1. List the possible values of $`X`$ and their probabilities.
2. Apply the function $`g`$ to each value of $`X`$ to obtain values of $`Y`$.
3. Assign the **same probabilities** from $`X`$ to the corresponding values of $`Y`$.

#### **Example:**

Let $`X`$ be a discrete random variable with the distribution:

$$
\begin{aligned}
P(X = 1) &= 0.2 \\
P(X = 2) &= 0.5 \\
P(X = 3) &= 0.3 \\
\end{aligned}
$$

Let $`Y = g(X) = 2X + 1`$. Then:

$$
\begin{aligned}
X = 1 &\Rightarrow Y = 3,\quad P(Y = 3) = 0.2 \\
X = 2 &\Rightarrow Y = 5,\quad P(Y = 5) = 0.5 \\
X = 3 &\Rightarrow Y = 7,\quad P(Y = 7) = 0.3 \\
\end{aligned}
$$

So, the distribution of $`Y`$ is:

$$
\boxed{
\begin{aligned}
P(Y = 3) &= 0.2 \\
P(Y = 5) &= 0.5 \\
P(Y = 7) &= 0.3 \\
\end{aligned}
}
$$

---

### **3. Calculating a Probability Involving a Transformed Random Variable**

To compute $`P(Y \in A)`$, for any event $`A \subseteq \text{Range}(Y)`$:

1. Identify the values of $`X`$ such that $`g(X) \in A`$
2. Use the original PMF of $`X`$ to compute $`P(X \in g^{-1}(A))`$

#### **Example:**

Using the transformation $`Y = 2X + 1`$, and original $`P(X)`$ as above, compute:

$$
P(Y \geq 5)
$$

Then:

$$
Y \geq 5 \Rightarrow X \geq 2
\Rightarrow P(X = 2) + P(X = 3) = 0.5 + 0.3 = \boxed{0.8}
$$

Alternatively, using $`Y`$'s PMF:

$$
P(Y \geq 5) = P(Y = 5) + P(Y = 7) = 0.5 + 0.3 = \boxed{0.8}
$$

---

### ✅ **Summary Table**

| Task                        | Method                                           |
| --------------------------- | ------------------------------------------------ |
| **Transform a discrete RV** | Apply one-to-one function $`Y = g(X)`$             |
| **Get PMF of $Y$**          | Map $X$'s values through $`g`$, keep probabilities |
| **Find $P(Y \in A)$**       | Use $`P(X \in g^{-1}(A))`$ or use new PMF of $`Y`$   |

---

### **Conclusion**

One-to-one transformations of discrete random variables **preserve probability structure** 
while changing the variable's values. This allows for **straightforward derivation of new distributions**, 
especially when computing probabilities involving derived or reparameterized 
quantities in probability, statistics, and information theory.
