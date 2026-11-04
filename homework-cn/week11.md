# week11

> **定理 2.1 (复合函数求导法则)**
> 
> 设 $y=f\left(u\right)$ 在 $u$ 处可导, $u=g\left(x\right)$ 在 $x$ 处可导, 则复合函数 $y=f\left(g\left(x\right)\right)$ 在 $x$ 处可导, 且 $\frac{\mathrm dy}{\mathrm dx}=\frac{\mathrm dy}{\mathrm du}\cdot\frac{\mathrm du}{\mathrm dx}=f'\left(g\left(x\right)\right)g'\left(x\right)$.

## 2.2-3-14

求导函数: $y=x^{\sqrt x}$.

### 解答 2.2-3-14

取对数: $\ln y=\sqrt x\ln x$. 两边求导:

$$
\frac{y'}y=\frac1{2\sqrt x}\ln x+\frac{\sqrt x}{x}=\frac{\ln x}{2\sqrt x}+\frac1{\sqrt x}.
$$

故

$$
y'=x^{\sqrt x}\left(\frac{\ln x}{2\sqrt x}+\frac1{\sqrt x}\right).
$$

$\blacksquare$

## 2.2-5

飞轮半径为 $r$, 以固定角速度 $\omega$ 旋转, 连杆长为 $a$ ($a> r$). 设 $x=x\left(t\right)$ 为时刻 $t$ 飞轮中心至活塞端点的距离, $x\left(0\right)=a+r$. 试给出 $x\left(t\right)$ 的表达式, 并求出 $x'\left(t\right)$ 及 $x'\left(0\right)$.

### 解答 2.2-5

设飞轮转角 $\theta\left(t\right)=\omega t$. 由几何关系,

$$
x\left(t\right)=r\cos\omega t+\sqrt{a^2-r^2\sin^2\omega t}.
$$

求导:

$$
x'\left(t\right)=-r\omega\sin\omega t+\frac{-2r^2\omega\sin\omega t\cos\omega t}{2\sqrt{a^2-r^2\sin^2\omega t}}=-r\omega\sin\omega t\left(1+\frac{r\cos\omega t}{\sqrt{a^2-r^2\sin^2\omega t}}\right).
$$

代入 $t=0$: $\sin0=0$, 故 $x'\left(0\right)=0$. $\blacksquare$

## 2.2-6

设 $y=y\left(x\right)$ 为下列方程所确定的隐函数, 试求其导数:

(1) $x^2+y^2=R^2$ ($y\ne0$);

(2) $y^2-2xy-x^2-2x=4$ ($y\ne x$).

### 解答 2.2-6

(1) 两边对 $x$ 求导: $2x+2yy'=0$, 故 $y'=-\frac{x}{y}$.

(2) 两边对 $x$ 求导:

$$
2yy'-2\left(y+xy'\right)-2x-2=0,
$$

整理得

$$
\left(2y-2x\right)y'=2y+2x+2,
$$

故 $y'=\frac{y+x+1}{y-x}$. $\blacksquare$

## 2.3-1-2

当 $x\to0$ 时, 下列无穷小量是几阶无穷小量: $y=\left(\sqrt{2+x}-\sqrt2\right)x$.

### 解答 2.3-1-2

$$
\sqrt{2+x}-\sqrt2=\frac{x}{\sqrt{2+x}+\sqrt2}\sim\frac{x}{2\sqrt2}.
$$

故 $y\sim\frac{x^2}{2\sqrt2}$, 由高阶无穷小的定义 知 $y$ 是 $x$ 的二阶无穷小量. $\blacksquare$

## 2.3-1-4

当 $x\to0$ 时, 下列无穷小量是几阶无穷小量: $y=\ln\left(1+x^2\right)+x^3$.

### 解答 2.3-1-4

$\ln\left(1+x^2\right)\sim x^2$, 而 $x^3=o\left(x^2\right)$. 由高阶无穷小的定义, $y\sim x^2$, 是二阶无穷小量. $\blacksquare$

## 2.3-3-1

计算下列函数在指定点 $x_0$ 的微分: $f\left(x\right)=x^2\arcsin x$, $x_0=0$.

### 解答 2.3-3-1

$$
f'\left(x\right)=2x\arcsin x+\frac{x^2}{\sqrt{1-x^2}}.
$$

$f'\left(0\right)=0$. 故 $\mathrm df\big|_{x_0=0}=0\cdot\mathrm dx=0$. $\blacksquare$

## 2.3-3-4

计算下列函数在指定点 $x_0$ 的微分: $f\left(x\right)=x\ln\left(1+x\right)$, $x_0=0$.

