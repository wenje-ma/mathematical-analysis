# 作业 49

> **定理 4.3**（魏尔斯特拉斯判别法）设 $f\left(x,y\right)$ 在 $\left[a,+\infty\right)\times Y$ 上有定义. 若存在 $F\left(x\right)$, 使得 (i)
> $$
> \left| f\left(x,y\right)\right|\le F\left(x\right)\left(\forall x\in\left[a,+\infty\right),y\in Y\right);
> $$
> (ii) $\int_a^{+\infty}F\left(x\right)\,\mathrm{d}x$ 收敛, 则无穷积分 $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ 关于 $y\in Y$ 一致收敛.

> **定理 4.4**（阿贝尔判别法）设 $f\left(x,y\right),g\left(x,y\right)$ 在 $\left[a,+\infty\right)\times Y$ 上有定义. 若 (i) $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ 关于 $y\in Y$ 一致收敛; (ii) $g\left(x,y\right)$ 关于 $x$ 单调, 且关于 $y\in Y$ 一致有界, 则 $\int_a^{+\infty}f\left(x,y\right)g\left(x,y\right)\,\mathrm{d}x$ 关于 $y\in Y$ 一致收敛.

> **定理 4.7**（积分次序交换定理）设 $f\left(x,y\right)$ 在 $\left[a,+\infty\right)\times\left[c,d\right]$ 上连续, 且 $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ 关于 $y\in\left[c,d\right]$ 一致收敛, 则
> $$
> \displaystyle\int_c^d\mathrm{d}y\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x=\int_a^{+\infty}\mathrm{d}x\int_c^d f\left(x,y\right)\,\mathrm{d}y.
> $$

> **定理 4.8**（积分号下求导）设 $f\left(x,y\right)$ 与 $f_y\left(x,y\right)$ 在 $\left[a,+\infty\right)\times\left[c,d\right]$ 上连续, 且 $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ 收敛, $\int_a^{+\infty}f_y\left(x,y\right)\,\mathrm{d}x$ 关于 $y\in\left[c,d\right]$ 一致收敛, 则 $I\left(y\right)=\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ 在 $\left[c,d\right]$ 上可导, 且 $I'\left(y\right)=\int_a^{+\infty}f_y\left(x,y\right)\,\mathrm{d}x$.

> **例 4.5**（狄利克雷积分）$\displaystyle\int_0^{+\infty}\frac{\sin x}{x}\,\mathrm{d}x=\frac{\pi}{2}$. 一般地,
> $$
> \displaystyle\int_0^{+\infty}\frac{\sin\left(kx\right)}{x}\,\mathrm{d}x=\frac{\pi}{2}\operatorname{sgn}\left(k\right).
> $$

### 习题一

（习题 12.4-1-1）讨论含参变量无穷积分 $\displaystyle\int_0^{+\infty}e^{-\alpha x^2}\,\mathrm{d}x$ 在 $\alpha\in\left[\alpha_0,+\infty\right)$($\alpha_0> 0$)上的一致收敛性.

### 解答 习题一

对任意 $x\ge0$ 及 $\alpha\ge\alpha_0$, 有 $e^{-\alpha x^2}\le e^{-\alpha_0 x^2}$. 而 $\int_0^{+\infty}e^{-\alpha_0 x^2}\,\mathrm{d}x=\frac12\sqrt{\frac{\pi}{\alpha_0}}$ 收敛. 由**定理 4.3**（魏尔斯特拉斯判别法）, 该无穷积分在 $\left[\alpha_0,+\infty\right)$ 上一致收敛. $\blacksquare$

### 习题二

（习题 12.4-1-3）讨论含参变量无穷积分 $\displaystyle\int_1^{+\infty}e^{-xy}\frac{\cos x}{x}\,\mathrm{d}x$ 在 $y\in\left[0,+\infty\right)$ 上的一致收敛性.

### 解答 习题二

将被积函数写成 $\frac{\cos x}{x}\cdot e^{-xy}$. 首先, $\int_1^{+\infty}\frac{\cos x}{x}\,\mathrm{d}x$ 收敛(由第 12 章**定理 1.6** 狄利克雷判别法), 且它不含参数 $y$, 故关于 $y\in\left[0,+\infty\right)$ 一致收敛. 其次, $e^{-xy}$ 关于 $x$ 单调递减, 且 $0< e^{-xy}\le1$ 关于 $y\in\left[0,+\infty\right)$ 一致有界. 由**定理 4.4**（阿贝尔判别法）, $\int_1^{+\infty}e^{-xy}\frac{\cos x}{x}\,\mathrm{d}x$ 在 $\left[0,+\infty\right)$ 上一致收敛. $\blacksquare$

