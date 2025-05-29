## **Extending Bayes' Theorem**

---

### **1. Computing a Conditional Probability Using Bayes’ Theorem**

Bayes' Theorem provides a way to **reverse conditional probabilities**:

$$
P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}
$$

Where:

* $`P(A|B)`$ is the **posterior** probability,
* $`P(B|A)`$ is the **likelihood**,
* $`P(A)`$ is the **prior** probability,
* $`P(B)`$ is the **total probability** of $B$, often expanded using the Law of Total Probability.

#### **Example:**

Given:

* $`P(D) = 0.01`$ (probability of disease),
* $`P(+|D) = 0.99`$ (true positive),
* $`P(+|\neg D) = 0.05`$ (false positive)

To compute: $`P(D|+)`$:

$$
P(D|+) = \frac{P(+|D) \cdot P(D)}{P(+|D) \cdot P(D) + P(+|\neg D) \cdot P(\neg D)} = \frac{0.99 \cdot 0.01}{0.99 \cdot 0.01 + 0.05 \cdot 0.99}
$$

---

### **2. Applying Bayes’ Theorem to a Situation in Context**

When given contextual data (medical tests, spam filters, manufacturing defects), Bayes’ theorem allows updating beliefs based on new evidence.

#### **Structured Application:**

* **Define Events**: Identify $`A`$, $`B`$, and their complements.
* **Translate Given Info**: Map known values to prior, likelihood, and marginal probabilities.
* **Apply Bayes’ Rule**: Solve for the posterior using the formula.

---

### **3. Solving for an Unknown Conditional Probability**

Bayes’ Theorem is often used **in reverse** to find a missing probability:

$$
P(B|A) = \frac{P(A|B) \cdot P(B)}{P(A)}
$$

If $P(A)$ is not given directly, use:

$$
P(A) = \sum_{i} P(A|B_i) \cdot P(B_i)
$$

Where the $`B_i`$ form a **partition** of the sample space.

#### **Example:**

Given:

* $`P(B_1) = 0.3`$, $`P(B_2) = 0.7`$
* $`P(A|B_1) = 0.2`$, $`P(A|B_2) = 0.6`$

Find: $`P(B_1|A)`$

$$
P(A) = 0.2 \cdot 0.3 + 0.6 \cdot 0.7 = 0.06 + 0.42 = 0.48
$$

$$
P(B_1|A) = \frac{0.2 \cdot 0.3}{0.48} = \frac{0.06}{0.48} = 0.125
$$

---

### **Summary**

| **Component**                | **Description**                               |                |                 |
| ---------------------------- | --------------------------------------------- | -------------- | --------------- |
| Bayes' Theorem Formula       | ( P(A                                         | B) = \frac{P(B | A)P(A)}{P(B)} ) |
| Used For                     | Updating probability based on new evidence    |                |                 |
| Total Probability Needed For | Calculating $`P(B)`$ when not given directly    |                |                 |
| Contextual Use Cases         | Medicine, AI/ML, manufacturing, risk analysis |                |                 |

Bayes' Theorem becomes more powerful when extended to partitions and real-world contexts, enabling precise reasoning under uncertainty.
