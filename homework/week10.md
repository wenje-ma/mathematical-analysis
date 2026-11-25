# week10

> **定理 1.3 (不定积分的线性法则)**
> 
> 设 $y=f\left(x\right)$ 及 $y=g\left(x\right)$ 在某个区间中有原函数. 则 $\int\left[af\left(x\right)+bg\left(x\right)\right]\mathrm{d}x=a\int{}f\left(x\right)\,\mathrm{d}x+b\int{}g\left(x\right)\,\mathrm{d}x$, 其中 $a,b$ 是两个任意常数.

> **定理 2.1 (第一换元法则)**
> 
> 设 $F'\left(u\right)=f\left(u\right)$, 且 $u=\varphi\left(x\right)$ 可导, 则 $\int{}f\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm{d}x=F\left(\varphi\left(x\right)\right)+C$.

> **定理 2.2 (第二换元法则)**
> 
> 设 $x=\varphi\left(t\right)$ 可导且有反函数, 又设 $\int{}f\left(\varphi\left(t\right)\right)\varphi'\left(t\right)\,\mathrm{d}t=G\left(t\right)+C$, 则 $\int{}f\left(x\right)\,\mathrm{d}x=G\left(\varphi^{-1}\left(x\right)\right)+C$.

## 4.1-2

证明: $\int\frac{\mathrm{d}x}{x^2+a^2}=\frac1a\arctan\frac{x}a+C$ ($a>0$).

### 解答 4.1-2

对右端求导:

$$
\left(\frac1a\arctan\frac{x}a\right)'=\frac1a\cdot\frac1{1+\left(x/a\right)^2}\cdot\frac1a=\frac1{a^2+x^2}.
$$

由原函数与不定积分的定义, 右端即为被积函数的一个原函数. 故 $\int\frac{\mathrm{d}x}{x^2+a^2}=\frac1a\arctan\frac{x}a+C$.

$\blacksquare$

## 4.1-4

证明: $\int\frac{\mathrm{d}x}{\sqrt{a^2-x^2}}=\arcsin\frac{x}a+C$ ($a>0$).

### 解答 4.1-4

对右端求导:

$$
\left(\arcsin\frac{x}a\right)'=\frac1{\sqrt{1-\left(x/a\right)^2}}\cdot\frac1a=\frac1{\sqrt{a^2-x^2}}.
$$

由原函数与不定积分的定义, 右端即为被积函数的一个原函数. 故 $\int\frac{\mathrm{d}x}{\sqrt{a^2-x^2}}=\arcsin\frac{x}a+C$.

$\blacksquare$

## 4.2-1-2

求不定积分 $\int\sqrt{2x+3}\,\mathrm{d}x$.

### 解答 4.2-1-2

令 $u=2x+3$, 则 $\mathrm{d}u=2\mathrm{d}x$. 由**定理 2.1 (第一换元法则)**,

$$
\int\sqrt{2x+3}\,\mathrm{d}x=\frac12\int{}u^{1/2}\,\mathrm{d}u=\frac13\left(2x+3\right)^{3/2}+C.
$$

$\blacksquare$

## 4.2-1-4

求不定积分 $\int\frac{\mathrm{d}x}{\left(x-1\right)^5}$.

### 解答 4.2-1-4

令 $u=x-1$. 由**定理 2.1 (第一换元法则)**,

$$
\int\frac{\mathrm{d}x}{\left(x-1\right)^5}=\int{}u^{-5}\,\mathrm{d}u=-\frac1{4\left(x-1\right)^4}+C.
$$

$\blacksquare$

## 4.2-1-6

求不定积分 $\int\mathrm{sh}\,x\,\mathrm{d}x$.

### 解答 4.2-1-6

由 $\left(\mathrm{ch}\,x\right)'=\mathrm{sh}\,x$, $\int\mathrm{sh}\,x\,\mathrm{d}x=\mathrm{ch}\,x+C$.

$\blacksquare$

## 4.2-1-8

求不定积分 $\int\frac{\mathrm{d}x}{a^2+b^2x^2}$ ($a>0$, $b>0$).

### 解答 4.2-1-8

变形: $\frac1{a^2+b^2x^2}=\frac1{a^2}\cdot\frac1{1+\left(\frac{bx}{a}\right)^2}$. 令 $u=\frac{bx}{a}$. 由**定理 2.1 (第一换元法则)**,

$$
\int\frac{\mathrm{d}x}{a^2+b^2x^2}=\frac1{ab}\arctan\frac{bx}{a}+C.
$$

$\blacksquare$

## 4.2-1-10

求不定积分 $\int\frac{\mathrm{d}x}{\sin{}x+\cos{}x}$.

