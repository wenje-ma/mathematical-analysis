# week8

> **命题 3.1 (唯一极值点即全局极值点)**
> 
> 设 $y=f\left(x\right)$ 在区间 $\left(a,b\right)$ (或 $\left[a,b\right]$) 上连续. 若 $x_0$ 是 $\left(a,b\right)$ 中唯一的极值点, 则当 $x_0$ 为极大值点时, $f\left(x_0\right)$ 为最大值; 当 $x_0$ 为极小值点时, $f\left(x_0\right)$ 为最小值.

> **定理 3.1 (极值点第一充分条件)**
> 
> 设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中可导, 且 $x_0\in\left(a,b\right)$ 是 $f$ 的一个稳定点, 即 $f'\left(x_0\right)=0$. 若存在 $r>0$, 使得当 $x\in\left(x_0-r,x_0\right)$ 时 $f'\left(x\right)>0$, 当 $x\in\left(x_0,x_0+r\right)$ 时 $f'\left(x\right)<0$, 则 $f\left(x_0\right)$ 是极大值; 若符号相反, 则 $f\left(x_0\right)$ 是极小值.

> **定理 3.2 (极值点第二充分条件)**
> 
> 设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中可导, $x_0\in\left(a,b\right)$ 是其稳定点, 并假定 $f$ 在 $x_0$ 有二阶导数. 若 $f''\left(x_0\right)>0$, 则 $x_0$ 为极小值点; 若 $f''\left(x_0\right)<0$, 则 $x_0$ 为极大值点.

> **定理 4.1 (局部泰勒展开式)**
> 
> 设 $y=f\left(x\right)$ 在 $x_0$ 点附近有定义, 且有 $n$ 阶导数 $f^{\left(n\right)}\left(x_0\right)$. 则 $f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right)$ ($x\to{x}_0$).

> **定理 4.2 (带拉格朗日余项的泰勒公式)**
> 
> 设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上有 $n$ 阶连续导数, 在 $\left(a,b\right)$ 中有 $n+1$ 阶导数. 则对任意 $x,x_0\in\left[a,b\right]$, 存在介于 $x_0$ 与 $x$ 之间的点 $\xi$, 使得 $f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n+1\right)}\left(\xi\right)}{\left(n+1\right)!}\left(x-x_0\right)^{n+1}$.

## 3.3-2

设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续. 假定 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 内有唯一极值点. 证明: (1) 函数在该极值点附近一定是严格极大或严格极小; (2) 若该极值点为极大值点, 则一定是最大值点; 若为极小值点, 则一定是最小值点.

### 解答 3.3-2

(1) 设 $x_0\in\left(a,b\right)$ 为唯一极值点. 若 $x_0$ 不是严格极大值点, 则存在一列点 $x_n\to{x}_0$ ($x_n\ne{x}_0$) 使得 $f\left(x_n\right)\ge{f}\left(x_0\right)$. 但若在 $x_0$ 的任意邻域内都有函数值等于 $f\left(x_0\right)$ 的点, 则 $f$ 在 $x_0$ 附近为常数, 从而有无穷多个极值点, 与唯一性矛盾. 故 $x_0$ 必为严格极大值点 (或严格极小值点).

(2) 设 $x_0$ 为极大值点. 反证: 假定 $f\left(x_0\right)$ 不是 $\left[a,b\right]$ 上的最大值, 则存在 $x_1\in\left[a,b\right]$ 使得 $f\left(x_1\right)>f\left(x_0\right)$. 考虑闭区间 $\left[x_0,x_1\right]$ 上的连续函数 $f$. 因 $f\left(x_1\right)>f\left(x_0\right)$ 且 $x_0$ 为严格极大值点, 故 $f$ 在 $\left(x_0,x_1\right)$ 内某点达到最小值, 该点即为极小值点. 这与 $x_0$ 是唯一极值点矛盾.

故 $f\left(x_0\right)$ 必为最大值. 极小值点的情形类似. 此即**命题 3.1 (唯一极值点即全局极值点)**.

$\blacksquare$

## 3.3-3

