# week40

> **Theorem 2.2 (Comparison Test)**<br>If $0\le a_n\le b_n$ and $\sum b_n$ converges, then $\sum a_n$ converges.

> **Theorem 3.2 (Dirichlet's Test)**<br>If $\left\{b_n\right\}$ is monotone tending to $0$ and the partial sums of $\sum a_n$ are bounded, then $\sum a_nb_n$ converges.

> **Theorem 3.3 (Abel's Test)**<br>If $\left\{b_n\right\}$ is monotone and bounded, and $\sum a_n$ converges, then $\sum a_nb_n$ converges.

---

## 10.3-2

Prove: $\sum\frac{\cos nx}{n^p}$ converges absolutely for $p> 1$ and conditionally for $0< p\le1$.

### Solution 10.3-2

For $p> 1$, by comparison with $\sum\frac1{n^p}$. For $0< p\le1$, not absolutely convergent (since $\left|\cos nx\right|\ge\cos^2nx$), but convergent by Dirichlet's test. $\blacksquare$

---

## 10.3-4

Prove the Dirichlet series has a half-line domain of convergence.

### Solution 10.3-4

By Abel's test applied to $\frac{a_n}{n^x}=\frac{a_n}{n^{x_0}}\cdot\frac1{n^{x-x_0}}$. $\blacksquare$

---

## 10.3-5

Prove: $S_{2n}=h_{2n}-h_n$, $S_{2n}\to\ln2$, and $\sum\frac{\left(-1\right)^{n-1}}n=\ln2$.

### Solution 10.3-5

Direct computation and using $h_n=\ln n+\gamma+o\left(1\right)$. $\blacksquare$
