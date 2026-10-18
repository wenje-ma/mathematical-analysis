# Assignment 23

> **Definition** (Supremum and Infimum) Let $E$ be a bounded set. If there exists a real number $\beta$ satisfying:
> (1) $\beta$ is an upper bound of $E$ ($\forall x\in E,x\le\beta$);
>
> (2) for any $\epsilon>0$, there exists $x_0\in E$ such that $x_0>\beta-\epsilon$, then $\beta$ is called the supremum of $E$, denoted $\sup E$. The infimum $\inf E$ is defined similarly.

> **Definition** (Oscillation) Let $f\left(x\right)$ be defined and bounded on an interval $I$. The number
> $$
> \omega_f\left(I\right)=\sup\left\{f\left(x\right):x\in I\right\}-\inf\left\{f\left(x\right):x\in I\right\}
> $$
> is called the oscillation of $f$ on $I$.

> **Theorem 1.3** (Necessary and Sufficient Condition for Continuity) Let $y=f\left(x\right)$ be bounded near $x_0$. Then $f$ is continuous at $x_0$ if and only if $\omega_f\left(x_0\right)=0$.

### Problem 1

(Problem 5.1-4) Let $y=f\left(x\right)$ and $y=g\left(x\right)$ be bounded functions on $\left[a,b\right]$. Prove:
(1)

$$
\sup\limits_{\left[a,b\right]}\left\{f\left(x\right)+g\left(x\right)\right\}\le\sup\limits_{\left[a,b\right]}f\left(x\right)+\sup\limits_{\left[a,b\right]}g\left(x\right);
$$

(2)

$$
\inf\limits_{\left[a,b\right]}\left\{f\left(x\right)+g\left(x\right)\right\}\ge\inf\limits_{\left[a,b\right]}f\left(x\right)+\inf\limits_{\left[a,b\right]}g\left(x\right).
$$

### Solution to Problem 1

(1) For any $x\in\left[a,b\right]$, we have $f\left(x\right)\le\sup f$, $g\left(x\right)\le\sup g$. Hence
$$
f\left(x\right)+g\left(x\right)\le\sup f+\sup g.
$$

That is, $\sup f+\sup g$ is an upper bound of $f\left(x\right)+g\left(x\right)$. By **Definition** (Supremum and Infimum), the supremum is the least upper bound, so
$$
\sup\left\{f\left(x\right)+g\left(x\right)\right\}\le\sup f+\sup g.
$$

(2) For any $x\in\left[a,b\right]$, we have $f\left(x\right)\ge\inf f$, $g\left(x\right)\ge\inf g$. Hence
$$
f\left(x\right)+g\left(x\right)\ge\inf f+\inf g.
$$

That is, $\inf f+\inf g$ is a lower bound of $f\left(x\right)+g\left(x\right)$. Since the infimum is the greatest lower bound,
$$
\inf\left\{f\left(x\right)+g\left(x\right)\right\}\ge\inf f+\inf g.
$$

$\blacksquare$
### Problem 2

(Problem 5.1-5) Prove:

$$
\omega_f\left(I\right)=\sup\left\{\left|f\left(x_1\right)-f\left(x_2\right)\right|:x_1,x_2\in I\right\}.
$$

### Solution to Problem 2

Set $M=\sup\left\{f\left(x\right):x\in I\right\}$, $m=\inf\left\{f\left(x\right):x\in I\right\}$. Then $\omega_f\left(I\right)=M-m$.

For any $x_1,x_2\in I$, we have
$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|\le M-m.
$$

Hence $M-m$ is an upper bound of the set

$$
\left\{\left|f\left(x_1\right)-f\left(x_2\right)\right|:x_1,x_2\in I\right\}
$$

.

On the other hand, for any $\epsilon>0$, there exists $x_1\in I$ such that $f\left(x_1\right)>M-\frac{\epsilon}{2}$, and there exists $x_2\in I$ such that $f\left(x_2\right)<m+\frac{\epsilon}{2}$. Thus
$$
f\left(x_1\right)-f\left(x_2\right)>M-m-\epsilon,
$$

i.e.

$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|>M-m-\epsilon.
$$

