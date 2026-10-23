# 作业 6

> **命题 6.1**（重要极限 $\lim\limits_{x\to0}\frac{\sin x}{x}=1$）$\lim\limits_{x\to0}\frac{\sin x}{x}=1$.

> **重要极限**（数 $e$ 的函数版本）$\lim\limits_{x\to\infty}\left(1+\frac1x\right)^x=e$.

> **定理 6.2**（函数的夹逼定理）设
> $$
> y=f\left(x\right),y=g\left(x\right),y=h\left(x\right)
> $$
> 在 $a$ 点的一个空心邻域内有定义, 且 $h\left(x\right)\le f\left(x\right)\le g\left(x\right)$. 若 $\lim g\left(x\right)=\lim h\left(x\right)=l$, 则 $\lim f\left(x\right)=l$.

### 习题一

（习题 1.6-2）用 $\varepsilon$-$\delta$ 语言证明: 若 $\lim\limits_{x\to a}f\left(x\right)=l$ 且 $l>0$, 则存在一个 $\delta>0$, 使得 $f\left(x\right)>\frac l2$, 只要 $0<\left|x-a\right|<\delta$.

### 解答 习题一

取 $\varepsilon=\frac l2>0$. 由**定义**（函数极限）, 存在 $\delta>0$, 使得当 $0<\left|x-a\right|<\delta$ 时 $\left|f\left(x\right)-l\right|<\frac l2$. 由第一章**命题 1.7**（三角不等式）, 

$$
f\left(x\right)=l-\left(l-f\left(x\right)\right)\ge l-\left|f\left(x\right)-l\right|>l-\frac l2=\frac l2.
$$

故 $f\left(x\right)>\frac l2$. $\blacksquare$

### 习题二

（习题 1.6-3）利用极限 $\lim\limits_{x\to0}\frac{\sin x}{x}=1$ 求下列极限: 
(1) $\lim\limits_{x\to0}\frac{\sin\alpha x}{\sin\beta x}\left(\beta\ne0\right)$;

(2) $\lim\limits_{x\to0}\frac{\tan3x-\tan5x}{\sin2x}$;

(3) $\lim\limits_{x\to0}\frac{1-\cos x}{x^2}$;

(4) $\lim\limits_{x\to a}\frac{\sin x-\sin a}{x-a}$.

### 解答 习题二

(1)$\frac{\sin\alpha x}{\sin\beta x}=\frac{\alpha}{\beta}\cdot\frac{\sin\alpha x}{\alpha x}\cdot\frac{\beta x}{\sin\beta x}$. 由**命题 6.1**（重要极限）及第一章**定理 5.1**, 极限为 $\frac{\alpha}{\beta}$.

(2)

$$
\tan3x-\tan5x=\frac{\sin3x}{\cos3x}-\frac{\sin5x}{\cos5x}=\frac{\sin3x\cos5x-\cos3x\sin5x}{\cos3x\cos5x}=\frac{-\sin2x}{\cos3x\cos5x}.
$$

故原式 $=\frac{-1}{\cos3x\cos5x}\to-1$.

(3)$1-\cos x=2\sin^2\frac x2$, 故

$$
\frac{1-\cos x}{x^2}=\frac{2\sin^2\left(x/2\right)}{x^2}=\frac12\left(\frac{\sin\left(x/2\right)}{x/2}\right)^2\to\frac12.
$$

(4)

$$
\sin x-\sin a=2\cos\frac{x+a}2\sin\frac{x-a}2,
$$
故

$$
\frac{\sin x-\sin a}{x-a}=\cos\frac{x+a}2\cdot\frac{\sin\left(x-a\right)/2}{\left(x-a\right)/2}\to\cos a.
$$

$\blacksquare$

### 习题三

（习题 1.6-4-1）利用 $\lim\limits_{x\to\infty}\left(1+\frac1x\right)^x=e$ 求极限: $\lim\limits_{x\to\infty}\left(1+\frac3x\right)^x\cdot\left(1+\frac5x\right)^x$.

### 解答 习题三

$$
\left(1+\frac3x\right)^x=\left[\left(1+\frac3x\right)^{x/3}\right]^3\to e^3,\left(1+\frac5x\right)^x=\left[\left(1+\frac5x\right)^{x/5}\right]^5\to e^5.
$$

由第一章**定理 5.1**, 乘积的极限为 $e^3\cdot e^5=e^8$. $\blacksquare$

### 习题四

（习题 1.6-4-3）求极限: $\lim\limits_{x\to0}\left(\frac{1+x}{1-x}\right)^{1/x}$.

### 解答 习题四

