# 作业 4

> **定理 4.2**（夹逼定理）设 $\left\{a_n\right\},\left\{b_n\right\},\left\{c_n\right\}$ 为三个序列, 并且存在一个自然数 $N_0$, 使得 $c_n\le a_n\le b_n,\forall n\ge N_0$. 若 $c_n$ 与 $b_n$ 都有极限存在, 并都等于 $l$, 则 $a_n$ 的极限存在, 并且也等于 $l$.

> **重要极限**（数 $e$）$\lim\limits_{n\to\infty}\left(1+\frac1n\right)^n=e$, 其中 $e$ 为无理数, $2<e<3$.

> **定义**（无穷小量）以 $0$ 为其极限的变量称作无穷小量.

### 习题一

（习题 1.4-1）求下列极限: 
(1) $\lim\limits_{n\to\infty}\left(1+\frac1{n+1}\right)^{n-1}$;

(2) $\lim\limits_{n\to\infty}\left(1-\frac1{n^2}\right)^{n^2+1}$;

(3) $\lim\limits_{n\to\infty}\left(1+\frac3{3n+1}\right)^n$;

(4) $\lim\limits_{n\to\infty}\left(\frac{n+3}{n+1}\right)^{n+1}$.

### 解答 习题一

(1)

$$
\left(1+\frac1{n+1}\right)^{n-1}=\left[\left(1+\frac1{n+1}\right)^{n+1}\right]^{\frac{n-1}{n+1}}.
$$

由**重要极限**（数 $e$）及第一章**定理 3.1**, 底数趋于 $e$, 指数 $\frac{n-1}{n+1}\to1$, 故极限为 $e$.

(2)

$$
\left(1-\frac1{n^2}\right)^{n^2+1}=\left(1-\frac1{n^2}\right)^{n^2}\cdot\left(1-\frac1{n^2}\right).
$$
令 $m=-n^2$, 则 $\left(1+\frac1m\right)^m\to e$, 故

$$
\left(1-\frac1{n^2}\right)^{n^2}=\left[\left(1+\frac1{-n^2}\right)^{-n^2}\right]^{-1}\to e^{-1},
$$

且 $\left(1-\frac1{n^2}\right)\to1$. 故极限为 $e^{-1}=\frac1e$.

(3)

$$
\left(1+\frac3{3n+1}\right)^n=\left[\left(1+\frac3{3n+1}\right)^{\frac{3n+1}{3}}\right]^{\frac{3n}{3n+1}}.
$$

由**重要极限**（数 $e$）, 底数趋于 $e$, 指数 $\frac{3n}{3n+1}\to1$, 故极限为 $e$.

(4)

$$
\left(\frac{n+3}{n+1}\right)^{n+1}=\left(1+\frac2{n+1}\right)^{n+1}=\left[\left(1+\frac2{n+1}\right)^{\frac{n+1}{2}}\right]^2.
$$

由**重要极限**（数 $e$）, 底数趋于 $e$, 故极限为 $e^2$. $\blacksquare$

### 习题二

（习题 1.4-3-2）利用单调有界序列有极限, 证明序列

$$
a_n=\frac1{n+1}+\frac1{n+2}+\cdots+\frac1{2n}
$$

的极限存在.

### 解答 习题二

先证 $\left\{a_n\right\}$ 单调递增: 

$$
a_{n+1}-a_n=\frac1{2n+1}+\frac1{2n+2}-\frac1{n+1}=\frac1{2n+1}-\frac1{2n+2}>0.
$$

故 $\left\{a_n\right\}$ 单调递增.

再证有上界:

$$
a_n=\displaystyle\sum_{k=n+1}^{2n}\frac1k\le\frac{n}{n+1}<1.
$$

由第一章**定理 3.2**（实数域完备性）, 单调递增有上界的序列有极限, 故 $\lim a_n$ 存在. $\blacksquare$

### 习题三

（习题 1.4-4）令 $0<a<b$, $n$ 为正整数. 证明: 
(1)

$$
\left(n+1\right)a^n<\frac{b^{n+1}-a^{n+1}}{b-a}<\left(n+1\right)b^n;
$$

(2) 令 $a=1+\frac1{n+1},b=1+\frac1n$, 由上式推出 $\left(1+\frac1n\right)^n$ 严格递增, $\left(1+\frac1n\right)^{n+1}$ 严格递减.

### 解答 习题三

(1)由因式分解, 

$$
\frac{b^{n+1}-a^{n+1}}{b-a}=b^n+b^{n-1}a+\cdots+ba^{n-1}+a^n=\sum_{k=0}^n b^{n-k}a^k.
$$

因 $0<a<b$, 对每一项 $b^{n-k}a^k$ 有 $a^n<b^{n-k}a^k<b^n$. 求和得

$$
\left(n+1\right)a^n<\sum_{k=0}^n b^{n-k}a^k<\left(n+1\right)b^n,
$$

即(1)成立.

