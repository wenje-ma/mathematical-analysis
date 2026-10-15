# Assignment 47

> **Definition** (Convergence of a Singular Integral) Let $f\left(x\right)$ be defined on $\left(a,b\right]$ and integrable on every closed interval $\left[a+\eta,b\right]\subset\left(a,b\right]\left(\eta>0\right)$, where $a$ is a singular point of $f\left(x\right)$. If the limit $\lim_{\eta\to0+0}\int_{a+\eta}^b f\left(x\right)\,\mathrm{d}x$ exists, then the singular integral $\int_a^b f\left(x\right)\,\mathrm{d}x$ is said to converge, and this limit is defined to be its value; otherwise it is said to diverge. When the singular point is the right endpoint or an interior point of the interval, the definition is completely analogous.

> **Example 2.2** (The Singular $p$-Integral) The singular integral $\displaystyle\int_a^b\frac{\mathrm{d}x}{\left(x-a\right)^p}$ ($p>0$) converges when $p<1$ and diverges when $p\ge1$.

> **Definition** (Absolute and Conditional Convergence) Let $f\left(x\right)$ be defined on $\left(a,b\right]$ and let $a$ be a singular point. If $\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x$ converges, then $\int_a^b f\left(x\right)\,\mathrm{d}x$ is said to converge absolutely; if $\int_a^b f\left(x\right)\,\mathrm{d}x$ converges but $\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x$ diverges, then it is said to converge conditionally.

> **Definition** (Cauchy Principal Value) Let $f\left(x\right)$ be defined on $\left[a,b\right]\setminus\left\{c\right\}$, where $c\in\left(a,b\right)$ is its singular point. Suppose the limit
> $$
> \displaystyle I=\lim_{\eta\to0+0}\left[\int_a^{c-\eta}f\left(x\right)\,\mathrm{d}x+\int_{c+\eta}^b f\left(x\right)\,\mathrm{d}x\right]
> $$
> exists. Then the singular integral $\int_a^b f\left(x\right)\,\mathrm{d}x$ is said to converge in the sense of the Cauchy principal value, and the limit $I$ is called its Cauchy principal value, denoted $\mathrm{\left(CPV\right)}\int_a^b f\left(x\right)\,\mathrm{d}x$.

### Problem 1

(Problem 12.2-1-1) Determine the convergence of the singular integral $\displaystyle\int_0^1\ln x\,\mathrm{d}x$. If it converges, find its value.

### Solution to Problem 1

$x=0$ is a singular point. For any $\eta\in\left(0,1\right)$, integrating by parts gives

$$
\int_\eta^1\ln x\,\mathrm{d}x=\left[x\ln x-x\right]_\eta^1=-1-\eta\ln\eta+\eta.
$$

As $\eta\to0+0$, $\eta\ln\eta\to0$ and $\eta\to0$, so the right side tends to $-1$. By **Definition** (Convergence of a Singular Integral), this singular integral converges, and its value is $-1$. $\blacksquare$

### Problem 2

(Problem 12.2-1-3) Determine the convergence of the singular integral $\displaystyle\int_{-1}^1\frac{\mathrm{d}x}{\sqrt{1-x^2}}$. If it converges, find its value.

### Solution to Problem 2

Both $x=\pm1$ are singular points. Split the integral as $\int_{-1}^0+\int_0^1$ and discuss each separately. For any $\eta\in\left(0,1\right)$,

$$
\int_0^{1-\eta}\frac{\mathrm{d}x}{\sqrt{1-x^2}}=\left[\arcsin x\right]_0^{1-\eta}=\arcsin\left(1-\eta\right)\to\frac{\pi}{2}\left(\eta\to0+0\right),
$$

$$
\int_{-1+\eta}^0\frac{\mathrm{d}x}{\sqrt{1-x^2}}=\left[\arcsin x\right]_{-1+\eta}^0=-\arcsin\left(-1+\eta\right)\to\frac{\pi}{2}\left(\eta\to0+0\right).
$$

Both singular integrals converge, so by **Definition** (Convergence of a Singular Integral), the original singular integral converges, with value $\frac{\pi}{2}+\frac{\pi}{2}=\pi$. $\blacksquare$

### Problem 3

(Problem 12.2-1-5) Determine the convergence of the singular integral $\displaystyle\int_0^1\frac{\mathrm{d}x}{x\ln^2 x}$. If it converges, find its value.

### Solution to Problem 3

Both $x=0$ and $x=1$ are singular points. It suffices to consider near $x=1$. For any $\eta\in\left(0,\frac12\right)$, make the substitution $u=\ln x$ ($\mathrm{d}u=\frac{\mathrm{d}x}{x}$). We have

$$
\int_{1/2}^{1-\eta}\frac{\mathrm{d}x}{x\ln^2 x}=\int_{\ln\left(1/2\right)}^{\ln\left(1-\eta\right)}\frac{\mathrm{d}u}{u^2}
=\left[-\frac1u\right]_{\ln\left(1/2\right)}^{\ln\left(1-\eta\right)}
=-\frac1{\ln\left(1-\eta\right)}+\frac1{\ln\left(1/2\right)}.
$$

