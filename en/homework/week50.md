# Assignment 50

> **Theorem 4.3** (The Weierstrass Test) Let $f\left(x,y\right)$ be defined on $\left(a,b\right]\times Y$, where $a$ is a singular point. If there exists $F\left(x\right)$ such that (i)
> $$
> \left| f\left(x,y\right)\right|\le F\left(x\right)\left(\forall x\in\left(a,b\right],y\in Y\right);
> $$
> (ii) the singular integral $\int_a^b F\left(x\right)\,\mathrm{d}x$ converges, then the parameter-dependent singular integral $\int_a^b f\left(x,y\right)\,\mathrm{d}x$ converges uniformly in $y\in Y$.

> **Theorem 4.7** (Interchanging the Order of Integration) Let $f\left(x,y\right)$ be continuous and of fixed sign on $\left(a,b\right]\times\left[c,d\right]$, and suppose $\int_a^b f\left(x,y\right)\,\mathrm{d}x$ converges uniformly in $y\in\left[c,d\right]$. Then
> $$
> \displaystyle\int_c^d\mathrm{d}y\int_a^b f\left(x,y\right)\,\mathrm{d}x=\int_a^b\mathrm{d}x\int_c^d f\left(x,y\right)\,\mathrm{d}y.
> $$

### Problem 1

(Problem 12.5-1-1) Discuss the uniform convergence of the parameter-dependent singular integral $\displaystyle\int_0^1\frac{\sin x}{x^\alpha}\,\mathrm{d}x$ on (i) $\alpha\le\alpha_0< 2$; (ii) $\alpha< 2$.

### Solution to Problem 1

The singular point is $x=0$. Since $\sin x\sim x\left(x\to0\right)$, the integrand near the singular point is of the same order as $x^{1-\alpha}$.

(i) When $\alpha\le\alpha_0< 2$, for $x\in\left(0,1\right]$ we have

$$
\left|\frac{\sin x}{x^\alpha}\right|\le\frac{x}{x^\alpha}=x^{1-\alpha}\le x^{1-\alpha_0}\ \left(\text{因}x\in\left(0,1\right)\text{时}x^t\text{关于}t\text{递减}\right).
$$

And $1-\alpha_0> -1$, so $\int_0^1 x^{1-\alpha_0}\,\mathrm{d}x$ converges. By **Theorem 4.3** (The Weierstrass Test), this singular integral converges uniformly on $\alpha\le\alpha_0< 2$.

(ii) When $\alpha< 2$ (i.e. on the open interval $\left(0,2\right)$), it does not converge uniformly. Indeed, take $\alpha_n=2-\frac1n\to2-0$. Then

$$
\int_0^{1/n}\frac{\sin x}{x^{\alpha_n}}\,\mathrm{d}x\sim\int_0^{1/n}x^{1-\alpha_n}\,\mathrm{d}x=\int_0^{1/n}x^{-1+1/n}\,\mathrm{d}x=n\cdot\left(\frac1n\right)^{1/n}\to n\cdot\frac1n=1,
$$

which does not tend to $0$ as $n\to\infty$, so the Cauchy condition for uniform convergence is not satisfied. That is, it does not converge uniformly on $\alpha< 2$. $\blacksquare$

### Problem 2

(Problem 12.5-1-2) Discuss the uniform convergence of the parameter-dependent singular integral $\displaystyle\int_0^1 x^{p-1}\,\mathrm{d}x$ on (i) $p\ge p_0> 0$; (ii) $p> 0$.

### Solution to Problem 2

The singular point is $x=0$.

(i) When $p\ge p_0> 0$, for $x\in\left(0,1\right]$ we have $x^{p-1}\le x^{p_0-1}$ (since $x^t$ decreases in $t$ when $x\in\left(0,1\right)$). And $p_0> 0$, so $\int_0^1 x^{p_0-1}\,\mathrm{d}x=\frac1{p_0}$ converges. By **Theorem 4.3** (The Weierstrass Test), this singular integral converges uniformly on $p\ge p_0> 0$.

(ii) When $p> 0$ (i.e. on the open interval $\left(0,+\infty\right)$), it does not converge uniformly. Indeed, take $p_n=\frac1n\to0+0$. Then

$$
\int_0^{1/n}x^{p_n-1}\,\mathrm{d}x=\frac{1}{p_n}\cdot\left(\frac1n\right)^{p_n}=n\cdot\left(\frac1n\right)^{1/n}\to1,
$$

which does not tend to $0$ as $n\to\infty$, so the Cauchy condition for uniform convergence is not satisfied. That is, it does not converge uniformly on $p> 0$. $\blacksquare$

### Problem 3

(Problem 12.5-2-1) Find the value of the integral $\displaystyle\int_0^1\frac{x^b-x^a}{\ln x}\,\mathrm{d}x$ ($a> -1,b> -1$).

### Solution to Problem 3

Noting that $\frac{x^b-x^a}{\ln x}=\displaystyle\int_a^b x^y\,\mathrm{d}y$

$$
\left(\text{因 }\int_a^b x^y\,\mathrm{d}y=\left[\frac{x^y}{\ln x}\right]_a^b=\frac{x^b-x^a}{\ln x}\right),
$$

we have

$$
I=\int_0^1\mathrm{d}x\int_a^b x^y\,\mathrm{d}y.
$$

The integrand $x^y\ge0$ is continuous on $\left(0,1\right]\times\left[a,b\right]$, and $\int_0^1 x^y\,\mathrm{d}x$ converges uniformly in $y\in\left[a,b\right]$ (since $x^y\le x^{\min\left(a,b\right)}$, while $\min\left(a,b\right)> -1$ and $\int_0^1 x^{\min\left(a,b\right)}\,\mathrm{d}x$ converges). By **Theorem 4.7** (Interchanging the Order of Integration),

$$
I=\int_a^b\mathrm{d}y\int_0^1 x^y\,\mathrm{d}x=\int_a^b\frac{\mathrm{d}y}{y+1}=\ln\frac{1+b}{1+a}.

$$

$\blacksquare$