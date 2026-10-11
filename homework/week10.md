# 作业 10

> **定义**（微分）设 $y=f\left(x\right)$ 在 $x_0$ 附近有定义. 若存在常数 $A$，使得 $\Delta y=A\Delta x+o\left(\Delta x\right)$，则称 $f$ 在 $x_0$ 可微，$\mathrm dy=A\Delta x$ 称为微分，且 $A=f'\left(x_0\right)$.

> **定义**（高阶无穷小）若 $\lim\limits_{x\to0}\frac{\alpha\left(x\right)}{\beta\left(x\right)}=0$，则称 $\alpha\left(x\right)=o\left(\beta\left(x\right)\right)$.

### 习题一

（习题 2.3-1-2）当 $x\to0$ 时，下列无穷小量是几阶无穷小量：$y=\left(\sqrt{2+x}-\sqrt2\right)x$.

### 解答 习题一

$$
\sqrt{2+x}-\sqrt2=\frac{x}{\sqrt{2+x}+\sqrt2}\sim\frac{x}{2\sqrt2}.
$$

故 $y\sim\frac{x^2}{2\sqrt2}$，由**定义**（高阶无穷小）知 $y$ 是 $x$ 的二阶无穷小量. $\blacksquare$

### 习题二

（习题 2.3-1-4）当 $x\to0$ 时，下列无穷小量是几阶无穷小量：$y=\ln\left(1+x^2\right)+x^3$.

### 解答 习题二

$\ln\left(1+x^2\right)\sim x^2$，而 $x^3=o\left(x^2\right)$. 由**定义**（高阶无穷小），$y\sim x^2$，是二阶无穷小量. $\blacksquare$

### 习题三

（习题 2.3-3-1）计算下列函数在指定点 $x_0$ 的微分：$f\left(x\right)=x^2\arcsin x,\ x_0=0$.

### 解答 习题三

$f'\left(x\right)=2x\arcsin x+\frac{x^2}{\sqrt{1-x^2}}$. $f'\left(0\right)=0$. 故 $\mathrm df\big|_{x_0=0}=0\cdot\mathrm dx=0$. $\blacksquare$

### 习题四

（习题 2.3-3-4）计算下列函数在指定点 $x_0$ 的微分：$f\left(x\right)=x\ln\left(1+x\right),\ x_0=0$.

### 解答 习题四

$f'\left(x\right)=\ln\left(1+x\right)+\frac{x}{1+x}$. $f'\left(0\right)=0$. 故 $\mathrm df\big|_{x_0=0}=0$. $\blacksquare$

### 习题五

（习题 2.3-4-2）求函数的微分：$f\left(x\right)=\ln\left(x+\sqrt{x^2+1}\right)$.

### 解答 习题五

$$
f'\left(x\right)=\frac1{x+\sqrt{x^2+1}}\cdot\left(1+\frac{x}{\sqrt{x^2+1}}\right)=\frac1{x+\sqrt{x^2+1}}\cdot\frac{\sqrt{x^2+1}+x}{\sqrt{x^2+1}}=\frac1{\sqrt{x^2+1}}.
$$

故 $\mathrm df=\frac1{\sqrt{x^2+1}}\mathrm dx$. $\blacksquare$

### 习题六

（习题 2.3-4-4）求函数的微分：$f\left(x\right)=\sqrt{1+x^2}+\sqrt x\sin x$.

### 解答 习题六

$$
f'\left(x\right)=\frac{x}{\sqrt{1+x^2}}+\frac1{2\sqrt x}\sin x+\sqrt x\cos x.
$$

故 $\mathrm df=\left(\frac{x}{\sqrt{1+x^2}}+\frac{\sin x}{2\sqrt x}+\sqrt x\cos x\right)\mathrm dx$. $\blacksquare$

### 习题七

（习题 2.3-5-1）填空：$\mathrm d\left(\ \ \right)=x^n\mathrm dx$.

### 解答 习题七

$\mathrm d\left(\frac{x^{n+1}}{n+1}\right)=x^n\mathrm dx\ \left(n\ne-1\right)$. $\blacksquare$

### 习题八

（习题 2.3-5-3）填空：$\mathrm d\left(\ \ \right)=\left(e^x+\sin2x\right)\mathrm dx$.

### 解答 习题八

$\mathrm d\left(e^x-\frac12\cos2x\right)=\left(e^x+\sin2x\right)\mathrm dx$. $\blacksquare$

### 习题九

（习题 2.3-5-5）填空：$\mathrm d\left(\ \ \right)=\frac{\sin x}{\cos x}\mathrm dx$.

### 解答 习题九

$\mathrm d\left(-\ln\left|\cos x\right|\right)=\frac{\sin x}{\cos x}\mathrm dx$. $\blacksquare$

### 习题十

（习题 2.3-6）计算 $\tan\left(\frac\pi4+0.01\right)$ 的近似值.

### 解答 习题十

令 $f\left(x\right)=\tan x$，取 $x_0=\frac\pi4$，$\Delta x=0.01$. $f'\left(x\right)=\sec^2x$，$f'\left(\frac\pi4\right)=2$. 由近似公式 $f\left(x_0+\Delta x\right)\approx f\left(x_0\right)+f'\left(x_0\right)\Delta x$，

$$
\tan\left(\frac\pi4+0.01\right)\approx\tan\frac\pi4+2\times0.01=1+0.02=1.02.
$$

$\blacksquare$
