# Assignment 19

> **Theorem 2.1** (First Substitution Rule) Let $F'\left(u\right)=f\left(u\right)$, and let $u=\varphi\left(x\right)$ be differentiable. Then
> $$
> \int f\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm{d}x=F\left(\varphi\left(x\right)\right)+C.
> $$
> **Theorem 2.2** (Second Substitution Rule) Let $x=\varphi\left(t\right)$ be differentiable and have an inverse function, and suppose
> $$
> \displaystyle\int f\left(\varphi\left(t\right)\right)\varphi'\left(t\right)\,\mathrm{d}t=G\left(t\right)+C,
> $$
> then
> $$
> \int f\left(x\right)\,\mathrm{d}x=G\left(\varphi^{-1}\left(x\right)\right)+C.
> $$
### Problem 1

(Problem 4.2-1-2) Find the indefinite integral $\displaystyle\int\sqrt{2x+3}\,\mathrm{d}x$.

### Solution to Problem 1

Let $u=2x+3$, then $\mathrm{d}u=2\mathrm{d}x$, i.e. $\mathrm{d}x=\frac12\mathrm{d}u$. By **Theorem 2.1** (First Substitution Rule),
$$
\int\sqrt{2x+3}\,\mathrm{d}x=\frac12\int u^{1/2}\,\mathrm{d}u=\frac12\cdot\frac23u^{3/2}+C=\frac13\left(2x+3\right)^{3/2}+C.
$$

$\blacksquare$
### Problem 2

(Problem 4.2-1-4) Find the indefinite integral $\displaystyle\int\frac{\mathrm{d}x}{\left(x-1\right)^5}$.

### Solution to Problem 2

Let $u=x-1$, then $\mathrm{d}u=\mathrm{d}x$. By **Theorem 2.1** (First Substitution Rule),
$$
\int\frac{\mathrm{d}x}{\left(x-1\right)^5}=\int u^{-5}\,\mathrm{d}u=\frac{u^{-4}}{-4}+C=-\frac{1}{4\left(x-1\right)^4}+C.
$$

$\blacksquare$
### Problem 3

(Problem 4.2-1-6) Find the indefinite integral $\displaystyle\int\mathrm{sh}\,x\,\mathrm{d}x$.

### Solution to Problem 3

Since $\left(\mathrm{ch}\,x\right)'=\mathrm{sh}\,x$, and by the definition of the indefinite integral,
$$
\int\mathrm{sh}\,x\,\mathrm{d}x=\mathrm{ch}\,x+C.
$$

$\blacksquare$
### Problem 4

(Problem 4.2-1-8) Find the indefinite integral $\displaystyle\int\frac{\mathrm{d}x}{a^2+b^2x^2}$ ($a> 0,b> 0$).

### Solution to Problem 4

Rewrite the integrand:
$$
\frac{1}{a^2+b^2x^2}=\frac{1}{a^2}\cdot\frac{1}{1+\left(\frac{bx}{a}\right)^2}.
$$

Let $u=\frac{bx}{a}$, then $\mathrm{d}u=\frac{b}{a}\mathrm{d}x$, i.e. $\mathrm{d}x=\frac{a}{b}\mathrm{d}u$. By **Theorem 2.1** (First Substitution Rule),
$$
\int\frac{\mathrm{d}x}{a^2+b^2x^2}=\frac{1}{a^2}\cdot\frac{a}{b}\int\frac{\mathrm{d}u}{1+u^2}=\frac{1}{ab}\arctan u+C=\frac{1}{ab}\arctan\frac{bx}{a}+C.
$$

$\blacksquare$
### Problem 5

(Problem 4.2-1-10) Find the indefinite integral $\displaystyle\int\frac{\mathrm{d}x}{\sin x+\cos x}$.

### Solution to Problem 5

Using the trigonometric identity:
$$
\sin x+\cos x=\sqrt2\sin\left(x+\frac{\pi}{4}\right).
$$

Hence
$$
\int\frac{\mathrm{d}x}{\sin x+\cos x}=\frac{1}{\sqrt2}\int\frac{\mathrm{d}x}{\sin\left(x+\frac{\pi}{4}\right)}.
$$

