# Assignment 14

> **Theorem 2.1** (Cauchy Mean Value Theorem) Let $y=f\left(x\right)$ and $y=g\left(x\right)$ be continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$, with $g'\left(x\right)\ne0$ ($a< x< b$). Then there exists a point $c\in\left(a,b\right)$ such that
> $$
> \frac{f\left(b\right)-f\left(a\right)}{g\left(b\right)-g\left(a\right)}=\frac{f'\left(c\right)}{g'\left(c\right)}.
> $$
> **Theorem 2.2** (L'Hôpital's Rule, $\frac00$ form) Let $y=f\left(x\right)$ and $y=g\left(x\right)$ be defined and differentiable on a punctured neighborhood of $a$, with $g'\left(x\right)\ne0$. Assume $\lim\limits_{x\to a}f\left(x\right)=\lim\limits_{x\to a}g\left(x\right)=0$, and that $\lim\limits_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ exists. Then
> $$
> \lim_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}.
> $$
> **Theorem 2.3** (L'Hôpital's Rule, $\frac{\infty}{\infty}$ form) Let $y=f\left(x\right)$ and $y=g\left(x\right)$ be defined and differentiable on a punctured neighborhood of $a$, with $g'\left(x\right)\ne0$. Assume
> $$
> \lim\limits_{x\to a}f\left(x\right)=\lim\limits_{x\to a}g\left(x\right)=\infty,
> $$
> and that $\lim\limits_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ exists. Then
> $$
> \lim_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}.
> $$
### Problem 1

(Problem 3.2-1) Find the limits of the following indeterminate forms:
(1) $\lim\limits_{x\to0}\frac{\ln\left(\cos ax\right)}{\ln\left(\cos bx\right)}$ ($a\ne0,b\ne0$);

(2) $\lim\limits_{x\to0}\frac{a^x-1}{x}$ ($a> 0$);

(3) $\lim\limits_{x\to0}\frac{\tan x-x}{x-\arcsin x}$;

(4) $\lim\limits_{x\to0+}x^x$;

(5) $\lim\limits_{x\to0+}x\ln x$;

(6) $\lim\limits_{x\to0+}\frac{\ln\left(\sin x\right)}{x^2}$;

(7) $\lim\limits_{x\to0+}\left(\sin x\right)^{\sin x}$.

### Solution to Problem 1

(1) This is a $\frac00$-type indeterminate form. By **Theorem 2.2** (L'Hôpital's Rule),
$$
\lim_{x\to0}\frac{\ln\left(\cos ax\right)}{\ln\left(\cos bx\right)}=\lim_{x\to0}\frac{\frac{-a\sin ax}{\cos ax}}{\frac{-b\sin bx}{\cos bx}}=\lim_{x\to0}\frac{a\tan ax}{b\tan bx}=\frac{a}{b}\cdot\frac{a}{b}=\frac{a^2}{b^2}.
$$

(2) This is a $\frac00$-type indeterminate form. By **Theorem 2.2** (L'Hôpital's Rule),
$$
\lim_{x\to0}\frac{a^x-1}{x}=\lim_{x\to0}\frac{a^x\ln a}{1}=\ln a.
$$

(3) This is a $\frac00$-type indeterminate form. By **Theorem 2.2** (L'Hôpital's Rule),
$$
\lim_{x\to0}\frac{\tan x-x}{x-\arcsin x}=\lim_{x\to0}\frac{\sec^2 x-1}{1-\frac{1}{\sqrt{1-x^2}}}.
$$

The numerator $\sec^2 x-1=\tan^2 x\sim x^2$ ($x\to0$). The denominator

$$
1-\frac{1}{\sqrt{1-x^2}}=\frac{\sqrt{1-x^2}-1}{\sqrt{1-x^2}}\sim-\frac{x^2}{2}\ \left(x\to0\right).
$$

Hence
$$
\lim_{x\to0}\frac{\tan x-x}{x-\arcsin x}=\frac{x^2}{-x^2/2}=-2.
$$

