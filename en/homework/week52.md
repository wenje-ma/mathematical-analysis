# Assignment 52

> **Definition** (Inner Product and Norm) In $R\left[-\pi,\pi\right]$ define the inner product
> $$
> \left\langle f,g\right\rangle=\frac1\pi\displaystyle\int_{-\pi}^\pi f\left(x\right)g\left(x\right)\,\mathrm{d}x,
> $$
and the norm
> $$
> \left| f\right|=\sqrt{\left\langle f,f\right\rangle}=\left(\frac1\pi\displaystyle\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x\right)^{1/2}.
> $$

> **Proposition** (Orthogonality of the Trigonometric System) The trigonometric system
> $$
> 1,\cos x,\sin x,\cos2x,\sin2x,\cdots
> $$
is pairwise orthogonal on $\left[-\pi,\pi\right]$, i.e. the integral over $\left[-\pi,\pi\right]$ of the product of any two distinct elements is $0$; and $\displaystyle\int_{-\pi}^\pi1\,\mathrm{d}x=2\pi$,
> $$
> \displaystyle\int_{-\pi}^\pi\cos^2 nx\,\mathrm{d}x=\int_{-\pi}^\pi\sin^2 nx\,\mathrm{d}x=\pi\left(n=1,2,\cdots\right).
> $$

### Problem 1

(Problem 13.1-1) Prove that the inner product $\left\langle f,g\right\rangle$ defined in this section has the following properties:
(1)

$$
\left\langle f,g\right\rangle=\left\langle g,f\right\rangle\left(\forall f,g\in R\left[-\pi,\pi\right]\right);
$$

(2) For all $\forall\,\lambda,\mu\in\mathbb R$, and $f,g,h\in R\left[-\pi,\pi\right]$,

$$
\left\langle\lambda f+\mu g,h\right\rangle=\lambda\left\langle f,h\right\rangle+\mu\left\langle g,h\right\rangle.
$$

### Solution to Problem 1

(1) By **Definition** (Inner Product and Norm) and the commutativity of multiplication,

$$
\left\langle f,g\right\rangle=\frac1\pi\int_{-\pi}^\pi f\left(x\right)g\left(x\right)\,\mathrm{d}x=\frac1\pi\int_{-\pi}^\pi g\left(x\right)f\left(x\right)\,\mathrm{d}x=\left\langle g,f\right\rangle.
$$

(2) By the linearity of integration,

$$
\left\langle\lambda f+\mu g,h\right\rangle
=\frac1\pi\int_{-\pi}^\pi\left(\lambda f\left(x\right)+\mu g\left(x\right)\right)h\left(x\right)\,\mathrm{d}x=\lambda\cdot\frac1\pi\int_{-\pi}^\pi f\left(x\right)h\left(x\right)\,\mathrm{d}x+\mu\cdot\frac1\pi\int_{-\pi}^\pi g\left(x\right)h\left(x\right)\,\mathrm{d}x=\lambda\left\langle f,h\right\rangle+\mu\left\langle g,h\right\rangle.

$$

$\blacksquare$
### Problem 2

(Problem 13.1-2) Let $f,g\in R\left[-\pi,\pi\right]$ be any two functions. Prove that $\left|\left\langle f,g\right\rangle\right|\le\left| f\right|\cdot\left| g\right|$.

### Solution to Problem 2

For any real number $\lambda$, by the nonnegativity of the norm, $\left| f-\lambda g\right|^2\ge0$. Expanding:

$$
\left| f-\lambda g\right|^2=\left\langle f-\lambda g,f-\lambda g\right\rangle=\left| f\right|^2-2\lambda\left\langle f,g\right\rangle+\lambda^2\left| g\right|^2\ge0\left(\forall\lambda\in\mathbb R\right).
$$

This is a quadratic polynomial in $\lambda$, always nonnegative, so its discriminant is at most $0$:

$$
4\left\langle f,g\right\rangle^2-4\left| f\right|^2\left| g\right|^2\le0,
$$

i.e. $\left\langle f,g\right\rangle^2\le\left| f\right|^2\left| g\right|^2$. Taking square roots gives $\left|\left\langle f,g\right\rangle\right|\le\left| f\right|\cdot\left| g\right|$. $\blacksquare$

### Problem 3

