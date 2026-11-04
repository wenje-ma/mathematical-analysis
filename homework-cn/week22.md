# week22

> **定理 1.3 (连续的充要条件)**
> 
> 设 $y=f\left(x\right)$ 在 $x_0$ 点附近为有界函数. 则 $f$ 在 $x_0$ 点连续的充要条件是 $\omega_f\left(x_0\right)=0$.

> **定理 2.1 (第一换元法则)**
> 
> 设 $F'\left(u\right)=f\left(u\right)$, 且 $u=\varphi\left(x\right)$ 可导, 则 $\int f\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm dx=F\left(\varphi\left(x\right)\right)+C$.

> **定理 4.1 (有理函数的分解)**
> 
> 任何有理函数 $\frac{P\left(x\right)}{Q\left(x\right)}$ 都可以分解为一个多项式与若干部分分式之和, 其中每个部分分式形如 $\frac{A}{\left(x-a\right)^k}$ 或 $\frac{Bx+C}{\left(x^2+px+q\right)^m}$ ($p^2-4q< 0$).

> **定理 5.1 (三角有理式的积分法)**
> 
> 三角函数的有理式 $R\left(\sin x,\cos x\right)$ 的不定积分, 总可通过万能代换 $t=\tan\frac x2$ 化为关于 $t$ 的有理函数的不定积分. 此时 $\sin x=\frac{2t}{1+t^2}$, $\cos x=\frac{1-t^2}{1+t^2}$, $\mathrm dx=\frac{2\mathrm dt}{1+t^2}$.

## 4.4-12

求不定积分 $\int\frac{e^t}{e^{2t}+5e^t+6}\,\mathrm dt$.

### 解答 4.4-12

令 $u=e^t$. 积分化为 $\int\frac{\mathrm du}{\left(u+2\right)\left(u+3\right)}$. 由**定理 4.1 (有理函数的分解)**, $\frac1{\left(u+2\right)\left(u+3\right)}=\frac1{u+2}-\frac1{u+3}$. 故

$$
\int\frac{e^t}{e^{2t}+5e^t+6}\,\mathrm dt=\ln\frac{e^t+2}{e^t+3}+C.
$$

$\blacksquare$

## 4.4-14

求不定积分 $\int\frac{\mathrm dx}{\left(x^2+4\right)^2\left(x+1\right)}$.

### 解答 4.4-14

由**定理 4.1 (有理函数的分解)**, 设

$$
\frac1{\left(x^2+4\right)^2\left(x+1\right)}=\frac A{x+1}+\frac{Bx+C}{x^2+4}+\frac{Dx+E}{\left(x^2+4\right)^2}.
$$

解得 $A=\frac1{25}$, $B=-\frac1{25}$, $C=\frac1{25}$, $D=-\frac15$, $E=\frac15$. 合并各项得

$$
\int\frac{\mathrm dx}{\left(x^2+4\right)^2\left(x+1\right)}=\frac1{25}\ln\left|x+1\right|-\frac1{50}\ln\left(x^2+4\right)+\frac{13}{400}\arctan\frac x2+\frac{x+4}{40\left(x^2+4\right)}+C.
$$

$\blacksquare$

## 4.5-1-1

求不定积分 $\int\frac{\mathrm dx}{2+\sin x}$.

### 解答 4.5-1-1

由**定理 5.1 (三角有理式的积分法)**, 令 $t=\tan\frac x2$, 则

$$
\int\frac{\mathrm dx}{2+\sin x}=\int\frac{\mathrm dt}{t^2+t+1}=\frac2{\sqrt3}\arctan\frac{2\tan\left(x/2\right)+1}{\sqrt3}+C.
$$

$\blacksquare$

## 4.5-1-3

求不定积分 $\int\cos^2x\,\mathrm dx$.

### 解答 4.5-1-3

利用半角公式 $\cos^2x=\frac{1+\cos2x}2$,

$$
\int\cos^2x\,\mathrm dx=\frac x2+\frac{\sin2x}4+C.
$$

$\blacksquare$

## 4.5-1-5

求不定积分 $\int\cot^2x\,\mathrm dx$.

### 解答 4.5-1-5

利用 $\cot^2x=\csc^2x-1$,

$$
\int\cot^2x\,\mathrm dx=-\cot x-x+C.
$$

$\blacksquare$

## 4.5-1-7

求不定积分 $\int\frac{\mathrm dx}{\sin x+2\cos x}$.

### 解答 4.5-1-7

将分母写成 $\sqrt5\sin\left(x+\varphi\right)$, 其中 $\varphi=\arctan2$. 故

$$
\int\frac{\mathrm dx}{\sin x+2\cos x}=\frac1{\sqrt5}\ln\left|\csc\left(x+\varphi\right)-\cot\left(x+\varphi\right)\right|+C.
$$

$\blacksquare$

## 4.5-1-9

求不定积分 $\int\sin^2x\cos^2x\,\mathrm dx$.

### 解答 4.5-1-9

利用 $\sin^2x\cos^2x=\frac{1-\cos4x}8$,

$$
\int\sin^2x\cos^2x\,\mathrm dx=\frac x8-\frac{\sin4x}{32}+C.
$$

