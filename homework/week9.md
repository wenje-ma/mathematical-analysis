# 作业 9

> **定理 2.1**（复合函数求导法则）设 $y=f\left(u\right)$ 在 $u$ 处可导, $u=g\left(x\right)$ 在 $x$ 处可导, 则复合函数 $y=f\left(g\left(x\right)\right)$ 在 $x$ 处可导, 且
> $$
> \frac{\mathrm dy}{\mathrm dx}=\frac{\mathrm dy}{\mathrm du}\cdot\frac{\mathrm du}{\mathrm dx}=f'\left(g\left(x\right)\right)g'\left(x\right).
> $$

### 习题一

（习题 2.2-2）设 $f\left(x\right)=1+x^2$, 求 $f'\left(\sin x\right)$ 及 $\left[f\left(\sin x\right)\right]'$.

### 解答 习题一

$f'\left(x\right)=2x$, 故 $f'\left(\sin x\right)=2\sin x$.

由**定理 2.1**（复合函数求导法则）, 

$$
\left[f\left(\sin x\right)\right]'=f'\left(\sin x\right)\cdot\left(\sin x\right)'=2\sin x\cos x=\sin2x.

$$

$\blacksquare$
### 习题二

（习题 2.2-3-2）求导函数: $y=\sqrt{1+x^2}$.

### 解答 习题二

$$
y'=\frac1{2\sqrt{1+x^2}}\cdot\left(1+x^2\right)'=\frac{2x}{2\sqrt{1+x^2}}=\frac{x}{\sqrt{1+x^2}}.

$$

$\blacksquare$
### 习题三

（习题 2.2-3-4）求导函数: $y=\frac12\sqrt{a^2-x^2}$.

### 解答 习题三

$$
y'=\frac12\cdot\frac1{2\sqrt{a^2-x^2}}\cdot\left(-2x\right)=-\frac{x}{2\sqrt{a^2-x^2}}.

$$

$\blacksquare$
### 习题四

（习题 2.2-3-6）求导函数: $y=\frac12\left(e^x-e^{-x}\right)$.

### 解答 习题四

$$
y'=\frac12\left(e^x-\left(-e^{-x}\right)\right)=\frac12\left(e^x+e^{-x}\right).

$$

$\blacksquare$
### 习题五

（习题 2.2-3-8）求导函数: $y=\sqrt{x^3+x+1}$.

### 解答 习题五

$$
y'=\frac1{2\sqrt{x^3+x+1}}\cdot\left(3x^2+1\right)=\frac{3x^2+1}{2\sqrt{x^3+x+1}}.

$$

$\blacksquare$
### 习题六

（习题 2.2-3-10）求导函数: $y=e^x+e^{x^2}+\cos x^2$.

### 解答 习题六

$$
y'=e^x+e^{x^2}\cdot2x-\sin x^2\cdot2x=e^x+2xe^{x^2}-2x\sin x^2.

$$

$\blacksquare$
### 习题七

（习题 2.2-3-12）求导函数: $y=\arctan x^2$.

### 解答 习题七

$$
y'=\frac1{1+\left(x^2\right)^2}\cdot2x=\frac{2x}{1+x^4}.

$$

$\blacksquare$
### 习题八

（习题 2.2-3-14）求导函数: $y=x^{\sqrt x}$.

### 解答 习题八

取对数: $\ln y=\sqrt x\ln x$. 两边求导: 

$$
\frac{y'}y=\frac1{2\sqrt x}\ln x+\frac{\sqrt x}{x}=\frac{\ln x}{2\sqrt x}+\frac1{\sqrt x}.
$$

故

$$
y'=x^{\sqrt x}\left(\frac{\ln x}{2\sqrt x}+\frac1{\sqrt x}\right).

$$

$\blacksquare$
### 习题九

（习题 2.2-5）飞轮半径为 $r$, 以固定角速度 $\omega$ 旋转, 连杆长为 $a\left(a>r\right)$. 设 $x=x\left(t\right)$ 为时刻 $t$ 飞轮中心至活塞端点的距离, $x\left(0\right)=a+r$. 试给出 $x\left(t\right)$ 的表达式, 并求出 $x'\left(t\right)$ 及 $x'\left(0\right)$.

### 解答 习题九

设飞轮转角 $\theta\left(t\right)=\omega t$. 由几何关系, 

$$
x\left(t\right)=r\cos\omega t+\sqrt{a^2-r^2\sin^2\omega t}.
$$

求导: 

$$
x'\left(t\right)=-r\omega\sin\omega t+\frac{-2r^2\omega\sin\omega t\cos\omega t}{2\sqrt{a^2-r^2\sin^2\omega t}}=-r\omega\sin\omega t\left(1+\frac{r\cos\omega t}{\sqrt{a^2-r^2\sin^2\omega t}}\right).
$$

代入 $t=0$: $\sin0=0$, 故 $x'\left(0\right)=0$. $\blacksquare$

### 习题十

（习题 2.2-6）设 $y=y\left(x\right)$ 为下列方程所确定的隐函数, 试求其导数: 
(1) $x^2+y^2=R^2\left(y\ne0\right)$;

(2)

$$
y^2-2xy-x^2-2x=4\left(y\ne x\right).
$$

### 解答 习题十

(1)两边对 $x$ 求导: $2x+2yy'=0$, 故 $y'=-\frac{x}{y}$.

(2)两边对 $x$ 求导:

$$
2yy'-2\left(y+xy'\right)-2x-2=0,
$$
整理得

$$
\left(2y-2x\right)y'=2y+2x+2,
$$

故 $y'=\frac{y+x+1}{y-x}$. $\blacksquare$
