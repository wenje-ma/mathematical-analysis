# 作业 22

> **定理 5.1**（三角有理式的积分法）三角函数的有理式 $R\left(\sin x,\cos x\right)$ 的不定积分，总可通过万能代换 $t=\tan\dfrac{x}{2}$ 化为关于 $t$ 的有理函数的不定积分. 此时
> $$\sin x=\frac{2t}{1+t^2},\ \cos x=\frac{1-t^2}{1+t^2},\ \mathrm{d}x=\frac{2\,\mathrm{d}t}{1+t^2}.$$

### 习题一

（习题 4.5-1-1）求不定积分 $\displaystyle\int\frac{\mathrm{d}x}{2+\sin x}$.

### 解答 习题一

由**定理 5.1**（三角有理式的积分法），令万能代换 $t=\tan\dfrac{x}{2}$，则 $\sin x=\dfrac{2t}{1+t^2}$，$\mathrm{d}x=\dfrac{2\mathrm{d}t}{1+t^2}$. 代入得
$$
\int\frac{\mathrm{d}x}{2+\sin x}=\int\frac{1}{2+\dfrac{2t}{1+t^2}}\cdot\frac{2\mathrm{d}t}{1+t^2}=\int\frac{\mathrm{d}t}{t^2+t+1}.
$$

配方：$t^2+t+1=\left(t+\dfrac12\right)^2+\dfrac34$. 故
$$
\int\frac{\mathrm{d}t}{t^2+t+1}=\frac{2}{\sqrt3}\arctan\frac{2t+1}{\sqrt3}+C=\frac{2}{\sqrt3}\arctan\frac{2\tan\left(x/2\right)+1}{\sqrt3}+C.
$$ $\blacksquare$

### 习题二

（习题 4.5-1-3）求不定积分 $\displaystyle\int\cos^2x\,\mathrm{d}x$.

### 解答 习题二

利用半角公式 $\cos^2x=\dfrac{1+\cos2x}{2}$，
$$
\int\cos^2x\,\mathrm{d}x=\int\frac{1+\cos2x}{2}\,\mathrm{d}x=\frac{x}{2}+\frac{\sin2x}{4}+C.
$$ $\blacksquare$

### 习题三

（习题 4.5-1-5）求不定积分 $\displaystyle\int\cot^2x\,\mathrm{d}x$.

### 解答 习题三

利用恒等式 $\cot^2x=\csc^2x-1$，
$$
\int\cot^2x\,\mathrm{d}x=\int\left(\csc^2x-1\right)\,\mathrm{d}x=-\cot x-x+C.
$$ $\blacksquare$

### 习题四

（习题 4.5-1-7）求不定积分 $\displaystyle\int\frac{\mathrm{d}x}{\sin x+2\cos x}$.

### 解答 习题四

将分母写成 $R\sin\left(x+\varphi\right)$ 的形式：
$$
\sin x+2\cos x=\sqrt5\sin\left(x+\varphi\right),
$$

其中 $\varphi=\arctan2$. 故
$$
\int\frac{\mathrm{d}x}{\sin x+2\cos x}=\frac{1}{\sqrt5}\int\frac{\mathrm{d}x}{\sin\left(x+\varphi\right)}=\frac{1}{\sqrt5}\ln\left|\csc\left(x+\varphi\right)-\cot\left(x+\varphi\right)\right|+C.
$$ $\blacksquare$

### 习题五

（习题 4.5-1-9）求不定积分 $\displaystyle\int\sin^2x\cos^2x\,\mathrm{d}x$.

### 解答 习题五

利用恒等式 $\sin^2x\cos^2x=\dfrac{\sin^22x}{4}=\dfrac{1-\cos4x}{8}$，
$$
\int\sin^2x\cos^2x\,\mathrm{d}x=\int\frac{1-\cos4x}{8}\,\mathrm{d}x=\frac{x}{8}-\frac{\sin4x}{32}+C.
$$ $\blacksquare$

### 习题六

（习题 4.5-1-11）求不定积分 $\displaystyle\int\frac{\mathrm{d}x}{x+2}$.

### 解答 习题六

这是基本积分：
$$
\int\frac{\mathrm{d}x}{x+2}=\ln\left|x+2\right|+C.
$$ $\blacksquare$

### 习题七

（习题 4.5-1-13）求不定积分 $\displaystyle\int\frac{\mathrm{d}x}{e^x-1}$.

### 解答 习题七

令 $t=e^x$，则 $\mathrm{d}x=\dfrac{\mathrm{d}t}{t}$. 代入得
$$
\int\frac{\mathrm{d}x}{e^x-1}=\int\frac{\mathrm{d}t}{t\left(t-1\right)}=\int\left(\frac{1}{t-1}-\frac1t\right)\mathrm{d}t=\ln\left|t-1\right|-\ln\left|t\right|+C=\ln\left|\frac{e^x-1}{e^x}\right|+C=\ln\left|1-e^{-x}\right|+C.
$$ $\blacksquare$

### 习题八

（习题 4.5-2）设 $R\left(X,Y\right)$ 是关于变元 $X$ 与 $Y$ 的有理式，证明不定积分
$$\int R\left(\sin^2x,\cos^2x\right)\,\mathrm{d}x$$
可通过变换 $t=\tan x$ 有理化.

### 解答 习题八

令 $t=\tan x$，则 $x=\arctan t$，$\mathrm{d}x=\dfrac{\mathrm{d}t}{1+t^2}$. 又
$$
\sin^2x=\frac{t^2}{1+t^2},\ \cos^2x=\frac{1}{1+t^2}.
$$

代入被积函数：
$$
R\left(\sin^2x,\cos^2x\right)\,\mathrm{d}x=R\left(\frac{t^2}{1+t^2},\frac{1}{1+t^2}\right)\cdot\frac{\mathrm{d}t}{1+t^2}.
$$

右端是关于 $t$ 的有理函数（因 $R$ 是有理式，且 $\dfrac{t^2}{1+t^2}$ 与 $\dfrac{1}{1+t^2}$ 都是 $t$ 的有理函数）. 故原积分可通过 $t=\tan x$ 有理化. $\blacksquare$
