# week15

> **定理 1.1 (费马定理)**
> 
> 设 $f\left(x\right)$ 在一点 $a$ 附近有定义, 且在 $a$ 点可微. 若 $a$ 点为 $y=f\left(x\right)$ 的极值点, 则 $f'\left(a\right)=0$.

> **定理 1.2 (罗尔定理)**
> 
> 设函数 $y=f\left(x\right)$ 在闭区间 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 中处处可导, 且 $f\left(a\right)=f\left(b\right)$. 则在 $\left(a,b\right)$ 中至少存在一点 $c$, 使得 $f'\left(c\right)=0$.

> **定理 1.3 (拉格朗日中值定理)**
> 
> 设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 内可导. 则存在 $c\in\left(a,b\right)$, 使得 $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

> **定理 1.4 (常数定理)**
> 
> 设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中处处可导, 且 $f'\left(x\right)=0$ ($x\in\left(a,b\right)$). 则 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 内必为常数.

> **定理 1.5 (单调性判定)**
> 
> 设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 可导. 若 $f'\left(x\right)>0$ ($\ge0$) 对一切 $x\in\left(a,b\right)$, 则 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上严格递增 (递增); 若 $f'\left(x\right)<0$ ($\le0$) 对一切 $x\in\left(a,b\right)$, 则严格递减 (递减).

