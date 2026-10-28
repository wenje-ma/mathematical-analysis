# week40

> **定理 2.2 (比较判别法)**<br>设 $\sum a_n$ 与 $\sum b_n$ 为正项级数, 且存在 $N_0$ 使 $a_n\le b_n$ ($n\ge N_0$). 若 $\sum b_n$ 收敛, 则 $\sum a_n$ 收敛.

> **定理 3.2 (狄利克雷判别法)**<br>设 $\left\{b_n\right\}$ 单调趋于零, 且 $\sum a_n$ 的部分和序列有界, 则 $\sum a_nb_n$ 收敛.

> **定理 3.3 (阿贝尔判别法)**<br>设 $\left\{b_n\right\}$ 单调有界, 且 $\sum a_n$ 收敛, 则 $\sum a_nb_n$ 收敛.

---

## 10.3-2

证明: $\sum_{n=1}^\infty\frac{\cos nx}{n^p}$ ($0< x< 2\pi$) 当 $p> 1$ 时绝对收敛, 当 $0< p\le1$ 时条件收敛.

### 解答 10.3-2

(1) $p> 1$ 时, $\left|\frac{\cos nx}{n^p}\right|\le\frac1{n^p}$, 由**定理 2.2 (比较判别法)** 及 $p$ 级数收敛, 原级数绝对收敛.

(2) $0< p\le1$ 时, 由 $\left|\cos nx\right|\ge\cos^2nx=\frac{1+\cos2nx}{2}$, 得 $\frac{\left|\cos nx\right|}{n^p}\ge\frac1{2n^p}+\frac{\cos2nx}{2n^p}$. 因 $\sum\frac1{n^p}$ 发散, 故原级数不绝对收敛. 又 $\sum\cos nx$ 部分和有界, $\frac1{n^p}$ 单调趋于零, 由**定理 3.2 (狄利克雷判别法)**, 原级数收敛. 故条件收敛. $\blacksquare$

---

## 10.3-4

证明狄利克雷级数 $\sum\frac{a_n}{n^x}$ 的收敛域为半无限区间.

### 解答 10.3-4

若 $\sum\frac{a_n}{n^{x_0}}$ 收敛且 $x> x_0$, 则 $\frac{a_n}{n^x}=\frac{a_n}{n^{x_0}}\cdot\frac1{n^{x-x_0}}$, 其中 $\frac1{n^{x-x_0}}$ 单调有界. 由**定理 3.3 (阿贝尔判别法)**, $\sum\frac{a_n}{n^x}$ 收敛. 发散情形同理反证. $\blacksquare$

---

## 10.3-5

设 $h_n=\sum_{k=1}^n\frac1k$, $S_n=\sum_{k=1}^n\frac{\left(-1\right)^{k-1}}k$. (1) 证明 $S_{2n}=h_{2n}-h_n$; (2) 利用 $h_n-\ln n\to\gamma$ 证明 $S_{2n}\to\ln2$; (3) 证明 $\sum\frac{\left(-1\right)^{n-1}}n=\ln2$.

### 解答 10.3-5

(1) 直接计算: $S_{2n}=h_{2n}-2\cdot\frac12h_n=h_{2n}-h_n$.

(2) $S_{2n}=h_{2n}-h_n=\ln\left(2n\right)+\gamma-\ln n-\gamma+o\left(1\right)=\ln2+o\left(1\right)$.

(3) $S_{2n-1}=S_{2n}+\frac1{2n}\to\ln2$. 偶数项与奇数项部分和均趋于 $\ln2$, 故 $\sum\frac{\left(-1\right)^{n-1}}n=\ln2$. $\blacksquare$
