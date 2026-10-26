# 数学分析

## 实数

**定义**（域）

粗略地说, 一个数集对加, 减, 乘, 除(除数不为 $0$)是封闭的, 并满足交换律, 结合律及分配律, 我们便称该数集为域.

**定义**（有序域）

在一个数域中建立了大小关系, 并且满足下述性质, 则称之为有序域: 对任意 $\alpha,b$, $\alpha=b$, $\alpha< b$, $b< \alpha$ 三种情况有且仅有一种成立; 且当 $a< b,b< c$ 时 $a< c$; 当 $a< b$ 时 $a+c< b+c$; 当 $0< a,b$ 时 $a\cdot b> 0$.

**命题 1.1**（有理数域为有序域）

有理数域 $\mathbb Q$ 是一个有序域.

**定义**（稠密性）

数集 $S$ 被称作在数轴上处处稠密, 如果对于数轴上的任意一个区间 $\left(a,b\right)$, 无论它位于何处, 多么小, $S$ 中都至少有数落在 $\left(a,b\right)$ 之中, 即 $S\cap\left(a,b\right)\ne\varnothing$.

**命题 1.3**（$\sqrt2$ 为无理数）

$\sqrt2$ 不是有理数.

**例 1.1**（无理数的运算）

无理数加有理数为无理数. 无理数乘以有理数为无理数.

**定义**（完备性）

如果一个有序数域满足下列要求, 则称之为完备的(或连续的): 对于任何一个单调递增的有界序列 $\left\{x_n\right\}$, 在该数域中都存在一个数 $a$, 使得 $x_n$ 可以无限接近 $a$.

**命题 1.5**（实数域的完备性）

设 $\left\{x_n\right\}$ 是实数域 $\mathbb R$ 中的任意一个单调递增, 有上界的数列, 则在 $\mathbb R$ 中存在一个数 $a$, 使得 $x_n\le a$, 且 $x_n$ 可以任意接近 $a$.

**定义**（有界集）

设 $E\subset\mathbb R$. 若存在 $M$ 使 $E$ 中一切点 $x$ 都有 $x\le M$, 则称 $E$ 有上界; 若存在 $m$ 使 $E$ 中一切点 $x$ 都有 $x\ge m$, 则称 $E$ 有下界; 既有上界又有下界的集合称作有界集合.

**命题 1.6**（绝对值的性质）

对于任意的 $x,y\in\mathbb R$, 有:

(1) $\left|x\right|\ge0$, 等号当且仅当 $x=0$ 时成立;

(2) $\left|-x\right|=\left|x\right|$;

(3) $\left|x+y\right|\le\left|x\right|+\left|y\right|$.

**命题 1.7**（三角不等式）

对于任意实数 $a,b,c$, 有:

(1) $\left|a-b\right|\ge0$, 等号当且仅当 $a=b$ 时成立;

(2) $\left|a-b\right|=\left|b-a\right|$;

(3) $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

## 函数的概念

**定义**（函数）

设 $x$ 与 $y$ 是两个变量, 分别在实数集合 $X$ 与 $Y$ 中取值. 假如有一种规则 $f$ 使得对每一个值 $x\in X$ 都能找到一个唯一确定的 $y\in Y$ 与之相对应, 则我们称 $f$ 是一个函数, 记作 $f:X\to Y$, 并称 $X$ 为 $f$ 的定义域. $Y$ 中一切可能被取到的函数值集合称作 $f$ 的值域, 记作 $f\left(X\right)$.

**定义**（复合函数）

假定有两个函数 $f:X\to Y$ 及 $g:Y^*\to Z$, 并假定 $Y\subset Y^*$. 对于每一个点 $x\in X$, 存在唯一的 $y=f\left(x\right)\in Y$, 再由 $g$ 得到 $z=g\left(y\right)$. 这样确定的从 $X$ 到 $Z$ 的对应 $x\mapsto z$, 其中 $z=g\left(f\left(x\right)\right)$, 称为 $f$ 与 $g$ 的复合函数, 记作 $z=g\left(f\left(x\right)\right)$.

**定义**（周期函数）

设 $y=f\left(x\right)$ 在 $\mathbb R$ 上有定义, 且存在一个数 $T\ne 0$ 使得 $f\left(x+T\right)=f\left(x\right),\forall x\in\mathbb R$, 则称 $y=f\left(x\right)$ 是周期函数, 其中 $T$ 称作 $f$ 的一个周期.

**命题 2.1**（有界函数的充要条件）

函数 $f:X\to Y$ 为有界函数的充分与必要条件是存在一个 $M> 0$, 使得 $\left|f\left(x\right)\right|\le M,\forall x\in X$.

## 序列的极限

**定义**（序列极限）

设 $\left\{a_n\right\}$ 是一个给定的序列. 若存在一个实数 $l$, 对于任意给定的正数 $\varepsilon$, 无论它多么小, 都存在一个自然数 $N$, 使得 $\left|a_n-l\right|< \varepsilon$, 只要 $n> N$, 则我们称 $a_n$ 以 $l$ 为极限, 记作

$$
\lim\limits_{n\to\infty}a_n=l.
$$

**例 3.3**（正数的 $n$ 次方根趋于 $1$）

设 $a$ 是任意的正数, 则

$$
\lim\limits_{n\to\infty}a^{1/n}=1.
$$

**定理 3.1**（极限四则运算定理）

设 $\left\{a_n\right\}$ 与 $\left\{b_n\right\}$ 都有极限, 它们的极限分别为 $l_1$ 与 $l_2$, 则有

$$
\lim\left(a_n\pm b_n\right)=l_1\pm l_2,;\lim\left(a_n\cdot b_n\right)=l_1\cdot l_2,;\lim\frac{a_n}{b_n}=\frac{l_1}{l_2}.
$$

**定理 3.2**（实数域完备性）

设 $\left\{a_n\right\}$ 是一个单调递增有上界的实数序列, 则存在 $l\in\mathbb R$, 使得 $\left\{a_n\right\}$ 以 $l$ 为极限. 简言之, 单调递增有上界的序列有极限.

## 序列极限的基本性质

**定理 4.2**（夹逼定理）

设 $\left\{a_n\right\},\left\{b_n\right\},\left\{c_n\right\}$ 为三个序列, 并且存在一个自然数 $N_0$, 使得 $c_n\le a_n\le b_n,\forall n\ge N_0$. 若 $c_n$ 与 $b_n$ 都有极限存在, 并都等于 $l$, 则 $a_n$ 的极限存在, 并且也等于 $l$.

**重要极限**（数 $e$）

$$
\lim\limits_{n\to\infty}\left(1+\frac1n\right)^n=e.
$$

其中 $e$ 为无理数, $2< e< 3$.

**定义**（无穷小量）

以 $0$ 为其极限的变量称作无穷小量.

## 函数的极限

**定义**（函数极限）

设 $y=f\left(x\right)$ 在 $a$ 点的一个空心邻域 $\left(a-r,a+r\right)\backslash\left\{a\right\}$ 内有定义. 若存在一个实数 $l$, 对于任意给定的 $\varepsilon> 0$, 无论它多么小, 都存在一个 $\delta> 0$, 使得当 $0< \left|x-a\right|< \delta$ 时, $\left|f\left(x\right)-l\right|< \varepsilon$, 则称当 $x\to a$ 时 $f\left(x\right)$ 以 $l$ 为极限, 记作

$$
\lim\limits_{x\to a}f\left(x\right)=l.
$$

**定义**（单侧极限）

若当 $x\to a+0$(或 $x\to a-0$)时 $f\left(x\right)$ 以 $l$ 为极限, 则称之为右极限(或左极限), 记作

$$
\lim\limits_{x\to a+0}f\left(x\right)=l,;\lim\limits_{x\to a-0}f\left(x\right)=l.
$$

**定理 5.1**（函数极限四则运算）

若 $\lim f\left(x\right)=l_1$, $\lim g\left(x\right)=l_2$, 则

