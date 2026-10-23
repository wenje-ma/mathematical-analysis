# Assignment 25

> **Definition** (Uniform Continuity) Let $y=f\left(x\right)$ be defined on an interval $X$. If for any given $\varepsilon>0$, there exists a $\delta>0$ such that for any two points $x_1$ and $x_2$ in $X$, $\left|f\left(x_1\right)-f\left(x_2\right)\right|<\varepsilon$ (whenever $\left|x_1-x_2\right|<\delta$), then $y=f\left(x\right)$ is said to be uniformly continuous in $X$.

> **Theorem 3.2** (Finite Covering Theorem) Let $\mathcal{F}=\left\{I_\alpha:\alpha\in A\right\}$ be any open cover of the closed interval $\left[a,b\right]$. Then there exist finitely many elements $I_{\alpha_1},\cdots,I_{\alpha_n}$ in $\mathcal{F}$ such that $\left[a,b\right]\subset\bigcup\limits_{k=1}^n I_{\alpha_k}$.

### Problem 1

(Problem 5.3-2) Let $f\left(x\right)=\frac1x$ ($0<x<1$). Directly from the definition, prove that $f\left(x\right)$ is not uniformly continuous on $\left(0,1\right)$.

### Solution to Problem 1

To prove that $f\left(x\right)=\frac1x$ is not uniformly continuous on $\left(0,1\right)$, we need to show that there exists $\varepsilon_0>0$ such that for any $\delta>0$, there exist $x_1,x_2\in\left(0,1\right)$ such that
$$
\left|x_1-x_2\right|<\delta,\text{但}\;\left|f\left(x_1\right)-f\left(x_2\right)\right|\ge\varepsilon_0.
$$

Take $\varepsilon_0=1$. For any $\delta>0$, take $x_1=\frac{\delta}{2}$, $x_2=\frac{\delta}{3}$. Then
$$
\left|x_1-x_2\right|=\frac{\delta}{6}<\delta,
$$

but
$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|=\left|\frac{2}{\delta}-\frac{3}{\delta}\right|=\frac1\delta\to\infty\left(\delta\to0\right).
$$

When $\delta<1$, $\frac1\delta>1=\varepsilon_0$. Hence $f\left(x\right)=\frac1x$ is not uniformly continuous on $\left(0,1\right)$. $\blacksquare$

### Problem 2

(Problem 5.3-3) Let the set $E=\left\{\frac1n:n=1,2,\cdots\right\}$. Construct an open cover of the set $E$ from which no finite number of elements can cover $E$.

### Solution to Problem 2

For each $n$, take the open interval $I_n=\left(\frac1n-\frac{1}{4n^2},\frac1n+\frac{1}{4n^2}\right)$. Clearly $\frac1n\in I_n$, so $E\subset\bigcup\limits_{n=1}^\infty I_n$, i.e. $\left\{I_n\right\}$ is an open cover of $E$.

But any finite number of intervals $I_{n_1},\cdots,I_{n_k}$ can only cover finitely many points $\frac1{n_1},\cdots,\frac1{n_k}$. Let $N=\max\left\{n_1,\cdots,n_k\right\}$; then when $n>N$, $\frac1n\in E$ but $\frac1n\notin\bigcup\limits_{i=1}^k I_{n_i}$ (since the center of $I_{n_i}$ is $\frac1{n_i}$ and its radius is $\frac{1}{4n_i^2}$, which does not contain $\frac1n$).

Hence no finite number of elements can be selected to cover $E$. $\blacksquare$

### Problem 3

(Problem 5.3-4) Prove that for the set

$$
E=\left\{\frac1n:n=1,2,\cdots\right\}\cup\left\{0\right\},
$$

every open cover has a finite subcover.

### Solution to Problem 3

This problem is a concrete application of **Theorem 3.2** (Finite Covering Theorem) on the compact set $E=\left\{1/n\right\}\cup\left\{0\right\}$, and its proof is the same idea as that theorem: first cover the accumulation point $0$, then cover the remaining finitely many isolated points.

Let $\mathcal{F}$ be any open cover of $E$. Since $0\in E$, there exists $I_0\in\mathcal{F}$ such that $0\in I_0$. Since $I_0$ is an open interval, there exists $\delta>0$ such that $\left(-\delta,\delta\right)\subset I_0$.

Take $N$ such that $\frac1N<\delta$. Then when $n>N$, $0<\frac1n<\delta$, i.e. $\frac1n\in\left(-\delta,\delta\right)\subset I_0$. Hence $I_0$ covers all points of $E$ except $\frac11,\frac12,\cdots,\frac1N$.

For each $n=1,2,\cdots,N$, since $\frac1n\in E$, there exists $I_n\in\mathcal{F}$ such that $\frac1n\in I_n$.

