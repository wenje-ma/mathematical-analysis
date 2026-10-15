# Assignment 12

> **Theorem 5.1** (Derivative Formula for Parametric Functions) Let $x=\varphi\left(t\right),y=\psi\left(t\right)$ be differentiable at the point $t_0$, with $\varphi'\left(t_0\right)\ne0$. Then the derivative of the parametric function is $\frac{\mathrm dy}{\mathrm dx}=\frac{\psi'\left(t\right)}{\varphi'\left(t\right)}$.

### Problem 1

(Problem 2.5-1-2) Find the derivative $\frac{\mathrm dy}{\mathrm dx}$ of the following parametric function: $\begin{cases}x=t\ln t,\y=e^t.\end{cases}$

### Solution to Problem 1

$\frac{\mathrm dx}{\mathrm dt}=\ln t+1$, $\frac{\mathrm dy}{\mathrm dt}=e^t$. By **Theorem 5.1**,

$$
\frac{\mathrm dy}{\mathrm dx}=\frac{e^t}{\ln t+1}.

$$

$\blacksquare$
### Problem 2

(Problem 2.5-1-4) Find the derivative $\frac{\mathrm dy}{\mathrm dx}$ of the following parametric function: $\begin{cases}x=\cos^4t,\y=\sin^4t.\end{cases}$

### Solution to Problem 2

$\frac{\mathrm dx}{\mathrm dt}=-4\cos^3t\sin t$, $\frac{\mathrm dy}{\mathrm dt}=4\sin^3t\cos t$. By **Theorem 5.1**,

$$
\frac{\mathrm dy}{\mathrm dx}=\frac{4\sin^3t\cos t}{-4\cos^3t\sin t}=-\tan^2t.

$$

$\blacksquare$
### Problem 3

(Problem 2.5-3) Let the curve be given by $\begin{cases}x=1-t^2,\y=t-t^2.\end{cases}$ Find the tangent-line equations of the curve at $t=1$ and at $t=\frac{\sqrt2}2$.

### Solution to Problem 3

$\frac{\mathrm dx}{\mathrm dt}=-2t$, $\frac{\mathrm dy}{\mathrm dt}=1-2t$, $\frac{\mathrm dy}{\mathrm dx}=\frac{1-2t}{-2t}=\frac{2t-1}{2t}$.

When $t=1$: $x=0,y=0$, slope $k=\frac{2-1}{2}=\frac12$. Tangent line: $y=\frac12x$.

When $t=\frac{\sqrt2}2$: $x=1-\frac12=\frac12$, $y=\frac{\sqrt2}2-\frac12=\frac{\sqrt2-1}2$, slope $k=\frac{\sqrt2-1}{\sqrt2}=1-\frac{\sqrt2}2$. Tangent line:

$$
y-\frac{\sqrt2-1}2=\left(1-\frac{\sqrt2}2\right)\left(x-\frac12\right).
$$

$\blacksquare$

### Problem 4

(Problem 2.5-4) Let $x=\varphi\left(t\right),y=\psi\left(t\right)$ be differentiable at the point $t_0$, with $\varphi'\left(t_0\right)\ne0$. Set $\Delta t\ne0$,

$$
\begin{aligned}
\Delta x&=\varphi\left(t_0+\Delta t\right)-\varphi\left(t_0\right),\
\Delta y&=\psi\left(t_0+\Delta t\right)-\psi\left(t_0\right).
\end{aligned}
$$

Prove that $\lim\limits_{\Delta t\to0}\frac{\Delta y}{\Delta x}=\frac{\psi'\left(t_0\right)}{\varphi'\left(t_0\right)}$.

### Solution to Problem 4

$$
\frac{\Delta y}{\Delta x}=\frac{\psi\left(t_0+\Delta t\right)-\psi\left(t_0\right)}{\varphi\left(t_0+\Delta t\right)-\varphi\left(t_0\right)}=\frac{\frac{\psi\left(t_0+\Delta t\right)-\psi\left(t_0\right)}{\Delta t}}{\frac{\varphi\left(t_0+\Delta t\right)-\varphi\left(t_0\right)}{\Delta t}}.
$$

As $\Delta t\to0$, the numerator tends to $\psi'\left(t_0\right)$ and the denominator tends to $\varphi'\left(t_0\right)\ne0$. By the arithmetic of limits,

$$
\lim_{\Delta t\to0}\frac{\Delta y}{\Delta x}=\frac{\psi'\left(t_0\right)}{\varphi'\left(t_0\right)}.

$$

$\blacksquare$