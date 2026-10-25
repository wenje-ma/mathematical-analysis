# 作业 51

> **定义**（伽马函数）
> $$
> \displaystyle\Gamma\left(\alpha\right)=\int_0^{+\infty}t^{\alpha-1}e^{-t}\,\mathrm{d}t\left(\alpha> 0\right).
> $$
> 它满足递推公式 $\Gamma\left(\alpha+1\right)=\alpha\Gamma\left(\alpha\right)$, $\Gamma\left(1\right)=1$, $\Gamma\left(n+1\right)=n!$, 且 $\Gamma\!\left(\frac12\right)=\sqrt\pi$.

> **定义**（贝塔函数）
> $$
> \displaystyle \Beta\left(p,q\right)=\int_0^1 t^{p-1}\left(1-t\right)^{q-1}\,\mathrm{d}t\left(p,q> 0\right),
> $$
> 且有 $\Beta\left(p,q\right)=\frac{\Gamma\left(p\right)\Gamma\left(q\right)}{\Gamma\left(p+q\right)}$.

> **命题**（伽马与贝塔的积分形式）
> $$
\begin{aligned}
> \displaystyle\int_0^{+\infty}\frac{x^{a-1}}{\left(1+x\right)^{a+b}}\,\mathrm{d}x&=\Beta\left(a,b\right),\
> \displaystyle\int_0^{\pi/2}\sin^m x\cos^n x\,\mathrm{d}x&=\frac12 \Beta\!\left(\frac{m+1}{2},\frac{n+1}{2}\right).
\end{aligned}
> $$

### 习题一

（习题 12.6-1-1）利用伽马函数与贝塔函数计算积分 $\displaystyle\int_0^{+\infty}\frac{4\sqrt x}{\left(1+x\right)^2}\,\mathrm{d}x$.

### 解答 习题一

由**命题**（伽马与贝塔的积分形式）,

$$
\displaystyle\int_0^{+\infty}\frac{x^{a-1}}{\left(1+x\right)^{a+b}}\,\mathrm{d}x=\Beta\left(a,b\right).
$$

这里被积函数为 $\frac{x^{1/2}}{\left(1+x\right)^2}$, 即 $a-1=\frac12$, $a+b=2$, 故 $a=\frac32$, $b=\frac12$. 于是

$$
\int_0^{+\infty}\frac{\sqrt x}{\left(1+x\right)^2}\,\mathrm{d}x=\Beta\!\left(\frac32,\frac12\right)=\frac{\Gamma\left(\frac32\right)\Gamma\left(\frac12\right)}{\Gamma\left(2\right)}.
$$

由**定义**（伽马函数）, $\Gamma\left(\frac32\right)=\frac12\Gamma\left(\frac12\right)=\frac{\sqrt\pi}{2}$, $\Gamma\left(\frac12\right)=\sqrt\pi$, $\Gamma\left(2\right)=1$, 故

$$
\int_0^{+\infty}\frac{4\sqrt x}{\left(1+x\right)^2}\,\mathrm{d}x=4\cdot\frac{\frac{\sqrt\pi}{2}\cdot\sqrt\pi}{1}=4\cdot\frac{\pi}{2}=2\pi.

$$

$\blacksquare$
### 习题二

（习题 12.6-1-2）利用伽马函数与贝塔函数计算积分 $\displaystyle\int_0^{+\infty}x^{-1/2}e^{-\alpha x}\,\mathrm{d}x$($\alpha> 0$).

### 解答 习题二

作代换 $t=\alpha x$($\mathrm{d}x=\frac{\mathrm{d}t}{\alpha}$), 则

$$
\int_0^{+\infty}x^{-1/2}e^{-\alpha x}\,\mathrm{d}x=\int_0^{+\infty}\left(\frac t\alpha\right)^{-1/2}e^{-t}\frac{\mathrm{d}t}{\alpha}=\alpha^{-1/2}\int_0^{+\infty}t^{-1/2}e^{-t}\,\mathrm{d}t.
$$

由**定义**（伽马函数）, 右端积分即 $\Gamma\!\left(\frac12\right)=\sqrt\pi$, 故

$$
\int_0^{+\infty}x^{-1/2}e^{-\alpha x}\,\mathrm{d}x=\frac{\sqrt\pi}{\sqrt\alpha}=\sqrt{\frac{\pi}{\alpha}}.

$$

$\blacksquare$
### 习题三

（习题 12.6-1-3）利用伽马函数与贝塔函数计算积分 $\displaystyle\int_0^1 x^8\sqrt{1-x^3}\,\mathrm{d}x$.

### 解答 习题三

作代换 $t=x^3$($x=t^{1/3}$, $\mathrm{d}x=\frac13 t^{-2/3}\mathrm{d}t$), 则 $x^8=t^{8/3}$, $\sqrt{1-x^3}=\sqrt{1-t}$, 于是

$$
\int_0^1 x^8\sqrt{1-x^3}\,\mathrm{d}x=\frac13\int_0^1 t^{8/3}\left(1-t\right)^{1/2}t^{-2/3}\,\mathrm{d}t=\frac13\int_0^1 t^2\left(1-t\right)^{1/2}\,\mathrm{d}t=\frac13 \Beta\!\left(3,\frac32\right).
$$

由**定义**（贝塔函数）, $\Beta\left(3,\frac32\right)=\frac{\Gamma\left(3\right)\Gamma\left(\frac32\right)}{\Gamma\left(\frac92\right)}$. 计算得 $\Gamma\left(3\right)=2$, $\Gamma\left(\frac32\right)=\frac{\sqrt\pi}{2}$, $\Gamma\left(\frac92\right)=\frac{105}{16}\sqrt\pi$, 故

