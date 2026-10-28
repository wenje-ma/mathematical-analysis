# week22

> **定理 5.1 (三角有理式的积分法)**<br>三角函数的有理式 $R\left(\sin x,\cos x\right)$ 的不定积分, 总可通过万能代换 $t=\tan\frac x2$ 化为关于 $t$ 的有理函数的不定积分. 此时 $\sin x=\frac{2t}{1+t^2}$, $\cos x=\frac{1-t^2}{1+t^2}$, $\mathrm dx=\frac{2\mathrm dt}{1+t^2}$.

---

## 4.5-1-1

求不定积分 $\int\frac{\mathrm dx}{2+\sin x}$.

### 解答 4.5-1-1

由**定理 5.1 (三角有理式的积分法)**, 令 $t=\tan\frac x2$, 则

$$
\int\frac{\mathrm dx}{2+\sin x}=\int\frac{\mathrm dt}{t^2+t+1}=\frac2{\sqrt3}\arctan\frac{2\tan\left(x/2\right)+1}{\sqrt3}+C.
$$

$\blacksquare$

---

## 4.5-1-3

求不定积分 $\int\cos^2x\,\mathrm dx$.

### 解答 4.5-1-3

利用半角公式 $\cos^2x=\frac{1+\cos2x}2$,

$$
\int\cos^2x\,\mathrm dx=\frac x2+\frac{\sin2x}4+C.
$$

$\blacksquare$

---

## 4.5-1-5

求不定积分 $\int\cot^2x\,\mathrm dx$.

### 解答 4.5-1-5

利用 $\cot^2x=\csc^2x-1$,

$$
\int\cot^2x\,\mathrm dx=-\cot x-x+C.
$$

$\blacksquare$

---

## 4.5-1-7

求不定积分 $\int\frac{\mathrm dx}{\sin x+2\cos x}$.

### 解答 4.5-1-7

将分母写成 $\sqrt5\sin\left(x+\varphi\right)$, 其中 $\varphi=\arctan2$. 故

$$
\int\frac{\mathrm dx}{\sin x+2\cos x}=\frac1{\sqrt5}\ln\left|\csc\left(x+\varphi\right)-\cot\left(x+\varphi\right)\right|+C.
$$

$\blacksquare$

---

## 4.5-1-9

求不定积分 $\int\sin^2x\cos^2x\,\mathrm dx$.

### 解答 4.5-1-9

利用 $\sin^2x\cos^2x=\frac{1-\cos4x}8$,

$$
\int\sin^2x\cos^2x\,\mathrm dx=\frac x8-\frac{\sin4x}{32}+C.
$$

$\blacksquare$

---

## 4.5-1-11

求不定积分 $\int\frac{\mathrm dx}{x+2}$.

### 解答 4.5-1-11

$$
\int\frac{\mathrm dx}{x+2}=\ln\left|x+2\right|+C.
$$

$\blacksquare$

---

## 4.5-1-13

求不定积分 $\int\frac{\mathrm dx}{e^x-1}$.

### 解答 4.5-1-13

令 $t=e^x$. 则

$$
\int\frac{\mathrm dx}{e^x-1}=\int\left(\frac1{t-1}-\frac1t\right)\mathrm dt=\ln\left|1-e^{-x}\right|+C.
$$

$\blacksquare$

---

## 4.5-2

设 $R\left(X,Y\right)$ 是关于变元 $X$ 与 $Y$ 的有理式, 证明 $\int R\left(\sin^2x,\cos^2x\right)\,\mathrm dx$ 可通过变换 $t=\tan x$ 有理化.

### 解答 4.5-2

令 $t=\tan x$, 则 $\mathrm dx=\frac{\mathrm dt}{1+t^2}$, $\sin^2x=\frac{t^2}{1+t^2}$, $\cos^2x=\frac1{1+t^2}$. 代入得

$$
R\left(\sin^2x,\cos^2x\right)\,\mathrm dx=R\left(\frac{t^2}{1+t^2},\frac1{1+t^2}\right)\cdot\frac{\mathrm dt}{1+t^2},
$$

右端是关于 $t$ 的有理函数. 故原积分可通过 $t=\tan x$ 有理化. $\blacksquare$
