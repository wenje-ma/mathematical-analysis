# Assignment 28

> **Proposition 1.3** (Necessary and Sufficient Condition for Rectifiability) Let $E$ be a bounded set in the plane and $\partial E$ its set of boundary points. Then $E$ is rectifiable if and only if $m^*\left(\partial E\right)=0$, i.e. $\partial E$ is a set of zero area. In particular, a bounded region whose boundary is a piecewise smooth curve is rectifiable.

> **Theorem 1.4** (Necessary and Sufficient Condition for Integrability) Let $D$ be a bounded closed region that is rectifiable. Then $z=f\left(x,y\right)$ is integrable on $D$ if and only if
> $$
> \lim_{\lambda\left(T\right)\to0}\left[D\left(T\right)-d\left(T\right)\right]=0,
> $$
> i.e. $\lim_{\lambda\left(T\right)\to0}\sum_i\omega_i\Delta\sigma_i=0$, where $\omega_i$ is the oscillation of $f$ on the small region $D_i$.

> **Theorem 1.5** (Continuous Functions Are Integrable) Let $D$ be a bounded closed region in the plane whose boundary is a set of zero area. Let $z=f\left(x,y\right)$ be continuous on $D$. Then $z=f\left(x,y\right)$ is integrable on $D$.

> **Property** (Basic Properties of Double Integrals) Let $D$ be a bounded closed region that is rectifiable, and let $f,g$ be integrable on $D$. Then:
> (2) additivity with respect to the region: if $D$ is decomposed into two rectifiable, non-overlapping regions $D_1,D_2$, then $\iint_D f=\iint_{D_1}f+\iint_{D_2}f$;
> 
> (3) the integral preserves inequalities: if $f\left(x,y\right)\le g\left(x,y\right)$ ($\forall\left(x,y\right)\in D$), then $\iint_D f\le\iint_D g$;
> 
> (4) mean value theorem for integrals: if $f$ is continuous on $D$, then there exists $\left(x_0,y_0\right)\in D$ such that $\iint_D f=f\left(x_0,y_0\right)\cdot S$, where $S$ is the area of $D$.

### Problem 1

(Problem 8.1-2) Let $z=f\left(x,y\right)$ and $z=g\left(x,y\right)$ both be integrable on a bounded closed region $D$. Prove that $z=f\left(x,y\right)\cdot g\left(x,y\right)$ is also integrable on $D$. (Hint: consider the oscillation $\omega_{f\cdot g}^{\left(i\right)}$ of $f\cdot g$ on a small region $D_i$, and prove that $\omega_{f\cdot g}^{\left(i\right)}\le A\omega_f^{\left(i\right)}+B\omega_g^{\left(i\right)}$.)

### Solution to Problem 1

Since $f,g$ are both integrable, by **Theorem 1.1** (Necessary Condition for Integrability), $f,g$ are bounded on $D$. Set $A=\sup_D\left| f\left(x,y\right)\right|$, $B=\sup_D\left| g\left(x,y\right)\right|$.

Take any partition $T$ of $D$. For each small region $D_i$ and any $P,Q\in D_i$, we have

$$
\begin{aligned}\left| f\left(P\right)g\left(P\right)-f\left(Q\right)g\left(Q\right)\right|&=\left| f\left(P\right)\left(g\left(P\right)-g\left(Q\right)\right)+g\left(Q\right)\left(f\left(P\right)-f\left(Q\right)\right)\right|\\&\le A\left| g\left(P\right)-g\left(Q\right)\right|+B\left| f\left(P\right)-f\left(Q\right)\right|.\end{aligned}
$$

Letting $P,Q$ range over $D_i$ so that $f\left(P\right)g\left(P\right)$ and $f\left(Q\right)g\left(Q\right)$ approach the upper and lower bounds, we get

$$
\omega_{fg}^{\left(i\right)}\le A\omega_g^{\left(i\right)}+B\omega_f^{\left(i\right)}.
$$

Summing over $i$ gives

$$
\sum_i\omega_{fg}^{\left(i\right)}\Delta\sigma_i\le A\sum_i\omega_g^{\left(i\right)}\Delta\sigma_i+B\sum_i\omega_f^{\left(i\right)}\Delta\sigma_i.
$$