$$
\lim\left(f\pm g\right)=l_1\pm l_2,;\lim\left(f\cdot g\right)=l_1\cdot l_2,;\lim\frac{f}{g}=\frac{l_1}{l_2}\left(l_2\ne0\right).
$$

**命题**（保号性）

若 $\lim\limits_{x\to a}f\left(x\right)=l$ 且 $l\ne0$, 则存在 $\delta> 0$ 使得当 $0< \left|x-a\right|< \delta$ 时 $\left|f\left(x\right)\right|> \frac{\left|l\right|}{2}$.

## 函数极限的性质

**命题 6.1**（重要极限 $\lim\limits_{x\to0}\frac{\sin x}{x}=1$）

$$
\lim\limits_{x\to0}\frac{\sin x}{x}=1.
$$

**重要极限**（数 $e$ 的函数版本）

$$
\lim\limits_{x\to\infty}\left(1+\frac1x\right)^x=e.
$$

**定理 6.2**（函数的夹逼定理）

设

$$
y=f\left(x\right),y=g\left(x\right),y=h\left(x\right)
$$

在 $a$ 点的一个空心邻域内有定义, 且 $h\left(x\right)\le f\left(x\right)\le g\left(x\right)$. 若 $\lim g\left(x\right)=\lim h\left(x\right)=l$, 则

$$
\lim f\left(x\right)=l.
$$

## 连续函数

**定义**（连续函数）

假定 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 内有定义. 若在一点 $x_0\in\left(a,b\right)$ 处 $\lim\limits_{x\to x_0}f\left(x\right)=f\left(x_0\right)$, 则称 $y=f\left(x\right)$ 在 $x_0$ 点连续. 若 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 的每一点都连续, 则称它在 $\left(a,b\right)$ 上连续.

**定理 7.2**（复合函数连续性）

若 $y=g\left(y\right)$ 在 $y_0$ 点连续, $y=f\left(x\right)$ 在 $x_0$ 点连续且 $f\left(x_0\right)=y_0$, 则复合函数 $y=g\left(f\left(x\right)\right)$ 在 $x_0$ 点连续.

**定义**（初等函数）

初等函数在其定义域内是连续的.

## 闭区间上连续函数的性质

**定理 8.1**（中间值定理）

设 $y=f\left(x\right)$ 在闭区间 $\left[a,b\right]$ 上连续, 且 $f\left(a\right)$ 与 $f\left(b\right)$ 反号, 则存在一点 $c\in\left(a,b\right)$ 使得 $f\left(c\right)=0$. 更一般地, $f$ 可取到 $f\left(a\right)$ 与 $f\left(b\right)$ 之间的一切值.

**定理 8.2**（有界性定理）

闭区间上的连续函数是有界的, 且达到最大值与最小值.

**区间套原理**

设 $\left\{\left[a_n,b_n\right]\right\}$ 为一列闭区间, 满足 $\left[a_{n+1},b_{n+1}\right]\subset\left[a_n,b_n\right]$ 且 $b_n-a_n\to0$, 则存在唯一的实数 $l$ 属于所有区间.

## 复合函数与反函数的导数

**定理 2.1**（复合函数求导法则）

设 $y=f\left(u\right)$ 在 $u$ 处可导, $u=g\left(x\right)$ 在 $x$ 处可导, 则复合函数 $y=f\left(g\left(x\right)\right)$ 在 $x$ 处可导, 且

$$
\frac{\mathrm dy}{\mathrm dx}=\frac{\mathrm dy}{\mathrm du}\cdot\frac{\mathrm du}{\mathrm dx}=f'\left(g\left(x\right)\right)g'\left(x\right).
$$

## 微分的概念

**定义**（微分）

设 $y=f\left(x\right)$ 在 $x_0$ 附近有定义. 若存在常数 $A$, 使得 $\Delta y=A\Delta x+o\left(\Delta x\right)$, 则称 $f$ 在 $x_0$ 可微, $\mathrm dy=A\Delta x$ 称为微分, 且 $A=f'\left(x_0\right)$.

**定义**（高阶无穷小）

若

$$
\lim\limits_{x\to0}\frac{\alpha\left(x\right)}{\beta\left(x\right)}=0,
$$

则称 $\alpha\left(x\right)=o\left(\beta\left(x\right)\right)$.

## 高阶导数与高阶微分

**定义**（高阶导数）

若 $y=f\left(x\right)$ 的导函数 $f'\left(x\right)$ 在 $x_0$ 点可导, 则其导数称为 $f$ 的二阶导数, 记作 $f''\left(x_0\right)$ 或 $\frac{\mathrm d^2f}{\mathrm dx^2}$. 一般地, $n$ 阶导数 $f^{\left(n\right)}\left(x\right)$ 由 $n-1$ 阶导数再求导得到.

## 一阶微分的形式不变性

**定理 5.1**（参变量函数求导公式）

设 $x=\varphi\left(t\right),y=\psi\left(t\right)$ 在 $t_0$ 点可导, 且 $\varphi'\left(t_0\right)\ne0$, 则参变量函数的导数为

$$
\frac{\mathrm dy}{\mathrm dx}=\frac{\psi'\left(t\right)}{\varphi'\left(t\right)}.
$$

## 拉格朗日中值定理

**定理 1.1**（费马定理）

设 $f\left(x\right)$ 在一点 $a$ 附近有定义, 且在 $a$ 点可微. 若 $a$ 点为 $y=f\left(x\right)$ 的极值点, 则 $f'\left(a\right)=0$.

**定理 1.2**（罗尔定理）

设函数 $y=f\left(x\right)$ 在闭区间 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 中处处可导, 且 $f\left(a\right)=f\left(b\right)$. 则在 $\left(a,b\right)$ 中至少存在一点 $c$, 使得 $f'\left(c\right)=0$.

**定理 1.3**（拉格朗日中值定理）

设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 内可导. 则存在点 $c\in\left(a,b\right)$, 使得
$$
f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}.
$$
**定理 1.4**（常数定理）

设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中处处可导, 且 $f'\left(x\right)=0$($x\in\left(a,b\right)$). 则 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 内必为常数.

**定理 1.5**（单调性判定）

设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 可导. 若 $f'\left(x\right)> 0$($\ge 0$)$\forall x\in\left(a,b\right)$, 则 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上严格递增(递增); 若 $f'\left(x\right)< 0$($\le 0$)$\forall x\in\left(a,b\right)$, 则 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上严格递减(递减).

## 柯西中值定理与洛必达法则

**定理 2.1**（柯西中值定理）

设 $y=f\left(x\right)$ 与 $y=g\left(x\right)$ 在 $\left[a,b\right]$ 中连续, 在 $\left(a,b\right)$ 中可导, 且 $g'\left(x\right)\ne0$($a< x< b$). 则存在点 $c\in\left(a,b\right)$, 使得
$$
\frac{f\left(b\right)-f\left(a\right)}{g\left(b\right)-g\left(a\right)}=\frac{f'\left(c\right)}{g'\left(c\right)}.
$$
**定理 2.2**（洛必达法则，$\frac00$ 型）

设 $y=f\left(x\right)$ 及 $y=g\left(x\right)$ 在 $a$ 点的一个空心邻域内有定义且可导, $g'\left(x\right)\ne0$. 假定 $\lim\limits_{x\to a}f\left(x\right)=\lim\limits_{x\to a}g\left(x\right)=0$, 且 $\lim\limits_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ 存在. 则
$$
\lim_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}.
$$
**定理 2.3**（洛必达法则，$\frac{\infty}{\infty}$ 型）

设 $y=f\left(x\right)$ 与 $y=g\left(x\right)$ 在 $a$ 点的一个空心邻域内有定义且可导, $g'\left(x\right)\ne0$. 假定

$$
\lim\limits_{x\to a}f\left(x\right)=\lim\limits_{x\to a}g\left(x\right)=\infty,
$$

