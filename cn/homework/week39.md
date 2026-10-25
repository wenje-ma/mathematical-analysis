# 作业 39

> **定理 2.2**（比较判别法）设 $\sum a_n$ 与 $\sum b_n$ 为正项级数, 且存在自然数 $N_0$ 使 $a_n\le b_n$($n\ge N_0$). 若 $\sum b_n$ 收敛, 则 $\sum a_n$ 收敛; 若 $\sum a_n$ 发散, 则 $\sum b_n$ 发散.
> 
> **定理 2.3**（比较判别法的极限形式）设 $\sum a_n$ 与 $\sum b_n$ 为正项级数, $b_n\ne 0$, 且 $\lim_{n\to\infty}\frac{a_n}{b_n}=l$. 当 $0< l< +\infty$ 时, 两级数同时收敛或同时发散; 当 $l=0$ 且 $\sum b_n$ 收敛时, $\sum a_n$ 收敛; 当 $l=+\infty$ 且 $\sum b_n$ 发散时, $\sum a_n$ 发散.
> 
> **定理 2.6**（达朗贝尔判别法）设 $\sum a_n$ 为正项级数, $a_n> 0$. 若 $\lim_{n\to\infty}\frac{a_{n+1}}{a_n}=r$, 则当 $r< 1$ 时级数收敛, 当 $r> 1$ 时级数发散.
> 
> **定理 2.9**（积分判别法）设 $f\left(x\right)$ 在 $\left[1,+\infty\right)$ 上正, 单调递减, 则级数 $\sum_{n=1}^{\infty}f\left(n\right)$ 与反常积分 $\int_1^{+\infty}f\left(x\right)\,\mathrm{d}x$ 同时收敛或同时发散.

### 习题一

（习题 10.2-1-15）讨论级数 $\sum_{n=1}^{\infty}\frac{\left(n!\right)^2}{\left(2n\right)!}$ 的收敛性.

### 解答 习题一

令 $a_n=\frac{\left(n!\right)^2}{\left(2n\right)!}$, 则

$$
\frac{a_{n+1}}{a_n}=\frac{\left(\left(n+1\right)!\right)^2}{\left(2n+2\right)!}\cdot\frac{\left(2n\right)!}{\left(n!\right)^2}
=\frac{\left(n+1\right)^2}{\left(2n+2\right)\left(2n+1\right)}=\frac{n+1}{2\left(2n+1\right)}\to\frac14< 1.
$$

由**定理 2.6**（达朗贝尔判别法）, 该级数收敛. $\blacksquare$

### 习题二

（习题 10.2-1-18）讨论级数 $\sum_{n=3}^{\infty}\frac{1}{n\left(\ln\ln n\right)^q}$($q> 0$)的收敛性.

### 解答 习题二

由提示, 注意到 $\frac{\ln n}{\left(\ln\ln n\right)^q}\to+\infty$(任意次幂的对数增长慢于 $\ln n$), 故存在 $N$, 当 $n\ge N$ 时 $\left(\ln\ln n\right)^q< \ln n$, 于是

$$
\frac{1}{n\left(\ln\ln n\right)^q}> \frac{1}{n\ln n}.
$$

而级数 $\sum_{n=3}^{\infty}\frac{1}{n\ln n}$ 由**定理 2.9**（积分判别法）发散, 因为

$$
\int_3^{+\infty}\frac{\mathrm{d}x}{x\ln x}=\ln\ln x\Big|_3^{+\infty}=+\infty.
$$

再由**定理 2.2**（比较判别法）, 大者发散故小者亦发散. 因此对任意 $q> 0$, 该级数发散. $\blacksquare$

### 习题三

（习题 10.2-2）用积分判别法讨论级数 $\sum_{n=3}^{\infty}\frac{1}{n\ln^p n\left(\ln\ln n\right)^q}$($p> 0,q> 0$)的收敛性.

### 解答 习题三

令 $f\left(x\right)=\frac{1}{x\ln^p x\left(\ln\ln x\right)^q}$, 当 $x$ 充分大时正且单调递减. 作代换 $t=\ln x$, 则 $\mathrm{d}t=\mathrm{d}x/x$, 由**定理 2.9**（积分判别法）, 原级数与积分

$$
\int_{\ln 3}^{+\infty}\frac{\mathrm{d}t}{t^p\left(\ln t\right)^q}
$$

同时收敛或发散. 分四种情况讨论.