(Problem 13.1-3) Let $f\left(x\right)$ and $g\left(x\right)$ be continuous on $\left[-\pi,\pi\right]$ and not identically zero. Prove that equality holds if and only if there exists a real number $\lambda$ such that $\lambda f\left(x\right)\equiv g\left(x\right)$:

$$
\displaystyle\left(\frac1\pi\int_{-\pi}^\pi f\left(x\right)g\left(x\right)\,\mathrm{d}x\right)^2=\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x\cdot\frac1\pi\int_{-\pi}^\pi g^2\left(x\right)\,\mathrm{d}x.
$$

### Solution to Problem 3

The right side is $\left| f\right|^2\left| g\right|^2$, and the left side is $\left\langle f,g\right\rangle^2$, so we must prove that equality holds if and only if $f,g$ are linearly dependent.

($\Leftarrow$) If there exists $\lambda$ such that $g\equiv\lambda f$, then

$$
\left\langle f,g\right\rangle=\left\langle f,\lambda f\right\rangle=\lambda\left| f\right|^2, \left| g\right|=\sqrt{\lambda^2\left\langle f,f\right\rangle}=\left|\lambda\right|\cdot\left| f\right|,
$$

so $\left\langle f,g\right\rangle^2=\lambda^2\left| f\right|^4=\left| f\right|^2\left| g\right|^2$, and equality holds.

($\Rightarrow$) If equality holds, i.e. $\left\langle f,g\right\rangle^2=\left| f\right|^2\left| g\right|^2$. By Problem 2, the discriminant of the quadratic polynomial $\left| f\right|^2\lambda^2-2\left\langle f,g\right\rangle\lambda+\left| g\right|^2$ is $0$, so there exists a double root $\lambda_0=\frac{\left\langle f,g\right\rangle}{\left| f\right|^2}$ such that $\left| f-\lambda_0 g\right|^2=0$. Since $f,g$ are continuous,

$$
\displaystyle\int_{-\pi}^\pi\left(f\left(x\right)-\lambda_0 g\left(x\right)\right)^2\,\mathrm{d}x=0
$$

implies $f\left(x\right)-\lambda_0 g\left(x\right)\equiv0$, i.e. $f\equiv\lambda_0 g$. $\blacksquare$

### Problem 4

(Problem 13.1-7) Let

$$
c_1+c_2\cos x+c_3\sin x\equiv0,
$$

where $c_1,c_2,c_3$ are constants. Using the orthogonality of the trigonometric system, prove that $c_1=c_2=c_3=0$, and extend this result to the following conclusion: any finite number of elements in the function system (1.2) are linearly independent.

### Solution to Problem 4

Multiply the identity

$$
c_1+c_2\cos x+c_3\sin x\equiv0
$$

on both sides respectively by $1,\cos x,\sin x$, and then integrate over $\left[-\pi,\pi\right]$. By **Proposition** (Orthogonality of the Trigonometric System), the integrals of the cross terms are all $0$, giving

$$
\int_{-\pi}^\pi\left(c_1+c_2\cos x+c_3\sin x\right)\,\mathrm{d}x=2\pi c_1=0,
$$

$$
\int_{-\pi}^\pi\left(c_1+c_2\cos x+c_3\sin x\right)\cos x\,\mathrm{d}x=\pi c_2=0,
$$

$$
\int_{-\pi}^\pi\left(c_1+c_2\cos x+c_3\sin x\right)\sin x\,\mathrm{d}x=\pi c_3=0.
$$

Hence $c_1=c_2=c_3=0$.

Extension: suppose a linear combination of finitely many elements of the function system

$$
1,\cos x,\sin x,\cos2x,\sin2x,\cdots
$$

is identically zero:

$$
\frac{a_0}{2}+\sum_{n=1}^N\left(a_n\cos nx+b_n\sin nx\right)\equiv0.
$$

Multiply both sides by $\cos mx$ ($0\le m\le N$) or $\sin mx$ ($1\le m\le N$) and integrate over $\left[-\pi,\pi\right]$. By **Proposition** (Orthogonality of the Trigonometric System), the integrals of all terms except the multiplied one are $0$, giving respectively $2\pi a_0=0$, $\pi a_m=0$, $\pi b_m=0$, i.e. all coefficients are $0$. Hence any finite number of elements of this function system are linearly independent. $\blacksquare$
