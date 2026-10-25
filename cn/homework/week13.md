# 作业 13

> **定理 1.1**（费马定理）设 $f\left(x\right)$ 在一点 $a$ 附近有定义, 且在 $a$ 点可微. 若 $a$ 点为 $y=f\left(x\right)$ 的极值点, 则 $f'\left(a\right)=0$.

> **定理 1.2**（罗尔定理）设函数 $y=f\left(x\right)$ 在闭区间 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 中处处可导, 且 $f\left(a\right)=f\left(b\right)$. 则在 $\left(a,b\right)$ 中至少存在一点 $c$, 使得 $f'\left(c\right)=0$.

> **定理 1.3**（拉格朗日中值定理）设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 内可导. 则存在点 $c\in\left(a,b\right)$, 使得
> $$
> f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}.
> $$
> **定理 1.4**（常数定理）设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中处处可导, 且 $f'\left(x\right)=0$($x\in\left(a,b\right)$). 则 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 内必为常数.

> **定理 1.5**（单调性判定）设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 可导. 若 $f'\left(x\right)> 0$($\ge 0$)$\forall x\in\left(a,b\right)$, 则 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上严格递增(递增); 若 $f'\left(x\right)< 0$($\le 0$)$\forall x\in\left(a,b\right)$, 则 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上严格递减(递减).

### 习题一

（习题 3.1-1）设 $y=f\left(x\right)$ 在 $\left(-\infty,+\infty\right)$ 内可导, 且 $\lim\limits_{x\to-\infty}f\left(x\right)=\lim\limits_{x\to+\infty}f\left(x\right)$. 证明: 存在一点 $c\in\left(-\infty,+\infty\right)$ 使得 $f'\left(c\right)=0$.

### 解答 习题一

记

$$
l=\lim_{x\to-\infty}f\left(x\right)=\lim_{x\to+\infty}f\left(x\right).
$$

分两种情况讨论.

若 $f\left(x\right)\equiv l$, 则 $f'\left(x\right)\equiv0$, 结论显然成立.

若 $f$ 不恒等于 $l$, 则存在 $x_0$ 使得 $f\left(x_0\right)\ne l$. 不妨设 $f\left(x_0\right)> l$($f\left(x_0\right)< l$ 的情形类似). 由 $\lim_{x\to\pm\infty}f\left(x\right)=l$, 取 $\varepsilon=\frac{f\left(x_0\right)-l}{2}> 0$, 则存在 $A> \left|x_0\right|$, 使得当 $\left|x\right|> A$ 时 $\left|f\left(x\right)-l\right|< \varepsilon$, 即
$$
f\left(x\right)< l+\varepsilon=\frac{f\left(x_0\right)+l}{2}< f\left(x_0\right).
$$
考虑闭区间 $\left[-A,A\right]$ 上的连续函数 $f$. 由于 $f\left(-A\right)< f\left(x_0\right)$ 且 $f\left(A\right)< f\left(x_0\right)$, 而 $x_0\in\left(-A,A\right)$, 故 $f$ 在 $\left[-A,A\right]$ 上的最大值不在端点 $-A$ 或 $A$ 处达到, 而在某点 $c\in\left(-A,A\right)$ 处达到. 于是 $c$ 为极大值点. 又 $f$ 在 $\left(-A,A\right)$ 内可导, 由**定理 1.1**（费马定理）, $f'\left(c\right)=0$. $\blacksquare$

### 习题二

（习题 3.1-2）设 $p\left(x\right)=x^n+qx+r$($n$ 为正整数, $q,r$ 为实数). 证明: $n$ 为偶数时至多有两个实根; $n$ 为奇数时至多有三个实根.

### 解答 习题二

反证法. 设 $n$ 为偶数, 假定 $p\left(x\right)$ 至少有三个不同的实根 $x_1< x_2< x_3$. 由**定理 1.2**（罗尔定理）, 在 $\left(x_1,x_2\right)$ 与 $\left(x_2,x_3\right)$ 内分别存在点 $\xi_1,\xi_2$, 使得
$$
p'\left(\xi_1\right)=0, p'\left(\xi_2\right)=0.
$$
而 $p'\left(x\right)=nx^{n-1}+q$. 因 $n$ 为偶数, $n-1$ 为奇数, 方程 $nx^{n-1}+q=0$ 至多有一个实根(奇次幂 $x^{n-1}$ 严格单调递增). 这与 $p'\left(\xi_1\right)=p'\left(\xi_2\right)=0$ 且 $\xi_1\ne\xi_2$ 矛盾. 故 $n$ 为偶数时 $p\left(x\right)$ 至多有两个实根.

