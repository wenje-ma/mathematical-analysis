# 作业 14

> **定理 2.1**（柯西中值定理）设 $y=f\left(x\right)$ 与 $y=g\left(x\right)$ 在 $\left[a,b\right]$ 中连续, 在 $\left(a,b\right)$ 中可导, 且 $g'\left(x\right)\ne0$($a<x<b$). 则存在点 $c\in\left(a,b\right)$, 使得
> $$
> \frac{f\left(b\right)-f\left(a\right)}{g\left(b\right)-g\left(a\right)}=\frac{f'\left(c\right)}{g'\left(c\right)}.
> $$
> **定理 2.2**（洛必达法则，$\frac00$ 型）设 $y=f\left(x\right)$ 及 $y=g\left(x\right)$ 在 $a$ 点的一个空心邻域内有定义且可导, $g'\left(x\right)\ne0$. 假定 $\lim\limits_{x\to a}f\left(x\right)=\lim\limits_{x\to a}g\left(x\right)=0$, 且 $\lim\limits_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ 存在. 则
> $$
> \lim_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}.
> $$
> **定理 2.3**（洛必达法则，$\frac{\infty}{\infty}$ 型）设 $y=f\left(x\right)$ 与 $y=g\left(x\right)$ 在 $a$ 点的一个空心邻域内有定义且可导, $g'\left(x\right)\ne0$. 假定
> $$
> \lim\limits_{x\to a}f\left(x\right)=\lim\limits_{x\to a}g\left(x\right)=\infty,
> $$
> 且 $\lim\limits_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ 存在. 则
> $$
> \lim_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}.
> $$
### 习题一

（习题 3.2-1）求下列未定式的极限: 
(1) $\lim\limits_{x\to0}\frac{\ln\left(\cos ax\right)}{\ln\left(\cos bx\right)}$($a\ne0,b\ne0$); 

(2) $\lim\limits_{x\to0}\frac{a^x-1}{x}$($a>0$); 

(3) $\lim\limits_{x\to0}\frac{\tan x-x}{x-\arcsin x}$; 

(4) $\lim\limits_{x\to0+}x^x$; 

(5) $\lim\limits_{x\to0+}x\ln x$; 

(6) $\lim\limits_{x\to0+}\frac{\ln\left(\sin x\right)}{x^2}$; 

(7) $\lim\limits_{x\to0+}\left(\sin x\right)^{\sin x}$.

### 解答 习题一

(1)这是 $\frac00$ 型未定式. 由**定理 2.2**（洛必达法则）, 
$$
\lim_{x\to0}\frac{\ln\left(\cos ax\right)}{\ln\left(\cos bx\right)}=\lim_{x\to0}\frac{\frac{-a\sin ax}{\cos ax}}{\frac{-b\sin bx}{\cos bx}}=\lim_{x\to0}\frac{a\tan ax}{b\tan bx}=\frac{a}{b}\cdot\frac{a}{b}=\frac{a^2}{b^2}.
$$

(2)这是 $\frac00$ 型未定式. 由**定理 2.2**（洛必达法则）, 
$$
\lim_{x\to0}\frac{a^x-1}{x}=\lim_{x\to0}\frac{a^x\ln a}{1}=\ln a.
$$

(3)这是 $\frac00$ 型未定式. 由**定理 2.2**（洛必达法则）, 
$$
\lim_{x\to0}\frac{\tan x-x}{x-\arcsin x}=\lim_{x\to0}\frac{\sec^2 x-1}{1-\frac{1}{\sqrt{1-x^2}}}.
$$

分子 $\sec^2 x-1=\tan^2 x\sim x^2$($x\to0$). 分母

$$
1-\frac{1}{\sqrt{1-x^2}}=\frac{\sqrt{1-x^2}-1}{\sqrt{1-x^2}}\sim-\frac{x^2}{2}\ \left(x\to0\right).
$$

故
$$
\lim_{x\to0}\frac{\tan x-x}{x-\arcsin x}=\frac{x^2}{-x^2/2}=-2.
$$

