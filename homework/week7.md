# week7

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

## 3.1-1

设 $y=f\left(x\right)$ 在 $\left(-\infty,+\infty\right)$ 内可导, 且 $\lim_{x\to-\infty}f\left(x\right)=\lim_{x\to+\infty}f\left(x\right)$. 证明: 存在一点 $c\in\left(-\infty,+\infty\right)$ 使得 $f'\left(c\right)=0$.

### 解答 3.1-1

记

$$
l=\lim_{x\to-\infty}f\left(x\right)=\lim_{x\to+\infty}f\left(x\right).
$$

若 $f\left(x\right)\equiv{}l$, 则 $f'\left(x\right)\equiv0$, 结论显然成立.

若 $f$ 不恒等于 $l$, 则存在 $x_0$ 使得 $f\left(x_0\right)\ne{}l$. 不妨设 $f\left(x_0\right)>l$. 由 $\lim_{x\to\pm\infty}f\left(x\right)=l$, 取 $\varepsilon=\frac{f\left(x_0\right)-l}{2}>0$, 则存在 $A>\left|x_0\right|$, 使得当 $\left|x\right|>A$ 时 $\left|f\left(x\right)-l\right|<\varepsilon$, 即

$$
f\left(x\right)<{}l+\varepsilon=\frac{f\left(x_0\right)+l}{2}<{}f\left(x_0\right).
$$

考虑闭区间 $\left[-A,A\right]$ 上的连续函数 $f$. 由于 $f\left(-A\right)<{}f\left(x_0\right)$ 且 $f\left(A\right)<{}f\left(x_0\right)$, 而 $x_0\in\left(-A,A\right)$, 故 $f$ 在 $\left[-A,A\right]$ 上的最大值不在端点处达到, 而在某点 $c\in\left(-A,A\right)$ 处达到. 于是 $c$ 为极大值点. 又 $f$ 在 $\left(-A,A\right)$ 内可导, 由**定理 1.1 (费马定理)**, $f'\left(c\right)=0$.

$\blacksquare$

## 3.1-2

设 $p\left(x\right)=x^n+qx+r$ ($n$ 为正整数, $q,r$ 为实数). 证明: $n$ 为偶数时至多有两个实根; $n$ 为奇数时至多有三个实根.

### 解答 3.1-2

反证法. 设 $n$ 为偶数, 假定 $p\left(x\right)$ 至少有三个不同的实根 $x_1<{}x_2<{}x_3$. 由**定理 1.2 (罗尔定理)**, 在 $\left(x_1,x_2\right)$ 与 $\left(x_2,x_3\right)$ 内分别存在点 $\xi_1,\xi_2$, 使得

$$
p'\left(\xi_1\right)=0,\quad{}p'\left(\xi_2\right)=0.
$$

而 $p'\left(x\right)=nx^{n-1}+q$. 因 $n$ 为偶数, $n-1$ 为奇数, 方程 $nx^{n-1}+q=0$ 至多有一个实根. 这与 $p'\left(\xi_1\right)=p'\left(\xi_2\right)=0$ 且 $\xi_1\ne\xi_2$ 矛盾. 故 $n$ 为偶数时 $p\left(x\right)$ 至多有两个实根.

设 $n$ 为奇数, 假定 $p\left(x\right)$ 至少有四个不同的实根 $x_1<{}x_2<{}x_3<{}x_4$. 由**定理 1.2 (罗尔定理)**, 在 $\left(x_1,x_2\right)$, $\left(x_2,x_3\right)$, $\left(x_3,x_4\right)$ 内分别存在 $\xi_1,\xi_2,\xi_3$, 使得

$$
p'\left(\xi_1\right)=p'\left(\xi_2\right)=p'\left(\xi_3\right)=0.
$$

再对 $p'\left(x\right)$ 使用**定理 1.2 (罗尔定理)**, 在 $\left(\xi_1,\xi_2\right)$ 与 $\left(\xi_2,\xi_3\right)$ 内分别存在 $\eta_1,\eta_2$, 使得

$$
p''\left(\eta_1\right)=0,\quad{}p''\left(\eta_2\right)=0.
$$

