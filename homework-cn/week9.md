# week9

> **命题 1.7 (三角不等式)**
> 
> 对于任意实数 $a,b,c$, $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **定理 7.2 (复合函数连续性)**
> 
> 若 $y=g\left(u\right)$ 在 $u_0$ 点连续, $u=f\left(x\right)$ 在 $x_0$ 点连续且 $f\left(x_0\right)=u_0$, 则复合函数 $y=g\left(f\left(x\right)\right)$ 在 $x_0$ 点连续.

> **定理 8.1 (中间值定理)**
> 
> 设 $y=f\left(x\right)$ 在闭区间 $\left[a,b\right]$ 上连续, 且 $f\left(a\right)$ 与 $f\left(b\right)$ 反号, 则存在一点 $c\in\left(a,b\right)$ 使得 $f\left(c\right)=0$. 更一般地, $f$ 可取到 $f\left(a\right)$ 与 $f\left(b\right)$ 之间的一切值.

> **定理 8.2 (有界性定理)**
> 
> 闭区间上的连续函数是有界的, 且达到最大值与最小值.

## 1.7-4

设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中连续. 又设 $x=g\left(t\right)$ 当 $t\to\infty$ 时有极限, 且极限落在 $\left(a,b\right)$ 之中. 试证明

$$
\lim_{t\to\infty}f\left(g\left(t\right)\right)=f\left(\lim_{t\to\infty}g\left(t\right)\right).
$$

### 解答 1.7-4

设 $\lim_{t\to\infty}g\left(t\right)=c\in\left(a,b\right)$. 由连续函数的定义, 任给 $\varepsilon>0$, 存在 $\delta>0$, 使得当 $\left|x-c\right|<\delta$ 时 $\left|f\left(x\right)-f\left(c\right)\right|<\varepsilon$. 又因 $g\left(t\right)\to{c}$, 存在 $T>0$, 当 $t>{}T$ 时 $\left|g\left(t\right)-c\right|<\delta$. 于是当 $t>{}T$ 时 $\left|f\left(g\left(t\right)\right)-f\left(c\right)\right|<\varepsilon$. 即 $\lim{f}\left(g\left(t\right)\right)=f\left(c\right)$. $\blacksquare$

## 1.7-5

设 $y=f\left(x\right)$ 及 $y=g\left(x\right)$ 在实数域 $\mathbb{R}$ 中有定义且连续. 假定 $f\left(x\right)=g\left(x\right)$ 对一切 $x\in\mathbb{Q}$ 成立, 试证明 $f\left(x\right)\equiv{g}\left(x\right)$ 对一切 $x\in\mathbb{R}$ 成立.

### 解答 1.7-5

任取 $x_0\in\mathbb{R}$. 由有理数的稠密性, 存在有理序列 $\left\{r_n\right\}$ 使 $r_n\to{x}_0$. 因 $f,g$ 连续,

$$
f\left(x_0\right)=\lim_{n\to\infty}f\left(r_n\right)=\lim_{n\to\infty}g\left(r_n\right)=g\left(x_0\right).
$$

故 $f\left(x_0\right)=g\left(x_0\right)$. 由 $x_0$ 的任意性, $f\equiv{g}$. $\blacksquare$

## 1.7-6

设 $t_1$ 与 $t_2$ 是任意两个实数. 请在不利用公式 $e^{t_1+t_2}=e^{t_1}\cdot{e}^{t_2}$ 的条件下, 证明下列极限等式:

$$
\lim_{x\to\infty}\left[\left(1+\frac{t_1}{x}\right)\left(1+\frac{t_2}{x}\right)\right]^x=e^{t_1+t_2}.
$$

### 解答 1.7-6

$$
\left[\left(1+\frac{t_1}{x}\right)\left(1+\frac{t_2}{x}\right)\right]^x=\left(1+\frac{t_1+t_2+t_1t_2/x}{x}\right)^x=\left[\left(1+\frac{t_1+t_2+o\left(1\right)}{x}\right)^{\frac{x}{t_1+t_2+o\left(1\right)}}\right]^{t_1+t_2+o\left(1\right)}.
$$

底数趋于 $e$, 指数趋于 $t_1+t_2$. 由指数函数连续性, 极限为 $e^{t_1+t_2}$. $\blacksquare$

