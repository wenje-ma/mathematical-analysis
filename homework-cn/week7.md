# week7

> **命题 1.7 (三角不等式)**
> 
> 对于任意实数 $a,b,c$, $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **定理 5.1 (函数极限四则运算)**
> 
> 若 $\lim{f}\left(x\right)=l_1$, $\lim{g}\left(x\right)=l_2$, 则 $\lim\left(f\pm{g}\right)=l_1\pm{l}_2$, $\lim\left(f\cdot{g}\right)=l_1\cdot{l}_2$, 且当 $l_2\ne0$ 时 $\lim\frac{f}{g}=\frac{l_1}{l_2}$.

> **命题 6.1 (重要极限 $\lim_{x\to0}\frac{\sin{x}}{x}=1$)**
> 
> $\lim_{x\to0}\frac{\sin{x}}{x}=1$.

> **定理 6.2 (函数的夹逼定理)**
> 
> 设 $y=f\left(x\right)$, $y=g\left(x\right)$, $y=h\left(x\right)$ 在 $a$ 点的一个空心邻域内有定义, 且 $h\left(x\right)\le{f}\left(x\right)\le{g}\left(x\right)$. 若 $\lim{g}\left(x\right)=\lim{h}\left(x\right)=l$, 则 $\lim{f}\left(x\right)=l$.

## 1.5-5

设 $\lim_{x\to2}f\left(x\right)=l$, 证明: $y\to\sqrt2$ 时, $f\left(y^2\right)\to{l}$.

### 解答 1.5-5

任给 $\varepsilon>0$, 由函数极限的定义, 存在 $\delta_1>0$, 使得当 $0<\left|x-2\right|<\delta_1$ 时 $\left|f\left(x\right)-l\right|<\varepsilon$. 令 $x=y^2$, 则需 $0<\left|y^2-2\right|<\delta_1$.

因 $y\to\sqrt2$, 可限制 $\left|y-\sqrt2\right|<1$, 此时 $\left|y+\sqrt2\right|\le2\sqrt2+1$. 取 $\delta=\min\left\{1,\frac{\delta_1}{2\sqrt2+1}\right\}$, 则当 $0<\left|y-\sqrt2\right|<\delta$ 时,

$$
\left|y^2-2\right|=\left|y-\sqrt2\right|\left|y+\sqrt2\right|<\delta\cdot\left(2\sqrt2+1\right)\le\delta_1,
$$

且 $y^2\ne2$ (否则 $y=\pm\sqrt2$, 而 $y\to\sqrt2$ 且 $y\ne\sqrt2$ 时 $y^2\ne2$). 故 $\left|f\left(y^2\right)-l\right|<\varepsilon$. 由函数极限的定义, $f\left(y^2\right)\to{l}$. $\blacksquare$

## 1.5-6

讨论下列函数在 $x=0$ 点的左右极限:

(1) $y=\left[x\right]\cdot\left(1+x\right)$;

(2) $y=\cos{x}\cdot\operatorname{sgn}x$;

(3) $y=\frac{\left|x\right|}{x}\cdot\frac1{1+x^n}$.

### 解答 1.5-6

(1) 当 $x\to0+0$ 时 $\left[x\right]=0$, 故 $y=0$, 右极限为 $0$. 当 $x\to0-0$ 时 $\left[x\right]=-1$, 故 $y=-\left(1+x\right)\to-1$, 左极限为 $-1$.

(2) 当 $x\to0+0$ 时 $\operatorname{sgn}x=1$, 故 $y=\cos{x}\to1$, 右极限为 $1$. 当 $x\to0-0$ 时 $\operatorname{sgn}x=-1$, 故 $y=-\cos{x}\to-1$, 左极限为 $-1$.

(3) 当 $x\to0+0$ 时 $\frac{\left|x\right|}{x}=1$, 且 $\frac1{1+x^n}\to1$, 右极限为 $1$. 当 $x\to0-0$ 时 $\frac{\left|x\right|}{x}=-1$, 且 $\frac1{1+x^n}\to1$ (因 $x^n\to0$), 左极限为 $-1$. $\blacksquare$

## 1.5-7

求极限:

(1) $\lim_{x\to-1}\left(\frac1{x+1}-\frac3{x^3+1}\right)$;

(2) $\lim_{x\to0}\frac{\sqrt{a^2+x}-a}{x}$ ($a>0$).

### 解答 1.5-7

(1) 由因式分解 $x^3+1=\left(x+1\right)\left(x^2-x+1\right)$,

$$
\frac1{x+1}-\frac3{x^3+1}=\frac{x^2-x+1-3}{\left(x+1\right)\left(x^2-x+1\right)}=\frac{x^2-x-2}{\left(x+1\right)\left(x^2-x+1\right)}=\frac{\left(x-2\right)\left(x+1\right)}{\left(x+1\right)\left(x^2-x+1\right)}=\frac{x-2}{x^2-x+1}.
$$

