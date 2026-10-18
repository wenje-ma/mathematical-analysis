# 作业 5

> **定义**（函数极限）设 $y=f\left(x\right)$ 在 $a$ 点的一个空心邻域 $\left(a-r,a+r\right)\backslash\left\{a\right\}$ 内有定义. 若存在一个实数 $l$, 对于任意给定的 $\epsilon>0$, 无论它多么小, 都存在一个 $\delta>0$, 使得当 $0<\left|x-a\right|<\delta$ 时, $\left|f\left(x\right)-l\right|<\epsilon$, 则称当 $x\to a$ 时 $f\left(x\right)$ 以 $l$ 为极限, 记作 $\lim\limits_{x\to a}f\left(x\right)=l$.

> **定义**（单侧极限）若当 $x\to a+0$(或 $x\to a-0$)时 $f\left(x\right)$ 以 $l$ 为极限, 则称之为右极限(或左极限), 记作 $\lim\limits_{x\to a+0}f\left(x\right)=l$(或 $\lim\limits_{x\to a-0}f\left(x\right)=l$).

> **定理 5.1**（函数极限四则运算）若 $\lim f\left(x\right)=l_1$, $\lim g\left(x\right)=l_2$, 则 $\lim\left(f\pm g\right)=l_1\pm l_2$, $\lim\left(f\cdot g\right)=l_1\cdot l_2$, 且当 $l_2\ne0$ 时 $\lim\frac{f}{g}=\frac{l_1}{l_2}$.

> **命题**（保号性）若 $\lim\limits_{x\to a}f\left(x\right)=l$ 且 $l\ne0$, 则存在 $\delta>0$ 使得当 $0<\left|x-a\right|<\delta$ 时 $\left|f\left(x\right)\right|>\frac{\left|l\right|}{2}$.

### 习题一

（习题 1.5-1-2）利用 $\epsilon$-$\delta$ 语言证明: $\lim\limits_{x\to a}\cos x=\cos a$.

### 解答 习题一

由和差化积公式, 

$$
\left|\cos x-\cos a\right|=2\left|\sin\frac{x+a}2\right|\left|\sin\frac{x-a}2\right|\le2\cdot1\cdot\frac{\left|x-a\right|}2=\left|x-a\right|,
$$

其中用到 $\left|\sin t\right|\le\left|t\right|$ 对一切 $t$ 成立.

任给 $\epsilon>0$, 取 $\delta=\epsilon$, 则当 $0<\left|x-a\right|<\delta$ 时, 

$$
\left|\cos x-\cos a\right|\le\left|x-a\right|<\epsilon.
$$

由**定义**（函数极限）, $\lim\limits_{x\to a}\cos x=\cos a$. $\blacksquare$

### 习题二

（习题 1.5-1-3）利用 $\epsilon$-$\delta$ 语言证明: $\lim\limits_{x\to+\infty}\frac{6x+5}{x+1}=6$.

### 解答 习题二

$$
\left|\frac{6x+5}{x+1}-6\right|=\left|\frac{6x+5-6\left(x+1\right)}{x+1}\right|=\frac1{x+1}.
$$

任给 $\epsilon>0$, 取 $X=\frac1\epsilon-1$, 则当 $x>X$ 时, 

$$
\left|\frac{6x+5}{x+1}-6\right|=\frac1{x+1}<\epsilon.
$$

由**定义**（函数极限）的 $x\to+\infty$ 版本, $\lim\limits_{x\to+\infty}\frac{6x+5}{x+1}=6$. $\blacksquare$

### 习题三

（习题 1.5-1-5）利用 $\epsilon$-$\delta$ 语言证明: $\lim\limits_{x\to2-0}\sqrt{4-x^2}=0$.

### 解答 习题三

$\left|\sqrt{4-x^2}-0\right|=\sqrt{4-x^2}$. 要使 $\sqrt{4-x^2}<\epsilon$, 只需 $4-x^2<\epsilon^2$, 即 $x^2>4-\epsilon^2$. 因 $x\to2-0$ 时 $x<2$, 故只需 $x>\sqrt{4-\epsilon^2}$. 取 $\delta=2-\sqrt{4-\epsilon^2}$, 则当 $2-\delta<x<2$ 时, 

$$
0<2-x<\delta\Rightarrow x>\sqrt{4-\epsilon^2}\Rightarrow\sqrt{4-x^2}<\epsilon.
$$

由**定义**（单侧极限）, $\lim\limits_{x\to2-0}\sqrt{4-x^2}=0$. $\blacksquare$

### 习题四

（习题 1.5-1-7）设 $a>0$, 证明 $\lim\limits_{x\to0}a^x=1$.

### 解答 习题四

不妨设 $a>1$($0<a<1$ 时同理). 要使 $\left|a^x-1\right|<\epsilon$, 即 $1-\epsilon<a^x<1+\epsilon$. 假设 $0<\epsilon<1$, 则左边 $a^x>1-\epsilon>0$, 取对数得 $x>\log_a\left(1-\epsilon\right)$; 右边 $a^x<1+\epsilon$ 得 $x<\log_a\left(1+\epsilon\right)$.

取

$$
\delta=\min\left\{-\log_a\left(1-\epsilon\right),\log_a\left(1+\epsilon\right)\right\}>0,
$$

则当 $0<\left|x\right|<\delta$ 时 $\left|a^x-1\right|<\epsilon$. 由**定义**（函数极限）, $\lim\limits_{x\to0}a^x=1$. $\blacksquare$

### 习题五

