## **Type I and Type II Errors**

---

### **1. Overview of Hypothesis Testing Errors**

In hypothesis testing, decisions are made based on limited data. Two types of errors can occur:

| **Reality**       | **Decision**           | **Result**                         |
|-------------------|------------------------| ---------------------------------- |
| $`H_0`$ is true   | Fail to reject $`H_0`$ | Correct decision                   |
| $`H_0`$ is true   | Reject $`H_0`$         | **Type I Error** (False Positive)  |
| $`H_0`$ is false  | Reject $`H_0`$         | Correct decision                   |
| $`H_0`$ is false  | Fail to reject $`H_0`$ | **Type II Error** (False Negative) |

---

### **2. Identifying Type I Errors**

A **Type I Error** occurs when:

* The **null hypothesis $`H_0`$** is **true**,


* But we **incorrectly reject** it.

#### **Notation:**

* Probability of Type I Error = **α** (significance level)

#### **Examples:**

* A medical test wrongly indicates a disease when the person is healthy.


* A bank detects fraud when there was no fraudulent activity.


* A researcher claims a new drug works when it actually doesn't.

---

### **3. Type I Errors in Modeling Contexts**

In statistical modeling and machine learning, Type I Errors manifest as **false alarms** or **false positives**.

#### **Applications:**

| **Context**          | **Type I Error**                             |
| -------------------- | -------------------------------------------- |
| Email spam detection | A legitimate email is flagged as spam.       |
| Fraud detection      | A valid transaction is marked as fraudulent. |
| A/B testing          | Conclude version B is better when it’s not.  |
| Quality control      | A good product is rejected as defective.     |

Controlling Type I Error is **crucial** in high-stakes environments. Choosing a smaller α (e.g., 0.01) reduces Type I Errors but may increase Type II Errors.

---

### **4. Identifying Type II Errors**

A **Type II Error** occurs when:

* The **null hypothesis $`H_0`$** is **false**,


* But we **fail to reject** it.



#### **Notation:**

* Probability of Type II Error = **β**


* Power of the test = $`1 - \beta`$ (probability of correctly rejecting a false $H_0$)


#### **Examples:**

* A cancer test fails to detect the disease in a sick patient.


* A researcher fails to detect a real effect in data.

---

### **5. Type II Errors in Modeling Contexts**

These are **missed detections** or **false negatives**.

#### **Applications:**

| **Context**          | **Type II Error**                                  |
| -------------------- | -------------------------------------------------- |
| Email spam detection | A spam email is mistakenly allowed into the inbox. |
| Fraud detection      | A fraudulent transaction goes undetected.          |
| A/B testing          | A genuinely better version is missed.              |
| Quality control      | A defective product passes inspection.             |

Type II Errors are especially costly when **failing to act** on a real issue causes harm.

---

### **6. Balancing Type I and Type II Errors**

There's a **tradeoff** between α and β:

* **Lowering α** (fewer false positives) usually increases β (more false negatives).


* To reduce both:

  * **Increase sample size**
  * Use **more sensitive test statistics**
  * Improve **measurement precision**

---

### **7. Summary Table**

| **Error Type** | **Condition**                                | **Real-World Impact**             | **Symbol** |
| -------------- |----------------------------------------------| --------------------------------- | ---------- |
| Type I         | Reject $`H_0`$ when $`H_0`$ is true          | False positive (false alarm)      | $`\alpha`$   |
| Type II        | Fail to reject $`H_0`$ when $`H_0`$ is false | False negative (missed detection) | $`\beta`$    |

---

### **8. Visual Representation (Conceptual)**

* Imagine two overlapping distributions:

  * One under $`H_0`$, the other under $`H_1`$


* The **rejection region** is determined by α.


* **Type I Error:** area under $`H_0`$ in rejection region.


* **Type II Error:** area under $`H_1`$ in non-rejection region.

---