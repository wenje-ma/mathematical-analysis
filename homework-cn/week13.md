# week13

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

若 $f\left(x\right)\equiv{l}$, 则 $f'\left(x\right)\equiv0$, 结论显然成立.

若 $f$ 不恒等于 $l$, 则存在 $x_0$ 使得 $f\left(x_0\right)\ne{l}$. 不妨设 $f\left(x_0\right)>{}l$. 由 $\lim_{x\to\pm\infty}f\left(x\right)=l$, 取 $\varepsilon=\frac{f\left(x_0\right)-l}{2}>0$, 则存在 $A>\left|x_0\right|$, 使得当 $\left|x\right|>{}A$ 时 $\left|f\left(x\right)-l\right|<\varepsilon$, 即

$$
f\left(x\right)<{}l+\varepsilon=\frac{f\left(x_0\right)+l}{2}<{}f\left(x_0\right).
$$

考虑闭区间 $\left[-A,A\right]$ 上的连续函数 $f$. 由于 $f\left(-A\right)<{}f\left(x_0\right)$ 且 $f\left(A\right)<{}f\left(x_0\right)$, 而 $x_0\in\left(-A,A\right)$, 故 $f$ 在 $\left[-A,A\right]$ 上的最大值不在端点处达到, 而在某点 $c\in\left(-A,A\right)$ 处达到. 于是 $c$ 为极大值点. 又 $f$ 在 $\left(-A,A\right)$ 内可导, 由**定理 1.1 (费马定理)**, $f'\left(c\right)=0$. $\blacksquare$

## 3.1-2

设 $p\left(x\right)=x^n+qx+r$ ($n$ 为正整数, $q,r$ 为实数). 证明: $n$ 为偶数时至多有两个实根; $n$ 为奇数时至多有三个实根.

### 解答 3.1-2

反证法. 设 $n$ 为偶数, 假定 $p\left(x\right)$ 至少有三个不同的实根 $x_1<{}x_2<{}x_3$. 由**定理 1.2 (罗尔定理)**, 在 $\left(x_1,x_2\right)$ 与 $\left(x_2,x_3\right)$ 内分别存在点 $\xi_1,\xi_2$, 使得

$$
p'\left(\xi_1\right)=0,\quad{p}'\left(\xi_2\right)=0.
$$

而 $p'\left(x\right)=nx^{n-1}+q$. 因 $n$ 为偶数, $n-1$ 为奇数, 方程 $nx^{n-1}+q=0$ 至多有一个实根. 这与 $p'\left(\xi_1\right)=p'\left(\xi_2\right)=0$ 且 $\xi_1\ne\xi_2$ 矛盾. 故 $n$ 为偶数时 $p\left(x\right)$ 至多有两个实根.

设 $n$ 为奇数, 假定 $p\left(x\right)$ 至少有四个不同的实根 $x_1<{}x_2<{}x_3<{}x_4$. 由**定理 1.2 (罗尔定理)**, 在 $\left(x_1,x_2\right)$, $\left(x_2,x_3\right)$, $\left(x_3,x_4\right)$ 内分别存在 $\xi_1,\xi_2,\xi_3$, 使得

$$
p'\left(\xi_1\right)=p'\left(\xi_2\right)=p'\left(\xi_3\right)=0.
$$

再对 $p'\left(x\right)$ 使用**定理 1.2 (罗尔定理)**, 在 $\left(\xi_1,\xi_2\right)$ 与 $\left(\xi_2,\xi_3\right)$ 内分别存在 $\eta_1,\eta_2$, 使得

$$
p''\left(\eta_1\right)=0,\quad{p}''\left(\eta_2\right)=0.
$$

而 $p''\left(x\right)=n\left(n-1\right)x^{n-2}$. 因 $n$ 为奇数, $n-2$ 亦为奇数, 方程 $n\left(n-1\right)x^{n-2}=0$ 只有一个实根 $x=0$. 这与 $p''\left(\eta_1\right)=p''\left(\eta_2\right)=0$ 且 $\eta_1\ne\eta_2$ 矛盾. 故 $n$ 为奇数时 $p\left(x\right)$ 至多有三个实根. $\blacksquare$

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

(4) $f'\left(x\right)=4x^3-1$. 令 $f'\left(x\right)=0$, 得 $x=\sqrt\left[3\right]{\frac14}$. 当 $x<\sqrt\left[3\right]{\frac14}$ 时 $f'\left(x\right)<0$, 当 $x>\sqrt\left[3\right]{\frac14}$ 时 $f'\left(x\right)>0$. 由**定理 1.5 (单调性判定)**, $f\left(x\right)$ 在 $\left(-\infty,\sqrt\left[3\right]{\frac14}\right]$ 上严格递减, 在 $\left[\sqrt\left[3\right]{\frac14},+\infty\right)$ 上严格递增. $\blacksquare$

## 3.1-5

设 $f\left(x\right)$ 与 $g\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 中可导, 且有 $f'\left(x\right)>{}g'\left(x\right)$. 假定 $f\left(a\right)=g\left(a\right)$, 证明 $f\left(x\right)>{}g\left(x\right)$ 对一切 $x\in\left(a,b\right]$ 成立.

### 解答 3.1-5

令 $h\left(x\right)=f\left(x\right)-g\left(x\right)$. 由题设, $h\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 中可导, 且

$$
h'\left(x\right)=f'\left(x\right)-g'\left(x\right)>0\quad\left(\forall{x}\in\left(a,b\right)\right).
$$

由**定理 1.5 (单调性判定)**, $h\left(x\right)$ 在 $\left[a,b\right]$ 上严格递增. 又 $h\left(a\right)=f\left(a\right)-g\left(a\right)=0$, 故对任意 $x\in\left(a,b\right]$, 有

$$
h\left(x\right)>{}h\left(a\right)=0,
$$

即 $f\left(x\right)-g\left(x\right)>0$, 亦即 $f\left(x\right)>{}g\left(x\right)$. $\blacksquare$
