# **The Sample Covariance Matrix**

The **sample covariance matrix** captures the pairwise covariances between multiple variables in a multivariate dataset. 
It generalizes the concept of variance to higher dimensions and is central to multivariate statistics.

---

## **1. Observation Matrix**

Suppose we have a dataset with $n$ observations of $p$ variables. This dataset can be represented as an **observation matrix** $X \in \mathbb{R}^{n \times p}$:

$$
X = 
\begin{bmatrix}
x_{11} & x_{12} & \dots & x_{1p} \\
x_{21} & x_{22} & \dots & x_{2p} \\
\vdots & \vdots & \ddots & \vdots \\
x_{n1} & x_{n2} & \dots & x_{np}
\end{bmatrix}
$$

Each row is an observation; each column is a variable.

---

## **2. Finding the Sample Mean of an Observation Matrix**

The **sample mean vector** $`\mu \in \mathbb{R}^{p}`$ is:

$$
\mu = \frac{1}{n} \sum_{i=1}^{n} x_i
$$

Where $`x_i \in \mathbb{R}^{p}`$ is the $`i`$-th observation (row of $`X`$).

Equivalently, this is the **mean of each column** of $X$, written as:

$$
\mu = 
\begin{bmatrix}
\bar{x}_1 \\
\bar{x}_2 \\
\vdots \\
\bar{x}_p
\end{bmatrix}
\quad \text{where } \bar{x}_j = \frac{1}{n} \sum_{i=1}^{n} x_{ij}
$$

---

## **3. Finding the Mean-Deviation Form of an Observation Matrix**

Let $`\mathbf{1}_n \in \mathbb{R}^{n \times 1}`$ be a column vector of ones. Then the matrix of mean values repeated across rows is:

$$
M = \mathbf{1}_n \mu^T
$$

The **mean-deviation matrix** $`D \in \mathbb{R}^{n \times p}`$ is:

$$
D = X - M = X - \mathbf{1}_n \mu^T
$$

Each row of $D$ represents the deviation of an observation from the mean.

---

## **4. Finding the Covariance Matrix**

The **sample covariance matrix** $`\Sigma \in \mathbb{R}^{p \times p}`$ is:

$$
\Sigma = \frac{1}{n - 1} D^T D
$$

Or, explicitly:

$$
\Sigma_{jk} = \frac{1}{n - 1} \sum_{i=1}^{n} (x_{ij} - \bar{x}_j)(x_{ik} - \bar{x}_k)
$$

Each entry $`\Sigma_{jk}`$ represents the **covariance** between variable $`j`$ and variable $`k`$.

* If $`j = k`$, $`\Sigma_{jj}`$ is the **sample variance** of variable $j$.
* If $`j \ne k`$, $`\Sigma_{jk}`$ is the **sample covariance** between variables $j$ and $k$.

---

## **Summary**

| Step | Description                                              |
| ---- | -------------------------------------------------------- |
| 1    | Represent data as matrix $`X \in \mathbb{R}^{n \times p}`$ |
| 2    | Compute column-wise sample mean $`\mu \in \mathbb{R}^{p}`$ |
| 3    | Form mean-deviation matrix $`D = X - \mathbf{1}_n \mu^T`$  |
| 4    | Compute covariance matrix $`\Sigma = \frac{1}{n-1} D^T D`$ |

---

This matrix plays a foundational role in PCA, multivariate normal distributions, and regression diagnostics.
