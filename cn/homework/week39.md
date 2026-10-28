# week39

> **定理 2.2 (比较判别法)**<br>设 $\sum a_n$ 与 $\sum b_n$ 为正项级数, 且存在 $N_0$ 使 $a_n\le b_n$ ($n\ge N_0$). 若 $\sum b_n$ 收敛, 则 $\sum a_n$ 收敛; 若 $\sum a_n$ 发散, 则 $\sum b_n$ 发散.

> **定理 2.3 (比较判别法的极限形式)**<br>设 $\sum a_n$ 与 $\sum b_n$ 为正项级数, 且 $\lim_{n\to\infty}\frac{a_n}{b_n}=l$. 当 $0< l< +\infty$ 时两级数同敛散; 当 $l=0$ 且 $\sum b_n$ 收敛时 $\sum a_n$ 收敛; 当 $l=+\infty$ 且 $\sum b_n$ 发散时 $\sum a_n$ 发散.

> **定理 2.6 (达朗贝尔判别法)**<br>设 $\sum a_n$ 为正项级数. 若 $\lim_{n\to\infty}\frac{a_{n+1}}{a_n}=r$, 则当 $r< 1$ 时收敛, 当 $r> 1$ 时发散.

> **定理 2.9 (积分判别法)**<br>设 $f\left(x\right)$ 在 $\left[1,+\infty\right)$ 上正, 单调递减. 则 $\sum_{n=1}^\infty f\left(n\right)$ 与 $\int_1^{+\infty}f\left(x\right)\,\mathrm dx$ 同敛散.

---

## 10.2-1-15

讨论 $\sum_{n=1}^\infty\frac{\left(n!\right)^2}{\left(2n\right)!}$ 的收敛性.

### 解答 10.2-1-15

$\frac{a_{n+1}}{a_n}=\frac{n+1}{2\left(2n+1\right)}\to\frac14< 1$. 由**定理 2.6 (达朗贝尔判别法)**, 级数收敛. $\blacksquare$

---

## 10.2-1-18

讨论 $\sum_{n=3}^\infty\frac1{n\left(\ln\ln n\right)^q}$ ($q> 0$) 的收敛性.

### 解答 10.2-1-18

因 $\frac1{n\left(\ln\ln n\right)^q}> \frac1{n\ln n}$, 而 $\sum\frac1{n\ln n}$ 由**定理 2.9 (积分判别法)** 发散. 由**定理 2.2 (比较判别法)**, 原级数发散. $\blacksquare$

---

## 10.2-2

用积分判别法讨论 $\sum_{n=3}^\infty\frac1{n\ln^p n\left(\ln\ln n\right)^q}$ ($p> 0,q> 0$) 的收敛性.

### 解答 10.2-2

令 $t=\ln x$, 由**定理 2.9 (积分判别法)**, 原级数与 $\int_{\ln3}^{+\infty}\frac{\mathrm dt}{t^p\left(\ln t\right)^q}$ 同敛散.

(i) $p> 1$ 时收敛; (ii) $p< 1$ 时发散; (iii) $p=1,q> 1$ 时收敛; (iv) $p=1,q\le1$ 时发散. $\blacksquare$

---

## 10.2-6

设 $\lim_{n\to\infty}na_n=l\in\left(0,+\infty\right)$. 证明 $\sum a_n^2$ 收敛而 $\sum a_n$ 发散.

### 解答 10.2-6

由 $\lim_{n\to\infty}\frac{a_n}{1/n}=l\in\left(0,+\infty\right)$, 及**定理 2.3 (比较判别法的极限形式)**, $\sum a_n$ 与调和级数同发散. 又 $\lim_{n\to\infty}\frac{a_n^2}{1/n^2}=l^2\in\left(0,+\infty\right)$, 而 $\sum\frac1{n^2}$ 收敛, 故 $\sum a_n^2$ 收敛. $\blacksquare$

---

## 10.2-7

若 $\sum a_n^2$ 与 $\sum b_n^2$ 都收敛, 证明下列级数均收敛: $\sum\left|a_nb_n\right|$; $\sum\left(a_n+b_n\right)^2$; $\sum\frac{\left|a_n\right|}{n}$.

### 解答 10.2-7

(1) 由 $2\left|a_nb_n\right|\le a_n^2+b_n^2$, 及**定理 2.2 (比较判别法)**, $\sum\left|a_nb_n\right|$ 收敛.

(2) $\left(a_n+b_n\right)^2\le a_n^2+2\left|a_nb_n\right|+b_n^2$, 由 (1) 及比较判别法, 收敛.

(3) 由 $2\frac{\left|a_n\right|}{n}\le a_n^2+\frac1{n^2}$, 及比较判别法, 收敛. $\blacksquare$