### 习题三

（习题 12.4-1-5）讨论含参变量无穷积分 $\displaystyle\int_0^{+\infty}e^{-x^2y^2}\cos x\,\mathrm{d}x$ 在 $y\in\left[y_0,+\infty\right)$($y_0> 0$)上的一致收敛性.

### 解答 习题三

对任意 $x\ge0$ 及 $y\ge y_0$, 有

$$
\left| e^{-x^2y^2}\cos x\right|\le e^{-x^2y^2}\le e^{-x^2y_0^2}.
$$

而 $\int_0^{+\infty}e^{-x^2y_0^2}\,\mathrm{d}x=\frac{1}{2y_0}\sqrt\pi$ 收敛. 由**定理 4.3**（魏尔斯特拉斯判别法）, 该无穷积分在 $\left[y_0,+\infty\right)$ 上一致收敛. $\blacksquare$

### 习题四

（习题 12.4-2-1）求积分 $\displaystyle\int_0^{+\infty}\frac{e^{-ax}-e^{-bx}}{x}\,\mathrm{d}x$($0< a< b$)的值.

### 解答 习题四

注意到 $\frac{e^{-ax}-e^{-bx}}{x}=\int_a^b e^{-xy}\,\mathrm{d}y$, 故

$$
I=\int_0^{+\infty}\mathrm{d}x\int_a^b e^{-xy}\,\mathrm{d}y.
$$

被积函数 $e^{-xy}$ 在 $\left[0,+\infty\right)\times\left[a,b\right]$ 上连续且非负, 且 $\int_0^{+\infty}e^{-xy}\,\mathrm{d}x$ 关于 $y\in\left[a,b\right]$ 一致收敛(因 $e^{-xy}\le e^{-ax}$, 而 $\int_0^{+\infty}e^{-ax}\,\mathrm{d}x=1/a$ 收敛, 由**定理 4.3**). 由**定理 4.7**（积分次序交换定理）, 

$$
I=\int_a^b\mathrm{d}y\int_0^{+\infty}e^{-xy}\,\mathrm{d}x=\int_a^b\frac{\mathrm{d}y}{y}=\ln\frac ba.

$$

$\blacksquare$
### 习题五

（习题 12.4-2-2）求积分

$$
\displaystyle\int_0^{+\infty}\frac{\sin\left(\alpha x\right)\cos\left(\beta x\right)}{x}\,\mathrm{d}x\ \left(\alpha> 0,\beta> 0\right)
$$

的值.

### 解答 习题五

由三角恒等式

$$
\sin\left(\alpha x\right)\cos\left(\beta x\right)=\frac12\left[\sin\left(\left(\alpha+\beta\right)x\right)+\sin\left(\left(\alpha-\beta\right)x\right)\right],
$$

得

$$
I=\frac12\int_0^{+\infty}\frac{\sin\left(\left(\alpha+\beta\right)x\right)}{x}\,\mathrm{d}x+\frac12\int_0^{+\infty}\frac{\sin\left(\left(\alpha-\beta\right)x\right)}{x}\,\mathrm{d}x.
$$

由**例 4.5**（狄利克雷积分）,

$$
\int_0^{+\infty}\frac{\sin\left(kx\right)}{x}\,\mathrm{d}x=\frac{\pi}{2}\operatorname{sgn}\left(k\right).
$$

因 $\alpha+\beta> 0$, 第一项为 $\frac12\cdot\frac{\pi}{2}=\frac{\pi}{4}$. 第二项依 $\alpha-\beta$ 的符号而定:

$$
I=
\begin{cases}
\frac12\cdot\frac{\pi}{4}+\frac12\cdot\left(-\frac{\pi}{4}\right)=0,&\alpha< \beta,\\[4pt\right]
\frac{\pi}{4}+0=\frac{\pi}{4},&\alpha=\beta,\\[4pt\right]
\frac{\pi}{4}+\frac12\cdot\frac{\pi}{2}=\frac{\pi}{2},&\alpha> \beta.
\end{cases}

$$

$\blacksquare$
### 习题六

（习题 12.4-2-4）求积分 $\displaystyle\int_0^{+\infty}\frac{1-\cos\left(\alpha x\right)}{x}e^{-x}\,\mathrm{d}x$ 的值.