$$
\left(\frac{1+x}{1-x}\right)^{1/x}=\left[\left(1+\frac{2x}{1-x}\right)^{\frac{1-x}{2x}}\right]^{\frac{2}{1-x}}.
$$

底数趋于 $e$, 指数 $\frac2{1-x}\to2$. 由**重要极限**（数 $e$）及**定理 6.2** 相关运算, 极限为 $e^2$. $\blacksquare$

### 习题五

（习题 1.6-4-5）求极限: $\lim\limits_{y\to0}\left(1-5y\right)^{1/y}$.

### 解答 习题五

$$
\left(1-5y\right)^{1/y}=\left[\left(1+\frac1{-1/\left(5y\right)}\right)^{-1/\left(5y\right)}\right]^{-5}.
$$

底数趋于 $e$, 指数为 $-5$. 由**重要极限**（数 $e$）, 极限为 $e^{-5}=\frac1{e^5}$. $\blacksquare$

### 习题六

（习题 1.6-4-6）求极限: $\lim\limits_{x\to\infty}\left(1+\frac1x\right)^{x+100}$.

### 解答 习题六

$$
\left(1+\frac1x\right)^{x+100}=\left(1+\frac1x\right)^x\cdot\left(1+\frac1x\right)^{100}\to e\cdot1=e.

$$

$\blacksquare$
### 习题七

（习题 1.6-5）求出常数 $a$ 与 $b$, 使

$$
\lim\limits_{x\to+\infty}\left[\frac{x^2+1}{x+1}-\left(ax+b\right)\right]=0.
$$

试说明几何意义.

### 解答 习题七

$$
\frac{x^2+1}{x+1}-ax-b=\frac{x^2+1-\left(ax+b\right)\left(x+1\right)}{x+1}=\frac{\left(1-a\right)x^2-\left(a+b\right)x+1-b}{x+1}.
$$

要使其趋于 $0$, 分子次数必须低于分母次数, 故 $1-a=0$ 且 $a+b=0$. 解得 $a=1,b=-1$.

几何意义: 直线 $y=x-1$ 是曲线 $y=\frac{x^2+1}{x+1}$ 当 $x\to+\infty$ 时的斜渐近线. $\blacksquare$

### 习题八

（习题 1.6-7）证明 $\lim\limits_{x\to+\infty}\left(1+\frac1x\right)^{x^2}=+\infty$.

### 解答 习题八

$$
\left(1+\frac1x\right)^{x^2}=\left[\left(1+\frac1x\right)^x\right]^x.
$$

当 $x$ 充分大时 $\left(1+\frac1x\right)^x>2$(因趋于 $e>2$), 故 $\left(1+\frac1x\right)^{x^2}>2^x\to+\infty$. 因此极限为 $+\infty$. $\blacksquare$

### 习题九

（习题 1.6-9）设 $\lim\limits_{x\to+\infty}\frac{f\left(x\right)}x=0$, 且 $f\left(x\right)>0\left(x>0\right)$. 证明 $\lim\limits_{x\to+\infty}\left(1+\frac1x\right)^{f\left(x\right)}=1$.

### 解答 习题九

取对数:

$$
\left(1+\frac1x\right)^{f\left(x\right)}=e^{f\left(x\right)\ln\left(1+1/x\right)}.
$$

因

$$
0<f\left(x\right)\ln\left(1+\frac1x\right)<f\left(x\right)\cdot\frac1x\to0,
$$

由**定理 6.2**（函数的夹逼定理）, 指数趋于 $0$. 由 $e^t$ 的连续性, 原极限为 $e^0=1$. $\blacksquare$

### 习题十

（习题 1.6-10）设 $y=D\left(x\right)$ 为狄利克雷函数. 证明: 对于任意一点 $a\in\mathbb R$, 极限 $\lim\limits_{x\to a}D\left(x\right)$ 不存在.

### 解答 习题十

取有理序列 $\left\{r_n\right\}$ 和无理序列 $\left\{s_n\right\}$, 均以 $a$ 为极限(由有理数与无理数的稠密性). 则 $D\left(r_n\right)=1\to1$, $D\left(s_n\right)=0\to0$. 两子序列极限不同, 由函数极限与序列极限的归结原则, $\lim\limits_{x\to a}D\left(x\right)$ 不存在. $\blacksquare$

### 习题十一

（习题 1.6-11）求极限: $\lim\limits_{x\to+\infty}\frac{\left(\ln x\right)^5}{x}$.

### 解答 习题十一

作变量替换 $y=\ln x$, 则 $x=e^y$, 当 $x\to+\infty$ 时 $y\to+\infty$. 原式化为 $\lim\limits_{y\to+\infty}\frac{y^5}{e^y}=0$(指数函数增长快于任何幂函数). $\blacksquare$
