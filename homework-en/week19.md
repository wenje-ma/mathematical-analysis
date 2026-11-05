# week19

> **Theorem 1.3 (Lagrange Mean Value Theorem)**
> 
> If $f$ is continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$, then there exists $c\in\left(a,b\right)$ such that $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

> **Theorem 1.3 (Linearity of Indefinite Integral)**
> 
> If $f$ and $g$ have antiderivatives, then $\int\left[af\left(x\right)+bg\left(x\right)\right]\mathrm{d}x=a\int{f}\left(x\right)\,\mathrm{d}x+b\int{g}\left(x\right)\,\mathrm{d}x$.

> **Theorem 5.1 (Second Derivative Criterion for Convexity)**
> 
> If $f$ is twice differentiable on $\left(a,b\right)$, then $f$ is convex iff $f''\left(x\right)\ge0$, and concave iff $f''\left(x\right)\le0$.

## 3.5-3

Let $f$ and $g$ be convex on $\left(a,b\right)$. Prove $F\left(x\right)=\max\left\{f\left(x\right),g\left(x\right)\right\}$ is convex.

### Solution to 3.5-3

For any $x_1,x_2$ and $t\in\left(0,1\right)$, since both $f$ and $g$ are convex,

$$
f\left(tx_1+\left(1-t\right)x_2\right)\le{t}F\left(x_1\right)+\left(1-t\right)F\left(x_2\right),
$$

$$
g\left(tx_1+\left(1-t\right)x_2\right)\le{t}F\left(x_1\right)+\left(1-t\right)F\left(x_2\right).
$$

Taking the max gives $F\left(tx_1+\left(1-t\right)x_2\right)\le{t}F\left(x_1\right)+\left(1-t\right)F\left(x_2\right)$. $\blacksquare$

## 3.5-5

Let $f\left(u\right)$ be convex and increasing on $\mathbb{R}$, and $g\left(x\right)$ be convex on $\left(a,b\right)$. Prove $f\left(g\left(x\right)\right)$ is convex.

### Solution to 3.5-5

Since $g$ is convex, $g\left(tx_1+\left(1-t\right)x_2\right)\le{t}g\left(x_1\right)+\left(1-t\right)g\left(x_2\right)$. Since $f$ is increasing,

$$
f\left(g\left(tx_1+\left(1-t\right)x_2\right)\right)\le{f}\left(tg\left(x_1\right)+\left(1-t\right)g\left(x_2\right)\right).
$$

Since $f$ is convex,

$$
f\left(tg\left(x_1\right)+\left(1-t\right)g\left(x_2\right)\right)\le{t}f\left(g\left(x_1\right)\right)+\left(1-t\right)f\left(g\left(x_2\right)\right).
$$

Thus $f\left(g\left(x\right)\right)$ is convex. $\blacksquare$

## 3.5-6

Let $f$ be differentiable, convex, and bounded on $\mathbb{R}$. Prove $f$ is constant.

### Solution to 3.5-6

By **Theorem 5.1 (Second Derivative Criterion for Convexity)**, $f''\ge0$, so $f'$ is increasing. If $f'\left(x_0\right)>0$, then for $x>{}x_0$, by **Theorem 1.3 (Lagrange Mean Value Theorem)**, $f\left(x\right)\ge{f}\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)\to+\infty$, contradicting boundedness. If $f'\left(x_0\right)<0$, similarly $f\left(x\right)\to+\infty$ as $x\to-\infty$. Hence $f'\equiv0$ and $f$ is constant. $\blacksquare$

## 3.5-7-1

Sketch $y=\frac{\left(x+1\right)^3}{\left(x-1\right)^2}$.

### Solution to 3.5-7-1

Domain $\left(-\infty,1\right)\cup\left(1,+\infty\right)$. Vertical asymptote $x=1$, oblique asymptote $y=x+5$. $y'=\frac{\left(x+1\right)^2\left(x-5\right)}{\left(x-1\right)^3}$; $x=5$ is a local minimum with value $\frac{27}2$. $y''=\frac{16\left(x+1\right)}{\left(x-1\right)^4}$; concave for $x<-1$, convex for $x>-1$; inflection point $\left(-1,0\right)$. $\blacksquare$

## 3.5-7-2

Sketch $y=xe^{-x}$.

### Solution to 3.5-7-2

Domain $\mathbb{R}$. Horizontal asymptote $y=0$ as $x\to+\infty$. $y'=\left(1-x\right)e^{-x}$; $x=1$ is a local maximum with value $\frac1e$. $y''=\left(x-2\right)e^{-x}$; concave for $x<2$, convex for $x>2$; inflection point $\left(2,2e^{-2}\right)$. $\blacksquare$

## 3.5-7-3

Sketch $y=xe^{-x^2}$.

### Solution to 3.5-7-3

Domain $\mathbb{R}$, odd function. Horizontal asymptote $y=0$. $y'=\left(1-2x^2\right)e^{-x^2}$; local minimum at $x=-\frac1{\sqrt2}$ with value $-\frac1{\sqrt{2e}}$, local maximum at $x=\frac1{\sqrt2}$ with value $\frac1{\sqrt{2e}}$. $y''=2x\left(2x^2-3\right)e^{-x^2}$; inflection points at $\left(0,0\right)$ and $\left(\pm\sqrt{\frac32},\pm\sqrt{\frac32}e^{-3/2}\right)$. $\blacksquare$

## 4.1-1-1

Find $\int\left(x^3+4\right)\,\mathrm{d}x$.

### Solution to 4.1-1-1

By **Theorem 1.3 (Linearity of Indefinite Integral)**,

$$
\int\left(x^3+4\right)\,\mathrm{d}x=\frac{x^4}4+4x+C.
$$

$\blacksquare$

## 4.1-1-4

Find $\int\tan^2x\,\mathrm{d}x$.

### Solution to 4.1-1-4

Using $\tan^2x=\sec^2x-1$ and **Theorem 1.3 (Linearity of Indefinite Integral)**,

$$
\int\tan^2x\,\mathrm{d}x=\tan{x}-x+C.
$$

$\blacksquare$
