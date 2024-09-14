# week3

> **命题 1.7 (三角不等式)**
> 
> 对于任意实数 $a,b,c$, $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **定理 3.1 (极限四则运算定理)**
> 
> 设 $\left\{a_n\right\}$ 与 $\left\{b_n\right\}$ 都有极限, 分别为 $l_1$ 与 $l_2$, 则 $\lim\left(a_n\pm{b}_n\right)=l_1\pm{l}_2$, $\lim\left(a_n\cdot{b}_n\right)=l_1\cdot{l}_2$, 且当 $l_2\ne0$ 时 $\lim\frac{a_n}{b_n}=\frac{l_1}{l_2}$.

> **定理 3.2 (实数域完备性)**
> 
> 设 $\left\{a_n\right\}$ 是一个单调递增有上界的实数序列, 则存在 $l\in\mathbb{R}$, 使得 $\left\{a_n\right\}$ 以 $l$ 为极限.

> **定理 4.2 (夹逼定理)**
> 
> 设 $\left\{a_n\right\},\left\{b_n\right\},\left\{c_n\right\}$ 为三个序列, 并且存在一个自然数 $N_0$, 使得 $c_n\le{a}_n\le{b}_n$ 对一切 $n\ge{N}_0$ 成立. 若 $c_n$ 与 $b_n$ 都有极限且都等于 $l$, 则 $a_n$ 的极限存在并且也等于 $l$.

> **定理 5.1 (函数极限四则运算)**
> 
> 若 $\lim{f}\left(x\right)=l_1$, $\lim{g}\left(x\right)=l_2$, 则 $\lim\left(f\pm{g}\right)=l_1\pm{l}_2$, $\lim\left(f\cdot{g}\right)=l_1\cdot{l}_2$, 且当 $l_2\ne0$ 时 $\lim\frac{f}{g}=\frac{l_1}{l_2}$.

## 1.4-16

设 $\lim_{n\to\infty}a_n=a$, 证明:

(1) $\lim_{n\to\infty}\frac{\left[na_n\right]}{n}=a$;

(2) 若 $a>0$ 且 $a_n>0$, 则 $\lim_{n\to\infty}\sqrt[n]{a_n}=1$.

### 解答 1.4-16

(1) 由取整函数定义, $na_n-1<\left[na_n\right]\le{n}a_n$, 故

$$
a_n-\frac1n<\frac{\left[na_n\right]}{n}\le{a}_n.
$$

当 $n\to\infty$ 时 $a_n\to{a}$, $a_n-\frac1n\to{a}$ (因 $\frac1n\to0$). 由**定理 4.2 (夹逼定理)**, $\frac{\left[na_n\right]}{n}\to{a}$.

(2) 因 $a_n\to{a}>0$, 存在 $N$ 使得当 $n>N$ 时 $\frac{a}2<{}a_n<2a$. 于是

$$
\left(\frac{a}2\right)^{1/n}<{}a_n^{1/n}<\left(2a\right)^{1/n}.
$$

由**例 3.3 (正数的 $n$ 次方根趋于 $1$)**, 两端均趋于 $1$. 由**定理 4.2 (夹逼定理)**, $\sqrt[n]{a_n}\to1$.

$\blacksquare$

## 1.4-18

证明 $\lim_{n\to\infty}\left(1+\frac1{n^2}\right)^n=1$.

### 解答 1.4-18

由二项式展开,

$$
\left(1+\frac1{n^2}\right)^n=\sum_{k=0}^n\binom{n}k\frac1{n^{2k}}=1+\frac1n+\sum_{k=2}^n\binom{n}k\frac1{n^{2k}}.
$$

对 $k\ge2$, $\binom{n}k\le\frac{n^k}{k!}$, 故

$$
0\le\left(1+\frac1{n^2}\right)^n-1\le\frac1n+\frac1{n^2}\sum_{k=2}^n\frac1{k!}\le\frac1n+\frac{e-2}{n^2}.
$$

右端当 $n\to\infty$ 时趋于 $0$. 由**定理 4.2 (夹逼定理)**, $\left(1+\frac1{n^2}\right)^n\to1$.

$\blacksquare$

## 1.5-1-2

利用 $\varepsilon$-$\delta$ 语言证明: $\lim_{x\to{a}}\cos{x}=\cos{a}$.

### 解答 1.5-1-2

由和差化积公式,

$$
\left|\cos{x}-\cos{a}\right|=2\left|\sin\frac{x+a}2\right|\left|\sin\frac{x-a}2\right|\le2\cdot1\cdot\frac{\left|x-a\right|}2=\left|x-a\right|,
$$

