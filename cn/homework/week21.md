# 作业 21

> **定理 4.1**（有理函数的分解）任何有理函数 $\frac{P\left(x\right)}{Q\left(x\right)}$ 都可以分解为一个多项式与若干部分分式之和, 其中每个部分分式形如 $\frac{A}{\left(x-a\right)^k}$ 或 $\frac{Bx+C}{\left(x^2+px+q\right)^m}$($p^2-4q< 0$).

### 习题一

（习题 4.4-2）求不定积分 $\displaystyle\int\frac{x^3}{x^2+x-6}\,\mathrm{d}x$.

### 解答 习题一

因分子次数高于分母, 先做多项式除法: 
$$
\frac{x^3}{x^2+x-6}=x-1+\frac{7x-6}{x^2+x-6}.
$$

分解分母:

$$
x^2+x-6=\left(x+3\right)\left(x-2\right).
$$

由**定理 4.1**（有理函数的分解）, 设
$$
\frac{7x-6}{\left(x+3\right)\left(x-2\right)}=\frac{A}{x+3}+\frac{B}{x-2}.
$$

通分后比较分子:

$$
7x-6=A\left(x-2\right)+B\left(x+3\right).
$$

令 $x=-3$, 得 $-27=-5A$, 即 $A=\frac{27}{5}$. 令 $x=2$, 得 $8=5B$, 即 $B=\frac85$.

故
$$
\int\frac{x^3}{x^2+x-6}\,\mathrm{d}x=\int\left(x-1\right)\,\mathrm{d}x+\frac{27}{5}\int\frac{\mathrm{d}x}{x+3}+\frac85\int\frac{\mathrm{d}x}{x-2}=\frac{x^2}{2}-x+\frac{27}{5}\ln\left|x+3\right|+\frac85\ln\left|x-2\right|+C.
$$

$\blacksquare$
### 习题二

（习题 4.4-4）求不定积分 $\displaystyle\int\frac{4x^2}{x\left(x+2\right)}\,\mathrm{d}x$.

### 解答 习题二

化简被积函数: 
$$
\frac{4x^2}{x\left(x+2\right)}=\frac{4x}{x+2}=4-\frac{8}{x+2}.
$$

故
$$
\int\frac{4x^2}{x\left(x+2\right)}\,\mathrm{d}x=\int4\,\mathrm{d}x-8\int\frac{\mathrm{d}x}{x+2}=4x-8\ln\left|x+2\right|+C.
$$

$\blacksquare$
### 习题三

（习题 4.4-6）求不定积分 $\displaystyle\int\frac{2x^2-5}{x^4-5x^2+6}\,\mathrm{d}x$.

### 解答 习题三

分解分母:

$$
x^4-5x^2+6=\left(x^2-2\right)\left(x^2-3\right).
$$

由**定理 4.1**（有理函数的分解）, 设
$$
\frac{2x^2-5}{\left(x^2-2\right)\left(x^2-3\right)}=\frac{A}{x^2-2}+\frac{B}{x^2-3}.
$$

通分后比较分子:

$$
2x^2-5=A\left(x^2-3\right)+B\left(x^2-2\right)=\left(A+B\right)x^2+\left(-3A-2B\right).
$$

比较系数得 $A+B=2$, $-3A-2B=-5$. 解得 $A=1$, $B=1$.

故
$$
\int\frac{2x^2-5}{x^4-5x^2+6}\,\mathrm{d}x=\int\frac{\mathrm{d}x}{x^2-2}+\int\frac{\mathrm{d}x}{x^2-3}=\frac{1}{2\sqrt2}\ln\left|\frac{x-\sqrt2}{x+\sqrt2}\right|+\frac{1}{2\sqrt3}\ln\left|\frac{x-\sqrt3}{x+\sqrt3}\right|+C.
$$

$\blacksquare$
### 习题四

（习题 4.4-8）求不定积分 $\displaystyle\int\frac{x}{\left(x^2+2\right)^2}\,\mathrm{d}x$.

### 解答 习题四

令 $u=x^2+2$, 则 $\mathrm{d}u=2x\,\mathrm{d}x$. 由第一换元法则, 
$$
\int\frac{x}{\left(x^2+2\right)^2}\,\mathrm{d}x=\frac12\int\frac{\mathrm{d}u}{u^2}=-\frac{1}{2u}+C=-\frac{1}{2\left(x^2+2\right)}+C.
$$

$\blacksquare$
### 习题五

（习题 4.4-10）求不定积分 $\displaystyle\int\frac{x^3}{\left(x-1\right)^2}\,\mathrm{d}x$.

### 解答 习题五