而 $p''\left(x\right)=n\left(n-1\right)x^{n-2}$. 因 $n$ 为奇数, $n-2$ 亦为奇数, 方程 $n\left(n-1\right)x^{n-2}=0$ 只有一个实根 $x=0$. 这与 $p''\left(\eta_1\right)=p''\left(\eta_2\right)=0$ 且 $\eta_1\ne\eta_2$ 矛盾. 故 $n$ 为奇数时 $p\left(x\right)$ 至多有三个实根.

$\blacksquare$

## 3.1-4

确定下列函数的单调区间:

(1) $f\left(x\right)=xe^x$;

(2) $f\left(x\right)=\frac{x^2-1}{x}$;

(3) $f\left(x\right)=\sqrt{x-2}$;

(4) $f\left(x\right)=x^4-x+1$.

### 解答 3.1-4

(1) $f'\left(x\right)=e^x+xe^x=\left(1+x\right)e^x$. 因 $e^x>0$, 故 $f'\left(x\right)$ 的符号由 $1+x$ 决定. 当 $x<-1$ 时 $f'\left(x\right)<0$, 当 $x>-1$ 时 $f'\left(x\right)>0$. 由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left(-\infty,-1\right]$ 上严格递减, 在 $\left[-1,+\infty\right)$ 上严格递增.

(2) $f\left(x\right)=x-\frac1x$, 定义域为 $\left(-\infty,0\right)\cup\left(0,+\infty\right)$. $f'\left(x\right)=1+\frac1{x^2}>0$. 由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left(-\infty,0\right)$ 与 $\left(0,+\infty\right)$ 上均严格递增.

(3) 定义域为 $\left[2,+\infty\right)$. $f'\left(x\right)=\frac1{2\sqrt{x-2}}>0$ ($x>2$). 由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left[2,+\infty\right)$ 上严格递增.

(4) $f'\left(x\right)=4x^3-1$. 令 $f'\left(x\right)=0$, 得 $x=\sqrt[3]{\frac14}$. 当 $x<\sqrt[3]{\frac14}$ 时 $f'\left(x\right)<0$, 当 $x>\sqrt[3]{\frac14}$ 时 $f'\left(x\right)>0$. 由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left(-\infty,\sqrt[3]{\frac14}\right]$ 上严格递减, 在 $\left[\sqrt[3]{\frac14},+\infty\right)$ 上严格递增.

$\blacksquare$

## 3.1-5

设 $f\left(x\right)$ 与 $g\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 中可导, 且有 $f'\left(x\right)>g'\left(x\right)$. 假定 $f\left(a\right)=g\left(a\right)$, 证明 $f\left(x\right)>g\left(x\right)$ 对一切 $x\in\left(a,b\right]$ 成立.

### 解答 3.1-5

令 $h\left(x\right)=f\left(x\right)-g\left(x\right)$. 由题设, $h\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 中可导, 且

$$
h'\left(x\right)=f'\left(x\right)-g'\left(x\right)>0\quad\left(\forall{}x\in\left(a,b\right)\right).
$$

由**定理 1.5 (单调性判定)**, $h\left(x\right)$ 在 $\left[a,b\right]$ 上严格递增. 又 $h\left(a\right)=f\left(a\right)-g\left(a\right)=0$, 故对任意 $x\in\left(a,b\right]$, 有

$$
h\left(x\right)>h\left(a\right)=0,
$$

即 $f\left(x\right)-g\left(x\right)>0$, 亦即 $f\left(x\right)>g\left(x\right)$.

$\blacksquare$

## 3.1-6

证明下列不等式:

(1) $\ln\left(1+x\right)<{}x$ ($x>0$);

(2) $\cos{}x>1-\frac{x^2}{2}$ ($x\ne0$);

(3) $\sin{}x<{}x$ ($x>0$);

(4) $\tan{}x>x$ ($0<{}x<\frac\pi2$).

### 解答 3.1-6

(1) 令 $f\left(x\right)=\ln\left(1+x\right)-x$. 则 $f\left(0\right)=0$, 且

$$
f'\left(x\right)=\frac1{1+x}-1=-\frac{x}{1+x}<0\quad\left(x>0\right).
$$

由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left[0,+\infty\right)$ 上严格递减. 故当 $x>0$ 时 $f\left(x\right)<{}f\left(0\right)=0$, 即 $\ln\left(1+x\right)<{}x$.

