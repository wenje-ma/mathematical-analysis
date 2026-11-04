# week6

> **命题 1.7 (三角不等式)**
> 
> 对于任意实数 $a,b,c$, $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **定理 3.1 (极限四则运算定理)**
> 
> 设 $\left\{a_n\right\}$ 与 $\left\{b_n\right\}$ 都有极限, 分别为 $l_1$ 与 $l_2$, 则 $\lim\left(a_n\pm b_n\right)=l_1\pm l_2$, $\lim\left(a_n\cdot b_n\right)=l_1\cdot l_2$, 且当 $l_2\ne0$ 时 $\lim\frac{a_n}{b_n}=\frac{l_1}{l_2}$.

> **定理 3.2 (实数域完备性)**
> 
> 设 $\left\{a_n\right\}$ 是一个单调递增有上界的实数序列, 则存在 $l\in\mathbb R$, 使得 $\left\{a_n\right\}$ 以 $l$ 为极限.

> **例 3.3 (正数的 $n$ 次方根趋于 $1$)**
> 
> 设 $a$ 是任意的正数, 则 $\lim_{n\to\infty}a^{1/n}=1$.

> **定理 4.2 (夹逼定理)**
> 
> 设 $\left\{a_n\right\},\left\{b_n\right\},\left\{c_n\right\}$ 为三个序列, 并且存在一个自然数 $N_0$, 使得 $c_n\le a_n\le b_n$ 对一切 $n\ge N_0$ 成立. 若 $c_n$ 与 $b_n$ 都有极限且都等于 $l$, 则 $a_n$ 的极限存在并且也等于 $l$.

> **定理 5.1 (函数极限四则运算)**
> 
> 若 $\lim f\left(x\right)=l_1$, $\lim g\left(x\right)=l_2$, 则 $\lim\left(f\pm g\right)=l_1\pm l_2$, $\lim\left(f\cdot g\right)=l_1\cdot l_2$, 且当 $l_2\ne0$ 时 $\lim\frac{f}{g}=\frac{l_1}{l_2}$.

## 1.4-14

设有两个序列 $\left\{a_n\right\}$ 与 $\left\{b_n\right\}$, 其中 $\left\{a_n\right\}$ 为**无穷小量**, 而 $\left\{b_n\right\}$ 为有界序列, 即存在正数 $M$ 使得 $\left|b_n\right|\le M$ 对一切 $n$ 成立. 证明 $\lim_{n\to\infty}a_nb_n=0$.

### 解答 1.4-14

因 $\left\{a_n\right\}$ 为**无穷小量**, 即 $\lim_{n\to\infty}a_n=0$. 又 $\left|b_n\right|\le M$, 故

$$
0\le\left|a_nb_n\right|\le M\left|a_n\right|.
$$

当 $n\to\infty$ 时 $M\left|a_n\right|\to0$, 左端 $0\to0$. 由**定理 4.2 (夹逼定理)**, $\lim_{n\to\infty}\left|a_nb_n\right|=0$, 即 $\lim_{n\to\infty}a_nb_n=0$. $\blacksquare$

## 1.4-16

设 $\lim_{n\to\infty}a_n=a$, 证明:

(1) $\lim_{n\to\infty}\frac{\left[na_n\right]}{n}=a$;

(2) 若 $a> 0$ 且 $a_n> 0$, 则 $\lim_{n\to\infty}\sqrt\left[n\right]{a_n}=1$.

### 解答 1.4-16

(1) 由取整函数定义, $na_n-1< \left[na_n\right]\le na_n$, 故

$$
a_n-\frac1n< \frac{\left[na_n\right]}{n}\le a_n.
$$

当 $n\to\infty$ 时 $a_n\to a$, $a_n-\frac1n\to a$ (因 $\frac1n\to0$). 由**定理 4.2 (夹逼定理)**, $\frac{\left[na_n\right]}{n}\to a$.

(2) 因 $a_n\to a> 0$, 存在 $N$ 使得当 $n> N$ 时 $\frac a2< a_n< 2a$. 于是

$$
\left(\frac a2\right)^{1/n}< a_n^{1/n}< \left(2a\right)^{1/n}.
$$

由**例 3.3 (正数的 $n$ 次方根趋于 $1$)**, 两端均趋于 $1$. 由**定理 4.2 (夹逼定理)**, $\sqrt\left[n\right]{a_n}\to1$. $\blacksquare$

## 1.4-18

证明 $\lim_{n\to\infty}\left(1+\frac1{n^2}\right)^n=1$.

### 解答 1.4-18

由二项式展开,

$$
\left(1+\frac1{n^2}\right)^n=\sum_{k=0}^n\binom nk\frac1{n^{2k}}=1+\frac1n+\sum_{k=2}^n\binom nk\frac1{n^{2k}}.
$$

对 $k\ge2$, $\binom nk\le\frac{n^k}{k!}$, 故

$$
0\le\left(1+\frac1{n^2}\right)^n-1\le\frac1n+\frac1{n^2}\sum_{k=2}^n\frac1{k!}\le\frac1n+\frac{e-2}{n^2}.
$$

