# 作业 18

> **定义**（原函数与不定积分）设 $y=f\left(x\right)$ 定义在 $\left(a,b\right)$ 区间之中. 若 $F\left(x\right)$ 在 $\left(a,b\right)$ 中可微, 且 $F'\left(x\right)=f\left(x\right)$($\forall x\in\left(a,b\right)$), 则称 $y=F\left(x\right)$ 是 $y=f\left(x\right)$ 的一个原函数. $f\left(x\right)$ 的一切原函数 $F\left(x\right)+C$($C$ 为任意常数)称作 $f\left(x\right)$ 的不定积分, 记作
> $$
> \int f\left(x\right)\,\mathrm{d}x=F\left(x\right)+C.
> $$
> **定理 1.3**（不定积分的线性法则）设 $y=f\left(x\right)$ 及 $y=g\left(x\right)$ 在某个区间中有原函数. 则
> $$
> \int\left[af\left(x\right)+bg\left(x\right)\right]\mathrm{d}x=a\int f\left(x\right)\,\mathrm{d}x+b\int g\left(x\right)\,\mathrm{d}x,
> $$
> 其中 $a,b$ 是两个任意常数.

### 习题一

（习题 4.1-1-1）求不定积分 $\displaystyle\int\left(x^3+4\right)\,\mathrm{d}x$.

### 解答 习题一

由**定理 1.3**（不定积分的线性法则）, 
$$
\int\left(x^3+4\right)\,\mathrm{d}x=\int x^3\,\mathrm{d}x+4\int 1\,\mathrm{d}x=\frac{x^4}{4}+4x+C.
$$

$\blacksquare$
### 习题二

（习题 4.1-1-4）求不定积分 $\displaystyle\int\tan^2x\,\mathrm{d}x$.

### 解答 习题二

利用三角恒等式 $\tan^2x=\sec^2x-1$, 由**定理 1.3**（不定积分的线性法则）, 
$$
\int\tan^2x\,\mathrm{d}x=\int\left(\sec^2x-1\right)\,\mathrm{d}x=\int\sec^2x\,\mathrm{d}x-\int1\,\mathrm{d}x=\tan x-x+C.
$$

$\blacksquare$
### 习题三

（习题 4.1-1-6）求不定积分 $\displaystyle\int\left(3^x-4^{-x}\right)^2\,\mathrm{d}x$.

### 解答 习题三

展开被积函数: 
$$
\left(3^x-4^{-x}\right)^2=9^x-2\cdot3^x\cdot4^{-x}+16^{-x}=9^x-2\cdot\left(\frac34\right)^x+16^{-x}.
$$

由**定理 1.3**（不定积分的线性法则）及指数函数积分公式 $\displaystyle\int a^x\,\mathrm{d}x=\frac{a^x}{\ln a}+C$, 
$$
\int\left(3^x-4^{-x}\right)^2\,\mathrm{d}x=\frac{9^x}{\ln9}-2\cdot\frac{\left(3/4\right)^x}{\ln\left(3/4\right)}+\frac{16^{-x}}{-\ln16}+C.
$$

$\blacksquare$
### 习题四

（习题 4.1-1-8）求不定积分 $\displaystyle\int\frac{x^2}{1+x^2}\,\mathrm{d}x$.

### 解答 习题四

将被积函数变形: 
$$
\frac{x^2}{1+x^2}=\frac{x^2+1-1}{1+x^2}=1-\frac{1}{1+x^2}.
$$

由**定理 1.3**（不定积分的线性法则）, 
$$
\int\frac{x^2}{1+x^2}\,\mathrm{d}x=\int1\,\mathrm{d}x-\int\frac{1}{1+x^2}\,\mathrm{d}x=x-\arctan x+C.
$$

$\blacksquare$
### 习题五

（习题 4.1-1-10）求不定积分 $\displaystyle\int\left(a\,\mathrm{sh}\,x+b\,\mathrm{ch}\,x\right)\,\mathrm{d}x$($a,b$ 为常数).

### 解答 习题五

由 $\left(\mathrm{sh}\,x\right)'=\mathrm{ch}\,x$, $\left(\mathrm{ch}\,x\right)'=\mathrm{sh}\,x$, 及**定理 1.3**（不定积分的线性法则）, 
$$
\int\left(a\,\mathrm{sh}\,x+b\,\mathrm{ch}\,x\right)\,\mathrm{d}x=a\,\mathrm{ch}\,x+b\,\mathrm{sh}\,x+C.
$$

$\blacksquare$
### 习题六

（习题 4.1-1-11）求不定积分 $\displaystyle\int\frac{1}{\sin^2x\cos^2x}\,\mathrm{d}x$.

### 解答 习题六

利用三角恒等式 $1=\sin^2x+\cos^2x$, 
$$
\frac{1}{\sin^2x\cos^2x}=\frac{\sin^2x+\cos^2x}{\sin^2x\cos^2x}=\frac{1}{\cos^2x}+\frac{1}{\sin^2x}=\sec^2x+\csc^2x.
$$

由**定理 1.3**（不定积分的线性法则）, 
$$
\int\frac{1}{\sin^2x\cos^2x}\,\mathrm{d}x=\int\sec^2x\,\mathrm{d}x+\int\csc^2x\,\mathrm{d}x=\tan x-\cot x+C.
$$

$\blacksquare$
### 习题七

（习题 4.1-1-12）求不定积分 $\displaystyle\int\sin^2\frac{x}{2}\,\mathrm{d}x$.

### 解答 习题七

利用半角公式 $\sin^2\frac{x}{2}=\frac{1-\cos x}{2}$, 由**定理 1.3**（不定积分的线性法则）, 
$$
\int\sin^2\frac{x}{2}\,\mathrm{d}x=\int\frac{1-\cos x}{2}\,\mathrm{d}x=\frac12\int1\,\mathrm{d}x-\frac12\int\cos x\,\mathrm{d}x=\frac{x}{2}-\frac{\sin x}{2}+C.
$$

$\blacksquare$
### 习题八

（习题 4.1-2）证明:

$$
\displaystyle\int\frac{\mathrm{d}x}{x^2+a^2}=\frac1a\arctan\frac{x}{a}+C\ \left(a>0\right).
$$

### 解答 习题八

对右端求导: 
$$
\left(\frac1a\arctan\frac{x}{a}\right)'=\frac1a\cdot\frac{1}{1+\left(x/a\right)^2}\cdot\frac1a=\frac{1}{a^2+x^2}.
$$

由**定义**（原函数与不定积分）, 右端即为被积函数的一个原函数. 故
$$
\int\frac{\mathrm{d}x}{x^2+a^2}=\frac1a\arctan\frac{x}{a}+C.
$$

$\blacksquare$
### 习题九

（习题 4.1-4）证明:

$$
\displaystyle\int\frac{\mathrm{d}x}{\sqrt{a^2-x^2}}=\arcsin\frac{x}{a}+C\ \left(a>0\right).
$$

### 解答 习题九

对右端求导: 
$$
\left(\arcsin\frac{x}{a}\right)'=\frac{1}{\sqrt{1-\left(x/a\right)^2}}\cdot\frac1a=\frac{1}{\sqrt{a^2-x^2}}.
$$

由**定义**（原函数与不定积分）, 右端即为被积函数的一个原函数. 故
$$
\int\frac{\mathrm{d}x}{\sqrt{a^2-x^2}}=\arcsin\frac{x}{a}+C.
$$

$\blacksquare$