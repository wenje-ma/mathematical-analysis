# 作业 28

> **命题 1.3**（可求面积的充要条件）设 $E$ 为平面上的有界集合, $\partial E$ 为其边界点集合. 则 $E$ 是可求面积的充要条件是 $m^*\left(\partial E\right)=0$, 即 $\partial E$ 为零面积集合. 特别地, 边界为逐段光滑曲线的有界区域是可求面积的.

> **定理 1.4**（可积的充要条件）设 $D$ 为可求面积的有界闭区域. 则 $z=f\left(x,y\right)$ 在 $D$ 上可积的充要条件是
> $$
> \lim_{\lambda\left(T\right)\to0}\left[D\left(T\right)-d\left(T\right)\right]=0,
> $$
> 亦即 $\lim_{\lambda\left(T\right)\to0}\sum_i\omega_i\Delta\sigma_i=0$, 其中 $\omega_i$ 为 $f$ 在小区域 $D_i$ 上的振幅.

> **定理 1.5**（连续函数可积）设 $D$ 是平面上有界闭区域, 其边界是零面积集合. 又设 $z=f\left(x,y\right)$ 在 $D$ 上连续. 则 $z=f\left(x,y\right)$ 在 $D$ 上可积.

> **性质**（二重积分的基本性质）设 $D$ 为可求面积的有界闭区域, $f,g$ 在 $D$ 上可积, 则:
> (2) 积分对区域的可加性: 若 $D$ 分解为两个可求面积, 互不重叠的区域 $D_1,D_2$, 则 $\iint_D f=\iint_{D_1}f+\iint_{D_2}f$;
> 
> (3) 积分保持不等号: 若 $f\left(x,y\right)\le g\left(x,y\right)$ ($\forall\left(x,y\right)\in D$), 则 $\iint_D f\le\iint_D g$;
> 
> (4) 积分中值定理: 若 $f$ 在 $D$ 上连续, 则存在 $\left(x_0,y_0\right)\in D$ 使 $\iint_D f=f\left(x_0,y_0\right)\cdot S$, 其中 $S$ 为 $D$ 的面积.

### 习题一

（习题 8.1-2）设 $z=f\left(x,y\right)$ 及 $z=g\left(x,y\right)$ 在有界闭区域 $D$ 上可积. 证明 $z=f\left(x,y\right)\cdot g\left(x,y\right)$ 在 $D$ 上也可积. (提示: 考察 $f\cdot g$ 在一个小区域 $D_i$ 上的振幅 $\omega_{f\cdot g}^{\left(i\right)}$, 并证明 $\omega_{f\cdot g}^{\left(i\right)}\le A\omega_f^{\left(i\right)}+B\omega_g^{\left(i\right)}$.)

### 解答 习题一

因 $f,g$ 均可积, 由**定理 1.1**（可积的必要条件）, $f,g$ 在 $D$ 上有界. 记 $A=\sup_D\left| f\left(x,y\right)\right|$, $B=\sup_D\left| g\left(x,y\right)\right|$.

任取 $D$ 的一个分割 $T$, 对每个小区域 $D_i$ 及任意 $P,Q\in D_i$, 有

$$
\left| f\left(P\right)g\left(P\right)-f\left(Q\right)g\left(Q\right)\right|=\left| f\left(P\right)\left(g\left(P\right)-g\left(Q\right)\right)+g\left(Q\right)\left(f\left(P\right)-f\left(Q\right)\right)\right|\le A\left| g\left(P\right)-g\left(Q\right)\right|+B\left| f\left(P\right)-f\left(Q\right)\right|.
$$

令 $P,Q$ 分别取遍 $D_i$ 使 $f\left(P\right)g\left(P\right)$ 与 $f\left(Q\right)g\left(Q\right)$ 接近上下确界, 得

$$
\omega_{fg}^{\left(i\right)}\le A\omega_g^{\left(i\right)}+B\omega_f^{\left(i\right)}.
$$

对 $i$ 求和得

$$
\sum_i\omega_{fg}^{\left(i\right)}\Delta\sigma_i\le A\sum_i\omega_g^{\left(i\right)}\Delta\sigma_i+B\sum_i\omega_f^{\left(i\right)}\Delta\sigma_i.
$$

