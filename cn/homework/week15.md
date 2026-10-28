# week15

> **命题 3.1 (唯一极值点即全局极值点)**<br>设 $y=f\left(x\right)$ 在区间 $\left(a,b\right)$ (或 $\left[a,b\right]$) 上连续. 若 $x_0$ 是 $\left(a,b\right)$ 中唯一的极值点, 则当 $x_0$ 为极大值点时, $f\left(x_0\right)$ 为最大值; 当 $x_0$ 为极小值点时, $f\left(x_0\right)$ 为最小值.

> **定理 3.1 (极值点第一充分条件)**<br>设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中可导, 且 $x_0\in\left(a,b\right)$ 是 $f$ 的一个稳定点, 即 $f'\left(x_0\right)=0$. 若存在 $r> 0$, 使得当 $x\in\left(x_0-r,x_0\right)$ 时 $f'\left(x\right)> 0$, 当 $x\in\left(x_0,x_0+r\right)$ 时 $f'\left(x\right)< 0$, 则 $f\left(x_0\right)$ 是极大值; 若符号相反, 则 $f\left(x_0\right)$ 是极小值.

> **定理 3.2 (极值点第二充分条件)**<br>设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中可导, $x_0\in\left(a,b\right)$ 是其稳定点, 并假定 $f$ 在 $x_0$ 有二阶导数. 若 $f''\left(x_0\right)> 0$, 则 $x_0$ 为极小值点; 若 $f''\left(x_0\right)< 0$, 则 $x_0$ 为极大值点.

---

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

- $x=\sqrt{\frac53}$: $y''> 0$, 故为极小值点.
- $x=-\sqrt{\frac53}$: $y''< 0$, 故为极大值点.
- $x=\frac1{\sqrt3}$: $y''< 0$, 故为极大值点.
- $x=-\frac1{\sqrt3}$: $y''> 0$, 故为极小值点.

由**定理 3.2 (极值点第二充分条件)**, 上述判断成立. $\blacksquare$

---

## 3.3-1-3

求函数 $y=x\ln x$ ($x> 0$) 的稳定点, 并判断这些稳定点是否为极值点.

### 解答 3.3-1-3

求导得 $y'=\ln x+1$. 令 $y'=0$, 得 $x=\frac1e$.

再求二阶导数: $y''=\frac1x> 0$ ($x> 0$). 故 $y''\left(\frac1e\right)=e> 0$. 由**定理 3.2 (极值点第二充分条件)**, $x=\frac1e$ 为极小值点, 极小值为 $y\left(\frac1e\right)=-\frac1e$. $\blacksquare$

---

## 3.3-2

设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续. 假定 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 内有唯一极值点. 证明: (1) 函数在该极值点附近一定是严格极大或严格极小; (2) 若该极值点为极大值点, 则一定是最大值点; 若为极小值点, 则一定是最小值点.

### 解答 3.3-2

(1) 设 $x_0\in\left(a,b\right)$ 为唯一极值点. 若 $x_0$ 不是严格极大值点, 则存在一列点 $x_n\to x_0$ ($x_n\ne x_0$) 使得 $f\left(x_n\right)\ge f\left(x_0\right)$. 但若在 $x_0$ 的任意邻域内都有函数值等于 $f\left(x_0\right)$ 的点, 则 $f$ 在 $x_0$ 附近为常数, 从而有无穷多个极值点, 与唯一性矛盾. 故 $x_0$ 必为严格极大值点 (或严格极小值点).

(2) 设 $x_0$ 为极大值点. 反证: 假定 $f\left(x_0\right)$ 不是 $\left[a,b\right]$ 上的最大值, 则存在 $x_1\in\left[a,b\right]$ 使得 $f\left(x_1\right)> f\left(x_0\right)$. 考虑闭区间 $\left[x_0,x_1\right]$ 上的连续函数 $f$. 因 $f\left(x_1\right)> f\left(x_0\right)$ 且 $x_0$ 为严格极大值点, 故 $f$ 在 $\left(x_0,x_1\right)$ 内某点达到最小值, 该点即为极小值点. 这与 $x_0$ 是唯一极值点矛盾.

故 $f\left(x_0\right)$ 必为最大值. 极小值点的情形类似. 此即**命题 3.1 (唯一极值点即全局极值点)**. $\blacksquare$

---

## 3.3-3

(光的折射定律) 设有甲, 乙两种介质, 其交界面为一平面. 假设光自甲种介质中之 $A$ 点发出, 经过两种介质的交界面到达乙种介质中的 $B$ 点处. 从物理学上我们知道, 光所走的路径一定满足折射定律: $\frac{\sin\alpha}{\sin\beta}=\frac{v_1}{v_2}$, 其中 $\alpha$ 是光的入射角, $\beta$ 是折射角, $v_1,v_2$ 分别为光在甲, 乙两种介质中的速度. 证明光所走的路径是时间最少的路径.

### 解答 3.3-3

设交界面为 $x$ 轴, $A=\left(0,a\right)$ (甲介质, $y> 0$), $B=\left(d,-b\right)$ (乙介质, $y< 0$). 设光在交界面上的入射点为 $P=\left(x,0\right)$.

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
T''\left(x\right)=\frac{a^2}{v_1\left(x^2+a^2\right)^{3/2}}+\frac{b^2}{v_2\left(\left(d-x\right)^2+b^2\right)^{3/2}}> 0,
$$

故 $T'\left(x\right)=0$ 的点为极小值点. 由**命题 3.1 (唯一极值点即全局极值点)**, 该点即为时间最少的路径. $\blacksquare$

