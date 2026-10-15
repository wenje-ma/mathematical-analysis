# Assignment 21

> **Theorem 4.1** (Decomposition of Rational Functions) Any rational function $\frac{P\left(x\right)}{Q\left(x\right)}$ can be decomposed into a polynomial plus a sum of partial fractions, where each partial fraction is of the form $\frac{A}{\left(x-a\right)^k}$ or $\frac{Bx+C}{\left(x^2+px+q\right)^m}$ ($p^2-4q<0$).

### Problem 1

(Problem 4.4-2) Find the indefinite integral $\displaystyle\int\frac{x^3}{x^2+x-6}\,\mathrm{d}x$.

### Solution to Problem 1

Since the degree of the numerator is higher than that of the denominator, first perform polynomial long division:
$$
\frac{x^3}{x^2+x-6}=x-1+\frac{7x-6}{x^2+x-6}.
$$

Factor the denominator:

$$
x^2+x-6=\left(x+3\right)\left(x-2\right).
$$

By **Theorem 4.1** (Decomposition of Rational Functions), set
$$
\frac{7x-6}{\left(x+3\right)\left(x-2\right)}=\frac{A}{x+3}+\frac{B}{x-2}.
$$

After bringing to a common denominator, compare numerators:

$$
7x-6=A\left(x-2\right)+B\left(x+3\right).
$$

Setting $x=-3$, we get $-27=-5A$, i.e. $A=\frac{27}{5}$. Setting $x=2$, we get $8=5B$, i.e. $B=\frac85$.

Hence
$$
\int\frac{x^3}{x^2+x-6}\,\mathrm{d}x=\int\left(x-1\right)\,\mathrm{d}x+\frac{27}{5}\int\frac{\mathrm{d}x}{x+3}+\frac85\int\frac{\mathrm{d}x}{x-2}=\frac{x^2}{2}-x+\frac{27}{5}\ln\left|x+3\right|+\frac85\ln\left|x-2\right|+C.
$$

$\blacksquare$
### Problem 2

(Problem 4.4-4) Find the indefinite integral $\displaystyle\int\frac{4x^2}{x\left(x+2\right)}\,\mathrm{d}x$.

### Solution to Problem 2

Simplify the integrand:
$$
\frac{4x^2}{x\left(x+2\right)}=\frac{4x}{x+2}=4-\frac{8}{x+2}.
$$

Hence
$$
\int\frac{4x^2}{x\left(x+2\right)}\,\mathrm{d}x=\int4\,\mathrm{d}x-8\int\frac{\mathrm{d}x}{x+2}=4x-8\ln\left|x+2\right|+C.
$$

$\blacksquare$
### Problem 3

(Problem 4.4-6) Find the indefinite integral $\displaystyle\int\frac{2x^2-5}{x^4-5x^2+6}\,\mathrm{d}x$.

### Solution to Problem 3

Factor the denominator:

$$
x^4-5x^2+6=\left(x^2-2\right)\left(x^2-3\right).
$$

By **Theorem 4.1** (Decomposition of Rational Functions), set
$$
\frac{2x^2-5}{\left(x^2-2\right)\left(x^2-3\right)}=\frac{A}{x^2-2}+\frac{B}{x^2-3}.
$$

After bringing to a common denominator, compare numerators:

$$
2x^2-5=A\left(x^2-3\right)+B\left(x^2-2\right)=\left(A+B\right)x^2+\left(-3A-2B\right).
$$

Comparing coefficients gives $A+B=2$, $-3A-2B=-5$. Solving gives $A=1$, $B=1$.

Hence
$$
\int\frac{2x^2-5}{x^4-5x^2+6}\,\mathrm{d}x=\int\frac{\mathrm{d}x}{x^2-2}+\int\frac{\mathrm{d}x}{x^2-3}=\frac{1}{2\sqrt2}\ln\left|\frac{x-\sqrt2}{x+\sqrt2}\right|+\frac{1}{2\sqrt3}\ln\left|\frac{x-\sqrt3}{x+\sqrt3}\right|+C.
$$

$\blacksquare$
### Problem 4

(Problem 4.4-8) Find the indefinite integral $\displaystyle\int\frac{x}{\left(x^2+2\right)^2}\,\mathrm{d}x$.

### Solution to Problem 4

Let $u=x^2+2$, then $\mathrm{d}u=2x\,\mathrm{d}x$. By the first substitution rule,
$$
\int\frac{x}{\left(x^2+2\right)^2}\,\mathrm{d}x=\frac12\int\frac{\mathrm{d}u}{u^2}=-\frac{1}{2u}+C=-\frac{1}{2\left(x^2+2\right)}+C.
$$

$\blacksquare$
### Problem 5

(Problem 4.4-10) Find the indefinite integral $\displaystyle\int\frac{x^3}{\left(x-1\right)^2}\,\mathrm{d}x$.

### Solution to Problem 5

