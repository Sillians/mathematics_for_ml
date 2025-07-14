## **Confidence Intervals for One Variance**

---

### 1 | Setting

A random sample

$$
X_1,\;X_2,\;\dots,\;X_n \;\; \stackrel{\text{i.i.d.}}{\sim}\; \mathcal N\!\bigl(\mu,\sigma^{2}\bigr)
$$

with **unknown variance** $`\sigma^{2}`$.

---

### 2 | Sampling Distribution of the Sample Variance

The (unbiased) sample variance

$$
S^{2}= \frac{1}{\,n-1\,}\sum_{i=1}^{n}(X_i-\bar X)^{2}
$$

satisfies

$$
\boxed{\,\frac{(n-1)S^{2}}{\sigma^{2}} \sim \chi^{2}_{\,n-1}\,}.
$$

This chi‑square pivot is the key to interval estimation.

---

### 3 | Finding a Confidence Interval for the Population Variance $\sigma^{2}$

For confidence level $`1-\alpha`$ (two‑tailed), let

$`\chi^{2}_{\alpha/2,\;n-1},\quad \chi^{2}_{1-\alpha/2,\;n-1}`$

denote the **lower** and **upper** critical values of the chi‑square distribution with $n-1$ d.f.

The exact $`(1-\alpha)`$ confidence interval is

$`\boxed{ \left(\, \frac{(n-1)S^{2}}{\chi^{2}_{1-\alpha/2,\;n-1}}\;,\; \frac{(n-1)S^{2}}{\chi^{2}_{\alpha/2,\;n-1}} \right). }`$

---

### 4 | Confidence Interval for the Standard Deviation $\sigma$

Simply **take square‑roots** of the variance limits:

$`\boxed{ \left(\, \sqrt{\frac{(n-1)S^{2}}{\chi^{2}_{1-\alpha/2,\;n-1}}}\;,\; \sqrt{\frac{(n-1)S^{2}}{\chi^{2}_{\alpha/2,\;n-1}}} \right). }`$

---

### 5 | Worked Example

Sample size $`n = 15`$; calculated $`S^{2}=42\ \mathrm{(units^2)}`$.
Goal: 95 % CI.

*Degrees of freedom:* $`\nu = 14`$.


From chi‑square table:

$`\chi^{2}_{0.025,14}=\,5.629, \qquad \chi^{2}_{0.975,14}=\,26.119.`$

**Variance CI**

$`\left(\frac{14\times 42}{26.119},\; \frac{14\times 42}{5.629} \right) = \bigl(22.5,\;104.5\bigr)`$

**Std–dev CI**

$`\bigl(\sqrt{22.5},\;\sqrt{104.5}\bigr) =\;(4.75,\;10.22)`$

Interpretation: we are 95 % confident the population variance lies between 22.5 and 104.5, equivalently the true σ is between 4.75 and 10.22.

---

### 6 | Assumptions & Caveats

| Requirement                     | Reason                                          |
| ------------------------------- | ----------------------------------------------- |
| **Normality of the population** | Chi‑square pivot is exact only under normality. |
| **Random, independent sample**  | Ensures validity of the sampling distribution.  |

For **moderate departures** from normality, the interval may be conservative or liberal; robust alternatives (e.g., bootstrap) can be considered.

---

### 7 | Applications

| Field / Scenario                | Why the Variance Interval Matters                                                     |
| ------------------------------- | ------------------------------------------------------------------------------------- |
| **Manufacturing quality**       | Ensures process variability stays within tolerance limits (e.g., diameters, weights). |
| **Finance / Risk**              | Interval for σ of returns quantifies uncertainty in volatility estimates.             |
| **Metrology & instrumentation** | Assess precision (repeatability variance) of measurement devices.                     |
| **Clinical trials**             | Determine variability of blood‑pressure response to a drug for dose planning.         |
| **Engineering reliability**     | Interval for stress/strain variance guides safety factors in design.                  |

---

### 8 | Quick‑Reference Table

| Target CI      | Interval End‑points                                                                                            |
|----------------| -------------------------------------------------------------------------------------------------------------- |
| $`\sigma^{2}`$ | $`\displaystyle \frac{(n-1)S^{2}}{\chi^{2}_{1-\alpha/2,\;n-1}},\; \frac{(n-1)S^{2}}{\chi^{2}_{\alpha/2,\;n-1}}`$ |
| $`\sigma`$     | Square‑roots of the variance limits                                                                            |

---

#### ✔ Key Takeaway

Because $`\sigma^{2}`$ drives variability, its confidence interval—built from the chi‑square distribution—underpins rigorous statements about spread, precision, 
and risk whenever population normality is a reasonable assumption.