> **定理 2.1 (柯西中值定理)**
> 
> 设 $y=f\left(x\right)$ 与 $y=g\left(x\right)$ 在 $\left[a,b\right]$ 中连续, 在 $\left(a,b\right)$ 中可导, 且 $g'\left(x\right)\ne0$ ($a<{}x<{}b$). 则存在点 $c\in\left(a,b\right)$, 使得 $\frac{f\left(b\right)-f\left(a\right)}{g\left(b\right)-g\left(a\right)}=\frac{f'\left(c\right)}{g'\left(c\right)}$.

> **定理 2.2 (洛必达法则, $\frac00$ 型)**
> 
> 设 $f$ 及 $g$ 在 $a$ 点的一个空心邻域内有定义且可导, $g'\left(x\right)\ne0$. 假定 $\lim_{x\to{a}}f\left(x\right)=\lim_{x\to{a}}g\left(x\right)=0$, 且 $\lim_{x\to{a}}\frac{f'\left(x\right)}{g'\left(x\right)}$ 存在. 则 $\lim_{x\to{a}}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to{a}}\frac{f'\left(x\right)}{g'\left(x\right)}$.

> **定理 2.3 (洛必达法则, $\frac{\infty}{\infty}$ 型)**
> 
> 设 $f$ 与 $g$ 在 $a$ 点的一个空心邻域内有定义且可导, $g'\left(x\right)\ne0$. 假定 $\lim_{x\to{a}}f\left(x\right)=\lim_{x\to{a}}g\left(x\right)=\infty$, 且 $\lim_{x\to{a}}\frac{f'\left(x\right)}{g'\left(x\right)}$ 存在. 则 $\lim_{x\to{a}}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to{a}}\frac{f'\left(x\right)}{g'\left(x\right)}$.

## 3.1-14

设

$$
f\left(x\right)=\arctan\frac{1+x}{1-x}-\arctan{x},
$$

又设 $\left(a,b\right)$ 是不包含 $x=1$ 的任意一个区间. 证明 $f\left(x\right)=C$ 对一切 $x\in\left(a,b\right)$ 成立, $C$ 为常数. 令 $\left(a,b\right)=\left(-\infty,1\right)$, 试证这时 $C=\frac\pi4$. 又问: 当 $x\in\left(1,+\infty\right)$ 时, $C$ 为何值?

### 解答 3.1-14

求导得

$$
f'\left(x\right)=\frac{1}{1+\left(\frac{1+x}{1-x}\right)^2}\cdot\frac{2}{\left(1-x\right)^2}-\frac1{1+x^2}=\frac{2}{\left(1-x\right)^2+\left(1+x\right)^2}-\frac1{1+x^2}=\frac1{1+x^2}-\frac1{1+x^2}=0.
$$

由**定理 1.4 (常数定理)**, $f\left(x\right)$ 在 $\left(a,b\right)$ 内为常数, 记为 $C$.

当 $\left(a,b\right)=\left(-\infty,1\right)$ 时, 取 $x=0$, 则

$$
f\left(0\right)=\arctan1-\arctan0=\frac\pi4.
$$

故 $C=\frac\pi4$, 即

$$
\arctan\frac{1+x}{1-x}=\arctan{x}+\frac\pi4\quad\left(x<1\right).
$$

当 $x\in\left(1,+\infty\right)$ 时, 取 $x\to+\infty$, 则 $\frac{1+x}{1-x}\to-1$, $\arctan\frac{1+x}{1-x}\to-\frac\pi4$, 而 $\arctan{x}\to\frac\pi2$. 故

$$
C=\lim_{x\to+\infty}f\left(x\right)=-\frac\pi4-\frac\pi2=-\frac{3\pi}4.
$$

$\blacksquare$

## 3.2-1

求下列未定式的极限:

(1) $\lim_{x\to0}\frac{\ln\left(\cos{a}x\right)}{\ln\left(\cos{b}x\right)}$ ($a\ne0$, $b\ne0$);

(2) $\lim_{x\to0}\frac{a^x-1}{x}$ ($a>0$);

(3) $\lim_{x\to0}\frac{\tan{x}-x}{x-\arcsin{x}}$;

(4) $\lim_{x\to0+}x^x$;

(5) $\lim_{x\to0+}x\ln{x}$;

(6) $\lim_{x\to0+}\frac{\ln\left(\sin{x}\right)}{x^2}$;

(7) $\lim_{x\to0+}\left(\sin{x}\right)^{\sin{x}}$.

### 解答 3.2-1

(1) 这是 $\frac00$ 型. 由**定理 2.2 (洛必达法则, $\frac00$ 型)**,

$$
\lim_{x\to0}\frac{\ln\left(\cos{a}x\right)}{\ln\left(\cos{b}x\right)}=\lim_{x\to0}\frac{\frac{-a\sin{a}x}{\cos{a}x}}{\frac{-b\sin{b}x}{\cos{b}x}}=\lim_{x\to0}\frac{a\tan{a}x}{b\tan{b}x}=\frac{a^2}{b^2}.
$$

(2) 这是 $\frac00$ 型. 由**定理 2.2 (洛必达法则, $\frac00$ 型)**,

$$
\lim_{x\to0}\frac{a^x-1}{x}=\lim_{x\to0}\frac{a^x\ln{a}}{1}=\ln{a}.
$$

(3) 这是 $\frac00$ 型. 由**定理 2.2 (洛必达法则, $\frac00$ 型)**,

$$
\lim_{x\to0}\frac{\tan{x}-x}{x-\arcsin{x}}=\lim_{x\to0}\frac{\sec^2x-1}{1-\frac1{\sqrt{1-x^2}}}.
$$

分子 $\sec^2x-1=\tan^2x\sim{x}^2$. 分母 $1-\frac1{\sqrt{1-x^2}}\sim-\frac{x^2}{2}$. 故极限为 $\frac{x^2}{-x^2/2}=-2$.

(4) 这是 $0^0$ 型. 令 $y=x^x$, 则 $\ln{y}=x\ln{x}$. 由 (5) 知 $\lim_{x\to0+}x\ln{x}=0$, 故 $\lim_{x\to0+}x^x=e^0=1$.

(5) 这是 $0\cdot\infty$ 型. 改写为 $\frac{\infty}{\infty}$ 后应用**定理 2.3 (洛必达法则, $\frac{\infty}{\infty}$ 型)**:

$$
\lim_{x\to0+}x\ln{x}=\lim_{x\to0+}\frac{\ln{x}}{1/x}=\lim_{x\to0+}\frac{1/x}{-1/x^2}=\lim_{x\to0+}\left(-x\right)=0.
$$

(6) 这是 $\frac{\infty}{\infty}$ 型. 由**定理 2.3 (洛必达法则, $\frac{\infty}{\infty}$ 型)**,

$$
\lim_{x\to0+}\frac{\ln\left(\sin{x}\right)}{x^2}=\lim_{x\to0+}\frac{\cot{x}}{2x}=\lim_{x\to0+}\frac{\cos{x}}{2x\sin{x}}=+\infty.
$$

(7) 这是 $0^0$ 型. 令 $y=\left(\sin{x}\right)^{\sin{x}}$, 则 $\ln{y}=\sin{x}\ln\left(\sin{x}\right)$. 由 (5) 的结果 (将 $x$ 换成 $\sin{x}$), $\lim_{x\to0+}\sin{x}\ln\left(\sin{x}\right)=0$. 故 $\lim_{x\to0+}\left(\sin{x}\right)^{\sin{x}}=e^0=1$. $\blacksquare$

## 3.2-2

若 $\lim_{x\to{a}}\frac{f'\left(x\right)}{g'\left(x\right)}$ 不存在, 能否说明 $\lim_{x\to{a}}\frac{f\left(x\right)}{g\left(x\right)}$ 也不存在? 试考察 $f\left(x\right)=x^2\sin\frac1x$ 及 $g\left(x\right)=x$ 在 $x\to0$ 时的情况.

### 解答 3.2-2

不能. 取 $f\left(x\right)=x^2\sin\frac1x$, $g\left(x\right)=x$, $x\to0$.

首先,

$$
\lim_{x\to0}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to0}x\sin\frac1x=0.
$$