(2) 令 $f\left(x\right)=\cos{}x-1+\frac{x^2}{2}$. 则 $f\left(0\right)=0$, 且 $f'\left(x\right)=-\sin{}x+x$. 由 (3), 当 $x>0$ 时 $\sin{}x<{}x$, 故 $f'\left(x\right)=x-\sin{}x>0$. 由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left[0,+\infty\right)$ 上严格递增. 故当 $x>0$ 时 $f\left(x\right)>f\left(0\right)=0$, 即 $\cos{}x>1-\frac{x^2}{2}$. 当 $x<0$ 时由偶函数性质得同样结论.

(3) 令 $f\left(x\right)=x-\sin{}x$. 则 $f\left(0\right)=0$, 且 $f'\left(x\right)=1-\cos{}x\ge0$, 且 $f'\left(x\right)=0$ 仅在孤立点 $x=2k\pi$ 处成立. 由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left[0,+\infty\right)$ 上严格递增. 故当 $x>0$ 时 $f\left(x\right)>f\left(0\right)=0$, 即 $\sin{}x<{}x$.

(4) 令 $f\left(x\right)=\tan{}x-x$. 则 $f\left(0\right)=0$, 且

$$
f'\left(x\right)=\sec^2x-1=\tan^2x>0\quad\left(0<{}x<\frac\pi2\right).
$$

由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left[0,\frac\pi2\right)$ 上严格递增. 故当 $0<{}x<\frac\pi2$ 时 $f\left(x\right)>f\left(0\right)=0$, 即 $\tan{}x>x$.

$\blacksquare$

## 3.1-8

设 $f\left(x\right)$ 在 $x_0$ 点的一个邻域 $U$ 内连续, 并在 $x_0$ 点的空心邻域 $U\setminus\left\{x_0\right\}$ 中可导. 试证明: 若极限 $\lim_{x\to{}x_0}f'\left(x\right)$ 存在, 则 $f\left(x\right)$ 在 $x_0$ 点可导, 且 $f'\left(x_0\right)=\lim_{x\to{}x_0}f'\left(x\right)$.

### 解答 3.1-8

设 $\lim_{x\to{}x_0}f'\left(x\right)=A$. 对任意 $x\in{}U\setminus\left\{x_0\right\}$, 在以 $x_0$ 与 $x$ 为端点的闭区间上应用**定理 1.3 (拉格朗日中值定理)**, 存在介于 $x_0$ 与 $x$ 之间的点 $\xi$, 使得

$$
f\left(x\right)-f\left(x_0\right)=f'\left(\xi\right)\left(x-x_0\right).
$$

于是

$$
\frac{f\left(x\right)-f\left(x_0\right)}{x-x_0}=f'\left(\xi\right).
$$

当 $x\to{}x_0$ 时, $\xi\to{}x_0$. 由题设 $\lim_{x\to{}x_0}f'\left(x\right)=A$, 故

$$
\lim_{x\to{}x_0}\frac{f\left(x\right)-f\left(x_0\right)}{x-x_0}=\lim_{\xi\to{}x_0}f'\left(\xi\right)=A.
$$

由导数的定义, $f$ 在 $x_0$ 点可导, 且 $f'\left(x_0\right)=A=\lim_{x\to{}x_0}f'\left(x\right)$.

$\blacksquare$

## 3.1-10

证明达布定理: 设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中可导. 若存在 $x_1,x_2\in\left(a,b\right)$, 使得 $f'\left(x_1\right)>0$, $f'\left(x_2\right)<0$, 则 $x_1$ 与 $x_2$ 之间有一点 $c$, 使得 $f'\left(c\right)=0$.

### 解答 3.1-10

不妨设 $x_1<{}x_2$. 由 $f'\left(x_1\right)>0$, 根据导数定义, 存在 $\delta_1>0$, 使得当 $x\in\left(x_1,x_1+\delta_1\right)$ 时

$$
\frac{f\left(x\right)-f\left(x_1\right)}{x-x_1}>0,
$$

即 $f\left(x\right)>f\left(x_1\right)$. 同理, 由 $f'\left(x_2\right)<0$, 存在 $\delta_2>0$, 使得当 $x\in\left(x_2-\delta_2,x_2\right)$ 时

$$
\frac{f\left(x\right)-f\left(x_2\right)}{x-x_2}<0.
$$

