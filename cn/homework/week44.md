# 作业 44

> **定理 3.2**（收敛半径的柯西公式）设幂级数 $\sum_{n=0}^{\infty}a_nx^n$, 则其收敛半径 $R$ 满足
> $$
> \frac{1}{R}=\limsup_{n\to\infty}\sqrt\left[n\right]{\left|a_n\right|}.
> $$
> 
> **定理 3.3**（收敛半径的达朗贝尔公式）设 $a_n\ne 0$ 且 $\lim_{n\to\infty}\left|\frac{a_n}{a_{n+1}}\right|=R$, 则该幂级数的收敛半径为 $R$.
> 
> **定理 3.4**（内闭一致收敛性）幂级数在其收敛区间内部的任意闭区间上一致收敛, 因而可在收敛区间内逐项求导与逐项积分, 且收敛半径不变.

### 习题一

（习题 11.3-1-1）求幂级数 $\sum_{n=0}^{+\infty}\frac{3^n}{n!}x^n$ 的收敛半径.

### 解答 习题一

令 $a_n=\frac{3^n}{n!}$, 则

$$
\left|\frac{a_n}{a_{n+1}}\right|=\frac{3^n/n!}{3^{n+1}/\left(n+1\right)!}=\frac{n+1}{3}\to+\infty.
$$

由**定理 3.3**（达朗贝尔公式）, 收敛半径 $R=+\infty$. $\blacksquare$

### 习题二

（习题 11.3-1-2）求幂级数 $\sum_{n=0}^{+\infty}\frac{n}{2^n}x^n$ 的收敛半径.

### 解答 习题二

令 $a_n=\frac{n}{2^n}$, 则

$$
\left|\frac{a_n}{a_{n+1}}\right|=\frac{n/2^n}{\left(n+1\right)/2^{n+1}}=\frac{2n}{n+1}\to 2.
$$

由**定理 3.3**（达朗贝尔公式）, 收敛半径 $R=2$. $\blacksquare$

### 习题三

（习题 11.3-1-3）求幂级数 $\sum_{n=0}^{+\infty}\frac{n!}{\left(2n\right)!}x^n$ 的收敛半径.

### 解答 习题三

令 $a_n=\frac{n!}{\left(2n\right)!}$, 则

$$
\left|\frac{a_n}{a_{n+1}}\right|=\frac{n!/\left(2n\right)!}{\left(n+1\right)!/\left(2n+2\right)!}=\frac{\left(2n+2\right)\left(2n+1\right)}{n+1}=2\left(2n+1\right)\to+\infty.
$$

由**定理 3.3**（达朗贝尔公式）, 收敛半径 $R=+\infty$. $\blacksquare$

### 习题四

（习题 11.3-1-4）求幂级数 $\sum_{n=0}^{+\infty}\frac{\left(n!\right)^2}{\left(2n\right)!}x^n$ 的收敛半径.

### 解答 习题四

令 $a_n=\frac{\left(n!\right)^2}{\left(2n\right)!}$, 则

$$
\left|\frac{a_n}{a_{n+1}}\right|=\frac{\left(n!\right)^2/\left(2n\right)!}{\left(\left(n+1\right)!\right)^2/\left(2n+2\right)!}=\frac{\left(2n+2\right)\left(2n+1\right)}{\left(n+1\right)^2}=\frac{2\left(2n+1\right)}{n+1}\to 4.
$$

由**定理 3.3**（达朗贝尔公式）, 收敛半径 $R=4$. $\blacksquare$

### 习题五

（习题 11.3-2-2）求幂级数 $\sum_{n=1}^{+\infty}n^3\left(x-5\right)^n$ 的收敛点集合.

### 解答 习题五

令 $t=x-5$, 则级数为 $\sum n^3 t^n$. 由**定理 3.3**, $\left|\frac{n^3}{\left(n+1\right)^3}\right|\to 1$, 故收敛半径 $R=1$, 即 $\left|t\right|< 1$, 亦即 $4< x< 6$.

当 $t=1$($x=6$)时, 级数为 $\sum n^3$, 通项不趋于零, 发散; 当 $t=-1$($x=4$)时, 级数为 $\sum\left(-1\right)^n n^3$, 通项亦不趋于零, 发散. 故收敛点集合为 $\left(4,6\right)$. $\blacksquare$

### 习题六

（习题 11.3-2-4）求幂级数 $\sum_{n=1}^{+\infty}\frac{\left(-1\right)^n}{\sqrt n}x^n$ 的收敛点集合.

### 解答 习题六

由**定理 3.3**,

