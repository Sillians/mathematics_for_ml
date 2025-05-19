## **Variance of Discrete Random Variables**

The **variance** of a discrete random variable measures how much the values of the variable **deviate from their mean** 
(expected value). It is a key metric in probability and statistics for quantifying **spread**, **dispersion**, or **uncertainty**.

---

### **Definition of Variance**

For a discrete random variable $X$ with **probability mass function (PMF)** $`P(X = x_i) = p_i`$, the variance is defined as:

$$
\text{Var}(X) = \mathbb{E}[(X - \mu)^2]
$$

Where $`\mu = \mathbb{E}[X]`$ is the **mean** of the random variable.

---

### **1. Computing Variance Using the Definition and a PMF**

If you're given the full PMF:

$$
\text{Var}(X) = \sum_{i} (x_i - \mu)^2 \cdot p_i
$$

#### **Example:**

Let $`X`$ take values $`1, 2, 3`$ with probabilities $`0.2, 0.5, 0.3`$

* First, compute the mean:

$$
\mathbb{E}[X] = 1(0.2) + 2(0.5) + 3(0.3) = 0.2 + 1.0 + 0.9 = 2.1
$$

* Then compute variance:

$$
\text{Var}(X) = (1 - 2.1)^2(0.2) + (2 - 2.1)^2(0.5) + (3 - 2.1)^2(0.3)
$$

$$
= (1.21)(0.2) + (0.01)(0.5) + (0.81)(0.3) = 0.242 + 0.005 + 0.243 = \boxed{0.49}
$$

---

### **2. Computing Variance Given $`\mathbb{E}[X]`$ and $`\mathbb{E}[X^2]`$**

Another way to compute variance:

$$
\text{Var}(X) = \mathbb{E}[X^2] - \left( \mathbb{E}[X] \right)^2
$$

#### **Example:**

If $`\mathbb{E}[X] = 3`$, and $`\mathbb{E}[X^2] = 11`$, then:

$$
\text{Var}(X) = 11 - (3)^2 = 11 - 9 = \boxed{2}
$$

---

### **3. Computing Variance Given a PMF (Shortcut)**

Given:

* Values of $`X`$: $`x_1, x_2, ..., x_n`$
* Corresponding probabilities: $`p_1, p_2, ..., p_n`$

Use:

$$
\mathbb{E}[X] = \sum x_i p_i, \quad \mathbb{E}[X^2] = \sum x_i^2 p_i, \quad \text{Var}(X) = \mathbb{E}[X^2] - \left(\mathbb{E}[X]\right)^2
$$

#### **Example:**

Let $`X \in \{1, 2\}`$ with $`P(X=1) = 0.4, P(X=2) = 0.6`$

* $`\mathbb{E}[X] = 1(0.4) + 2(0.6) = 1.6`$
* $`\mathbb{E}[X^2] = 1^2(0.4) + 2^2(0.6) = 0.4 + 2.4 = 2.8`$
* $`\text{Var}(X) = 2.8 - (1.6)^2 = 2.8 - 2.56 = \boxed{0.24}`$

---

### **4. Computing the Standard Deviation**

The **standard deviation** is the **square root** of the variance:

$$
\sigma_X = \sqrt{\text{Var}(X)}
$$

#### **Example:**

If $`\text{Var}(X) = 0.24`$, then:

$$
\sigma_X = \sqrt{0.24} \approx \boxed{0.49}
$$

---

### ✅ **Summary Table**

| Metric                 | Formula                                                            |
| ---------------------- | ------------------------------------------------------------------ |
| **Mean**               | $`\mathbb{E}[X] = \sum x_i p_i`$                                     |
| **Second moment**      | $`\mathbb{E}[X^2] = \sum x_i^2 p_i`$                                 |
| **Variance**           | $`\text{Var}(X) = \mathbb{E}[X^2] - \left( \mathbb{E}[X] \right)^2`$ |
| **Standard Deviation** | $`\sigma_X = \sqrt{\text{Var}(X)}`$                                  |

---

### **Conclusion**

Variance and standard deviation for discrete random variables provide vital insights into the **spread** or 
**dispersion** around the mean. Whether you're working from raw probabilities or known expectations, 
mastering these computations enables better analysis of uncertainty in real-world data.