Let $u=x+\frac{\pi}{4}$, then $\mathrm{d}u=\mathrm{d}x$. By **Theorem 2.1** (First Substitution Rule),
$$
\int\frac{\mathrm{d}u}{\sin u}=\int\csc u\,\mathrm{d}u=\ln\left|\csc u-\cot u\right|+C.
$$

Therefore
$$
\int\frac{\mathrm{d}x}{\sin x+\cos x}=\frac{1}{\sqrt2}\ln\left|\csc\left(x+\frac{\pi}{4}\right)-\cot\left(x+\frac{\pi}{4}\right)\right|+C.
$$

$\blacksquare$
### Problem 6

(Problem 4.2-2-1) Find the indefinite integral $\displaystyle\int\sqrt{a^2-x^2}\,\mathrm{d}x$ ($a> 0$).

### Solution to Problem 6

Let $x=a\sin t$ ($-\frac{\pi}{2}\le t\le\frac{\pi}{2}$), then $\mathrm{d}x=a\cos t\,\mathrm{d}t$, and $\sqrt{a^2-x^2}=a\cos t$. By **Theorem 2.2** (Second Substitution Rule),
$$
\int\sqrt{a^2-x^2}\,\mathrm{d}x=\int a\cos t\cdot a\cos t\,\mathrm{d}t=a^2\int\cos^2t\,\mathrm{d}t.
$$

Using $\cos^2t=\frac{1+\cos2t}{2}$,
$$
a^2\int\cos^2t\,\mathrm{d}t=\frac{a^2}{2}\left(t+\frac{\sin2t}{2}\right)+C=\frac{a^2}{2}\left(t+\sin t\cos t\right)+C.
$$

Substituting back $t=\arcsin\frac{x}{a}$, $\sin t=\frac{x}{a}$, $\cos t=\frac{\sqrt{a^2-x^2}}{a}$, we get
$$
\int\sqrt{a^2-x^2}\,\mathrm{d}x=\frac{a^2}{2}\arcsin\frac{x}{a}+\frac{x}{2}\sqrt{a^2-x^2}+C.
$$

$\blacksquare$
### Problem 7

(Problem 4.2-2-3) Find the indefinite integral $\displaystyle\int\frac{\mathrm{d}x}{\sqrt{x^2+a^2}}$ ($a> 0$).

### Solution to Problem 7

Let $x=a\tan t$ ($-\frac{\pi}{2}< t< \frac{\pi}{2}$), then $\mathrm{d}x=a\sec^2t\,\mathrm{d}t$, and $\sqrt{x^2+a^2}=a\sec t$. By **Theorem 2.2** (Second Substitution Rule),
$$
\int\frac{\mathrm{d}x}{\sqrt{x^2+a^2}}=\int\frac{a\sec^2t}{a\sec t}\,\mathrm{d}t=\int\sec t\,\mathrm{d}t=\ln\left|\sec t+\tan t\right|+C.
$$

Substituting back $\tan t=\frac{x}{a}$, $\sec t=\frac{\sqrt{x^2+a^2}}{a}$, we get
$$
\int\frac{\mathrm{d}x}{\sqrt{x^2+a^2}}=\ln\left|\frac{x+\sqrt{x^2+a^2}}{a}\right|+C=\ln\left(x+\sqrt{x^2+a^2}\right)+C'.
$$

$\blacksquare$
### Problem 8

(Problem 4.2-2-5) Find the indefinite integral $\displaystyle\int\sqrt{x^2-a^2}\,\mathrm{d}x$ ($a> 0$).

### Solution to Problem 8

Let $x=a\sec t$ ($0< t< \frac{\pi}{2}$), then $\mathrm{d}x=a\sec t\tan t\,\mathrm{d}t$, and $\sqrt{x^2-a^2}=a\tan t$. By **Theorem 2.2** (Second Substitution Rule),
$$
\int\sqrt{x^2-a^2}\,\mathrm{d}x=\int a\tan t\cdot a\sec t\tan t\,\mathrm{d}t=a^2\int\tan^2t\sec t\,\mathrm{d}t.
$$

Using $\tan^2t=\sec^2t-1$,
$$
a^2\int\left(\sec^3t-\sec t\right)\,\mathrm{d}t.
$$

By integration by parts we obtain

$$
\displaystyle\int\sec^3t\,\mathrm{d}t=\frac12\left(\sec t\tan t+\ln\left|\sec t+\tan t\right|\right)+C.
$$