因 $f,g$ 可积, 由**定理 1.4**, 右端两项在 $\lambda\left(T\right)\to0$ 时均趋于 $0$, 故左端亦趋于 $0$. 再由**定理 1.4**, $f\cdot g$ 在 $D$ 上可积. $\blacksquare$

### 习题二

（习题 8.1-3）设有函数

$$
D\left(x,y\right)=
\begin{cases}
1,&\text{当 }x,y\text{ 均为有理数},\\
0,&\text{其他点 }\left(x,y\right).
\end{cases}
$$

证明 $D\left(x,y\right)$ 在

$$
R=\left\{\left(x,y\right):0\le x\le1,0\le y\le1\right\}
$$

中不可积.

### 解答 习题二

对 $R$ 作任意分割 $T$, 将 $R$ 分成若干可求面积的小区域 $D_1,\dots,D_n$. 由于每个小区域 $D_i$ 是有内点的区域, 其中既含有理点 (两个坐标均为有理数) 又含无理点. 故 $f$ 在 $D_i$ 上的上确界 $M_i=1$, 下确界 $m_i=0$, 从而振幅 $\omega_i=M_i-m_i=1$. 于是达布大和与达布小和之差为

$$
D\left(T\right)-d\left(T\right)=\sum_i\omega_i\Delta\sigma_i=\sum_i\Delta\sigma_i=1,
$$

不随 $\lambda\left(T\right)\to0$ 而趋于 $0$. 由**定理 1.4**, $D\left(x,y\right)$ 在 $R$ 上不可积. $\blacksquare$

### 习题三

（习题 8.1-4）设 $z=f\left(x,y\right)$ 与 $z=g\left(x,y\right)$ 均在区域 $D$ 上可积, 其中 $D$ 是有界闭区域, $D$ 的边界由逐段光滑曲线组成. 又设 $\gamma$ 是 $D$ 内部的一条直线段, 并且 $f\left(x,y\right)=g\left(x,y\right)$, $\left(x,y\right)\in D\setminus\gamma$. 证明

$$
\iint_D f\left(x,y\right)\,\mathrm{d}\sigma=\iint_D g\left(x,y\right)\,\mathrm{d}\sigma.
$$

该题结论告诉我们, 在积分区域的一条直线段上修改函数值, 其二重积分的值不变.

### 解答 习题三

直线段 $\gamma$ 是逐段光滑曲线, 由**命题 1.3**, $\gamma$ 是零面积集合. 因而 $\gamma$ 自身的面积为 $0$, 即

$$
\iint_\gamma f=\iint_\gamma g=0.
$$

将 $D$ 分解为 $D\setminus\gamma$ 与 $\gamma$ 两个互不重叠的区域. 由**性质**（二重积分的基本性质）(2) (可加性),

$$
\iint_D f=\iint_{D\setminus\gamma}f+\iint_\gamma f=\iint_{D\setminus\gamma}f,
$$

同理 $\iint_D g=\iint_{D\setminus\gamma}g$. 因 $f=g$ 在 $D\setminus\gamma$ 上, 故 $\iint_{D\setminus\gamma}f=\iint_{D\setminus\gamma}g$. 因此

$$
\iint_D f\left(x,y\right)\,\mathrm{d}\sigma=\iint_D g\left(x,y\right)\,\mathrm{d}\sigma.

$$

$\blacksquare$
### 习题四

（习题 8.1-5）设 $z=f\left(x,y\right)$ 在有界闭区域 $D$ 上可积. 证明 $z=\left| f\left(x,y\right)\right|$ 在 $D$ 上也可积.

### 解答 习题四

任取 $D$ 的一个分割 $T$, 对每个小区域 $D_i$ 及任意 $P,Q\in D_i$, 由三角不等式

$$
\left|\right| f\left(P\right)\left|-\right| f\left(Q\right)\left|\right|\le\left| f\left(P\right)-f\left(Q\right)\right|.
$$

令 $P,Q$ 取遍 $D_i$, 得 $\omega_{\left| f\right|}^{\left(i\right)}\le\omega_f^{\left(i\right)}$. 于是

$$
\sum_i\omega_{\left| f\right|}^{\left(i\right)}\Delta\sigma_i\le\sum_i\omega_f^{\left(i\right)}\Delta\sigma_i.
$$

