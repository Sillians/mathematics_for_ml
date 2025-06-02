## **Modeling With Discrete Uniform Distributions**

---

## **1. Definition: Discrete Uniform Distribution**

A **discrete uniform distribution** is a probability distribution in which **all outcomes in a finite set are equally likely**.

Let $X$ be a random variable that takes values in the finite set:

$$
\{x_1, x_2, \dots, x_n\}
$$

Then $`X \sim \text{Uniform}(x_1, x_2, \dots, x_n)`$ implies:

$$
\mathbb{P}(X = x_i) = \frac{1}{n}, \quad \text{for all } i = 1, 2, \dots, n
$$

---

## **2. Properties of Discrete Uniform Distribution**

Let $`X \sim \text{Uniform}(a, a+1, \dots, b)`$, where the values are consecutive integers.

* **Number of values**:

$$
n = b - a + 1
$$

* **Mean (Expected Value)**:

$$
\mathbb{E}[X] = \frac{a + b}{2}
$$

* **Variance**:

$$
\text{Var}(X) = \frac{(b - a + 1)^2 - 1}{12}
$$

---

## **3. Determining Situations That Can Be Modeled as Discrete Uniform**

A situation can be modeled as a discrete uniform distribution if:

* The number of **outcomes is finite**.
* Each outcome is **equally likely**.
* There is **no bias** or **preference** toward any outcome.

### **Common Scenarios**:

| Scenario                                         | Modeled As                                   |
| ------------------------------------------------ | -------------------------------------------- |
| Rolling a fair die                               | $`X \sim \text{Uniform}(1, 2, 3, 4, 5, 6)`$    |
| Drawing a random card from a set of unique cards | Uniform over 52 cards                        |
| Picking a random day of the week                 | $`X \sim \text{Uniform}(1, 2, 3, 4, 5, 6, 7)`$ |
| Spinning a fair roulette wheel (0–36)            | $`X \sim \text{Uniform}(0, 1, \dots, 36)`$     |

---

## **4. Modeling a Situation in Context With the Discrete Uniform Distribution**

### **Example 1: Random Password Generator**

Suppose a random password generator selects one character uniformly from the digits 0–9.

* Outcome space: $`\{0, 1, 2, \dots, 9\}`$
* Model: $`X \sim \text{Uniform}(0, 9)`$
* Probability of picking 7:

$$
\mathbb{P}(X = 7) = \frac{1}{10}
$$

* Expected value:

$$
\mathbb{E}[X] = \frac{0 + 9}{2} = 4.5
$$

---

### **Example 2: Choosing a Random Page**

You pick a random page number from a 100-page book.

* Model: $`X \sim \text{Uniform}(1, 2, \dots, 100)`$
* $`\mathbb{E}[X] = \frac{1 + 100}{2} = 50.5`$
* Probability of selecting page 42:

$$
\mathbb{P}(X = 42) = \frac{1}{100}
$$

---

## **5. Summary Table**

| Feature  | Discrete Uniform Distribution                  |
| -------- | ---------------------------------------------- |
| PMF      | $`\mathbb{P}(X = x) = \frac{1}{n}`$              |
| Support  | $`\{x_1, x_2, \dots, x_n\}`$                     |
| Mean     | $`\mathbb{E}[X] = \frac{a + b}{2}`$              |
| Variance | $`\text{Var}(X) = \frac{(b - a + 1)^2 - 1}{12}`$ |
| Use Case | Equal-likelihood over finite values            |

---

## **6. Visualization (Conceptual)**

A bar graph of a discrete uniform distribution has **equal-height bars** across the outcome space. It is **flat**, indicating no bias.