因 $x-x_2<0$, 故 $f\left(x\right)-f\left(x_2\right)>0$, 即 $f\left(x\right)>f\left(x_2\right)$.

考虑 $f$ 在闭区间 $\left[x_1,x_2\right]$ 上的最大值. 由上述讨论, $f$ 在 $x_1$ 右侧附近的点处函数值大于 $f\left(x_1\right)$, 故最大值不在 $x_1$ 处达到; 同理, 最大值不在 $x_2$ 处达到. 因此最大值在某点 $c\in\left(x_1,x_2\right)$ 处达到, 即 $c$ 为极大值点. 又 $f$ 在 $\left(a,b\right)$ 内可导, 由**定理 1.1 (费马定理)**, $f'\left(c\right)=0$.

$\blacksquare$

## 3.1-11

证明: 若 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 区间中可导, 且 $f'\left(x\right)\ne0$, 则 $f$ 在 $\left(a,b\right)$ 中要么严格递增, 要么严格递减.

### 解答 3.1-11

用反证法. 假定 $f$ 在 $\left(a,b\right)$ 中既不严格递增也不严格递减. 则由**定理 1.3 (拉格朗日中值定理)**, 存在两点使得 $f$ 的增量为正, 又存在两点使得 $f$ 的增量为负, 故 $f'$ 在某处取正值, 在某处取负值. 由 3.1-10 的达布定理, $f'$ 必取零值, 与 $f'\left(x\right)\ne0$ 矛盾. 故 $f$ 只能严格递增或严格递减.

$\blacksquare$

## 3.1-13

证明不等式 $e^x>1+x$ ($x>0$).

### 解答 3.1-13

令 $f\left(x\right)=e^x-1-x$. 则 $f\left(0\right)=0$, 且

$$
f'\left(x\right)=e^x-1>0\quad\left(x>0\right).
$$

由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left[0,+\infty\right)$ 上严格递增. 故当 $x>0$ 时 $f\left(x\right)>f\left(0\right)=0$, 即 $e^x>1+x$.

$\blacksquare$

## 3.1-14

设

$$
f\left(x\right)=\arctan\frac{1+x}{1-x}-\arctan{}x,
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
\arctan\frac{1+x}{1-x}=\arctan{}x+\frac\pi4\quad\left(x<1\right).
$$

当 $x\in\left(1,+\infty\right)$ 时, 取 $x\to+\infty$, 则 $\frac{1+x}{1-x}\to-1$, $\arctan\frac{1+x}{1-x}\to-\frac\pi4$, 而 $\arctan{}x\to\frac\pi2$. 故

$$
C=\lim_{x\to+\infty}f\left(x\right)=-\frac\pi4-\frac\pi2=-\frac{3\pi}4.
$$

$\blacksquare$

## 3.2-1

求下列未定式的极限:

(1) $\lim_{x\to0}\frac{\ln\left(\cos{}ax\right)}{\ln\left(\cos{}bx\right)}$ ($a\ne0$, $b\ne0$);

(2) $\lim_{x\to0}\frac{a^x-1}{x}$ ($a>0$);

(3) $\lim_{x\to0}\frac{\tan{}x-x}{x-\arcsin{}x}$;

(4) $\lim_{x\to0+}x^x$;

(5) $\lim_{x\to0+}x\ln{}x$;

(6) $\lim_{x\to0+}\frac{\ln\left(\sin{}x\right)}{x^2}$;

(7) $\lim_{x\to0+}\left(\sin{}x\right)^{\sin{}x}$.

### 解答 3.2-1

(1) 这是 $\frac00$ 型. 由**定理 2.2 (洛必达法则, $\frac00$ 型)**,

$$
\lim_{x\to0}\frac{\ln\left(\cos{}ax\right)}{\ln\left(\cos{}bx\right)}=\lim_{x\to0}\frac{\frac{-a\sin{}ax}{\cos{}ax}}{\frac{-b\sin{}bx}{\cos{}bx}}=\lim_{x\to0}\frac{a\tan{}ax}{b\tan{}bx}=\frac{a^2}{b^2}.
$$

(2) 这是 $\frac00$ 型. 由**定理 2.2 (洛必达法则, $\frac00$ 型)**,

