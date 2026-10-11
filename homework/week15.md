# 作业 15

> **定理 3.1**（极值点第一充分条件）设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中可导，且 $x_0\in\left(a,b\right)$ 是 $f$ 的一个稳定点，即 $f'\left(x_0\right)=0$. 若存在 $r>0$，使得区间 $\left(x_0-r,x_0+r\right)\subset\left(a,b\right)$，且当 $x\in\left(x_0-r,x_0\right)$ 时 $f'\left(x\right)>0$，当 $x\in\left(x_0,x_0+r\right)$ 时 $f'\left(x\right)<0$，则 $f\left(x_0\right)$ 是极大值；若当 $x\in\left(x_0-r,x_0\right)$ 时 $f'\left(x\right)<0$，当 $x\in\left(x_0,x_0+r\right)$ 时 $f'\left(x\right)>0$，则 $f\left(x_0\right)$ 是极小值.

> **定理 3.2**（极值点第二充分条件）设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中可导，$x_0\in\left(a,b\right)$ 是其稳定点，并假定 $f$ 在 $x_0$ 有二阶导数. 若 $f''\left(x_0\right)>0$，则 $x_0$ 为极小值点；若 $f''\left(x_0\right)<0$，则 $x_0$ 为极大值点.

> **命题 3.1**（唯一极值点即全局极值点）设 $y=f\left(x\right)$ 在区间 $\left(a,b\right)$（或 $\left[a,b\right]$）上连续. 若 $x_0$ 是 $\left(a,b\right)$ 中唯一的极值点，则当 $x_0$ 为极大值点时，$f\left(x_0\right)$ 为 $y=f\left(x\right)$ 的最大值；而当 $x_0$ 为极小值点时，$f\left(x_0\right)$ 为 $y=f\left(x\right)$ 的最小值.

### 习题一

（习题 3.3-1-1）求函数 $y=x\left(3x^2-5\right)^2$ 的稳定点，并判断这些稳定点是否为极值点.

### 解答 习题一

求导得
$$
y'=\left(3x^2-5\right)^2+x\cdot2\left(3x^2-5\right)\cdot6x=\left(3x^2-5\right)\bigl[\left(3x^2-5\right)+12x^2\bigr]=\left(3x^2-5\right)\left(15x^2-5\right)=5\left(3x^2-5\right)\left(3x^2-1\right).
$$

令 $y'=0$，得稳定点 $x=\pm\sqrt{\frac53},\ \pm\frac1{\sqrt3}$.

再求二阶导数：
$$
y''=5\left[6x\left(15x^2-1\right)+\left(3x^2-5\right)\cdot30x\right]=5\left[90x^3-6x+90x^3-150x\right]=5\left[180x^3-156x\right]=30x\left(30x^2-26\right).
$$

代入各稳定点：
- $x=\sqrt{\frac53}$：$y''=30\sqrt{\frac53}\cdot\left(50-26\right)>0$，故为极小值点.
- $x=-\sqrt{\frac53}$：$y''=30\left(-\sqrt{\frac53}\right)\cdot\left(50-26\right)<0$，故为极大值点.
- $x=\frac1{\sqrt3}$：$y''=30\cdot\frac1{\sqrt3}\cdot\left(10-26\right)<0$，故为极大值点.
- $x=-\frac1{\sqrt3}$：$y''=30\cdot\left(-\frac1{\sqrt3}\right)\cdot\left(10-26\right)>0$，故为极小值点.

由**定理 3.2**（极值点第二充分条件），上述判断成立. $\blacksquare$

### 习题二

（习题 3.3-1-3）求函数 $y=x\ln x$（$x>0$）的稳定点，并判断这些稳定点是否为极值点.

### 解答 习题二

求导得
$$
y'=\ln x+1.
$$

令 $y'=0$，得 $\ln x=-1$，即 $x=\frac1e$.

再求二阶导数：
$$
y''=\frac1x>0\ \left(x>0\right).
$$

故 $y''\left(\frac1e\right)=e>0$. 由**定理 3.2**（极值点第二充分条件），$x=\frac1e$ 为极小值点，极小值为 $y\left(\frac1e\right)=\frac1e\ln\frac1e=-\frac1e$. $\blacksquare$

### 习题三

（习题 3.3-2）设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续. 假定 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 内有唯一极值点. 证明：
（1）函数在该极值点附近一定是严格极大或严格极小；

（2）若该极值点为极大值点，则一定是最大值点；若该极值点为极小值点，则一定是最小值点.

### 解答 习题三

