## **Independence of Discrete Random Variables**

---

### **1. What Does Independence Mean?**

Two discrete random variables $X$ and $Y$ are **independent** if knowing the value of one does **not affect** the probability distribution of the other.

**Formally**, $X$ and $Y$ are independent if for **all** values of $x$ and $y$:

$$
P(X = x, Y = y) = P(X = x) \cdot P(Y = y)
$$

This condition must hold for **every pair** $`(x, y)`$ in their joint support.

---

### **2. Determining Whether Two Random Variables Are Independent**

#### **Steps:**

1. **Compute the marginal distributions**:

* $`P(X = x) = \sum_y P(X = x, Y = y)`$
* $`P(Y = y) = \sum_x P(X = x, Y = y)`$

2. **Check the independence condition** for every value of $`(x, y)`$:

$$
P(X = x, Y = y) \stackrel{?}{=} P(X = x) \cdot P(Y = y)
$$

If the equality fails **for any pair**, the variables are **not independent**.

---

### **3. Determining Whether Two Random Variables Are Independent Given the Joint PMF Only**

Given a **joint PMF table**, do the following:

* Compute **marginal probabilities** by summing rows and columns.
* For each cell $`(x, y)`$, check whether:

$$
f(x, y) = f_X(x) \cdot f_Y(y)
$$

If the condition is true for all entries, then $`X`$ and $`Y`$ are independent.

**Example:**

|         | $`Y = 0`$ | $`Y = 1`$ |
| ------- | ------- | ------- |
| $`X = 0`$ | 0.2     | 0.3     |
| $`X = 1`$ | 0.1     | 0.4     |

Check:

* $`P(X = 0) = 0.2 + 0.3 = 0.5`$
* $`P(Y = 0) = 0.2 + 0.1 = 0.3`$
  Then:
* $`P(X = 0, Y = 0) = 0.2`$
* $`P(X = 0) \cdot P(Y = 0) = 0.5 \cdot 0.3 = 0.15 \neq 0.2`$
  ❌ Not independent.

---

### **4. Calculating Joint Probabilities**

The **joint probability** of two events occurring simultaneously is either:

* Given directly from the joint PMF table:
  $`P(X = x, Y = y)`$

Or if independent:

* $`P(X = x, Y = y) = P(X = x) \cdot P(Y = y)`$

This is used when **independence is known or assumed**.

---

### ✅ **Summary Table**

| **Concept**                        | **Action**                                                         |
| ---------------------------------- | ------------------------------------------------------------------ |
| Independence                       | $`P(X = x, Y = y) = P(X = x) \cdot P(Y = y)`$ for all $`x, y`$         |
| From Joint PMF                     | Sum across rows/columns to get marginals, then verify independence |
| Joint Probability (general)        | Use joint table: $`f(x, y)`$                                         |
| Joint Probability (if independent) | Multiply marginals: $`f_X(x) \cdot f_Y(y)`$                          |

Independence is a **strong condition** and must be validated across all values, not just a few.