(4)这是 $0^0$ 型未定式. 令 $y=x^x$, 则 $\ln y=x\ln x$. 由(5)知 $\lim_{x\to0+}x\ln x=0$, 故
$$
\lim_{x\to0+}x^x=e^0=1.
$$

(5)这是 $0\cdot\infty$ 型未定式. 改写为 $\frac{\infty}{\infty}$ 型后应用**定理 2.3**（洛必达法则）: 
$$
\lim_{x\to0+}x\ln x=\lim_{x\to0+}\frac{\ln x}{1/x}=\lim_{x\to0+}\frac{1/x}{-1/x^2}=\lim_{x\to0+}\left(-x\right)=0.
$$

(6)这是 $\frac{\infty}{\infty}$ 型未定式. 由**定理 2.3**（洛必达法则）, 
$$
\lim_{x\to0+}\frac{\ln\left(\sin x\right)}{x^2}=\lim_{x\to0+}\frac{\cot x}{2x}=\lim_{x\to0+}\frac{\cos x}{2x\sin x}=+\infty.
$$

(7)这是 $0^0$ 型未定式. 令 $y=\left(\sin x\right)^{\sin x}$, 则 $\ln y=\sin x\ln\left(\sin x\right)$. 当 $x\to0+$ 时, $\sin x\to0$, 由(5)的结果(将 $x$ 换成 $\sin x$), 
$$
\lim_{x\to0+}\sin x\ln\left(\sin x\right)=0.
$$

故
$$
\lim_{x\to0+}\left(\sin x\right)^{\sin x}=e^0=1.
$$

$\blacksquare$
### 习题二

（习题 3.2-2）若 $\lim\limits_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ 不存在, 能否说明 $\lim\limits_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}$ 也不存在? 试考察 $f\left(x\right)=x\sin\frac1x$ 及 $g\left(x\right)=x^2$ 在 $x\to0$ 时的情况.

### 解答 习题二

不能. 考察 $f\left(x\right)=x\sin\frac1x$, $g\left(x\right)=x^2$, $x\to0$.

首先,

$$
\lim\limits_{x\to0}\frac{f\left(x\right)}{g\left(x\right)}=\lim\limits_{x\to0}\frac{x\sin\left(1/x\right)}{x^2}=\lim\limits_{x\to0}\frac{\sin\left(1/x\right)}{x}.
$$

该极限不存在(因 $\sin\left(1/x\right)$ 在 $-1$ 与 $1$ 之间振荡, 而 $1/x\to\infty$).

但这不是一个好的例子, 因为我们需要说明 $\lim f/g$ 存在但 $\lim f'/g'$ 不存在. 修正如下: 取 $f\left(x\right)=x^2\sin\frac1x$, $g\left(x\right)=x$. 则
$$
\lim_{x\to0}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to0}x\sin\frac1x=0.
$$

而
$$
f'\left(x\right)=2x\sin\frac1x-\cos\frac1x, g'\left(x\right)=1.
$$

于是
$$
\frac{f'\left(x\right)}{g'\left(x\right)}=2x\sin\frac1x-\cos\frac1x.
$$

当 $x\to0$ 时, $2x\sin\left(1/x\right)\to0$, 但 $\cos\left(1/x\right)$ 振荡无极限. 故 $\lim\limits_{x\to0}\frac{f'\left(x\right)}{g'\left(x\right)}$ 不存在.

这说明: $\lim f'\left(x\right)/g'\left(x\right)$ 不存在时, $\lim f\left(x\right)/g\left(x\right)$ 仍可能存在. 即洛必达法则的逆命题不成立. $\blacksquare$

### 习题三

（习题 3.2-4）设 $y=f\left(x\right)$ 在 $a$ 点有二阶导数, 并令
$$
T\left(x\right)=f\left(a\right)+f'\left(a\right)\Delta x+\frac{f''\left(a\right)}{2}\left(\Delta x\right)^2,
$$
其中 $\Delta x=x-a$. 证明: 函数 $g\left(x\right)=f\left(x\right)-T\left(x\right)$ 满足