且 $\lim\limits_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ 存在. 则
$$
\lim_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}.
$$
## 极值问题

**定理 3.1**（极值点第一充分条件）

设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中可导, 且 $x_0\in\left(a,b\right)$ 是 $f$ 的一个稳定点, 即 $f'\left(x_0\right)=0$. 若存在 $r> 0$, 使得区间 $\left(x_0-r,x_0+r\right)\subset\left(a,b\right)$, 且当 $x\in\left(x_0-r,x_0\right)$ 时 $f'\left(x\right)> 0$, 当 $x\in\left(x_0,x_0+r\right)$ 时 $f'\left(x\right)< 0$, 则 $f\left(x_0\right)$ 是极大值; 若当 $x\in\left(x_0-r,x_0\right)$ 时 $f'\left(x\right)< 0$, 当 $x\in\left(x_0,x_0+r\right)$ 时 $f'\left(x\right)> 0$, 则 $f\left(x_0\right)$ 是极小值.

**定理 3.2**（极值点第二充分条件）

设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中可导, $x_0\in\left(a,b\right)$ 是其稳定点, 并假定 $f$ 在 $x_0$ 有二阶导数. 若 $f''\left(x_0\right)> 0$, 则 $x_0$ 为极小值点; 若 $f''\left(x_0\right)< 0$, 则 $x_0$ 为极大值点.

**命题 3.1**（唯一极值点即全局极值点）

设 $y=f\left(x\right)$ 在区间 $\left(a,b\right)$(或 $\left[a,b\right]$)上连续. 若 $x_0$ 是 $\left(a,b\right)$ 中唯一的极值点, 则当 $x_0$ 为极大值点时, $f\left(x_0\right)$ 为 $y=f\left(x\right)$ 的最大值; 而当 $x_0$ 为极小值点时, $f\left(x_0\right)$ 为 $y=f\left(x\right)$ 的最小值.

## 泰勒公式

**定理 4.1**（局部泰勒展开式）

设 $y=f\left(x\right)$ 在 $x_0$ 点附近有定义, 且有 $n$ 阶导数 $f^{\left(n\right)}\left(x_0\right)$. 则
$$
f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\frac{f''\left(x_0\right)}{2!}\left(x-x_0\right)^2+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right)\left(x\to x_0\right).
$$
**定理 4.2**（带拉格朗日余项的泰勒公式）

设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上有 $n$ 阶连续导数, 在 $\left(a,b\right)$ 中有 $n+1$ 阶导数. 则对任意 $x,x_0\in\left[a,b\right]$, 存在介于 $x_0$ 与 $x$ 之间的点 $\xi$, 使得
$$
f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+\frac{f^{\left(n+1\right)}\left(\xi\right)}{\left(n+1\right)!}\left(x-x_0\right)^{n+1}.
$$
## 函数的凸凹性及函数作图

**定义**（凸函数）

设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中有定义. 若对 $\left(a,b\right)$ 中任意两点 $x_1$ 与 $x_2$($x_1< x_2$), 都有
$$
f\left(tx_1+\left(1-t\right)x_2\right)\le tf\left(x_1\right)+\left(1-t\right)f\left(x_2\right),
$$
其中 $t$ 是 $\left(0,1\right)$ 中任意数, 则称函数 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 上是凸函数. 反之, 若上述不等式反向成立, 则称 $y=f\left(x\right)$ 为 $\left(a,b\right)$ 上的凹函数.

**定理 5.1**（凸函数的二阶导数判别）

设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 上二阶可导. 则 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 上为凸函数的充要条件是 $f''\left(x\right)\ge0$($\forall x\in\left(a,b\right)$); $y=f\left(x\right)$ 在 $\left(a,b\right)$ 上为凹函数的充要条件是 $f''\left(x\right)\le0$($\forall x\in\left(a,b\right)$).

## 原函数与不定积分

**定义**（原函数与不定积分）

设 $y=f\left(x\right)$ 定义在 $\left(a,b\right)$ 区间之中. 若 $F\left(x\right)$ 在 $\left(a,b\right)$ 中可微, 且 $F'\left(x\right)=f\left(x\right)$($\forall x\in\left(a,b\right)$), 则称 $y=F\left(x\right)$ 是 $y=f\left(x\right)$ 的一个原函数. $f\left(x\right)$ 的一切原函数 $F\left(x\right)+C$($C$ 为任意常数)称作 $f\left(x\right)$ 的不定积分, 记作
$$
\int f\left(x\right)\,\mathrm{d}x=F\left(x\right)+C.
$$
**定理 1.3**（不定积分的线性法则）

设 $y=f\left(x\right)$ 及 $y=g\left(x\right)$ 在某个区间中有原函数. 则
$$
\int\left[af\left(x\right)+bg\left(x\right)\right]\mathrm{d}x=a\int f\left(x\right)\,\mathrm{d}x+b\int g\left(x\right)\,\mathrm{d}x,
$$
其中 $a,b$ 是两个任意常数.

## 不定积分换元法则

**定理 2.1**（第一换元法则）

设 $F'\left(u\right)=f\left(u\right)$, 且 $u=\varphi\left(x\right)$ 可导, 则
$$
\int f\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm{d}x=F\left(\varphi\left(x\right)\right)+C.
$$
**定理 2.2**（第二换元法则）

设 $x=\varphi\left(t\right)$ 可导且有反函数, 又设

$$
\int f\left(\varphi\left(t\right)\right)\varphi'\left(t\right)\,\mathrm{d}t=G\left(t\right)+C,
$$

则
$$
\int f\left(x\right)\,\mathrm{d}x=G\left(\varphi^{-1}\left(x\right)\right)+C.
$$
## 分部积分法

**定理 3.1**（分部积分公式）

设 $u\left(x\right),v\left(x\right)$ 可导, 则
$$
\int u\left(x\right)\,\mathrm{d}v\left(x\right)=u\left(x\right)v\left(x\right)-\int v\left(x\right)\,\mathrm{d}u\left(x\right).
$$
## 有理函数的积分

**定理 4.1**（有理函数的分解）

任何有理函数 $\frac{P\left(x\right)}{Q\left(x\right)}$ 都可以分解为一个多项式与若干部分分式之和, 其中每个部分分式形如 $\frac{A}{\left(x-a\right)^k}$ 或 $\frac{Bx+C}{\left(x^2+px+q\right)^m}$($p^2-4q< 0$).

## 不定积分的有理化方法

**定理 5.1**（三角有理式的积分法）

三角函数的有理式 $R\left(\sin x,\cos x\right)$ 的不定积分, 总可通过万能代换 $t=\tan\frac{x}{2}$ 化为关于 $t$ 的有理函数的不定积分. 此时

$$
\sin x=\frac{2t}{1+t^2},;\cos x=\frac{1-t^2}{1+t^2},;\mathrm{d}x=\frac{2\,\mathrm{d}t}{1+t^2}.
$$

## 实数集合的上下确界

**定义**（上确界与下确界）

设 $E$ 为有界集合. 若存在实数 $\beta$ 满足: 
(1) $\beta$ 是 $E$ 的上界($\forall x\in E,x\le\beta$); 

(2) 对任意 $\varepsilon> 0$, 存在 $x_0\in E$ 使得 $x_0> \beta-\varepsilon$, 则称 $\beta$ 为 $E$ 的上确界, 记作 $\sup E$. 类似地定义下确界 $\inf E$.

**定义**（振幅）

设 $f\left(x\right)$ 在区间 $I$ 中有定义且有界. 称

$$
\omega_f\left(I\right)=\sup\left\{f\left(x\right):x\in I\right\}-\inf\left\{f\left(x\right):x\in I\right\}
$$

为 $f$ 在 $I$ 上的振幅.

**定理 1.3**（连续的充要条件）

设 $y=f\left(x\right)$ 在 $x_0$ 点附近为有界函数. 则 $f$ 在 $x_0$ 点连续的充要条件是 $\omega_f\left(x_0\right)=0$.

