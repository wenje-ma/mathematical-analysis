# week42

> **基础知识: 函数序列一致收敛的定义**<br>若对任意 $\varepsilon> 0$, 存在 $N$, 当 $n> N$ 时, 对一切 $x\in X$ 均有 $\left|f_n\left(x\right)-f\left(x\right)\right|< \varepsilon$, 则称 $\left\{f_n\right\}$ 在 $X$ 上一致收敛于 $f$.

> **定理 1.1 (M 判别法)**<br>若存在 $M_n> 0$, $M_n\to0$, 使 $\left|f_n\left(x\right)-f\left(x\right)\right|\le M_n$ 对一切 $x\in X$ 成立, 则 $\left\{f_n\right\}$ 在 $X$ 上一致收敛于 $f$.

> **定理 1.2 (极限函数的连续性)**<br>若 $\left\{f_n\right\}$ 在区间 $X$ 上一致收敛于 $f$, 且每个 $f_n$ 连续, 则 $f$ 在 $X$ 上连续.

---

## 11.1-1-1

讨论 $f_n\left(x\right)=\frac1{1+nx}$ 在 $\left(0,1\right)$ 上的一致收敛性.

### 解答 11.1-1-1

极限函数 $f\left(x\right)\equiv0$. 取 $x_n=\frac1n$, 则 $\left|f_n\left(x_n\right)\right|=\frac12\not\to0$. 由**基础知识: 函数序列一致收敛的定义**, 不一致收敛. $\blacksquare$

---

## 11.1-1-3

讨论 $f_n\left(x\right)=\frac{\sin\left(nx+n\right)}n$ 在 $\mathbb R$ 上的一致收敛性.

### 解答 11.1-1-3

极限函数 $f\left(x\right)\equiv0$. 又 $\left|f_n\left(x\right)\right|\le\frac1n=M_n$, $M_n\to0$. 由**定理 1.1 (M 判别法)**, 一致收敛. $\blacksquare$

---

## 11.1-1-5

讨论 $f_n\left(x\right)=nxe^{-nx^2}$ 在 $\left[0,1\right]$ 上的一致收敛性.

### 解答 11.1-1-5

极限函数 $f\left(x\right)\equiv0$. 取 $x_n=\frac1{\sqrt{2n}}$, 则 $\left|f_n\left(x_n\right)\right|=\sqrt{\frac n{2e}}\to+\infty$. 由**基础知识: 函数序列一致收敛的定义**, 不一致收敛. $\blacksquare$

---

## 11.1-2

设 $f_n$ 在 $\left(a,b\right)$ 内一致收敛于 $f$, 且 $\lim_{x\to x_0}f_n\left(x\right)$ 存在. 证明 $\lim_{x\to x_0}f\left(x\right)=\lim_{n\to\infty}\lim_{x\to x_0}f_n\left(x\right)$.

### 解答 11.1-2

记 $A_n=\lim_{x\to x_0}f_n\left(x\right)$. 由一致收敛性, $\left\{A_n\right\}$ 为柯西列, 设极限为 $A$. 再由三角不等式得 $\left|f\left(x\right)-A\right|< \varepsilon$. 故等式成立. $\blacksquare$

---

## 11.1-3

证明 $f_n\left(x\right)=\left(1+\frac xn\right)^n$ 在 $\left[0,+\infty\right)$ 上不一致收敛于 $e^x$.

### 解答 11.1-3

取 $x_n=n$, 则 $\left|f_n\left(x_n\right)-e^{x_n}\right|=e^n-2^n\to+\infty$. 由**基础知识: 函数序列一致收敛的定义**, 不一致收敛. $\blacksquare$

---

## 11.1-4

证明 $f_n\left(x\right)=\left(1+\frac xn\right)^n$ 在任一闭区间 $\left[0,A\right]$ 上一致收敛于 $e^x$.

### 解答 11.1-4

由不等式 $0\le e^x-\left(1+\frac xn\right)^n\le e^A\cdot\frac{A^2}{2n}=M_n$, $M_n\to0$. 由**定理 1.1 (M 判别法)**, 一致收敛. $\blacksquare$

---

## 11.1-5

设 $f$ 及 $f_n$ 均连续, $M_n=\max_{x\in\left[a,b\right]}\left|f_n\left(x\right)-f\left(x\right)\right|$. 证明: $f_n$ 在 $\left[a,b\right]$ 上一致收敛于 $f$ 当且仅当 $M_n\to0$.

### 解答 11.1-5

必要性: 由一致收敛性直接得 $M_n< \varepsilon$. 充分性: 由 $M_n\to0$, 对一切 $x$ 有 $\left|f_n\left(x\right)-f\left(x\right)\right|\le M_n< \varepsilon$. 由**基础知识: 函数序列一致收敛的定义**, 一致收敛. $\blacksquare$
