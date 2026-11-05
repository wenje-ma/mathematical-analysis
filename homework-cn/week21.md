# week21

> **定理 2.1 (第一换元法则)**
> 
> 设 $F'\left(u\right)=f\left(u\right)$, 且 $u=\varphi\left(x\right)$ 可导, 则 $\int{f}\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm{d}x=F\left(\varphi\left(x\right)\right)+C$.

> **定理 2.2 (第二换元法则)**
> 
> 设 $x=\varphi\left(t\right)$ 可导且有反函数, 又设 $\int{f}\left(\varphi\left(t\right)\right)\varphi'\left(t\right)\,\mathrm{d}t=G\left(t\right)+C$, 则 $\int{f}\left(x\right)\,\mathrm{d}x=G\left(\varphi^{-1}\left(x\right)\right)+C$.

> **定理 3.1 (分部积分公式)**
> 
> 设 $u\left(x\right),v\left(x\right)$ 可导, 则 $\int{u}\left(x\right)\,\mathrm{d}v\left(x\right)=u\left(x\right)v\left(x\right)-\int{v}\left(x\right)\,\mathrm{d}u\left(x\right)$.

> **定理 4.1 (有理函数的分解)**
> 
> 任何有理函数 $\frac{P\left(x\right)}{Q\left(x\right)}$ 都可以分解为一个多项式与若干部分分式之和, 其中每个部分分式形如 $\frac{A}{\left(x-a\right)^k}$ 或 $\frac{Bx+C}{\left(x^2+px+q\right)^m}$ ($p^2-4q<0$).

## 4.2-2-7

求不定积分 $\int\frac{\mathrm{d}x}{x\sqrt{a^2-x^2}}$ ($a>0$).

### 解答 4.2-2-7

令 $x=a\sin{t}$. 由**定理 2.2 (第二换元法则)**,

$$
\int\frac{\mathrm{d}x}{x\sqrt{a^2-x^2}}=\frac1a\int\frac{\mathrm{d}t}{\sin{t}}=\frac1a\ln\left|\csc{t}-\cot{t}\right|+C.
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

令 $x=a\tan{t}$. 由**定理 2.2 (第二换元法则)**,

$$
\int\frac{\mathrm{d}x}{x^2\sqrt{x^2+a^2}}=\frac1{a^2}\int\frac{\cos{t}}{\sin^2t}\,\mathrm{d}t.
$$

令 $u=\sin{t}$, 则 $\frac1{a^2}\int\frac{\mathrm{d}u}{u^2}=-\frac1{a^2u}+C$. 代回 $u=\frac{x}{\sqrt{x^2+a^2}}$, 得

$$
\int\frac{\mathrm{d}x}{x^2\sqrt{x^2+a^2}}=-\frac{\sqrt{x^2+a^2}}{a^2x}+C.
$$

$\blacksquare$

## 4.3-1-11

求不定积分 $\int{x}\csc^2x\,\mathrm{d}x$.

### 解答 4.3-1-11

令 $u=x$, $\mathrm{d}v=\csc^2x\,\mathrm{d}x$, 则 $\mathrm{d}u=\mathrm{d}x$, $v=-\cot{x}$. 由**定理 3.1 (分部积分公式)**,

$$
\int{x}\csc^2x\,\mathrm{d}x=-x\cot{x}+\int\cot{x}\,\mathrm{d}x=-x\cot{x}+\ln\left|\sin{x}\right|+C.
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

令 $u=\sec{x}$, $\mathrm{d}v=\sec^2x\,\mathrm{d}x$. 由**定理 3.1 (分部积分公式)**,

$$
\int\sec^3x\,\mathrm{d}x=\sec{x}\tan{x}-\int\sec{x}\tan^2x\,\mathrm{d}x.
$$

利用 $\tan^2x=\sec^2x-1$,

$$
\int\sec^3x\,\mathrm{d}x=\sec{x}\tan{x}-\int\sec^3x\,\mathrm{d}x+\int\sec{x}\,\mathrm{d}x.
$$

移项得 $2\int\sec^3x\,\mathrm{d}x=\sec{x}\tan{x}+\int\sec{x}\,\mathrm{d}x$. 而 $\int\sec{x}\,\mathrm{d}x=\ln\left|\sec{x}+\tan{x}\right|+C$. 故

$$
\int\sec^3x\,\mathrm{d}x=\frac12\left(\sec{x}\tan{x}+\ln\left|\sec{x}+\tan{x}\right|\right)+C.
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

## 4.4-4

求不定积分 $\int\frac{4x^2}{x\left(x+2\right)}\,\mathrm{d}x$.

### 解答 4.4-4

化简: $\frac{4x^2}{x\left(x+2\right)}=\frac{4x}{x+2}=4-\frac8{x+2}$. 故

$$
\int\frac{4x^2}{x\left(x+2\right)}\,\mathrm{d}x=4x-8\ln\left|x+2\right|+C.
$$

$\blacksquare$

## 4.4-6

求不定积分 $\int\frac{2x^2-5}{x^4-5x^2+6}\,\mathrm{d}x$.

### 解答 4.4-6

分解分母: $x^4-5x^2+6=\left(x^2-2\right)\left(x^2-3\right)$. 由**定理 4.1 (有理函数的分解)**, 设 $\frac{2x^2-5}{\left(x^2-2\right)\left(x^2-3\right)}=\frac{A}{x^2-2}+\frac{B}{x^2-3}$. 解得 $A=1$, $B=1$. 故

$$
\int\frac{2x^2-5}{x^4-5x^2+6}\,\mathrm{d}x=\frac1{2\sqrt2}\ln\left|\frac{x-\sqrt2}{x+\sqrt2}\right|+\frac1{2\sqrt3}\ln\left|\frac{x-\sqrt3}{x+\sqrt3}\right|+C.
$$

$\blacksquare$

## 4.4-8

求不定积分 $\int\frac{x}{\left(x^2+2\right)^2}\,\mathrm{d}x$.

### 解答 4.4-8

令 $u=x^2+2$. 由**定理 2.1 (第一换元法则)**,

$$
\int\frac{x}{\left(x^2+2\right)^2}\,\mathrm{d}x=\frac12\int\frac{\mathrm{d}u}{u^2}=-\frac1{2\left(x^2+2\right)}+C.
$$

$\blacksquare$

## 4.4-10

求不定积分 $\int\frac{x^3}{\left(x-1\right)^2}\,\mathrm{d}x$.

### 解答 4.4-10

令 $u=x-1$. 被积函数变为 $\frac{\left(u+1\right)^3}{u^2}=u+3+\frac3u+\frac1{u^2}$. 故

$$
\int\frac{x^3}{\left(x-1\right)^2}\,\mathrm{d}x=\frac{\left(x-1\right)^2}2+3\left(x-1\right)+3\ln\left|x-1\right|-\frac1{x-1}+C.
$$

$\blacksquare$
