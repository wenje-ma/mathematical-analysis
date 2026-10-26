# Assignment 51

> **Definition** (The Gamma Function)
> $$
> \displaystyle\Gamma\left(\alpha\right)=\int_0^{+\infty}t^{\alpha-1}e^{-t}\,\mathrm{d}t\left(\alpha> 0\right).
> $$
> It satisfies the recurrence $\Gamma\left(\alpha+1\right)=\alpha\Gamma\left(\alpha\right)$, $\Gamma\left(1\right)=1$, $\Gamma\left(n+1\right)=n!$, and $\Gamma\!\left(\frac12\right)=\sqrt\pi$.

> **Definition** (The Beta Function)
> $$
> \displaystyle \Beta\left(p,q\right)=\int_0^1 t^{p-1}\left(1-t\right)^{q-1}\,\mathrm{d}t\left(p,q> 0\right),
> $$
> and we have $\Beta\left(p,q\right)=\frac{\Gamma\left(p\right)\Gamma\left(q\right)}{\Gamma\left(p+q\right)}$.

> **Proposition** (Integral Forms of Gamma and Beta)
> $$
> \displaystyle\int_0^{+\infty}\frac{x^{a-1}}{\left(1+x\right)^{a+b}}\,\mathrm{d}x=\Beta\left(a,b\right),\
> \displaystyle\int_0^{\pi/2}\sin^m x\cos^n x\,\mathrm{d}x=\frac12 \Beta\!\left(\frac{m+1}{2},\frac{n+1}{2}\right).
> $$

### Problem 1

(Problem 12.6-1-1) Using the Gamma and Beta functions, compute the integral $\displaystyle\int_0^{+\infty}\frac{4\sqrt x}{\left(1+x\right)^2}\,\mathrm{d}x$.

### Solution to Problem 1

By **Proposition** (Integral Forms of Gamma and Beta),

$$
\displaystyle\int_0^{+\infty}\frac{x^{a-1}}{\left(1+x\right)^{a+b}}\,\mathrm{d}x=\Beta\left(a,b\right).
$$

Here the integrand is $\frac{x^{1/2}}{\left(1+x\right)^2}$, i.e. $a-1=\frac12$ and $a+b=2$, so $a=\frac32$ and $b=\frac12$. Hence

$$
\int_0^{+\infty}\frac{\sqrt x}{\left(1+x\right)^2}\,\mathrm{d}x=\Beta\!\left(\frac32,\frac12\right)=\frac{\Gamma\left(\frac32\right)\Gamma\left(\frac12\right)}{\Gamma\left(2\right)}.
$$

By **Definition** (The Gamma Function), $\Gamma\left(\frac32\right)=\frac12\Gamma\left(\frac12\right)=\frac{\sqrt\pi}{2}$, $\Gamma\left(\frac12\right)=\sqrt\pi$, and $\Gamma\left(2\right)=1$. Hence

$$
\int_0^{+\infty}\frac{4\sqrt x}{\left(1+x\right)^2}\,\mathrm{d}x=4\cdot\frac{\frac{\sqrt\pi}{2}\cdot\sqrt\pi}{1}=4\cdot\frac{\pi}{2}=2\pi.

$$

$\blacksquare$
### Problem 2

(Problem 12.6-1-2) Using the Gamma and Beta functions, compute the integral $\displaystyle\int_0^{+\infty}x^{-1/2}e^{-\alpha x}\,\mathrm{d}x$ ($\alpha> 0$).

### Solution to Problem 2

Make the substitution $t=\alpha x$ ($\mathrm{d}x=\frac{\mathrm{d}t}{\alpha}$). Then

$$
\int_0^{+\infty}x^{-1/2}e^{-\alpha x}\,\mathrm{d}x=\int_0^{+\infty}\left(\frac t\alpha\right)^{-1/2}e^{-t}\frac{\mathrm{d}t}{\alpha}=\alpha^{-1/2}\int_0^{+\infty}t^{-1/2}e^{-t}\,\mathrm{d}t.
$$

By **Definition** (The Gamma Function), the integral on the right is $\Gamma\!\left(\frac12\right)=\sqrt\pi$. Hence

$$
\int_0^{+\infty}x^{-1/2}e^{-\alpha x}\,\mathrm{d}x=\frac{\sqrt\pi}{\sqrt\alpha}=\sqrt{\frac{\pi}{\alpha}}.

$$

$\blacksquare$
### Problem 3

(Problem 12.6-1-3) Using the Gamma and Beta functions, compute the integral $\displaystyle\int_0^1 x^8\sqrt{1-x^3}\,\mathrm{d}x$.

### Solution to Problem 3

Make the substitution $t=x^3$ ($x=t^{1/3}$, $\mathrm{d}x=\frac13 t^{-2/3}\mathrm{d}t$). Then $x^8=t^{8/3}$ and $\sqrt{1-x^3}=\sqrt{1-t}$. Hence

$$
\int_0^1 x^8\sqrt{1-x^3}\,\mathrm{d}x=\frac13\int_0^1 t^{8/3}\left(1-t\right)^{1/2}t^{-2/3}\,\mathrm{d}t=\frac13\int_0^1 t^2\left(1-t\right)^{1/2}\,\mathrm{d}t=\frac13 \Beta\!\left(3,\frac32\right).
$$

By **Definition** (The Beta Function), $\Beta\left(3,\frac32\right)=\frac{\Gamma\left(3\right)\Gamma\left(\frac32\right)}{\Gamma\left(\frac92\right)}$. Computing: $\Gamma\left(3\right)=2$, $\Gamma\left(\frac32\right)=\frac{\sqrt\pi}{2}$, $\Gamma\left(\frac92\right)=\frac{105}{16}\sqrt\pi$. Hence

