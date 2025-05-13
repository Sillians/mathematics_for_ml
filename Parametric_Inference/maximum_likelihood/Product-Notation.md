## **Product Notation (Π Notation)**

**Product notation**, denoted by the Greek letter **Π** (capital pi), is used to represent 
the **product of a sequence of terms**, just as summation (Σ) represents a sum.

---

### **1. What Is Product Notation?**

The general form is:

$$
\prod_{i = m}^{n} a_i = a_m \cdot a_{m+1} \cdot a_{m+2} \cdots a_n
$$

* $`i`$: index of multiplication
* $`m`$: lower bound
* $`n`$: upper bound
* $`a_i`$: general term of the product

---

### **2. Evaluating a Product**

To evaluate a product, multiply all terms from the lower bound to the upper bound.

#### **Example:**

$$
\prod_{k=1}^{4} k = 1 \cdot 2 \cdot 3 \cdot 4 = 24
$$

This is equivalent to $`4! = 24`$

---

### **3. Writing a Product Using Product Notation**

You can write a multiplication pattern compactly using Π notation.

#### **Example:**

The product $`2 \cdot 4 \cdot 6 \cdot 8`$ can be written as:

$$
\prod_{k=1}^{4} 2k
$$

Here, the general term $`2k`$ generates even numbers.

---

### **4. Simplifying a Product**

Sometimes you can simplify a product using algebraic rules, factorials, or cancelation.

#### **Example (Factorial form):**

$$
\prod_{k=1}^{n} k = n!
$$

#### **Example (Telescoping Product):**

$$
\prod_{k=2}^{4} \frac{k}{k-1} = \frac{2}{1} \cdot \frac{3}{2} \cdot \frac{4}{3} = 4
$$

Many terms cancel out, leaving just the first numerator and the last denominator.

---

### ✅ **Summary Table**

| Task                       | Example                                              |
| -------------------------- | ---------------------------------------------------- |
| **Evaluating**             | $\prod_{i=1}^{3} i^2 = 1^2 \cdot 2^2 \cdot 3^2 = 36$ |
| **Writing using notation** | $3 \cdot 6 \cdot 9$ → $\prod_{k=1}^{3} 3k$           |
| **Simplifying**            | $\prod_{k=2}^{n} \frac{k}{k-1} = n$                  |

---

### **Conclusion**

Product notation provides a compact and powerful way to represent multiplication over sequences, making it essential for algebra, calculus, and combinatorics. Mastery of Π notation is key for working with factorials, limits, and infinite products in advanced mathematics.