Since $f,g$ are integrable, by **Theorem 1.4**, both terms on the right tend to $0$ as $\lambda\left(T\right)\to0$, so the left-hand side also tends to $0$. Again by **Theorem 1.4**, $f\cdot g$ is integrable on $D$. $\blacksquare$

### Problem 2

(Problem 8.1-3) Consider the function

$$
D\left(x,y\right)=
\begin{cases}
1,&\text{当 }x,y\text{ 均为有理数},\\
0,&\text{其他点 }\left(x,y\right).
\end{cases}
$$

Prove that $D\left(x,y\right)$ is not integrable on

$$
R=\left\{\left(x,y\right):0\le x\le1,0\le y\le1\right\}
$$

.

### Solution to Problem 2

Make any partition $T$ of $R$, dividing $R$ into several rectifiable small regions $D_1,\dots,D_n$. Since each small region $D_i$ is a region with interior points, it contains both rational points (both coordinates rational) and irrational points. Hence the supremum of $f$ on $D_i$ is $M_i=1$ and the infimum is $m_i=0$, so the oscillation is $\omega_i=M_i-m_i=1$. Thus the difference between the upper and lower Darboux sums is

$$
D\left(T\right)-d\left(T\right)=\sum_i\omega_i\Delta\sigma_i=\sum_i\Delta\sigma_i=1,
$$

which does not tend to $0$ as $\lambda\left(T\right)\to0$. By **Theorem 1.4**, $D\left(x,y\right)$ is not integrable on $R$. $\blacksquare$

### Problem 3

(Problem 8.1-4) Let $z=f\left(x,y\right)$ and $z=g\left(x,y\right)$ both be integrable on a region $D$, where $D$ is a bounded closed region and the boundary of $D$ consists of piecewise smooth curves. Let $\gamma$ be a line segment in the interior of $D$, and suppose $f\left(x,y\right)=g\left(x,y\right)$ for $\left(x,y\right)\in D\setminus\gamma$. Prove

$$
\iint_D f\left(x,y\right)\,\mathrm{d}\sigma=\iint_D g\left(x,y\right)\,\mathrm{d}\sigma.
$$

The conclusion of this problem tells us that modifying the function value on a line segment of the integration region does not change the value of its double integral.

### Solution to Problem 3

The line segment $\gamma$ is a piecewise smooth curve; by **Proposition 1.3**, $\gamma$ is a set of zero area. Hence the area of $\gamma$ itself is $0$, i.e.

$$
\iint_\gamma f=\iint_\gamma g=0.
$$

Decompose $D$ into the two non-overlapping regions $D\setminus\gamma$ and $\gamma$. By **Property** (Basic Properties of Double Integrals) (2) (additivity),

$$
\iint_D f=\iint_{D\setminus\gamma}f+\iint_\gamma f=\iint_{D\setminus\gamma}f,
$$

similarly $\iint_D g=\iint_{D\setminus\gamma}g$. Since $f=g$ on $D\setminus\gamma$, we have $\iint_{D\setminus\gamma}f=\iint_{D\setminus\gamma}g$. Therefore

$$
\iint_D f\left(x,y\right)\,\mathrm{d}\sigma=\iint_D g\left(x,y\right)\,\mathrm{d}\sigma.

$$

$\blacksquare$
### Problem 4

(Problem 8.1-5) Let $z=f\left(x,y\right)$ be integrable on a bounded closed region $D$. Prove that $z=\left| f\left(x,y\right)\right|$ is also integrable on $D$.

### Solution to Problem 4

Take any partition $T$ of $D$. For each small region $D_i$ and any $P,Q\in D_i$, by the triangle inequality

$$
\left|\right| f\left(P\right)\left|-\right| f\left(Q\right)\left|\right|\le\left| f\left(P\right)-f\left(Q\right)\right|.
$$

Letting $P,Q$ range over $D_i$, we get $\omega_{\left| f\right|}^{\left(i\right)}\le\omega_f^{\left(i\right)}$. Thus

$$
\sum_i\omega_{\left| f\right|}^{\left(i\right)}\Delta\sigma_i\le\sum_i\omega_f^{\left(i\right)}\Delta\sigma_i.
$$