（习题 1.5-4）设 $\lim\limits_{x\to a}f\left(x\right)=l$, 且 $l\ne0$. 证明函数 $y=\frac1{f\left(x\right)}$ 当 $x\to a$ 时为有界变量.

### 解答 习题五

取 $\epsilon=\frac{\left|l\right|}{2}$. 由**定义**（函数极限）, 存在 $\delta>0$, 使得当 $0<\left|x-a\right|<\delta$ 时, $\left|f\left(x\right)-l\right|<\frac{\left|l\right|}{2}$. 由第一章**命题 1.7**（三角不等式）, 

$$
\left|f\left(x\right)\right|=\left|l-\left(l-f\left(x\right)\right)\right|\ge\left|l\right|-\left|l-f\left(x\right)\right|>\left|l\right|-\frac{\left|l\right|}{2}=\frac{\left|l\right|}{2}.
$$

于是 $\left|\frac1{f\left(x\right)}\right|<\frac2{\left|l\right|}$, 即 $\frac1{f\left(x\right)}$ 当 $x\to a$ 时有界. 此即**命题**（保号性）的推论. $\blacksquare$

### 习题六

（习题 1.5-5）设 $\lim\limits_{x\to2}f\left(x\right)=l$, 证明: $y\to\sqrt2$ 时, $f\left(y^2\right)\to l$.

### 解答 习题六

任给 $\epsilon>0$, 由**定义**（函数极限）, 存在 $\delta_1>0$, 使得当 $0<\left|x-2\right|<\delta_1$ 时 $\left|f\left(x\right)-l\right|<\epsilon$. 令 $x=y^2$, 则需 $0<\left|y^2-2\right|<\delta_1$.

因 $y\to\sqrt2$, 可限制 $\left|y-\sqrt2\right|<1$, 此时 $\left|y+\sqrt2\right|\le2\sqrt2+1$. 取 $\delta=\min\left\{1,\frac{\delta_1}{2\sqrt2+1}\right\}$, 则当 $0<\left|y-\sqrt2\right|<\delta$ 时, 

$$
\left|y^2-2\right|=\left|y-\sqrt2\right|\left|y+\sqrt2\right|<\delta\cdot\left(2\sqrt2+1\right)\le\delta_1,
$$

且 $y^2\ne2$(否则 $y=\pm\sqrt2$, 而 $y\to\sqrt2$ 且 $y\ne\sqrt2$ 时 $y^2\ne2$). 故 $\left|f\left(y^2\right)-l\right|<\epsilon$. 由**定义**（函数极限）, $f\left(y^2\right)\to l$. $\blacksquare$

### 习题七

（习题 1.5-6）讨论下列函数在 $x=0$ 点的左右极限: 
(1) $y=\left[x\right]\cdot\left(1+x\right)$;

(2) $y=\cos x\cdot\operatorname{sgn}x$;

(3) $y=\frac{\left|x\right|}{x}\cdot\frac1{1+x^n}$.

### 解答 习题七

(1)当 $x\to0+0$ 时 $\left[x\right]=0$, 故 $y=0$, 右极限为 $0$. 当 $x\to0-0$ 时 $\left[x\right]=-1$, 故 $y=-\left(1+x\right)\to-1$, 左极限为 $-1$.

(2)当 $x\to0+0$ 时 $\operatorname{sgn}x=1$, 故 $y=\cos x\to1$, 右极限为 $1$. 当 $x\to0-0$ 时 $\operatorname{sgn}x=-1$, 故 $y=-\cos x\to-1$, 左极限为 $-1$.

(3)当 $x\to0+0$ 时 $\frac{\left|x\right|}{x}=1$, 且 $\frac1{1+x^n}\to1$, 右极限为 $1$. 当 $x\to0-0$ 时 $\frac{\left|x\right|}{x}=-1$, 且 $\frac1{1+x^n}\to1$(因 $x^n\to0$), 左极限为 $-1$. $\blacksquare$

### 习题八

（习题 1.5-7）求极限: 
(1) $\lim\limits_{x\to-1}\left(\frac1{x+1}-\frac3{x^3+1}\right)$;

(2) $\lim\limits_{x\to0}\frac{\sqrt{a^2+x}-a}{x}\left(a>0\right)$.

### 解答 习题八

(1)由因式分解

$$
x^3+1=\left(x+1\right)\left(x^2-x+1\right),
$$

$$
\frac1{x+1}-\frac3{x^3+1}=\frac{x^2-x+1-3}{\left(x+1\right)\left(x^2-x+1\right)}=\frac{x^2-x-2}{\left(x+1\right)\left(x^2-x+1\right)}=\frac{\left(x-2\right)\left(x+1\right)}{\left(x+1\right)\left(x^2-x+1\right)}=\frac{x-2}{x^2-x+1}.
$$

由**定理 5.1**（函数极限四则运算）, 

$$
\lim_{x\to-1}\frac{x-2}{x^2-x+1}=\frac{-1-2}{1+1+1}=-1.
$$

(2)分子有理化: 

$$
\frac{\sqrt{a^2+x}-a}{x}=\frac{\left(\sqrt{a^2+x}-a\right)\left(\sqrt{a^2+x}+a\right)}{x\left(\sqrt{a^2+x}+a\right)}=\frac{x}{x\left(\sqrt{a^2+x}+a\right)}=\frac1{\sqrt{a^2+x}+a}.
$$

由**定理 5.1**（函数极限四则运算）及 $\lim\limits_{x\to0}\sqrt{a^2+x}=a$, 

$$
\lim_{x\to0}\frac{\sqrt{a^2+x}-a}{x}=\frac1{2a}.

$$

$\blacksquare$