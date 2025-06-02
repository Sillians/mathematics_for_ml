## **Expected Values of Sums and Products of Random Variables**

---

## **1. Definition: Expected Value**

For a random variable $X$, the **expected value** (or **mean**) is defined as:

* **Discrete case**:

$$
\mathbb{E}[X] = \sum_x x \cdot \mathbb{P}(X = x)
$$

* **Continuous case**:

$$
\mathbb{E}[X] = \int_{-\infty}^{\infty} x \cdot f_X(x) \, dx
$$

Where $`f_X(x)`$ is the probability density function (pdf) of $`X`$.

---

## **2. Expected Value of the Sum of Random Variables**

For random variables $`X_1, X_2, \dots, X_n`$, the expected value of their sum is:

$$
\mathbb{E}[X_1 + X_2 + \cdots + X_n] = \mathbb{E}[X_1] + \mathbb{E}[X_2] + \cdots + \mathbb{E}[X_n]
$$

✅ **Always true**, whether the variables are **independent or dependent**.

---

### **Example: Finding the Expected Value of a Sum**

Let $`X_1, X_2`$ be the results of rolling two fair six-sided dice. Then:

$$
\mathbb{E}[X_1 + X_2] = \mathbb{E}[X_1] + \mathbb{E}[X_2] = 3.5 + 3.5 = 7
$$

---

## **3. Expected Value of a Sum in Context**

### **Example: Expected Cost**

Suppose a customer buys $`X`$ apples and $`Y`$ oranges, where:

* $`\mathbb{E}[X] = 4`$ apples, price = \$1 each
* $`\mathbb{E}[Y] = 3`$ oranges, price = \$2 each

Expected total cost:

$$
\mathbb{E}[\text{Cost}] = \mathbb{E}[1 \cdot X + 2 \cdot Y] = 1 \cdot \mathbb{E}[X] + 2 \cdot \mathbb{E}[Y] = 1(4) + 2(3) = 10
$$

---

## **4. Expected Value of the Product of Random Variables**

### **If $X$ and $Y$ are **independent**:**

$$
\mathbb{E}[XY] = \mathbb{E}[X] \cdot \mathbb{E}[Y]
$$

### **If $X$ and $Y$ are **not independent**:**

$$
\mathbb{E}[XY] \ne \mathbb{E}[X] \cdot \mathbb{E}[Y]
$$

Instead, you must use the **joint distribution**:

* **Discrete**:

$$
\mathbb{E}[XY] = \sum_{x,y} x y \cdot \mathbb{P}(X = x, Y = y)
$$

* **Continuous**:

$$
\mathbb{E}[XY] = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} xy \cdot f_{X,Y}(x,y) \, dx \, dy
$$

---

### **Example: Independent Case**

Let $`X, Y \sim \text{Uniform}\{1, 2, 3\}`$, independent.

Then:

$$
\mathbb{E}[X] = \mathbb{E}[Y] = \frac{1 + 2 + 3}{3} = 2
\quad \Rightarrow \quad
\mathbb{E}[XY] = 2 \cdot 2 = 4
$$

---

### **Example: Dependent Case**

Let $`Y = X`$, where $`X \sim \text{Bernoulli}(p)`$. Then:

$$
\mathbb{E}[XY] = \mathbb{E}[X^2] = \mathbb{E}[X] = p,
\quad
\mathbb{E}[X] \cdot \mathbb{E}[Y] = p^2
$$

So:

$$
\mathbb{E}[XY] = p \ne p^2 = \mathbb{E}[X] \cdot \mathbb{E}[Y]
$$

---

## **5. Summary Table**

| Expression                | Independence Required? | Formula                             |
| ------------------------- | ---------------------- | ----------------------------------- |
| $`\mathbb{E}[X + Y]`$       | ❌ No                   | $`\mathbb{E}[X] + \mathbb{E}[Y]`$     |
| $`\mathbb{E}[aX + bY]`$     | ❌ No                   | $`a\mathbb{E}[X] + b\mathbb{E}[Y]`$   |
| $`\mathbb{E}[XY]`$          | ✅ Yes                  | $`\mathbb{E}[X] \cdot \mathbb{E}[Y]`$ |
| $`\mathbb{E}[XY]`$, general | ❌ No                   | Use joint distribution              |

---

## **6. Linearity of Expectation**

For constants $`a_i`$ and random variables $`X_i`$:

$$
\mathbb{E}\left[\sum_{i=1}^n a_i X_i\right] = \sum_{i=1}^n a_i \mathbb{E}[X_i]
$$

This is the most powerful and widely used identity in probability!
