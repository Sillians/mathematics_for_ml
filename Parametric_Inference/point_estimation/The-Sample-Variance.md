## **The Sample Variance**

The **sample variance** is a key measure of dispersion that estimates the variability of a population based on a sample. 
It tells how spread out the sample data is around the sample mean.

---

## **Definition of Sample Variance**

Given a sample $`x_1, x_2, \dots, x_n`$, the **sample variance** $`s^2`$ is defined as:

$$
s^2 = \frac{1}{n - 1} \sum_{i=1}^{n} (x_i - \bar{x})^2
$$

Where:

* $`n`$ is the sample size,
* $`\bar{x}`$ is the sample mean:

$$
\bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i
$$

---

## **Computing an Estimate of the Population Variance**

The sample variance $`s^2`$ is used as an **unbiased estimator** of the population variance $`\sigma^2`$. 
This is why we divide by $`n - 1`$ instead of $n$.

### **Key Idea:**

$$
\text{Estimate of } \sigma^2 \approx s^2 = \frac{1}{n - 1} \sum_{i=1}^{n} (x_i - \bar{x})^2
$$

---

## **Computing an Estimate of the Population Variance Using the Alternative Formula**

A computationally simpler (but algebraically equivalent) formula is:

$$
s^2 = \frac{1}{n - 1} \left( \sum_{i=1}^{n} x_i^2 - \frac{(\sum_{i=1}^{n} x_i)^2}{n} \right)
$$

### **Why Use This?**

* Avoids repeated calculations of the sample mean.
* Useful for hand computations or streaming data.

---

## **Estimating the Population Variance From Sample Data**

### **Steps:**

1. Compute the sample mean:

$$
\bar{x} = \frac{1}{n} \sum x_i
$$

2. Use the definition:

$$
s^2 = \frac{1}{n - 1} \sum (x_i - \bar{x})^2
$$

**OR**

Use the alternative formula:

$$
s^2 = \frac{1}{n - 1} \left( \sum x_i^2 - \frac{(\sum x_i)^2}{n} \right)
$$

---

## **Example**

Given sample: $3, 7, 7, 19$

* $n = 4$
* $\bar{x} = \frac{3 + 7 + 7 + 19}{4} = 9$

Then:

$$
s^2 = \frac{1}{3} \left[(3 - 9)^2 + (7 - 9)^2 + (7 - 9)^2 + (19 - 9)^2\right]
= \frac{1}{3} [36 + 4 + 4 + 100] = \frac{144}{3} = 48
$$

---

## **Summary**

* Sample variance estimates population variance when population data is unavailable.
* Use $n - 1$ in the denominator for an unbiased estimate.
* Both standard and alternative formulas are valid and useful depending on context.

---

Let me know if you’d like this visualized or converted to a study worksheet.