Let $u=x-1$, then $x=u+1$, $\mathrm{d}x=\mathrm{d}u$. The integrand becomes
$$
\frac{\left(u+1\right)^3}{u^2}=\frac{u^3+3u^2+3u+1}{u^2}=u+3+\frac3u+\frac{1}{u^2}.
$$

Hence
$$
\int\frac{x^3}{\left(x-1\right)^2}\,\mathrm{d}x=\int\left(u+3+\frac3u+\frac{1}{u^2}\right)\mathrm{d}u=\frac{u^2}{2}+3u+3\ln\left|u\right|-\frac1u+C.
$$

Substituting back $u=x-1$:
$$
\int\frac{x^3}{\left(x-1\right)^2}\,\mathrm{d}x=\frac{\left(x-1\right)^2}{2}+3\left(x-1\right)+3\ln\left|x-1\right|-\frac{1}{x-1}+C.
$$

$\blacksquare$
### Problem 6

(Problem 4.4-12) Find the indefinite integral $\displaystyle\int\frac{e^t}{e^{2t}+5e^t+6}\,\mathrm{d}t$.

### Solution to Problem 6

Let $u=e^t$, then $\mathrm{d}u=e^t\,\mathrm{d}t$. The integral becomes
$$
\int\frac{\mathrm{d}u}{u^2+5u+6}=\int\frac{\mathrm{d}u}{\left(u+2\right)\left(u+3\right)}.
$$

By **Theorem 4.1** (Decomposition of Rational Functions), set $\frac{1}{\left(u+2\right)\left(u+3\right)}=\frac{A}{u+2}+\frac{B}{u+3}$. Setting $u=-2$, we get $A=1$. Setting $u=-3$, we get $B=-1$.

Hence
$$
\int\frac{e^t}{e^{2t}+5e^t+6}\,\mathrm{d}t=\ln\left|u+2\right|-\ln\left|u+3\right|+C=\ln\frac{e^t+2}{e^t+3}+C.
$$

$\blacksquare$
### Problem 7

(Problem 4.4-14) Find the indefinite integral $\displaystyle\int\frac{\mathrm{d}x}{\left(x^2+4\right)^2\left(x+1\right)}$.

### Solution to Problem 7

By **Theorem 4.1** (Decomposition of Rational Functions), set
$$
\frac{1}{\left(x^2+4\right)^2\left(x+1\right)}=\frac{A}{x+1}+\frac{Bx+C}{x^2+4}+\frac{Dx+E}{\left(x^2+4\right)^2}.
$$

After bringing to a common denominator, compare numerators:
$$
1=A\left(x^2+4\right)^2+\left(Bx+C\right)\left(x^2+4\right)\left(x+1\right)+\left(Dx+E\right)\left(x+1\right).
$$

Setting $x=-1$, we get $1=A\cdot25$, i.e. $A=\frac{1}{25}$. Comparing the coefficients of each power:

- $x^4$: $A+B=0$, hence $B=-\frac{1}{25}$.
- $x^3$: $B+C=0$, hence $C=\frac{1}{25}$.
- $x^2$: $8A+4B+C+D=0$, i.e. $\frac{8}{25}-\frac{4}{25}+\frac{1}{25}+D=0$, hence $D=-\frac15$.
- $x$: $4B+4C+D+E=0$, i.e. $-\frac{4}{25}+\frac{4}{25}-\frac15+E=0$, hence $E=\frac15$.

Hence
$$
\int\frac{\mathrm{d}x}{\left(x^2+4\right)^2\left(x+1\right)}=\frac{1}{25}\int\frac{\mathrm{d}x}{x+1}+\int\frac{-x/25+1/25}{x^2+4}\,\mathrm{d}x+\int\frac{-x/5+1/5}{\left(x^2+4\right)^2}\,\mathrm{d}x.
$$

Compute each term separately:
$$
\int\frac{\mathrm{d}x}{x+1}=\ln\left|x+1\right|,
$$
$$
\int\frac{x}{x^2+4}\,\mathrm{d}x=\frac12\ln\left(x^2+4\right),\int\frac{\mathrm{d}x}{x^2+4}=\frac12\arctan\frac{x}{2},
$$
$$
\int\frac{x}{\left(x^2+4\right)^2}\,\mathrm{d}x=-\frac{1}{2\left(x^2+4\right)},\int\frac{\mathrm{d}x}{\left(x^2+4\right)^2}=\frac{x}{8\left(x^2+4\right)}+\frac{1}{16}\arctan\frac{x}{2}.
$$

Combining gives
$$
\int\frac{\mathrm{d}x}{\left(x^2+4\right)^2\left(x+1\right)}=\frac{1}{25}\ln\left|x+1\right|-\frac{1}{50}\ln\left(x^2+4\right)+\frac{13}{400}\arctan\frac{x}{2}+\frac{x+4}{40\left(x^2+4\right)}+C.
$$

$\blacksquare$