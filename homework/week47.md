# 作业 47

> **定义**（瑕积分的收敛）设 $f\left(x\right)$ 在 $\left(a,b\right]$ 上有定义, 且在任意闭区间 $\left[a+\eta,b\right]\subset\left(a,b\right]\left(\eta>0\right)$ 上可积, 而 $a$ 为 $f\left(x\right)$ 的瑕点. 若极限 $\lim_{\eta\to0+0}\int_{a+\eta}^b f\left(x\right)\,\mathrm{d}x$ 存在, 则称瑕积分 $\int_a^b f\left(x\right)\,\mathrm{d}x$ 收敛, 并把该极限定义为其值; 否则称其发散. 瑕点为右端点或区间内点时, 定义完全类似.

> **例 2.2**（瑕 $p$-积分）瑕积分 $\displaystyle\int_a^b\frac{\mathrm{d}x}{\left(x-a\right)^p}$($p>0$)当 $p<1$ 时收敛, 当 $p\ge1$ 时发散.

> **定义**（绝对收敛与条件收敛）设 $f\left(x\right)$ 在 $\left(a,b\right]$ 上有定义, $a$ 为瑕点. 若 $\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x$ 收敛, 则称 $\int_a^b f\left(x\right)\,\mathrm{d}x$ 绝对收敛; 若 $\int_a^b f\left(x\right)\,\mathrm{d}x$ 收敛而 $\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x$ 发散, 则称其条件收敛.

> **定义**（柯西主值）设 $f\left(x\right)$ 在 $\left[a,b\right]\setminus\left\{c\right\}$ 上有定义, $c\in\left(a,b\right)$ 为其瑕点. 假若极限
> $$
> \displaystyle I=\lim_{\eta\to0+0}\left[\int_a^{c-\eta}f\left(x\right)\,\mathrm{d}x+\int_{c+\eta}^b f\left(x\right)\,\mathrm{d}x\right]
> $$
> 存在, 则称瑕积分 $\int_a^b f\left(x\right)\,\mathrm{d}x$ 在柯西主值意义下收敛, 极限值 $I$ 称为其柯西主值, 记作 $\mathrm{\left(CPV\right)}\int_a^b f\left(x\right)\,\mathrm{d}x$.

### 习题一

（习题 12.2-1-1）判断瑕积分 $\displaystyle\int_0^1\ln x\,\mathrm{d}x$ 的收敛性. 如果收敛, 请求其值.

### 解答 习题一

$x=0$ 是瑕点. 对任意 $\eta\in\left(0,1\right)$, 分部积分得

$$
\int_\eta^1\ln x\,\mathrm{d}x=\left[x\ln x-x\right]_\eta^1=-1-\eta\ln\eta+\eta.
$$

当 $\eta\to0+0$ 时 $\eta\ln\eta\to0$, $\eta\to0$, 上式右端趋于 $-1$. 由**定义**（瑕积分的收敛）, 该瑕积分收敛, 其值为 $-1$. $\blacksquare$

### 习题二

（习题 12.2-1-3）判断瑕积分 $\displaystyle\int_{-1}^1\frac{\mathrm{d}x}{\sqrt{1-x^2}}$ 的收敛性. 如果收敛, 请求其值.

### 解答 习题二

$x=\pm1$ 均为瑕点. 将积分拆为 $\int_{-1}^0+\int_0^1$ 分别讨论. 对任意 $\eta\in\left(0,1\right)$, 

$$
\int_0^{1-\eta}\frac{\mathrm{d}x}{\sqrt{1-x^2}}=\left[\arcsin x\right]_0^{1-\eta}=\arcsin\left(1-\eta\right)\to\frac{\pi}{2}\left(\eta\to0+0\right),
$$

$$
\int_{-1+\eta}^0\frac{\mathrm{d}x}{\sqrt{1-x^2}}=\left[\arcsin x\right]_{-1+\eta}^0=-\arcsin\left(-1+\eta\right)\to\frac{\pi}{2}\left(\eta\to0+0\right).
$$

两个瑕积分均收敛, 故由**定义**（瑕积分的收敛）, 原瑕积分收敛, 其值为 $\frac{\pi}{2}+\frac{\pi}{2}=\pi$. $\blacksquare$

### 习题三

（习题 12.2-1-5）判断瑕积分 $\displaystyle\int_0^1\frac{\mathrm{d}x}{x\ln^2 x}$ 的收敛性. 如果收敛, 请求其值.

### 解答 习题三

$x=0$ 与 $x=1$ 均为瑕点. 只看 $x=1$ 附近即可. 对任意 $\eta\in\left(0,\frac12\right)$, 作代换 $u=\ln x$($\mathrm{d}u=\frac{\mathrm{d}x}{x}$), 有

$$
\int_{1/2}^{1-\eta}\frac{\mathrm{d}x}{x\ln^2 x}=\int_{\ln\left(1/2\right)}^{\ln\left(1-\eta\right)}\frac{\mathrm{d}u}{u^2}
=\left[-\frac1u\right]_{\ln\left(1/2\right)}^{\ln\left(1-\eta\right)}
=-\frac1{\ln\left(1-\eta\right)}+\frac1{\ln\left(1/2\right)}.
$$