$$
\left|\frac{\left(-1\right)^n/\sqrt n}{\left(-1\right)^{n+1}/\sqrt{n+1}}\right|=\sqrt{\frac{n+1}{n}}\to 1,
$$

故收敛半径 $R=1$.

当 $x=1$ 时, 级数为 $\sum\frac{\left(-1\right)^n}{\sqrt n}$, 由第十章**定理 3.1**（莱布尼茨判别法）收敛; 当 $x=-1$ 时, 级数为 $\sum\frac{-1}{\sqrt n}$, 为 $p=\frac12< 1$ 的 $p$ 级数, 发散. 故收敛点集合为 $\left(-1,1\right]$. $\blacksquare$

### 习题七

（习题 11.3-2-6）求幂级数 $\sum_{n=2}^{+\infty}\frac{\left(-1\right)^n x^n}{4^n\ln n}$ 的收敛点集合.

### 解答 习题七

由**定理 3.3**,

$$
\left|\frac{a_n}{a_{n+1}}\right|=\frac{4^{n+1}\ln\left(n+1\right)}{4^n\ln n}=4\frac{\ln\left(n+1\right)}{\ln n}\to 4,
$$

故收敛半径 $R=4$.

当 $x=\pm 4$ 时, 两端点处通项均不满足收敛条件, 级数发散. 故收敛点集合为 $\left(-4,4\right)$. $\blacksquare$

### 习题八

（习题 11.3-2-8）求幂级数

$$
\sum_{n=1}^{+\infty}\left(1+\frac12+\cdots+\frac1n\right)x^n
$$

的收敛点集合.

### 解答 习题八

令

$$
a_n=1+\frac12+\cdots+\frac1n=h_n.
$$

由 $h_n-\ln n\to\gamma$ 知 $h_n\to+\infty$ 但 $\frac{h_{n+1}}{h_n}\to 1$. 由**定理 3.3**,

$$
\left|\frac{a_n}{a_{n+1}}\right|=\frac{h_n}{h_{n+1}}\to 1,
$$

故收敛半径 $R=1$.

当 $x=1$ 时, 级数为 $\sum h_n$, 通项 $h_n\to+\infty\ne 0$, 发散; 当 $x=-1$ 时, 级数为 $\sum\left(-1\right)^n h_n$, 通项亦不趋于零, 发散. 故收敛点集合为 $\left(-1,1\right)$. $\blacksquare$

### 习题九

（习题 11.3-2-10）求幂级数 $\sum_{n=2}^{+\infty}\frac{\left(-1\right)^n\left(2x+3\right)^n}{n\ln n}$ 的收敛点集合.

### 解答 习题九

令 $t=2x+3$. 由**定理 3.3**, $\left|\frac{a_n}{a_{n+1}}\right|=\frac{\left(n+1\right)\ln\left(n+1\right)}{n\ln n}\to 1$, 故收敛半径 $R=1$, 即 $\left|t\right|< 1$, 亦即 $-1< 2x+3< 1$, $-2< x< -1$.

当 $t=\pm 1$ 时, 两端点处级数均发散. 故收敛点集合为 $\left(-2,-1\right)$. $\blacksquare$

### 习题十

（习题 11.3-3-1）利用幂级数的逐项求导运算求 $\sum_{n=0}^{+\infty}\left(n+1\right)x^n$ 的和函数.

### 解答 习题十

已知 $\sum_{n=0}^{\infty}x^{n+1}=\frac{x}{1-x}$($\left|x\right|< 1$). 由**定理 3.4**（内闭一致收敛性）, 可在收敛区间内逐项求导: 

$$
\sum_{n=0}^{\infty}\left(n+1\right)x^n=\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{x}{1-x}\right)=\frac{1}{\left(1-x\right)^2}, \left|x\right|< 1.

$$

$\blacksquare$
### 习题十一

（习题 11.3-3-3）求 $\sum_{n=1}^{+\infty}n^2x^n$ 的和函数.

### 解答 习题十一

利用分解 $n^2=n\left(n-1\right)+n$, 有

$$
\sum_{n=1}^{\infty}n^2x^n=x\sum_{n=1}^{\infty}n\left(n-1\right)x^{n-1}+x\sum_{n=1}^{\infty}nx^{n-1}.
$$

由**定理 3.4** 逐项求导两次与一次, 得

$$
\sum_{n=1}^{\infty}n\left(n-1\right)x^{n-1}=\frac{\mathrm{d}^2}{\mathrm{d}x^2}\left(\frac{1}{1-x}\right)=\frac{2}{\left(1-x\right)^3},
$$

$$
\sum_{n=1}^{\infty}nx^{n-1}=\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{1}{1-x}\right)=\frac{1}{\left(1-x\right)^2}.
$$

