# 作业 16

> **定理 4.1**（局部泰勒展开式）设 $y=f\left(x\right)$ 在 $x_0$ 点附近有定义, 且有 $n$ 阶导数 $f^{\left(n\right)}\left(x_0\right)$. 则
> $$
> f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\frac{f''\left(x_0\right)}{2!}\left(x-x_0\right)^2+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right)\left(x\to x_0\right).
> $$
> **定理 4.2**（带拉格朗日余项的泰勒公式）设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上有 $n$ 阶连续导数, 在 $\left(a,b\right)$ 中有 $n+1$ 阶导数. 则对任意 $x,x_0\in\left[a,b\right]$, 存在介于 $x_0$ 与 $x$ 之间的点 $\xi$, 使得
> $$
> f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+\frac{f^{\left(n+1\right)}\left(\xi\right)}{\left(n+1\right)!}\left(x-x_0\right)^{n+1}.
> $$
### 习题一

（习题 3.4-1-2）写出函数 $y=\frac{1}{1-x}$ 在 $x=0$ 点的局部泰勒公式.

### 解答 习题一

对 $f\left(x\right)=\frac{1}{1-x}$ 求各阶导数: 
$$
f'\left(x\right)=\frac{1}{\left(1-x\right)^2}, f''\left(x\right)=\frac{2}{\left(1-x\right)^3},\cdots, f^{\left(n\right)}\left(x\right)=\frac{n!}{\left(1-x\right)^{n+1}}.
$$

故 $f^{\left(n\right)}\left(0\right)=n!$. 由**定理 4.1**（局部泰勒展开式）, 
$$
\frac{1}{1-x}=1+x+x^2+\cdots+x^n+o\left(x^n\right)\left(x\to0\right).
$$

$\blacksquare$
### 习题二

（习题 3.4-1-4）写出函数 $y=\arctan x$ 在 $x=0$ 点的局部泰勒公式(展开至 $x^5$ 为止).

### 解答 习题二

对 $f\left(x\right)=\arctan x$ 求各阶导数: 
$$
f'\left(x\right)=\frac{1}{1+x^2}, f''\left(x\right)=\frac{-2x}{\left(1+x^2\right)^2}, f'''\left(x\right)=\frac{6x^2-2}{\left(1+x^2\right)^3},
$$
$$
f^{\left(4\right)}\left(x\right)=\frac{24x\left(1-x^2\right)}{\left(1+x^2\right)^4}, f^{\left(5\right)}\left(x\right)=\frac{24\left(1-10x^2+5x^4\right)}{\left(1+x^2\right)^5}.
$$

代入 $x=0$: 
$$
f\left(0\right)=0, f'\left(0\right)=1, f''\left(0\right)=0, f'''\left(0\right)=-2, f^{\left(4\right)}\left(0\right)=0, f^{\left(5\right)}\left(0\right)=24.
$$

由**定理 4.1**（局部泰勒展开式）, 
$$
\arctan x=x-\frac{x^3}{3}+\frac{x^5}{5}+o\left(x^5\right)\left(x\to0\right).
$$

$\blacksquare$
### 习题三

（习题 3.4-1-5）写出函数 $y=\tan x$ 在 $x=0$ 点的局部泰勒公式(展开至 $x^3$ 为止).

### 解答 习题三

对 $f\left(x\right)=\tan x$ 求各阶导数: 
$$
f'\left(x\right)=\sec^2 x, f''\left(x\right)=2\sec^2 x\tan x, f'''\left(x\right)=4\sec^2 x\tan^2 x+2\sec^4 x.
$$

代入 $x=0$: 
$$
f\left(0\right)=0, f'\left(0\right)=1, f''\left(0\right)=0, f'''\left(0\right)=2.
$$

由**定理 4.1**（局部泰勒展开式）, 
$$
\tan x=x+\frac{x^3}{3}+o\left(x^3\right)\left(x\to0\right).
$$