Thus $\left\{I_0,I_1,\cdots,I_N\right\}$ is a finite subset of $\mathcal{F}$ and covers $E$. $\blacksquare$

### Problem 4

(Problem 5.3-5) Prove that $y=\sin x$ is uniformly continuous on $\left(-\infty,+\infty\right)$.

### Solution to Problem 4

For any $x_1,x_2\in\mathbb R$, by the Lagrange mean value theorem,
$$
\left|\sin x_1-\sin x_2\right|=\left|\cos\xi\right|\cdot\left|x_1-x_2\right|\le\left|x_1-x_2\right|,
$$

where $\xi$ lies between $x_1$ and $x_2$.

For any $\varepsilon>0$, take $\delta=\varepsilon$. Then when $\left|x_1-x_2\right|<\delta$,
$$
\left|\sin x_1-\sin x_2\right|\le\left|x_1-x_2\right|<\delta=\varepsilon.
$$

By **Definition** (Uniform Continuity), $y=\sin x$ is uniformly continuous on $\mathbb R$. $\blacksquare$

### Problem 5

(Problem 5.3-6) Prove that $y=\cos x$ is uniformly continuous on $\left(-\infty,+\infty\right)$.

### Solution to Problem 5

For any $x_1,x_2\in\mathbb R$, by the Lagrange mean value theorem,
$$
\left|\cos x_1-\cos x_2\right|=\left|-\sin\xi\right|\cdot\left|x_1-x_2\right|\le\left|x_1-x_2\right|,
$$

where $\xi$ lies between $x_1$ and $x_2$.

For any $\varepsilon>0$, take $\delta=\varepsilon$. Then when $\left|x_1-x_2\right|<\delta$,
$$
\left|\cos x_1-\cos x_2\right|\le\left|x_1-x_2\right|<\delta=\varepsilon.
$$

By the definition of uniform continuity, $y=\cos x$ is uniformly continuous on $\mathbb R$. $\blacksquare$

### Problem 6

(Problem 5.3-7) Prove that $y=\sin 3x+5x+1$ is uniformly continuous on $\left(-\infty,+\infty\right)$.

### Solution to Problem 6

For any $x_1,x_2\in\mathbb R$,
$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|=\left|\sin3x_1-\sin3x_2+5\left(x_1-x_2\right)\right|.
$$

By the triangle inequality and Problem 4 ($\sin x$ is uniformly continuous),
$$
\left|\sin3x_1-\sin3x_2\right|\le3\left|x_1-x_2\right|.
$$

Hence
$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|\le3\left|x_1-x_2\right|+5\left|x_1-x_2\right|=8\left|x_1-x_2\right|.
$$

For any $\varepsilon>0$, take $\delta=\frac{\varepsilon}{8}$. Then when $\left|x_1-x_2\right|<\delta$, $\left|f\left(x_1\right)-f\left(x_2\right)\right|<\varepsilon$. By the definition of uniform continuity, $f\left(x\right)$ is uniformly continuous on $\mathbb R$. $\blacksquare$

### Problem 7

(Problem 5.3-8) Let $f\left(x\right)$ be defined on $\left(a,b\right)$ and satisfy the following condition:
$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|\le H\left|x_1-x_2\right|^\alpha,\forall x_1,x_2\in\left(a,b\right),
$$
where $H>0$ and $0<\alpha\le1$ are constants. In this case, $f\left(x\right)$ is said to be Hölder continuous on $\left(a,b\right)$. Prove that a function Hölder continuous on $\left(a,b\right)$ must be uniformly continuous. Further prove that when $f\left(x\right)$ is differentiable on $\left(a,b\right)$ and its derivative is bounded, $f\left(x\right)$ satisfies a Hölder condition on $\left(a,b\right)$ with $\alpha=1$.

### Solution to Problem 7

**Part 1**: Let $f$ satisfy a Hölder condition with exponent $\alpha$. For any $\varepsilon>0$, take $\delta=\left(\frac{\varepsilon}{H}\right)^{1/\alpha}$. Then when $\left|x_1-x_2\right|<\delta$,
$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|\le H\left|x_1-x_2\right|^\alpha<H\delta^\alpha=\varepsilon.
$$

By the definition of uniform continuity, $f$ is uniformly continuous on $\left(a,b\right)$.

**Part 2**: Let $f'\left(x\right)$ be bounded on $\left(a,b\right)$, i.e. there exists $M>0$ such that $\left|f'\left(x\right)\right|\le M$ ($\forall x\in\left(a,b\right)$). For any $x_1,x_2\in\left(a,b\right)$, by the Lagrange mean value theorem,
$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|=\left|f'\left(\xi\right)\right|\cdot\left|x_1-x_2\right|\le M\left|x_1-x_2\right|,
$$

where $\xi$ lies between $x_1$ and $x_2$. This is exactly the Hölder condition with $\alpha=1$ and $H=M$. $\blacksquare$
