## **Singular Value Decomposition (SVD) and the Pseudoinverse Matrix**

---

## 1 | Recap of the SVD

For any real $`m\times n`$ matrix $A$ (rank $r$) there exist orthogonal matrices

$$
U\in\mathbb R^{m\times m},\qquad
V\in\mathbb R^{n\times n},
$$

and a diagonal matrix

$$
\Sigma=\operatorname{diag}(\sigma_1,\dots,\sigma_r,0,\dots)
\qquad(\sigma_1\ge\dots\ge\sigma_r>0)
$$

such that

$$
A = U\Sigma V^{\!\top}.
$$

* **$`\sigma_i`$**: *singular values*


* **$U$**: columns are *left singular vectors*


* **$V$**: columns are *right singular vectors*

---

## 2 | Moore–Penrose Pseudoinverse via Full SVD

Given $`A = U\Sigma V^{\!\top}`$,

$$
\boxed{\,A^{+} = V \Sigma^{+} U^{\!\top}\,}
$$

where $`\Sigma^{+}`$ is obtained by **reciprocating the non‑zero singular values** and transposing the rectangular block:

$$
\Sigma^{+}= \operatorname{diag}\!\bigl(\tfrac1{\sigma_1},\dots,\tfrac1{\sigma_r},0,\dots\bigr)^{\top}.
$$

---

## 3 | Finding the Pseudoinverse of a **Diagonal Matrix**

If

$$
D = \operatorname{diag}(d_1,d_2,\dots,d_k),
$$

its pseudoinverse is

$$
D^{+} = \operatorname{diag}\!\Bigl(
\;\tfrac1{d_1}\mathbf 1_{\{d_1\neq0\}},\,
\dots,\,
\tfrac1{d_k}\mathbf 1_{\{d_k\neq0\}}
\Bigr),
$$

that is, **invert non‑zero diagonals, leave zeros unchanged**.

*Example*
$`D=\operatorname{diag}(5,0,2) \Rightarrow D^{+}=\operatorname{diag}\bigl(\tfrac15,0,\tfrac12\bigr).`$

---

## 4 | Pseudoinverse from a **Full SVD** — Step‑by‑Step

1. **Compute SVD** $`A = U \Sigma V^{\!\top}`$.


2. **Form $`\Sigma^{+}`$** by reciprocating positive singular values.


3. **Assemble** $`A^{+} = V \Sigma^{+} U^{\!\top}`$.

### Mini‑Example

$`A = \begin{bmatrix}0&4\\3&0\end{bmatrix}`$

Full SVD (sketched):

$$
U=
\begin{bmatrix}0&1\\1&0\end{bmatrix},\;
\Sigma=\operatorname{diag}(4,3),\;
V=
\begin{bmatrix}1&0\\0&1\end{bmatrix}.
$$

$$
\Sigma^{+}=\operatorname{diag}\!\bigl(\tfrac14,\tfrac13\bigr),\qquad
A^{+}=V\Sigma^{+}U^{\!\top}
      =\begin{bmatrix}0&\tfrac14\\[2pt]\tfrac13&0\end{bmatrix}.
$$

---

## 5 | Pseudoinverse from a **Reduced SVD**

The **economy (thin) SVD** keeps only rank‑$r$ components:

$$
A = U_r \,\Sigma_r \, V_r^{\!\top},
\qquad
U_r\in\mathbb R^{m\times r},\;
\Sigma_r\in\mathbb R^{r\times r},\;
V_r\in\mathbb R^{n\times r}.
$$

Because $`U_r^{\!\top}U_r = V_r^{\!\top}V_r = I_r`$,

$$
\boxed{\,A^{+} = V_r\,\Sigma_r^{-1}\,U_r^{\!\top}\,}.
$$

### Why useful?

* Saves memory (store only rank $r$).
* Faster for large, low‑rank matrices.

---

## 6 | At‑a‑Glance Summary

| Task                                       | Key Formula                          |
|--------------------------------------------| ------------------------------------ |
| Diagonal $D$                               | Invert non‑zero diagonals ⇒ $`D^{+}`$  |
| Full SVD $`A=U\Sigma V^{\!\top}`$          | $`A^{+}=V\Sigma^{+}U^{\!\top}`$        |
| Reduced SVD $`A=U_r\Sigma_r V_r^{\!\top}`$ | $`A^{+}=V_r\Sigma_r^{-1}U_r^{\!\top}`$ |


Singular‑value‑based construction ensures **all four Moore–Penrose conditions** are satisfied, 
yielding the unique pseudoinverse needed in least‑squares, signal processing, control, and data science.