设 $n$ 为奇数, 假定 $p\left(x\right)$ 至少有四个不同的实根 $x_1< x_2< x_3< x_4$. 由**定理 1.2**（罗尔定理）, 在 $\left(x_1,x_2\right),\left(x_2,x_3\right),\left(x_3,x_4\right)$ 内分别存在 $\xi_1,\xi_2,\xi_3$, 使得

$$
p'\left(\xi_1\right)=p'\left(\xi_2\right)=p'\left(\xi_3\right)=0.
$$

再对 $p'\left(x\right)$ 使用**定理 1.2**（罗尔定理）, 在 $\left(\xi_1,\xi_2\right)$ 与 $\left(\xi_2,\xi_3\right)$ 内分别存在 $\eta_1,\eta_2$, 使得
$$
p''\left(\eta_1\right)=0, p''\left(\eta_2\right)=0.
$$
而 $p''\left(x\right)=n\left(n-1\right)x^{n-2}$. 因 $n$ 为奇数, $n-2$ 亦为奇数, 方程 $n\left(n-1\right)x^{n-2}=0$ 只有一个实根 $x=0$. 这与 $p''\left(\eta_1\right)=p''\left(\eta_2\right)=0$ 且 $\eta_1\ne\eta_2$ 矛盾. 故 $n$ 为奇数时 $p\left(x\right)$ 至多有三个实根. $\blacksquare$

### 习题三

（习题 3.1-4）确定下列函数的单调区间: 
(1) $f\left(x\right)=xe^x$; 

(2) $f\left(x\right)=\frac{x^2-1}{x}$; 

(3) $f\left(x\right)=\sqrt{x-2}$; 

(4) $f\left(x\right)=x^4-x+1$.

### 解答 习题三

(1)

$$
f'\left(x\right)=e^x+xe^x=\left(1+x\right)e^x.
$$

因 $e^x> 0$ 恒成立, 故 $f'\left(x\right)$ 的符号由 $1+x$ 决定. 当 $x< -1$ 时 $f'\left(x\right)< 0$, 当 $x> -1$ 时 $f'\left(x\right)> 0$. 由**定理 1.5**（单调性判定）, $f\left(x\right)$ 在 $\left(-\infty,-1\right]$ 上严格递减, 在 $\left[-1,+\infty\right)$ 上严格递增.

(2)$f\left(x\right)=x-\frac1x$, 定义域为 $\left(-\infty,0\right)\cup\left(0,+\infty\right)$. $f'\left(x\right)=1+\frac1{x^2}> 0$ 恒成立. 由**定理 1.5**（单调性判定）, $f\left(x\right)$ 在 $\left(-\infty,0\right)$ 上严格递增, 在 $\left(0,+\infty\right)$ 上严格递增.

(3)定义域为 $\left[2,+\infty\right)$. $f'\left(x\right)=\frac{1}{2\sqrt{x-2}}> 0$($x> 2$). 由**定理 1.5**（单调性判定）, $f\left(x\right)$ 在 $\left[2,+\infty\right)$ 上严格递增.

(4)$f'\left(x\right)=4x^3-1$. 令 $f'\left(x\right)=0$, 得

$$
x=\sqrt\left[3\right]{\frac14}.
$$
当

$$
x< \sqrt\left[3\right]{\frac14}
$$
时 $f'\left(x\right)< 0$, 当

$$
x> \sqrt\left[3\right]{\frac14}
$$
时 $f'\left(x\right)> 0$. 由**定理 1.5**（单调性判定）, $f\left(x\right)$ 在

$$
\left(-\infty,\sqrt\left[3\right]{\frac14}\right]
$$
上严格递减, 在

$$
\left[\sqrt\left[3\right]{\frac14},+\infty\right)
$$

