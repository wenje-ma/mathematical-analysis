# week55

> **定理 4.1 (贝塞尔不等式)**<br>$\frac{a_0^2}2+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right)\le\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\mathrm dx$, 特别地 $\sum a_n^2$ 与 $\sum b_n^2$ 均收敛.

> **定理 4.2 (封闭性方程/Parseval 等式)**<br>$\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\mathrm dx=\frac{a_0^2}2+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right)$.

---

## 13.4-1

证明 $\sum\frac{a_n}{n}$ 及 $\sum\frac{b_n}{n}$ 收敛.

### 解答 13.4-1

由**定理 4.1 (贝塞尔不等式)**, $\sum\left(a_n^2+b_n^2\right)< \infty$. 由柯西-施瓦茨不等式, $\sum\left|\frac{a_n}n\right|\le\left(\sum a_n^2\right)^{1/2}\left(\sum\frac1{n^2}\right)^{1/2}< \infty$. 故绝对收敛. $\blacksquare$

---

## 13.4-2

说明 $\frac{a_0}2+\sum\frac1{\ln n\cdot\ln\ln n}\cos nx$ 处处收敛但不是任何可积函数的傅里叶级数.

### 解答 13.4-2

收敛性: 由狄利克雷判别法. 不是傅里叶级数: 由**定理 4.1 (贝塞尔不等式)** 与 13.4-1, 必须 $\sum\frac{a_n}n$ 收敛, 但 $\sum\frac1{n\ln n\cdot\ln\ln n}$ 由积分判别法发散. $\blacksquare$

---

## 13.4-5

利用 $f\left(x\right)=x^2$ 的 Parseval 等式求 $\sum\frac1{n^4}$.

### 解答 13.4-5

由**定理 4.2 (封闭性方程/Parseval 等式)**, $\frac{2\pi^4}5=\frac{2\pi^4}9+16\sum\frac1{n^4}$, 得 $\sum\frac1{n^4}=\frac{\pi^4}{90}$. $\blacksquare$

---

## 13.4-7

利用 $f\left(x\right)=\left|x\right|$ 的 Parseval 等式求 $\sum\frac1{\left(2n-1\right)^4}$.

### 解答 13.4-7

由**定理 4.2 (封闭性方程/Parseval 等式)**, $\frac{2\pi^2}3=\frac{\pi^2}2+\frac{16}{\pi^2}\sum\frac1{\left(2n-1\right)^4}$, 得 $\sum\frac1{\left(2n-1\right)^4}=\frac{\pi^4}{96}$. $\blacksquare$