## 上下极限与柯西收敛原理

**定理 2.1**（上下极限与极限存在）

设 $\left\{a_n\right\}$ 为一个有界序列. 则序列 $\left\{a_n\right\}$ 有极限之充要条件为其上极限与下极限相等.

**定理 2.2**（柯西收敛原理）

序列 $\left\{a_n\right\}$ 有极限之充要条件是: 对任意给定的 $\varepsilon> 0$, 存在一个自然数 $N$, 使得 $\left|a_n-a_m\right|< \varepsilon$ (只要 $m\ge N,n\ge N$).

## 闭区间上连续函数的一致连续性

**定义**（一致连续）

设 $y=f\left(x\right)$ 在一个区间 $X$ 上有定义. 如果对任意给定的 $\varepsilon> 0$, 存在一个 $\delta> 0$, 使得 $X$ 中的任意两点 $x_1$ 与 $x_2$, 都有 $\left|f\left(x_1\right)-f\left(x_2\right)\right|< \varepsilon$ (只要 $\left|x_1-x_2\right|< \delta$), 则称 $y=f\left(x\right)$ 在 $X$ 中一致连续.

**定理 3.2**（有限覆盖定理）

设 $\mathcal{F}=\left\{I_\alpha:\alpha\in A\right\}$ 是闭区间 $\left[a,b\right]$ 的任意一个开覆盖, 则存在 $\mathcal{F}$ 中的有限个元素 $I_{\alpha_1},\cdots,I_{\alpha_n}$, 使得

$$
\left[a,b\right]\subset\bigcup\limits_{k=1}^n I_{\alpha_k}.
$$

## 定积分的基本概念

**定义**（定积分）

设 $f\left(x\right)$ 定义在区间 $\left[a,b\right]$ 上. 对 $\left[a,b\right]$ 作分割

$$
T:a=x_0< x_1< \cdots< x_n=b,
$$
记 $\Delta x_k=x_k-x_{k-1}$, $\lambda\left(T\right)=\max_{1\le k\le n}\Delta x_k$. 若存在常数 $I$, 使得对任意 $\varepsilon> 0$, 存在 $\delta> 0$, 只要 $\lambda\left(T\right)< \delta$, 不论分割 $T$ 如何取, 中间点 $\xi_k\in\left[x_{k-1},x_k\right]$ 如何取, 都有

$$
\left|\sum_{k=1}^n f\left(\xi_k\right)\Delta x_k-I\right|< \varepsilon,
$$

则称 $I$ 为 $f\left(x\right)$ 在 $\left[a,b\right]$ 上的定积分, 记作

$$
\int_a^b f\left(x\right)\,\mathrm{d}x.
$$

**性质**（定积分的比较性质）

设 $f,g$ 在 $\left[a,b\right]$ 上可积, 且 $f\left(x\right)\le g\left(x\right)$ ($\forall x\in\left[a,b\right]$), 则

$$
\int_a^b f\left(x\right)\,\mathrm{d}x\le\int_a^b g\left(x\right)\,\mathrm{d}x,;\int_a^b f\left(x\right)\,\mathrm{d}x\ge0.
$$

## 连续函数的可积性

**引理 2.1**（分点加密的效应）

