## **The Correlation Coefficient for Two Random Variables**

### **1. Definition and Purpose**

The **correlation coefficient** between two random variables $X$ and $Y$, denoted $`\rho_{X,Y}`$, quantifies the **strength and direction** of their **linear relationship**. 
It is a standardized measure ranging from:

$$
-1 \leq \rho_{X,Y} \leq 1
$$

* $`\rho = 1`$: perfect positive linear relationship


* $`\rho = -1`$: perfect negative linear relationship


* $`\rho = 0`$: no linear relationship (though other forms of dependence may exist)

---

### **2. Formula for the Correlation Coefficient**

$$
\rho_{X,Y} = \frac{\mathrm{Cov}(X,Y)}{\sigma_X \sigma_Y}
$$

Where:

* $`\mathrm{Cov}(X,Y)`$ is the **covariance** of $X$ and $Y$


* $`\sigma_X = \sqrt{\mathrm{Var}(X)}`$, $`\sigma_Y = \sqrt{\mathrm{Var}(Y)}`$

This dimensionless ratio standardizes covariance, making $`\rho`$ comparable across different contexts.

---

### **3. Finding a Correlation Coefficient Given Variances and Covariance**

If you're given:

* $`\mathrm{Var}(X)`$


* $`\mathrm{Var}(Y)`$


* $`\mathrm{Cov}(X, Y)`$

Then:

$$
\rho_{X,Y} = \frac{\mathrm{Cov}(X, Y)}{\sqrt{\mathrm{Var}(X)} \cdot \sqrt{\mathrm{Var}(Y)}}
$$

#### **Example**:

Let $`\mathrm{Cov}(X, Y) = 3`$, $`\mathrm{Var}(X) = 4`$, $`\mathrm{Var}(Y) = 9`$.
Then:

$$
\rho = \frac{3}{\sqrt{4} \cdot \sqrt{9}} = \frac{3}{2 \cdot 3} = \frac{3}{6} = 0.5
$$

---

### **4. Finding the Correlation Coefficient of Two Discrete Random Variables**

#### **Step-by-Step Process**:

Given the joint PMF $`p(x,y)`$ of $X$ and $Y$:

1. Compute $`\mathbb{E}[X]`$, $`\mathbb{E}[Y]`$


2. Compute $`\mathbb{E}[XY]`$


3. Find $`\mathrm{Cov}(X,Y) = \mathbb{E}[XY] - \mathbb{E}[X]\,\mathbb{E}[Y]`$


4. Find $`\mathrm{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2`$, similarly for $Y$


5. Use:

$$
\rho = \frac{\mathrm{Cov}(X, Y)}{\sqrt{\mathrm{Var}(X)} \cdot \sqrt{\mathrm{Var}(Y)}}
$$

#### **Example**:

| $`(x, y)`$ | $`p(x, y)`$ |
|-----------|-------------|
| (1, 1)    | 0.2         |
| (1, 2)    | 0.3         |
| (2, 1)    | 0.1         |
| (2, 2)    | 0.4         |

You'd compute expectations, variances, and covariance from the table, then apply the formula.

---

### **5. Finding the Correlation Coefficient of Two Continuous Random Variables**

Given a joint PDF $`f(x, y)`$:

#### **Steps**:

1. Compute:

   * $`\mathbb{E}[X] = \int\int x f(x, y)\,dxdy`$
   * $`\mathbb{E}[Y] = \int\int y f(x, y)\,dxdy`$
   * $`\mathbb{E}[XY] = \int\int xy f(x, y)\,dxdy`$


2. Find:

   * $`\mathrm{Cov}(X,Y) = \mathbb{E}[XY] - \mathbb{E}[X]\,\mathbb{E}[Y]`$
   * $`\mathrm{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2`$, and similarly for $Y$


3. Plug into:

$$
\rho = \frac{\mathrm{Cov}(X,Y)}{\sqrt{\mathrm{Var}(X)} \cdot \sqrt{\mathrm{Var}(Y)}}
$$

---

### **6. Summary Table**

| Quantity            | Expression                                                    |
| ------------------- |---------------------------------------------------------------|
| $`\rho_{X,Y}`$        | $`\displaystyle \frac{\mathrm{Cov}(X,Y)}{\sigma_X \sigma_Y}`$ |
| $`\mathrm{Cov}(X,Y)`$ | $`\mathbb{E}[XY] - \mathbb{E}[X]\,\mathbb{E}[Y]`$             |
| $`\sigma_X`$          | $`\sqrt{ \mathbb{E}[X^2] - (\mathbb{E}[X])^2 }`$              |
| $`\sigma_Y`$          | $`\sqrt{ \mathbb{E}[Y^2] - (\mathbb{E}[Y])^2 }`$              |

---

### **7. Interpretation of Correlation**

| $\rho$ | Interpretation                                 |
| ------ | ---------------------------------------------- |
| $`= 1`$  | Perfect positive linear association            |
| $`> 0`$  | Positive linear association                    |
| $`= 0`$  | No linear correlation (but possibly dependent) |
| $`< 0`$  | Negative linear association                    |
| $`= -1`$ | Perfect negative linear association            |

---

The correlation coefficient is a **powerful summary statistic** for linear relationships, but always pair it with scatterplots or context to avoid misinterpretation — especially in the presence of nonlinear dependencies.