$\blacksquare$
### 习题四

（习题 3.4-4）将 $y=\sin\left(x+\alpha\right)$ 在 $\alpha=0$ 点展开成带拉格朗日余项的泰勒公式, 并估计展开式
$$
\sin\left(x+\alpha\right)=\sin x+\left(\cos x\right)\alpha+r\left(\alpha\right)
$$
中余项的大小.

### 解答 习题四

将 $x$ 视作常数, 对 $\alpha$ 求导: 
$$
\frac{\mathrm{d}}{\mathrm{d}\alpha}\sin\left(x+\alpha\right)=\cos\left(x+\alpha\right),\frac{\mathrm{d}^2}{\mathrm{d}\alpha^2}\sin\left(x+\alpha\right)=-\sin\left(x+\alpha\right).
$$

在 $\alpha=0$ 处, 
$$
\sin\left(x+0\right)=\sin x,\frac{\mathrm{d}}{\mathrm{d}\alpha}\sin\left(x+\alpha\right)\Big|_{\alpha=0}=\cos x.
$$

由**定理 4.2**（带拉格朗日余项的泰勒公式）, 
$$
\sin\left(x+\alpha\right)=\sin x+\left(\cos x\right)\alpha+\frac{-\sin\left(x+\xi\right)}{2!}\alpha^2,
$$

其中 $\xi$ 介于 $0$ 与 $\alpha$ 之间.

余项 $r\left(\alpha\right)=-\frac{\sin\left(x+\xi\right)}{2}\alpha^2$, 故
$$
\left|r\left(\alpha\right)\right|\le\frac{\alpha^2}{2}.
$$

$\blacksquare$
### 习题五

（习题 3.4-5）将 $y=x+\frac{x^3}{3}$ 在 $x=\pm1$ 点展成泰勒公式. 说明: 任何一个多项式 $P_n\left(x\right)$ 在任何一点 $a$ 的 $n$ 次泰勒展开式之余项为 $0$.

### 解答 习题五

对 $f\left(x\right)=x+\frac{x^3}{3}$ 求各阶导数: 
$$
f'\left(x\right)=1+x^2, f''\left(x\right)=2x, f'''\left(x\right)=2, f^{\left(4\right)}\left(x\right)=0.
$$

在 $x=1$ 处: 
$$
f\left(1\right)=1+\frac13=\frac43, f'\left(1\right)=2, f''\left(1\right)=2, f'''\left(1\right)=2.
$$

由**定理 4.1**（局部泰勒展开式）, 
$$
x+\frac{x^3}{3}=\frac43+2\left(x-1\right)+\frac{2}{2!}\left(x-1\right)^2+\frac{2}{3!}\left(x-1\right)^3=\frac43+2\left(x-1\right)+\left(x-1\right)^2+\frac13\left(x-1\right)^3.
$$

在 $x=-1$ 处: 
$$
f\left(-1\right)=-1-\frac13=-\frac43, f'\left(-1\right)=2, f''\left(-1\right)=-2, f'''\left(-1\right)=2.
$$

故
$$
x+\frac{x^3}{3}=-\frac43+2\left(x+1\right)-\left(x+1\right)^2+\frac13\left(x+1\right)^3.
$$

对于一般多项式 $P_n\left(x\right)$, 其次数为 $n$, 故 $P_n^{\left(n+1\right)}\left(x\right)\equiv0$. 由**定理 4.2**（带拉格朗日余项的泰勒公式）, 余项
$$
R_n\left(x\right)=\frac{P_n^{\left(n+1\right)}\left(\xi\right)}{\left(n+1\right)!}\left(x-a\right)^{n+1}=0.
$$

即多项式的泰勒展开式是精确的, 余项为 $0$. $\blacksquare$

### 习题六