(2)取 $a=1+\frac1{n+1},b=1+\frac1n$, 则

$$
b-a=\frac1{n\left(n+1\right)}.
$$

由(1)的右半: $\frac{b^{n+1}-a^{n+1}}{b-a}<\left(n+1\right)b^n$, 即

$$
n\left(n+1\right)\left(b^{n+1}-a^{n+1}\right)<\left(n+1\right)b^n,
$$

亦即 $n\left(b^{n+1}-a^{n+1}\right)<b^n$. 整理得 $nb^{n+1}-b^n<na^{n+1}$, 即 $b^n\left(nb-1\right)<na^{n+1}$. 代入 $nb=n+1$, 得 $b^n\cdot n<na^{n+1}$, 即 $b^n<a^{n+1}$, 亦即

$$
\left(1+\frac1n\right)^n<\left(1+\frac1{n+1}\right)^{n+1},
$$

故 $\left(1+\frac1n\right)^n$ 严格递增.

由(1)的左半: $\left(n+1\right)a^n<\frac{b^{n+1}-a^{n+1}}{b-a}$, 即

$$
\left(n+1\right)a^n<n\left(n+1\right)\left(b^{n+1}-a^{n+1}\right),
$$

亦即 $a^n<n\left(b^{n+1}-a^{n+1}\right)$. 整理得 $a^n+na^{n+1}<nb^{n+1}$, 即 $a^n\left(na+1\right)<nb^{n+1}$. 代入 $na=\frac{n\left(n+2\right)}{n+1}$, 化简可得 $a^{n+2}<b^{n+1}$, 亦即

$$
\left(1+\frac1{n+1}\right)^{n+2}<\left(1+\frac1n\right)^{n+1},
$$

故 $\left(1+\frac1n\right)^{n+1}$ 严格递减. $\blacksquare$

### 习题四

（习题 1.4-5）证明

$$
\left(1+\frac1n\right)^n<e<\left(1+\frac1n\right)^{n+1},n=1,2,\cdots.
$$

### 解答 习题四

由**习题三**, $\left(1+\frac1n\right)^n$ 严格递增, 且由**重要极限**（数 $e$）其极限为 $e$, 故对一切 $n$ 有

$$
\left(1+\frac1n\right)^n<e.
$$

同理, $\left(1+\frac1n\right)^{n+1}$ 严格递减, 其极限为

$$
\lim\left(1+\frac1n\right)^{n+1}=\lim\left(1+\frac1n\right)^n\cdot\left(1+\frac1n\right)=e\cdot1=e,
$$

故对一切 $n$ 有

$$
e<\left(1+\frac1n\right)^{n+1}.
$$

合并得

$$
\left(1+\frac1n\right)^n<e<\left(1+\frac1n\right)^{n+1}.
$$

$\blacksquare$

### 习题五

（习题 1.4-6）设 $\left\{a_n\right\}$ 为递增序列, 而 $\left\{b_n\right\}$ 为递减序列, 并假定 $\lim\limits_{n\to\infty}\left(a_n-b_n\right)=0$. 证明 $\lim a_n$ 与 $\lim b_n$ 都存在, 且相等.

### 解答 习题五

因 $\lim\left(a_n-b_n\right)=0$, 存在 $N$ 使得当 $n>N$ 时 $\left|a_n-b_n\right|<1$, 即 $a_n<b_n+1$. 又 $\left\{b_n\right\}$ 递减, 故 $b_n\le b_1$, 从而 $a_n<b_1+1$($n>N$). 对 $n\le N$, $a_n$ 取有限个值有界. 故 $\left\{a_n\right\}$ 递增且有上界, 由第一章**定理 3.2**（实数域完备性）, $\lim a_n=A$ 存在.

同理, 当 $n>N$ 时 $b_n>a_n-1\ge a_1-1$(因 $a_n\ge a_1$), 故 $\left\{b_n\right\}$ 递减且有下界. 由**定理 3.2** 的递减版本, $\lim b_n=B$ 存在.

最后,

$$
A-B=\lim\left(a_n-b_n\right)=0,
$$

故 $A=B$. $\blacksquare$

### 习题六

（习题 1.4-9）证明

$$
e=\lim\limits_{n\to\infty}\left(1+1+\frac1{2!}+\cdots+\frac1{n!}\right).
$$

### 解答 习题六

由牛顿二项式展开, 

$$
\left(1+\frac1n\right)^n=\sum_{k=0}^n\binom nk\frac1{n^k}=1+1+\sum_{k=2}^n\frac1{k!}\left(1-\frac1n\right)\left(1-\frac2n\right)\cdots\left(1-\frac{k-1}n\right).
$$

对任意固定的 $m\ge2$, 当 $n>m$ 时, 

$$
\left(1+\frac1n\right)^n>1+1+\sum_{k=2}^m\frac1{k!}\left(1-\frac1n\right)\left(1-\frac2n\right)\cdots\left(1-\frac{k-1}n\right).
$$