而

$$
f'\left(x\right)=2x\sin\frac1x-\cos\frac1x,\quad{g}'\left(x\right)=1.
$$

于是 $\frac{f'\left(x\right)}{g'\left(x\right)}=2x\sin\frac1x-\cos\frac1x$. 当 $x\to0$ 时, $2x\sin\frac1x\to0$, 但 $\cos\frac1x$ 振荡无极限. 故 $\lim_{x\to0}\frac{f'\left(x\right)}{g'\left(x\right)}$ 不存在.

这说明: $\lim\frac{f'}{g'}$ 不存在时, $\lim\frac{f}{g}$ 仍可能存在, 即洛必达法则的逆命题不成立. $\blacksquare$

## 3.2-4

设 $y=f\left(x\right)$ 在 $a$ 点有二阶导数, 并令

$$
T\left(x\right)=f\left(a\right)+f'\left(a\right)\Delta{x}+\frac{f''\left(a\right)}2\left(\Delta{x}\right)^2,
$$

其中 $\Delta{x}=x-a$. 证明: 函数 $g\left(x\right)=f\left(x\right)-T\left(x\right)$ 满足 $g\left(a\right)=0$, $g'\left(a\right)=0$, $g''\left(a\right)=0$, 且 $f\left(x\right)=T\left(x\right)+o\left(\left(\Delta{x}\right)^2\right)$ ($x\to{a}$).

### 解答 3.2-4

由 $T\left(x\right)$ 的定义, $T\left(a\right)=f\left(a\right)$, $T'\left(x\right)=f'\left(a\right)+f''\left(a\right)\Delta{x}$, $T''\left(x\right)=f''\left(a\right)$.

计算得

$$
g\left(a\right)=f\left(a\right)-T\left(a\right)=0,
$$

$$
g'\left(a\right)=f'\left(a\right)-T'\left(a\right)=0,
$$

$$
g''\left(a\right)=f''\left(a\right)-T''\left(a\right)=0.
$$

下面证明 $g\left(x\right)=o\left(\left(\Delta{x}\right)^2\right)$. 这是 $\frac00$ 型. 由**定理 2.2 (洛必达法则, $\frac00$ 型)**,

$$
\lim_{\Delta{x}\to0}\frac{g\left(x\right)}{\left(\Delta{x}\right)^2}=\lim_{\Delta{x}\to0}\frac{g'\left(x\right)}{2\Delta{x}}.
$$

右端仍是 $\frac00$ 型. 再用一次**定理 2.2 (洛必达法则, $\frac00$ 型)**,

$$
\lim_{\Delta{x}\to0}\frac{g'\left(x\right)}{2\Delta{x}}=\lim_{\Delta{x}\to0}\frac{g''\left(x\right)}2=\frac{g''\left(a\right)}2=0.
$$

这里用到了 $g''$ 在 $a$ 点的连续性. 故 $g\left(x\right)=o\left(\left(\Delta{x}\right)^2\right)$, 即 $f\left(x\right)=T\left(x\right)+o\left(\left(x-a\right)^2\right)$. $\blacksquare$