设 $T'$ 是由分割 $T$ 增加有限个分点而形成的分割, 则 $d\left(T\right)\le d\left(T'\right)$, $D\left(T'\right)\le D\left(T\right)$, 即分点增加时达布小和不减, 达布大和不增.

**定理 2.2**（可积的充要条件）

设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上有界. 则 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上黎曼可积的充要条件是

$$
\lim_{\lambda\left(T\right)\to0}\left[D\left(T\right)-d\left(T\right)\right]=0,
$$

其中 $D\left(T\right)$, $d\left(T\right)$ 分别为达布大和与达布小和.

## 二重积分的概念

**命题 1.3**（可求面积的充要条件）

设 $E$ 为平面上的有界集合, $\partial E$ 为其边界点集合. 则 $E$ 是可求面积的充要条件是 $m^*\left(\partial E\right)=0$, 即 $\partial E$ 为零面积集合. 特别地, 边界为逐段光滑曲线的有界区域是可求面积的.

**定理 1.4**（可积的充要条件）

设 $D$ 为可求面积的有界闭区域. 则 $z=f\left(x,y\right)$ 在 $D$ 上可积的充要条件是

$$
\lim_{\lambda\left(T\right)\to0}\left[D\left(T\right)-d\left(T\right)\right]=0,;\lim_{\lambda\left(T\right)\to0}\sum_i\omega_i\Delta\sigma_i=0.
$$

其中 $\omega_i$ 为 $f$ 在小区域 $D_i$ 上的振幅.

**定理 1.5**（连续函数可积）

设 $D$ 是平面上有界闭区域, 其边界是零面积集合. 又设 $z=f\left(x,y\right)$ 在 $D$ 上连续. 则 $z=f\left(x,y\right)$ 在 $D$ 上可积.

**性质**（二重积分的基本性质）

设 $D$ 为可求面积的有界闭区域, $f,g$ 在 $D$ 上可积, 则:

(2) 积分对区域的可加性: 若 $D$ 分解为两个可求面积, 互不重叠的区域 $D_1,D_2$, 则

$$
\iint_D f=\iint_{D_1}f+\iint_{D_2}f;
$$

(3) 积分保持不等号: 若 $f\left(x,y\right)\le g\left(x,y\right)$ ($\forall\left(x,y\right)\in D$), 则

$$
\iint_D f\le\iint_D g;
$$

(4) 积分中值定理: 若 $f$ 在 $D$ 上连续, 则存在 $\left(x_0,y_0\right)\in D$ 使 $\iint_D f=f\left(x_0,y_0\right)\cdot S$, 其中 $S$ 为 $D$ 的面积.

## 二重积分的计算

**定理 2.1**（化二重积分为累次积分）

设 $z=f\left(x,y\right)$ 在闭区域 $D$ 上连续,

$$
D=\left\{\left(x,y\right):a\le x\le b,\varphi_1\left(x\right)\le y\le\varphi_2\left(x\right)\right\},
$$

其中 $\varphi_1,\varphi_2$ 在 $\left[a,b\right]$ 上连续. 则

$$
\iint_D f\left(x,y\right)\,\mathrm{d}x\mathrm{d}y=\int_a^b\mathrm{d}x\int_{\varphi_1\left(x\right)}^{\varphi_2\left(x\right)}f\left(x,y\right)\,\mathrm{d}y.
$$

**定理 2.2**（极坐标下的二重积分）

设 $D$ 为可求面积的有界闭区域, $z=f\left(x,y\right)$ 在 $D$ 上可积. 则

$$
\iint_D f\left(x,y\right)\,\mathrm{d}x\mathrm{d}y=\iint_{D^*}f\left(r\cos\theta,r\sin\theta\right)\,r\,\mathrm{d}r\mathrm{d}\theta,
$$

其中

$$
D^*=\left\{\left(r,\theta\right):\left(r\cos\theta,r\sin\theta\right)\in D\right\}.
$$

## 二重积分的一般变量替换法则

**定理 3.1**（二重积分的变量替换公式）

设 $z=f\left(x,y\right)$ 在可求面积的有界闭区域 $D$ 上连续. 设变换

$$
F:\left(u,v\right)\mapsto\left(x\left(u,v\right),y\left(u,v\right)\right)
$$

是有界闭区域 $G$ 到 $D$ 的一一映射, $x\left(u,v\right),y\left(u,v\right)$ 在 $G$ 上有连续的一阶偏导数, 且雅可比行列式 $J\left(u,v\right)=\frac{\partial\left(x,y\right)}{\partial\left(u,v\right)}\ne0$. 则

$$
\iint_D f\left(x,y\right)\,\mathrm{d}x\mathrm{d}y=\iint_G f\left(x\left(u,v\right),y\left(u,v\right)\right)\left| J\left(u,v\right)\right|\,\mathrm{d}u\mathrm{d}v.
$$

特别地, 区域 $D$ 的面积为

$$
m\left(D\right)=\iint_G\left| J\left(u,v\right)\right|\,\mathrm{d}u\mathrm{d}v.
$$

## 三重积分的概念与计算

**定理 4.2**（三重积分的穿线法）

设

$$
\Omega=\left\{\left(x,y,z\right):\left(x,y\right)\in D,z_1\left(x,y\right)\le z\le z_2\left(x,y\right)\right\},
$$

其中 $D$ 为 $Oxy$ 平面上可求面积的有界闭区域, $z_1,z_2$ 在 $D$ 上连续, $f$ 在 $\Omega$ 上连续. 则

$$
\iiint_\Omega f\left(x,y,z\right)\,\mathrm{d}V=\iint_D\mathrm{d}x\mathrm{d}y\int_{z_1\left(x,y\right)}^{z_2\left(x,y\right)}f\left(x,y,z\right)\,\mathrm{d}z.
$$

**定理 4.4**（三重积分换元公式）

在变量替换 $x=x\left(u,v,w\right)$, $y=y\left(u,v,w\right)$, $z=z\left(u,v,w\right)$ 下,

$$
\iiint_\Omega f\,\mathrm{d}x\mathrm{d}y\mathrm{d}z=\iiint_{\Omega'}f\left(x\left(u,v,w\right),y\left(u,v,w\right),z\left(u,v,w\right)\right)\left| J\left(u,v,w\right)\right|\,\mathrm{d}u\mathrm{d}v\mathrm{d}w,
$$

其中 $J=\frac{\partial\left(x,y,z\right)}{\partial\left(u,v,w\right)}$. 特别地, 柱坐标 $\left(r,\theta,z\right)$ 下 $\left| J\right|=r$, 球坐标 $\left(\rho,\varphi,\theta\right)$ 下 $\left| J\right|=\rho^2\sin\varphi$.

## 重积分应用举例

**命题 5.1**（曲面面积公式）

设 $z=f\left(x,y\right)$ 在可求面积的有界闭区域 $D$ 上有连续的一阶偏导数, 则曲面 $z=f\left(x,y\right)$ ($\left(x,y\right)\in D$) 的面积为

$$
S=\iint_D\sqrt{1+f_x^2\left(x,y\right)+f_y^2\left(x,y\right)}\,\mathrm{d}x\mathrm{d}y.
$$

**公式**（质心坐标）

设物体占据区域 $\Omega$, 密度为 $\rho\left(x,y,z\right)$, 质量 $m=\iiint_\Omega\rho\,\mathrm{d}V$, 则质心坐标为

$$
x_0=\frac1m\iiint_\Omega x\rho\,\mathrm{d}V,;y_0=\frac1m\iiint_\Omega y\rho\,\mathrm{d}V,;z_0=\frac1m\iiint_\Omega z\rho\,\mathrm{d}V.
$$

**公式**（转动惯量）

物体关于 $z$ 轴的转动惯量为

$$
J_z=\iiint_\Omega\left(x^2+y^2\right)\rho\left(x,y,z\right)\,\mathrm{d}V.
$$

## 第一型曲线积分

**定理 1.2**（光滑曲线的弧长公式）

设空间曲线 $L$ 的参数方程为 $x=x\left(t\right)$, $y=y\left(t\right)$, $z=z\left(t\right)$ ($\alpha\le t\le\beta$), 且 $x'\left(t\right),y'\left(t\right),z'\left(t\right)$ 在 $\left[\alpha,\beta\right]$ 上连续. 则 $L$ 可求长, 且弧长

$$
s=\int_\alpha^\beta\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm{d}t.
$$

弧微分

$$
\mathrm{d}s=\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm{d}t.
$$

**定理 1.3**（第一型曲线积分的计算）

设 $L$ 为光滑曲线, 参数方程同上, $f\left(x,y,z\right)$ 在 $L$ 上连续, 则

$$
\int_L f\left(x,y,z\right)\,\mathrm{d}s=\int_\alpha^\beta f\left(x\left(t\right),y\left(t\right),z\left(t\right)\right)\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm{d}t.
$$

注意上限 $\beta$ 须大于下限 $\alpha$.

## 第二型曲线积分

**定理 2.2**（格林公式）

设 $L$ 为平面 $Oxy$ 上逐段光滑的简单闭曲线, 它所围的有界闭区域为 $D$, $P\left(x,y\right),Q\left(x,y\right)$ 在 $D$ 上有一阶连续偏导数. 则

$$
\oint_{L^+}P\left(x,y\right)\,\mathrm{d}x+Q\left(x,y\right)\,\mathrm{d}y=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y,
$$

其中 $L^+$ 表示逆时针方向.

**定理 2.4**（积分与路径无关的条件）

设 $D$ 为平面单连通域, $P,Q$ 在 $D$ 内有一阶连续偏导数. 则曲线积分 $\int P\,\mathrm{d}x+Q\,\mathrm{d}y$ 与路径无关等价于

$$
\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}
$$

在 $D$ 内处处成立.

**定理 2.5**（恰当微分形式）

在上述条件下, $P\,\mathrm{d}x+Q\,\mathrm{d}y$ 为恰当微分形式的充要条件是 $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$ 在 $D$ 内处处成立.

## 曲面积分

**公式**（第一型曲面积分的计算）

设光滑曲面 $S$ 由参数方程 $x=x\left(u,v\right)$, $y=y\left(u,v\right)$, $z=z\left(u,v\right)$ ($\left(u,v\right)\in D$) 给出, $E=x_u^2+y_u^2+z_u^2$, $F=x_ux_v+y_uy_v+z_uz_v$, $G=x_v^2+y_v^2+z_v^2$. 则

$$
\iint_S f\left(x,y,z\right)\,\mathrm{d}S=\iint_D f\left(x\left(u,v\right),y\left(u,v\right),z\left(u,v\right)\right)\sqrt{EG-F^2}\,\mathrm{d}u\mathrm{d}v.
$$

特别地, 当曲面由 $z=g\left(x,y\right)$ ($\left(x,y\right)\in D$) 给出时, $\mathrm{d}S=\sqrt{1+g_x^2+g_y^2}\,\mathrm{d}x\mathrm{d}y$.

**公式**（第二型曲面积分的计算）

设曲面 $S:z=g\left(x,y\right)$ ($\left(x,y\right)\in D$), 取上侧. 则

$$
\iint_S P\,\mathrm{d}y\mathrm{d}z+Q\,\mathrm{d}z\mathrm{d}x+R\,\mathrm{d}x\mathrm{d}y=\iint_D\left[P\left(-g_x\right)+Q\left(-g_y\right)+R\right]\mathrm{d}x\mathrm{d}y.
$$

下侧时取负号.

## 奥-高公式与斯托克斯公式

**定理 4.1**（奥-高公式）

设空间曲面 $S$ 是分片光滑的封闭曲面, 所围空间闭区域为 $\Omega$, $P,Q,R$ 在 $\Omega$ 中有一阶连续偏导数. 则

$$
\oiint_{S^+}P\,\mathrm{d}y\mathrm{d}z+Q\,\mathrm{d}z\mathrm{d}x+R\,\mathrm{d}x\mathrm{d}y=\iiint_\Omega\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)\mathrm{d}V,
$$

其中 $S^+$ 表示外侧.

**定理 4.2**（斯托克斯公式）

设 $S$ 为分片光滑的双侧曲面, 边界 $L$ 为分段光滑闭曲线, $L$ 的定向与 $S$ 的法向量构成右手系. 则

$$
\oint_{L^+}P\,\mathrm{d}x+Q\,\mathrm{d}y+R\,\mathrm{d}z=\iint_{S^+}\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right)\mathrm{d}y\mathrm{d}z+\left(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}\right)\mathrm{d}z\mathrm{d}x+\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y.
$$

