## **Bayes' Theorem**

Bayes’ Theorem is a fundamental result in probability theory that allows you to update the probability 
of a hypothesis given new evidence. It reverses conditional probabilities, making it essential in 
inference, decision theory, and real-world applications such as diagnostics and classification.

---

### **1. Bayes' Theorem Formula**

The classic form of Bayes' Theorem is:

$$
P(A \mid B) = \frac{P(B \mid A) \cdot P(A)}{P(B)}
$$

Where:

* $`P(A \mid B)`$ is the **posterior probability** (updated probability of hypothesis $A$ given data $B$)
* $`P(B \mid A)`$ is the **likelihood** (probability of observing $B$ if $A$ is true)
* $`P(A)`$ is the **prior probability** of $A$
* $`P(B)`$ is the **marginal probability** of observing $B$

---

### **2. Computing a Conditional Probability Using Bayes' Theorem**

**Example:**
A test for a disease is 99% accurate, and the disease affects 1 in 1000 people. 
What is the probability that a person has the disease given a positive test?

* Let $`D`$: has disease, $T$: tests positive
* $`P(D) = 0.001`$, $`P(T \mid D) = 0.99`$, $`P(T \mid \text{no } D) = 0.01`$, $`P(\text{no } D) = 0.999`$

Then:

$$
P(D \mid T) = \frac{P(T \mid D) \cdot P(D)}{P(T \mid D) \cdot P(D) + P(T \mid \text{no } D) \cdot P(\text{no } D)} = \frac{0.99 \cdot 0.001}{0.99 \cdot 0.001 + 0.01 \cdot 0.999}
$$

$$
P(D \mid T) \approx \frac{0.00099}{0.00099 + 0.00999} = \frac{0.00099}{0.01098} \approx 0.0901
$$

So there's only about a **9.01%** chance the person actually has the disease.

---

### **3. Applying Bayes’ Theorem to a Situation in Context**

In **spam filtering**, a message is flagged as spam based on the probability that it contains certain words. 
Bayes' theorem allows updating the probability that a message is spam given the presence of specific words (features).

---

### **4. Applying Bayes’ Theorem With the Law of Total Probability**

If multiple mutually exclusive events $`A_1, A_2, \dots, A_n`$ partition the sample space, then:

$$
P(B) = \sum_{i=1}^{n} P(B \mid A_i) \cdot P(A_i)
$$

Then for any $A_k$:

$$
P(A_k \mid B) = \frac{P(B \mid A_k) \cdot P(A_k)}{\sum_{i=1}^{n} P(B \mid A_i) \cdot P(A_i)}
$$

This version is useful when multiple causes could explain an outcome.

---

### **5. Determining the Accuracy of Medical Tests**

In medical diagnostics:

* **Sensitivity** $`= P(\text{Positive} \mid \text{Disease})`$
* **Specificity** $`= P(\text{Negative} \mid \text{No Disease})`$

Bayes' Theorem is used to find:

$$
P(\text{Disease} \mid \text{Positive}) = \frac{P(\text{Positive} \mid \text{Disease}) \cdot P(\text{Disease})}{P(\text{Positive})}
$$

This accounts for **false positives** and shows why even accurate tests can lead to misleading interpretations when the condition is rare.

---

**In summary,**, Bayes’ Theorem is a powerful tool for probabilistic reasoning, widely used in:

* Medical diagnostics
* Machine learning classification
* Risk assessment
* Natural language processing
* Decision-making under uncertainty
