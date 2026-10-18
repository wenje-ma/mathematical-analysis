# 作业 7

> **定义**（连续函数）假定 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 内有定义. 若在一点 $x_0\in\left(a,b\right)$ 处 $\lim\limits_{x\to x_0}f\left(x\right)=f\left(x_0\right)$, 则称 $y=f\left(x\right)$ 在 $x_0$ 点连续. 若 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 的每一点都连续, 则称它在 $\left(a,b\right)$ 上连续.

> **定理 7.2**（复合函数连续性）若 $y=g\left(y\right)$ 在 $y_0$ 点连续, $y=f\left(x\right)$ 在 $x_0$ 点连续且 $f\left(x_0\right)=y_0$, 则复合函数 $y=g\left(f\left(x\right)\right)$ 在 $x_0$ 点连续.

> **定义**（初等函数）初等函数在其定义域内是连续的.

### 习题一

（习题 1.7-1）指出下列函数的间断点及其类型: 
(1) $y=\operatorname{sgn}\left(\sin x\right)$;

(2)

$$
y=f\left(x\right)=\begin{cases}x^2e^x,&x>0,\\sin\frac{\pi}{1+x^2},&x<0,\1,&x=0;\end{cases}
$$

(3) $y=\cos\left\{\left(x-\left[x\right]\right)\pi\right\}$;

(4)

$$
y=f\left(x\right)=\begin{cases}e^{\sin\frac1x},&x\ne0,\0,&x=0.\end{cases}
$$

### 解答 习题一

(1)当 $x=k\pi$($k\in\mathbb Z$)时 $\sin x=0$, $\operatorname{sgn}\left(\sin x\right)$ 左右极限分别为 $1$ 与 $-1$(或反之), 为第一类间断点(跳跃间断点). 其余点连续.

(2)$x\to0+0$ 时 $f\left(x\right)=x^2e^x\to0$; $x\to0-0$ 时

$$
f\left(x\right)=\sin\frac{\pi}{1+x^2}\to\sin\pi=0.
$$

但 $f\left(0\right)=1$, 故 $x=0$ 为可去间断点(第一类).

(3)$x-\left[x\right]=\left\{x\right\}$ 为小数部分, 在整数点处左右极限分别为 $\cos0=1$ 与 $\cos\pi=-1$, 故整数点为跳跃间断点(第一类). 其余点连续.

(4)$x\to0$ 时 $\frac1x$ 振荡, $\sin\frac1x$ 在 $\left[-1,1\right]$ 内振荡, $e^{\sin\left(1/x\right)}$ 在 $e^{-1}$ 与 $e$ 之间振荡, 极限不存在, 故 $x=0$ 为第二类间断点(振荡间断点). $\blacksquare$

### 习题二

（习题 1.7-2-2）试用 $\epsilon$-$\delta$ 语言证明: 若 $y=f\left(x\right)$ 在 $a$ 点连续, 则 $y=\left|f\left(x\right)\right|$ 在 $a$ 点连续.

### 解答 习题二

由**定义**（连续函数）, 任给 $\epsilon>0$, 存在 $\delta>0$, 使得当 $\left|x-a\right|<\delta$ 时 $\left|f\left(x\right)-f\left(a\right)\right|<\epsilon$. 由第一章**命题 1.7**（三角不等式）, 

$$
\left|\left|f\left(x\right)\right|-\left|f\left(a\right)\right|\right|\le\left|f\left(x\right)-f\left(a\right)\right|<\epsilon.
$$

故 $\left|f\left(x\right)\right|$ 在 $a$ 点连续. $\blacksquare$

### 习题三

（习题 1.7-3）利用初等函数的连续性求下列极限: 
(1) $\lim\limits_{x\to0}\cos\left(\sqrt{1+x^2}-1\right)$;

(2) $\lim\limits_{x\to0}e^{\frac{\sin x}{\sin2x}}$;

(3) $\lim\limits_{x\to\infty}\arctan\frac{\sqrt{x^4+2}}{1+x^2}$;

(4) $\lim\limits_{x\to5}x^{\sqrt x}$;

(5) $\lim\limits_{x\to\infty}\left(1+\frac1x+\frac1{x^2}\right)^{x+\sqrt x}$.

### 解答 习题三