---

## 3.3-4

设一电灯可以沿铅垂线 $OB$ 移动, $OA$ 是一条水平线, 长度为 $a$. 问灯距离 $O$ 点多高时, $A$ 点有最大的照度?

### 解答 3.3-4

设灯距离 $O$ 点的高度为 $h$. 照度 $J$ 与光线入射角的余弦成正比, 与距离的平方成反比. 光线从灯到 $A$ 点 $\left(a,0\right)$ 的距离为 $r=\sqrt{a^2+h^2}$, 入射角 $\theta$ (光线与铅垂线的夹角) 满足 $\cos\theta=\frac{h}{r}$. 故

$$
J\left(h\right)=C\cdot\frac{\cos\theta}{r^2}=\frac{Ch}{\left(a^2+h^2\right)^{3/2}},
$$

其中 $C> 0$ 为比例常数.

求导得

$$
J'\left(h\right)=C\cdot\frac{a^2-2h^2}{\left(a^2+h^2\right)^{5/2}}.
$$

令 $J'\left(h\right)=0$, 得 $h=\frac{a}{\sqrt2}$. 当 $h< \frac{a}{\sqrt2}$ 时 $J'\left(h\right)> 0$, 当 $h> \frac{a}{\sqrt2}$ 时 $J'\left(h\right)< 0$. 由**定理 3.1 (极值点第一充分条件)**, $h=\frac{a}{\sqrt2}$ 为极大值点. 由**命题 3.1 (唯一极值点即全局极值点)**, 此时 $A$ 点照度最大. $\blacksquare$

---

## 3.3-5

证明不等式: $x^\alpha-\alpha x+\alpha-1\le0$ 对一切 $x> 0$, 其中 $0< \alpha< 1$.

### 解答 3.3-5

令 $f\left(x\right)=x^\alpha-\alpha x+\alpha-1$ ($x> 0$). 求导得

$$
f'\left(x\right)=\alpha x^{\alpha-1}-\alpha=\alpha\left(x^{\alpha-1}-1\right).
$$

令 $f'\left(x\right)=0$, 得 $x=1$. 当 $0< x< 1$ 时 $f'\left(x\right)> 0$, 当 $x> 1$ 时 $f'\left(x\right)< 0$. 由**定理 3.1 (极值点第一充分条件)**, $x=1$ 为极大值点. 又 $f\left(1\right)=0$. 由**命题 3.1 (唯一极值点即全局极值点)**, $f\left(1\right)=0$ 为最大值. 故 $f\left(x\right)\le0$. $\blacksquare$

---

## 3.3-6

证明: 设 $a> 0$, $b> 0$, $p> 1$, $q> 1$, 且 $\frac1p+\frac1q=1$, 则 $a^{1/p}b^{1/q}\le\frac{a}{p}+\frac{b}{q}$.

### 解答 3.3-6

在 3.3-5 中取 $\alpha=\frac1p$, 则 $1-\alpha=\frac1q$. 对任意 $x> 0$,

$$
x^{1/p}-\frac1p x+\frac1p-1\le0.
$$

令 $x=\frac{a}{b}$, 代入并两边乘以 $b$, 整理得

$$
a^{1/p}b^{1/q}\le\frac{a}{p}+\frac{b}{q}.
$$

此即杨氏不等式. $\blacksquare$

---

## 3.3-7

设 $\triangle ABC$ 的边分别为 $a,b$ 与 $c$. 假定 $b=c$, 且 $a+b+c=2l$, 其中 $l$ 为一定数. 问 $\triangle ABC$ 何时面积最大?

### 解答 3.3-7

因 $b=c$, 三角形为等腰三角形. 由 $a+2b=2l$, 得 $b=l-\frac a2$. 面积为

$$
S=\frac12 a\sqrt{b^2-\frac{a^2}{4}}=\frac12 a\sqrt{l^2-la}.
$$

为求最大值, 只需最大化 $S^2=\frac14\left(l^2a^2-la^3\right)$. 求导得

$$
\left(S^2\right)'=\frac{la}{4}\left(2l-3a\right).
$$

令 $\left(S^2\right)'=0$, 得 $a=\frac{2l}{3}$. 当 $0< a< \frac{2l}{3}$ 时 $\left(S^2\right)'> 0$, 当 $\frac{2l}{3}< a< 2l$ 时 $\left(S^2\right)'< 0$. 由**定理 3.1 (极值点第一充分条件)**, $a=\frac{2l}{3}$ 为极大值点. 此时 $b=c=\frac{2l}{3}$, 即三角形为等边三角形时面积最大. $\blacksquare$

---

## 3.3-8

设 $f\left(x\right)=\sin^p x+\cos^p x$, 求它在 $\left[0,\frac\pi2\right]$ 上的最大值与最小值.

### 解答 3.3-8

求导得

$$
f'\left(x\right)=p\sin x\cos x\left(\sin^{p-2}x-\cos^{p-2}x\right).
$$

令 $f'\left(x\right)=0$, 在 $\left(0,\frac\pi2\right)$ 内得 $x=\frac\pi4$. 计算各点函数值:

- $f\left(0\right)=1$,
- $f\left(\frac\pi4\right)=2^{1-p/2}$,
- $f\left(\frac\pi2\right)=1$.

当 $p> 2$ 时, $2^{1-p/2}< 1$. 故最大值为 $1$ (在端点处达到), 最小值为 $2^{1-p/2}$ (在 $x=\frac\pi4$ 处达到). $\blacksquare$