由**定理 5.1 (函数极限四则运算)**,

$$
\lim_{x\to-1}\frac{x-2}{x^2-x+1}=\frac{-1-2}{1+1+1}=-1.
$$

(2) 分子有理化:

$$
\frac{\sqrt{a^2+x}-a}{x}=\frac{\left(\sqrt{a^2+x}-a\right)\left(\sqrt{a^2+x}+a\right)}{x\left(\sqrt{a^2+x}+a\right)}=\frac{x}{x\left(\sqrt{a^2+x}+a\right)}=\frac1{\sqrt{a^2+x}+a}.
$$

由**定理 5.1 (函数极限四则运算)** 及 $\lim_{x\to0}\sqrt{a^2+x}=a$,

$$
\lim_{x\to0}\frac{\sqrt{a^2+x}-a}{x}=\frac1{2a}.
$$

$\blacksquare$

## 1.6-2

用 $\varepsilon$-$\delta$ 语言证明: 若 $\lim_{x\to{a}}f\left(x\right)=l$ 且 $l>0$, 则存在 $\delta>0$, 使得 $f\left(x\right)>\frac{l}2$, 只要 $0<\left|x-a\right|<\delta$.

### 解答 1.6-2

取 $\varepsilon=\frac{l}2>0$. 由函数极限的定义, 存在 $\delta>0$, 使得当 $0<\left|x-a\right|<\delta$ 时 $\left|f\left(x\right)-l\right|<\frac{l}2$. 由**命题 1.7 (三角不等式)**,

$$
f\left(x\right)=l-\left(l-f\left(x\right)\right)\ge{l}-\left|f\left(x\right)-l\right|>{}l-\frac{l}2=\frac{l}2.
$$

故 $f\left(x\right)>\frac{l}2$. $\blacksquare$

## 1.6-3

利用极限 $\lim_{x\to0}\frac{\sin{x}}{x}=1$ 求下列极限:

(1) $\lim_{x\to0}\frac{\sin\alpha{x}}{\sin\beta{x}}$ ($\beta\ne0$);

(2) $\lim_{x\to0}\frac{\tan3x-\tan5x}{\sin2x}$;

(3) $\lim_{x\to0}\frac{1-\cos{x}}{x^2}$;

(4) $\lim_{x\to{a}}\frac{\sin{x}-\sin{a}}{x-a}$.

### 解答 1.6-3

(1) $\frac{\sin\alpha{x}}{\sin\beta{x}}=\frac{\alpha}{\beta}\cdot\frac{\sin\alpha{x}}{\alpha{x}}\cdot\frac{\beta{x}}{\sin\beta{x}}$. 由**命题 6.1 (重要极限 $\lim_{x\to0}\frac{\sin{x}}{x}=1$)** 及**定理 5.1 (函数极限四则运算)**, 极限为 $\frac{\alpha}{\beta}$.

(2)

$$
\tan3x-\tan5x=\frac{\sin3x}{\cos3x}-\frac{\sin5x}{\cos5x}=\frac{\sin3x\cos5x-\cos3x\sin5x}{\cos3x\cos5x}=\frac{-\sin2x}{\cos3x\cos5x}.
$$

故原式 $=\frac{-1}{\cos3x\cos5x}\to-1$.

(3) $1-\cos{x}=2\sin^2\frac{x}2$, 故

$$
\frac{1-\cos{x}}{x^2}=\frac{2\sin^2\left(x/2\right)}{x^2}=\frac12\left(\frac{\sin\left(x/2\right)}{x/2}\right)^2\to\frac12.
$$

(4)

$$
\sin{x}-\sin{a}=2\cos\frac{x+a}2\sin\frac{x-a}2,
$$

故

$$
\frac{\sin{x}-\sin{a}}{x-a}=\cos\frac{x+a}2\cdot\frac{\sin\left(x-a\right)/2}{\left(x-a\right)/2}\to\cos{a}.
$$

$\blacksquare$

## 1.6-4-1

利用 $\lim_{x\to\infty}\left(1+\frac1x\right)^x=e$ 求极限: $\lim_{x\to\infty}\left(1+\frac3x\right)^x\cdot\left(1+\frac5x\right)^x$.

### 解答 1.6-4-1

$$
\left(1+\frac3x\right)^x=\left[\left(1+\frac3x\right)^{x/3}\right]^3\to{e}^3,\quad\left(1+\frac5x\right)^x=\left[\left(1+\frac5x\right)^{x/5}\right]^5\to{e}^5.
$$

由**定理 5.1 (函数极限四则运算)**, 乘积的极限为 $e^3\cdot{e}^5=e^8$. $\blacksquare$