## 场论初步

**定义**（散度）

设向量场 $\boldsymbol{F}=\left(P,Q,R\right)$, 其中 $P,Q,R$ 有一阶连续偏导数. 则

$$
\operatorname{div}\boldsymbol{F}=\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}.
$$

**定义**（旋度）

向量场 $\boldsymbol{F}=\left(P,Q,R\right)$ 的旋度为

$$
\operatorname{rot}\boldsymbol{F}=\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z},\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x},\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right).
$$

## 无穷级数的基本概念

**定义**（级数收敛）

给定数列 $\left\{a_n\right\}$, 作部分和 $S_n=\sum_{k=1}^{n}a_k$. 若 $\lim_{n\to\infty}S_n=S$ 存在且有限, 则称级数 $\sum_{n=1}^{\infty}a_n$ 收敛, $S$ 称为其和; 否则称级数发散.

**定理 1.1**（收敛级数的必要条件）

若级数 $\sum_{n=1}^{\infty}a_n$ 收敛, 则

$$
\lim_{n\to\infty}a_n=0.
$$

## 正项级数

**定理 2.2**（比较判别法）

设 $\sum a_n$ 与 $\sum b_n$ 为正项级数, 且存在自然数 $N_0$ 使 $a_n\le b_n$($n\ge N_0$). 若 $\sum b_n$ 收敛, 则 $\sum a_n$ 收敛; 若 $\sum a_n$ 发散, 则 $\sum b_n$ 发散.

**定理 2.3**（比较判别法的极限形式）

设 $\sum a_n$ 与 $\sum b_n$ 为正项级数, $b_n\ne 0$, 且

$$
\lim_{n\to\infty}\frac{a_n}{b_n}=l.
$$

当 $0< l< +\infty$ 时, 两级数同时收敛或同时发散.

**定理 2.6**（达朗贝尔判别法）

设 $\sum a_n$ 为正项级数, $a_n> 0$. 若

$$
\lim_{n\to\infty}\frac{a_{n+1}}{a_n}=r,
$$

则当 $r< 1$ 时级数收敛, 当 $r> 1$ 时级数发散.

**定理 2.9**（积分判别法）

设 $f\left(x\right)$ 在 $\left[1,+\infty\right)$ 上正, 单调递减, 则级数 $\sum_{n=1}^{\infty}f\left(n\right)$ 与反常积分 $\int_1^{+\infty}f\left(x\right)\,\mathrm{d}x$ 同时收敛或同时发散.

## 任意项级数

**定理 3.2**（狄利克雷判别法）

设数列 $\left\{b_n\right\}$ 单调趋于零, 且级数 $\sum a_n$ 的部分和序列有界, 则级数 $\sum a_nb_n$ 收敛.

**定理 3.3**（阿贝尔判别法）

设数列 $\left\{b_n\right\}$ 单调有界, 且级数 $\sum a_n$ 收敛, 则级数 $\sum a_nb_n$ 收敛.

## 无穷乘积

**定理 4.1**（无穷乘积与级数的关系）

设 $p_n> 0$($n=1,2,\dots$), 则无穷乘积 $\prod_{n=1}^{\infty}p_n$ 收敛的充要条件是级数 $\sum_{n=1}^{\infty}\ln p_n$ 收敛, 且此时
$$
\prod_{n=1}^{\infty}p_n=\exp\left(\sum_{n=1}^{\infty}\ln p_n\right).
$$
**定理 4.2**（同号项无穷乘积）

设 $\alpha_n\ge 0$(或 $\alpha_n\le 0$), 则无穷乘积 $\prod_{n=1}^{\infty}\left(1+\alpha_n\right)$ 收敛的充要条件是级数 $\sum_{n=1}^{\infty}\alpha_n$ 收敛.

**定理 4.4**（绝对收敛）

设 $\alpha_n\ne -1$, 则无穷乘积 $\prod_{n=1}^{\infty}\left(1+\alpha_n\right)$ 绝对收敛的充要条件是级数 $\sum_{n=1}^{\infty}\left|\alpha_n\right|$ 收敛.

## 函数序列的一致收敛性

**定义**（函数序列的一致收敛）

设 $\left\{f_n\left(x\right)\right\}$ 在集合 $X$ 上有定义, $f\left(x\right)$ 为 $X$ 上的函数. 若对任意 $\varepsilon> 0$, 存在自然数 $N$, 使得当 $n> N$ 时, 对一切 $x\in X$ 均有 $\left|f_n\left(x\right)-f\left(x\right)\right|< \varepsilon$, 则称 $\left\{f_n\left(x\right)\right\}$ 在 $X$ 上一致收敛于 $f\left(x\right)$.

**定理 1.1**（M 判别法）

设存在数列 $M_n> 0$, $M_n\to 0$, 使得 $\left|f_n\left(x\right)-f\left(x\right)\right|\le M_n$ 对一切 $x\in X$ 成立, 则 $\left\{f_n\left(x\right)\right\}$ 在 $X$ 上一致收敛于 $f\left(x\right)$.

**定理 1.2**（极限函数的连续性）

设 $\left\{f_n\left(x\right)\right\}$ 在区间 $X$ 上一致收敛于 $f\left(x\right)$, 且每个 $f_n\left(x\right)$ 在 $X$ 上连续, 则 $f\left(x\right)$ 在 $X$ 上连续.

## 函数项级数

**定理 2.2**（魏尔斯特拉斯 M 判别法）

设 $\left|u_n\left(x\right)\right|\le a_n$ 对一切 $x\in X$ 及充分大的 $n$ 成立, 且 $\sum a_n$ 收敛, 则函数项级数 $\sum u_n\left(x\right)$ 在 $X$ 上一致收敛.

**定理 2.4**（狄利克雷判别法）

设函数项级数 $\sum a_n\left(x\right)b_n\left(x\right)$ 中, $\sum a_n\left(x\right)$ 的部分和序列在 $X$ 上一致有界, $b_n\left(x\right)$ 对每个 $x\in X$ 关于 $n$ 单调, 且 $b_n\left(x\right)$ 在 $X$ 上一致趋于零, 则 $\sum a_n\left(x\right)b_n\left(x\right)$ 在 $X$ 上一致收敛.

**定理 2.5**（和函数的连续性）

设 $u_n\left(x\right)$ 在区间 $X$ 上连续, 且 $\sum u_n\left(x\right)$ 在 $X$ 上一致收敛, 则其和函数 $S\left(x\right)$ 在 $X$ 上连续.

**定理 2.7**（逐项求导定理）

设 $\sum u_n\left(x\right)$ 在 $\left[a,b\right]$ 上收敛于 $S\left(x\right)$, $u_n\left(x\right)$ 在 $\left[a,b\right]$ 上有连续导数, 且 $\sum u_n'\left(x\right)$ 在 $\left[a,b\right]$ 上一致收敛, 则 $S\left(x\right)$ 在 $\left[a,b\right]$ 上可导, 且

$$
S'\left(x\right)=\sum u_n'\left(x\right).
$$

## 幂级数

**定理 3.2**（收敛半径的柯西公式）

设幂级数 $\sum_{n=0}^{\infty}a_nx^n$, 则其收敛半径 $R$ 满足

$$
\frac{1}{R}=\limsup_{n\to\infty}\sqrt\left[n\right]{\left|a_n\right|}.
$$

**定理 3.3**（收敛半径的达朗贝尔公式）

设 $a_n\ne 0$ 且

$$
\lim_{n\to\infty}\left|\frac{a_n}{a_{n+1}}\right|=R,
$$

则该幂级数的收敛半径为 $R$.

**定理 3.4**（内闭一致收敛性）

幂级数在其收敛区间内部的任意闭区间上一致收敛, 因而可在收敛区间内逐项求导与逐项积分, 且收敛半径不变.

## 泰勒级数