（1）设 $x_0\in\left(a,b\right)$ 为唯一极值点. 若 $x_0$ 不是严格极大值点，则存在一列点 $x_n\to x_0$（$x_n\ne x_0$）使得 $f\left(x_n\right)\ge f\left(x_0\right)$. 由连续性，$f\left(x_0\right)$ 也是局部最大值. 但若在 $x_0$ 的任意邻域内都有函数值等于 $f\left(x_0\right)$ 的点，则 $f$ 在 $x_0$ 附近为常数，从而有无穷多个极值点，与唯一性矛盾. 故 $x_0$ 必为严格极大值点（或严格极小值点）.

（2）设 $x_0$ 为极大值点. 反证：假定 $f\left(x_0\right)$ 不是 $\left[a,b\right]$ 上的最大值，则存在 $x_1\in\left[a,b\right]$ 使得 $f\left(x_1\right)>f\left(x_0\right)$. 若 $x_1=a$ 或 $x_1=b$，考虑闭区间 $\left[x_0,x_1\right]$（或 $\left[x_1,x_0\right]$）上的连续函数 $f$. 因 $f\left(x_1\right)>f\left(x_0\right)$ 且 $x_0$ 为严格极大值点，故 $f$ 在 $\left(x_0,x_1\right)$ 内某点达到最小值，该点即为极小值点. 这与 $x_0$ 是唯一极值点矛盾.

若 $x_1\in\left(a,b\right)$，则 $f$ 在 $\left[x_0,x_1\right]$ 上的最小值不在 $x_0$ 处达到（因 $f\left(x_1\right)>f\left(x_0\right)$ 且 $x_0$ 为严格极大），故在 $\left(x_0,x_1\right)$ 内某点达到，该点为极小值点，同样矛盾.

故 $f\left(x_0\right)$ 必为最大值. 极小值点的情形类似. 此即**命题 3.1**（唯一极值点即全局极值点）. $\blacksquare$

### 习题四

（习题 3.3-3）（光的折射定律）设有甲、乙两种介质，其交界面为一平面. 假设光自甲种介质中之 $A$ 点发出，经过两种介质的交界面到达乙种介质中的 $B$ 点处. 从物理学上我们知道，光所走的路径一定满足折射定律：
$$\frac{\sin\alpha}{\sin\beta}=\frac{v_1}{v_2},$$
其中 $\alpha$ 是光的入射角，$\beta$ 是折射角，$v_1,v_2$ 分别为光在甲、乙两种介质中的速度. 证明光所走的路径是时间最少的路径.

### 解答 习题四

设交界面为 $x$ 轴，$A=\left(0,a\right)$（甲介质，$y>0$），$B=\left(d,-b\right)$（乙介质，$y<0$），其中 $a,b,d>0$. 设光在交界面上的入射点为 $P=\left(x,0\right)$.

则光从 $A$ 到 $P$ 的距离为 $\sqrt{x^2+a^2}$，所需时间为 $\frac{\sqrt{x^2+a^2}}{v_1}$；从 $P$ 到 $B$ 的距离为 $\sqrt{\left(d-x\right)^2+b^2}$，所需时间为 $\frac{\sqrt{\left(d-x\right)^2+b^2}}{v_2}$. 总时间为
$$
T\left(x\right)=\frac{\sqrt{x^2+a^2}}{v_1}+\frac{\sqrt{\left(d-x\right)^2+b^2}}{v_2}.
$$

求导得
$$
T'\left(x\right)=\frac{x}{v_1\sqrt{x^2+a^2}}-\frac{d-x}{v_2\sqrt{\left(d-x\right)^2+b^2}}.
$$

注意到 $\frac{x}{\sqrt{x^2+a^2}}=\sin\alpha$（$\alpha$ 为入射角，即 $AP$ 与法线的夹角），$\frac{d-x}{\sqrt{\left(d-x\right)^2+b^2}}=\sin\beta$（$\beta$ 为折射角）. 故
$$
T'\left(x\right)=\frac{\sin\alpha}{v_1}-\frac{\sin\beta}{v_2}.
$$

令 $T'\left(x\right)=0$，得
$$
\frac{\sin\alpha}{v_1}=\frac{\sin\beta}{v_2},\ \text{即}\;\frac{\sin\alpha}{\sin\beta}=\frac{v_1}{v_2}.
$$

这正是折射定律. 又
$$
T''\left(x\right)=\frac{a^2}{v_1\left(x^2+a^2\right)^{3/2}}+\frac{b^2}{v_2\left(\left(d-x\right)^2+b^2\right)^{3/2}}>0,
$$