$$
\Beta\!\left(3,\frac32\right)=\frac{2\cdot\frac{\sqrt\pi}{2}}{\frac{105}{16}\sqrt\pi}=\frac{16}{105},
$$

and therefore the original integral is $=\frac13\cdot\frac{16}{105}=\frac{16}{315}$. $\blacksquare$

### Problem 4

(Problem 12.6-1-4) Using the Gamma and Beta functions, compute the integral $\displaystyle\int_0^{\pi/2}\sin^6 x\cos^4 x\,\mathrm{d}x$.

### Solution to Problem 4

By **Proposition** (Integral Forms of Gamma and Beta),

$$
\int_0^{\pi/2}\sin^6 x\cos^4 x\,\mathrm{d}x=\frac12 \Beta\!\left(\frac72,\frac52\right)=\frac12\cdot\frac{\Gamma\left(\frac72\right)\Gamma\left(\frac52\right)}{\Gamma\left(6\right)}.
$$

By **Definition** (The Gamma Function), $\Gamma\left(\frac72\right)=\frac{15}{8}\sqrt\pi$, $\Gamma\left(\frac52\right)=\frac{3}{4}\sqrt\pi$, and $\Gamma\left(6\right)=120$. Hence

$$
\text{原积分}=\frac12\cdot\frac{\frac{15}{8}\sqrt\pi\cdot\frac34\sqrt\pi}{120}=\frac12\cdot\frac{45\pi}{3840}=\frac{3\pi}{512}.

$$

$\blacksquare$
### Problem 5

(Problem 12.6-1-9) Using the Gamma and Beta functions, compute the integral $\displaystyle\int_0^1\frac{\mathrm{d}x}{\sqrt{1-x^4}}$ (hint: let $t=x^4$).

### Solution to Problem 5

Make the substitution $t=x^4$ ($x=t^{1/4}$, $\mathrm{d}x=\frac14 t^{-3/4}\mathrm{d}t$). Then

$$
\int_0^1\frac{\mathrm{d}x}{\sqrt{1-x^4}}=\frac14\int_0^1 t^{-3/4}\left(1-t\right)^{-1/2}\,\mathrm{d}t=\frac14 \Beta\!\left(\frac14,\frac12\right).
$$

By **Definition** (The Beta Function), $\Beta\left(\frac14,\frac12\right)=\frac{\Gamma\left(\frac14\right)\Gamma\left(\frac12\right)}{\Gamma\left(\frac34\right)}$. Hence the original integral is $=\frac14 \Beta\!\left(\frac14,\frac12\right)$. $\blacksquare$

### Problem 6

(Problem 12.6-1-10) Using the Gamma and Beta functions, compute the integral $\displaystyle\int_0^{+\infty}\frac{\mathrm{d}x}{1+x^3}$ (hint: let $t=\frac{1}{1+x^3}$).

### Solution to Problem 6

In the formula of **Proposition** (Integral Forms of Gamma and Beta)

$$
\int_0^{+\infty}\frac{x^{a-1}}{\left(1+x\right)^{a+b}}\,\mathrm{d}x=\Beta\left(a,b\right)
$$

replace the denominator by $1+x^3$. Make the substitution $u=x^3$ ($x=u^{1/3}$, $\mathrm{d}x=\frac13 u^{-2/3}\mathrm{d}u$). Then

$$
\int_0^{+\infty}\frac{\mathrm{d}x}{1+x^3}=\frac13\int_0^{+\infty}\frac{u^{-2/3}}{1+u}\,\mathrm{d}u=\frac13 \Beta\!\left(\frac13,\frac23\right).
$$

By **Definition** (The Beta Function),

$$
\Beta\left(\frac13,\frac23\right)=\Gamma\left(\frac13\right)\Gamma\left(\frac23\right),
$$

so the original integral is $=\frac13\Gamma\!\left(\frac23\right)\Gamma\!\left(\frac13\right)$. $\blacksquare$

### Problem 7

(Problem 12.6-2) Prove that $\Gamma\left(\alpha\right)$, as a parameter-dependent improper integral, does not converge uniformly on $\left(0,+\infty\right)$.

### Solution to Problem 7

$\Gamma\left(\alpha\right)=\displaystyle\int_0^{+\infty}t^{\alpha-1}e^{-t}\,\mathrm{d}t$ is split as

$$
\displaystyle\int_0^1 t^{\alpha-1}e^{-t}\,\mathrm{d}t+\int_1^{+\infty}t^{\alpha-1}e^{-t}\,\mathrm{d}t.
$$

The second integral converges uniformly on any $\left[\alpha_0,+\infty\right)$, but this does not affect uniformity on $\left(0,+\infty\right)$.

The key is the first integral $\displaystyle\int_0^1 t^{\alpha-1}e^{-t}\,\mathrm{d}t$. Take $\alpha_n=\frac1n\to0+0$. Then

$$
\int_0^{1/n}t^{\alpha_n-1}e^{-t}\,\mathrm{d}t\ge e^{-1/n}\int_0^{1/n}t^{-1+1/n}\,\mathrm{d}t=e^{-1/n}\cdot n\cdot\left(\frac1n\right)^{1/n}\to1\left(n\to\infty\right).
$$

This lower bound does not tend to $0$, so the Cauchy condition for uniform convergence is not satisfied. Therefore $\Gamma\left(\alpha\right)$ does not converge uniformly on $\left(0,+\infty\right)$. $\blacksquare$