当 $\eta\to0+0$ 时 $\ln\left(1-\eta\right)\to0-0$, 故 $-\frac1{\ln\left(1-\eta\right)}\to+\infty$. 由**定义**（瑕积分的收敛）, 该瑕积分发散. $\blacksquare$

### 习题四

（习题 12.2-2-1）讨论广义积分 $\displaystyle\int_0^{+\infty}\frac{\mathrm{d}x}{\sqrt x\,\left(1+x\right)}$ 的收敛性.

### 解答 习题四

$x=0$ 是瑕点, 积分区间又是无穷区间, 分两段讨论.

在 $x=0$ 附近, $\frac1{\sqrt x\,\left(1+x\right)}\sim\frac1{\sqrt x}$, 而由**例 2.2**（瑕 $p$-积分）, $\int_0^1\frac{\mathrm{d}x}{\sqrt x}$ 收敛($p=\frac12<1$). 在 $x\to+\infty$ 时, $\frac1{\sqrt x\,\left(1+x\right)}\sim\frac1{x^{3/2}}$, 而由第 12 章**例 1.2**（$p$-积分）, $\int_1^{+\infty}\frac{\mathrm{d}x}{x^{3/2}}$ 收敛($p=\frac32>1$). 两段均收敛, 故原广义积分收敛.

事实上其值为: 作代换 $t=\sqrt x$($\mathrm{d}x=2t\,\mathrm{d}t$), 

$$
\int_0^{+\infty}\frac{\mathrm{d}x}{\sqrt x\,\left(1+x\right)}=\int_0^{+\infty}\frac{2t\,\mathrm{d}t}{t\left(1+t^2\right)}=2\int_0^{+\infty}\frac{\mathrm{d}t}{1+t^2}=2\cdot\frac{\pi}{2}=\pi.

$$

$\blacksquare$
### 习题五

（习题 12.2-2-3）讨论广义积分 $\displaystyle\int_0^{+\infty}\frac{\mathrm{d}x}{x^p+x^q}$ 的收敛性.

### 解答 习题五

$x=0$ 是瑕点, 积分区间又是无穷区间, 分两段讨论.

在 $x=0$ 附近, $x^p+x^q\sim x^{\min\left(p,q\right)}$, 故被积函数与 $\frac1{x^{\min\left(p,q\right)}}$ 同阶. 由**例 2.2**（瑕 $p$-积分）, 该端收敛当且仅当 $\min\left(p,q\right)<1$.

在 $x\to+\infty$ 时, $x^p+x^q\sim x^{\max\left(p,q\right)}$, 故被积函数与 $\frac1{x^{\max\left(p,q\right)}}$ 同阶. 由第 12 章**例 1.2**（$p$-积分）, 该端收敛当且仅当 $\max\left(p,q\right)>1$.

两段须同时收敛, 故原广义积分收敛当且仅当

$$
\min\left(p,q\right)<1<\max\left(p,q\right)\ \left(\text{即}p,q\text{中一个小于}1\text{, 另一个大于}1\right),
$$

其余情形均发散. $\blacksquare$

### 习题六

（习题 12.2-2-5）讨论广义积分 $\displaystyle\int_0^{\pi/2}\frac{\mathrm{d}x}{\sin^2 x\cos^2 x}$ 的收敛性.

### 解答 习题六

$x=0$ 与 $x=\frac{\pi}{2}$ 均为瑕点. 在 $x=0$ 附近, $\sin x\sim x$, $\cos x\sim1$, 故被积函数与 $\frac1{x^2}$ 同阶. 由**例 2.2**（瑕 $p$-积分）, $\int_0^{\pi/4}\frac{\mathrm{d}x}{x^2}$ 发散($p=2>1$). 故原广义积分发散. $\blacksquare$

### 习题七

（习题 12.2-2-7）讨论广义积分 $\displaystyle\int_0^1 x^p\left(1-x\right)^q\,\mathrm{d}x$($p>0,q>0$)的收敛性.

### 解答 习题七

$x=0$ 与 $x=1$ 均可能为瑕点. 在 $x=0$ 附近, $x^p\left(1-x\right)^q\sim x^p$, 由**例 2.2**（瑕 $p$-积分）, 该端收敛当且仅当 $p>-1$; 题设 $p>0$, 故恒收敛. 在 $x=1$ 附近, $x^p\left(1-x\right)^q\sim\left(1-x\right)^q$, 该端收敛当且仅当 $q>-1$; 题设 $q>0$, 故亦恒收敛. 两段同时收敛, 故对一切 $p>0,q>0$, 原广义积分均收敛. $\blacksquare$

### 习题八