右端当 $n\to\infty$ 时趋于 $0$. 由**定理 4.2 (夹逼定理)**, $\left(1+\frac1{n^2}\right)^n\to1$. $\blacksquare$

## 1.5-1-2

利用 $\varepsilon$-$\delta$ 语言证明: $\lim_{x\to a}\cos x=\cos a$.

### 解答 1.5-1-2

由和差化积公式,

$$
\left|\cos x-\cos a\right|=2\left|\sin\frac{x+a}2\right|\left|\sin\frac{x-a}2\right|\le2\cdot1\cdot\frac{\left|x-a\right|}2=\left|x-a\right|,
$$

其中用到 $\left|\sin t\right|\le\left|t\right|$ 对一切 $t$ 成立.

任给 $\varepsilon> 0$, 取 $\delta=\varepsilon$, 则当 $0< \left|x-a\right|< \delta$ 时,

$$
\left|\cos x-\cos a\right|\le\left|x-a\right|< \varepsilon.
$$

由函数极限的定义, $\lim_{x\to a}\cos x=\cos a$. $\blacksquare$

## 1.5-1-3

利用 $\varepsilon$-$\delta$ 语言证明: $\lim_{x\to+\infty}\frac{6x+5}{x+1}=6$.

### 解答 1.5-1-3

$$
\left|\frac{6x+5}{x+1}-6\right|=\left|\frac{6x+5-6\left(x+1\right)}{x+1}\right|=\frac1{x+1}.
$$

任给 $\varepsilon> 0$, 取 $X=\frac1\varepsilon-1$, 则当 $x> X$ 时,

$$
\left|\frac{6x+5}{x+1}-6\right|=\frac1{x+1}< \varepsilon.
$$

由函数极限的定义 的 $x\to+\infty$ 版本, $\lim_{x\to+\infty}\frac{6x+5}{x+1}=6$. $\blacksquare$

## 1.5-1-5

利用 $\varepsilon$-$\delta$ 语言证明: $\lim_{x\to2-0}\sqrt{4-x^2}=0$.

### 解答 1.5-1-5

$\left|\sqrt{4-x^2}-0\right|=\sqrt{4-x^2}$. 要使 $\sqrt{4-x^2}< \varepsilon$, 只需 $4-x^2< \varepsilon^2$, 即 $x^2> 4-\varepsilon^2$. 因 $x\to2-0$ 时 $x< 2$, 故只需 $x> \sqrt{4-\varepsilon^2}$. 取 $\delta=2-\sqrt{4-\varepsilon^2}$, 则当 $2-\delta< x< 2$ 时,

$$
0< 2-x< \delta\Rightarrow x> \sqrt{4-\varepsilon^2}\Rightarrow\sqrt{4-x^2}< \varepsilon.
$$

由单侧极限的定义, $\lim_{x\to2-0}\sqrt{4-x^2}=0$. $\blacksquare$

## 1.5-1-7

设 $a> 0$, 证明 $\lim_{x\to0}a^x=1$.

### 解答 1.5-1-7

不妨设 $a> 1$ ($0< a< 1$ 时同理). 要使 $\left|a^x-1\right|< \varepsilon$, 即 $1-\varepsilon< a^x< 1+\varepsilon$. 假设 $0< \varepsilon< 1$, 则左边 $a^x> 1-\varepsilon> 0$, 取对数得 $x> \log_a\left(1-\varepsilon\right)$; 右边 $a^x< 1+\varepsilon$ 得 $x< \log_a\left(1+\varepsilon\right)$.

取

$$
\delta=\min\left\{-\log_a\left(1-\varepsilon\right),\log_a\left(1+\varepsilon\right)\right\}> 0,
$$

则当 $0< \left|x\right|< \delta$ 时 $\left|a^x-1\right|< \varepsilon$. 由函数极限的定义, $\lim_{x\to0}a^x=1$. $\blacksquare$

## 1.5-4

设 $\lim_{x\to a}f\left(x\right)=l$, 且 $l\ne0$. 证明函数 $y=\frac1{f\left(x\right)}$ 当 $x\to a$ 时为有界变量.

### 解答 1.5-4

取 $\varepsilon=\frac{\left|l\right|}{2}$. 由函数极限的定义, 存在 $\delta> 0$, 使得当 $0< \left|x-a\right|< \delta$ 时, $\left|f\left(x\right)-l\right|< \frac{\left|l\right|}{2}$. 由**命题 1.7 (三角不等式)**,

$$
\left|f\left(x\right)\right|=\left|l-\left(l-f\left(x\right)\right)\right|\ge\left|l\right|-\left|l-f\left(x\right)\right|> \left|l\right|-\frac{\left|l\right|}{2}=\frac{\left|l\right|}{2}.
$$

于是 $\left|\frac1{f\left(x\right)}\right|< \frac2{\left|l\right|}$, 即 $\frac1{f\left(x\right)}$ 当 $x\to a$ 时有界. 此即极限的保号性 的推论. $\blacksquare$
