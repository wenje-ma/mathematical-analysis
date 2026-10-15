# Assignment 20

> **Theorem 3.1** (Integration by Parts Formula) Let $u\left(x\right),v\left(x\right)$ be differentiable. Then
> $$
> \int u\left(x\right)\,\mathrm{d}v\left(x\right)=u\left(x\right)v\left(x\right)-\int v\left(x\right)\,\mathrm{d}u\left(x\right).
> $$
### Problem 1

(Problem 4.3-1-11) Find the indefinite integral $\displaystyle\int x\csc^2x\,\mathrm{d}x$.

### Solution to Problem 1

Let $u=x$, $\mathrm{d}v=\csc^2x\,\mathrm{d}x$, then $\mathrm{d}u=\mathrm{d}x$, $v=-\cot x$. By **Theorem 3.1** (Integration by Parts Formula),
$$
\int x\csc^2x\,\mathrm{d}x=-x\cot x+\int\cot x\,\mathrm{d}x=-x\cot x+\ln\left|\sin x\right|+C.
$$

$\blacksquare$
### Problem 2

(Problem 4.3-1-13) Find the indefinite integral $\displaystyle\int\sqrt{1+9x^2}\,\mathrm{d}x$.

### Solution to Problem 2

Let $u=\sqrt{1+9x^2}$, $\mathrm{d}v=\mathrm{d}x$, then
$$
\mathrm{d}u=\frac{9x}{\sqrt{1+9x^2}}\,\mathrm{d}x, v=x.
$$

By **Theorem 3.1** (Integration by Parts Formula),
$$
\int\sqrt{1+9x^2}\,\mathrm{d}x=x\sqrt{1+9x^2}-\int\frac{9x^2}{\sqrt{1+9x^2}}\,\mathrm{d}x.
$$

Rewrite the integrand:
$$
\frac{9x^2}{\sqrt{1+9x^2}}=\frac{9x^2+1-1}{\sqrt{1+9x^2}}=\sqrt{1+9x^2}-\frac{1}{\sqrt{1+9x^2}}.
$$

Substituting gives
$$
\int\sqrt{1+9x^2}\,\mathrm{d}x=x\sqrt{1+9x^2}-\int\sqrt{1+9x^2}\,\mathrm{d}x+\int\frac{\mathrm{d}x}{\sqrt{1+9x^2}}.
$$

Rearranging:
$$
2\int\sqrt{1+9x^2}\,\mathrm{d}x=x\sqrt{1+9x^2}+\int\frac{\mathrm{d}x}{\sqrt{1+9x^2}}.
$$

Moreover,
$$
\int\frac{\mathrm{d}x}{\sqrt{1+9x^2}}=\frac13\ln\left(3x+\sqrt{1+9x^2}\right)+C.
$$

Hence
$$
\int\sqrt{1+9x^2}\,\mathrm{d}x=\frac{x}{2}\sqrt{1+9x^2}+\frac16\ln\left(3x+\sqrt{1+9x^2}\right)+C.
$$

$\blacksquare$
### Problem 3

(Problem 4.3-1-14) Find the indefinite integral $\displaystyle\int\sec^3x\,\mathrm{d}x$.

### Solution to Problem 3

Let $u=\sec x$, $\mathrm{d}v=\sec^2x\,\mathrm{d}x$, then $\mathrm{d}u=\sec x\tan x\,\mathrm{d}x$, $v=\tan x$. By **Theorem 3.1** (Integration by Parts Formula),
$$
\int\sec^3x\,\mathrm{d}x=\sec x\tan x-\int\sec x\tan^2x\,\mathrm{d}x.
$$

Using $\tan^2x=\sec^2x-1$,
$$
\int\sec^3x\,\mathrm{d}x=\sec x\tan x-\int\sec x\left(\sec^2x-1\right)\,\mathrm{d}x=\sec x\tan x-\int\sec^3x\,\mathrm{d}x+\int\sec x\,\mathrm{d}x.
$$

Rearranging:
$$
2\int\sec^3x\,\mathrm{d}x=\sec x\tan x+\int\sec x\,\mathrm{d}x.
$$

Moreover,

$$
\displaystyle\int\sec x\,\mathrm{d}x=\ln\left|\sec x+\tan x\right|+C.
$$

Hence
$$
\int\sec^3x\,\mathrm{d}x=\frac12\left(\sec x\tan x+\ln\left|\sec x+\tan x\right|\right)+C.
$$

$\blacksquare$