（习题 12.2-3）设 $f\left(x\right)$ 在 $\left(a,b\right]$ 上有定义, 且在任意区间 $\left[a+\eta,b\right]\left(\eta>0\right)$ 上可积. 证明: 若 $\displaystyle\int_a^b f^2\left(x\right)\,\mathrm{d}x$ 收敛, 则 $\displaystyle\int_a^b f\left(x\right)\,\mathrm{d}x$ 绝对收敛. 又问: 若 $\displaystyle\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x$ 收敛, 是否必然有 $\displaystyle\int_a^b f^2\left(x\right)\,\mathrm{d}x$ 收敛?

### 解答 习题八

由不等式 $2\left| t\right|\le1+t^2$(即 $\left(\left| t\right|-1\right)^2\ge0$), 得

$$
\left| f\left(x\right)\right|\le\frac12+\frac{f^2\left(x\right)}2.
$$

对任意 $\eta>0$, 在 $\left[a+\eta,b\right]$ 上积分得

$$
\int_{a+\eta}^b\left| f\left(x\right)\right|\,\mathrm{d}x\le\frac{b-a}{2}+\frac12\int_{a+\eta}^b f^2\left(x\right)\,\mathrm{d}x\le\frac{b-a}{2}+\frac12\int_a^b f^2\left(x\right)\,\mathrm{d}x<+\infty.
$$

右端与 $\eta$ 无关且有界, 故 $\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x$ 收敛. 由**定义**（绝对收敛与条件收敛）, $\int_a^b f\left(x\right)\,\mathrm{d}x$ 绝对收敛.

反之不然. 反例: 取 $f\left(x\right)=\frac1{\sqrt x}$ 在 $\left(0,1\right]$ 上. 由**例 2.2**（瑕 $p$-积分）, $\int_0^1\frac{\mathrm{d}x}{\sqrt x}$ 收敛($p=\frac12<1$), 即 $\int_0^1\left| f\left(x\right)\right|\,\mathrm{d}x$ 收敛; 但 $\int_0^1 f^2\left(x\right)\,\mathrm{d}x=\int_0^1\frac{\mathrm{d}x}{x}$ 发散($p=1$). 故 $\int\left| f\right|$ 收敛不能保证 $\int f^2$ 收敛. $\blacksquare$

### 习题九

（习题 12.2-4-1）判断广义积分 $\displaystyle\int_0^2\frac{\mathrm{d}x}{x-1}$ 是否在柯西主值意义下收敛. 若收敛, 试求其柯西主值.

### 解答 习题九

$x=1$ 是瑕点. 先按普通意义看:

$$
\int_0^{1-\eta}\frac{\mathrm{d}x}{x-1}=\left[\ln\left| x-1\right|\right]_0^{1-\eta}=\ln\eta-\ln1=\ln\eta\to-\infty\left(\eta\to0+0\right),
$$

故普通意义下发散.

再看柯西主值. 由**定义**（柯西主值）, 

$$
\begin{aligned}
\mathrm{\left(CPV\right)}\int_0^2\frac{\mathrm{d}x}{x-1}
&=\lim_{\eta\to0+0}\left(\int_0^{1-\eta}\frac{\mathrm{d}x}{x-1}+\int_{1+\eta}^2\frac{\mathrm{d}x}{x-1}\right)\\
&=\lim_{\eta\to0+0}\left(\left(\ln\eta-\ln1\right)+\left(\ln1-\ln\eta\right)\right)=0.
\end{aligned}
$$

故该积分在柯西主值意义下收敛, 其柯西主值为 $0$. $\blacksquare$

### 习题十

（习题 12.2-4-2）判断广义积分 $\displaystyle\int_{1/2}^2\frac{\mathrm{d}x}{x\ln x}$ 是否在柯西主值意义下收敛. 若收敛, 试求其柯西主值.

### 解答 习题十

$x=1$ 是瑕点. 被积函数的原函数为 $\ln\left|\ln x\right|$. 由**定义**（柯西主值）, 

$$
\begin{aligned}
\mathrm{\left(CPV\right)}\int_{1/2}^2\frac{\mathrm{d}x}{x\ln x}
&=\lim_{\eta\to0+0}\left(\int_{1/2}^{1-\eta}\frac{\mathrm{d}x}{x\ln x}+\int_{1+\eta}^2\frac{\mathrm{d}x}{x\ln x}\right)\\
&=\lim_{\eta\to0+0}\left[\ln\left|\ln\left(1-\eta\right)\right|-\ln\left|\ln\frac12\right|+\ln\left|\ln2\right|-\ln\left|\ln\left(1+\eta\right)\right|\right]\\
&=\lim_{\eta\to0+0}\ln\frac{-\ln\left(1-\eta\right)}{\ln\left(1+\eta\right)}.
\end{aligned}
$$

当 $\eta\to0+0$ 时 $-\ln\left(1-\eta\right)\sim\eta$, $\ln\left(1+\eta\right)\sim\eta$, 故比值趋于 $1$, 对数趋于 $\ln1=0$. 因此该积分在柯西主值意义下收敛, 其柯西主值为 $0$. $\blacksquare$