$$
\Beta\!\left(3,\frac32\right)=\frac{2\cdot\frac{\sqrt\pi}{2}}{\frac{105}{16}\sqrt\pi}=\frac{16}{105},
$$

从而原积分 $=\frac13\cdot\frac{16}{105}=\frac{16}{315}$. $\blacksquare$

### 习题四

（习题 12.6-1-4）利用伽马函数与贝塔函数计算积分 $\displaystyle\int_0^{\pi/2}\sin^6 x\cos^4 x\,\mathrm{d}x$.

### 解答 习题四

由**命题**（伽马与贝塔的积分形式）, 

$$
\int_0^{\pi/2}\sin^6 x\cos^4 x\,\mathrm{d}x=\frac12 \Beta\!\left(\frac72,\frac52\right)=\frac12\cdot\frac{\Gamma\left(\frac72\right)\Gamma\left(\frac52\right)}{\Gamma\left(6\right)}.
$$

由**定义**（伽马函数）, $\Gamma\left(\frac72\right)=\frac{15}{8}\sqrt\pi$, $\Gamma\left(\frac52\right)=\frac{3}{4}\sqrt\pi$, $\Gamma\left(6\right)=120$, 故

$$
\text{原积分}=\frac12\cdot\frac{\frac{15}{8}\sqrt\pi\cdot\frac34\sqrt\pi}{120}=\frac12\cdot\frac{45\pi}{3840}=\frac{3\pi}{512}.

$$

$\blacksquare$
### 习题五

（习题 12.6-1-9）利用伽马函数与贝塔函数计算积分 $\displaystyle\int_0^1\frac{\mathrm{d}x}{\sqrt{1-x^4}}$(提示: 令 $t=x^4$).

### 解答 习题五

作代换 $t=x^4$($x=t^{1/4}$, $\mathrm{d}x=\frac14 t^{-3/4}\mathrm{d}t$), 则

$$
\int_0^1\frac{\mathrm{d}x}{\sqrt{1-x^4}}=\frac14\int_0^1 t^{-3/4}\left(1-t\right)^{-1/2}\,\mathrm{d}t=\frac14 \Beta\!\left(\frac14,\frac12\right).
$$

由**定义**（贝塔函数）, $\Beta\left(\frac14,\frac12\right)=\frac{\Gamma\left(\frac14\right)\Gamma\left(\frac12\right)}{\Gamma\left(\frac34\right)}$, 故原积分 $=\frac14 \Beta\!\left(\frac14,\frac12\right)$. $\blacksquare$

### 习题六

（习题 12.6-1-10）利用伽马函数与贝塔函数计算积分 $\displaystyle\int_0^{+\infty}\frac{\mathrm{d}x}{1+x^3}$(提示: 令 $t=\frac{1}{1+x^3}$).

### 解答 习题六

在**命题**（伽马与贝塔的积分形式）的公式

$$
\int_0^{+\infty}\frac{x^{a-1}}{\left(1+x\right)^{a+b}}\,\mathrm{d}x=\Beta\left(a,b\right)
$$

中, 将分母换为 $1+x^3$. 作代换 $u=x^3$($x=u^{1/3}$, $\mathrm{d}x=\frac13 u^{-2/3}\mathrm{d}u$), 则

$$
\int_0^{+\infty}\frac{\mathrm{d}x}{1+x^3}=\frac13\int_0^{+\infty}\frac{u^{-2/3}}{1+u}\,\mathrm{d}u=\frac13 \Beta\!\left(\frac13,\frac23\right).
$$

由**定义**（贝塔函数）,

$$
\Beta\left(\frac13,\frac23\right)=\Gamma\left(\frac13\right)\Gamma\left(\frac23\right),
$$

故原积分 $=\frac13\Gamma\!\left(\frac23\right)\Gamma\!\left(\frac13\right)$. $\blacksquare$

### 习题七

（习题 12.6-2）证明 $\Gamma\left(\alpha\right)$ 作为含参变量广义积分在 $\left(0,+\infty\right)$ 上不一致收敛.

### 解答 习题七

$\Gamma\left(\alpha\right)=\displaystyle\int_0^{+\infty}t^{\alpha-1}e^{-t}\,\mathrm{d}t$ 拆为

$$
\displaystyle\int_0^1 t^{\alpha-1}e^{-t}\,\mathrm{d}t+\int_1^{+\infty}t^{\alpha-1}e^{-t}\,\mathrm{d}t.
$$

第二个积分在任意 $\left[\alpha_0,+\infty\right)$ 上一致收敛, 但不影响 $\left(0,+\infty\right)$ 上的一致性.

关键在第一个积分 $\displaystyle\int_0^1 t^{\alpha-1}e^{-t}\,\mathrm{d}t$. 取 $\alpha_n=\frac1n\to0+0$, 则

$$
\int_0^{1/n}t^{\alpha_n-1}e^{-t}\,\mathrm{d}t\ge e^{-1/n}\int_0^{1/n}t^{-1+1/n}\,\mathrm{d}t=e^{-1/n}\cdot n\cdot\left(\frac1n\right)^{1/n}\to1\left(n\to\infty\right).
$$

该下界不趋于 $0$, 故不满足一致收敛的柯西条件. 因此 $\Gamma\left(\alpha\right)$ 在 $\left(0,+\infty\right)$ 上不一致收敛. $\blacksquare$
