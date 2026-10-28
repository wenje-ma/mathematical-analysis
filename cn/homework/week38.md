# week38

> **基础知识: 级数收敛的定义**<br>给定数列 $\left\{a_n\right\}$, 作部分和 $S_n=\sum_{k=1}^n a_k$. 若 $\lim_{n\to\infty}S_n=S$ 存在且有限, 则称级数 $\sum a_n$ 收敛, $S$ 为其和; 否则称发散.

> **定理 1.1 (收敛级数的必要条件)**<br>若级数 $\sum a_n$ 收敛, 则 $\lim_{n\to\infty}a_n=0$.

---

## 10.1-1

证明等比级数 $a_0+a_0q+\cdots$ 当 $\left|q\right|< 1$ 时收敛且和为 $\frac{a_0}{1-q}$, 当 $\left|q\right|\ge1$ 时发散.

### 解答 10.1-1

部分和 $S_n=a_0\frac{1-q^{n+1}}{1-q}$. 当 $\left|q\right|< 1$ 时, $q^{n+1}\to0$, 由**基础知识: 级数收敛的定义**, 级数收敛且和为 $\frac{a_0}{1-q}$. 当 $q=1$ 时 $S_n\to\infty$. 当 $\left|q\right|> 1$ 时通项不趋于 $0$, 由**定理 1.1 (收敛级数的必要条件)**, 发散. $\blacksquare$

---

## 10.1-2-1

讨论 $\sum_{n=1}^\infty\left(\sqrt{n+1}-\sqrt n\right)$ 的收敛性.

### 解答 10.1-2-1

部分和 $S_N=\sqrt{N+1}-1\to+\infty$. 由**基础知识: 级数收敛的定义**, 级数发散. $\blacksquare$

---

## 10.1-2-2

讨论 $\sum_{n=1}^\infty\frac1{\left(2n-1\right)\left(2n+1\right)}$ 的收敛性.

### 解答 10.1-2-2

裂项: $\frac1{\left(2n-1\right)\left(2n+1\right)}=\frac12\left(\frac1{2n-1}-\frac1{2n+1}\right)$. 部分和 $S_N=\frac12\left(1-\frac1{2N+1}\right)\to\frac12$. 由**基础知识: 级数收敛的定义**, 级数收敛. $\blacksquare$

---

## 10.1-2-3

讨论 $\sum_{n=1}^\infty\ln\frac n{n+5}$ 的收敛性.

### 解答 10.1-2-3

裂项相消后 $S_N=\ln\left(1\cdot2\cdot3\cdot4\cdot5\right)-\ln\left(\left(N+1\right)\cdots\left(N+5\right)\right)\to-\infty$. 由**基础知识: 级数收敛的定义**, 级数发散. $\blacksquare$

---

## 10.1-2-7

讨论 $\sum_{n=1}^\infty\cos^2\frac\pi n$ 的收敛性.

### 解答 10.1-2-7

通项 $\cos^2\frac\pi n\to1\ne0$. 由**定理 1.1 (收敛级数的必要条件)**, 级数发散. $\blacksquare$

---

## 10.1-2-8

讨论 $\sum_{n=1}^\infty\arctan\frac1{2n^2}$ 的收敛性.

### 解答 10.1-2-8

因 $0\le\arctan\frac1{2n^2}\le\frac1{2n^2}$, 且 $\sum\frac1{2n^2}$ 收敛, 故部分和单调递增且有上界. 由**基础知识: 级数收敛的定义**, 级数收敛. $\blacksquare$