令 $u=x-1$, 则 $x=u+1$, $\mathrm{d}x=\mathrm{d}u$. 被积函数变为
$$
\frac{\left(u+1\right)^3}{u^2}=\frac{u^3+3u^2+3u+1}{u^2}=u+3+\frac3u+\frac{1}{u^2}.
$$

故
$$
\int\frac{x^3}{\left(x-1\right)^2}\,\mathrm{d}x=\int\left(u+3+\frac3u+\frac{1}{u^2}\right)\mathrm{d}u=\frac{u^2}{2}+3u+3\ln\left|u\right|-\frac1u+C.
$$

代回 $u=x-1$: 
$$
\int\frac{x^3}{\left(x-1\right)^2}\,\mathrm{d}x=\frac{\left(x-1\right)^2}{2}+3\left(x-1\right)+3\ln\left|x-1\right|-\frac{1}{x-1}+C.
$$

$\blacksquare$
### 习题六

（习题 4.4-12）求不定积分 $\displaystyle\int\frac{e^t}{e^{2t}+5e^t+6}\,\mathrm{d}t$.

### 解答 习题六

令 $u=e^t$, 则 $\mathrm{d}u=e^t\,\mathrm{d}t$. 积分化为
$$
\int\frac{\mathrm{d}u}{u^2+5u+6}=\int\frac{\mathrm{d}u}{\left(u+2\right)\left(u+3\right)}.
$$

由**定理 4.1**（有理函数的分解）, 设 $\frac{1}{\left(u+2\right)\left(u+3\right)}=\frac{A}{u+2}+\frac{B}{u+3}$. 令 $u=-2$, 得 $A=1$. 令 $u=-3$, 得 $B=-1$.

故
$$
\int\frac{e^t}{e^{2t}+5e^t+6}\,\mathrm{d}t=\ln\left|u+2\right|-\ln\left|u+3\right|+C=\ln\frac{e^t+2}{e^t+3}+C.
$$

$\blacksquare$
### 习题七

（习题 4.4-14）求不定积分 $\displaystyle\int\frac{\mathrm{d}x}{\left(x^2+4\right)^2\left(x+1\right)}$.

### 解答 习题七

由**定理 4.1**（有理函数的分解）, 设
$$
\frac{1}{\left(x^2+4\right)^2\left(x+1\right)}=\frac{A}{x+1}+\frac{Bx+C}{x^2+4}+\frac{Dx+E}{\left(x^2+4\right)^2}.
$$

通分后比较分子: 
$$
1=A\left(x^2+4\right)^2+\left(Bx+C\right)\left(x^2+4\right)\left(x+1\right)+\left(Dx+E\right)\left(x+1\right).
$$

令 $x=-1$, 得 $1=A\cdot25$, 即 $A=\frac{1}{25}$. 比较各次项系数: 

- $x^4$: $A+B=0$, 故 $B=-\frac{1}{25}$.
- $x^3$: $B+C=0$, 故 $C=\frac{1}{25}$.
- $x^2$: $8A+4B+C+D=0$, 即 $\frac{8}{25}-\frac{4}{25}+\frac{1}{25}+D=0$, 故 $D=-\frac15$.
- $x$: $4B+4C+D+E=0$, 即 $-\frac{4}{25}+\frac{4}{25}-\frac15+E=0$, 故 $E=\frac15$.

故
$$
\int\frac{\mathrm{d}x}{\left(x^2+4\right)^2\left(x+1\right)}=\frac{1}{25}\int\frac{\mathrm{d}x}{x+1}+\int\frac{-x/25+1/25}{x^2+4}\,\mathrm{d}x+\int\frac{-x/5+1/5}{\left(x^2+4\right)^2}\,\mathrm{d}x.
$$

分别计算各项: 
$$
\int\frac{\mathrm{d}x}{x+1}=\ln\left|x+1\right|,
$$
$$
\int\frac{x}{x^2+4}\,\mathrm{d}x=\frac12\ln\left(x^2+4\right),\int\frac{\mathrm{d}x}{x^2+4}=\frac12\arctan\frac{x}{2},
$$
$$
\int\frac{x}{\left(x^2+4\right)^2}\,\mathrm{d}x=-\frac{1}{2\left(x^2+4\right)},\int\frac{\mathrm{d}x}{\left(x^2+4\right)^2}=\frac{x}{8\left(x^2+4\right)}+\frac{1}{16}\arctan\frac{x}{2}.
$$

合并得
$$
\int\frac{\mathrm{d}x}{\left(x^2+4\right)^2\left(x+1\right)}=\frac{1}{25}\ln\left|x+1\right|-\frac{1}{50}\ln\left(x^2+4\right)+\frac{13}{400}\arctan\frac{x}{2}+\frac{x+4}{40\left(x^2+4\right)}+C.
$$

$\blacksquare$