### 解答 4.2-1-10

利用 $\sin{}x+\cos{}x=\sqrt2\sin\left(x+\frac\pi4\right)$. 令 $u=x+\frac\pi4$. 由**定理 2.1 (第一换元法则)**,

$$
\int\frac{\mathrm{d}x}{\sin{}x+\cos{}x}=\frac1{\sqrt2}\int\frac{\mathrm{d}u}{\sin{}u}=\frac1{\sqrt2}\ln\left|\csc{}u-\cot{}u\right|+C.
$$

$\blacksquare$

## 4.2-2-1

求不定积分 $\int\sqrt{a^2-x^2}\,\mathrm{d}x$ ($a>0$).

### 解答 4.2-2-1

令 $x=a\sin{}t$. 由**定理 2.2 (第二换元法则)**,

$$
\int\sqrt{a^2-x^2}\,\mathrm{d}x=a^2\int\cos^2t\,\mathrm{d}t=\frac{a^2}2\left(t+\sin{}t\cos{}t\right)+C.
$$

代回 $t=\arcsin\frac{x}a$, 得

$$
\int\sqrt{a^2-x^2}\,\mathrm{d}x=\frac{a^2}2\arcsin\frac{x}a+\frac{x}2\sqrt{a^2-x^2}+C.
$$

$\blacksquare$

## 4.2-2-3

求不定积分 $\int\frac{\mathrm{d}x}{\sqrt{x^2+a^2}}$ ($a>0$).

### 解答 4.2-2-3

令 $x=a\tan{}t$. 由**定理 2.2 (第二换元法则)**,

$$
\int\frac{\mathrm{d}x}{\sqrt{x^2+a^2}}=\int\sec{}t\,\mathrm{d}t=\ln\left|\sec{}t+\tan{}t\right|+C.
$$

代回得

$$
\int\frac{\mathrm{d}x}{\sqrt{x^2+a^2}}=\ln\left(x+\sqrt{x^2+a^2}\right)+C'.
$$

$\blacksquare$

## 4.2-2-5

求不定积分 $\int\sqrt{x^2-a^2}\,\mathrm{d}x$ ($a>0$).

### 解答 4.2-2-5

令 $x=a\sec{}t$. 由**定理 2.2 (第二换元法则)**,

$$
\int\sqrt{x^2-a^2}\,\mathrm{d}x=a^2\int\left(\sec^3t-\sec{}t\right)\,\mathrm{d}t.
$$

由分部积分可得 $\int\sec^3t\,\mathrm{d}t=\frac12\left(\sec{}t\tan{}t+\ln\left|\sec{}t+\tan{}t\right|\right)+C$. 故

$$
\int\sqrt{x^2-a^2}\,\mathrm{d}x=\frac{x}2\sqrt{x^2-a^2}-\frac{a^2}2\ln\left|x+\sqrt{x^2-a^2}\right|+C.
$$

$\blacksquare$

## 4.2-2-7

求不定积分 $\int\frac{\mathrm{d}x}{x\sqrt{a^2-x^2}}$ ($a>0$).

### 解答 4.2-2-7

令 $x=a\sin{}t$. 由**定理 2.2 (第二换元法则)**,

$$
\int\frac{\mathrm{d}x}{x\sqrt{a^2-x^2}}=\frac1a\int\frac{\mathrm{d}t}{\sin{}t}=\frac1a\ln\left|\csc{}t-\cot{}t\right|+C.
$$

代回得

$$
\int\frac{\mathrm{d}x}{x\sqrt{a^2-x^2}}=\frac1a\ln\left|\frac{a-\sqrt{a^2-x^2}}x\right|+C.
$$

$\blacksquare$

## 4.2-2-9

求不定积分 $\int\sqrt{7+x-x^2}\,\mathrm{d}x$.

### 解答 4.2-2-9

配方: $7+x-x^2=\frac{29}4-\left(x-\frac12\right)^2$. 令 $u=x-\frac12$. 由**定理 2.1 (第一换元法则)** 及 4.2-2-1 的结果,

$$
\int\sqrt{7+x-x^2}\,\mathrm{d}x=\frac{29}8\arcsin\frac{2x-1}{\sqrt{29}}+\frac{2x-1}4\sqrt{7+x-x^2}+C.
$$

$\blacksquare$

## 4.2-2-11

求不定积分 $\int\frac{\mathrm{d}x}{x^2\sqrt{x^2+a^2}}$ ($a>0$).

### 解答 4.2-2-11

令 $x=a\tan{}t$. 由**定理 2.2 (第二换元法则)**,