Since $f$ is integrable, by **Theorem 1.4**, the right-hand side tends to $0$ as $\lambda\left(T\right)\to0$, so the left-hand side also tends to $0$. Again by **Theorem 1.4**, $\left| f\left(x,y\right)\right|$ is integrable on $D$. $\blacksquare$

### Problem 5

(Problem 8.1-8) Let the function $f\left(x,y\right)$ be continuous on a bounded closed region $D$ that is rectifiable, let $g\left(x,y\right)$ be greater than zero on $D$, and let $g\left(x,y\right)$ be continuous on $D$. Prove that there exists in $D$ a point $\left(x_0,y_0\right)$ such that

$$
\iint_D f\left(x,y\right)g\left(x,y\right)\,\mathrm{d}\sigma=f\left(x_0,y_0\right)\iint_D g\left(x,y\right)\,\mathrm{d}\sigma.
$$

### Solution to Problem 5

Since $f$ is continuous on the bounded closed region $D$, by **Theorem 1.5** (Continuous Functions Are Integrable), $f$ is integrable on $D$, and $f$ has a maximum $M$ and minimum $m$ on $D$. Moreover, since $g\left(x,y\right)> 0$ on $D$, we have

$$
m\,g\left(x,y\right)\le f\left(x,y\right)g\left(x,y\right)\le M\,g\left(x,y\right).
$$

By **Property** (Basic Properties of Double Integrals) (3) (comparison property),

$$
m\iint_D g\le\iint_D fg\le M\iint_D g.
$$

Since $g$ is continuous and $g> 0$, and $D$ has positive area, we have $\iint_D g> 0$. Thus

$$
m\le\frac{\iint_D fg}{\iint_D g}\le M.
$$

By the intermediate value theorem for continuous functions of two variables (properties of continuous functions in Chapter 1), there exists $\left(x_0,y_0\right)\in D$ such that $f\left(x_0,y_0\right)=\frac{\iint_D fg}{\iint_D g}$, i.e.

$$
\iint_D f\left(x,y\right)g\left(x,y\right)\,\mathrm{d}\sigma=f\left(x_0,y_0\right)\iint_D g\left(x,y\right)\,\mathrm{d}\sigma.

$$

$\blacksquare$
### Problem 6

(Problem 8.1-9) Let the function $f\left(x,y\right)$ be continuous, nonnegative, and satisfy $\iint_D f\left(x,y\right)\,\mathrm{d}x\mathrm{d}y=0$ on a bounded closed region $D$ that is rectifiable. Prove that $f\left(x,y\right)=0$ whenever $\left(x,y\right)\in D$.

### Solution to Problem 6

Suppose, for contradiction, that there exists $\left(x_0,y_0\right)\in D$ such that $f\left(x_0,y_0\right)> 0$. By the continuity of $f$ at $\left(x_0,y_0\right)$, for $\varepsilon=\frac{f\left(x_0,y_0\right)}2> 0$, there exists $\delta> 0$ such that when $\left(x,y\right)\in D$ and

$$
\sqrt{\left(x-x_0\right)^2+\left(y-y_0\right)^2}< \delta
$$

,

$$
\left| f\left(x,y\right)-f\left(x_0,y_0\right)\right|< \frac{f\left(x_0,y_0\right)}2,
$$

i.e. $f\left(x,y\right)> \frac{f\left(x_0,y_0\right)}2$. Set

$$
R_\delta=D\cap\left\{\left(x,y\right):\sqrt{\left(x-x_0\right)^2+\left(y-y_0\right)^2}< \delta\right\}.
$$

Since $\left(x_0,y_0\right)$ is an interior or boundary point of $D$, $R_\delta$ is a rectifiable region with area $\left|R_\delta\right|> 0$. By **Property** (Basic Properties of Double Integrals) (3),

$$
\iint_D f\left(x,y\right)\,\mathrm{d}\sigma\ge\iint_{R_\delta}f\left(x,y\right)\,\mathrm{d}\sigma\ge\frac{f\left(x_0,y_0\right)}2\cdot\left|R_\delta\right|> 0,
$$

which contradicts $\iint_D f=0$. Hence $f\left(x,y\right)\equiv0$ on $D$. $\blacksquare$