（习题 3.4-7）设 $y=f\left(x\right)$ 在 $a$ 点有 $n+1$ 阶导数. 证明: $f$ 在 $a$ 的 $n+1$ 阶泰勒多项式的导数等于 $f'$ 在 $a$ 点的 $n$ 阶泰勒多项式.

### 解答 习题六

$f$ 在 $a$ 点的 $n+1$ 阶泰勒多项式为
$$
T_{n+1}\left(x\right)=f\left(a\right)+f'\left(a\right)\left(x-a\right)+\frac{f''\left(a\right)}{2!}\left(x-a\right)^2+\cdots+\frac{f^{\left(n+1\right)}\left(a\right)}{\left(n+1\right)!}\left(x-a\right)^{n+1}.
$$

对 $x$ 求导: 
$$
T_{n+1}'\left(x\right)=f'\left(a\right)+f''\left(a\right)\left(x-a\right)+\frac{f'''\left(a\right)}{2!}\left(x-a\right)^2+\cdots+\frac{f^{\left(n+1\right)}\left(a\right)}{n!}\left(x-a\right)^n.
$$

而 $f'$ 在 $a$ 点的 $n$ 阶泰勒多项式为
$$
U_n\left(x\right)=f'\left(a\right)+\left(f'\right)'\left(a\right)\left(x-a\right)+\frac{\left(f'\right)''\left(a\right)}{2!}\left(x-a\right)^2+\cdots+\frac{\left(f'\right)^{\left(n\right)}\left(a\right)}{n!}\left(x-a\right)^n.
$$

注意到 $\left(f'\right)^{\left(k\right)}\left(a\right)=f^{\left(k+1\right)}\left(a\right)$, 故
$$
U_n\left(x\right)=f'\left(a\right)+f''\left(a\right)\left(x-a\right)+\frac{f'''\left(a\right)}{2!}\left(x-a\right)^2+\cdots+\frac{f^{\left(n+1\right)}\left(a\right)}{n!}\left(x-a\right)^n.
$$

比较两式, 即得 $T_{n+1}'\left(x\right)=U_n\left(x\right)$. $\blacksquare$

### 习题七

（习题 3.4-10）证明: 当 $x\to0$ 时, 
$$
\arctan x=x-\frac{x^3}{3}+\frac{x^5}{5}-\cdots+\left(-1\right)^m\frac{x^{2m+1}}{2m+1}+o\left(x^{2m+1}\right).
$$
### 解答 习题七

由习题六(第 7 题)的结果, $f$ 的泰勒多项式的导数等于 $f'$ 的泰勒多项式.

对 $f\left(x\right)=\arctan x$, 有
$$
f'\left(x\right)=\frac{1}{1+x^2}.
$$

由习题一(第 1(2) 题)的结果, 将 $-x^2$ 代入 $\frac{1}{1-t}$ 的展开式: 
$$
\frac{1}{1+x^2}=1-x^2+x^4-\cdots+\left(-1\right)^m x^{2m}+o\left(x^{2m}\right)\left(x\to0\right).
$$

即 $f'\left(x\right)$ 的 $2m$ 阶泰勒多项式为
$$
1-x^2+x^4-\cdots+\left(-1\right)^m x^{2m}.
$$

由习题六(第 7 题)的结果, $f\left(x\right)$ 的 $2m+1$ 阶泰勒多项式为上述多项式从常数项开始逐项积分(即求原多项式): 
$$
\arctan x=x-\frac{x^3}{3}+\frac{x^5}{5}-\cdots+\left(-1\right)^m\frac{x^{2m+1}}{2m+1}+o\left(x^{2m+1}\right)\left(x\to0\right).
$$

$\blacksquare$
### 习题八

（习题 3.4-11）设 $f\left(x\right)=x^{1/5}$, $x=32$, $\Delta x=0.16$. 那么
$$
f\left(32.16\right)=f\left(32\right)+f'\left(32\right)\Delta x+\frac{f''\left(\xi\right)}{2!}\left(\Delta x\right)^2,
$$
其中 $\xi$ 在 $32$ 与 $32.16$ 之间. 由第二章例可知