**定理 4.1**（泰勒级数）

若函数 $f\left(x\right)$ 在 $\left(x_0-R,x_0+R\right)$ 内可展开为幂级数

$$
f\left(x\right)=\sum_{n=0}^{\infty}a_n\left(x-x_0\right)^n,
$$

则其系数必为
$$
a_n=\frac{f^{\left(n\right)}\left(x_0\right)}{n!},
$$
即幂级数展开是唯一的, 称为 $f$ 在 $x_0$ 处的泰勒级数.

**定义**（基本展开式）

在 $x=0$ 处有:

$$
e^x=\sum_{n=0}^{\infty}\frac{x^n}{n!}\ \left(\left|x\right|< +\infty\right),;\ln\left(1+x\right)=\sum_{n=1}^{\infty}\frac{\left(-1\right)^{n-1}x^n}{n}\ \left(\left|x\right|< 1\right),;\cos x=\sum_{n=0}^{\infty}\frac{\left(-1\right)^n x^{2n}}{\left(2n\right)!}\ \left(\left|x\right|< +\infty\right).
$$

## 无穷积分

**定义**（无穷积分的收敛）

设函数 $f\left(x\right)$ 在 $\left[a,+\infty\right)$ 上有定义, 且在任意闭区间 $\left[a,A\right]$ 上可积. 若极限 $\lim_{A\to+\infty}\int_a^A f\left(x\right)\,\mathrm{d}x$ 存在, 则称无穷积分 $\int_a^{+\infty} f\left(x\right)\,\mathrm{d}x$ 收敛, 并把这个极限定义为该无穷积分的值; 否则称其发散.

**例 1.2**（$p$-积分）

无穷积分 $\int_1^{+\infty}\frac{\mathrm{d}x}{x^p}$ 当 $p> 1$ 时收敛, 当 $p\le 1$ 时发散.

**定理 1.1**（无穷积分的柯西收敛原理）

设 $f\left(x\right)$ 在 $\left[a,+\infty\right)$ 上有定义, 且在任意闭区间 $\left[a,A\right]$ 上可积. 则无穷积分 $\int_a^{+\infty} f\left(x\right)\,\mathrm{d}x$ 收敛的充要条件是: 对任意 $\varepsilon> 0$, 存在 $X> 0$, 只要 $A',A''> X$, 都有 $\left|\int_{A'}^{A''} f\left(x\right)\,\mathrm{d}x\right|< \varepsilon$.

**定理 1.3**（比较判别法）

设 $f\left(x\right)$ 及 $g\left(x\right)$ 在 $\left[a,+\infty\right)$ 上有定义, 且在任意闭区间 $\left[a,A\right]$ 上可积. 又设存在 $X_0> a$, 使得

$$
0\le f\left(x\right)\le g\left(x\right)\left(\forall x\ge X_0\right).
$$

则若 $\int_a^{+\infty}g\left(x\right)\,\mathrm{d}x$ 收敛, 必有 $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ 收敛; 若 $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ 发散, 必有 $\int_a^{+\infty}g\left(x\right)\,\mathrm{d}x$ 发散.

**定理 1.6**（狄利克雷判别法）

设 $f\left(x\right)$ 与 $g\left(x\right)$ 在 $\left[a,+\infty\right)$ 上有定义, 且在任意区间 $\left[a,A\right]$ 上可积. 若 $f\left(x\right)$ 在 $\left[a,+\infty\right)$ 上单调, 且 $\lim_{x\to+\infty}f\left(x\right)=0$, 又 $\int_a^A g\left(x\right)\,\mathrm{d}x$ 关于 $A$ 有界, 则 $\int_a^{+\infty}f\left(x\right)g\left(x\right)\,\mathrm{d}x$ 收敛.

**定义**（绝对收敛与条件收敛）

若 $\int_a^{+\infty}\left| f\left(x\right)\right|\,\mathrm{d}x$ 收敛, 则称无穷积分 $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ 绝对收敛; 若 $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ 收敛, 但 $\int_a^{+\infty}\left| f\left(x\right)\right|\,\mathrm{d}x$ 发散, 则称其为条件收敛.

## 瑕积分

**定义**（瑕积分的收敛）

设 $f\left(x\right)$ 在 $\left(a,b\right]$ 上有定义, 且在任意闭区间 $\left[a+\eta,b\right]\subset\left(a,b\right]\left(\eta> 0\right)$ 上可积, 而 $a$ 为 $f\left(x\right)$ 的瑕点. 若极限 $\lim_{\eta\to0+0}\int_{a+\eta}^b f\left(x\right)\,\mathrm{d}x$ 存在, 则称瑕积分 $\int_a^b f\left(x\right)\,\mathrm{d}x$ 收敛, 并把该极限定义为其值; 否则称其发散. 瑕点为右端点或区间内点时, 定义完全类似.

**例 2.2**（瑕 $p$-积分）

瑕积分 $\int_a^b\frac{\mathrm{d}x}{\left(x-a\right)^p}$($p> 0$)当 $p< 1$ 时收敛, 当 $p\ge1$ 时发散.

**定义**（绝对收敛与条件收敛）

设 $f\left(x\right)$ 在 $\left(a,b\right]$ 上有定义, $a$ 为瑕点. 若 $\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x$ 收敛, 则称 $\int_a^b f\left(x\right)\,\mathrm{d}x$ 绝对收敛; 若 $\int_a^b f\left(x\right)\,\mathrm{d}x$ 收敛而 $\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x$ 发散, 则称其条件收敛.

**定义**（柯西主值）

设 $f\left(x\right)$ 在 $\left[a,b\right]\setminus\left\{c\right\}$ 上有定义, $c\in\left(a,b\right)$ 为其瑕点. 假若极限

$$
I=\lim_{\eta\to0+0}\left[\int_a^{c-\eta}f\left(x\right)\,\mathrm{d}x+\int_{c+\eta}^b f\left(x\right)\,\mathrm{d}x\right]
$$

存在, 则称瑕积分 $\int_a^b f\left(x\right)\,\mathrm{d}x$ 在柯西主值意义下收敛, 极限值 $I$ 称为其柯西主值, 记作

$$
\mathrm{\left(CPV\right)}\int_a^b f\left(x\right)\,\mathrm{d}x.
$$

## 含参变量积分

**定理 3.3**（积分号下求导）

设 $f\left(x,y\right)$ 与 $f_y\left(x,y\right)$ 在 $\left[a,b\right]\times\left[c,d\right]$ 上连续, 则函数 $I\left(y\right)=\int_a^b f\left(x,y\right)\,\mathrm{d}x$ 在 $\left[c,d\right]$ 上可导, 且
$$
I'\left(y\right)=\int_a^b f_y\left(x,y\right)\,\mathrm{d}x, \forall\,y\in\left[c,d\right].
$$
当积分限也依赖于 $y$ 时, 即 $I\left(y\right)=\int_{a\left(y\right)}^{b\left(y\right)}f\left(x,y\right)\,\mathrm{d}x$, 再由牛顿–莱布尼茨公式补上边界项: 
$$
I'\left(y\right)=f\left(b\left(y\right),y\right)b'\left(y\right)-f\left(a\left(y\right),y\right)a'\left(y\right)+\int_{a\left(y\right)}^{b\left(y\right)}f_y\left(x,y\right)\,\mathrm{d}x.
$$
## 含参变量无穷积分

**定理 4.3**（魏尔斯特拉斯判别法）

设 $f\left(x,y\right)$ 在 $\left[a,+\infty\right)\times Y$ 上有定义. 若存在 $F\left(x\right)$, 使得 (i)

$$
\left| f\left(x,y\right)\right|\le F\left(x\right)\left(\forall x\in\left[a,+\infty\right),y\in Y\right);
$$

(ii) $\int_a^{+\infty}F\left(x\right)\,\mathrm{d}x$ 收敛, 则无穷积分 $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ 关于 $y\in Y$ 一致收敛.

