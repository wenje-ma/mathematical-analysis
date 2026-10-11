# 作业 12

> **定理 5.1**（参变量函数求导公式）设 $x=\varphi\left(t\right),\ y=\psi\left(t\right)$ 在 $t_0$ 点可导，且 $\varphi'\left(t_0\right)\ne0$，则参变量函数的导数为 $\frac{\mathrm dy}{\mathrm dx}=\frac{\psi'\left(t\right)}{\varphi'\left(t\right)}$.

### 习题一

（习题 2.5-1-2）求下列参变量函数的导数 $\frac{\mathrm dy}{\mathrm dx}$：$\begin{cases}x=t\ln t,\\ y=e^t.\end{cases}$

### 解答 习题一

$\frac{\mathrm dx}{\mathrm dt}=\ln t+1$，$\frac{\mathrm dy}{\mathrm dt}=e^t$. 由**定理 5.1**，

$$
\frac{\mathrm dy}{\mathrm dx}=\frac{e^t}{\ln t+1}.
$$

$\blacksquare$

### 习题二

（习题 2.5-1-4）求下列参变量函数的导数 $\frac{\mathrm dy}{\mathrm dx}$：$\begin{cases}x=\cos^4t,\\ y=\sin^4t.\end{cases}$

### 解答 习题二

$\frac{\mathrm dx}{\mathrm dt}=-4\cos^3t\sin t$，$\frac{\mathrm dy}{\mathrm dt}=4\sin^3t\cos t$. 由**定理 5.1**，

$$
\frac{\mathrm dy}{\mathrm dx}=\frac{4\sin^3t\cos t}{-4\cos^3t\sin t}=-\tan^2t.
$$

$\blacksquare$

### 习题三

（习题 2.5-3）设曲线方程为 $\begin{cases}x=1-t^2,\\ y=t-t^2.\end{cases}$ 求在 $t=1$ 及 $t=\frac{\sqrt2}2$ 时曲线的切线方程.

### 解答 习题三

$\frac{\mathrm dx}{\mathrm dt}=-2t$，$\frac{\mathrm dy}{\mathrm dt}=1-2t$，$\frac{\mathrm dy}{\mathrm dx}=\frac{1-2t}{-2t}=\frac{2t-1}{2t}$.

当 $t=1$ 时：$x=0,\ y=0$，斜率 $k=\frac{2-1}{2}=\frac12$. 切线方程：$y=\frac12x$.

当 $t=\frac{\sqrt2}2$ 时：$x=1-\frac12=\frac12$，$y=\frac{\sqrt2}2-\frac12=\frac{\sqrt2-1}2$，斜率 $k=\frac{\sqrt2-1}{\sqrt2}=1-\frac{\sqrt2}2$. 切线方程：$y-\frac{\sqrt2-1}2=\left(1-\frac{\sqrt2}2\right)\left(x-\frac12\right)$. $\blacksquare$

### 习题四

（习题 2.5-4）设 $x=\varphi\left(t\right),\ y=\psi\left(t\right)$ 在 $t_0$ 点可导，且 $\varphi'\left(t_0\right)\ne0$. 令 $\Delta t\ne0$，$\Delta x=\varphi\left(t_0+\Delta t\right)-\varphi\left(t_0\right)$，$\Delta y=\psi\left(t_0+\Delta t\right)-\psi\left(t_0\right)$. 试证明 $\lim\limits_{\Delta t\to0}\frac{\Delta y}{\Delta x}=\frac{\psi'\left(t_0\right)}{\varphi'\left(t_0\right)}$.

### 解答 习题四

$$
\frac{\Delta y}{\Delta x}=\frac{\psi\left(t_0+\Delta t\right)-\psi\left(t_0\right)}{\varphi\left(t_0+\Delta t\right)-\varphi\left(t_0\right)}=\frac{\frac{\psi\left(t_0+\Delta t\right)-\psi\left(t_0\right)}{\Delta t}}{\frac{\varphi\left(t_0+\Delta t\right)-\varphi\left(t_0\right)}{\Delta t}}.
$$

当 $\Delta t\to0$ 时，分子趋于 $\psi'\left(t_0\right)$，分母趋于 $\varphi'\left(t_0\right)\ne0$. 由极限四则运算，

$$
\lim_{\Delta t\to0}\frac{\Delta y}{\Delta x}=\frac{\psi'\left(t_0\right)}{\varphi'\left(t_0\right)}.
$$

$\blacksquare$