(4) This is a $0^0$-type indeterminate form. Let $y=x^x$, then $\ln y=x\ln x$. From (5), $\lim_{x\to0+}x\ln x=0$, so
$$
\lim_{x\to0+}x^x=e^0=1.
$$

(5) This is a $0\cdot\infty$-type indeterminate form. Rewrite it as a $\frac{\infty}{\infty}$ form and apply **Theorem 2.3** (L'Hôpital's Rule):
$$
\lim_{x\to0+}x\ln x=\lim_{x\to0+}\frac{\ln x}{1/x}=\lim_{x\to0+}\frac{1/x}{-1/x^2}=\lim_{x\to0+}\left(-x\right)=0.
$$

(6) This is a $\frac{\infty}{\infty}$-type indeterminate form. By **Theorem 2.3** (L'Hôpital's Rule),
$$
\lim_{x\to0+}\frac{\ln\left(\sin x\right)}{x^2}=\lim_{x\to0+}\frac{\cot x}{2x}=\lim_{x\to0+}\frac{\cos x}{2x\sin x}=+\infty.
$$

(7) This is a $0^0$-type indeterminate form. Let $y=\left(\sin x\right)^{\sin x}$, then $\ln y=\sin x\ln\left(\sin x\right)$. As $x\to0+$, $\sin x\to0$; by the result of (5) (replacing $x$ with $\sin x$),
$$
\lim_{x\to0+}\sin x\ln\left(\sin x\right)=0.
$$

Hence
$$
\lim_{x\to0+}\left(\sin x\right)^{\sin x}=e^0=1.
$$

$\blacksquare$
### Problem 2

(Problem 3.2-2) If $\lim\limits_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ does not exist, does it follow that $\lim\limits_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}$ also does not exist? Examine $f\left(x\right)=x\sin\frac1x$ and $g\left(x\right)=x^2$ as $x\to0$.

### Solution to Problem 2

No. Consider $f\left(x\right)=x\sin\frac1x$, $g\left(x\right)=x^2$, $x\to0$.

First,

$$
\lim\limits_{x\to0}\frac{f\left(x\right)}{g\left(x\right)}=\lim\limits_{x\to0}\frac{x\sin\left(1/x\right)}{x^2}=\lim\limits_{x\to0}\frac{\sin\left(1/x\right)}{x}.
$$

This limit does not exist (since $\sin\left(1/x\right)$ oscillates between $-1$ and $1$, while $1/x\to\infty$).

But this is not a good example, because we need to show that $\lim f/g$ exists while $\lim f'/g'$ does not. The corrected example is: take $f\left(x\right)=x^2\sin\frac1x$, $g\left(x\right)=x$. Then
$$
\lim_{x\to0}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to0}x\sin\frac1x=0.
$$

On the other hand,
$$
f'\left(x\right)=2x\sin\frac1x-\cos\frac1x, g'\left(x\right)=1.
$$

Thus
$$
\frac{f'\left(x\right)}{g'\left(x\right)}=2x\sin\frac1x-\cos\frac1x.
$$

As $x\to0$, $2x\sin\left(1/x\right)\to0$, but $\cos\left(1/x\right)$ oscillates and has no limit. Hence $\lim\limits_{x\to0}\frac{f'\left(x\right)}{g'\left(x\right)}$ does not exist.

This shows that when $\lim f'\left(x\right)/g'\left(x\right)$ does not exist, $\lim f\left(x\right)/g\left(x\right)$ may still exist. That is, the converse of L'Hôpital's rule does not hold. $\blacksquare$

### Problem 3

(Problem 3.2-4) Let $y=f\left(x\right)$ have a second derivative at $a$, and set
$$
T\left(x\right)=f\left(a\right)+f'\left(a\right)\Delta x+\frac{f''\left(a\right)}{2}\left(\Delta x\right)^2,
$$
where $\Delta x=x-a$. Prove that the function $g\left(x\right)=f\left(x\right)-T\left(x\right)$ satisfies

$$
\begin{aligned}
g\left(a\right)&=0,g'\left(a\right)=0,g''\left(a\right)=0,\
f\left(x\right)&=T\left(x\right)+o\left(\left(\Delta x\right)^2\right)\ \left(x\to a\right).
\end{aligned}
$$