**定理 4.4**（阿贝尔判别法）

设 $f\left(x,y\right),g\left(x,y\right)$ 在 $\left[a,+\infty\right)\times Y$ 上有定义. 若 (i) $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ 关于 $y\in Y$ 一致收敛; (ii) $g\left(x,y\right)$ 关于 $x$ 单调, 且关于 $y\in Y$ 一致有界, 则 $\int_a^{+\infty}f\left(x,y\right)g\left(x,y\right)\,\mathrm{d}x$ 关于 $y\in Y$ 一致收敛.

**定理 4.7**（积分次序交换定理）

设 $f\left(x,y\right)$ 在 $\left[a,+\infty\right)\times\left[c,d\right]$ 上连续, 且 $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ 关于 $y\in\left[c,d\right]$ 一致收敛, 则

$$
\int_c^d\mathrm{d}y\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x=\int_a^{+\infty}\mathrm{d}x\int_c^d f\left(x,y\right)\,\mathrm{d}y.
$$

**定理 4.8**（积分号下求导）

设 $f\left(x,y\right)$ 与 $f_y\left(x,y\right)$ 在 $\left[a,+\infty\right)\times\left[c,d\right]$ 上连续, 且 $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ 关于 $y\in\left[c,d\right]$ 一致收敛, $\int_a^{+\infty}f_y\left(x,y\right)\,\mathrm{d}x$ 也一致收敛, 则 $I\left(y\right)=\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ 在 $\left[c,d\right]$ 上可导, 且

$$
I'\left(y\right)=\int_a^{+\infty}f_y\left(x,y\right)\,\mathrm{d}x.
$$

**例 4.5**（狄利克雷积分）

$$
\int_0^{+\infty}\frac{\sin x}{x}\,\mathrm{d}x=\frac{\pi}{2}.
$$

一般地,

$$
\int_0^{+\infty}\frac{\sin\left(kx\right)}{x}\,\mathrm{d}x=\frac{\pi}{2}\operatorname{sgn}\left(k\right).
$$

## 含参变量瑕积分

**定理 4.3**（魏尔斯特拉斯判别法）

设 $f\left(x,y\right)$ 在 $\left(a,b\right]\times Y$ 上有定义, $a$ 为瑕点. 若存在 $F\left(x\right)$, 使得 (i)

$$
\left| f\left(x,y\right)\right|\le F\left(x\right)\left(\forall x\in\left(a,b\right],y\in Y\right);
$$

(ii) 瑕积分 $\int_a^b F\left(x\right)\,\mathrm{d}x$ 收敛, 则含参变量瑕积分 $\int_a^b f\left(x,y\right)\,\mathrm{d}x$ 关于 $y\in Y$ 一致收敛.

**定理 4.7**（积分次序交换定理）

设 $f\left(x,y\right)$ 在 $\left(a,b\right]\times\left[c,d\right]$ 上连续且保持固定符号, $\int_a^b f\left(x,y\right)\,\mathrm{d}x$ 关于 $y\in\left[c,d\right]$ 一致收敛, 则

$$
\int_c^d\mathrm{d}y\int_a^b f\left(x,y\right)\,\mathrm{d}x=\int_a^b\mathrm{d}x\int_c^d f\left(x,y\right)\,\mathrm{d}y.
$$

## 伽马函数与贝塔函数

**定义**（伽马函数）

$$
\Gamma\left(\alpha\right)=\int_0^{+\infty}t^{\alpha-1}e^{-t}\,\mathrm{d}t\ \left(\alpha> 0\right).
$$

它满足递推公式 $\Gamma\left(\alpha+1\right)=\alpha\Gamma\left(\alpha\right)$, $\Gamma\left(1\right)=1$, $\Gamma\left(n+1\right)=n!$, 且

$$
\Gamma\!\left(\frac12\right)=\sqrt\pi.
$$

**定义**（贝塔函数）

$$
\Beta\left(p,q\right)=\int_0^1 t^{p-1}\left(1-t\right)^{q-1}\,\mathrm{d}t\left(p,q> 0\right),;\Beta\left(p,q\right)=\frac{\Gamma\left(p\right)\Gamma\left(q\right)}{\Gamma\left(p+q\right)}.
$$

**命题**（伽马与贝塔的积分形式）

$$
\int_0^{+\infty}\frac{x^{a-1}}{\left(1+x\right)^{a+b}}\,\mathrm{d}x=\Beta\left(a,b\right),;\int_0^{\pi/2}\sin^m x\cos^n x\,\mathrm{d}x=\frac12 \Beta\!\left(\frac{m+1}{2},\frac{n+1}{2}\right).
$$

## 三角函数系及其正交性

**定义**（内积与范数）

在 $R\left[-\pi,\pi\right]$ 中定义内积

$$
\left\langle f,g\right\rangle=\frac1\pi\int_{-\pi}^\pi f\left(x\right)g\left(x\right)\,\mathrm{d}x,
$$
范数

$$
\left| f\right|=\sqrt{\left\langle f,f\right\rangle}=\left(\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x\right)^{1/2}.
$$

**命题**（三角函数系的正交性）

三角函数系

$$
1,\cos x,\sin x,\cos2x,\sin2x,\cdots
$$

在 $\left[-\pi,\pi\right]$ 上两两正交, 即任意两个不同元素之积在 $\left[-\pi,\pi\right]$ 上的积分为 $0$; 且

$$
\int_{-\pi}^\pi1\,\mathrm{d}x=2\pi,;\int_{-\pi}^\pi\cos^2 nx\,\mathrm{d}x=\int_{-\pi}^\pi\sin^2 nx\,\mathrm{d}x=\pi\left(n=1,2,\cdots\right).
$$

## 周期函数的傅里叶级数

**命题**（傅里叶系数）

设 $f\left(x\right)$ 在 $\left[-\pi,\pi\right]$ 上可积且平方可积, 则其傅里叶级数为

$$
f\left(x\right)\sim\frac{a_0}{2}+\sum_{n=1}^\infty\left(a_n\cos nx+b_n\sin nx\right),
$$

其中

$$
a_n=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\cos nx\,\mathrm{d}x\left(n=0,1,2,\cdots\right),;b_n=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\sin nx\,\mathrm{d}x\left(n=1,2,\cdots\right).
$$

## 傅里叶级数的收敛性

**定理 3.1**（狄利克雷收敛定理）

设 $f\left(x\right)$ 以 $2\pi$ 为周期且在 $\left[-\pi,\pi\right]$ 上逐段单调有界, 则其傅里叶级数在每点 $x$ 收敛于 $\frac{f\left(x+0\right)+f\left(x-0\right)}{2}$; 在 $f$ 的连续点收敛于 $f\left(x\right)$, 在间断点收敛于左右极限的平均值.

**命题**（傅里叶系数）

以 $2\pi$ 为周期的可积函数 $f\left(x\right)$ 的傅里叶系数为

$$
a_n=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\cos nx\,\mathrm{d}x,;b_n=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\sin nx\,\mathrm{d}x.
$$

**定理**（封闭性方程）

设 $f\left(x\right)$ 的傅里叶系数为 $a_n,b_n$, 则

$$
\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x=\frac{a_0^2}{2}+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right).
$$

## 均方逼近与贝塞尔不等式

**定理 4.1**（贝塞尔不等式）

设 $f\left(x\right)$ 在 $\left[-\pi,\pi\right]$ 上黎曼可积, 其傅里叶系数为 $a_n,b_n$, 则

$$
\frac{a_0^2}{2}+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right)\le\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x.
$$

且 $\sum_{n=1}^\infty a_n^2$, $\sum_{n=1}^\infty b_n^2$ 均收敛.

**定理 4.2**（封闭性方程/帕塞瓦尔等式）

设 $f\left(x\right)$ 在 $\left[-\pi,\pi\right]$ 上黎曼可积且平方可积, 则

$$
\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x=\frac{a_0^2}{2}+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right).
$$