Hence
$$
\int\sqrt{x^2-a^2}\,\mathrm{d}x=\frac{x}{2}\sqrt{x^2-a^2}-\frac{a^2}{2}\ln\left|x+\sqrt{x^2-a^2}\right|+C.
$$

$\blacksquare$
### Problem 9

(Problem 4.2-2-7) Find the indefinite integral $\displaystyle\int\frac{\mathrm{d}x}{x\sqrt{a^2-x^2}}$ ($a> 0$).

### Solution to Problem 9

Let $x=a\sin t$, then $\mathrm{d}x=a\cos t\,\mathrm{d}t$, $\sqrt{a^2-x^2}=a\cos t$. By **Theorem 2.2** (Second Substitution Rule),
$$
\int\frac{\mathrm{d}x}{x\sqrt{a^2-x^2}}=\int\frac{a\cos t\,\mathrm{d}t}{a\sin t\cdot a\cos t}=\frac1a\int\frac{\mathrm{d}t}{\sin t}=\frac1a\ln\left|\csc t-\cot t\right|+C.
$$

Substituting back $\csc t=\frac{a}{x}$, $\cot t=\frac{\sqrt{a^2-x^2}}{x}$, we get
$$
\int\frac{\mathrm{d}x}{x\sqrt{a^2-x^2}}=\frac1a\ln\left|\frac{a-\sqrt{a^2-x^2}}{x}\right|+C.
$$

$\blacksquare$
### Problem 10

(Problem 4.2-2-9) Find the indefinite integral $\displaystyle\int\sqrt{7+x-x^2}\,\mathrm{d}x$.

### Solution to Problem 10

Complete the square:
$$
7+x-x^2=\frac{29}{4}-\left(x-\frac12\right)^2.
$$

Let $u=x-\frac12$, then $\mathrm{d}u=\mathrm{d}x$. By **Theorem 2.1** (First Substitution Rule),
$$
\int\sqrt{7+x-x^2}\,\mathrm{d}x=\int\sqrt{\frac{29}{4}-u^2}\,\mathrm{d}u.
$$

By the result of Problem 6 (2-1),
$$
\int\sqrt{a^2-u^2}\,\mathrm{d}u=\frac{a^2}{2}\arcsin\frac{u}{a}+\frac{u}{2}\sqrt{a^2-u^2}+C,
$$

where $a=\frac{\sqrt{29}}{2}$. Substituting back gives
$$
\int\sqrt{7+x-x^2}\,\mathrm{d}x=\frac{29}{8}\arcsin\frac{2x-1}{\sqrt{29}}+\frac{2x-1}{4}\sqrt{7+x-x^2}+C.
$$

$\blacksquare$
### Problem 11

(Problem 4.2-2-11) Find the indefinite integral $\displaystyle\int\frac{\mathrm{d}x}{x^2\sqrt{x^2+a^2}}$ ($a> 0$).

### Solution to Problem 11

Let $x=a\tan t$, then $\mathrm{d}x=a\sec^2t\,\mathrm{d}t$, $\sqrt{x^2+a^2}=a\sec t$. By **Theorem 2.2** (Second Substitution Rule),
$$
\int\frac{\mathrm{d}x}{x^2\sqrt{x^2+a^2}}=\int\frac{a\sec^2t\,\mathrm{d}t}{a^2\tan^2t\cdot a\sec t}=\frac{1}{a^2}\int\frac{\sec t}{\tan^2t}\,\mathrm{d}t.
$$

Simplify:
$$
\frac{\sec t}{\tan^2t}=\frac{\cos t}{\sin^2t}.
$$

Let $u=\sin t$, then

$$
\mathrm{d}u=\cos t\,\mathrm{d}t,
$$
$$
\frac{1}{a^2}\int\frac{\cos t}{\sin^2t}\,\mathrm{d}t=\frac{1}{a^2}\int\frac{\mathrm{d}u}{u^2}=-\frac{1}{a^2u}+C.
$$

Substituting back $u=\sin t=\frac{x}{\sqrt{x^2+a^2}}$, we get
$$
\int\frac{\mathrm{d}x}{x^2\sqrt{x^2+a^2}}=-\frac{\sqrt{x^2+a^2}}{a^2x}+C.
$$

$\blacksquare$