其中用到 $\left|\sin{t}\right|\le\left|t\right|$ 对一切 $t$ 成立.

任给 $\varepsilon>0$, 取 $\delta=\varepsilon$, 则当 $0<\left|x-a\right|<\delta$ 时,

$$
\left|\cos{x}-\cos{a}\right|\le\left|x-a\right|<\varepsilon.
$$

由函数极限的定义, $\lim_{x\to{a}}\cos{x}=\cos{a}$.

$\blacksquare$

## 1.5-1-3

利用 $\varepsilon$-$\delta$ 语言证明: $\lim_{x\to+\infty}\frac{6x+5}{x+1}=6$.

### 解答 1.5-1-3

$$
\left|\frac{6x+5}{x+1}-6\right|=\left|\frac{6x+5-6\left(x+1\right)}{x+1}\right|=\frac1{x+1}.
$$

任给 $\varepsilon>0$, 取 $X=\frac1\varepsilon-1$, 则当 $x>X$ 时,

$$
\left|\frac{6x+5}{x+1}-6\right|=\frac1{x+1}<\varepsilon.
$$

由函数极限的定义 的 $x\to+\infty$ 版本, $\lim_{x\to+\infty}\frac{6x+5}{x+1}=6$.

$\blacksquare$

## 1.5-1-5

利用 $\varepsilon$-$\delta$ 语言证明: $\lim_{x\to2-0}\sqrt{4-x^2}=0$.

### 解答 1.5-1-5

$\left|\sqrt{4-x^2}-0\right|=\sqrt{4-x^2}$. 要使 $\sqrt{4-x^2}<\varepsilon$, 只需 $4-x^2<\varepsilon^2$, 即 $x^2>4-\varepsilon^2$. 因 $x\to2-0$ 时 $x<2$, 故只需 $x>\sqrt{4-\varepsilon^2}$. 取 $\delta=2-\sqrt{4-\varepsilon^2}$, 则当 $2-\delta<{}x<2$ 时,

$$
0<2-x<\delta\Rightarrow{x}>\sqrt{4-\varepsilon^2}\Rightarrow\sqrt{4-x^2}<\varepsilon.
$$

由单侧极限的定义, $\lim_{x\to2-0}\sqrt{4-x^2}=0$.

$\blacksquare$

## 1.5-1-7

设 $a>0$, 证明 $\lim_{x\to0}a^x=1$.

### 解答 1.5-1-7

不妨设 $a>1$ ($0<{}a<1$ 时同理). 要使 $\left|a^x-1\right|<\varepsilon$, 即 $1-\varepsilon<{}a^x<1+\varepsilon$. 假设 $0<\varepsilon<1$, 则左边 $a^x>1-\varepsilon>0$, 取对数得 $x>\log_a\left(1-\varepsilon\right)$; 右边 $a^x<1+\varepsilon$ 得 $x<\log_a\left(1+\varepsilon\right)$.

取

$$
\delta=\min\left\{-\log_a\left(1-\varepsilon\right),\log_a\left(1+\varepsilon\right)\right\}>0,
$$

则当 $0<\left|x\right|<\delta$ 时 $\left|a^x-1\right|<\varepsilon$. 由函数极限的定义, $\lim_{x\to0}a^x=1$.

$\blacksquare$

## 1.5-4

设 $\lim_{x\to{a}}f\left(x\right)=l$, 且 $l\ne0$. 证明函数 $y=\frac1{f\left(x\right)}$ 当 $x\to{a}$ 时为有界变量.

### 解答 1.5-4

取 $\varepsilon=\frac{\left|l\right|}{2}$. 由函数极限的定义, 存在 $\delta>0$, 使得当 $0<\left|x-a\right|<\delta$ 时, $\left|f\left(x\right)-l\right|<\frac{\left|l\right|}{2}$. 由**命题 1.7 (三角不等式)**,

$$
\left|f\left(x\right)\right|=\left|l-\left(l-f\left(x\right)\right)\right|\ge\left|l\right|-\left|l-f\left(x\right)\right|>\left|l\right|-\frac{\left|l\right|}{2}=\frac{\left|l\right|}{2}.
$$

于是 $\left|\frac1{f\left(x\right)}\right|<\frac2{\left|l\right|}$, 即 $\frac1{f\left(x\right)}$ 当 $x\to{a}$ 时有界. 此即极限的保号性 的推论.

$\blacksquare$

## 1.5-5

设 $\lim_{x\to2}f\left(x\right)=l$, 证明: $y\to\sqrt2$ 时, $f\left(y^2\right)\to{l}$.

