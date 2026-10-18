# Assignment 49

> **Theorem 4.3** (The Weierstrass Test) Let $f\left(x,y\right)$ be defined on $\left[a,+\infty\right)\times Y$. If there exists $F\left(x\right)$ such that (i)
> $$
> \left| f\left(x,y\right)\right|\le F\left(x\right)\left(\forall x\in\left[a,+\infty\right),y\in Y\right);
> $$
> (ii) $\int_a^{+\infty}F\left(x\right)\,\mathrm{d}x$ converges, then the improper integral $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ converges uniformly in $y\in Y$.

> **Theorem 4.4** (Abel's Test) Let $f\left(x,y\right),g\left(x,y\right)$ be defined on $\left[a,+\infty\right)\times Y$. If (i) $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ converges uniformly in $y\in Y$; (ii) $g\left(x,y\right)$ is monotone in $x$ and uniformly bounded in $y\in Y$, then $\int_a^{+\infty}f\left(x,y\right)g\left(x,y\right)\,\mathrm{d}x$ converges uniformly in $y\in Y$.

> **Theorem 4.7** (Interchanging the Order of Integration) Let $f\left(x,y\right)$ be continuous on $\left[a,+\infty\right)\times\left[c,d\right]$, and suppose $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ converges uniformly in $y\in\left[c,d\right]$. Then
> $$
> \displaystyle\int_c^d\mathrm{d}y\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x=\int_a^{+\infty}\mathrm{d}x\int_c^d f\left(x,y\right)\,\mathrm{d}y.
> $$

> **Theorem 4.8** (Differentiation Under the Integral Sign) Let $f\left(x,y\right)$ and $f_y\left(x,y\right)$ be continuous on $\left[a,+\infty\right)\times\left[c,d\right]$, suppose $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ converges and $\int_a^{+\infty}f_y\left(x,y\right)\,\mathrm{d}x$ converges uniformly in $y\in\left[c,d\right]$. Then $I\left(y\right)=\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ is differentiable on $\left[c,d\right]$, and $I'\left(y\right)=\int_a^{+\infty}f_y\left(x,y\right)\,\mathrm{d}x$.

> **Example 4.5** (The Dirichlet Integral) $\displaystyle\int_0^{+\infty}\frac{\sin x}{x}\,\mathrm{d}x=\frac{\pi}{2}$. In general,
> $$
> \displaystyle\int_0^{+\infty}\frac{\sin\left(kx\right)}{x}\,\mathrm{d}x=\frac{\pi}{2}\operatorname{sgn}\left(k\right).
> $$

### Problem 1

(Problem 12.4-1-1) Discuss the uniform convergence of the parameter-dependent improper integral $\displaystyle\int_0^{+\infty}e^{-\alpha x^2}\,\mathrm{d}x$ on $\alpha\in\left[\alpha_0,+\infty\right)$ ($\alpha_0>0$).

### Solution to Problem 1

For any $x\ge0$ and $\alpha\ge\alpha_0$, we have $e^{-\alpha x^2}\le e^{-\alpha_0 x^2}$. And $\int_0^{+\infty}e^{-\alpha_0 x^2}\,\mathrm{d}x=\frac12\sqrt{\frac{\pi}{\alpha_0}}$ converges. By **Theorem 4.3** (The Weierstrass Test), this improper integral converges uniformly on $\left[\alpha_0,+\infty\right)$. $\blacksquare$

### Problem 2

(Problem 12.4-1-3) Discuss the uniform convergence of the parameter-dependent improper integral $\displaystyle\int_1^{+\infty}e^{-xy}\frac{\cos x}{x}\,\mathrm{d}x$ on $y\in\left[0,+\infty\right)$.

### Solution to Problem 2

Write the integrand as $\frac{\cos x}{x}\cdot e^{-xy}$. First, $\int_1^{+\infty}\frac{\cos x}{x}\,\mathrm{d}x$ converges (by **Theorem 1.6** of Chapter 12, Dirichlet's Test), and it does not involve the parameter $y$, so it converges uniformly in $y\in\left[0,+\infty\right)$. Second, $e^{-xy}$ is monotonically decreasing in $x$, and $0<e^{-xy}\le1$ is uniformly bounded in $y\in\left[0,+\infty\right)$. By **Theorem 4.4** (Abel's Test), $\int_1^{+\infty}e^{-xy}\frac{\cos x}{x}\,\mathrm{d}x$ converges uniformly on $\left[0,+\infty\right)$. $\blacksquare$

### Problem 3

(Problem 12.4-1-5) Discuss the uniform convergence of the parameter-dependent improper integral $\displaystyle\int_0^{+\infty}e^{-x^2y^2}\cos x\,\mathrm{d}x$ on $y\in\left[y_0,+\infty\right)$ ($y_0>0$).

### Solution to Problem 3

For any $x\ge0$ and $y\ge y_0$, we have

$$
\left| e^{-x^2y^2}\cos x\right|\le e^{-x^2y^2}\le e^{-x^2y_0^2}.
$$

And $\int_0^{+\infty}e^{-x^2y_0^2}\,\mathrm{d}x=\frac{1}{2y_0}\sqrt\pi$ converges. By **Theorem 4.3** (The Weierstrass Test), this improper integral converges uniformly on $\left[y_0,+\infty\right)$. $\blacksquare$

### Problem 4

(Problem 12.4-2-1) Find the value of the integral $\displaystyle\int_0^{+\infty}\frac{e^{-ax}-e^{-bx}}{x}\,\mathrm{d}x$ ($0<a<b$).

### Solution to Problem 4

Noting that $\frac{e^{-ax}-e^{-bx}}{x}=\int_a^b e^{-xy}\,\mathrm{d}y$, we have

$$
I=\int_0^{+\infty}\mathrm{d}x\int_a^b e^{-xy}\,\mathrm{d}y.
$$

The integrand $e^{-xy}$ is continuous and nonnegative on $\left[0,+\infty\right)\times\left[a,b\right]$, and $\int_0^{+\infty}e^{-xy}\,\mathrm{d}x$ converges uniformly in $y\in\left[a,b\right]$ (since $e^{-xy}\le e^{-ax}$, and $\int_0^{+\infty}e^{-ax}\,\mathrm{d}x=1/a$ converges, by **Theorem 4.3**). By **Theorem 4.7** (Interchanging the Order of Integration),

$$
I=\int_a^b\mathrm{d}y\int_0^{+\infty}e^{-xy}\,\mathrm{d}x=\int_a^b\frac{\mathrm{d}y}{y}=\ln\frac ba.

$$

$\blacksquare$
### Problem 5

(Problem 12.4-2-2) Find the value of the integral

$$
\displaystyle\int_0^{+\infty}\frac{\sin\left(\alpha x\right)\cos\left(\beta x\right)}{x}\,\mathrm{d}x\ \left(\alpha>0,\beta>0\right)
$$

.

### Solution to Problem 5

From the trigonometric identity

$$
\sin\left(\alpha x\right)\cos\left(\beta x\right)=\frac12\left[\sin\left(\left(\alpha+\beta\right)x\right)+\sin\left(\left(\alpha-\beta\right)x\right)\right],
$$

we get

$$
I=\frac12\int_0^{+\infty}\frac{\sin\left(\left(\alpha+\beta\right)x\right)}{x}\,\mathrm{d}x+\frac12\int_0^{+\infty}\frac{\sin\left(\left(\alpha-\beta\right)x\right)}{x}\,\mathrm{d}x.
$$

By **Example 4.5** (The Dirichlet Integral),

$$
\int_0^{+\infty}\frac{\sin\left(kx\right)}{x}\,\mathrm{d}x=\frac{\pi}{2}\operatorname{sgn}\left(k\right).
$$

Since $\alpha+\beta>0$, the first term is $\frac12\cdot\frac{\pi}{2}=\frac{\pi}{4}$. The second term depends on the sign of $\alpha-\beta$:

$$
I=
\begin{cases}
\frac12\cdot\frac{\pi}{4}+\frac12\cdot\left(-\frac{\pi}{4}\right)=0,&\alpha<\beta,\\[4pt\right]
\frac{\pi}{4}+0=\frac{\pi}{4},&\alpha=\beta,\\[4pt\right]
\frac{\pi}{4}+\frac12\cdot\frac{\pi}{2}=\frac{\pi}{2},&\alpha>\beta.
\end{cases}

$$

$\blacksquare$
### Problem 6

(Problem 12.4-2-4) Find the value of the integral $\displaystyle\int_0^{+\infty}\frac{1-\cos\left(\alpha x\right)}{x}e^{-x}\,\mathrm{d}x$.

### Solution to Problem 6

Let

$$
I\left(\alpha\right)=\int_0^{+\infty}\frac{1-\cos\left(\alpha x\right)}{x}e^{-x}\,\mathrm{d}x.
$$

The partial derivative of the integrand with respect to $\alpha$ is $e^{-x}\sin\left(\alpha x\right)$, which is continuous on $\left[0,+\infty\right)\times\left[0,+\infty\right)$, and $\int_0^{+\infty}e^{-x}\sin\left(\alpha x\right)\,\mathrm{d}x$ converges uniformly in $\alpha$ (since $\left| e^{-x}\sin\left(\alpha x\right)\right|\le e^{-x}$, and $\int_0^{+\infty}e^{-x}\,\mathrm{d}x$ converges, by **Theorem 4.3**). By **Theorem 4.8** (Differentiation Under the Integral Sign),

$$
I'\left(\alpha\right)=\int_0^{+\infty}e^{-x}\sin\left(\alpha x\right)\,\mathrm{d}x.
$$

By Problem 12.1-3 of Chapter 12 (taking the parameter as $1$),

$$
\int_0^{+\infty}e^{-x}\sin\left(\alpha x\right)\,\mathrm{d}x=\frac{\alpha}{1+\alpha^2}.
$$

Hence

$$
I\left(\alpha\right)=\int_0^\alpha\frac{t}{1+t^2}\,\mathrm{d}t=\frac12\ln\left(1+\alpha^2\right)+C.
$$

Moreover, $I\left(0\right)=0$, so $C=0$, and thus

$$
I\left(\alpha\right)=\frac12\ln\left(1+\alpha^2\right).

$$

$\blacksquare$
### Problem 7

(Problem 12.4-5) Prove Dini's theorem for series of functions: Let $u_n\left(x\right)$ be continuous on $\left[a,b\right]$ ($n=1,2,\cdots$), and suppose $u_n\left(x\right)\ge0\left(\forall x\in\left[a,b\right]\right)$. Suppose further that $S\left(x\right)=\displaystyle\sum_{n=1}^\infty u_n\left(x\right)$ converges at every point $x\in\left[a,b\right]$, and that $S\left(x\right)$ is continuous on $\left[a,b\right]$. Then $\displaystyle\sum_{n=1}^\infty u_n\left(x\right)$ converges uniformly on $\left[a,b\right]$.

### Solution to Problem 7

Let $S_N\left(x\right)=\sum_{n=1}^N u_n\left(x\right)$,

$$
R_N\left(x\right)=S\left(x\right)-S_N\left(x\right)=\sum_{n=N+1}^\infty u_n\left(x\right).
$$

Since $u_n\ge0$, we have $R_N\left(x\right)\ge0$, and $R_N\left(x\right)$ is monotonically decreasing in $N$; moreover, $R_N\left(x\right)$ is the difference of two continuous functions, so it is continuous on $\left[a,b\right]$. By pointwise convergence, $R_N\left(x\right)\to0\left(N\to\infty\right)$ for each $x$.

By contradiction. Suppose $\sum u_n$ does not converge uniformly on $\left[a,b\right]$. Then there exist $\epsilon_0>0$, a sequence $N_k\to\infty$, and points $x_k\in\left[a,b\right]$ such that $R_{N_k}\left(x_k\right)\ge\epsilon_0$. By the Bolzano–Weierstrass theorem, $\left\{x_k\right\}$ has a subsequence converging to some $x_0\in\left[a,b\right]$; relabeling, still write $x_k\to x_0$.

For any fixed $m$, whenever $N_k\ge m$, since $R_N\left(x\right)$ is monotonically decreasing in $N$, we have $R_{N_k}\left(x_k\right)\le R_m\left(x_k\right)$. Letting $k\to\infty$, by the continuity of $R_m\left(x\right)$,

$$
\epsilon_0\le\lim_{k\to\infty}R_{N_k}\left(x_k\right)\le\lim_{k\to\infty}R_m\left(x_k\right)=R_m\left(x_0\right).
$$

This holds for all $m$. But by pointwise convergence, $R_m\left(x_0\right)\to0\left(m\to\infty\right)$, a contradiction. Hence $\sum u_n\left(x\right)$ converges uniformly on $\left[a,b\right]$. $\blacksquare$
