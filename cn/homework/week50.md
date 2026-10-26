# 作业 50

> **定理 4.3**（魏尔斯特拉斯判别法）设 $f\left(x,y\right)$ 在 $\left(a,b\right]\times Y$ 上有定义, $a$ 为瑕点. 若存在 $F\left(x\right)$, 使得 (i)
> $$
> \left| f\left(x,y\right)\right|\le F\left(x\right)\left(\forall x\in\left(a,b\right],y\in Y\right);
> $$
> (ii) 瑕积分 $\int_a^b F\left(x\right)\,\mathrm{d}x$ 收敛, 则含参变量瑕积分 $\int_a^b f\left(x,y\right)\,\mathrm{d}x$ 关于 $y\in Y$ 一致收敛.

> **定理 4.7**（积分次序交换定理）设 $f\left(x,y\right)$ 在 $\left(a,b\right]\times\left[c,d\right]$ 上连续且保持固定符号, $\int_a^b f\left(x,y\right)\,\mathrm{d}x$ 关于 $y\in\left[c,d\right]$ 一致收敛, 则
> $$
> \displaystyle\int_c^d\mathrm{d}y\int_a^b f\left(x,y\right)\,\mathrm{d}x=\int_a^b\mathrm{d}x\int_c^d f\left(x,y\right)\,\mathrm{d}y.
> $$

### 习题一

（习题 12.5-1-1）讨论含参变量瑕积分 $\displaystyle\int_0^1\frac{\sin x}{x^\alpha}\,\mathrm{d}x$ 在 (i) $\alpha\le\alpha_0< 2$; (ii) $\alpha< 2$ 上的一致收敛性.

### 解答 习题一

瑕点为 $x=0$. 因 $\sin x\sim x\left(x\to0\right)$, 被积函数在瑕点附近与 $x^{1-\alpha}$ 同阶.

(i)当 $\alpha\le\alpha_0< 2$ 时, 对 $x\in\left(0,1\right]$ 有

$$
\left|\frac{\sin x}{x^\alpha}\right|\le\frac{x}{x^\alpha}=x^{1-\alpha}\le x^{1-\alpha_0}\ \left(\text{因}x\in\left(0,1\right)\text{时}x^\top\text{关于}t\text{递减}\right).
$$

而 $1-\alpha_0> -1$, 故 $\int_0^1 x^{1-\alpha_0}\,\mathrm{d}x$ 收敛. 由**定理 4.3**（魏尔斯特拉斯判别法）, 该瑕积分在 $\alpha\le\alpha_0< 2$ 上一致收敛.

(ii)当 $\alpha< 2$(即在开区间 $\left(0,2\right)$ 上)时, 不一致收敛. 事实上, 取 $\alpha_n=2-\frac1n\to2-0$, 则

$$
\int_0^{1/n}\frac{\sin x}{x^{\alpha_n}}\,\mathrm{d}x\sim\int_0^{1/n}x^{1-\alpha_n}\,\mathrm{d}x=\int_0^{1/n}x^{-1+1/n}\,\mathrm{d}x=n\cdot\left(\frac1n\right)^{1/n}\to n\cdot\frac1n=1,
$$

不随 $n\to\infty$ 而趋于 $0$, 故不满足一致收敛的柯西条件. 即在 $\alpha< 2$ 上不一致收敛. $\blacksquare$

### 习题二

（习题 12.5-1-2）讨论含参变量瑕积分 $\displaystyle\int_0^1 x^{p-1}\,\mathrm{d}x$ 在 (i) $p\ge p_0> 0$; (ii) $p> 0$ 上的一致收敛性.

### 解答 习题二

瑕点为 $x=0$.

(i)当 $p\ge p_0> 0$ 时, 对 $x\in\left(0,1\right]$ 有 $x^{p-1}\le x^{p_0-1}$(因 $x\in\left(0,1\right)$ 时 $x^\top$ 关于 $t$ 递减). 而 $p_0> 0$, 故 $\int_0^1 x^{p_0-1}\,\mathrm{d}x=\frac1{p_0}$ 收敛. 由**定理 4.3**（魏尔斯特拉斯判别法）, 该瑕积分在 $p\ge p_0> 0$ 上一致收敛.

(ii)当 $p> 0$(即在开区间 $\left(0,+\infty\right)$ 上)时, 不一致收敛. 事实上, 取 $p_n=\frac1n\to0+0$, 则

$$
\int_0^{1/n}x^{p_n-1}\,\mathrm{d}x=\frac{1}{p_n}\cdot\left(\frac1n\right)^{p_n}=n\cdot\left(\frac1n\right)^{1/n}\to1,
$$

不随 $n\to\infty$ 而趋于 $0$, 故不满足一致收敛的柯西条件. 即在 $p> 0$ 上不一致收敛. $\blacksquare$

### 习题三

（习题 12.5-2-1）求积分 $\displaystyle\int_0^1\frac{x^b-x^a}{\ln x}\,\mathrm{d}x$ 的值($a> -1,b> -1$).

### 解答 习题三

注意到 $\frac{x^b-x^a}{\ln x}=\displaystyle\int_a^b x^y\,\mathrm{d}y$

$$
\left(\text{因 }\int_a^b x^y\,\mathrm{d}y=\left[\frac{x^y}{\ln x}\right]_a^b=\frac{x^b-x^a}{\ln x}\right),
$$

故

$$
I=\int_0^1\mathrm{d}x\int_a^b x^y\,\mathrm{d}y.
$$

被积函数 $x^y\ge0$ 在 $\left(0,1\right]\times\left[a,b\right]$ 上连续, 且 $\int_0^1 x^y\,\mathrm{d}x$ 关于 $y\in\left[a,b\right]$ 一致收敛(因 $x^y\le x^{\min\left(a,b\right)}$, 而 $\min\left(a,b\right)> -1$, $\int_0^1 x^{\min\left(a,b\right)}\,\mathrm{d}x$ 收敛). 由**定理 4.7**（积分次序交换定理）, 

$$
I=\int_a^b\mathrm{d}y\int_0^1 x^y\,\mathrm{d}x=\int_a^b\frac{\mathrm{d}y}{y+1}=\ln\frac{1+b}{1+a}.

$$

$\blacksquare$