By the definition of supremum,
$$
\sup\left\{\left|f\left(x_1\right)-f\left(x_2\right)\right|\right\}\ge M-m.
$$

Combining the two sides, we obtain

$$
\omega_f\left(I\right)=M-m=\sup\left\{\left|f\left(x_1\right)-f\left(x_2\right)\right|\right\}.
$$

$\blacksquare$

### Problem 3

(Problem 5.1-6) Let $y=D\left(x\right)$ be the Dirichlet function, i.e.
$$
D\left(x\right)=\begin{cases}0,&x\text{ 为无理数},\\1,&x\text{ 为有理数}.\end{cases}
$$
Prove that the oscillation of $D\left(x\right)$ on any interval is $1$, and the oscillation at every point $x$ is $1$.

### Solution to Problem 3

For any interval $I$, $I$ contains both rational and irrational numbers. Hence
$$
\sup_{x\in I}D\left(x\right)=1,\inf_{x\in I}D\left(x\right)=0.
$$

Therefore $\omega_D\left(I\right)=1-0=1$.

For any point $x_0$, every neighborhood of $x_0$ contains both rational and irrational numbers. Hence the oscillation of $D$ at $x_0$ is $\omega_D\left(x_0\right)=1$. By **Theorem 1.3** (Necessary and Sufficient Condition for Continuity), $D\left(x\right)$ is discontinuous at every point. $\blacksquare$

### Problem 4

(Problem 5.1-7) Use the theorem that every nonempty set bounded above has a supremum to deduce that every monotonically increasing sequence bounded above has a limit.

### Solution to Problem 4

Let $\left\{a_n\right\}$ be monotonically increasing and bounded above. By the existence theorem for suprema, the set $E=\left\{a_n:n\ge1\right\}$ has a supremum, denoted $l=\sup E$.

For any $\epsilon>0$, by the definition of supremum, there exists $N$ such that $a_N>l-\epsilon$. Since $\left\{a_n\right\}$ is monotonically increasing, when $n>N$ we have
$$
a_n\ge a_N>l-\epsilon.
$$

On the other hand, since $l$ is an upper bound, $a_n\le l<l+\epsilon$. Thus
$$
\left|a_n-l\right|<\epsilon,\forall n>N.
$$

By the definition of the limit of a sequence, $\lim\limits_{n\to\infty}a_n=l$. $\blacksquare$

### Problem 5

(Problem 5.1-9) Let $y=R\left(x\right)$ be the Riemann function, i.e.
$$
R\left(x\right)=\begin{cases}0,&x\text{ 为无理数},\\1/q,&x=p/q\text{ 为既约有理数},\left(p,q\right)=1.\end{cases}
$$
Prove:
(1) for any rational number $x=p/q$, the oscillation of $R\left(x\right)$ at that point is $\omega_R\left(x\right)=1/q$;

(2) for any irrational number $x$, $\omega_R\left(x\right)=0$.

### Solution to Problem 5

(1) Let $x_0=p/q$ be a reduced rational number, then $R\left(x_0\right)=1/q$. In every neighborhood of $x_0$, there are irrational numbers $x$ with $R\left(x\right)=0$, and there is also $x_0$ itself with $R\left(x_0\right)=1/q$. Hence
$$
\sup R=1/q,\inf R=0.
$$

Therefore $\omega_R\left(x_0\right)=1/q-0=1/q$.

(2) Let $x_0$ be irrational. For any $\epsilon>0$, there are only finitely many positive integers $q$ satisfying $1/q\ge\epsilon$. For each such $q$, there are also only finitely many reduced rational numbers $p/q$ with denominator $q$. Hence, in some sufficiently small neighborhood of $x_0$, except for $x_0$ itself (which is irrational, $R\left(x_0\right)=0$), all other rational points $p/q$ satisfy $1/q<\epsilon$. Hence in that neighborhood, $0\le R\left(x\right)<\epsilon$. Thus
$$
\sup R-\inf R<\epsilon.
$$

By the arbitrariness of $\epsilon$, $\omega_R\left(x_0\right)=0$. By **Theorem 1.3** (Necessary and Sufficient Condition for Continuity), the Riemann function is continuous at irrational points. $\blacksquare$
