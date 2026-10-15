# Assignment 48

> **Theorem 3.3** (Differentiation Under the Integral Sign) Let $f\left(x,y\right)$ and $f_y\left(x,y\right)$ be continuous on $\left[a,b\right]\times\left[c,d\right]$. Then the function $I\left(y\right)=\displaystyle\int_a^b f\left(x,y\right)\,\mathrm{d}x$ is differentiable on $\left[c,d\right]$, and
> $$
> I'\left(y\right)=\int_a^b f_y\left(x,y\right)\,\mathrm{d}x, \forall\,y\in\left[c,d\right].
> $$
> When the limits of integration also depend on $y$, i.e. $I\left(y\right)=\displaystyle\int_{a\left(y\right)}^{b\left(y\right)}f\left(x,y\right)\,\mathrm{d}x$, the boundary terms are added by the Newton–Leibniz formula:
> $$
> I'\left(y\right)=f\left(b\left(y\right),y\right)b'\left(y\right)-f\left(a\left(y\right),y\right)a'\left(y\right)+\int_{a\left(y\right)}^{b\left(y\right)}f_y\left(x,y\right)\,\mathrm{d}x.
> $$
### Problem 1

(Problem 12.3-2-5) Find the derivative of the function $\displaystyle I\left(y\right)=\int_{\sin y}^{\cos y}e^{y\sqrt{1-x^2}}\,\mathrm{d}x$ ($y\in\left[0,\frac{\pi}{2}\right]$).

### Solution to Problem 1

The integrand $f\left(x,y\right)=e^{y\sqrt{1-x^2}}$ and its partial derivative $f_y=\sqrt{1-x^2}\,e^{y\sqrt{1-x^2}}$ with respect to $y$ are both continuous, and the limits $a\left(y\right)=\sin y$, $b\left(y\right)=\cos y$ are both differentiable. By **Theorem 3.3** (Differentiation Under the Integral Sign),

$$
I'\left(y\right)=f\left(\cos y,y\right)\cdot\left(-\sin y\right)-f\left(\sin y,y\right)\cdot\cos y+\int_{\sin y}^{\cos y}\sqrt{1-x^2}\,e^{y\sqrt{1-x^2}}\,\mathrm{d}x.
$$

When $y\in\left[0,\pi/2\right]$, $\sqrt{1-\cos^2 y}=\sin y$ and $\sqrt{1-\sin^2 y}=\cos y$. Substituting,

$$
I'\left(y\right)=\int_{\sin y}^{\cos y}\sqrt{1-x^2}\,e^{y\sqrt{1-x^2}}\,\mathrm{d}x-e^{y\sin y}\sin y-e^{y\cos y}\cos y.

$$

$\blacksquare$
### Problem 2

(Problem 12.3-2-6) Find the derivative of the function $\displaystyle I\left(y\right)=\int_0^{x/y}y\sin\left(xy\right)\,\mathrm{d}x$ ($y>0$, with $x$ a fixed constant).

### Solution to Problem 2

The integrand is $f\left(x,y\right)=y\sin\left(xy\right)$,

$$
f_y=\sin\left(xy\right)+xy\cos\left(xy\right),
$$

and the upper limit is $a\left(y\right)=x/y$, $a'\left(y\right)=-x/y^2$. By **Theorem 3.3** (Differentiation Under the Integral Sign),

$$
I'\left(y\right)=y\sin\!\left(y\cdot\frac{x}{y}\right)\!\left(-\frac{x}{y^2}\right)+\int_0^{x/y}\left[\sin\left(xy\right)+xy\cos\left(xy\right)\right]\,\mathrm{d}x.
$$

Noting that

$$
\frac{\mathrm{d}}{\mathrm{d}x}\left[x\sin\left(xy\right)\right]=\sin\left(xy\right)+xy\cos\left(xy\right),
$$

we have

$$
\int_0^{x/y}\left[\sin\left(xy\right)+xy\cos\left(xy\right)\right]\,\mathrm{d}x=\left[x\sin\left(xy\right)\right]_0^{x/y}=\frac{x}{y}\sin x.
$$

The boundary term is $-\frac{x}{y}\sin x$, and the two cancel, so

$$
I'\left(y\right)=-\frac{x}{y}\sin x+\frac{x}{y}\sin x=0.

$$

$\blacksquare$
### Problem 3

(Problem 12.3-2-7) Find the derivative of the function

$$
\displaystyle I\left(y\right)=\int_0^{y^2}\sin\left(x^2+y^2\right)\,\mathrm{d}x
$$

.

### Solution to Problem 3

The integrand is $f\left(x,y\right)=\sin\left(x^2+y^2\right)$, $f_y=2y\cos\left(x^2+y^2\right)$, and the upper limit is $b\left(y\right)=y^2$, $b'\left(y\right)=2y$. By **Theorem 3.3** (Differentiation Under the Integral Sign),

$$
I'\left(y\right)=\sin\left(\left(y^2\right)^2+y^2\right)\cdot 2y+\int_0^{y^2}2y\cos\left(x^2+y^2\right)\,\mathrm{d}x,
$$

i.e.

$$
I'\left(y\right)=\int_0^{y^2}2y\cos\left(x^2+y^2\right)\,\mathrm{d}x+2y\sin\left(y^4+y^2\right).

$$

$\blacksquare$
### Problem 4

(Problem 12.3-2-8) Find the derivative of the function

$$
\displaystyle I\left(y\right)=\int_0^y\frac{\ln\left(1+xy\right)}{x}\,\mathrm{d}x\ \left(y>0\right)
$$

.

### Solution to Problem 4