上严格递增. $\blacksquare$

### 习题四

（习题 3.1-5）设 $f\left(x\right)$ 与 $g\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 中可导, 且有 $f'\left(x\right)> g'\left(x\right)$. 假定 $f\left(a\right)=g\left(a\right)$, 证明 $f\left(x\right)> g\left(x\right)$, $x\in\left(a,b\right]$.

### 解答 习题四

令 $h\left(x\right)=f\left(x\right)-g\left(x\right)$. 由题设, $h\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 中可导, 且
$$
h'\left(x\right)=f'\left(x\right)-g'\left(x\right)> 0\left(\forall x\in\left(a,b\right)\right).
$$
由**定理 1.5**（单调性判定）, $h\left(x\right)$ 在 $\left[a,b\right]$ 上严格递增. 又 $h\left(a\right)=f\left(a\right)-g\left(a\right)=0$, 故对任意 $x\in\left(a,b\right]$, 有
$$
h\left(x\right)> h\left(a\right)=0,
$$
即 $f\left(x\right)-g\left(x\right)> 0$, 亦即 $f\left(x\right)> g\left(x\right)$. $\blacksquare$

### 习题五

（习题 3.1-6）证明下列不等式: 
(1) $\ln\left(1+x\right)< x$($x> 0$); 

(2) $\cos x> 1-\frac{x^2}{2}$($x\ne0$); 

(3) $\sin x< x$($x> 0$); 

(4) $\tan x> x$($0< x< \frac{\pi}{2}$).

### 解答 习题五

(1)令 $f\left(x\right)=\ln\left(1+x\right)-x$. 则 $f\left(0\right)=0$, 且
$$
f'\left(x\right)=\frac{1}{1+x}-1=-\frac{x}{1+x}< 0\left(x> 0\right).
$$
由**定理 1.5**（单调性判定）, $f\left(x\right)$ 在 $\left[0,+\infty\right)$ 上严格递减. 故当 $x> 0$ 时 $f\left(x\right)< f\left(0\right)=0$, 即 $\ln\left(1+x\right)-x< 0$, 亦即 $\ln\left(1+x\right)< x$.

(2)令 $f\left(x\right)=\cos x-1+\frac{x^2}{2}$. 则 $f\left(0\right)=0$, 且
$$
f'\left(x\right)=-\sin x+x.
$$
由(3)(见下文), 当 $x> 0$ 时 $\sin x< x$, 故 $f'\left(x\right)=x-\sin x> 0$. 由**定理 1.5**（单调性判定）, $f\left(x\right)$ 在 $\left[0,+\infty\right)$ 上严格递增. 故当 $x> 0$ 时 $f\left(x\right)> f\left(0\right)=0$, 即 $\cos x> 1-\frac{x^2}{2}$. 当 $x< 0$ 时, 令 $t=-x> 0$, 由偶函数性质得同样结论.

(3)令 $f\left(x\right)=x-\sin x$. 则 $f\left(0\right)=0$, 且
$$
f'\left(x\right)=1-\cos x\ge0.
$$
且 $f'\left(x\right)=0$ 仅在孤立点 $x=2k\pi$ 处成立. 由**定理 1.5**（单调性判定）, $f\left(x\right)$ 在 $\left[0,+\infty\right)$ 上严格递增. 故当 $x> 0$ 时 $f\left(x\right)> f\left(0\right)=0$, 即 $x-\sin x> 0$, 亦即 $\sin x< x$.

(4)令 $f\left(x\right)=\tan x-x$. 则 $f\left(0\right)=0$, 且
$$
f'\left(x\right)=\sec^2 x-1=\tan^2 x> 0\left(0< x< \frac{\pi}{2}\right).
$$
由**定理 1.5**（单调性判定）, $f\left(x\right)$ 在 $\left[0,\frac{\pi}{2}\right)$ 上严格递增. 故当 $0< x< \frac{\pi}{2}$ 时 $f\left(x\right)> f\left(0\right)=0$, 即 $\tan x-x> 0$, 亦即 $\tan x> x$. $\blacksquare$

### 习题六