$$
\lim_{x\to0}\frac{a^x-1}{x}=\lim_{x\to0}\frac{a^x\ln{}a}{1}=\ln{}a.
$$

(3) 这是 $\frac00$ 型. 由**定理 2.2 (洛必达法则, $\frac00$ 型)**,

$$
\lim_{x\to0}\frac{\tan{}x-x}{x-\arcsin{}x}=\lim_{x\to0}\frac{\sec^2x-1}{1-\frac1{\sqrt{1-x^2}}}.
$$

分子 $\sec^2x-1=\tan^2x\sim{}x^2$. 分母 $1-\frac1{\sqrt{1-x^2}}\sim-\frac{x^2}{2}$. 故极限为 $\frac{x^2}{-x^2/2}=-2$.

(4) 这是 $0^0$ 型. 令 $y=x^x$, 则 $\ln{}y=x\ln{}x$. 由 (5) 知 $\lim_{x\to0+}x\ln{}x=0$, 故 $\lim_{x\to0+}x^x=e^0=1$.

(5) 这是 $0\cdot\infty$ 型. 改写为 $\frac{\infty}{\infty}$ 后应用**定理 2.3 (洛必达法则, $\frac{\infty}{\infty}$ 型)**:

$$
\lim_{x\to0+}x\ln{}x=\lim_{x\to0+}\frac{\ln{}x}{1/x}=\lim_{x\to0+}\frac{1/x}{-1/x^2}=\lim_{x\to0+}\left(-x\right)=0.
$$

(6) 这是 $\frac{\infty}{\infty}$ 型. 由**定理 2.3 (洛必达法则, $\frac{\infty}{\infty}$ 型)**,

$$
\lim_{x\to0+}\frac{\ln\left(\sin{}x\right)}{x^2}=\lim_{x\to0+}\frac{\cot{}x}{2x}=\lim_{x\to0+}\frac{\cos{}x}{2x\sin{}x}=+\infty.
$$

(7) 这是 $0^0$ 型. 令 $y=\left(\sin{}x\right)^{\sin{}x}$, 则 $\ln{}y=\sin{}x\ln\left(\sin{}x\right)$. 由 (5) 的结果 (将 $x$ 换成 $\sin{}x$), $\lim_{x\to0+}\sin{}x\ln\left(\sin{}x\right)=0$. 故 $\lim_{x\to0+}\left(\sin{}x\right)^{\sin{}x}=e^0=1$.

$\blacksquare$

## 3.2-2

若 $\lim_{x\to{}a}\frac{f'\left(x\right)}{g'\left(x\right)}$ 不存在, 能否说明 $\lim_{x\to{}a}\frac{f\left(x\right)}{g\left(x\right)}$ 也不存在? 试考察 $f\left(x\right)=x^2\sin\frac1x$ 及 $g\left(x\right)=x$ 在 $x\to0$ 时的情况.

### 解答 3.2-2

不能. 取 $f\left(x\right)=x^2\sin\frac1x$, $g\left(x\right)=x$, $x\to0$.

首先,

$$
\lim_{x\to0}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to0}x\sin\frac1x=0.
$$

而

$$
f'\left(x\right)=2x\sin\frac1x-\cos\frac1x,\quad{}g'\left(x\right)=1.
$$

于是 $\frac{f'\left(x\right)}{g'\left(x\right)}=2x\sin\frac1x-\cos\frac1x$. 当 $x\to0$ 时, $2x\sin\frac1x\to0$, 但 $\cos\frac1x$ 振荡无极限. 故 $\lim_{x\to0}\frac{f'\left(x\right)}{g'\left(x\right)}$ 不存在.

这说明: $\lim\frac{f'}{g'}$ 不存在时, $\lim\frac{f}{g}$ 仍可能存在, 即洛必达法则的逆命题不成立.

$\blacksquare$

## 3.2-4

设 $y=f\left(x\right)$ 在 $a$ 点有二阶导数, 并令

$$
T\left(x\right)=f\left(a\right)+f'\left(a\right)\Delta{}x+\frac{f''\left(a\right)}2\left(\Delta{}x\right)^2,
$$

其中 $\Delta{}x=x-a$. 证明: 函数 $g\left(x\right)=f\left(x\right)-T\left(x\right)$ 满足 $g\left(a\right)=0$, $g'\left(a\right)=0$, $g''\left(a\right)=0$, 且 $f\left(x\right)=T\left(x\right)+o\left(\left(\Delta{}x\right)^2\right)$ ($x\to{}a$).

