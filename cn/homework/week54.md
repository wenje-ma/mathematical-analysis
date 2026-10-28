# week54

> **定理 3.1 (狄利克雷收敛定理)**<br>设 $f\left(x\right)$ 以 $2\pi$ 为周期且逐段单调有界, 则其傅里叶级数在每点 $x$ 收敛于 $\frac{f\left(x+0\right)+f\left(x-0\right)}2$.

> **命题 (傅里叶系数)**<br>$a_n=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\cos nx\,\mathrm dx$, $b_n=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\sin nx\,\mathrm dx$.

> **定理 (封闭性方程)**<br>$\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\mathrm dx=\frac{a_0^2}2+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right)$.

---

## 13.3-1

证明: 当 $0< x< \pi$ 时 $1=\frac12+\frac2\pi\sum_{n=0}^\infty\frac{\sin\left(2n+1\right)x}{2n+1}$, 并推出 $\frac\pi4=\sum_{n=0}^\infty\frac{\left(-1\right)^n}{2n+1}$.

### 解答 13.3-1

由**命题 (傅里叶系数)**, $a_0=1$, $a_n=0$, $b_n=\frac{1-\left(-1\right)^n}{n\pi}$. 由**定理 3.1 (狄利克雷收敛定理)**, 连续点处等式成立. 取 $x=\frac\pi2$ 得 $\frac\pi4=\sum\frac{\left(-1\right)^n}{2n+1}$. $\blacksquare$

---

## 13.3-3

求 $f\left(x\right)=\left(\pi-\left|x\right|\right)^2$ 的傅里叶级数, 并求 $\sum\frac1{n^2}$ 与 $\sum\frac1{n^4}$.

### 解答 13.3-3

由**命题 (傅里叶系数)**, $a_0=\frac{2\pi^2}3$, $a_n=\frac4{n^2}$. 在 $x=0$ 处由**定理 3.1 (狄利克雷收敛定理)**, $\pi^2=\frac{\pi^2}3+4\sum\frac1{n^2}$, 得 $\sum\frac1{n^2}=\frac{\pi^2}6$. 由**定理 (封闭性方程)**, 得 $\sum\frac1{n^4}=\frac{\pi^4}{90}$. $\blacksquare$

---

## 13.3-4

利用 $f\left(x\right)=x^2$ ($|x|\le\pi$) 的傅里叶级数求 $\sum\frac{\left(-1\right)^{n+1}}{n^2}$ 及 $\sum\frac1{n^2}$.

### 解答 13.3-4

$x^2\sim\frac{\pi^2}3+4\sum\frac{\left(-1\right)^n}{n^2}\cos nx$. 取 $x=\pi$ 得 $\sum\frac1{n^2}=\frac{\pi^2}6$; 取 $x=0$ 得 $\sum\frac{\left(-1\right)^{n+1}}{n^2}=\frac{\pi^2}{12}$. $\blacksquare$