### 解答 2.3-3-4

$f'\left(x\right)=\ln\left(1+x\right)+\frac{x}{1+x}$. $f'\left(0\right)=0$. 故 $\mathrm df\big|_{x_0=0}=0$. $\blacksquare$

## 2.3-4-2

求函数的微分: $f\left(x\right)=\ln\left(x+\sqrt{x^2+1}\right)$.

### 解答 2.3-4-2

$$
f'\left(x\right)=\frac1{x+\sqrt{x^2+1}}\cdot\left(1+\frac{x}{\sqrt{x^2+1}}\right)=\frac1{x+\sqrt{x^2+1}}\cdot\frac{\sqrt{x^2+1}+x}{\sqrt{x^2+1}}=\frac1{\sqrt{x^2+1}}.
$$

故 $\mathrm df=\frac1{\sqrt{x^2+1}}\mathrm dx$. $\blacksquare$

## 2.3-4-4

求函数的微分: $f\left(x\right)=\sqrt{1+x^2}+\sqrt x\sin x$.

### 解答 2.3-4-4

$$
f'\left(x\right)=\frac{x}{\sqrt{1+x^2}}+\frac1{2\sqrt x}\sin x+\sqrt x\cos x.
$$

故

$$
\mathrm df=\left(\frac{x}{\sqrt{1+x^2}}+\frac{\sin x}{2\sqrt x}+\sqrt x\cos x\right)\mathrm dx.
$$

$\blacksquare$

## 2.3-5-1

填空: $\mathrm d\left(\right)=x^n\mathrm dx$.

### 解答 2.3-5-1

$$
\mathrm d\left(\frac{x^{n+1}}{n+1}\right)=x^n\mathrm dx\quad\left(n\ne-1\right).
$$

$\blacksquare$

## 2.3-5-3

填空: $\mathrm d\left(\right)=\left(e^x+\sin2x\right)\mathrm dx$.

### 解答 2.3-5-3

$$
\mathrm d\left(e^x-\frac12\cos2x\right)=\left(e^x+\sin2x\right)\mathrm dx.
$$

$\blacksquare$

## 2.3-5-5

填空: $\mathrm d\left(\right)=\frac{\sin x}{\cos x}\mathrm dx$.

### 解答 2.3-5-5

$\mathrm d\left(-\ln\left|\cos x\right|\right)=\frac{\sin x}{\cos x}\mathrm dx$. $\blacksquare$

## 2.3-6

计算 $\tan\left(\frac\pi4+0.01\right)$ 的近似值.

### 解答 2.3-6

令 $f\left(x\right)=\tan x$, 取 $x_0=\frac\pi4$, $\Delta x=0.01$. $f'\left(x\right)=\sec^2x$, $f'\left(\frac\pi4\right)=2$. 由微分的定义 导出的近似公式

$$
f\left(x_0+\Delta x\right)\approx f\left(x_0\right)+f'\left(x_0\right)\Delta x,
$$

$$
\tan\left(\frac\pi4+0.01\right)\approx\tan\frac\pi4+2\times0.01=1+0.02=1.02.
$$

$\blacksquare$

## 2.4-1

求下列函数的 $n$ 阶导数:

(1) $y=x^2e^x$;

(4) $y=x\ln\left(1+x\right)$.

### 解答 2.4-1

由高阶导数的定义, $n$ 阶导数由 $n-1$ 阶导数再求导得到.

(1) 由莱布尼茨公式, 其中 $u=x^2$, $v=e^x$.

$$
u'=2x,\quad u''=2,\quad u^{\left(k\right)}=0\quad\left(k\ge3\right).
$$

故

$$
y^{\left(n\right)}=x^2e^x+2nx e^x+n\left(n-1\right)e^x=e^x\left[x^2+2nx+n\left(n-1\right)\right].
$$

(4) $y'=\ln\left(1+x\right)+\frac{x}{1+x}$.

$$
y''=\frac1{1+x}+\frac1{\left(1+x\right)^2}=\frac{2+x}{\left(1+x\right)^2}.
$$

一般地, 对 $n\ge2$,

$$
y^{\left(n\right)}=\left(-1\right)^n\frac{\left(n-2\right)!}{\left(1+x\right)^{n-1}}+\left(-1\right)^{n-1}\frac{\left(n-1\right)!}{\left(1+x\right)^n}.
$$

化简得

$$
y^{\left(n\right)}=\left(-1\right)^n\frac{\left(n-2\right)!}{\left(1+x\right)^{n-1}}\cdot\frac{x}{1+x}\quad\left(n\ge2\right).
$$

$\blacksquare$