As $\eta\to0+0$, $\ln\left(1-\eta\right)\to0-0$, so $-\frac1{\ln\left(1-\eta\right)}\to+\infty$. By **Definition** (Convergence of a Singular Integral), this singular integral diverges. $\blacksquare$

### Problem 4

(Problem 12.2-2-1) Discuss the convergence of the improper integral $\displaystyle\int_0^{+\infty}\frac{\mathrm{d}x}{\sqrt x\,\left(1+x\right)}$.

### Solution to Problem 4

$x=0$ is a singular point, and the integration interval is also infinite, so discuss the two segments separately.

Near $x=0$, $\frac1{\sqrt x\,\left(1+x\right)}\sim\frac1{\sqrt x}$, and by **Example 2.2** (The Singular $p$-Integral), $\int_0^1\frac{\mathrm{d}x}{\sqrt x}$ converges ($p=\frac12<1$). As $x\to+\infty$, $\frac1{\sqrt x\,\left(1+x\right)}\sim\frac1{x^{3/2}}$, and by **Example 1.2** (The $p$-Integral) of Chapter 12, $\int_1^{+\infty}\frac{\mathrm{d}x}{x^{3/2}}$ converges ($p=\frac32>1$). Both segments converge, so the original improper integral converges.

In fact its value is: make the substitution $t=\sqrt x$ ($\mathrm{d}x=2t\,\mathrm{d}t$),

$$
\int_0^{+\infty}\frac{\mathrm{d}x}{\sqrt x\,\left(1+x\right)}=\int_0^{+\infty}\frac{2t\,\mathrm{d}t}{t\left(1+t^2\right)}=2\int_0^{+\infty}\frac{\mathrm{d}t}{1+t^2}=2\cdot\frac{\pi}{2}=\pi.

$$

$\blacksquare$
### Problem 5

(Problem 12.2-2-3) Discuss the convergence of the improper integral $\displaystyle\int_0^{+\infty}\frac{\mathrm{d}x}{x^p+x^q}$.

### Solution to Problem 5

$x=0$ is a singular point, and the integration interval is also infinite, so discuss the two segments separately.

Near $x=0$, $x^p+x^q\sim x^{\min\left(p,q\right)}$, so the integrand is of the same order as $\frac1{x^{\min\left(p,q\right)}}$. By **Example 2.2** (The Singular $p$-Integral), this endpoint converges if and only if $\min\left(p,q\right)<1$.

As $x\to+\infty$, $x^p+x^q\sim x^{\max\left(p,q\right)}$, so the integrand is of the same order as $\frac1{x^{\max\left(p,q\right)}}$. By **Example 1.2** (The $p$-Integral) of Chapter 12, this endpoint converges if and only if $\max\left(p,q\right)>1$.

Both segments must converge simultaneously, so the original improper integral converges if and only if

$$
\min\left(p,q\right)<1<\max\left(p,q\right)\ \left(\text{即}p,q\text{中一个小于}1\text{, 另一个大于}1\right),
$$

and all other cases diverge. $\blacksquare$

### Problem 6

(Problem 12.2-2-5) Discuss the convergence of the improper integral $\displaystyle\int_0^{\pi/2}\frac{\mathrm{d}x}{\sin^2 x\cos^2 x}$.

### Solution to Problem 6

Both $x=0$ and $x=\frac{\pi}{2}$ are singular points. Near $x=0$, $\sin x\sim x$ and $\cos x\sim1$, so the integrand is of the same order as $\frac1{x^2}$. By **Example 2.2** (The Singular $p$-Integral), $\int_0^{\pi/4}\frac{\mathrm{d}x}{x^2}$ diverges ($p=2>1$). Hence the original improper integral diverges. $\blacksquare$

### Problem 7

(Problem 12.2-2-7) Discuss the convergence of the improper integral $\displaystyle\int_0^1 x^p\left(1-x\right)^q\,\mathrm{d}x$ ($p>0,q>0$).

### Solution to Problem 7

Both $x=0$ and $x=1$ may be singular points. Near $x=0$, $x^p\left(1-x\right)^q\sim x^p$, and by **Example 2.2** (The Singular $p$-Integral), this endpoint converges if and only if $p>-1$; since the hypothesis is $p>0$, it always converges. Near $x=1$, $x^p\left(1-x\right)^q\sim\left(1-x\right)^q$, and this endpoint converges if and only if $q>-1$; since the hypothesis is $q>0$, it also always converges. Both segments converge simultaneously, so the original improper integral converges for all $p>0,q>0$. $\blacksquare$

### Problem 8