$\blacksquare$

## 4.5-1-11

求不定积分 $\int\frac{\mathrm dx}{x+2}$.

### 解答 4.5-1-11

$$
\int\frac{\mathrm dx}{x+2}=\ln\left|x+2\right|+C.
$$

$\blacksquare$

## 4.5-1-13

求不定积分 $\int\frac{\mathrm dx}{e^x-1}$.

### 解答 4.5-1-13

令 $t=e^x$. 则

$$
\int\frac{\mathrm dx}{e^x-1}=\int\left(\frac1{t-1}-\frac1t\right)\mathrm dt=\ln\left|1-e^{-x}\right|+C.
$$

$\blacksquare$

## 4.5-2

设 $R\left(X,Y\right)$ 是关于变元 $X$ 与 $Y$ 的有理式, 证明 $\int R\left(\sin^2x,\cos^2x\right)\,\mathrm dx$ 可通过变换 $t=\tan x$ 有理化.

### 解答 4.5-2

令 $t=\tan x$, 则 $\mathrm dx=\frac{\mathrm dt}{1+t^2}$, $\sin^2x=\frac{t^2}{1+t^2}$, $\cos^2x=\frac1{1+t^2}$. 代入得

$$
R\left(\sin^2x,\cos^2x\right)\,\mathrm dx=R\left(\frac{t^2}{1+t^2},\frac1{1+t^2}\right)\cdot\frac{\mathrm dt}{1+t^2},
$$

右端是关于 $t$ 的有理函数. 故原积分可通过 $t=\tan x$ 有理化. $\blacksquare$

## 5.1-4

设 $y=f\left(x\right)$ 及 $y=g\left(x\right)$ 为 $\left[a,b\right]$ 上的有界函数. 证明:

(1) $\sup_{\left[a,b\right]}\left\{f\left(x\right)+g\left(x\right)\right\}\le\sup_{\left[a,b\right]}f\left(x\right)+\sup_{\left[a,b\right]}g\left(x\right)$;

(2) $\inf_{\left[a,b\right]}\left\{f\left(x\right)+g\left(x\right)\right\}\ge\inf_{\left[a,b\right]}f\left(x\right)+\inf_{\left[a,b\right]}g\left(x\right)$.

### 解答 5.1-4

(1) 对任意 $x\in\left[a,b\right]$, $f\left(x\right)\le\sup f$, $g\left(x\right)\le\sup g$. 故 $f\left(x\right)+g\left(x\right)\le\sup f+\sup g$. 即 $\sup f+\sup g$ 是 $f+g$ 的一个上界. 由上确界与下确界的定义, 上确界是最小上界, 得 $\sup\left\{f+g\right\}\le\sup f+\sup g$.

(2) 同理, $f\left(x\right)+g\left(x\right)\ge\inf f+\inf g$, 故 $\inf\left\{f+g\right\}\ge\inf f+\inf g$. $\blacksquare$

## 5.1-5

证明: $\omega_f\left(I\right)=\sup\left\{\left|f\left(x_1\right)-f\left(x_2\right)\right|:x_1,x_2\in I\right\}$.

### 解答 5.1-5

记 $M=\sup\left\{f\left(x\right):x\in I\right\}$, $m=\inf\left\{f\left(x\right):x\in I\right\}$. 则 $\omega_f\left(I\right)=M-m$.

对任意 $x_1,x_2\in I$, $\left|f\left(x_1\right)-f\left(x_2\right)\right|\le M-m$. 故 $M-m$ 是该集合的一个上界.

另一方面, 对任意 $\varepsilon> 0$, 存在 $x_1,x_2\in I$ 使得 $f\left(x_1\right)> M-\frac\varepsilon2$, $f\left(x_2\right)< m+\frac\varepsilon2$. 于是 $\left|f\left(x_1\right)-f\left(x_2\right)\right|> M-m-\varepsilon$. 由上确界与下确界的定义, $\sup\left\{\left|f\left(x_1\right)-f\left(x_2\right)\right|\right\}\ge M-m$.

综合两方面, $\omega_f\left(I\right)=\sup\left\{\left|f\left(x_1\right)-f\left(x_2\right)\right|\right\}$. $\blacksquare$

## 5.1-6

设 $y=D\left(x\right)$ 为狄利克雷函数, 即 $D\left(x\right)=0$ ($x$ 为无理数), $D\left(x\right)=1$ ($x$ 为有理数). 证明: $D\left(x\right)$ 在任意区间中的振幅为 $1$, 且在每一点的振幅为 $1$.

### 解答 5.1-6

对任意区间 $I$, $I$ 中既有有理数又有无理数. 故 $\sup_{x\in I}D\left(x\right)=1$, $\inf_{x\in I}D\left(x\right)=0$. 因此 $\omega_D\left(I\right)=1$.

对任意点 $x_0$, 在 $x_0$ 的任意邻域内都既有有理数又有无理数. 故 $\omega_D\left(x_0\right)=1$. 由**定理 1.3 (连续的充要条件)**, $D\left(x\right)$ 在每一点都不连续. $\blacksquare$