（习题 3.1-8）设 $f\left(x\right)$ 在 $x_0$ 点的一个邻域 $U$ 内连续, 并在 $x_0$ 点的空心邻域 $U\setminus\left\{x_0\right\}$ 中可导. 试证明: 若极限 $\lim\limits_{x\to x_0}f'\left(x\right)$ 存在, 则 $f\left(x\right)$ 在 $x_0$ 点可导, 且
$$
f'\left(x_0\right)=\lim_{x\to x_0}f'\left(x\right).
$$
### 解答 习题六

设 $\lim_{x\to x_0}f'\left(x\right)=A$. 对任意 $x\in U\setminus\left\{x_0\right\}$, 在以 $x_0$ 与 $x$ 为端点的闭区间上应用**定理 1.3**（拉格朗日中值定理）, 存在介于 $x_0$ 与 $x$ 之间的点 $\xi$, 使得
$$
f\left(x\right)-f\left(x_0\right)=f'\left(\xi\right)\left(x-x_0\right).
$$
于是
$$
\frac{f\left(x\right)-f\left(x_0\right)}{x-x_0}=f'\left(\xi\right).
$$
当 $x\to x_0$ 时, $\xi\to x_0$. 由题设 $\lim_{x\to x_0}f'\left(x\right)=A$, 故
$$
\lim_{x\to x_0}\frac{f\left(x\right)-f\left(x_0\right)}{x-x_0}=\lim_{\xi\to x_0}f'\left(\xi\right)=A.
$$
由导数的定义, $f$ 在 $x_0$ 点可导, 且

$$
f'\left(x_0\right)=A=\lim_{x\to x_0}f'\left(x\right).
$$

$\blacksquare$

### 习题七

（习题 3.1-10）证明达布定理: 设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中可导. 若存在 $x_1,x_2\in\left(a,b\right)$, 使得 $f'\left(x_1\right)> 0$, $f'\left(x_2\right)< 0$, 则 $x_1$ 与 $x_2$ 之间有一点 $c$, 使得 $f'\left(c\right)=0$.

### 解答 习题七

不妨设 $x_1< x_2$. 由 $f'\left(x_1\right)> 0$, 根据导数定义, 存在 $\delta_1> 0$, 使得当 $x\in\left(x_1,x_1+\delta_1\right)$ 时
$$
\frac{f\left(x\right)-f\left(x_1\right)}{x-x_1}> 0,
$$
即 $f\left(x\right)> f\left(x_1\right)$. 同理, 由 $f'\left(x_2\right)< 0$, 存在 $\delta_2> 0$, 使得当 $x\in\left(x_2-\delta_2,x_2\right)$ 时
$$
\frac{f\left(x\right)-f\left(x_2\right)}{x-x_2}< 0.
$$
因 $x-x_2< 0$, 故 $f\left(x\right)-f\left(x_2\right)> 0$, 即 $f\left(x\right)> f\left(x_2\right)$.

考虑 $f$ 在闭区间 $\left[x_1,x_2\right]$ 上的最大值. 由上述讨论, $f$ 在 $x_1$ 右侧附近的点处函数值大于 $f\left(x_1\right)$, 故最大值不在 $x_1$ 处达到; 同理, $f$ 在 $x_2$ 左侧附近的点处函数值大于 $f\left(x_2\right)$, 故最大值不在 $x_2$ 处达到. 因此最大值在某点 $c\in\left(x_1,x_2\right)$ 处达到, 即 $c$ 为极大值点. 又 $f$ 在 $\left(a,b\right)$ 内可导, 由**定理 1.1**（费马定理）, $f'\left(c\right)=0$. $\blacksquare$

### 习题八

（习题 3.1-11）证明: 若 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 区间中可导, 且 $f'\left(x\right)\ne0$, 则 $f$ 在 $\left(a,b\right)$ 中要么严格递增, 要么严格递减.

### 解答 习题八

用反证法. 假定 $f$ 在 $\left(a,b\right)$ 中既不严格递增也不严格递减. 则存在 $x_1< x_2< x_3$ 使得 $f\left(x_2\right)\le f\left(x_1\right)$ 且 $f\left(x_2\right)\le f\left(x_3\right)$(或类似的反向情形).