(i)当 $p> 1$ 时, 取 $p'$ 满足 $1< p'< p$. 因 $\frac{t^{p'}}{t^p\left(\ln t\right)^q}=\frac{1}{t^{p-p'}\left(\ln t\right)^q}\to 0$, 故 $t$ 充分大时 $\frac{1}{t^p\left(\ln t\right)^q}\le\frac{1}{t^{p'}}$, 而 $\int^{+\infty}\frac{\mathrm{d}t}{t^{p'}}$ 收敛, 故原积分收敛, 原级数收敛.

(ii)当 $p< 1$ 时, 因

$$
\frac{t}{t^p\left(\ln t\right)^q}=t^{1-p}/\left(\ln t\right)^q\to+\infty,
$$

故 $t$ 充分大时 $\frac{1}{t^p\left(\ln t\right)^q}\ge\frac{1}{t}$, 而 $\int^{+\infty}\frac{\mathrm{d}t}{t}$ 发散, 故原级数发散.

(iii)当 $p=1$ 且 $q> 1$ 时, 作代换 $u=\ln t$, 则 $\mathrm{d}u=\mathrm{d}t/t$, 原积分化为 $\int^{+\infty}\frac{\mathrm{d}u}{u^q}$, 当 $q> 1$ 时收敛, 故原级数收敛.

(iv)当 $p=1$ 且 $q\le 1$ 时, 同理原积分化为 $\int^{+\infty}\frac{\mathrm{d}u}{u^q}$, 当 $q\le 1$ 时发散, 故原级数发散. $\blacksquare$

### 习题四

（习题 10.2-6）设

$$
\lim_{n\to\infty}na_n=l,0< l< +\infty.
$$

证明: $\sum_{n=1}^{\infty}a_n^2$ 收敛, 而 $\sum_{n=1}^{\infty}a_n$ 发散.

### 解答 习题四

由 $\lim_{n\to\infty}na_n=l$ 得 $\lim_{n\to\infty}a_n=\frac{l}{n}$, 即

$$
\lim_{n\to\infty}\frac{a_n}{1/n}=l\in\left(0,+\infty\right).
$$

由**定理 2.3**（比较判别法的极限形式）, $\sum a_n$ 与 $\sum\frac1n$ 同发散, 故 $\sum a_n$ 发散.

又

$$
\lim_{n\to\infty}\frac{a_n^2}{1/n^2}=\lim_{n\to\infty}\left(na_n\right)^2=l^2\in\left(0,+\infty\right),
$$

而 $\sum\frac{1}{n^2}$ 为 $p=2> 1$ 的 $p$ 级数, 收敛. 再由**定理 2.3**, $\sum a_n^2$ 收敛. $\blacksquare$

### 习题五

（习题 10.2-7）若级数 $\sum_{n=1}^{\infty}a_n^2$ 与 $\sum_{n=1}^{\infty}b_n^2$ 都收敛, 证明下列级数均收敛: 
$$
\sum_{n=1}^{\infty}\left|a_nb_n\right|;\;\sum_{n=1}^{\infty}\left(a_n+b_n\right)^2;\;\sum_{n=1}^{\infty}\frac{\left|a_n\right|}{n}.
$$

### 解答 习题五

(1)由不等式 $2\left|a_nb_n\right|\le a_n^2+b_n^2$, 得

$$
\left|a_nb_n\right|\le\frac{a_n^2+b_n^2}{2}.
$$

由假设 $\sum a_n^2$ 与 $\sum b_n^2$ 均收敛, 故 $\sum\frac{a_n^2+b_n^2}{2}$ 收敛. 由**定理 2.2**（比较判别法）, $\sum\left|a_nb_n\right|$ 收敛.

(2)展开

$$
\left(a_n+b_n\right)^2=a_n^2+2a_nb_n+b_n^2,
$$

于是

$$
\left(a_n+b_n\right)^2\le a_n^2+2\left|a_nb_n\right|+b_n^2.
$$

右端三项分别由假设与(1)知对应的级数均收敛, 故 $\sum\left(a_n+b_n\right)^2$ 由**定理 2.2** 知收敛.

(3)由不等式 $2\frac{\left|a_n\right|}{n}\le a_n^2+\frac{1}{n^2}$, 得

$$
\frac{\left|a_n\right|}{n}\le\frac{a_n^2}{2}+\frac{1}{2n^2}.
$$

右端两项对应的级数分别由假设与 $p$ 级数($p=2$)知均收敛, 故再由**定理 2.2**, $\sum\frac{\left|a_n\right|}{n}$ 收敛. $\blacksquare$
