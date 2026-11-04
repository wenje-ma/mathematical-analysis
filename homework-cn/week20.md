# week20

> **定理 1.3 (不定积分的线性法则)**
> 
> 设 $y=f\left(x\right)$ 及 $y=g\left(x\right)$ 在某个区间中有原函数. 则 $\int\left[af\left(x\right)+bg\left(x\right)\right]\mathrm dx=a\int f\left(x\right)\,\mathrm dx+b\int g\left(x\right)\,\mathrm dx$, 其中 $a,b$ 是两个任意常数.

> **定理 2.1 (第一换元法则)**
> 
> 设 $F'\left(u\right)=f\left(u\right)$, 且 $u=\varphi\left(x\right)$ 可导, 则 $\int f\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm dx=F\left(\varphi\left(x\right)\right)+C$.

> **定理 2.2 (第二换元法则)**
> 
> 设 $x=\varphi\left(t\right)$ 可导且有反函数, 又设 $\int f\left(\varphi\left(t\right)\right)\varphi'\left(t\right)\,\mathrm dt=G\left(t\right)+C$, 则 $\int f\left(x\right)\,\mathrm dx=G\left(\varphi^{-1}\left(x\right)\right)+C$.

## 4.1-1-6

求不定积分 $\int\left(3^x-4^{-x}\right)^2\,\mathrm dx$.

### 解答 4.1-1-6

展开被积函数: $\left(3^x-4^{-x}\right)^2=9^x-2\left(\frac34\right)^x+16^{-x}$. 由**定理 1.3 (不定积分的线性法则)** 及 $\int a^x\,\mathrm dx=\frac{a^x}{\ln a}+C$,

$$
\int\left(3^x-4^{-x}\right)^2\,\mathrm dx=\frac{9^x}{\ln9}-2\cdot\frac{\left(3/4\right)^x}{\ln\left(3/4\right)}-\frac{16^{-x}}{\ln16}+C.
$$

$\blacksquare$

## 4.1-1-8

求不定积分 $\int\frac{x^2}{1+x^2}\,\mathrm dx$.

### 解答 4.1-1-8

将被积函数变形: $\frac{x^2}{1+x^2}=1-\frac1{1+x^2}$. 由**定理 1.3 (不定积分的线性法则)**,

$$
\int\frac{x^2}{1+x^2}\,\mathrm dx=x-\arctan x+C.
$$

$\blacksquare$

## 4.1-1-10

求不定积分 $\int\left(a\,\mathrm{sh}\,x+b\,\mathrm{ch}\,x\right)\,\mathrm dx$.

### 解答 4.1-1-10

由 $\left(\mathrm{sh}\,x\right)'=\mathrm{ch}\,x$, $\left(\mathrm{ch}\,x\right)'=\mathrm{sh}\,x$, 及**定理 1.3 (不定积分的线性法则)**,

$$
\int\left(a\,\mathrm{sh}\,x+b\,\mathrm{ch}\,x\right)\,\mathrm dx=a\,\mathrm{ch}\,x+b\,\mathrm{sh}\,x+C.
$$

$\blacksquare$

## 4.1-1-11

求不定积分 $\int\frac1{\sin^2x\cos^2x}\,\mathrm dx$.

### 解答 4.1-1-11

利用 $1=\sin^2x+\cos^2x$, $\frac1{\sin^2x\cos^2x}=\sec^2x+\csc^2x$. 由**定理 1.3 (不定积分的线性法则)**,

$$
\int\frac1{\sin^2x\cos^2x}\,\mathrm dx=\tan x-\cot x+C.
$$

$\blacksquare$

## 4.1-1-12

求不定积分 $\int\sin^2\frac x2\,\mathrm dx$.

### 解答 4.1-1-12

利用半角公式 $\sin^2\frac x2=\frac{1-\cos x}2$, 由**定理 1.3 (不定积分的线性法则)**,

$$
\int\sin^2\frac x2\,\mathrm dx=\frac x2-\frac{\sin x}2+C.
$$

$\blacksquare$

## 4.1-2

证明: $\int\frac{\mathrm dx}{x^2+a^2}=\frac1a\arctan\frac xa+C$ ($a> 0$).

### 解答 4.1-2

对右端求导:

$$
\left(\frac1a\arctan\frac xa\right)'=\frac1a\cdot\frac1{1+\left(x/a\right)^2}\cdot\frac1a=\frac1{a^2+x^2}.
$$

由原函数与不定积分的定义, 右端即为被积函数的一个原函数. 故 $\int\frac{\mathrm dx}{x^2+a^2}=\frac1a\arctan\frac xa+C$. $\blacksquare$

## 4.1-4

证明: $\int\frac{\mathrm dx}{\sqrt{a^2-x^2}}=\arcsin\frac xa+C$ ($a> 0$).

### 解答 4.1-4

对右端求导:

$$
\left(\arcsin\frac xa\right)'=\frac1{\sqrt{1-\left(x/a\right)^2}}\cdot\frac1a=\frac1{\sqrt{a^2-x^2}}.
$$