考虑 $f$ 在 $\left[x_1,x_3\right]$ 上的最小值. 若最小值在 $x_2$ 处达到, 则 $x_2$ 为极小值点, 由**定理 1.1**（费马定理）得 $f'\left(x_2\right)=0$, 与题设矛盾.

若最小值不在 $x_2$ 处达到, 则在 $\left(x_1,x_2\right)$ 与 $\left(x_2,x_3\right)$ 中必有一个区间的端点处取得最小值. 不妨设在 $\left(x_2,x_3\right]$ 内某点达到最小值. 又由假定 $f\left(x_2\right)\le f\left(x_1\right)$, 可知 $f$ 在 $\left[x_1,x_2\right]$ 上的最大值与最小值的关系导致 $f'$ 在某处变号. 由习题七(达布定理), $f'$ 必取零值, 矛盾.

更严格地说: 由**定理 1.3**（拉格朗日中值定理）, 若存在两点使得 $f$ 的增量为正, 又存在两点使得 $f$ 的增量为负, 则 $f'$ 在某处取正值, 在某处取负值. 由达布定理(习题七), $f'$ 必取零值, 与 $f'\left(x\right)\ne0$ 矛盾.

故 $f$ 只能严格递增或严格递减. $\blacksquare$

### 习题九

（习题 3.1-13）证明不等式 $e^x> 1+x$($x> 0$).

### 解答 习题九

令 $f\left(x\right)=e^x-1-x$. 则 $f\left(0\right)=0$, 且
$$
f'\left(x\right)=e^x-1> 0\left(x> 0\right).
$$
由**定理 1.5**（单调性判定）, $f\left(x\right)$ 在 $\left[0,+\infty\right)$ 上严格递增. 故当 $x> 0$ 时 $f\left(x\right)> f\left(0\right)=0$, 即 $e^x-1-x> 0$, 亦即 $e^x> 1+x$. $\blacksquare$

### 习题十

（习题 3.1-14）设

$$
f\left(x\right)=\arctan\frac{1+x}{1-x}-\arctan x,
$$

又设 $\left(a,b\right)$ 是不包含 $x=1$ 的任意一个区间. 证明 $f\left(x\right)=C$, $\forall x\in\left(a,b\right)$, $C$ 为常数. 令 $\left(a,b\right)=\left(-\infty,1\right)$, 试证这时 $C=\frac{\pi}{4}$. 又问: 当 $x\in\left(1,+\infty\right)$ 时, $C$ 为何值?

### 解答 习题十

求导得
$$
\begin{aligned}
f'\left(x\right)&=\frac{1}{1+\left(\frac{1+x}{1-x}\right)^2}\cdot\frac{\left(1-x\right)+\left(1+x\right)}{\left(1-x\right)^2}-\frac{1}{1+x^2}\\
&=\frac{\left(1-x\right)^2}{\left(1-x\right)^2+\left(1+x\right)^2}\cdot\frac{2}{\left(1-x\right)^2}-\frac{1}{1+x^2}\\
&=\frac{2}{\left(1-x\right)^2+\left(1+x\right)^2}-\frac{1}{1+x^2}\\
&=\frac{1}{1+x^2}-\frac{1}{1+x^2}=0.
\end{aligned}
$$

由**定理 1.4**（常数定理）, $f\left(x\right)$ 在 $\left(a,b\right)$ 内为常数, 记为 $C$.

当 $\left(a,b\right)=\left(-\infty,1\right)$ 时, 取 $x=0$, 则
$$
f\left(0\right)=\arctan 1-\arctan 0=\frac{\pi}{4}.
$$
故 $C=\frac{\pi}{4}$, 即
$$
\arctan\frac{1+x}{1-x}=\arctan x+\frac{\pi}{4}\left(x< 1\right).
$$
当 $x\in\left(1,+\infty\right)$ 时, 取 $x\to+\infty$, 则 $\frac{1+x}{1-x}\to-1$, $\arctan\frac{1+x}{1-x}\to-\frac{\pi}{4}$, 而 $\arctan x\to\frac{\pi}{2}$. 故

$$
C=\lim_{x\to+\infty}f\left(x\right)=-\frac{\pi}{4}-\frac{\pi}{2}=-\frac{3\pi}{4}.
$$

$\blacksquare$
