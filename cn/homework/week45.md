# week45

> **基础知识: 基本展开式**<br>$e^x=\sum_{n=0}^\infty\frac{x^n}{n!}$; $\ln\left(1+x\right)=\sum_{n=1}^\infty\frac{\left(-1\right)^{n-1}x^n}{n}$; $\cos x=\sum_{n=0}^\infty\frac{\left(-1\right)^nx^{2n}}{\left(2n\right)!}$.

> **定理 4.1 (泰勒级数)**<br>若 $f\left(x\right)$ 可展开为幂级数 $\sum a_n\left(x-x_0\right)^n$, 则 $a_n=\frac{f^{\left(n\right)}\left(x_0\right)}{n!}$, 展开唯一.

---

## 11.4-1-3

求 $f\left(x\right)=e^x$ 在 $x_0=3$ 处的幂级数展开式.

### 解答 11.4-1-3

令 $t=x-3$, 由**基础知识: 基本展开式**, $e^x=e^3\sum_{n=0}^\infty\frac{\left(x-3\right)^n}{n!}$. 由**定理 4.1 (泰勒级数)**, 此即泰勒展开式. $\blacksquare$

---

## 11.4-1-4

求 $f\left(x\right)=\ln x$ 在 $x_0=2$ 处的幂级数展开式.

### 解答 11.4-1-4

$\ln x=\ln2+\ln\left(1+\frac{x-2}2\right)$. 由**基础知识: 基本展开式**, $\ln x=\ln2+\sum_{n=1}^\infty\frac{\left(-1\right)^{n-1}}{n\cdot2^n}\left(x-2\right)^n$, $0< x< 4$. $\blacksquare$

---

## 11.4-1-5

求 $f\left(x\right)=\cos^2x$ 在 $x_0=0$ 处的幂级数展开式.

### 解答 11.4-1-5

由半角公式 $\cos^2x=\frac{1+\cos2x}2$. 由**基础知识: 基本展开式**, $\cos^2x=\frac12+\sum_{n=0}^\infty\frac{\left(-1\right)^n2^{2n-1}}{\left(2n\right)!}x^{2n}$. $\blacksquare$

---

## 11.4-2

证明 $\sum_{n=0}^\infty\frac{x^n}{\left(n+1\right)!}=\frac1x\left(e^x-1\right)$, 并推出 $\sum_{n=1}^\infty\frac n{\left(n+1\right)!}=1$.

### 解答 11.4-2

由**基础知识: 基本展开式**, $e^x-1=x\sum_{n=0}^\infty\frac{x^n}{\left(n+1\right)!}$. 两边除以 $x$ 即得第一式. 对 $x$ 求导, 令 $x=1$, 得 $\sum_{n=1}^\infty\frac n{\left(n+1\right)!}=1$. $\blacksquare$

---

## 11.4-3

证明 $\sum_{n=1}^\infty\frac n{\left(n+2\right)!}=3-e$.

### 解答 11.4-3

改写 $\frac n{\left(n+2\right)!}=\frac1{\left(n+1\right)!}-\frac2{\left(n+2\right)!}$. 利用 $e=\sum_{m=0}^\infty\frac1{m!}$, 计算得 $3-e$. $\blacksquare$
