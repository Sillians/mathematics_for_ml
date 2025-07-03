## **Marginal Distributions for Discrete Random Variables**

---

### **Definition**

A **marginal distribution** describes the probabilities of the individual values of one variable in a joint 
distribution, obtained by summing over the possible values of the other variable.

For random variables $X$ and $Y$, if $`f(x, y)`$ is the joint probability mass function (PMF), then:

* **Marginal distribution of $X$**:
  $`f_X(x) = \sum_{y} f(x, y)`$
* **Marginal distribution of $Y$**:
  $`f_Y(y) = \sum_{x} f(x, y)`$

---

### **1. Finding a Marginal Probability**

A **marginal probability** is the probability that a single variable takes a certain value, regardless of the value of the other variable.

**Example**:
If $`P(X = 2, Y = 1) = 0.1`$, $`P(X = 2, Y = 2) = 0.2`$, then:

$$
P(X = 2) = 0.1 + 0.2 = 0.3
$$

---

### **2. Finding a Marginal Probability Distribution**

To find the **full marginal distribution**, sum the joint PMF across the rows or columns of the joint table.

**Example**:

|         | $`Y = 0`$ | $`Y = 1`$ | $`Y = 2`$ |
| ------- | ------- | ------- | ------- |
| $`X = 0`$ | 0.1     | 0.2     | 0.1     |
| $`X = 1`$ | 0.2     | 0.1     | 0.3     |

* $`P(X = 0) = 0.1 + 0.2 + 0.1 = 0.4`$
* $`P(X = 1) = 0.2 + 0.1 + 0.3 = 0.6`$

This gives the marginal PMF of $X$.

---

### **3. Finding a Cumulative Probability Given a Joint Distribution**

A **cumulative probability** over a region is the sum of all joint probabilities in that region.

**Example**:
Find $`P(X \leq 1, Y \leq 1)`$:
Sum $`f(x, y)`$ over all $`x = 0, 1`$ and $`y = 0, 1`$.

$$
P(X \leq 1, Y \leq 1) = f(0,0) + f(0,1) + f(1,0) + f(1,1)
$$

---

### **Summary**

* Marginal distributions summarize one variable regardless of the other.
* Marginal probabilities are single values from the marginal distribution.
* Cumulative probabilities add values from multiple points in the joint distribution.