### 解答 1.5-5

任给 $\varepsilon>0$, 由函数极限的定义, 存在 $\delta_1>0$, 使得当 $0<\left|x-2\right|<\delta_1$ 时 $\left|f\left(x\right)-l\right|<\varepsilon$. 令 $x=y^2$, 则需 $0<\left|y^2-2\right|<\delta_1$.

因 $y\to\sqrt2$, 可限制 $\left|y-\sqrt2\right|<1$, 此时 $\left|y+\sqrt2\right|\le2\sqrt2+1$. 取 $\delta=\min\left\{1,\frac{\delta_1}{2\sqrt2+1}\right\}$, 则当 $0<\left|y-\sqrt2\right|<\delta$ 时,

$$
\left|y^2-2\right|=\left|y-\sqrt2\right|\left|y+\sqrt2\right|<\delta\cdot\left(2\sqrt2+1\right)\le\delta_1,
$$

且 $y^2\ne2$ (否则 $y=\pm\sqrt2$, 而 $y\to\sqrt2$ 且 $y\ne\sqrt2$ 时 $y^2\ne2$). 故 $\left|f\left(y^2\right)-l\right|<\varepsilon$. 由函数极限的定义, $f\left(y^2\right)\to{l}$.

$\blacksquare$

## 1.5-6

讨论下列函数在 $x=0$ 点的左右极限:

(1) $y=\left[x\right]\cdot\left(1+x\right)$;

(2) $y=\cos{x}\cdot\operatorname{sgn}x$;

(3) $y=\frac{\left|x\right|}{x}\cdot\frac1{1+x^n}$.

### 解答 1.5-6

(1) 当 $x\to0+0$ 时 $\left[x\right]=0$, 故 $y=0$, 右极限为 $0$. 当 $x\to0-0$ 时 $\left[x\right]=-1$, 故 $y=-\left(1+x\right)\to-1$, 左极限为 $-1$.

(2) 当 $x\to0+0$ 时 $\operatorname{sgn}x=1$, 故 $y=\cos{x}\to1$, 右极限为 $1$. 当 $x\to0-0$ 时 $\operatorname{sgn}x=-1$, 故 $y=-\cos{x}\to-1$, 左极限为 $-1$.

(3) 当 $x\to0+0$ 时 $\frac{\left|x\right|}{x}=1$, 且 $\frac1{1+x^n}\to1$, 右极限为 $1$. 当 $x\to0-0$ 时 $\frac{\left|x\right|}{x}=-1$, 且 $\frac1{1+x^n}\to1$ (因 $x^n\to0$), 左极限为 $-1$.

$\blacksquare$

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
f\left(x\right)=l-\left(l-f\left(x\right)\right)\ge{l}-\left|f\left(x\right)-l\right|>l-\frac{l}2=\frac{l}2.
$$

故 $f\left(x\right)>\frac{l}2$.

$\blacksquare$

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

由**定理 5.1 (函数极限四则运算)**, 乘积的极限为 $e^3\cdot{e}^5=e^8$.

$\blacksquare$

## 1.6-4-3

求极限: $\lim_{x\to0}\left(\frac{1+x}{1-x}\right)^{1/x}$.

### 解答 1.6-4-3

$$
\left(\frac{1+x}{1-x}\right)^{1/x}=\left[\left(1+\frac{2x}{1-x}\right)^{\frac{1-x}{2x}}\right]^{\frac2{1-x}}.
$$

底数趋于 $e$, 指数 $\frac2{1-x}\to2$. 由重要极限数 $e$ 的函数版本 及**定理 6.2 (函数的夹逼定理)** 相关运算, 极限为 $e^2$.

$\blacksquare$

## 1.6-4-5

求极限: $\lim_{y\to0}\left(1-5y\right)^{1/y}$.

### 解答 1.6-4-5

$$
\left(1-5y\right)^{1/y}=\left[\left(1+\frac1{-1/\left(5y\right)}\right)^{-1/\left(5y\right)}\right]^{-5}.
$$

底数趋于 $e$, 指数为 $-5$. 由重要极限数 $e$ 的函数版本, 极限为 $e^{-5}=\frac1{e^5}$.

$\blacksquare$

## 1.6-4-6

求极限: $\lim_{x\to\infty}\left(1+\frac1x\right)^{x+100}$.

### 解答 1.6-4-6

$$
\left(1+\frac1x\right)^{x+100}=\left(1+\frac1x\right)^x\cdot\left(1+\frac1x\right)^{100}\to{e}\cdot1=e.
$$

$\blacksquare$