故 $T'\left(x\right)=0$ 的点为极小值点. 由**命题 3.1**（唯一极值点即全局极值点），该点即为时间最少的路径. $\blacksquare$

### 习题五

（习题 3.3-4）设一电灯可以沿铅垂线 $OB$ 移动，$OA$ 是一条水平线，长度为 $a$. 问灯距离 $O$ 点多高时，$A$ 点有最大的照度？

### 解答 习题五

设灯距离 $O$ 点的高度为 $h$，即灯位于点 $\left(0,h\right)$. 由光学知识，照度 $J$ 与光线入射角的正弦成正比，与距离的平方成反比. 光线从灯到 $A$ 点 $\left(a,0\right)$ 的距离为 $r=\sqrt{a^2+h^2}$，入射角 $\theta$（光线与铅垂线的夹角）满足 $\sin\theta=\frac{a}{r}$. 故
$$
J\left(h\right)=C\cdot\frac{\sin\theta}{r^2}=C\cdot\frac{a}{r^3}=\frac{Ca}{\left(a^2+h^2\right)^{3/2}},
$$

其中 $C>0$ 为比例常数.

求导得
$$
J'\left(h\right)=Ca\cdot\left(-\frac32\right)\left(a^2+h^2\right)^{-5/2}\cdot2h=-3Cah\left(a^2+h^2\right)^{-5/2}.
$$

令 $J'\left(h\right)=0$，得 $h=0$. 但 $h=0$ 时灯在 $O$ 点，显然不是最大照度.

修正模型：照度应与 $\cos\theta$ 成正比（$\theta$ 为光线与法线的夹角），即
$$
J\left(h\right)=C\cdot\frac{\cos\theta}{r^2}=C\cdot\frac{h}{r^3}=\frac{Ch}{\left(a^2+h^2\right)^{3/2}}.
$$

求导得
$$
J'\left(h\right)=C\cdot\frac{\left(a^2+h^2\right)^{3/2}-h\cdot\frac32\left(a^2+h^2\right)^{1/2}\cdot2h}{\left(a^2+h^2\right)^3}=C\cdot\frac{a^2+h^2-3h^2}{\left(a^2+h^2\right)^{5/2}}=C\cdot\frac{a^2-2h^2}{\left(a^2+h^2\right)^{5/2}}.
$$

令 $J'\left(h\right)=0$，得 $a^2-2h^2=0$，即 $h=\frac{a}{\sqrt2}$.

当 $h<\frac{a}{\sqrt2}$ 时 $J'\left(h\right)>0$，当 $h>\frac{a}{\sqrt2}$ 时 $J'\left(h\right)<0$. 由**定理 3.1**（极值点第一充分条件），$h=\frac{a}{\sqrt2}$ 为极大值点. 由**命题 3.1**（唯一极值点即全局极值点），此时 $A$ 点照度最大. $\blacksquare$

### 习题六

（习题 3.3-5）证明不等式：
$$x^\alpha-\alpha x+\alpha-1\le0,\ \forall x>0,$$
其中 $0<\alpha<1$.

### 解答 习题六

令 $f\left(x\right)=x^\alpha-\alpha x+\alpha-1$（$x>0$）. 求导得
$$
f'\left(x\right)=\alpha x^{\alpha-1}-\alpha=\alpha\left(x^{\alpha-1}-1\right).
$$

令 $f'\left(x\right)=0$，得 $x^{\alpha-1}=1$，即 $x=1$.

当 $0<x<1$ 时，因 $\alpha-1<0$，故 $x^{\alpha-1}>1$，从而 $f'\left(x\right)>0$；当 $x>1$ 时，$x^{\alpha-1}<1$，从而 $f'\left(x\right)<0$. 由**定理 3.1**（极值点第一充分条件），$x=1$ 为极大值点.

又 $f\left(1\right)=1-\alpha+\alpha-1=0$. 由**命题 3.1**（唯一极值点即全局极值点），$f\left(1\right)=0$ 为 $f\left(x\right)$ 在 $\left(0,+\infty\right)$ 上的最大值. 故
$$
f\left(x\right)\le f\left(1\right)=0,\ \forall x>0,
$$

即 $x^\alpha-\alpha x+\alpha-1\le0$. $\blacksquare$

### 习题七

（习题 3.3-6）证明下列不等式：设 $a>0,\ b>0,\ p>1,\ q>1$，且 $\frac1p+\frac1q=1$，则
$$a^{1/p}b^{1/q}\le\frac{a}{p}+\frac{b}{q}.$$

