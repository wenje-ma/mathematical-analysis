# week14

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

## 3.1-6

证明下列不等式:

(1) $\ln\left(1+x\right)<{}x$ ($x>0$);

(2) $\cos{x}>1-\frac{x^2}{2}$ ($x\ne0$);

(3) $\sin{x}<{}x$ ($x>0$);

(4) $\tan{x}>{}x$ ($0<{}x<\frac\pi2$).

### 解答 3.1-6

(1) 令 $f\left(x\right)=\ln\left(1+x\right)-x$. 则 $f\left(0\right)=0$, 且

$$
f'\left(x\right)=\frac1{1+x}-1=-\frac{x}{1+x}<0\quad\left(x>0\right).
$$

由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left[0,+\infty\right)$ 上严格递减. 故当 $x>0$ 时 $f\left(x\right)<{}f\left(0\right)=0$, 即 $\ln\left(1+x\right)<{}x$.

(2) 令 $f\left(x\right)=\cos{x}-1+\frac{x^2}{2}$. 则 $f\left(0\right)=0$, 且 $f'\left(x\right)=-\sin{x}+x$. 由 (3), 当 $x>0$ 时 $\sin{x}<{}x$, 故 $f'\left(x\right)=x-\sin{x}>0$. 由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left[0,+\infty\right)$ 上严格递增. 故当 $x>0$ 时 $f\left(x\right)>{}f\left(0\right)=0$, 即 $\cos{x}>1-\frac{x^2}{2}$. 当 $x<0$ 时由偶函数性质得同样结论.

(3) 令 $f\left(x\right)=x-\sin{x}$. 则 $f\left(0\right)=0$, 且 $f'\left(x\right)=1-\cos{x}\ge0$, 且 $f'\left(x\right)=0$ 仅在孤立点 $x=2k\pi$ 处成立. 由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left[0,+\infty\right)$ 上严格递增. 故当 $x>0$ 时 $f\left(x\right)>{}f\left(0\right)=0$, 即 $\sin{x}<{}x$.

(4) 令 $f\left(x\right)=\tan{x}-x$. 则 $f\left(0\right)=0$, 且

$$
f'\left(x\right)=\sec^2x-1=\tan^2x>0\quad\left(0<{}x<\frac\pi2\right).
$$

由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left[0,\frac\pi2\right)$ 上严格递增. 故当 $0<{}x<\frac\pi2$ 时 $f\left(x\right)>{}f\left(0\right)=0$, 即 $\tan{x}>{}x$. $\blacksquare$

## 3.1-8

设 $f\left(x\right)$ 在 $x_0$ 点的一个邻域 $U$ 内连续, 并在 $x_0$ 点的空心邻域 $U\setminus\left\{x_0\right\}$ 中可导. 试证明: 若极限 $\lim_{x\to{x}_0}f'\left(x\right)$ 存在, 则 $f\left(x\right)$ 在 $x_0$ 点可导, 且 $f'\left(x_0\right)=\lim_{x\to{x}_0}f'\left(x\right)$.

### 解答 3.1-8

设 $\lim_{x\to{x}_0}f'\left(x\right)=A$. 对任意 $x\in{U}\setminus\left\{x_0\right\}$, 在以 $x_0$ 与 $x$ 为端点的闭区间上应用**定理 1.3 (拉格朗日中值定理)**, 存在介于 $x_0$ 与 $x$ 之间的点 $\xi$, 使得

$$
f\left(x\right)-f\left(x_0\right)=f'\left(\xi\right)\left(x-x_0\right).
$$

于是

$$
\frac{f\left(x\right)-f\left(x_0\right)}{x-x_0}=f'\left(\xi\right).
$$

当 $x\to{x}_0$ 时, $\xi\to{x}_0$. 由题设 $\lim_{x\to{x}_0}f'\left(x\right)=A$, 故

$$
\lim_{x\to{x}_0}\frac{f\left(x\right)-f\left(x_0\right)}{x-x_0}=\lim_{\xi\to{x}_0}f'\left(\xi\right)=A.
$$

由导数的定义, $f$ 在 $x_0$ 点可导, 且 $f'\left(x_0\right)=A=\lim_{x\to{x}_0}f'\left(x\right)$. $\blacksquare$

## 3.1-10

证明达布定理: 设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中可导. 若存在 $x_1,x_2\in\left(a,b\right)$, 使得 $f'\left(x_1\right)>0$, $f'\left(x_2\right)<0$, 则 $x_1$ 与 $x_2$ 之间有一点 $c$, 使得 $f'\left(c\right)=0$.

### 解答 3.1-10

不妨设 $x_1<{}x_2$. 由 $f'\left(x_1\right)>0$, 根据导数定义, 存在 $\delta_1>0$, 使得当 $x\in\left(x_1,x_1+\delta_1\right)$ 时

$$
\frac{f\left(x\right)-f\left(x_1\right)}{x-x_1}>0,
$$

即 $f\left(x\right)>{}f\left(x_1\right)$. 同理, 由 $f'\left(x_2\right)<0$, 存在 $\delta_2>0$, 使得当 $x\in\left(x_2-\delta_2,x_2\right)$ 时

$$
\frac{f\left(x\right)-f\left(x_2\right)}{x-x_2}<0.
$$

因 $x-x_2<0$, 故 $f\left(x\right)-f\left(x_2\right)>0$, 即 $f\left(x\right)>{}f\left(x_2\right)$.

考虑 $f$ 在闭区间 $\left[x_1,x_2\right]$ 上的最大值. 由上述讨论, $f$ 在 $x_1$ 右侧附近的点处函数值大于 $f\left(x_1\right)$, 故最大值不在 $x_1$ 处达到; 同理, 最大值不在 $x_2$ 处达到. 因此最大值在某点 $c\in\left(x_1,x_2\right)$ 处达到, 即 $c$ 为极大值点. 又 $f$ 在 $\left(a,b\right)$ 内可导, 由**定理 1.1 (费马定理)**, $f'\left(c\right)=0$. $\blacksquare$

## 3.1-11

证明: 若 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 区间中可导, 且 $f'\left(x\right)\ne0$, 则 $f$ 在 $\left(a,b\right)$ 中要么严格递增, 要么严格递减.

### 解答 3.1-11

用反证法. 假定 $f$ 在 $\left(a,b\right)$ 中既不严格递增也不严格递减. 则由**定理 1.3 (拉格朗日中值定理)**, 存在两点使得 $f$ 的增量为正, 又存在两点使得 $f$ 的增量为负, 故 $f'$ 在某处取正值, 在某处取负值. 由 3.1-10 的达布定理, $f'$ 必取零值, 与 $f'\left(x\right)\ne0$ 矛盾. 故 $f$ 只能严格递增或严格递减. $\blacksquare$

## 3.1-13

证明不等式 $e^x>1+x$ ($x>0$).

### 解答 3.1-13

令 $f\left(x\right)=e^x-1-x$. 则 $f\left(0\right)=0$, 且

$$
f'\left(x\right)=e^x-1>0\quad\left(x>0\right).
$$

由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left[0,+\infty\right)$ 上严格递增. 故当 $x>0$ 时 $f\left(x\right)>{}f\left(0\right)=0$, 即 $e^x>1+x$. $\blacksquare$