令 $n\to\infty$, 由**重要极限**（数 $e$）及第一章**定理 3.1**, 左端趋于 $e$, 右端趋于 $1+1+\frac1{2!}+\cdots+\frac1{m!}$, 故

$$
e\ge1+1+\frac1{2!}+\cdots+\frac1{m!}.
$$

另一方面, 对一切 $n$,

$$
\left(1+\frac1n\right)^n<1+1+\frac1{2!}+\cdots+\frac1{n!}\ \left(\text{因各项因子}<1\right),
$$

令 $n\to\infty$ 得

$$
e\le\lim_{n\to\infty}\left(1+1+\frac1{2!}+\cdots+\frac1{n!}\right).
$$

结合两方面,

$$
e=\lim\limits_{n\to\infty}\left(1+1+\frac1{2!}+\cdots+\frac1{n!}\right).
$$

$\blacksquare$

### 习题七

（习题 1.4-10）利用上题结果证明 $2<e<3$.

### 解答 习题七

由**习题六**, $e=\displaystyle\sum_{k=0}^{\infty}\frac1{k!}>1+1=2$.

又对 $k\ge2$, $k!=2\cdot3\cdots k\ge2^{k-1}$, 故 $\frac1{k!}\le\frac1{2^{k-1}}$. 于是

$$
e=1+1+\sum_{k=2}^{\infty}\frac1{k!}\le2+\sum_{k=2}^{\infty}\frac1{2^{k-1}}=2+1=3.
$$

且等号不可能成立(因 $k=3$ 时 $1/6<1/4$), 故 $e<3$. 综上 $2<e<3$. $\blacksquare$

### 习题八

（习题 1.4-14）设有两个序列 $\left\{a_n\right\}$ 与 $\left\{b_n\right\}$, 其中 $\left\{a_n\right\}$ 为**无穷小量**, 而 $\left\{b_n\right\}$ 为有界序列, 即存在一个正数 $M$, 使得 $\left|b_n\right|\le M,\forall n=1,2,\cdots$. 证明 $\lim\limits_{n\to\infty}a_nb_n=0$.

### 解答 习题八

因 $\left\{a_n\right\}$ 为**无穷小量**, 即 $\lim a_n=0$. 又 $\left|b_n\right|\le M$, 故

$$
0\le\left|a_nb_n\right|\le M\left|a_n\right|.
$$

当 $n\to\infty$ 时 $M\left|a_n\right|\to0$, 左端 $0\to0$. 由**定理 4.2**（夹逼定理）, $\lim\left|a_nb_n\right|=0$, 即 $\lim a_nb_n=0$. $\blacksquare$

### 习题九

（习题 1.4-16）设 $\lim\limits_{n\to\infty}a_n=a$, 证明: 
(1) $\lim\limits_{n\to\infty}\frac{\left[na_n\right]}{n}=a$;

(2) 若 $a>0$ 且 $a_n>0$, 则

$$
\lim\limits_{n\to\infty}\sqrt\left[n\right]{a_n}=1.
$$

### 解答 习题九

(1)由取整函数定义, $na_n-1<\left[na_n\right]\le na_n$, 故

$$
a_n-\frac1n<\frac{\left[na_n\right]}{n}\le a_n.
$$

当 $n\to\infty$ 时 $a_n\to a$, $a_n-\frac1n\to a$(因 $\frac1n\to0$). 由**定理 4.2**（夹逼定理）, $\frac{\left[na_n\right]}{n}\to a$.

(2)因 $a_n\to a>0$, 存在 $N$ 使得当 $n>N$ 时 $\frac a2<a_n<2a$. 于是

$$
\left(\frac a2\right)^{1/n}<a_n^{1/n}<\left(2a\right)^{1/n}.
$$

由第一章**例 3.3**（正数的 $n$ 次方根趋于 $1$）, 两端均趋于 $1$. 由**定理 4.2**（夹逼定理）,

$$
\sqrt\left[n\right]{a_n}\to1.
$$

$\blacksquare$

### 习题十

（习题 1.4-18）证明 $\lim\limits_{n\to\infty}\left(1+\frac1{n^2}\right)^n=1$.

### 解答 习题十

由牛顿二项式展开, 

$$
\left(1+\frac1{n^2}\right)^n=\sum_{k=0}^n\binom nk\frac1{n^{2k}}=1+\frac1n+\sum_{k=2}^n\binom nk\frac1{n^{2k}}.
$$

对 $k\ge2$, $\binom nk\le\frac{n^k}{k!}$, 故

$$
0\le\left(1+\frac1{n^2}\right)^n-1\le\frac1n+\frac1{n^2}\sum_{k=2}^n\frac1{k!}\le\frac1n+\frac{e-2}{n^2}.
$$

右端当 $n\to\infty$ 时趋于 $0$. 由**定理 4.2**（夹逼定理）, $\left(1+\frac1{n^2}\right)^n\to1$. $\blacksquare$
