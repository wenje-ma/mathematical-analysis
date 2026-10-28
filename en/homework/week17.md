# week17

> **Basic Knowledge: Definition of Convex and Concave Functions**<br>If $f$ satisfies $f\left(tx_1+\left(1-t\right)x_2\right)\le tf\left(x_1\right)+\left(1-t\right)f\left(x_2\right)$ for all $x_1,x_2$ and $t\in\left(0,1\right)$, it is convex; if the inequality reverses, it is concave.

> **Theorem 1.3 (Lagrange Mean Value Theorem)**<br>If $f$ is continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$, then there exists $c\in\left(a,b\right)$ such that $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

> **Theorem 5.1 (Second Derivative Criterion for Convexity)**<br>If $f$ is twice differentiable on $\left(a,b\right)$, then $f$ is convex iff $f''\left(x\right)\ge0$, and concave iff $f''\left(x\right)\le0$.

---

## 3.5-1-1

Find the convexity intervals and inflection points of $y=xe^x$.

### Solution 3.5-1-1

$y'=\left(1+x\right)e^x$, $y''=\left(2+x\right)e^x$. Setting $y''=0$ gives $x=-2$. By **Theorem 5.1 (Second Derivative Criterion for Convexity)**, $y$ is concave on $\left(-\infty,-2\right]$ and convex on $\left[-2,+\infty\right)$. The inflection point is $\left(-2,-2e^{-2}\right)$. $\blacksquare$

---

## 3.5-1-4

Find the convexity intervals and inflection points of $y=x\ln x$.

### Solution 3.5-1-4

Domain $\left(0,+\infty\right)$. $y''=\frac1x> 0$. By **Theorem 5.1 (Second Derivative Criterion for Convexity)**, $y=x\ln x$ is convex on $\left(0,+\infty\right)$ with no inflection points. $\blacksquare$

---

## 3.5-2

Use convexity to prove:

(1) $2\arctan\frac{a+b}2\ge\arctan a+\arctan b$ for $a,b> 0$;

(2) $a^\alpha b^\beta c^\gamma\le\alpha a+\beta b+\gamma c$ for $a,b,c> 0$, $\alpha+\beta+\gamma=1$.

### Solution 3.5-2

(1) $f\left(x\right)=\arctan x$ has $f''\left(x\right)=\frac{-2x}{\left(1+x^2\right)^2}< 0$ for $x> 0$, so it is concave. By **Basic Knowledge: Definition of Convex and Concave Functions** with $t=\frac12$,

$$
f\left(\frac{a+b}2\right)\ge\frac{f\left(a\right)+f\left(b\right)}2.
$$

(2) $f\left(x\right)=\ln x$ is concave ($f''=-\frac1{x^2}< 0$). By concavity,

$$
\alpha\ln a+\beta\ln b+\gamma\ln c\le\ln\left(\alpha a+\beta b+\gamma c\right),
$$

which gives the weighted AM-GM inequality. $\blacksquare$

---

## 3.5-3

Let $f$ and $g$ be convex on $\left(a,b\right)$. Prove $F\left(x\right)=\max\left\{f\left(x\right),g\left(x\right)\right\}$ is convex.

### Solution 3.5-3

For any $x_1,x_2$ and $t\in\left(0,1\right)$, since both $f$ and $g$ are convex,

$$
f\left(tx_1+\left(1-t\right)x_2\right)\le tF\left(x_1\right)+\left(1-t\right)F\left(x_2\right),
$$

$$
g\left(tx_1+\left(1-t\right)x_2\right)\le tF\left(x_1\right)+\left(1-t\right)F\left(x_2\right).
$$

Taking the max gives $F\left(tx_1+\left(1-t\right)x_2\right)\le tF\left(x_1\right)+\left(1-t\right)F\left(x_2\right)$. $\blacksquare$

---

## 3.5-5

Let $f\left(u\right)$ be convex and increasing on $\mathbb R$, and $g\left(x\right)$ be convex on $\left(a,b\right)$. Prove $f\left(g\left(x\right)\right)$ is convex.

### Solution 3.5-5

Since $g$ is convex, $g\left(tx_1+\left(1-t\right)x_2\right)\le tg\left(x_1\right)+\left(1-t\right)g\left(x_2\right)$. Since $f$ is increasing,

$$
f\left(g\left(tx_1+\left(1-t\right)x_2\right)\right)\le f\left(tg\left(x_1\right)+\left(1-t\right)g\left(x_2\right)\right).
$$

Since $f$ is convex,

$$
f\left(tg\left(x_1\right)+\left(1-t\right)g\left(x_2\right)\right)\le tf\left(g\left(x_1\right)\right)+\left(1-t\right)f\left(g\left(x_2\right)\right).
$$

Thus $f\left(g\left(x\right)\right)$ is convex. $\blacksquare$

---

## 3.5-6

Let $f$ be differentiable, convex, and bounded on $\mathbb R$. Prove $f$ is constant.

### Solution 3.5-6

By **Theorem 5.1 (Second Derivative Criterion for Convexity)**, $f''\ge0$, so $f'$ is increasing. If $f'\left(x_0\right)> 0$, then for $x> x_0$, by **Theorem 1.3 (Lagrange Mean Value Theorem)**, $f\left(x\right)\ge f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)\to+\infty$, contradicting boundedness. If $f'\left(x_0\right)< 0$, similarly $f\left(x\right)\to+\infty$ as $x\to-\infty$. Hence $f'\equiv0$ and $f$ is constant. $\blacksquare$

---

## 3.5-7-1

Sketch $y=\frac{\left(x+1\right)^3}{\left(x-1\right)^2}$.

### Solution 3.5-7-1

Domain $\left(-\infty,1\right)\cup\left(1,+\infty\right)$. Vertical asymptote $x=1$, oblique asymptote $y=x+5$. $y'=\frac{\left(x+1\right)^2\left(x-5\right)}{\left(x-1\right)^3}$; $x=5$ is a local minimum with value $\frac{27}2$. $y''=\frac{16\left(x+1\right)}{\left(x-1\right)^4}$; concave for $x< -1$, convex for $x> -1$; inflection point $\left(-1,0\right)$. $\blacksquare$

---

## 3.5-7-2

Sketch $y=xe^{-x}$.

### Solution 3.5-7-2

Domain $\mathbb R$. Horizontal asymptote $y=0$ as $x\to+\infty$. $y'=\left(1-x\right)e^{-x}$; $x=1$ is a local maximum with value $\frac1e$. $y''=\left(x-2\right)e^{-x}$; concave for $x< 2$, convex for $x> 2$; inflection point $\left(2,2e^{-2}\right)$. $\blacksquare$

---

## 3.5-7-3

Sketch $y=xe^{-x^2}$.

### Solution 3.5-7-3

Domain $\mathbb R$, odd function. Horizontal asymptote $y=0$. $y'=\left(1-2x^2\right)e^{-x^2}$; local minimum at $x=-\frac1{\sqrt2}$ with value $-\frac1{\sqrt{2e}}$, local maximum at $x=\frac1{\sqrt2}$ with value $\frac1{\sqrt{2e}}$. $y''=2x\left(2x^2-3\right)e^{-x^2}$; inflection points at $\left(0,0\right)$ and $\left(\pm\sqrt{\frac32},\pm\sqrt{\frac32}e^{-3/2}\right)$. $\blacksquare$