(光的折射定律) 设有甲, 乙两种介质, 其交界面为一平面. 假设光自甲种介质中之 $A$ 点发出, 经过两种介质的交界面到达乙种介质中的 $B$ 点处. 从物理学上我们知道, 光所走的路径一定满足折射定律: $\frac{\sin\alpha}{\sin\beta}=\frac{v_1}{v_2}$, 其中 $\alpha$ 是光的入射角, $\beta$ 是折射角, $v_1,v_2$ 分别为光在甲, 乙两种介质中的速度. 证明光所走的路径是时间最少的路径.

### 解答 3.3-3

设交界面为 $x$ 轴, $A=\left(0,a\right)$ (甲介质, $y>0$), $B=\left(d,-b\right)$ (乙介质, $y<0$). 设光在交界面上的入射点为 $P=\left(x,0\right)$.

总时间为

$$
T\left(x\right)=\frac{\sqrt{x^2+a^2}}{v_1}+\frac{\sqrt{\left(d-x\right)^2+b^2}}{v_2}.
$$

求导得

$$
T'\left(x\right)=\frac{x}{v_1\sqrt{x^2+a^2}}-\frac{d-x}{v_2\sqrt{\left(d-x\right)^2+b^2}}=\frac{\sin\alpha}{v_1}-\frac{\sin\beta}{v_2}.
$$

令 $T'\left(x\right)=0$, 得 $\frac{\sin\alpha}{\sin\beta}=\frac{v_1}{v_2}$, 即折射定律. 又

$$
T''\left(x\right)=\frac{a^2}{v_1\left(x^2+a^2\right)^{3/2}}+\frac{b^2}{v_2\left(\left(d-x\right)^2+b^2\right)^{3/2}}>0,
$$

故 $T'\left(x\right)=0$ 的点为极小值点. 由**命题 3.1 (唯一极值点即全局极值点)**, 该点即为时间最少的路径.

$\blacksquare$

## 3.3-4

设一电灯可以沿铅垂线 $OB$ 移动, $OA$ 是一条水平线, 长度为 $a$. 问灯距离 $O$ 点多高时, $A$ 点有最大的照度?

### 解答 3.3-4

设灯距离 $O$ 点的高度为 $h$. 照度 $J$ 与光线入射角的余弦成正比, 与距离的平方成反比. 光线从灯到 $A$ 点 $\left(a,0\right)$ 的距离为 $r=\sqrt{a^2+h^2}$, 入射角 $\theta$ (光线与铅垂线的夹角) 满足 $\cos\theta=\frac{h}{r}$. 故

$$
J\left(h\right)=C\cdot\frac{\cos\theta}{r^2}=\frac{Ch}{\left(a^2+h^2\right)^{3/2}},
$$

其中 $C>0$ 为比例常数.

求导得

$$
J'\left(h\right)=C\cdot\frac{a^2-2h^2}{\left(a^2+h^2\right)^{5/2}}.
$$

令 $J'\left(h\right)=0$, 得 $h=\frac{a}{\sqrt2}$. 当 $h<\frac{a}{\sqrt2}$ 时 $J'\left(h\right)>0$, 当 $h>\frac{a}{\sqrt2}$ 时 $J'\left(h\right)<0$. 由**定理 3.1 (极值点第一充分条件)**, $h=\frac{a}{\sqrt2}$ 为极大值点. 由**命题 3.1 (唯一极值点即全局极值点)**, 此时 $A$ 点照度最大.

$\blacksquare$

## 3.3-5

证明不等式: $x^\alpha-\alpha{x}+\alpha-1\le0$ 对一切 $x>0$, 其中 $0<\alpha<1$.

### 解答 3.3-5

令 $f\left(x\right)=x^\alpha-\alpha{x}+\alpha-1$ ($x>0$). 求导得

$$
f'\left(x\right)=\alpha{x}^{\alpha-1}-\alpha=\alpha\left(x^{\alpha-1}-1\right).
$$

令 $f'\left(x\right)=0$, 得 $x=1$. 当 $0<{}x<1$ 时 $f'\left(x\right)>0$, 当 $x>1$ 时 $f'\left(x\right)<0$. 由**定理 3.1 (极值点第一充分条件)**, $x=1$ 为极大值点. 又 $f\left(1\right)=0$. 由**命题 3.1 (唯一极值点即全局极值点)**, $f\left(1\right)=0$ 为最大值. 故 $f\left(x\right)\le0$.