$$
\int\frac{\mathrm{d}x}{x^2\sqrt{x^2+a^2}}=\frac1{a^2}\int\frac{\cos{}t}{\sin^2t}\,\mathrm{d}t.
$$

令 $u=\sin{}t$, 则 $\frac1{a^2}\int\frac{\mathrm{d}u}{u^2}=-\frac1{a^2u}+C$. 代回 $u=\frac{x}{\sqrt{x^2+a^2}}$, 得

$$
\int\frac{\mathrm{d}x}{x^2\sqrt{x^2+a^2}}=-\frac{\sqrt{x^2+a^2}}{a^2x}+C.
$$

$\blacksquare$

## 4.3-1-11

求不定积分 $\int{}x\csc^2x\,\mathrm{d}x$.

### 解答 4.3-1-11

令 $u=x$, $\mathrm{d}v=\csc^2x\,\mathrm{d}x$, 则 $\mathrm{d}u=\mathrm{d}x$, $v=-\cot{}x$. 由**定理 3.1 (分部积分公式)**,

$$
\int{}x\csc^2x\,\mathrm{d}x=-x\cot{}x+\int\cot{}x\,\mathrm{d}x=-x\cot{}x+\ln\left|\sin{}x\right|+C.
$$

$\blacksquare$

## 4.3-1-13

求不定积分 $\int\sqrt{1+9x^2}\,\mathrm{d}x$.

### 解答 4.3-1-13

令 $u=\sqrt{1+9x^2}$, $\mathrm{d}v=\mathrm{d}x$. 由**定理 3.1 (分部积分公式)**,

$$
\int\sqrt{1+9x^2}\,\mathrm{d}x=x\sqrt{1+9x^2}-\int\frac{9x^2}{\sqrt{1+9x^2}}\,\mathrm{d}x.
$$

将被积函数变形: $\frac{9x^2}{\sqrt{1+9x^2}}=\sqrt{1+9x^2}-\frac1{\sqrt{1+9x^2}}$. 代入得

$$
2\int\sqrt{1+9x^2}\,\mathrm{d}x=x\sqrt{1+9x^2}+\int\frac{\mathrm{d}x}{\sqrt{1+9x^2}}.
$$

而 $\int\frac{\mathrm{d}x}{\sqrt{1+9x^2}}=\frac13\ln\left(3x+\sqrt{1+9x^2}\right)+C$. 故

$$
\int\sqrt{1+9x^2}\,\mathrm{d}x=\frac{x}2\sqrt{1+9x^2}+\frac16\ln\left(3x+\sqrt{1+9x^2}\right)+C.
$$

$\blacksquare$

## 4.3-1-14

求不定积分 $\int\sec^3x\,\mathrm{d}x$.

### 解答 4.3-1-14

令 $u=\sec{}x$, $\mathrm{d}v=\sec^2x\,\mathrm{d}x$. 由**定理 3.1 (分部积分公式)**,

$$
\int\sec^3x\,\mathrm{d}x=\sec{}x\tan{}x-\int\sec{}x\tan^2x\,\mathrm{d}x.
$$

利用 $\tan^2x=\sec^2x-1$,

$$
\int\sec^3x\,\mathrm{d}x=\sec{}x\tan{}x-\int\sec^3x\,\mathrm{d}x+\int\sec{}x\,\mathrm{d}x.
$$

移项得 $2\int\sec^3x\,\mathrm{d}x=\sec{}x\tan{}x+\int\sec{}x\,\mathrm{d}x$. 而 $\int\sec{}x\,\mathrm{d}x=\ln\left|\sec{}x+\tan{}x\right|+C$. 故

$$
\int\sec^3x\,\mathrm{d}x=\frac12\left(\sec{}x\tan{}x+\ln\left|\sec{}x+\tan{}x\right|\right)+C.
$$

$\blacksquare$

## 4.4-2

求不定积分 $\int\frac{x^3}{x^2+x-6}\,\mathrm{d}x$.

### 解答 4.4-2

先做多项式除法: $\frac{x^3}{x^2+x-6}=x-1+\frac{7x-6}{x^2+x-6}$. 分解分母: $x^2+x-6=\left(x+3\right)\left(x-2\right)$. 由**定理 4.1 (有理函数的分解)**, 设 $\frac{7x-6}{\left(x+3\right)\left(x-2\right)}=\frac{A}{x+3}+\frac{B}{x-2}$. 解得 $A=\frac{27}5$, $B=\frac85$. 故

$$
\int\frac{x^3}{x^2+x-6}\,\mathrm{d}x=\frac{x^2}2-x+\frac{27}5\ln\left|x+3\right|+\frac85\ln\left|x-2\right|+C.
$$

$\blacksquare$
