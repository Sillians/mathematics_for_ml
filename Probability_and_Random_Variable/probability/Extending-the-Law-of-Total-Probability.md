## **Extending the Law of Total Probability**

---

### **1. What Is the Law of Total Probability?**

The **Law of Total Probability** allows you to compute the probability of an event by breaking it down over a **partition** of the sample space. 
It's especially useful when calculating probabilities through **intermediate or conditional scenarios**.

### **Formal Definition:**

Let $`B_1, B_2, ..., B_n`$ be a **partition** of the sample space $`S`$ (i.e., disjoint events with $`\bigcup B_i = S`$ and $`P(B_i) > 0`$), then for any event $A$:

$$
P(A) = \sum_{i=1}^{n} P(A \mid B_i) \cdot P(B_i)
$$

This lets us find $`P(A)`$ by considering **all the different ways** $A$ can happen through different $B_i$'s.

---

### **2. Applying the Law of Total Probability**

**Example:**

Suppose:

* A factory has 3 machines:
  $`M_1`$, $`M_2`$, $`M_3`$
* Machine usage: $`P(M_1) = 0.3`$, $`P(M_2) = 0.5`$, $`P(M_3) = 0.2`$
* Defect probabilities:
  $`P(D \mid M_1) = 0.01`$, $`P(D \mid M_2) = 0.02`$, $`P(D \mid M_3) = 0.03`$

**Find the total probability that a product is defective:**

$$
P(D) = P(D \mid M_1)P(M_1) + P(D \mid M_2)P(M_2) + P(D \mid M_3)P(M_3)
$$

$$
P(D) = (0.01)(0.3) + (0.02)(0.5) + (0.03)(0.2) = 0.003 + 0.01 + 0.006 = 0.019
$$

---

### **3. Applying the Law in Terms of Conditional Probability**

The law also expresses the total probability of $A$ **given another event $C$**:

$$
P(A \mid C) = \sum_{i=1}^{n} P(A \mid B_i \cap C) \cdot P(B_i \mid C)
$$

This is useful when conditioning on additional known information (context or observed data).

---

### **4. Finding a Conditional Probability Using the Law of Total Probability**

Sometimes, you want to find a conditional probability such as $`P(B_k \mid A)`$. This is where **Bayes' Theorem** comes in, **after** using the Law of Total Probability to compute $`P(A)`$.

**Bayes' Theorem with Total Probability**:

$$
P(B_k \mid A) = \frac{P(A \mid B_k) \cdot P(B_k)}{\sum_{i=1}^{n} P(A \mid B_i) \cdot P(B_i)}
$$

**Example continuation:**

Find the probability that a defective item came from machine $`M_2`$:

$$
P(M_2 \mid D) = \frac{P(D \mid M_2) \cdot P(M_2)}{P(D)} = \frac{0.02 \cdot 0.5}{0.019} \approx 0.526
$$

---

### ✅ **Summary**

| Concept                  | Description                                           |
| ------------------------ | ----------------------------------------------------- |
| Law of Total Probability | Breaks $`P(A)`$ into weighted sum over partitions $`B_i`$ |
| Conditional version      | Adjusts for another known event $`C`$                   |
| Used in Bayes' Theorem   | Provides denominator (normalizing constant)           |

This principle is critical in modeling **complex, multi-stage** probability problems, and forms the foundation for **Bayesian inference**, 
**decision theory**, and **machine learning classification**.
