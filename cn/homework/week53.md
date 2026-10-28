# week53

> **命题 (傅里叶系数)**<br>以 $2\pi$ 为周期的可积函数 $f\left(x\right)$ 的傅里叶级数为 $f\left(x\right)\sim\frac{a_0}2+\sum_{n=1}^\infty\left(a_n\cos nx+b_n\sin nx\right)$, 其中 $a_n=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\cos nx\,\mathrm dx$, $b_n=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\sin nx\,\mathrm dx$.

---

## 13.2-1-1

求 $f\left(x\right)=x^2$ ($-\pi\le x\le\pi$) 的傅里叶级数.

### 解答 13.2-1-1

由**命题 (傅里叶系数)**, $a_0=\frac{2\pi^2}3$, $a_n=\frac{4\left(-1\right)^n}{n^2}$, $b_n=0$. 故 $x^2\sim\frac{\pi^2}3+4\sum_{n=1}^\infty\frac{\left(-1\right)^n}{n^2}\cos nx$. $\blacksquare$

---

## 13.2-1-3

求 $f\left(x\right)=\sin^4x$ 的傅里叶级数.

### 解答 13.2-1-3

三角恒等变换得 $\sin^4x=\frac38-\frac12\cos2x+\frac18\cos4x$. 由**命题 (傅里叶系数)** 直接读出系数. $\blacksquare$

---

## 13.2-1-5

求 $f\left(x\right)=\begin{cases}0,&-\pi\le x< 0\\ x,&0\le x\le\pi\end{cases}$ 的傅里叶级数.

### 解答 13.2-1-5

由**命题 (傅里叶系数)**, $a_0=\frac\pi2$, $a_n=\frac{\left(-1\right)^n-1}{n^2\pi}$, $b_n=\frac{\left(-1\right)^{n+1}}n$. 故 $f\left(x\right)\sim\frac\pi4-\frac2\pi\sum_{k=0}^\infty\frac{\cos\left(2k+1\right)x}{\left(2k+1\right)^2}+\sum_{n=1}^\infty\frac{\left(-1\right)^{n+1}}n\sin nx$. $\blacksquare$

---

## 13.2-7

证明: 若 $f\left(x+\pi\right)=f\left(x\right)$, 则 $a_{2n-1}=b_{2n-1}=0$; 若 $f\left(x+\pi\right)=-f\left(x\right)$, 则 $a_{2n}=b_{2n}=0$.

### 解答 13.2-7

拆积分并作代换 $x=t-\pi$, 利用 $\cos\left(n\left(t-\pi\right)\right)=\left(-1\right)^n\cos nt$. 条件 (i) 时 $\left(-1\right)^n+1=0$ ($n$ 奇); 条件 (ii) 时 $1-\left(-1\right)^n=0$ ($n$ 偶). $\blacksquare$