$$
f\left(32\right)+f'\left(32\right)\Delta x=2.002.
$$

证明: $2.002$ 作为 $32.16^{1/5}$ 的近似值, 其误差的绝对值小于 $10^{-6}$.

### 解答 习题八

误差为拉格朗日余项: 
$$
R_1=\frac{f''\left(\xi\right)}{2!}\left(\Delta x\right)^2,\xi\in\left(32,32.16\right).
$$

对 $f\left(x\right)=x^{1/5}$ 求二阶导数: 
$$
f'\left(x\right)=\frac15 x^{-4/5}, f''\left(x\right)=\frac15\cdot\left(-\frac45\right)x^{-9/5}=-\frac{4}{25}x^{-9/5}.
$$

故
$$
\left|R_1\right|=\left|\frac{f''\left(\xi\right)}{2}\right|\left(0.16\right)^2=\frac{2}{25}\xi^{-9/5}\cdot\left(0.16\right)^2.
$$

因 $\xi>32$, 故

$$
\xi^{-9/5}<32^{-9/5}=\left(2^5\right)^{-9/5}=2^{-9}=\frac{1}{512}.
$$

于是
$$
\left|R_1\right|<\frac{2}{25}\cdot\frac{1}{512}\cdot\left(0.16\right)^2=\frac{2\cdot0.0256}{25\cdot512}=4\times10^{-6}.
$$

即 $2.002$ 作为 $32.16^{1/5}$ 的近似值, 其误差绝对值约为 $4\times10^{-6}$. $\blacksquare$

### 习题九

（习题 3.4-12）用泰勒局部展开式证明下列结论: 设 $y=f\left(x\right)$ 在 $x_0$ 点有 $n$ 阶导数, $n>1$, 且
$$
f'\left(x_0\right)=f''\left(x_0\right)=\cdots=f^{\left(n-1\right)}\left(x_0\right)=0, f^{\left(n\right)}\left(x_0\right)\ne0.
$$
当 $n$ 为奇数时, $x_0$ 一定不是极值点; 当 $n$ 是偶数时, 若 $f^{\left(n\right)}\left(x_0\right)>0$, 则 $x_0$ 为极小值点; 若 $f^{\left(n\right)}\left(x_0\right)<0$, 则 $x_0$ 为极大值点.

### 解答 习题九

由**定理 4.1**（局部泰勒展开式）, 在 $x_0$ 附近, 
$$
f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right).
$$

由题设

$$
f'\left(x_0\right)=\cdots=f^{\left(n-1\right)}\left(x_0\right)=0,
$$

故
$$
f\left(x\right)-f\left(x_0\right)=\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right).
$$

当 $n$ 为奇数时, $\left(x-x_0\right)^n$ 在 $x_0$ 两侧变号(左负右正), 而 $\frac{f^{\left(n\right)}\left(x_0\right)}{n!}$ 为固定非零常数, 故 $f\left(x\right)-f\left(x_0\right)$ 在 $x_0$ 两侧变号. 因此 $x_0$ 不是极值点.

当 $n$ 为偶数时, $\left(x-x_0\right)^n>0$($x\ne x_0$). 若 $f^{\left(n\right)}\left(x_0\right)>$, 则 $f\left(x\right)-f\left(x_0\right)>0$($x$ 充分接近 $x_0$ 且 $x\ne x_0$), 即 $f\left(x\right)>f\left(x_0\right)$, 故 $x_0$ 为极小值点. 若 $f^{\left(n\right)}\left(x_0\right)<0$, 则 $f\left(x\right)-f\left(x_0\right)<0$, 即 $f\left(x\right)<f\left(x_0\right)$, 故 $x_0$ 为极大值点. $\blacksquare$