The integrand is $f\left(x,y\right)=\frac{\ln\left(1+xy\right)}{x}$, $f_y=\frac{1}{1+xy}$, and the upper limit is $b\left(y\right)=y$, $b'\left(y\right)=1$. By **Theorem 3.3** (Differentiation Under the Integral Sign),

$$
I'\left(y\right)=\frac{\ln\left(1+y^2\right)}{y}\cdot 1+\int_0^y\frac{\mathrm{d}x}{1+xy},
$$

i.e.

$$
I'\left(y\right)=\frac{\ln\left(1+y^2\right)}{y}+\int_0^y\frac{\mathrm{d}x}{1+xy}.

$$

$\blacksquare$
### Problem 5

(Problem 12.3-4-1) Using the method of differentiation under the integral sign, compute the definite integral

$$
\displaystyle I\left(r\right)=\int_0^\pi\ln\left(1-2r\cos x+r^2\right)\,\mathrm{d}x\ \left(\left|r\right|<1\right).
$$

### Solution to Problem 5

For any $r\in\left(-1,1\right)$, the integrand and its partial derivative with respect to $r$ are continuous on $\left[0,\pi\right]\times\left(-1,1\right)$. By **Theorem 3.3** (Differentiation Under the Integral Sign),

$$
I'\left(r\right)=\int_0^\pi\frac{-2\cos x+2r}{1-2r\cos x+r^2}\,\mathrm{d}x.
$$

Write $D=1-2r\cos x+r^2$. Then

$$
\frac{2r-2\cos x}{D}=\frac1r-\frac{1-r^2}{rD},
$$

which is verified by multiplying both sides by $r$. Hence

$$
I'\left(r\right)=\frac{\pi}{r}-\frac{1-r^2}{r}\int_0^\pi\frac{\mathrm{d}x}{1-2r\cos x+r^2}.
$$

Making the substitution $t=\tan\frac{x}{2}$, we obtain the standard integral

$$
\int_0^\pi\frac{\mathrm{d}x}{1-2r\cos x+r^2}=\frac{\pi}{1-r^2}\left(\left|r\right|<1\right).
$$

Substituting,

$$
I'\left(r\right)=\frac{\pi}{r}-\frac{1-r^2}{r}\cdot\frac{\pi}{1-r^2}=0.
$$

Hence $I\left(r\right)$ is a constant. Moreover, $I\left(0\right)=\int_0^\pi\ln1\,\mathrm{d}x=0$, so

$$
I\left(r\right)=0\left(\left|r\right|<1\right).

$$

$\blacksquare$
### Problem 6

(Problem 12.3-6) Let

$$
\displaystyle I\left(\alpha\right)=\int_0^{2\pi}\ln\left(1-\alpha\cos\theta\right)\,\mathrm{d}\theta
$$
($\left|\alpha\right|<1$). Prove that

$$
\displaystyle I'\left(\alpha\right)=\frac{2\pi\left(\sqrt{1-\alpha^2}-1\right)}{\alpha\sqrt{1-\alpha^2}},
$$
and deduce that

$$
\displaystyle I\left(\alpha\right)=2\pi\ln\frac{1+\sqrt{1-\alpha^2}}{2}.
$$

### Solution to Problem 6

By **Theorem 3.3** (Differentiation Under the Integral Sign),

$$
I'\left(\alpha\right)=\int_0^{2\pi}\frac{-\cos\theta}{1-\alpha\cos\theta}\,\mathrm{d}\theta.
$$

Decompose the integrand:

$$
\frac{-\cos\theta}{1-\alpha\cos\theta}=\frac1\alpha-\frac{1}{\alpha\left(1-\alpha\cos\theta\right)}.
$$

Making the substitution $t=\tan\frac{\theta}{2}$, we obtain the standard integral

$$
\int_0^{2\pi}\frac{\mathrm{d}\theta}{1-\alpha\cos\theta}=\frac{2\pi}{\sqrt{1-\alpha^2}}\left(\left|\alpha\right|<1\right).
$$

Hence

$$
I'\left(\alpha\right)=\frac{2\pi}{\alpha}-\frac{1}{\alpha}\cdot\frac{2\pi}{\sqrt{1-\alpha^2}}
=\frac{2\pi}{\alpha}\left(1-\frac1{\sqrt{1-\alpha^2}}\right)
=\frac{2\pi\left(\sqrt{1-\alpha^2}-1\right)}{\alpha\sqrt{1-\alpha^2}}.
$$

Now integrate with respect to $\alpha$. Noting that

$$
\frac{\mathrm{d}}{\mathrm{d}\alpha}\ln\frac{1+\sqrt{1-\alpha^2}}{2}
=\frac{1}{1+\sqrt{1-\alpha^2}}\cdot\frac{-\alpha}{\sqrt{1-\alpha^2}}
=\frac{\sqrt{1-\alpha^2}-1}{\alpha\sqrt{1-\alpha^2}},
$$

(the last step rationalizes: $\frac{1}{1+\sqrt{1-\alpha^2}}=\frac{1-\sqrt{1-\alpha^2}}{\alpha^2}$), we have

$$
I\left(\alpha\right)=2\pi\ln\frac{1+\sqrt{1-\alpha^2}}{2}+C.
$$

Moreover, $I\left(0\right)=\int_0^{2\pi}\ln1\,\mathrm{d}\theta=0$, while the right side at $\alpha=0$ is $2\pi\ln1+C=C$, so $C=0$. Therefore

$$
I\left(\alpha\right)=2\pi\ln\frac{1+\sqrt{1-\alpha^2}}{2}.

$$

$\blacksquare$