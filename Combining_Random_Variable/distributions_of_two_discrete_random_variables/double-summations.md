## **Double Summations**

Double summations are used to compute the sum of terms arranged in a **two-dimensional grid**, 
such as matrices or indexed sequences in calculus, statistics, and linear algebra. 
They extend the idea of a single summation to two indices.

---

### **1. Notation of a Double Summation**

A **double summation** is written as:

$$
\sum_{i=m}^{n} \sum_{j=p}^{q} a_{ij}
$$

* The **inner sum** (over $j$) is evaluated **first** for a fixed $i$.
* The **outer sum** (over $i$) sums over the results of the inner sum.

---

### **2. Computing a Double Summation**

**Example:**

$$
\sum_{i=1}^{2} \sum_{j=1}^{3} (i + j)
$$

**Step 1: Inner sum (for each $i$)**

* For $i = 1$:

  $$
  \sum_{j=1}^{3} (1 + j) = 1+1 + 1+2 + 1+3 = 2 + 3 + 4 = 9
  $$

* For $i = 2$:

  $$
  \sum_{j=1}^{3} (2 + j) = 2+1 + 2+2 + 2+3 = 3 + 4 + 5 = 12
  $$

**Step 2: Add outer results:**

$$
9 + 12 = \boxed{21}
$$

---

### **3. Applying the Sum and Constant Multiple Rules**

#### **Sum Rule:**

$$
\sum_i \sum_j (a_{ij} + b_{ij}) = \sum_i \sum_j a_{ij} + \sum_i \sum_j b_{ij}
$$

#### **Constant Multiple Rule:**

$$
\sum_i \sum_j c \cdot a_{ij} = c \cdot \sum_i \sum_j a_{ij}
$$

**Example:**

$$
\sum_{i=1}^2 \sum_{j=1}^2 3(i + j) = 3 \cdot \sum_{i=1}^2 \sum_{j=1}^2 (i + j)
$$

---

### **4. Applying the Product Rule and Swap Rules**

#### **Product Rule (for separable expressions):**

If the summand can be separated as a product:

$$
\sum_i \sum_j f(i)g(j) = \left( \sum_i f(i) \right) \left( \sum_j g(j) \right)
$$

**Example:**

$$
\sum_{i=1}^2 \sum_{j=1}^3 i \cdot j = \left( \sum_{i=1}^2 i \right) \cdot \left( \sum_{j=1}^3 j \right) = (1 + 2)(1 + 2 + 3) = 3 \cdot 6 = \boxed{18}
$$

---

#### **Swap Rule (Fubini's Theorem for finite sums):**

$$
\sum_{i=m}^{n} \sum_{j=p}^{q} a_{ij} = \sum_{j=p}^{q} \sum_{i=m}^{n} a_{ij}
$$

Swapping the order of summation is valid as long as the limits are **independent**.

---

### **Summary Table**

| Concept                | Rule / Formula                                           |
| ---------------------- | -------------------------------------------------------- |
| **Compute double sum** | Inner sum first, then outer                              |
| **Sum Rule**           | $\sum (a + b) = \sum a + \sum b$                         |
| **Constant Rule**      | $\sum c \cdot a = c \cdot \sum a$                        |
| **Product Rule**       | $\sum_i \sum_j f(i)g(j) = \sum_i f(i) \cdot \sum_j g(j)$ |
| **Swap Rule**          | $\sum_i \sum_j a_{ij} = \sum_j \sum_i a_{ij}$            |

---

Mastering double summations helps with **evaluating series**, **summarizing grids or tables**, 
and simplifying expressions in multivariable calculus, probability, and matrix operations.
