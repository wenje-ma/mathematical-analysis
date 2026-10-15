# Assignment 27

> **Lemma 2.1** (Effect of Refining the Partition Points) Let $T'$ be a partition obtained from $T$ by adding finitely many partition points. Then $d\left(T\right)\le d\left(T'\right)$ and $D\left(T'\right)\le D\left(T\right)$; that is, as partition points are added, the lower Darboux sum does not decrease and the upper Darboux sum does not increase.

> **Theorem 2.2** (Necessary and Sufficient Condition for Integrability) Let $y=f\left(x\right)$ be bounded on $\left[a,b\right]$. Then $y=f\left(x\right)$ is Riemann integrable on $\left[a,b\right]$ if and only if
> $$
> \lim_{\lambda\left(T\right)\to0}\left[D\left(T\right)-d\left(T\right)\right]=0,
> $$
> where $D\left(T\right)$ and $d\left(T\right)$ are the upper and lower Darboux sums, respectively.

### Problem 1

(Problem 6.2-1) Let $y=f\left(x\right)$ be integrable on $\left[a,b\right]$, and let $\left[c,d\right]\subset\left[a,b\right]$. Prove that $y=f\left(x\right)$ is also integrable on $\left[c,d\right]$. (Hint: use Theorem 2.2.)

### Solution to Problem 1

Since $f$ is integrable on $\left[a,b\right]$, by **Theorem 1.1** (Necessary Condition for Integrability) in Chapter 1, $f$ is bounded on $\left[a,b\right]$; set $M=\sup_{\left[a,b\right]}\left| f\left(x\right)\right|$.

Take any partition $T'$ of $\left[c,d\right]$. Extend $T'$ to a partition $T$ of $\left[a,b\right]$: on $\left[a,c\right]$ and $\left[d,b\right]$ make several subintervals each of length at most $\lambda\left(T'\right)$. Then $\lambda\left(T\right)=\lambda\left(T'\right)$.

The partition $T$ corresponds to

$$
D\left(T\right)-d\left(T\right)=\sum\omega_k\Delta x_k,
$$

where $\omega_k$ is the oscillation of $f$ on the $k$-th subinterval. On the subintervals belonging to $\left[c,d\right]$, the partition points of $T$ and $T'$ are exactly the same, and the corresponding sum of oscillation terms is precisely $D\left(T'\right)-d\left(T'\right)$; the oscillation terms contributed by the subintervals on $\left[a,c\right]$ and $\left[d,b\right]$ are nonnegative. By **Lemma 2.1** (Effect of Refining the Partition Points), as partition points are added, the lower Darboux sum does not decrease and the upper Darboux sum does not increase, hence

$$
D\left(T'\right)-d\left(T'\right)\le D\left(T\right)-d\left(T\right).
$$

Since $f$ is integrable on $\left[a,b\right]$, by **Theorem 2.2**, letting $\lambda\left(T\right)=\lambda\left(T'\right)\to0$, the right-hand side tends to $0$, so $D\left(T'\right)-d\left(T'\right)\to0$. Again by **Theorem 2.2**, $f$ is integrable on $\left[c,d\right]$. $\blacksquare$

### Problem 2

(Problem 6.2-2) Let $y=f\left(x\right)$ and $y=g\left(x\right)$ both be integrable on $\left[a,b\right]$. Prove that $f\left(x\right)\cdot g\left(x\right)$ is integrable on $\left[a,b\right]$. (Hint: use Theorem 2.2 and the inequality

$$
\omega_{fg}\left(I\right)\le M\omega_g\left(I\right)+N\omega_f\left(I\right),
$$

$\forall I\subset\left[a,b\right]$.)

### Solution to Problem 2

Since $f,g$ are both integrable, they are both bounded. Set $M=\sup_{\left[a,b\right]}\left| f\left(x\right)\right|$, $N=\sup_{\left[a,b\right]}\left| g\left(x\right)\right|$.

Take any partition $T$ of $\left[a,b\right]$. For each subinterval $I_k=\left[x_{k-1},x_k\right]$ and any $u,v\in I_k$, we have

$$
\begin{aligned}\left| f\left(u\right)g\left(u\right)-f\left(v\right)g\left(v\right)\right|&=\left| f\left(u\right)\left(g\left(u\right)-g\left(v\right)\right)+g\left(v\right)\left(f\left(u\right)-f\left(v\right)\right)\right|\\&\le M\left| g\left(u\right)-g\left(v\right)\right|+N\left| f\left(u\right)-f\left(v\right)\right|.\end{aligned}
$$

Letting $u,v$ range over $I_k$ so that $f\left(u\right)g\left(u\right)$ and $f\left(v\right)g\left(v\right)$ approach the upper and lower bounds, we get

$$
\omega_{fg}\left(I_k\right)\le M\omega_g\left(I_k\right)+N\omega_f\left(I_k\right).
$$

Summing over $k$ gives

$$
\sum_k\omega_{fg}\left(I_k\right)\Delta x_k\le M\sum_k\omega_g\left(I_k\right)\Delta x_k+N\sum_k\omega_f\left(I_k\right)\Delta x_k.
$$

Since $f,g$ are integrable on $\left[a,b\right]$, by **Theorem 2.2**, both terms on the right tend to $0$ as $\lambda\left(T\right)\to0$, so the left-hand side also tends to $0$. Again by **Theorem 2.2**, $f\cdot g$ is integrable on $\left[a,b\right]$. $\blacksquare$

### Problem 3

(Problem 6.2-4) Let $y=f\left(x\right)$ be continuous on $\left[a,b\right]$ and satisfy $f\left(x\right)\ge0$. Prove that $\int_a^b f\left(x\right)\,\mathrm{d}x=0$ if and only if $f\left(x\right)\equiv0$.

### Solution to Problem 3

**Sufficiency** If $f\left(x\right)\equiv0$, then $\int_a^b f\left(x\right)\,\mathrm{d}x=0$ clearly holds.

**Necessity** Suppose, for contradiction, that $f$ is not identically zero. Then there exists $x_0\in\left[a,b\right]$ such that $f\left(x_0\right)>0$. By the continuity of $f$ at $x_0$, for $\varepsilon=\frac{f\left(x_0\right)}{2}>0$, there exists $\delta>0$ such that when $x\in\left[a,b\right]$ and $\left| x-x_0\right|<\delta$,

$$
\left| f\left(x\right)-f\left(x_0\right)\right|<\frac{f\left(x_0\right)}2,
$$

i.e. $f\left(x\right)>\frac{f\left(x_0\right)}2$. Set

$$
J=\left[a,b\right]\cap\left(x_0-\delta,x_0+\delta\right),
$$

whose length is $\left|J\right|>0$. By **Property** (Comparison Property of Definite Integrals) in Chapter 1,

$$
\int_a^b f\left(x\right)\,\mathrm{d}x\ge\int_J f\left(x\right)\,\mathrm{d}x\ge\frac{f\left(x_0\right)}2\cdot\left|J\right|>0,
$$

which contradicts $\int_a^b f\left(x\right)\,\mathrm{d}x=0$. Hence $f\left(x\right)\equiv0$. $\blacksquare$

### Problem 4

(Problem 6.2-6) Prove that if $y=f\left(x\right)$ is integrable on $\left[a,b\right]$, then $y=\left| f\left(x\right)\right|$ is integrable, and

$$
\left|\int_a^b f\left(x\right)\,\mathrm{d}x\right|\le\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x.
$$

### Solution to Problem 4

**Integrability** Take any partition $T$ of $\left[a,b\right]$. For each subinterval $I_k$ and any $u,v\in I_k$, by the triangle inequality

$$
\left|\right| f\left(u\right)\left|-\right| f\left(v\right)\left|\right|\le\left| f\left(u\right)-f\left(v\right)\right|.
$$

Letting $u,v$ range over $I_k$, we get $\omega_{\left| f\right|}\left(I_k\right)\le\omega_f\left(I_k\right)$. Thus

$$
\sum_k\omega_{\left| f\right|}\left(I_k\right)\Delta x_k\le\sum_k\omega_f\left(I_k\right)\Delta x_k.
$$

Since $f$ is integrable, by **Theorem 2.2**, the right-hand side tends to $0$ as $\lambda\left(T\right)\to0$, so the left-hand side also tends to $0$. Again by **Theorem 2.2**, $\left| f\left(x\right)\right|$ is integrable on $\left[a,b\right]$.

**The inequality** For all $x\in\left[a,b\right]$, we have $-\left| f\left(x\right)\right|\le f\left(x\right)\le\left| f\left(x\right)\right|$. By **Property** (Comparison Property of Definite Integrals) in Chapter 1,

$$
-\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x\le\int_a^b f\left(x\right)\,\mathrm{d}x\le\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x,
$$

i.e.

$$
\left|\int_a^b f\left(x\right)\,\mathrm{d}x\right|\le\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x.
$$

$\blacksquare$