$\blacksquare$

## 3.3-6

证明: 设 $a>0$, $b>0$, $p>1$, $q>1$, 且 $\frac1p+\frac1q=1$, 则 $a^{1/p}b^{1/q}\le\frac{a}{p}+\frac{b}{q}$.

### 解答 3.3-6

在 3.3-5 中取 $\alpha=\frac1p$, 则 $1-\alpha=\frac1q$. 对任意 $x>0$,

$$
x^{1/p}-\frac1px+\frac1p-1\le0.
$$

令 $x=\frac{a}{b}$, 代入并两边乘以 $b$, 整理得

$$
a^{1/p}b^{1/q}\le\frac{a}{p}+\frac{b}{q}.
$$

此即杨氏不等式.

$\blacksquare$

## 3.3-7

设 $\triangle{A}BC$ 的边分别为 $a,b$ 与 $c$. 假定 $b=c$, 且 $a+b+c=2l$, 其中 $l$ 为一定数. 问 $\triangle{A}BC$ 何时面积最大?

### 解答 3.3-7

因 $b=c$, 三角形为等腰三角形. 由 $a+2b=2l$, 得 $b=l-\frac{a}2$. 面积为

$$
S=\frac12a\sqrt{b^2-\frac{a^2}{4}}=\frac12a\sqrt{l^2-la}.
$$

为求最大值, 只需最大化 $S^2=\frac14\left(l^2a^2-la^3\right)$. 求导得

$$
\left(S^2\right)'=\frac{la}{4}\left(2l-3a\right).
$$

令 $\left(S^2\right)'=0$, 得 $a=\frac{2l}{3}$. 当 $0<{}a<\frac{2l}{3}$ 时 $\left(S^2\right)'>0$, 当 $\frac{2l}{3}<{}a<2l$ 时 $\left(S^2\right)'<0$. 由**定理 3.1 (极值点第一充分条件)**, $a=\frac{2l}{3}$ 为极大值点. 此时 $b=c=\frac{2l}{3}$, 即三角形为等边三角形时面积最大.

$\blacksquare$

## 3.3-8

设 $f\left(x\right)=\sin^px+\cos^px$, 求它在 $\left[0,\frac\pi2\right]$ 上的最大值与最小值.

### 解答 3.3-8

求导得

$$
f'\left(x\right)=p\sin{x}\cos{x}\left(\sin^{p-2}x-\cos^{p-2}x\right).
$$

令 $f'\left(x\right)=0$, 在 $\left(0,\frac\pi2\right)$ 内得 $x=\frac\pi4$. 计算各点函数值:

- $f\left(0\right)=1$,
- $f\left(\frac\pi4\right)=2^{1-p/2}$,
- $f\left(\frac\pi2\right)=1$.

当 $p>2$ 时, $2^{1-p/2}<1$. 故最大值为 $1$ (在端点处达到), 最小值为 $2^{1-p/2}$ (在 $x=\frac\pi4$ 处达到).

$\blacksquare$

## 3.4-1-2

写出函数 $y=\frac1{1-x}$ 在 $x=0$ 点的局部泰勒公式.

### 解答 3.4-1-2

对 $f\left(x\right)=\frac1{1-x}$ 求各阶导数: $f^{\left(n\right)}\left(x\right)=\frac{n!}{\left(1-x\right)^{n+1}}$. 故 $f^{\left(n\right)}\left(0\right)=n!$. 由**定理 4.1 (局部泰勒展开式)**,

$$
\frac1{1-x}=1+x+x^2+\cdots+x^n+o\left(x^n\right)\quad\left(x\to0\right).
$$

$\blacksquare$

## 3.4-1-4

写出函数 $y=\arctan{x}$ 在 $x=0$ 点的局部泰勒公式 (展开至 $x^5$ 为止).

### 解答 3.4-1-4

计算得 $f\left(0\right)=0$, $f'\left(0\right)=1$, $f''\left(0\right)=0$, $f'''\left(0\right)=-2$, $f^{\left(4\right)}\left(0\right)=0$, $f^{\left(5\right)}\left(0\right)=24$. 由**定理 4.1 (局部泰勒展开式)**,

