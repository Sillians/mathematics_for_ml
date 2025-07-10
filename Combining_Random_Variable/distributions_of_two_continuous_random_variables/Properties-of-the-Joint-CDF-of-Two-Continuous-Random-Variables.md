## **Properties of the Joint CDF of Two Continuous Random Variables**

---

### **1. Definition: Joint Cumulative Distribution Function (Joint CDF)**

For continuous random variables $X$ and $Y$, the **joint cumulative distribution function** (joint CDF) is:

$$
F_{X,Y}(x, y) = P(X \le x,\ Y \le y)
$$

It gives the probability that $X$ is less than or equal to $x$ and $Y$ is less than or equal to $y$.

---

### **2. Key Properties of the Joint CDF**

| Property           | Description                                          |
| ------------------ |------------------------------------------------------|
| **Non-decreasing** | $`F_{X,Y}(x, y)`$ increases as $x$ or $y$ increases. |
| **Limits**         |                                                      |

* $`\lim_{x \to -\infty} F_{X,Y}(x, y) = 0`$


* $`\lim_{y \to -\infty} F_{X,Y}(x, y) = 0`$


* $`\lim_{x \to \infty, y \to \infty} F_{X,Y}(x, y) = 1`$ |
  \| **Right-continuous** | $`F_{X,Y}(x, y)`$ is continuous from the right in both variables. |
  \| **Bounds** | $`0 \le F_{X,Y}(x, y) \le 1`$ for all $`x, y`$ |
  \| **Marginals** | Marginal CDFs can be obtained by letting one variable approach $`\infty`$ |

---

### **3. Finding a Marginal CDF Using a Joint CDF**

The **marginal CDFs** $`F_X(x)`$ and $`F_Y(y)`$ are defined as:

$$
F_X(x) = \lim_{y \to \infty} F_{X,Y}(x, y), \quad 
F_Y(y) = \lim_{x \to \infty} F_{X,Y}(x, y)
$$

#### **Example**:

Let:

$$
F_{X,Y}(x, y) = (1 - e^{-x})(1 - e^{-y}), \quad x > 0, y > 0
$$

Then:

* $`F_X(x) = \lim_{y \to \infty} F_{X,Y}(x, y) = (1 - e^{-x})(1 - 0) = 1 - e^{-x}`$


* $`F_Y(y) = 1 - e^{-y}`$

So both marginals are **Exponential(1)** CDFs.

---

### **4. Finding Part of a Joint CDF from Marginal CDFs**

In general, **marginal CDFs alone are not sufficient** to determine the joint CDF uniquely—unless independence is assumed.

If $X$ and $Y$ are **independent**, then:

$$
F_{X,Y}(x, y) = F_X(x) \cdot F_Y(y)
$$

#### **Example (Using Independence)**:

If:

* $`F_X(x) = 1 - e^{-x},\ x > 0`$


* $`F_Y(y) = 1 - e^{-2y},\ y > 0`$

Then under independence:

$$
F_{X,Y}(x, y) = (1 - e^{-x})(1 - e^{-2y})
$$

---

### **5. Recovering the Joint PDF from a Joint CDF**

If $`F_{X,Y}(x, y)`$ is continuously differentiable, then the **joint PDF** $`f_{X,Y}(x, y)`$ is the **mixed partial derivative**:

$$
f_{X,Y}(x, y) = \frac{\partial^2 F_{X,Y}(x, y)}{\partial x\, \partial y}
$$

#### **Example**:

Let:

$$
F_{X,Y}(x, y) = (1 - e^{-x})(1 - e^{-y}), \quad x > 0, y > 0
$$

Compute:

$$
f_{X,Y}(x, y) = \frac{\partial^2}{\partial x\, \partial y} \left( (1 - e^{-x})(1 - e^{-y}) \right)
$$

Step-by-step:

* $`\frac{\partial}{\partial y} = (1 - e^{-x})(e^{-y})`$


* $`\frac{\partial}{\partial x} = e^{-x} \cdot e^{-y} = e^{-(x + y)}`$

So:

$$
f_{X,Y}(x, y) = e^{-(x + y)}, \quad x > 0, y > 0
$$

This is the **joint PDF** of two independent Exponential(1) variables.

---

### **6. Summary Table**

| Concept                   | Formula or Rule                                                             |
| ------------------------- | --------------------------------------------------------------------------- |
| Joint CDF                 | $`F_{X,Y}(x, y) = P(X \le x, Y \le y)`$                                       |
| Marginal CDF (from joint) | $`F_X(x) = \lim_{y \to \infty} F_{X,Y}(x, y)`$                                |
| Independence              | $`F_{X,Y}(x, y) = F_X(x) \cdot F_Y(y)`$                                       |
| Recover PDF               | $`f_{X,Y}(x, y) = \frac{\partial^2 F_{X,Y}(x, y)}{\partial x \, \partial y}`$ |

---

### **7. Applications**

| Field            | Use Case                                                  |
| ---------------- | --------------------------------------------------------- |
| **Statistics**   | Compute probabilities involving two variables             |
| **Econometrics** | Model joint distribution of income and spending           |
| **ML / AI**      | Estimate joint likelihoods in generative models           |
| **Engineering**  | Reliability of systems with two interdependent components |

---