### 解答 3.2-4

由 $T\left(x\right)$ 的定义, $T\left(a\right)=f\left(a\right)$, $T'\left(x\right)=f'\left(a\right)+f''\left(a\right)\Delta{}x$, $T''\left(x\right)=f''\left(a\right)$.

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

下面证明 $g\left(x\right)=o\left(\left(\Delta{}x\right)^2\right)$. 这是 $\frac00$ 型. 由**定理 2.2 (洛必达法则, $\frac00$ 型)**,

$$
\lim_{\Delta{}x\to0}\frac{g\left(x\right)}{\left(\Delta{}x\right)^2}=\lim_{\Delta{}x\to0}\frac{g'\left(x\right)}{2\Delta{}x}.
$$

右端仍是 $\frac00$ 型. 再用一次**定理 2.2 (洛必达法则, $\frac00$ 型)**,

$$
\lim_{\Delta{}x\to0}\frac{g'\left(x\right)}{2\Delta{}x}=\lim_{\Delta{}x\to0}\frac{g''\left(x\right)}2=\frac{g''\left(a\right)}2=0.
$$

这里用到了 $g''$ 在 $a$ 点的连续性. 故 $g\left(x\right)=o\left(\left(\Delta{}x\right)^2\right)$, 即 $f\left(x\right)=T\left(x\right)+o\left(\left(x-a\right)^2\right)$.

$\blacksquare$

## 3.2-6

设 $c$ 为常数, 问 $c$ 为何值时, 有 $\lim_{x\to\infty}\left(\frac{x+c}{x-c}\right)^x=e^2$.

### 解答 3.2-6

这是 $1^\infty$ 型. 令 $y=\left(\frac{x+c}{x-c}\right)^x$, 则

$$
\ln{}y=x\ln\frac{x+c}{x-c}=x\ln\left(1+\frac{2c}{x-c}\right).
$$

当 $x\to\infty$ 时, $\frac{2c}{x-c}\to0$, 利用等价无穷小 $\ln\left(1+t\right)\sim{}t$, 得

$$
\ln{}y\sim{}x\cdot\frac{2c}{x-c}=\frac{2cx}{x-c}\to2c.
$$

故 $\lim_{x\to\infty}y=e^{2c}$. 由题设 $e^{2c}=e^2$, 得 $2c=2$, 即 $c=1$.

$\blacksquare$

## 3.3-1-1

求函数 $y=x\left(3x^2-5\right)^2$ 的稳定点, 并判断这些稳定点是否为极值点.

### 解答 3.3-1-1

求导得

$$
y'=\left(3x^2-5\right)^2+x\cdot2\left(3x^2-5\right)\cdot6x=\left(3x^2-5\right)\left(15x^2-5\right)=5\left(3x^2-5\right)\left(3x^2-1\right).
$$

令 $y'=0$, 得稳定点 $x=\pm\sqrt{\frac53}$, $\pm\frac1{\sqrt3}$.

再求二阶导数:

$$
y''=30x\left(30x^2-26\right).
$$

代入各稳定点:

- $x=\sqrt{\frac53}$: $y''>0$, 故为极小值点.
- $x=-\sqrt{\frac53}$: $y''<0$, 故为极大值点.
- $x=\frac1{\sqrt3}$: $y''<0$, 故为极大值点.
- $x=-\frac1{\sqrt3}$: $y''>0$, 故为极小值点.

由**定理 3.2 (极值点第二充分条件)**, 上述判断成立.

$\blacksquare$

## 3.3-1-3

求函数 $y=x\ln{}x$ ($x>0$) 的稳定点, 并判断这些稳定点是否为极值点.

### 解答 3.3-1-3

求导得 $y'=\ln{}x+1$. 令 $y'=0$, 得 $x=\frac1e$.

再求二阶导数: $y''=\frac1x>0$ ($x>0$). 故 $y''\left(\frac1e\right)=e>0$. 由**定理 3.2 (极值点第二充分条件)**, $x=\frac1e$ 为极小值点, 极小值为 $y\left(\frac1e\right)=-\frac1e$.

$\blacksquare$
