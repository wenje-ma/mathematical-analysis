# 作业 27

> **引理 2.1**（分点加密的效应）设 $T'$ 是由分割 $T$ 增加有限个分点而形成的分割, 则 $d\left(T\right)\le d\left(T'\right)$, $D\left(T'\right)\le D\left(T\right)$, 即分点增加时达布小和不减, 达布大和不增.

> **定理 2.2**（可积的充要条件）设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上有界. 则 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上黎曼可积的充要条件是
> $$
> \lim_{\lambda\left(T\right)\to0}\left[D\left(T\right)-d\left(T\right)\right]=0,
> $$
> 其中 $D\left(T\right)$, $d\left(T\right)$ 分别为达布大和与达布小和.

### 习题一

（习题 6.2-1）设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上可积, 又设 $\left[c,d\right]\subset\left[a,b\right]$. 证明: $y=f\left(x\right)$ 在 $\left[c,d\right]$ 上也可积. (提示: 利用定理 2.2.)

### 解答 习题一

因 $f$ 在 $\left[a,b\right]$ 上可积, 由第一章**定理 1.1**（可积的必要条件）, $f$ 在 $\left[a,b\right]$ 上有界, 记 $M=\sup_{\left[a,b\right]}\left| f\left(x\right)\right|$.

任取 $\left[c,d\right]$ 的一个分割 $T'$. 将 $T'$ 扩充为 $\left[a,b\right]$ 的一个分割 $T$: 在 $\left[a,c\right]$ 与 $\left[d,b\right]$ 上各作若干小区间, 使其长度均不超过 $\lambda\left(T'\right)$. 则 $\lambda\left(T\right)=\lambda\left(T'\right)$.

分割 $T$ 对应的

$$
D\left(T\right)-d\left(T\right)=\sum\omega_k\Delta x_k,
$$

其中 $\omega_k$ 为 $f$ 在第 $k$ 个小区间上的振幅. 在属于 $\left[c,d\right]$ 的那些小区间上, $T$ 与 $T'$ 的分点完全相同, 对应的振幅项之和恰为 $D\left(T'\right)-d\left(T'\right)$; 在 $\left[a,c\right]$ 与 $\left[d,b\right]$ 上的小区间所贡献的振幅项非负. 由**引理 2.1**（分点加密的效应）, 分点增加时达布小和不减, 达布大和不增, 故

$$
D\left(T'\right)-d\left(T'\right)\le D\left(T\right)-d\left(T\right).
$$

因 $f$ 在 $\left[a,b\right]$ 上可积, 由**定理 2.2**, 令 $\lambda\left(T\right)=\lambda\left(T'\right)\to0$, 右端趋于 $0$, 故 $D\left(T'\right)-d\left(T'\right)\to0$. 再由**定理 2.2**, $f$ 在 $\left[c,d\right]$ 上可积. $\blacksquare$

### 习题二

（习题 6.2-2）设 $y=f\left(x\right)$ 与 $y=g\left(x\right)$ 均在 $\left[a,b\right]$ 中可积. 证明: $f\left(x\right)\cdot g\left(x\right)$ 在 $\left[a,b\right]$ 中可积. (提示: 利用定理 2.2 及不等式

$$
\omega_{fg}\left(I\right)\le M\omega_g\left(I\right)+N\omega_f\left(I\right),
$$

$\forall I\subset\left[a,b\right]$.)

### 解答 习题二

因 $f,g$ 均可积, 故均有界. 记 $M=\sup_{\left[a,b\right]}\left| f\left(x\right)\right|$, $N=\sup_{\left[a,b\right]}\left| g\left(x\right)\right|$.

任取 $\left[a,b\right]$ 的一个分割 $T$, 对每个小区间 $I_k=\left[x_{k-1},x_k\right]$ 及任意 $u,v\in I_k$, 有

$$
\left| f\left(u\right)g\left(u\right)-f\left(v\right)g\left(v\right)\right|=\left| f\left(u\right)\left(g\left(u\right)-g\left(v\right)\right)+g\left(v\right)\left(f\left(u\right)-f\left(v\right)\right)\right|\le M\left| g\left(u\right)-g\left(v\right)\right|+N\left| f\left(u\right)-f\left(v\right)\right|.
$$

令 $u,v$ 分别取遍 $I_k$ 使 $f\left(u\right)g\left(u\right)$ 与 $f\left(v\right)g\left(v\right)$ 接近上下确界, 得

$$
\omega_{fg}\left(I_k\right)\le M\omega_g\left(I_k\right)+N\omega_f\left(I_k\right).
$$

对 $k$ 求和得

$$
\sum_k\omega_{fg}\left(I_k\right)\Delta x_k\le M\sum_k\omega_g\left(I_k\right)\Delta x_k+N\sum_k\omega_f\left(I_k\right)\Delta x_k.
$$

因 $f,g$ 在 $\left[a,b\right]$ 上可积, 由**定理 2.2**, 右端两项在 $\lambda\left(T\right)\to0$ 时均趋于 $0$, 故左端亦趋于 $0$. 再由**定理 2.2**, $f\cdot g$ 在 $\left[a,b\right]$ 上可积. $\blacksquare$

### 习题三

（习题 6.2-4）设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 且 $f\left(x\right)\ge0$. 证明: 当且仅当 $f\left(x\right)\equiv0$ 时, $\int_a^b f\left(x\right)\,\mathrm{d}x=0$.

### 解答 习题三

**充分性** 若 $f\left(x\right)\equiv0$, 则 $\int_a^b f\left(x\right)\,\mathrm{d}x=0$ 显然成立.

**必要性** 反设 $f$ 不恒为零, 则存在 $x_0\in\left[a,b\right]$ 使 $f\left(x_0\right)> 0$. 由 $f$ 在 $x_0$ 处连续, 对 $\varepsilon=\frac{f\left(x_0\right)}{2}> 0$, 存在 $\delta> 0$, 使当 $x\in\left[a,b\right]$ 且 $\left| x-x_0\right|< \delta$ 时,

$$
\left| f\left(x\right)-f\left(x_0\right)\right|< \frac{f\left(x_0\right)}2,
$$

即 $f\left(x\right)> \frac{f\left(x_0\right)}2$. 记

$$
J=\left[a,b\right]\cap\left(x_0-\delta,x_0+\delta\right),
$$

其长度 $\left|J\right|> 0$. 由第一章**性质**（定积分的比较性质）,

$$
\int_a^b f\left(x\right)\,\mathrm{d}x\ge\int_J f\left(x\right)\,\mathrm{d}x\ge\frac{f\left(x_0\right)}2\cdot\left|J\right|> 0,
$$

与 $\int_a^b f\left(x\right)\,\mathrm{d}x=0$ 矛盾. 故 $f\left(x\right)\equiv0$. $\blacksquare$

### 习题四

（习题 6.2-6）证明: 若 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上可积, 则 $y=\left| f\left(x\right)\right|$ 可积, 且有

$$
\left|\int_a^b f\left(x\right)\,\mathrm{d}x\right|\le\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x.
$$

### 解答 习题四

**可积性** 任取 $\left[a,b\right]$ 的分割 $T$, 对每个小区间 $I_k$ 及任意 $u,v\in I_k$, 由三角不等式

$$
\left|\right| f\left(u\right)\left|-\right| f\left(v\right)\left|\right|\le\left| f\left(u\right)-f\left(v\right)\right|.
$$

令 $u,v$ 取遍 $I_k$, 得 $\omega_{\left| f\right|}\left(I_k\right)\le\omega_f\left(I_k\right)$. 于是

$$
\sum_k\omega_{\left| f\right|}\left(I_k\right)\Delta x_k\le\sum_k\omega_f\left(I_k\right)\Delta x_k.
$$

因 $f$ 可积, 由**定理 2.2**, 右端在 $\lambda\left(T\right)\to0$ 时趋于 $0$, 故左端亦趋于 $0$. 再由**定理 2.2**, $\left| f\left(x\right)\right|$ 在 $\left[a,b\right]$ 上可积.

**不等式** 对一切 $x\in\left[a,b\right]$, 有 $-\left| f\left(x\right)\right|\le f\left(x\right)\le\left| f\left(x\right)\right|$. 由第一章**性质**（定积分的比较性质）,

$$
-\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x\le\int_a^b f\left(x\right)\,\mathrm{d}x\le\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x,
$$

即

$$
\left|\int_a^b f\left(x\right)\,\mathrm{d}x\right|\le\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x.
$$

$\blacksquare$
