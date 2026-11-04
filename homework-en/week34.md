# week34

> **Theorem 1.1 (Cauchy Criterion)**
> 
> The integral converges iff for every $\varepsilon> 0$, there exists $X$ such that $\left|\int_{A'}^{A''}f\right|< \varepsilon$ for $A',A''> X$.

> **Example 1.2 (p-Integral)**
> 
> $\int_1^\infty\frac{\mathrm dx}{x^p}$ converges iff $p> 1$.

> **Theorem 1.3 (Comparison Test)**
> 
> If $0\le f\le g$, then $\int g$ convergent implies $\int f$ convergent.

> **Theorem 1.6 (Dirichlet's Test)**
> 
> If $f$ is monotone tending to $0$ and $\int_a^A g$ is bounded for all $A$, then $\int fg$ converges.

> **Example 2.2 (Singular p-Integral)**
> 
> $\int_a^b\frac{\mathrm dx}{\left(x-a\right)^p}$ converges iff $p< 1$.

> **Theorem 3.3 (Differentiation Under the Integral Sign)**
> 
> $I'\left(y\right)=\int_a^b f_y\left(x,y\right)\mathrm dx$. If limits depend on $y$, add boundary terms.

## 12.1-3

Evaluate $I_1=\int_0^\infty e^{-xt}\sin t\mathrm dt$ and $I_2=\int_0^\infty e^{-xt}\cos t\mathrm dt$.

### Solution to 12.1-3

$I_1=\frac1{x^2+1}$, $I_2=\frac x{x^2+1}$. $\blacksquare$

## 12.1-4

Prove translation and reflection invariance.

### Solution to 12.1-4

By substitution. $\blacksquare$

## 12.1-5

Prove: $\int_1^\infty f$ converges iff $\sum a_n$ converges, where $a_n=\int_n^{n+1}f$.

### Solution to 12.1-5

By partial sums and $f\left(x\right)\to0$. $\blacksquare$

## 12.2-1-1

Evaluate $\int_0^1\ln x\mathrm dx$.

### Solution to 12.2-1-1

$-1$. $\blacksquare$

## 12.2-1-3

Evaluate $\int_{-1}^1\frac{\mathrm dx}{\sqrt{1-x^2}}$.

### Solution to 12.2-1-3

$\pi$. $\blacksquare$

## 12.2-1-5

Discuss $\int_0^1\frac{\mathrm dx}{x\ln^2x}$.

### Solution to 12.2-1-5

Diverges. $\blacksquare$

## 12.2-2-1

Discuss $\int_0^\infty\frac{\mathrm dx}{\sqrt x\left(1+x\right)}$.

### Solution to 12.2-2-1

Converges, value $\pi$. $\blacksquare$

## 12.2-2-3

Discuss $\int_0^\infty\frac{\mathrm dx}{x^p+x^q}$.

### Solution to 12.2-2-3

Converges iff $\min\left(p,q\right)< 1< \max\left(p,q\right)$. $\blacksquare$

## 12.2-2-5

Discuss $\int_0^{\pi/2}\frac{\mathrm dx}{\sin^2x\cos^2x}$.

### Solution to 12.2-2-5

Diverges. $\blacksquare$

## 12.2-2-7

Discuss $\int_0^1 x^p\left(1-x\right)^q\mathrm dx$.

### Solution to 12.2-2-7

Converges for all $p> 0,q> 0$. $\blacksquare$

## 12.2-3

Prove: $\int f^2$ convergent implies $\int\left|f\right|$ convergent.

### Solution to 12.2-3

By $2\left|f\right|\le1+f^2$. Converse is false. $\blacksquare$

## 12.2-4-1

Find the Cauchy principal value of $\int_0^2\frac{\mathrm dx}{x-1}$.

### Solution to 12.2-4-1

$0$. $\blacksquare$

## 12.2-4-2

Find the Cauchy principal value of $\int_{1/2}^2\frac{\mathrm dx}{x\ln x}$.

### Solution to 12.2-4-2

$0$. $\blacksquare$

## 12.3-2-5

Find $I'\left(y\right)$ for $I\left(y\right)=\int_{\sin y}^{\cos y}e^{y\sqrt{1-x^2}}\mathrm dx$.

### Solution to 12.3-2-5

$I'\left(y\right)=\int_{\sin y}^{\cos y}\sqrt{1-x^2}e^{y\sqrt{1-x^2}}\mathrm dx-e^{y\sin y}\sin y-e^{y\cos y}\cos y$. $\blacksquare$

## 12.3-2-6

Find $I'\left(y\right)$ for $I\left(y\right)=\int_0^{x/y}y\sin\left(xy\right)\mathrm dx$.

### Solution to 12.3-2-6

$I'\left(y\right)=0$. $\blacksquare$

## 12.3-2-7

Find $I'\left(y\right)$ for $I\left(y\right)=\int_0^{y^2}\sin\left(x^2+y^2\right)\mathrm dx$.

### Solution to 12.3-2-7

$I'\left(y\right)=\int_0^{y^2}2y\cos\left(x^2+y^2\right)\mathrm dx+2y\sin\left(y^4+y^2\right)$. $\blacksquare$

## 12.3-2-8

Find $I'\left(y\right)$ for $I\left(y\right)=\int_0^y\frac{\ln\left(1+xy\right)}x\mathrm dx$.

### Solution to 12.3-2-8

$I'\left(y\right)=\frac{\ln\left(1+y^2\right)}y+\int_0^y\frac{\mathrm dx}{1+xy}$. $\blacksquare$

## 12.3-4-1

Evaluate $I\left(r\right)=\int_0^\pi\ln\left(1-2r\cos x+r^2\right)\mathrm dx$.

### Solution to 12.3-4-1

$I\left(r\right)=0$. $\blacksquare$
