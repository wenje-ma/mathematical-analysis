# week18

> **基础知识: 原函数与不定积分的定义**<br>设 $y=f\left(x\right)$ 定义在 $\left(a,b\right)$ 区间之中. 若 $F\left(x\right)$ 在 $\left(a,b\right)$ 中可微, 且 $F'\left(x\right)=f\left(x\right)$ 对一切 $x\in\left(a,b\right)$ 成立, 则称 $F$ 是 $f$ 的一个原函数. $f$ 的一切原函数 $F\left(x\right)+C$ 称作 $f$ 的不定积分, 记作 $\int f\left(x\right)\,\mathrm dx=F\left(x\right)+C$.

> **定理 1.3 (不定积分的线性法则)**<br>设 $y=f\left(x\right)$ 及 $y=g\left(x\right)$ 在某个区间中有原函数. 则 $\int\left[af\left(x\right)+bg\left(x\right)\right]\mathrm dx=a\int f\left(x\right)\,\mathrm dx+b\int g\left(x\right)\,\mathrm dx$, 其中 $a,b$ 是两个任意常数.

---

## 4.1-1-1

求不定积分 $\int\left(x^3+4\right)\,\mathrm dx$.

### 解答 4.1-1-1

由**定理 1.3 (不定积分的线性法则)**,

$$
\int\left(x^3+4\right)\,\mathrm dx=\int x^3\,\mathrm dx+4\int1\,\mathrm dx=\frac{x^4}4+4x+C.
$$

$\blacksquare$

---

## 4.1-1-4

求不定积分 $\int\tan^2x\,\mathrm dx$.

### 解答 4.1-1-4

利用三角恒等式 $\tan^2x=\sec^2x-1$, 由**定理 1.3 (不定积分的线性法则)**,

$$
\int\tan^2x\,\mathrm dx=\int\left(\sec^2x-1\right)\,\mathrm dx=\tan x-x+C.
$$

$\blacksquare$

---

## 4.1-1-6

求不定积分 $\int\left(3^x-4^{-x}\right)^2\,\mathrm dx$.

### 解答 4.1-1-6

展开被积函数: $\left(3^x-4^{-x}\right)^2=9^x-2\left(\frac34\right)^x+16^{-x}$. 由**定理 1.3 (不定积分的线性法则)** 及 $\int a^x\,\mathrm dx=\frac{a^x}{\ln a}+C$,

$$
\int\left(3^x-4^{-x}\right)^2\,\mathrm dx=\frac{9^x}{\ln9}-2\cdot\frac{\left(3/4\right)^x}{\ln\left(3/4\right)}-\frac{16^{-x}}{\ln16}+C.
$$

$\blacksquare$

---

## 4.1-1-8

求不定积分 $\int\frac{x^2}{1+x^2}\,\mathrm dx$.

### 解答 4.1-1-8

将被积函数变形: $\frac{x^2}{1+x^2}=1-\frac1{1+x^2}$. 由**定理 1.3 (不定积分的线性法则)**,

$$
\int\frac{x^2}{1+x^2}\,\mathrm dx=x-\arctan x+C.
$$

$\blacksquare$

---

## 4.1-1-10

求不定积分 $\int\left(a\,\mathrm{sh}\,x+b\,\mathrm{ch}\,x\right)\,\mathrm dx$.

### 解答 4.1-1-10

由 $\left(\mathrm{sh}\,x\right)'=\mathrm{ch}\,x$, $\left(\mathrm{ch}\,x\right)'=\mathrm{sh}\,x$, 及**定理 1.3 (不定积分的线性法则)**,

$$
\int\left(a\,\mathrm{sh}\,x+b\,\mathrm{ch}\,x\right)\,\mathrm dx=a\,\mathrm{ch}\,x+b\,\mathrm{sh}\,x+C.
$$

$\blacksquare$

---

## 4.1-1-11

求不定积分 $\int\frac1{\sin^2x\cos^2x}\,\mathrm dx$.

### 解答 4.1-1-11

利用 $1=\sin^2x+\cos^2x$, $\frac1{\sin^2x\cos^2x}=\sec^2x+\csc^2x$. 由**定理 1.3 (不定积分的线性法则)**,

$$
\int\frac1{\sin^2x\cos^2x}\,\mathrm dx=\tan x-\cot x+C.
$$

$\blacksquare$

---

## 4.1-1-12

求不定积分 $\int\sin^2\frac x2\,\mathrm dx$.

### 解答 4.1-1-12

利用半角公式 $\sin^2\frac x2=\frac{1-\cos x}2$, 由**定理 1.3 (不定积分的线性法则)**,

$$
\int\sin^2\frac x2\,\mathrm dx=\frac x2-\frac{\sin x}2+C.
$$

$\blacksquare$

---

## 4.1-2

证明: $\int\frac{\mathrm dx}{x^2+a^2}=\frac1a\arctan\frac xa+C$ ($a> 0$).

### 解答 4.1-2

对右端求导:

$$
\left(\frac1a\arctan\frac xa\right)'=\frac1a\cdot\frac1{1+\left(x/a\right)^2}\cdot\frac1a=\frac1{a^2+x^2}.
$$

由**基础知识: 原函数与不定积分的定义**, 右端即为被积函数的一个原函数. 故 $\int\frac{\mathrm dx}{x^2+a^2}=\frac1a\arctan\frac xa+C$. $\blacksquare$

---

## 4.1-4

证明: $\int\frac{\mathrm dx}{\sqrt{a^2-x^2}}=\arcsin\frac xa+C$ ($a> 0$).

### 解答 4.1-4

对右端求导:

$$
\left(\arcsin\frac xa\right)'=\frac1{\sqrt{1-\left(x/a\right)^2}}\cdot\frac1a=\frac1{\sqrt{a^2-x^2}}.
$$

由**基础知识: 原函数与不定积分的定义**, 右端即为被积函数的一个原函数. 故 $\int\frac{\mathrm dx}{\sqrt{a^2-x^2}}=\arcsin\frac xa+C$. $\blacksquare$