### Solution to Problem 3

By the definition of $T\left(x\right)$, $T\left(a\right)=f\left(a\right)$,

$$
T'\left(x\right)=f'\left(a\right)+f''\left(a\right)\Delta x,
$$

$T''\left(x\right)=f''\left(a\right)$.

Computing gives
$$
g\left(a\right)=f\left(a\right)-T\left(a\right)=0,
$$
$$
g'\left(a\right)=f'\left(a\right)-T'\left(a\right)=f'\left(a\right)-f'\left(a\right)=0,
$$
$$
g''\left(a\right)=f''\left(a\right)-T''\left(a\right)=f''\left(a\right)-f''\left(a\right)=0.
$$

It remains to prove $g\left(x\right)=o\left(\left(\Delta x\right)^2\right)$, i.e. $\lim\limits_{\Delta x\to0}\frac{g\left(x\right)}{\left(\Delta x\right)^2}=0$.

This is a $\frac00$-type indeterminate form (since $g\left(a\right)=0$ and $g''\left(a\right)=0$ imply $g'\left(a\right)=0$). The theoretical basis of L'Hôpital's Rule (**Theorem 2.2**) is **Theorem 2.1** (Cauchy Mean Value Theorem). By **Theorem 2.2** (L'Hôpital's Rule),
$$
\lim_{\Delta x\to0}\frac{g\left(x\right)}{\left(\Delta x\right)^2}=\lim_{\Delta x\to0}\frac{g'\left(x\right)}{2\Delta x}.
$$

The right-hand side is still of $\frac00$ type (since $g'\left(a\right)=0$). Applying **Theorem 2.2** (L'Hôpital's Rule) once more,
$$
\lim_{\Delta x\to0}\frac{g'\left(x\right)}{2\Delta x}=\lim_{\Delta x\to0}\frac{g''\left(x\right)}{2}=\frac{g''\left(a\right)}{2}=0.
$$

Here we used the continuity of $g''$ at $a$ (which follows from $f$ having a second derivative at $a$). Hence $g\left(x\right)=o\left(\left(\Delta x\right)^2\right)$, i.e.
$$
f\left(x\right)=T\left(x\right)+o\left(\left(x-a\right)^2\right)\left(x\to a\right).
$$

$\blacksquare$
### Problem 4

(Problem 3.2-6) Let $c$ be a constant. For what value of $c$ do we have
$$
\lim_{x\to\infty}\left(\frac{x+c}{x-c}\right)^x=e^2.
$$
### Solution to Problem 4

This is a $1^\infty$-type indeterminate form. Let $y=\left(\frac{x+c}{x-c}\right)^x$, then
$$
\ln y=x\ln\frac{x+c}{x-c}=x\ln\left(1+\frac{2c}{x-c}\right).
$$

As $x\to\infty$, $\frac{2c}{x-c}\to0$; using the equivalent infinitesimal $\ln\left(1+t\right)\sim t$ ($t\to0$), we get
$$
\ln y\sim x\cdot\frac{2c}{x-c}=\frac{2cx}{x-c}\to2c\left(x\to\infty\right).
$$

It can also be verified by L'Hôpital's Rule: rewrite $\ln y$ as $\frac{\ln\left(\frac{x+c}{x-c}\right)}{1/x}$, which is of $\frac00$ type. By **Theorem 2.2** (L'Hôpital's Rule),
$$
\lim_{x\to\infty}\frac{\ln\left(\frac{x+c}{x-c}\right)}{1/x}=\lim_{x\to\infty}\frac{\frac{x-c}{x+c}\cdot\frac{\left(x-c\right)-\left(x+c\right)}{\left(x-c\right)^2}}{-1/x^2}=\lim_{x\to\infty}\frac{-2c}{x^2-c^2}\cdot\left(-x^2\right)=2c.
$$

Hence $\lim\limits_{x\to\infty}y=e^{2c}$. By the assumption $e^{2c}=e^2$, we get $2c=2$, i.e. $c=1$. $\blacksquare$
