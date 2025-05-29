## **Simulating Random Observations**

---

### **1. Simulating Observations Given a CDF**

When the **cumulative distribution function (CDF)** of a random variable is known, we can generate 
random observations using the **inverse transform sampling method**. This method works as follows:

#### **Steps:**

1. Generate a uniform random variable $`U \sim U(0, 1)`$.
2. Compute $`X = F^{-1}(U)`$, where $`F^{-1}`$ is the inverse of the CDF.
3. The value $X$ is a simulated observation from the original distribution.

#### **Example:**

Let the CDF be $`F(x) = 1 - e^{-\lambda x}`$ (Exponential distribution).

* Invert: $`F^{-1}(u) = -\frac{1}{\lambda} \ln(1 - u)`$
* Simulate: $`X = -\frac{1}{\lambda} \ln(1 - U)`$

---

### **2. Simulating Observations Given a PDF**

If the **probability density function (PDF)** is known but **no closed-form inverse CDF**, 
then simulation methods include:

#### **a. Inverse Transform (when CDF invertible)**

Same as above, but requires you to first integrate the PDF to get $`F(x)`$, then invert $F$.

#### **b. Rejection Sampling**

Used when the PDF is complex or the inverse CDF is not available.

**Steps:**

1. Choose an easy-to-sample proposal distribution $`g(x)`$ and constant $`c \geq 1`$ such that:

$$
f(x) \leq c \cdot g(x) \quad \text{for all } x
$$

2. Sample $`X \sim g(x)`$, then $`U \sim U(0, 1)`$
3. Accept $`X`$ if:

$$
U \leq \frac{f(X)}{c \cdot g(X)}
$$

Otherwise, reject and repeat.

---

### **Summary of Key Concepts:**

| Method                     | When to Use                     | Key Requirement                              |
| -------------------------- | ------------------------------- | -------------------------------------------- |
| Inverse Transform Sampling | Known, invertible CDF           | Must compute or have closed form of $F^{-1}$ |
| Rejection Sampling         | Complicated PDF, no inverse CDF | Must find suitable envelope function $g(x)$  |
| Numerical Inversion        | Known CDF but not invertible    | Requires root-finding or interpolation       |

---

These techniques are foundational in **Monte Carlo methods**, used in probabilistic simulations and numerical integrations.
