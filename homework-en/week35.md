# week35

> **Theorem 3.3 (Differentiation Under the Integral Sign)**
> 
> $I'\left(y\right)=\int_a^b f_y\left(x,y\right)\mathrm dx$. If limits depend on $y$, add boundary terms.

> **Theorem 4.3 (Weierstrass M-Test for Improper Integrals)**
> 
> If $\left|f\left(x,y\right)\right|\le F\left(x\right)$ and $\int F$ converges, then $\int f$ converges uniformly.

> **Theorem 4.4 (Abel's Test)**
> 
> If $\int f$ converges uniformly and $g$ is monotone and uniformly bounded, then $\int fg$ converges uniformly.

> **Example 4.5 (Dirichlet Integral)**
> 
> $\int_0^\infty\frac{\sin x}x\mathrm dx=\frac\pi2$.

> **Theorem 4.7 (Interchange of Order of Integration)**
> 
> Under uniform convergence, $\int_c^d\mathrm dy\int_a^\infty f\,\mathrm dx=\int_a^\infty\mathrm dx\int_c^d f\,\mathrm dy$.

> **Theorem 4.7 (Interchange of Order)**
> 
> Under uniform convergence and fixed sign, $\int_c^d\mathrm dy\int_a^b f=\int_a^b\mathrm dx\int_c^d f$.

> **Theorem 4.8 (Differentiation Under the Integral Sign)**
> 
> $I'\left(y\right)=\int_a^\infty f_y\,\mathrm dx$ under uniform convergence of $\int f_y$.

> **Proposition (Integral Forms)**
> 
> $\int_0^\infty\frac{x^{a-1}}{\left(1+x\right)^{a+b}}\mathrm dx=\Beta\left(a,b\right)$; $\int_0^{\pi/2}\sin^m x\cos^n x\,\mathrm dx=\frac12\Beta\left(\frac{m+1}2,\frac{n+1}2\right)$.

## 12.3-6

Prove $I\left(\alpha\right)=2\pi\ln\frac{1+\sqrt{1-\alpha^2}}2$.

### Solution to 12.3-6

By differentiation under the integral sign. $\blacksquare$

## 12.4-1-1

Discuss uniform convergence of $\int_0^\infty e^{-\alpha x^2}\mathrm dx$.

### Solution to 12.4-1-1

Uniformly convergent by the M-test. $\blacksquare$

## 12.4-1-3

Discuss $\int_1^\infty e^{-xy}\frac{\cos x}x\mathrm dx$.

### Solution to 12.4-1-3

Uniformly convergent by Abel's test. $\blacksquare$

## 12.4-1-5

Discuss $\int_0^\infty e^{-x^2y^2}\cos x\,\mathrm dx$.

### Solution to 12.4-1-5

Uniformly convergent by the M-test. $\blacksquare$

## 12.4-2-1

Evaluate $\int_0^\infty\frac{e^{-ax}-e^{-bx}}x\mathrm dx$.

### Solution to 12.4-2-1

$\ln\frac ba$. $\blacksquare$

## 12.4-2-2

Evaluate $\int_0^\infty\frac{\sin\left(\alpha x\right)\cos\left(\beta x\right)}x\mathrm dx$.

### Solution to 12.4-2-2

$0$ if $\alpha< \beta$, $\frac\pi4$ if $\alpha=\beta$, $\frac\pi2$ if $\alpha> \beta$. $\blacksquare$

## 12.4-2-4

Evaluate $\int_0^\infty\frac{1-\cos\left(\alpha x\right)}x e^{-x}\mathrm dx$.

### Solution to 12.4-2-4

$\frac12\ln\left(1+\alpha^2\right)$. $\blacksquare$

## 12.4-5

Prove Dini's theorem.

### Solution to 12.4-5

By contradiction using compactness and monotonicity. $\blacksquare$

## 12.5-1-1

Discuss uniform convergence of $\int_0^1\frac{\sin x}{x^\alpha}\mathrm dx$.

### Solution to 12.5-1-1

(i) Uniformly convergent for $\alpha\le\alpha_0< 2$. (ii) Not uniformly convergent on $\alpha< 2$. $\blacksquare$

## 12.5-1-2

Discuss $\int_0^1 x^{p-1}\mathrm dx$.

### Solution to 12.5-1-2

(i) Uniformly convergent for $p\ge p_0> 0$. (ii) Not uniformly convergent on $p> 0$. $\blacksquare$

## 12.5-2-1

Evaluate $\int_0^1\frac{x^b-x^a}{\ln x}\mathrm dx$.

### Solution to 12.5-2-1

$\ln\frac{1+b}{1+a}$. $\blacksquare$

## 12.6-1-1

Evaluate $\int_0^\infty\frac{4\sqrt x}{\left(1+x\right)^2}\mathrm dx$.

### Solution to 12.6-1-1

$2\pi$. $\blacksquare$

## 12.6-1-2

Evaluate $\int_0^\infty x^{-1/2}e^{-\alpha x}\mathrm dx$.

### Solution to 12.6-1-2

$\sqrt{\frac\pi\alpha}$. $\blacksquare$

## 12.6-1-3

Evaluate $\int_0^1 x^8\sqrt{1-x^3}\mathrm dx$.

### Solution to 12.6-1-3

$\frac{16}{315}$. $\blacksquare$

## 12.6-1-4

Evaluate $\int_0^{\pi/2}\sin^6x\cos^4x\,\mathrm dx$.

### Solution to 12.6-1-4

$\frac{3\pi}{512}$. $\blacksquare$

## 12.6-1-9

Evaluate $\int_0^1\frac{\mathrm dx}{\sqrt{1-x^4}}$.

### Solution to 12.6-1-9

$\frac14\Beta\left(\frac14,\frac12\right)$. $\blacksquare$

## 12.6-1-10

Evaluate $\int_0^\infty\frac{\mathrm dx}{1+x^3}$.

### Solution to 12.6-1-10

$\frac13\Gamma\left(\frac13\right)\Gamma\left(\frac23\right)$. $\blacksquare$
