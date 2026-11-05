# week25

> **定理 1.3 (拉格朗日中值定理)**
> 
> 设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 内可导. 则存在 $c\in\left(a,b\right)$, 使得 $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

> **命题 1.3 (可求面积的充要条件)**
> 
> $E$ 可求面积的充要条件是 $\partial{E}$ 为零面积集合. 特别地, 边界为逐段光滑曲线的有界区域可求面积.

> **定理 1.4 (可积的充要条件)**
> 
> $f$ 在可求面积区域 $D$ 上可积的充要条件是 $\lim_{\lambda\to0}\sum_i\omega_i\Delta\sigma_i=0$.

> **定理 1.5 (连续函数可积)**
> 
> 若 $D$ 是有界闭区域且边界为零面积集合, $f$ 在 $D$ 上连续, 则 $f$ 在 $D$ 上可积.

> **引理 2.1 (分点加密的效应)**
> 
> 设 $T'$ 是由分割 $T$ 增加有限个分点而形成的分割, 则达布小和不减, 达布大和不增.

> **定理 2.2 (可积的充要条件)**
> 
> 设 $f$ 在 $\left[a,b\right]$ 上有界. 则 $f$ 黎曼可积的充要条件是 $\lim_{\lambda\left(T\right)\to0}\left[D\left(T\right)-d\left(T\right)\right]=0$.

## 6.1-3

设 $x=\varphi\left(y\right)$ 在 $\left[c,d\right]$ 上连续且 $\varphi\left(y\right)>0$. 试用定积分表示所围面积; 又设 $c\ge0$, $\varphi$ 严格递增, 求 $\int_c^d\varphi\left(y\right)\,\mathrm{d}y+\int_a^b\psi\left(x\right)\,\mathrm{d}x$.

### 解答 6.1-3

(1) 面积为 $S=\int_c^d\varphi\left(y\right)\,\mathrm{d}y$.

(2) 两部分面积之和等于大矩形面积减去小矩形面积:

$$
\int_c^d\varphi\left(y\right)\,\mathrm{d}y+\int_a^b\psi\left(x\right)\,\mathrm{d}x=bd-ac.
$$

$\blacksquare$

## 6.1-5

证明: $f$ 在 $\left[a,b\right]$ 上可积的充要条件是 $\lim_{\lambda\to0}\sum{m}_i\Delta{x}_i$ 与 $\lim_{\lambda\to0}\sum{M}_i\Delta{x}_i$ 存在且相等.

### 解答 6.1-5

必要性: 设 $f$ 可积, 积分为 $I$. 对任意 $\varepsilon>0$, 由定积分的定义, 当 $\lambda\left(T\right)$ 充分小时, 任意黎曼和都接近 $I$. 取 $\xi_i^*$ 接近 $m_i$, 得 $\left|\sum{m}_i\Delta{x}_i-I\right|<2\varepsilon$. 同理 $\left|\sum{M}_i\Delta{x}_i-I\right|<2\varepsilon$.

充分性: 设两极限均为 $I$. 对任意中间点 $\xi_i$, $m_i\le{f}\left(\xi_i\right)\le{M}_i$. 由夹逼定理, $\sum{f}\left(\xi_i\right)\Delta{x}_i\to{I}$. 由定积分的定义, $f$ 可积. $\blacksquare$

## 6.1-6

证明下列不等式:

(1) $\frac\pi2\le\int_0^{\pi/2}\left(1+\sin{x}\right)\,\mathrm{d}x\le\pi$;

(2) $\sqrt2\le\int_0^1\sqrt{2+x-x^2}\,\mathrm{d}x\le\frac32$.

### 解答 6.1-6

(1) 在 $\left[0,\pi/2\right]$ 上, $1\le1+\sin{x}\le2$. 由定积分的比较性质, $\frac\pi2\le\int_0^{\pi/2}\left(1+\sin{x}\right)\,\mathrm{d}x\le\pi$.

(2) 在 $\left[0,1\right]$ 上, $2\le2+x-x^2\le\frac94$. 开方得 $\sqrt2\le\sqrt{2+x-x^2}\le\frac32$. 由定积分的比较性质, 得证. $\blacksquare$

## 6.1-8

设 $F$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 内可导, $F'\left(x\right)=f\left(x\right)$, 且 $f$ 可积. 证明 $\int_a^bf\left(x\right)\,\mathrm{d}x=F\left(b\right)-F\left(a\right)$.

### 解答 6.1-8

对 $\left[a,b\right]$ 任作分割 $T$. 则

$$
F\left(b\right)-F\left(a\right)=\sum_{k=1}^n\left[F\left(x_k\right)-F\left(x_{k-1}\right)\right].
$$

在每个小区间上, 由**定理 1.3 (拉格朗日中值定理)**, 存在 $\xi_k\in\left(x_{k-1},x_k\right)$ 使得

$$
F\left(x_k\right)-F\left(x_{k-1}\right)=f\left(\xi_k\right)\Delta{x}_k.
$$

