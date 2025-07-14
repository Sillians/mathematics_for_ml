# **The Singular Values of a Matrix**

An $`m\times n`$ real (or complex) matrix $A$ stretches $`\mathbb R^n`$ (the *domain*) into $`\mathbb R^m`$ (the *codomain*).
The **singular‐value decomposition (SVD)** extracts the pure geometric action of that stretch.

$$
\boxed{\,A \;=\; U\,\Sigma\,V^{\!T}\,}
$$

* $`U \in \mathbb R^{m\times m}`$ orthogonal (columns = *left* singular vectors)

* $`V \in \mathbb R^{n\times n}`$ orthogonal (columns = *right* singular vectors)

* $`\Sigma = \\mathrm{diag}\bigl(\sigma\_1,\ldots,\sigma\_r,0,\dots\bigr)`$, $`\sigma\_1\ge\dots\ge\sigma\_r>0`$



The numbers $`\sigma\_i`$ are the **singular values**.  Geometrically:

* The columns of $V$ form an orthonormal basis of the domain.


* $A$ sends the *unit* sphere into an *ellipsoid* whose semi‐axes have lengths $`\sigma\_1,\dots,\sigma\_r`$ and directions given by the corresponding columns of $U$.

---

## 1 · Finding the Semi-Major Axis of the Image of the Unit Sphere

The **longest semi-axis** of the ellipsoid $`A\bigl(S^{,n-1}\bigr)`$ is obtained by maximizing $`\lVert A\mathbf x\rVert`$ over all unit vectors $`\mathbf x`$:

$$
\sigma_{\max} \;=\; \max_{\lVert\mathbf x\rVert=1} \lVert A\mathbf x\rVert
$$

*Optimal vector* $`\mathbf v\_1`$ = the first right singular vector
*Image*         $`\sigma\_1,\mathbf u\_1`$ = the first left singular vector scaled by $`\sigma\_1`$.

Hence:

* **Length of semi-major axis:** $`\boxed{\sigma\_1}`$


* **Direction:** $`\mathbf u\_1`$

---

## 2 · Finding the Semi-Major Axis Given the Singular Values

If the singular values are already known:

$$
\Sigma=\\mathrm{diag}(\sigma_1,\sigma_2,\dots,\sigma_r,0,\dots)
$$

then

### •  Length

$$
\displaystyle\text{semi-major length}= \sigma_1
$$

### •  End-points in $`\mathbb R^m`$

$$
\pm\,\sigma_1\,\mathbf u_1
\quad\text{(where $\mathbf u_1$ is the first column of $U$)}
$$

---

## 3 · Problems Involving the Images of Unit Eigen-vectors of a Quadratic Form

Suppose we have a symmetric matrix $B$ (a quadratic form) with eigen-pairs $`(\lambda\_i,\mathbf w\_i)`$, $`\mathbf w\_i`$ orthonormal.

1. **Map each eigen-vector of $B$ through some linear map $A$.**
   The image of the unit sphere aligns with the singular vectors of $A$, not with the eigen-vectors of $B$ unless $A$ and $B$ commute or share eigen-bases.


2. **If $`A=B=:`$ $`S`$ is symmetric positive-definite**, then *singular* values equal *absolute* eigen-values and singular vectors equal eigen-vectors.

---

### Example Problem & Solution

> **Problem.** Let
>
> $$
> A=\begin{bmatrix}4&0&0\\0&2&0\\0&0&1\end{bmatrix}.
> $$
>
> (i) Find its singular values.
> 
> 
> (ii) Describe the image of the **unit sphere**.
> 
> 
> 
> (iii) Which unit vectors in the domain map to the semi-major axis?

**Solution**

1. Because $A$ is diagonal with positive entries, its singular values are its diagonal entries in descending order:

$$
\sigma_1=4,\;\sigma_2=2,\;\sigma_3=1.
$$

2. The unit sphere maps to the ellipsoid

$$
\frac{x'^2}{4^2}+\frac{y'^2}{2^2}+\frac{z'^2}{1^2}=1.
$$

3. The semi-major axis has length $`\sigma\_1=4`$ along the positive and negative $`x'`$-direction.
   The corresponding unit vectors in the domain are $`\pm(1,0,0)`$.

---

## ✨  Quick Reference

| Task                                 | Formula / Answer                                          |
| ------------------------------------ |-----------------------------------------------------------|
| *n*×*n* matrix $A$ SVD               | $`{\,A \;=\; U\,\Sigma\,V^{\!T}\,}`$                      |
| Singular values                      | $`\sigma\_i=\sqrt{\lambda\_i(A^TA)}`$                     |
| Semi-major axis length               | $`\sigma\_1`$                                             |
| Semi-major axis direction            | first left singular vector $`\mathbf u\_1`$               |
| Unit vectors mapped to semi-major axis | $`\pm,\mathbf v\_1`$ (first right singular vector)        |
| Image of unit sphere                 | Ellipsoid with semi-lengths $`(\sigma\_1,\dots,\sigma\_r)`$ |

---

**Take-away:**
Singular values *are* the semi-axis lengths of the image of the unit sphere under $A$.
The right singular vectors give the domain directions, and the left singular vectors give the codomain directions of those axes.
