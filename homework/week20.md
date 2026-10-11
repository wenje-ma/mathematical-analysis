# 作业 20

> **定理 3.1**（分部积分公式）设 $u\left(x\right),v\left(x\right)$ 可导，则
> $$\int u\left(x\right)\,\mathrm{d}v\left(x\right)=u\left(x\right)v\left(x\right)-\int v\left(x\right)\,\mathrm{d}u\left(x\right).$$

### 习题一

（习题 4.3-1-11）求不定积分 $\displaystyle\int x\csc^2x\,\mathrm{d}x$.

### 解答 习题一

令 $u=x$，$\mathrm{d}v=\csc^2x\,\mathrm{d}x$，则 $\mathrm{d}u=\mathrm{d}x$，$v=-\cot x$. 由**定理 3.1**（分部积分公式），
$$
\int x\csc^2x\,\mathrm{d}x=-x\cot x+\int\cot x\,\mathrm{d}x=-x\cot x+\ln\left|\sin x\right|+C.
$$ $\blacksquare$

### 习题二

（习题 4.3-1-13）求不定积分 $\displaystyle\int\sqrt{1+9x^2}\,\mathrm{d}x$.

### 解答 习题二

令 $u=\sqrt{1+9x^2}$，$\mathrm{d}v=\mathrm{d}x$，则
$$
\mathrm{d}u=\frac{9x}{\sqrt{1+9x^2}}\,\mathrm{d}x,\  v=x.
$$

由**定理 3.1**（分部积分公式），
$$
\int\sqrt{1+9x^2}\,\mathrm{d}x=x\sqrt{1+9x^2}-\int\frac{9x^2}{\sqrt{1+9x^2}}\,\mathrm{d}x.
$$

将被积函数变形：
$$
\frac{9x^2}{\sqrt{1+9x^2}}=\frac{9x^2+1-1}{\sqrt{1+9x^2}}=\sqrt{1+9x^2}-\frac{1}{\sqrt{1+9x^2}}.
$$

代入得
$$
\int\sqrt{1+9x^2}\,\mathrm{d}x=x\sqrt{1+9x^2}-\int\sqrt{1+9x^2}\,\mathrm{d}x+\int\frac{\mathrm{d}x}{\sqrt{1+9x^2}}.
$$

移项：
$$
2\int\sqrt{1+9x^2}\,\mathrm{d}x=x\sqrt{1+9x^2}+\int\frac{\mathrm{d}x}{\sqrt{1+9x^2}}.
$$

而
$$
\int\frac{\mathrm{d}x}{\sqrt{1+9x^2}}=\frac13\ln\left(3x+\sqrt{1+9x^2}\right)+C.
$$

故
$$
\int\sqrt{1+9x^2}\,\mathrm{d}x=\frac{x}{2}\sqrt{1+9x^2}+\frac16\ln\left(3x+\sqrt{1+9x^2}\right)+C.
$$ $\blacksquare$

### 习题三

（习题 4.3-1-14）求不定积分 $\displaystyle\int\sec^3x\,\mathrm{d}x$.

### 解答 习题三

令 $u=\sec x$，$\mathrm{d}v=\sec^2x\,\mathrm{d}x$，则 $\mathrm{d}u=\sec x\tan x\,\mathrm{d}x$，$v=\tan x$. 由**定理 3.1**（分部积分公式），
$$
\int\sec^3x\,\mathrm{d}x=\sec x\tan x-\int\sec x\tan^2x\,\mathrm{d}x.
$$

利用 $\tan^2x=\sec^2x-1$，
$$
\int\sec^3x\,\mathrm{d}x=\sec x\tan x-\int\sec x\left(\sec^2x-1\right)\,\mathrm{d}x=\sec x\tan x-\int\sec^3x\,\mathrm{d}x+\int\sec x\,\mathrm{d}x.
$$

移项：
$$
2\int\sec^3x\,\mathrm{d}x=\sec x\tan x+\int\sec x\,\mathrm{d}x.
$$

而 $\displaystyle\int\sec x\,\mathrm{d}x=\ln\left|\sec x+\tan x\right|+C$. 故
$$
\int\sec^3x\,\mathrm{d}x=\frac12\left(\sec x\tan x+\ln\left|\sec x+\tan x\right|\right)+C.
$$ $\blacksquare$