(1)由**定理 7.2**（复合函数连续性）, $\lim\limits_{x\to0}\left(\sqrt{1+x^2}-1\right)=0$, 故原式 $=\cos0=1$.

(2)$\frac{\sin x}{\sin2x}\to\frac12$, 由 $e^u$ 的连续性, 原式 $=e^{1/2}=\sqrt e$.

(3)$\frac{\sqrt{x^4+2}}{1+x^2}\to1$, 由 $\arctan u$ 的连续性, 原式 $=\arctan1=\frac\pi4$.

(4)$x^{\sqrt x}=e^{\sqrt x\ln x}$, $\sqrt x\ln x\to\sqrt5\ln5$, 由连续性, 原式 $=e^{\sqrt5\ln5}=5^{\sqrt5}$.

(5)

$$
\left(1+\frac1x+\frac1{x^2}\right)^{x+\sqrt x}=\left[\left(1+\frac{x+1}{x^2}\right)^{\frac{x^2}{x+1}}\right]^{\frac{\left(x+\sqrt x\right)\left(x+1\right)}{x^2}}.
$$

底数趋于 $e$, 指数趋于 $1$, 故原式 $=e$. $\blacksquare$

### 习题四

（习题 1.7-4）设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中连续. 又设 $x=g\left(t\right)$ 当 $t\to\infty$ 时有极限, 且极限落在 $\left(a,b\right)$ 之中. 试证明

$$
\lim\limits_{t\to\infty}f\left(g\left(t\right)\right)=f\left(\lim\limits_{t\to\infty}g\left(t\right)\right).
$$

### 解答 习题四

设 $\lim\limits_{t\to\infty}g\left(t\right)=c\in\left(a,b\right)$. 由**定义**（连续函数）, 任给 $\epsilon>0$, 存在 $\delta>0$, 使得当 $\left|x-c\right|<\delta$ 时 $\left|f\left(x\right)-f\left(c\right)\right|<\epsilon$. 又因 $g\left(t\right)\to c$, 存在 $T>0$, 当 $t>T$ 时 $\left|g\left(t\right)-c\right|<\delta$. 于是当 $t>T$ 时 $\left|f\left(g\left(t\right)\right)-f\left(c\right)\right|<\epsilon$. 即 $\lim f\left(g\left(t\right)\right)=f\left(c\right)$. $\blacksquare$

### 习题五

（习题 1.7-5）设 $y=f\left(x\right)$ 及 $y=g\left(x\right)$ 在实数域 $\mathbb R$ 中有定义且连续. 假定 $f\left(x\right)=g\left(x\right),\forall x\in\mathbb Q$, 试证明 $f\left(x\right)\equiv g\left(x\right),\forall x\in\mathbb R$.

### 解答 习题五

任取 $x_0\in\mathbb R$. 由有理数的稠密性, 存在有理序列 $\left\{r_n\right\}$ 使 $r_n\to x_0$. 因 $f,g$ 连续, 

$$
f\left(x_0\right)=\lim_{n\to\infty}f\left(r_n\right)=\lim_{n\to\infty}g\left(r_n\right)=g\left(x_0\right).
$$

故 $f\left(x_0\right)=g\left(x_0\right)$. 由 $x_0$ 的任意性, $f\equiv g$. $\blacksquare$

### 习题六

（习题 1.7-6）设 $t_1$ 与 $t_2$ 是任意两个实数. 请在不利用公式 $e^{t_1+t_2}=e^{t_1}\cdot e^{t_2}$ 的条件下, 证明下列极限等式:

$$
\lim\limits_{x\to\infty}\left[\left(1+\frac{t_1}{x}\right)\left(1+\frac{t_2}{x}\right)\right]^x=e^{t_1+t_2}.
$$

### 解答 习题六

$$
\left[\left(1+\frac{t_1}{x}\right)\left(1+\frac{t_2}{x}\right)\right]^x=\left(1+\frac{t_1+t_2+t_1t_2/x}{x}\right)^x=\left[\left(1+\frac{t_1+t_2+o\left(1\right)}{x}\right)^{\frac{x}{t_1+t_2+o\left(1\right)}}\right]^{t_1+t_2+o\left(1\right)}.
$$

底数趋于 $e$, 指数趋于 $t_1+t_2$. 由指数函数连续性, 极限为 $e^{t_1+t_2}$. $\blacksquare$
