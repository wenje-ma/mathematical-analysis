# week18

> **定理 1.3 (拉格朗日中值定理)**
> 
> 设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 内可导. 则存在 $c\in\left(a,b\right)$, 使得 $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

> **定理 4.1 (局部泰勒展开式)**
> 
> 设 $y=f\left(x\right)$ 在 $x_0$ 点附近有定义, 且有 $n$ 阶导数 $f^{\left(n\right)}\left(x_0\right)$. 则 $f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right)$ ($x\to{x}_0$).

> **定理 4.2 (带拉格朗日余项的泰勒公式)**
> 
> 设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上有 $n$ 阶连续导数, 在 $\left(a,b\right)$ 中有 $n+1$ 阶导数. 则对任意 $x,x_0\in\left[a,b\right]$, 存在介于 $x_0$ 与 $x$ 之间的点 $\xi$, 使得 $f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n+1\right)}\left(\xi\right)}{\left(n+1\right)!}\left(x-x_0\right)^{n+1}$.

> **定理 5.1 (凸函数的二阶导数判别)**
> 
> 设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 上二阶可导. 则 $f$ 为凸函数的充要条件是 $f''\left(x\right)\ge0$; $f$ 为凹函数的充要条件是 $f''\left(x\right)\le0$.

## 3.4-7

设 $y=f\left(x\right)$ 在 $a$ 点有 $n+1$ 阶导数. 证明: $f$ 在 $a$ 的 $n+1$ 阶泰勒多项式的导数等于 $f'$ 在 $a$ 点的 $n$ 阶泰勒多项式.

### 解答 3.4-7

$f$ 在 $a$ 点的 $n+1$ 阶泰勒多项式为

$$
T_{n+1}\left(x\right)=f\left(a\right)+f'\left(a\right)\left(x-a\right)+\cdots+\frac{f^{\left(n+1\right)}\left(a\right)}{\left(n+1\right)!}\left(x-a\right)^{n+1}.
$$

对 $x$ 求导:

$$
T_{n+1}'\left(x\right)=f'\left(a\right)+f''\left(a\right)\left(x-a\right)+\cdots+\frac{f^{\left(n+1\right)}\left(a\right)}{n!}\left(x-a\right)^n.
$$

而 $f'$ 在 $a$ 点的 $n$ 阶泰勒多项式为

$$
U_n\left(x\right)=f'\left(a\right)+f''\left(a\right)\left(x-a\right)+\cdots+\frac{f^{\left(n+1\right)}\left(a\right)}{n!}\left(x-a\right)^n.
$$

注意到 $\left(f'\right)^{\left(k\right)}\left(a\right)=f^{\left(k+1\right)}\left(a\right)$, 比较两式即得 $T_{n+1}'\left(x\right)=U_n\left(x\right)$. $\blacksquare$

## 3.4-10

证明: 当 $x\to0$ 时, $\arctan{x}=x-\frac{x^3}3+\frac{x^5}5-\cdots+\left(-1\right)^m\frac{x^{2m+1}}{2m+1}+o\left(x^{2m+1}\right)$.

### 解答 3.4-10

对 $f\left(x\right)=\arctan{x}$, 有 $f'\left(x\right)=\frac1{1+x^2}$. 由 3.4-1-2 的结果, 将 $-x^2$ 代入 $\frac1{1-t}$ 的展开式:

$$
\frac1{1+x^2}=1-x^2+x^4-\cdots+\left(-1\right)^mx^{2m}+o\left(x^{2m}\right).
$$

由 3.4-7 的结果, $f\left(x\right)$ 的 $2m+1$ 阶泰勒多项式为上述多项式逐项积分:

$$
\arctan{x}=x-\frac{x^3}3+\frac{x^5}5-\cdots+\left(-1\right)^m\frac{x^{2m+1}}{2m+1}+o\left(x^{2m+1}\right).
$$

$\blacksquare$

## 3.4-11

设 $f\left(x\right)=x^{1/5}$, $x=32$, $\Delta{x}=0.16$. 已知 $f\left(32\right)+f'\left(32\right)\Delta{x}=2.002$. 证明: $2.002$ 作为 $32.16^{1/5}$ 的近似值, 其误差的绝对值小于 $10^{-6}$.

### 解答 3.4-11

误差为拉格朗日余项:

$$
R_1=\frac{f''\left(\xi\right)}2\left(0.16\right)^2,\quad\xi\in\left(32,32.16\right).
$$

$f''\left(x\right)=-\frac4{25}x^{-9/5}$. 故

$$
\left|R_1\right|=\frac2{25}\xi^{-9/5}\cdot\left(0.16\right)^2.
$$

因 $\xi>32$, $\xi^{-9/5}<32^{-9/5}=2^{-9}=\frac1{512}$. 于是

$$
\left|R_1\right|<\frac2{25}\cdot\frac1{512}\cdot0.0256=4\times10^{-6}.
$$

$\blacksquare$

## 3.4-12

设 $y=f\left(x\right)$ 在 $x_0$ 点有 $n$ 阶导数, $n>1$, 且 $f'\left(x_0\right)=\cdots=f^{\left(n-1\right)}\left(x_0\right)=0$, $f^{\left(n\right)}\left(x_0\right)\ne0$. 当 $n$ 为奇数时, $x_0$ 一定不是极值点; 当 $n$ 是偶数时, 若 $f^{\left(n\right)}\left(x_0\right)>0$, 则 $x_0$ 为极小值点; 若 $f^{\left(n\right)}\left(x_0\right)<0$, 则 $x_0$ 为极大值点.

### 解答 3.4-12

由**定理 4.1 (局部泰勒展开式)**, 在 $x_0$ 附近,

$$
f\left(x\right)-f\left(x_0\right)=\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right).
$$