故

$$
\sum_{n=1}^{\infty}n^2x^n=x\cdot\frac{2}{\left(1-x\right)^3}+x\cdot\frac{1}{\left(1-x\right)^2}=\frac{x\left(1+x\right)}{\left(1-x\right)^3}, \left|x\right|< 1.

$$

$\blacksquare$
### 习题十二

（习题 11.3-3-5）求 $\sum_{n=1}^{+\infty}\frac{x^n}{n\left(n+1\right)}$ 的和函数.

### 解答 习题十二

注意到 $\frac{1}{n\left(n+1\right)}=\frac1n-\frac{1}{n+1}$, 故

$$
\sum_{n=1}^{\infty}\frac{x^n}{n\left(n+1\right)}=\sum_{n=1}^{\infty}\frac{x^n}{n}-\sum_{n=1}^{\infty}\frac{x^n}{n+1}.
$$

已知 $\sum_{n=1}^{\infty}\frac{x^n}{n}=-\ln\left(1-x\right)$($\left|x\right|< 1$), 而

$$
\sum_{n=1}^{\infty}\frac{x^n}{n+1}=\frac1x\sum_{n=1}^{\infty}\frac{x^{n+1}}{n+1}=\frac1x\left(-\ln\left(1-x\right)-x\right).
$$

两式相减得

$$
\sum_{n=1}^{\infty}\frac{x^n}{n\left(n+1\right)}=-\ln\left(1-x\right)+\frac{\ln\left(1-x\right)}{x}+1=1-\frac{1-x}{x}\ln\left(1-x\right), 0< \left|x\right|< 1.
$$

当 $x=0$ 时和函数为 $0$(由连续性延拓). $\blacksquare$

### 习题十三

（习题 11.3-3-7）求 $\sum_{n=1}^{+\infty}\frac{x^n}{n}$ 的和函数.

### 解答 习题十三

由**定理 3.4**, 在收敛区间内逐项求导: 

$$
\frac{\mathrm{d}}{\mathrm{d}x}\left(\sum_{n=1}^{\infty}\frac{x^n}{n}\right)=\sum_{n=1}^{\infty}x^{n-1}=\frac{1}{1-x}.
$$

积分并注意 $x=0$ 时和为 $0$, 得

$$
\sum_{n=1}^{\infty}\frac{x^n}{n}=\int_0^x\frac{\mathrm{d}t}{1-t}=-\ln\left(1-x\right), \left|x\right|< 1.

$$

$\blacksquare$
### 习题十四

（习题 11.3-4）证明: 若 $\sum_{n=0}^{+\infty}a_nx^n$ 的收敛半径是 $R$($0< R< +\infty$), 则 $\sum_{n=0}^{+\infty}a_nx^{2n}$ 的收敛半径是 $\sqrt R$.

### 解答 习题十四

令 $y=x^2$. 则 $\sum a_nx^{2n}=\sum a_ny^n$. 后者当且仅当 $\left|y\right|< R$ 时收敛(由收敛半径定义), 即 $\left|x^2\right|< R$, 亦即 $\left|x\right|< \sqrt R$. 当 $\left|x\right|> \sqrt R$ 时 $\left|y\right|> R$, 级数发散. 由**定理 3.2**（柯西公式）, $\sum a_nx^{2n}$ 的收敛半径为 $\sqrt R$. $\blacksquare$

### 习题十五

（习题 11.3-5）设 $\sum_{n=0}^{+\infty}a_nx^n$ 的收敛半径是 $R$($0< R< +\infty$), 证明: 对给定的 $A> \frac{1}{R}$, 存在 $C> 0$, 使得 $\left|a_n\right|\le CA^n$, $\forall n=1,2,\cdots$.

### 解答 习题十五

由 $A> \frac1R$ 得 $\frac1A< R$. 取 $r$ 满足 $\frac1A< r< R$. 则幂级数在 $x=r$ 处收敛, 故通项 $a_nr^n\to 0$, 从而有界, 即存在 $M> 0$ 使 $\left|a_nr^n\right|\le M$, $\forall n$. 于是

$$
\left|a_n\right|\le M\cdot r^{-n}=M\left(\frac1r\right)^n.
$$

因 $\frac1r< A$, 令 $q=\frac{1/\left(rA\right)}{1}< 1$, 则 $\left(\frac1r\right)^n=A^n\left(\frac{1}{rA}\right)^n\le A^n$(当 $\frac{1}{rA}\le 1$ 时), 或更一般地取 $C=M\max\left(1,\frac{1}{rA}\right)$, 即得 $\left|a_n\right|\le CA^n$. $\blacksquare$