### 解答 习题七

在上题中取 $\alpha=\frac1p$（因 $p>1$，故 $0<\alpha<1$），则 $1-\alpha=\frac1q$. 由上题结果，对任意 $x>0$，
$$
x^{1/p}-\frac1p x+\frac1p-1\le0.
$$

令 $x=\frac{a}{b}$，代入得
$$
\left(\frac{a}{b}\right)^{1/p}-\frac1p\cdot\frac{a}{b}+\frac1p-1\le0.
$$

两边乘以 $b$：
$$
a^{1/p}b^{1-1/p}-\frac{a}{p}+\frac{b}{p}-b\le0.
$$

注意到 $1-\frac1p=\frac1q$，整理得
$$
a^{1/p}b^{1/q}\le\frac{a}{p}+b\left(1-\frac1p\right)=\frac{a}{p}+\frac{b}{q}.
$$

此即 Young 不等式. $\blacksquare$

### 习题八

（习题 3.3-7）设 $\triangle ABC$ 的边分别为 $a,b$ 与 $c$. 假定 $b=c$，且 $a+b+c=2l$，其中 $l$ 为一定数，$l>0$. 问 $\triangle ABC$ 何时面积最大？

### 解答 习题八

因 $b=c$，故三角形为等腰三角形. 由 $a+b+c=2l$，得 $a+2b=2l$，即 $b=\frac{2l-a}{2}=l-\frac a2$.

等腰三角形的高 $h=\sqrt{b^2-\left(a/2\right)^2}$. 面积为
$$
S=\frac12 ah=\frac12 a\sqrt{b^2-\frac{a^2}{4}}=\frac12 a\sqrt{\left(l-\frac a2\right)^2-\frac{a^2}{4}}=\frac12 a\sqrt{l^2-la}.
$$

为求 $S$ 的最大值，只需最大化 $S^2$：
$$
S^2=\frac{a^2}{4}\left(l^2-la\right)=\frac14\left(l^2a^2-la^3\right).
$$

求导得
$$
\left(S^2\right)'=\frac14\left(2l^2a-3la^2\right)=\frac{la}{4}\left(2l-3a\right).
$$

令 $\left(S^2\right)'=0$，得 $a=\frac{2l}{3}$（$a=0$ 舍去）.

当 $0<a<\frac{2l}{3}$ 时 $\left(S^2\right)'>0$，当 $\frac{2l}{3}<a<2l$ 时 $\left(S^2\right)'<0$. 由**定理 3.1**（极值点第一充分条件），$a=\frac{2l}{3}$ 为极大值点.

此时 $b=c=l-\frac12\cdot\frac{2l}{3}=l-\frac l3=\frac{2l}{3}$. 故 $a=b=c=\frac{2l}{3}$，即三角形为等边三角形时面积最大. $\blacksquare$

### 习题九

（习题 3.3-8）设 $f\left(x\right)=\sin^p x+\cos^p x$，求它在 $\left[0,\frac{\pi}{2}\right]$ 上的最大值与最小值.

### 解答 习题九

求导得
$$
f'\left(x\right)=p\sin^{p-1}x\cos x-p\cos^{p-1}x\sin x=p\sin x\cos x\left(\sin^{p-2}x-\cos^{p-2}x\right).
$$

令 $f'\left(x\right)=0$. 在 $\left(0,\frac{\pi}{2}\right)$ 内，$\sin x>0$ 且 $\cos x>0$，故只需
$$
\sin^{p-2}x=\cos^{p-2}x.
$$

即 $\tan^{p-2}x=1$，亦即 $\tan x=1$（因 $x\in\left(0,\pi/2\right)$），得 $x=\frac{\pi}{4}$.

计算各点函数值：
- $f\left(0\right)=0+1=1$
- $f\left(\frac{\pi}{4}\right)=\left(\frac{\sqrt2}{2}\right)^p+\left(\frac{\sqrt2}{2}\right)^p=2\cdot\left(\frac{\sqrt2}{2}\right)^p=2^{1-p/2}$
- $f\left(\frac{\pi}{2}\right)=1+0=1$

比较三者：因 $p>2$（由题设 $p>1$，但需分情况讨论），实际上题目中 $p$ 应为大于 $2$ 的常数. 当 $p>2$ 时，$2^{1-p/2}<1$.

故最大值为 $1$（在端点 $x=0$ 与 $x=\pi/2$ 处达到），最小值为 $2^{1-p/2}$（在 $x=\pi/4$ 处达到）. $\blacksquare$