## 1.8-2

设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 上连续. 又设 $x_1,x_2,x_3$ 为 $\left(a,b\right)$ 中三点, $x_1<{}x_2<{}x_3$. 令

$$
\eta=\frac13\left[f\left(x_1\right)+f\left(x_2\right)+f\left(x_3\right)\right].
$$

证明: 在 $\left[x_1,x_3\right]$ 中存在一点 $\xi$, 使得 $f\left(\xi\right)=\eta$.

### 解答 1.8-2

$f$ 在 $\left[x_1,x_3\right]$ 上连续, 由**定理 8.2 (有界性定理)**, 设最大值为 $M$, 最小值为 $m$. 则 $m\le{f}\left(x_i\right)\le{M}$, 故 $m\le\eta\le{M}$. 由**定理 8.1 (中间值定理)**, 存在 $\xi\in\left[x_1,x_3\right]$ 使 $f\left(\xi\right)=\eta$. $\blacksquare$

## 1.8-3

设 $y=f\left(x\right)$ 在 $\left[a,+\infty\right)$ 中连续, 并且 $\lim_{x\to+\infty}f\left(x\right)=l$, 且 $l>{}f\left(a\right)$. 证明: 对于任一数 $\eta$ 满足 $f\left(a\right)<\eta<{}l$, 一定存在一个点 $\xi\in\left(a,+\infty\right)$, 使得 $f\left(\xi\right)=\eta$.

### 解答 1.8-3

因 $\lim_{x\to+\infty}f\left(x\right)=l>\eta$, 存在 $A>{}a$ 使得当 $x>{}A$ 时 $f\left(x\right)>\eta$. 取 $b>{}A$, 则 $f\left(a\right)<\eta<{}f\left(b\right)$. 又 $f$ 在 $\left[a,b\right]$ 上连续, 由**定理 8.1 (中间值定理)**, 存在 $\xi\in\left(a,b\right)\subset\left(a,+\infty\right)$ 使 $f\left(\xi\right)=\eta$. $\blacksquare$

## 1.8-4

设 $y=f\left(x\right)$ 在 $\left[a,+\infty\right)$ 上连续, 且 $\lim_{x\to+\infty}f\left(x\right)$ 存在. 证明: $f$ 在 $\left[a,+\infty\right)$ 上为有界函数.

### 解答 1.8-4

设 $\lim_{x\to+\infty}f\left(x\right)=l$. 存在 $A>{}a$ 使得当 $x>{}A$ 时 $\left|f\left(x\right)-l\right|<1$, 即 $\left|f\left(x\right)\right|<\left|l\right|+1$. 在 $\left[a,A\right]$ 上由**定理 8.2 (有界性定理)**, $f$ 有界, 设 $\left|f\left(x\right)\right|\le{M}$. 取 $\widetilde{M}=\max\left\{M,\left|l\right|+1\right\}$, 则对一切 $x\in\left[a,+\infty\right)$, $\left|f\left(x\right)\right|\le\widetilde{M}$. $\blacksquare$

## 1.8-5

设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中连续. 又设 $x_1,x_2\in\left(a,b\right)$, $x_1<{}x_2$, $m_1>0$, $m_2>0$. 证明: 存在一点 $\xi\in\left(a,b\right)$, 使得

$$
f\left(\xi\right)=\frac{m_1f\left(x_1\right)+m_2f\left(x_2\right)}{m_1+m_2}.
$$

### 解答 1.8-5

设 $f$ 在 $\left[x_1,x_2\right]$ 上的最大值为 $M$, 最小值为 $m$. 则

$$
m=\frac{m_1m+m_2m}{m_1+m_2}\le\frac{m_1f\left(x_1\right)+m_2f\left(x_2\right)}{m_1+m_2}\le\frac{m_1M+m_2M}{m_1+m_2}=M.
$$

由**定理 8.1 (中间值定理)**, 存在 $\xi\in\left[x_1,x_2\right]\subset\left(a,b\right)$ 使 $f\left(\xi\right)=\frac{m_1f\left(x_1\right)+m_2f\left(x_2\right)}{m_1+m_2}$. $\blacksquare$