(Problem 12.2-3) Let $f\left(x\right)$ be defined on $\left(a,b\right]$ and integrable on every interval $\left[a+\eta,b\right]\left(\eta>0\right)$. Prove that if $\displaystyle\int_a^b f^2\left(x\right)\,\mathrm{d}x$ converges, then $\displaystyle\int_a^b f\left(x\right)\,\mathrm{d}x$ converges absolutely. Also ask: if $\displaystyle\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x$ converges, does it necessarily follow that $\displaystyle\int_a^b f^2\left(x\right)\,\mathrm{d}x$ converges?

### Solution to Problem 8

From the inequality $2\left| t\right|\le1+t^2$ (i.e. $\left(\left| t\right|-1\right)^2\ge0$), we get

$$
\left| f\left(x\right)\right|\le\frac12+\frac{f^2\left(x\right)}2.
$$

For any $\eta>0$, integrating over $\left[a+\eta,b\right]$ gives

$$
\int_{a+\eta}^b\left| f\left(x\right)\right|\,\mathrm{d}x\le\frac{b-a}{2}+\frac12\int_{a+\eta}^b f^2\left(x\right)\,\mathrm{d}x\le\frac{b-a}{2}+\frac12\int_a^b f^2\left(x\right)\,\mathrm{d}x<+\infty.
$$

The right side is independent of $\eta$ and bounded, so $\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x$ converges. By **Definition** (Absolute and Conditional Convergence), $\int_a^b f\left(x\right)\,\mathrm{d}x$ converges absolutely.

The converse is not true. Counterexample: take $f\left(x\right)=\frac1{\sqrt x}$ on $\left(0,1\right]$. By **Example 2.2** (The Singular $p$-Integral), $\int_0^1\frac{\mathrm{d}x}{\sqrt x}$ converges ($p=\frac12<1$), i.e. $\int_0^1\left| f\left(x\right)\right|\,\mathrm{d}x$ converges; but $\int_0^1 f^2\left(x\right)\,\mathrm{d}x=\int_0^1\frac{\mathrm{d}x}{x}$ diverges ($p=1$). Hence the convergence of $\int\left| f\right|$ does not guarantee the convergence of $\int f^2$. $\blacksquare$

### Problem 9

(Problem 12.2-4-1) Determine whether the improper integral $\displaystyle\int_0^2\frac{\mathrm{d}x}{x-1}$ converges in the sense of the Cauchy principal value. If it converges, find its Cauchy principal value.

### Solution to Problem 9

$x=1$ is a singular point. First consider it in the ordinary sense:

$$
\int_0^{1-\eta}\frac{\mathrm{d}x}{x-1}=\left[\ln\left| x-1\right|\right]_0^{1-\eta}=\ln\eta-\ln1=\ln\eta\to-\infty\left(\eta\to0+0\right),
$$

so it diverges in the ordinary sense.

Now consider the Cauchy principal value. By **Definition** (Cauchy Principal Value),

$$
\begin{aligned}
\mathrm{\left(CPV\right)}\int_0^2\frac{\mathrm{d}x}{x-1}
&=\lim_{\eta\to0+0}\left(\int_0^{1-\eta}\frac{\mathrm{d}x}{x-1}+\int_{1+\eta}^2\frac{\mathrm{d}x}{x-1}\right)\\
&=\lim_{\eta\to0+0}\left(\left(\ln\eta-\ln1\right)+\left(\ln1-\ln\eta\right)\right)=0.
\end{aligned}
$$

Hence this integral converges in the sense of the Cauchy principal value, and its Cauchy principal value is $0$. $\blacksquare$

### Problem 10

(Problem 12.2-4-2) Determine whether the improper integral $\displaystyle\int_{1/2}^2\frac{\mathrm{d}x}{x\ln x}$ converges in the sense of the Cauchy principal value. If it converges, find its Cauchy principal value.

### Solution to Problem 10

$x=1$ is a singular point. An antiderivative of the integrand is $\ln\left|\ln x\right|$. By **Definition** (Cauchy Principal Value),

$$
\begin{aligned}
\mathrm{\left(CPV\right)}\int_{1/2}^2\frac{\mathrm{d}x}{x\ln x}
&=\lim_{\eta\to0+0}\left(\int_{1/2}^{1-\eta}\frac{\mathrm{d}x}{x\ln x}+\int_{1+\eta}^2\frac{\mathrm{d}x}{x\ln x}\right)\\
&=\lim_{\eta\to0+0}\left[\ln\left|\ln\left(1-\eta\right)\right|-\ln\left|\ln\frac12\right|+\ln\left|\ln2\right|-\ln\left|\ln\left(1+\eta\right)\right|\right]\\
&=\lim_{\eta\to0+0}\ln\frac{-\ln\left(1-\eta\right)}{\ln\left(1+\eta\right)}.
\end{aligned}
$$

As $\eta\to0+0$, $-\ln\left(1-\eta\right)\sim\eta$ and $\ln\left(1+\eta\right)\sim\eta$, so the ratio tends to $1$ and the logarithm tends to $\ln1=0$. Therefore this integral converges in the sense of the Cauchy principal value, and its Cauchy principal value is $0$. $\blacksquare$