由原函数与不定积分的定义, 右端即为被积函数的一个原函数. 故 $\int\frac{\mathrm dx}{\sqrt{a^2-x^2}}=\arcsin\frac xa+C$. $\blacksquare$

## 4.2-1-2

求不定积分 $\int\sqrt{2x+3}\,\mathrm dx$.

### 解答 4.2-1-2

令 $u=2x+3$, 则 $\mathrm du=2\mathrm dx$. 由**定理 2.1 (第一换元法则)**,

$$
\int\sqrt{2x+3}\,\mathrm dx=\frac12\int u^{1/2}\,\mathrm du=\frac13\left(2x+3\right)^{3/2}+C.
$$

$\blacksquare$

## 4.2-1-4

求不定积分 $\int\frac{\mathrm dx}{\left(x-1\right)^5}$.

### 解答 4.2-1-4

令 $u=x-1$. 由**定理 2.1 (第一换元法则)**,

$$
\int\frac{\mathrm dx}{\left(x-1\right)^5}=\int u^{-5}\,\mathrm du=-\frac1{4\left(x-1\right)^4}+C.
$$

$\blacksquare$

## 4.2-1-6

求不定积分 $\int\mathrm{sh}\,x\,\mathrm dx$.

### 解答 4.2-1-6

由 $\left(\mathrm{ch}\,x\right)'=\mathrm{sh}\,x$, $\int\mathrm{sh}\,x\,\mathrm dx=\mathrm{ch}\,x+C$. $\blacksquare$

## 4.2-1-8

求不定积分 $\int\frac{\mathrm dx}{a^2+b^2x^2}$ ($a> 0$, $b> 0$).

### 解答 4.2-1-8

变形: $\frac1{a^2+b^2x^2}=\frac1{a^2}\cdot\frac1{1+\left(\frac{bx}{a}\right)^2}$. 令 $u=\frac{bx}{a}$. 由**定理 2.1 (第一换元法则)**,

$$
\int\frac{\mathrm dx}{a^2+b^2x^2}=\frac1{ab}\arctan\frac{bx}{a}+C.
$$

$\blacksquare$

## 4.2-1-10

求不定积分 $\int\frac{\mathrm dx}{\sin x+\cos x}$.

### 解答 4.2-1-10

利用 $\sin x+\cos x=\sqrt2\sin\left(x+\frac\pi4\right)$. 令 $u=x+\frac\pi4$. 由**定理 2.1 (第一换元法则)**,

$$
\int\frac{\mathrm dx}{\sin x+\cos x}=\frac1{\sqrt2}\int\frac{\mathrm du}{\sin u}=\frac1{\sqrt2}\ln\left|\csc u-\cot u\right|+C.
$$

$\blacksquare$

## 4.2-2-1

求不定积分 $\int\sqrt{a^2-x^2}\,\mathrm dx$ ($a> 0$).

### 解答 4.2-2-1

令 $x=a\sin t$. 由**定理 2.2 (第二换元法则)**,

$$
\int\sqrt{a^2-x^2}\,\mathrm dx=a^2\int\cos^2t\,\mathrm dt=\frac{a^2}2\left(t+\sin t\cos t\right)+C.
$$

代回 $t=\arcsin\frac xa$, 得

$$
\int\sqrt{a^2-x^2}\,\mathrm dx=\frac{a^2}2\arcsin\frac xa+\frac x2\sqrt{a^2-x^2}+C.
$$

$\blacksquare$

## 4.2-2-3

求不定积分 $\int\frac{\mathrm dx}{\sqrt{x^2+a^2}}$ ($a> 0$).

### 解答 4.2-2-3

令 $x=a\tan t$. 由**定理 2.2 (第二换元法则)**,

$$
\int\frac{\mathrm dx}{\sqrt{x^2+a^2}}=\int\sec t\,\mathrm dt=\ln\left|\sec t+\tan t\right|+C.
$$

代回得

$$
\int\frac{\mathrm dx}{\sqrt{x^2+a^2}}=\ln\left(x+\sqrt{x^2+a^2}\right)+C'.
$$

$\blacksquare$

## 4.2-2-5

求不定积分 $\int\sqrt{x^2-a^2}\,\mathrm dx$ ($a> 0$).

### 解答 4.2-2-5

令 $x=a\sec t$. 由**定理 2.2 (第二换元法则)**,

$$
\int\sqrt{x^2-a^2}\,\mathrm dx=a^2\int\left(\sec^3t-\sec t\right)\,\mathrm dt.
$$

由分部积分可得 $\int\sec^3t\,\mathrm dt=\frac12\left(\sec t\tan t+\ln\left|\sec t+\tan t\right|\right)+C$. 故

$$
\int\sqrt{x^2-a^2}\,\mathrm dx=\frac x2\sqrt{x^2-a^2}-\frac{a^2}2\ln\left|x+\sqrt{x^2-a^2}\right|+C.
$$

$\blacksquare$