$$
\arctan{x}=x-\frac{x^3}{3}+\frac{x^5}{5}+o\left(x^5\right)\quad\left(x\to0\right).
$$

$\blacksquare$

## 3.4-1-5

写出函数 $y=\tan{x}$ 在 $x=0$ 点的局部泰勒公式 (展开至 $x^3$ 为止).

### 解答 3.4-1-5

计算得 $f\left(0\right)=0$, $f'\left(0\right)=1$, $f''\left(0\right)=0$, $f'''\left(0\right)=2$. 由**定理 4.1 (局部泰勒展开式)**,

$$
\tan{x}=x+\frac{x^3}{3}+o\left(x^3\right)\quad\left(x\to0\right).
$$

$\blacksquare$

## 3.4-4

将 $y=\sin\left(x+\alpha\right)$ 在 $\alpha=0$ 点展开成带拉格朗日余项的泰勒公式, 并估计余项大小.

### 解答 3.4-4

将 $x$ 视作常数, 对 $\alpha$ 求导: $\frac{\mathrm{d}}{\mathrm{d}\alpha}\sin\left(x+\alpha\right)=\cos\left(x+\alpha\right)$, $\frac{\mathrm{d}^2}{\mathrm{d}\alpha^2}\sin\left(x+\alpha\right)=-\sin\left(x+\alpha\right)$. 在 $\alpha=0$ 处, $\sin{x}$ 与 $\cos{x}$. 由**定理 4.2 (带拉格朗日余项的泰勒公式)**,

$$
\sin\left(x+\alpha\right)=\sin{x}+\left(\cos{x}\right)\alpha-\frac{\sin\left(x+\xi\right)}2\alpha^2,
$$

其中 $\xi$ 介于 $0$ 与 $\alpha$ 之间. 余项 $r\left(\alpha\right)=-\frac{\sin\left(x+\xi\right)}2\alpha^2$, 故 $\left|r\left(\alpha\right)\right|\le\frac{\alpha^2}2$.

$\blacksquare$

## 3.4-5

将 $y=x+\frac{x^3}3$ 在 $x=\pm1$ 点展成泰勒公式. 说明: 任何多项式 $P_n\left(x\right)$ 在任何一点 $a$ 的 $n$ 次泰勒展开式之余项为 $0$.

### 解答 3.4-5

$f'\left(x\right)=1+x^2$, $f''\left(x\right)=2x$, $f'''\left(x\right)=2$, $f^{\left(4\right)}\left(x\right)=0$.

在 $x=1$ 处: $f\left(1\right)=\frac43$, $f'\left(1\right)=2$, $f''\left(1\right)=2$, $f'''\left(1\right)=2$. 由**定理 4.1 (局部泰勒展开式)**,

$$
x+\frac{x^3}3=\frac43+2\left(x-1\right)+\left(x-1\right)^2+\frac13\left(x-1\right)^3.
$$

在 $x=-1$ 处:

$$
x+\frac{x^3}3=-\frac43+2\left(x+1\right)-\left(x+1\right)^2+\frac13\left(x+1\right)^3.
$$

对于一般多项式 $P_n\left(x\right)$, $P_n^{\left(n+1\right)}\left(x\right)\equiv0$. 由**定理 4.2 (带拉格朗日余项的泰勒公式)**, 余项 $R_n\left(x\right)=0$. 即多项式的泰勒展开式是精确的.

$\blacksquare$

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

注意到 $\left(f'\right)^{\left(k\right)}\left(a\right)=f^{\left(k+1\right)}\left(a\right)$, 比较两式即得 $T_{n+1}'\left(x\right)=U_n\left(x\right)$.

$\blacksquare$

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

当 $n$ 为偶数时, $\left(x-x_0\right)^n>0$ ($x\ne{x}_0$). 若 $f^{\left(n\right)}\left(x_0\right)>0$, 则 $f\left(x\right)-f\left(x_0\right)>0$, 故 $x_0$ 为极小值点. 若 $f^{\left(n\right)}\left(x_0\right)<0$, 则 $f\left(x\right)-f\left(x_0\right)<0$, 故 $x_0$ 为极大值点.

$\blacksquare$
