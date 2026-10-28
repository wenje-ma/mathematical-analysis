# week12

> **Theorem 5.1 (Parametric Differentiation Formula)**<br>If $x=\varphi\left(t\right)$, $y=\psi\left(t\right)$ are differentiable at $t_0$ with $\varphi'\left(t_0\right)\ne0$, then $\frac{\mathrm dy}{\mathrm dx}=\frac{\psi'\left(t\right)}{\varphi'\left(t\right)}$.

---

## 2.5-1-2

Find $\frac{\mathrm dy}{\mathrm dx}$ for: $\begin{cases}x=t\ln t,\\y=e^t.\end{cases}$

### Solution 2.5-1-2

$\frac{\mathrm dx}{\mathrm dt}=\ln t+1$, $\frac{\mathrm dy}{\mathrm dt}=e^t$. By **Theorem 5.1 (Parametric Differentiation Formula)**,

$$
\frac{\mathrm dy}{\mathrm dx}=\frac{e^t}{\ln t+1}.
$$

$\blacksquare$

---

## 2.5-1-4

Find $\frac{\mathrm dy}{\mathrm dx}$ for: $\begin{cases}x=\cos^4t,\\y=\sin^4t.\end{cases}$

### Solution 2.5-1-4

$\frac{\mathrm dx}{\mathrm dt}=-4\cos^3t\sin t$, $\frac{\mathrm dy}{\mathrm dt}=4\sin^3t\cos t$. By **Theorem 5.1 (Parametric Differentiation Formula)**,

$$
\frac{\mathrm dy}{\mathrm dx}=\frac{4\sin^3t\cos t}{-4\cos^3t\sin t}=-\tan^2t.
$$

$\blacksquare$

---

## 2.5-3

The curve is given by $\begin{cases}x=1-t^2,\\y=t-t^2.\end{cases}$ Find the tangent lines at $t=1$ and $t=\frac{\sqrt2}2$.

### Solution 2.5-3

$\frac{\mathrm dx}{\mathrm dt}=-2t$, $\frac{\mathrm dy}{\mathrm dt}=1-2t$, $\frac{\mathrm dy}{\mathrm dx}=\frac{1-2t}{-2t}=\frac{2t-1}{2t}$.

At $t=1$: $x=0$, $y=0$, slope $k=\frac{2-1}{2}=\frac12$. Tangent: $y=\frac12x$.

At $t=\frac{\sqrt2}2$: $x=1-\frac12=\frac12$, $y=\frac{\sqrt2}2-\frac12=\frac{\sqrt2-1}2$, slope $k=\frac{\sqrt2-1}{\sqrt2}=1-\frac{\sqrt2}2$. Tangent:

$$
y-\frac{\sqrt2-1}2=\left(1-\frac{\sqrt2}2\right)\left(x-\frac12\right).
$$

$\blacksquare$

---

## 2.5-4

Let $x=\varphi\left(t\right)$, $y=\psi\left(t\right)$ be differentiable at $t_0$ with $\varphi'\left(t_0\right)\ne0$. For $\Delta t\ne0$, set

$$
\Delta x=\varphi\left(t_0+\Delta t\right)-\varphi\left(t_0\right),\quad\Delta y=\psi\left(t_0+\Delta t\right)-\psi\left(t_0\right).
$$

Prove $\lim_{\Delta t\to0}\frac{\Delta y}{\Delta x}=\frac{\psi'\left(t_0\right)}{\varphi'\left(t_0\right)}$.

### Solution 2.5-4

$$
\frac{\Delta y}{\Delta x}=\frac{\psi\left(t_0+\Delta t\right)-\psi\left(t_0\right)}{\varphi\left(t_0+\Delta t\right)-\varphi\left(t_0\right)}=\frac{\frac{\psi\left(t_0+\Delta t\right)-\psi\left(t_0\right)}{\Delta t}}{\frac{\varphi\left(t_0+\Delta t\right)-\varphi\left(t_0\right)}{\Delta t}}.
$$

As $\Delta t\to0$, the numerator tends to $\psi'\left(t_0\right)$ and the denominator to $\varphi'\left(t_0\right)\ne0$. By arithmetic of limits,

$$
\lim_{\Delta t\to0}\frac{\Delta y}{\Delta x}=\frac{\psi'\left(t_0\right)}{\varphi'\left(t_0\right)}.
$$

$\blacksquare$