当 $n$ 为奇数时, $\left(x-x_0\right)^n$ 在 $x_0$ 两侧变号, 而 $\frac{f^{\left(n\right)}\left(x_0\right)}{n!}$ 为固定非零常数, 故 $f\left(x\right)-f\left(x_0\right)$ 在 $x_0$ 两侧变号. 因此 $x_0$ 不是极值点.

当 $n$ 为偶数时, $\left(x-x_0\right)^n>0$ ($x\ne{x}_0$). 若 $f^{\left(n\right)}\left(x_0\right)>0$, 则 $f\left(x\right)-f\left(x_0\right)>0$, 故 $x_0$ 为极小值点. 若 $f^{\left(n\right)}\left(x_0\right)<0$, 则 $f\left(x\right)-f\left(x_0\right)<0$, 故 $x_0$ 为极大值点. $\blacksquare$

## 3.5-1-1

求出函数 $y=xe^x$ 的凸凹性区间及拐点.

### 解答 3.5-1-1

求导得 $y'=\left(1+x\right)e^x$, $y''=\left(2+x\right)e^x$. 令 $y''=0$, 得 $x=-2$. 当 $x<-2$ 时 $y''<0$ (凹); 当 $x>-2$ 时 $y''>0$ (凸). 拐点为 $\left(-2,-2e^{-2}\right)$. 由**定理 5.1 (凸函数的二阶导数判别)**, $y=xe^x$ 在 $\left(-\infty,-2\right]$ 上为凹函数, 在 $\left[-2,+\infty\right)$ 上为凸函数. $\blacksquare$

## 3.5-1-4

求出函数 $y=x\ln{x}$ 的凸凹性区间及拐点.

### 解答 3.5-1-4

定义域为 $\left(0,+\infty\right)$. $y'=\ln{x}+1$, $y''=\frac1x>0$. 由**定理 5.1 (凸函数的二阶导数判别)**, $y=x\ln{x}$ 在 $\left(0,+\infty\right)$ 上为凸函数, 无拐点. $\blacksquare$

## 3.5-2

利用凸函数概念证明下列不等式:

(1) 设 $a>0$, $b>0$, 证明 $2\arctan\frac{a+b}2\ge\arctan{a}+\arctan{b}$;

(2) 若 $a,b,c$ 均为正数, 证明 $a^\alpha{b}^\beta{c}^\gamma\le\alpha{a}+\beta{b}+\gamma{c}$, 其中 $\alpha+\beta+\gamma=1$, $\alpha,\beta,\gamma>0$.

### 解答 3.5-2

(1) 令 $f\left(x\right)=\arctan{x}$. 则 $f''\left(x\right)=\frac{-2x}{\left(1+x^2\right)^2}$. 当 $x>0$ 时 $f''\left(x\right)<0$, 故 $f$ 在 $\left(0,+\infty\right)$ 上为凹函数. 由凸函数与凹函数的定义, 取 $t=\frac12$, 得

$$
f\left(\frac{a+b}2\right)\ge\frac{f\left(a\right)+f\left(b\right)}2,
$$

即 $2\arctan\frac{a+b}2\ge\arctan{a}+\arctan{b}$.

(2) 由 $f\left(x\right)=\ln{x}$ 为凹函数 ($f''\left(x\right)=-\frac1{x^2}<0$), 由凸函数与凹函数的定义,

$$
\alpha\ln{a}+\beta\ln{b}+\gamma\ln{c}\le\ln\left(\alpha{a}+\beta{b}+\gamma{c}\right).
$$

即 $a^\alpha{b}^\beta{c}^\gamma\le\alpha{a}+\beta{b}+\gamma{c}$. 此即加权 AM-GM 不等式. $\blacksquare$