$$
\begin{aligned}
g\left(a\right)&=0,g'\left(a\right)=0,g''\left(a\right)=0,\
f\left(x\right)&=T\left(x\right)+o\left(\left(\Delta x\right)^2\right)\ \left(x\to a\right).
\end{aligned}
$$

### 解答 习题三

由 $T\left(x\right)$ 的定义, $T\left(a\right)=f\left(a\right)$,

$$
T'\left(x\right)=f'\left(a\right)+f''\left(a\right)\Delta x,
$$

$T''\left(x\right)=f''\left(a\right)$.

计算得
$$
g\left(a\right)=f\left(a\right)-T\left(a\right)=0,
$$
$$
g'\left(a\right)=f'\left(a\right)-T'\left(a\right)=f'\left(a\right)-f'\left(a\right)=0,
$$
$$
g''\left(a\right)=f''\left(a\right)-T''\left(a\right)=f''\left(a\right)-f''\left(a\right)=0.
$$

下面证明 $g\left(x\right)=o\left(\left(\Delta x\right)^2\right)$. 即证 $\lim\limits_{\Delta x\to0}\frac{g\left(x\right)}{\left(\Delta x\right)^2}=0$.

这是 $\frac00$ 型未定式(因 $g\left(a\right)=0$ 且 $g''\left(a\right)=0$ 推出 $g'\left(a\right)=0$). 洛必达法则(**定理 2.2**)的理论基础是**定理 2.1**（柯西中值定理）. 由**定理 2.2**（洛必达法则）, 
$$
\lim_{\Delta x\to0}\frac{g\left(x\right)}{\left(\Delta x\right)^2}=\lim_{\Delta x\to0}\frac{g'\left(x\right)}{2\Delta x}.
$$

右端仍是 $\frac00$ 型(因 $g'\left(a\right)=0$). 再用一次**定理 2.2**（洛必达法则）, 
$$
\lim_{\Delta x\to0}\frac{g'\left(x\right)}{2\Delta x}=\lim_{\Delta x\to0}\frac{g''\left(x\right)}{2}=\frac{g''\left(a\right)}{2}=0.
$$

这里用到了 $g''$ 在 $a$ 点的连续性(由 $f$ 在 $a$ 点有二阶导数推出). 故 $g\left(x\right)=o\left(\left(\Delta x\right)^2\right)$, 即
$$
f\left(x\right)=T\left(x\right)+o\left(\left(x-a\right)^2\right)\left(x\to a\right).
$$

$\blacksquare$
### 习题四

（习题 3.2-6）设 $c$ 为常数, 问 $c$ 为何值时, 有
$$
\lim_{x\to\infty}\left(\frac{x+c}{x-c}\right)^x=e^2.
$$
### 解答 习题四

这是 $1^\infty$ 型未定式. 令 $y=\left(\frac{x+c}{x-c}\right)^x$, 则
$$
\ln y=x\ln\frac{x+c}{x-c}=x\ln\left(1+\frac{2c}{x-c}\right).
$$

当 $x\to\infty$ 时, $\frac{2c}{x-c}\to0$, 利用等价无穷小 $\ln\left(1+t\right)\sim t$($t\to0$), 得
$$
\ln y\sim x\cdot\frac{2c}{x-c}=\frac{2cx}{x-c}\to2c\left(x\to\infty\right).
$$

也可由洛必达法则验证: 将 $\ln y$ 改写为 $\frac{\ln\left(\frac{x+c}{x-c}\right)}{1/x}$, 这是 $\frac00$ 型. 由**定理 2.2**（洛必达法则）, 
$$
\lim_{x\to\infty}\frac{\ln\left(\frac{x+c}{x-c}\right)}{1/x}=\lim_{x\to\infty}\frac{\frac{x-c}{x+c}\cdot\frac{\left(x-c\right)-\left(x+c\right)}{\left(x-c\right)^2}}{-1/x^2}=\lim_{x\to\infty}\frac{-2c}{x^2-c^2}\cdot\left(-x^2\right)=2c.
$$

故 $\lim\limits_{x\to\infty}y=e^{2c}$. 由题设 $e^{2c}=e^2$, 得 $2c=2$, 即 $c=1$. $\blacksquare$