于是 $F\left(b\right)-F\left(a\right)=\sum{f}\left(\xi_k\right)\Delta{x}_k$. 令 $\lambda\left(T\right)\to0$, 由定积分的定义, 得 $\int_a^bf\left(x\right)\,\mathrm{d}x=F\left(b\right)-F\left(a\right)$. $\blacksquare$

## 6.2-1

设 $f$ 在 $\left[a,b\right]$ 上可积, 又设 $\left[c,d\right]\subset\left[a,b\right]$. 证明: $f$ 在 $\left[c,d\right]$ 上也可积.

### 解答 6.2-1

任取 $\left[c,d\right]$ 的分割 $T'$. 将 $T'$ 扩充为 $\left[a,b\right]$ 的分割 $T$. 由**引理 2.1 (分点加密的效应)**,

$$
D\left(T'\right)-d\left(T'\right)\le{D}\left(T\right)-d\left(T\right).
$$

因 $f$ 在 $\left[a,b\right]$ 上可积, 由**定理 2.2 (可积的充要条件)**, 右端趋于 $0$. 故 $D\left(T'\right)-d\left(T'\right)\to0$. 再由**定理 2.2 (可积的充要条件)**, $f$ 在 $\left[c,d\right]$ 上可积. $\blacksquare$

## 6.2-2

设 $f$ 与 $g$ 均在 $\left[a,b\right]$ 中可积. 证明: $f\cdot{g}$ 在 $\left[a,b\right]$ 中可积.

### 解答 6.2-2

因 $f,g$ 均可积, 故均有界. 记 $M=\sup\left|f\right|$, $N=\sup\left|g\right|$. 对每个小区间 $I_k$,

$$
\omega_{fg}\left(I_k\right)\le{M}\omega_g\left(I_k\right)+N\omega_f\left(I_k\right).
$$

求和得 $\sum\omega_{fg}\Delta{x}_k\le{M}\sum\omega_g\Delta{x}_k+N\sum\omega_f\Delta{x}_k$. 由**定理 2.2 (可积的充要条件)**, 右端趋于 $0$, 故左端亦趋于 $0$. 故 $f\cdot{g}$ 可积. $\blacksquare$

## 6.2-4

设 $f$ 在 $\left[a,b\right]$ 上连续且 $f\left(x\right)\ge0$. 证明: 当且仅当 $f\equiv0$ 时, $\int_a^bf\left(x\right)\,\mathrm{d}x=0$.

### 解答 6.2-4

充分性: 若 $f\equiv0$, 显然成立.

必要性: 反设存在 $x_0$ 使 $f\left(x_0\right)>0$. 由连续性, 在 $x_0$ 的某邻域 $J$ 内 $f\left(x\right)>\frac{f\left(x_0\right)}2$. 由定积分的比较性质,

$$
\int_a^bf\left(x\right)\,\mathrm{d}x\ge\int_Jf\left(x\right)\,\mathrm{d}x\ge\frac{f\left(x_0\right)}2\cdot\left|J\right|>0,
$$

矛盾. 故 $f\equiv0$. $\blacksquare$

## 6.2-6

证明: 若 $f$ 在 $\left[a,b\right]$ 上可积, 则 $\left|f\right|$ 可积, 且 $\left|\int_a^bf\left(x\right)\,\mathrm{d}x\right|\le\int_a^b\left|f\left(x\right)\right|\,\mathrm{d}x$.

### 解答 6.2-6

可积性: 对每个小区间 $I_k$, 由三角不等式, $\omega_{\left|f\right|}\left(I_k\right)\le\omega_f\left(I_k\right)$. 故 $\sum\omega_{\left|f\right|}\Delta{x}_k\le\sum\omega_f\Delta{x}_k$. 由**定理 2.2 (可积的充要条件)**, $\left|f\right|$ 可积.

不等式: 由 $-\left|f\right|\le{f}\le\left|f\right|$, 及定积分的比较性质,

$$
-\int_a^b\left|f\right|\,\mathrm{d}x\le\int_a^bf\,\mathrm{d}x\le\int_a^b\left|f\right|\,\mathrm{d}x,
$$

即 $\left|\int_a^bf\right|\le\int_a^b\left|f\right|$. $\blacksquare$

## 8.1-2

设 $f$ 与 $g$ 在有界闭区域 $D$ 上可积. 证明 $f\cdot{g}$ 在 $D$ 上也可积.

### 解答 8.1-2

因 $f,g$ 均可积, 故均有界. 记 $A=\sup_D\left|f\right|$, $B=\sup_D\left|g\right|$. 对每个小区域 $D_i$,

$$
\omega_{fg}^{\left(i\right)}\le{A}\omega_g^{\left(i\right)}+B\omega_f^{\left(i\right)}.
$$

求和得 $\sum\omega_{fg}\Delta\sigma_i\le{A}\sum\omega_g\Delta\sigma_i+B\sum\omega_f\Delta\sigma_i$. 由**定理 1.4 (可积的充要条件)**, 右端趋于 $0$, 故左端亦趋于 $0$. 故 $f\cdot{g}$ 可积. $\blacksquare$