### 解答 习题六

令

$$
I\left(\alpha\right)=\int_0^{+\infty}\frac{1-\cos\left(\alpha x\right)}{x}e^{-x}\,\mathrm{d}x.
$$

被积函数对 $\alpha$ 的偏导数为 $e^{-x}\sin\left(\alpha x\right)$, 它在 $\left[0,+\infty\right)\times\left[0,+\infty\right)$ 上连续, 且 $\int_0^{+\infty}e^{-x}\sin\left(\alpha x\right)\,\mathrm{d}x$ 关于 $\alpha$ 一致收敛(因 $\left| e^{-x}\sin\left(\alpha x\right)\right|\le e^{-x}$, 而 $\int_0^{+\infty}e^{-x}\,\mathrm{d}x$ 收敛, 由**定理 4.3**). 由**定理 4.8**（积分号下求导）,

$$
I'\left(\alpha\right)=\int_0^{+\infty}e^{-x}\sin\left(\alpha x\right)\,\mathrm{d}x.
$$

由第 12 章习题 12.1-3(取参数为 $1$),

$$
\int_0^{+\infty}e^{-x}\sin\left(\alpha x\right)\,\mathrm{d}x=\frac{\alpha}{1+\alpha^2}.
$$

于是

$$
I\left(\alpha\right)=\int_0^\alpha\frac{t}{1+t^2}\,\mathrm{d}t=\frac12\ln\left(1+\alpha^2\right)+C.
$$

又 $I\left(0\right)=0$, 故 $C=0$, 从而

$$
I\left(\alpha\right)=\frac12\ln\left(1+\alpha^2\right).

$$

$\blacksquare$
### 习题七

（习题 12.4-5）试证明关于函数项级数的迪尼定理: 设 $u_n\left(x\right)$ 在 $\left[a,b\right]$ 上连续($n=1,2,\cdots$), 且 $u_n\left(x\right)\ge0\left(\forall x\in\left[a,b\right]\right)$. 又设 $S\left(x\right)=\displaystyle\sum_{n=1}^\infty u_n\left(x\right)$ 在每一点 $x\in\left[a,b\right]$ 收敛, 且 $S\left(x\right)$ 在 $\left[a,b\right]$ 上连续. 则 $\displaystyle\sum_{n=1}^\infty u_n\left(x\right)$ 在 $\left[a,b\right]$ 上一致收敛.

### 解答 习题七

令 $S_N\left(x\right)=\sum_{n=1}^N u_n\left(x\right)$,

$$
R_N\left(x\right)=S\left(x\right)-S_N\left(x\right)=\sum_{n=N+1}^\infty u_n\left(x\right).
$$

因 $u_n\ge0$, 故 $R_N\left(x\right)\ge0$, 且 $R_N\left(x\right)$ 关于 $N$ 单调递减; 又 $R_N\left(x\right)$ 是两个连续函数之差, 故在 $\left[a,b\right]$ 上连续. 由点态收敛, $R_N\left(x\right)\to0\left(N\to\infty\right)$ 对每个 $x$ 成立.

用反证法. 假设 $\sum u_n$ 在 $\left[a,b\right]$ 上不一致收敛, 则存在 $\varepsilon_0> 0$ 及一列 $N_k\to\infty$ 和 $x_k\in\left[a,b\right]$, 使 $R_{N_k}\left(x_k\right)\ge\varepsilon_0$. 由波尔查诺–魏尔斯特拉斯定理, $\left\{x_k\right\}$ 有子列收敛于某 $x_0\in\left[a,b\right]$, 不妨仍记 $x_k\to x_0$.

对任意固定的 $m$, 当 $N_k\ge m$ 时, 由 $R_N\left(x\right)$ 关于 $N$ 单调递减, 有 $R_{N_k}\left(x_k\right)\le R_m\left(x_k\right)$. 令 $k\to\infty$, 由 $R_m\left(x\right)$ 连续得

$$
\varepsilon_0\le\lim_{k\to\infty}R_{N_k}\left(x_k\right)\le\lim_{k\to\infty}R_m\left(x_k\right)=R_m\left(x_0\right).
$$

此式对一切 $m$ 成立. 但由点态收敛 $R_m\left(x_0\right)\to0\left(m\to\infty\right)$, 矛盾. 故 $\sum u_n\left(x\right)$ 在 $\left[a,b\right]$ 上一致收敛. $\blacksquare$