因 $f$ 可积, 由**定理 1.4**, 右端在 $\lambda\left(T\right)\to0$ 时趋于 $0$, 故左端亦趋于 $0$. 再由**定理 1.4**, $\left| f\left(x,y\right)\right|$ 在 $D$ 上可积. $\blacksquare$

### 习题五

（习题 8.1-8）设函数 $f\left(x,y\right)$ 在可求面积的有界闭区域 $D$ 上连续, $g\left(x,y\right)$ 在 $D$ 上大于零, 且 $g\left(x,y\right)$ 在 $D$ 上连续. 证明: 在 $D$ 中存在点 $\left(x_0,y_0\right)$, 使

$$
\iint_D f\left(x,y\right)g\left(x,y\right)\,\mathrm{d}\sigma=f\left(x_0,y_0\right)\iint_D g\left(x,y\right)\,\mathrm{d}\sigma.
$$

### 解答 习题五

因 $f$ 在有界闭区域 $D$ 上连续, 由**定理 1.5**（连续函数可积）, $f$ 在 $D$ 上可积, 且 $f$ 在 $D$ 上有最大值 $M$ 与最小值 $m$. 又因 $g\left(x,y\right)> 0$ 于 $D$ 上, 故

$$
m\,g\left(x,y\right)\le f\left(x,y\right)g\left(x,y\right)\le M\,g\left(x,y\right).
$$

由**性质**（二重积分的基本性质）(3) (比较性质),

$$
m\iint_D g\le\iint_D fg\le M\iint_D g.
$$

又 $g$ 连续且 $g> 0$, $D$ 有正面积, 故 $\iint_D g> 0$. 于是

$$
m\le\frac{\iint_D fg}{\iint_D g}\le M.
$$

由二元连续函数的介值定理 (第一章连续函数性质), 存在 $\left(x_0,y_0\right)\in D$ 使 $f\left(x_0,y_0\right)=\frac{\iint_D fg}{\iint_D g}$, 即

$$
\iint_D f\left(x,y\right)g\left(x,y\right)\,\mathrm{d}\sigma=f\left(x_0,y_0\right)\iint_D g\left(x,y\right)\,\mathrm{d}\sigma.

$$

$\blacksquare$
### 习题六

（习题 8.1-9）设函数 $f\left(x,y\right)$ 在可求面积的有界闭区域 $D$ 上连续, 非负, 且 $\iint_D f\left(x,y\right)\,\mathrm{d}x\mathrm{d}y=0$. 证明当 $\left(x,y\right)\in D$ 时, $f\left(x,y\right)=0$.

### 解答 习题六

反设存在 $\left(x_0,y_0\right)\in D$ 使 $f\left(x_0,y_0\right)> 0$. 由 $f$ 在 $\left(x_0,y_0\right)$ 处连续, 对 $\varepsilon=\frac{f\left(x_0,y_0\right)}2> 0$, 存在 $\delta> 0$, 使当 $\left(x,y\right)\in D$ 且

$$
\sqrt{\left(x-x_0\right)^2+\left(y-y_0\right)^2}< \delta
$$

时,

$$
\left| f\left(x,y\right)-f\left(x_0,y_0\right)\right|< \frac{f\left(x_0,y_0\right)}2,
$$

即 $f\left(x,y\right)> \frac{f\left(x_0,y_0\right)}2$. 记

$$
R_\delta=D\cap\left\{\left(x,y\right):\sqrt{\left(x-x_0\right)^2+\left(y-y_0\right)^2}< \delta\right\}.
$$

因 $\left(x_0,y_0\right)$ 是 $D$ 的内点或边界点, $R_\delta$ 是可求面积的区域且面积 $\left|R_\delta\right|> 0$. 由**性质**（二重积分的基本性质）(3),

$$
\iint_D f\left(x,y\right)\,\mathrm{d}\sigma\ge\iint_{R_\delta}f\left(x,y\right)\,\mathrm{d}\sigma\ge\frac{f\left(x_0,y_0\right)}2\cdot\left|R_\delta\right|> 0,
$$

与 $\iint_D f=0$ 矛盾. 故 $f\left(x,y\right)\equiv0$ 于 $D$ 上. $\blacksquare$
