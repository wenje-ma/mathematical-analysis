# Mathematical Analysis

## Real Numbers

**Definition** (Field)

Roughly speaking, a set of numbers that is closed under addition, subtraction, multiplication and division (where the divisor is not $0$), and that satisfies the commutative, associative and distributive laws, is called a field.

**Definition** (Ordered Field)

A number field on which an order relation is defined and which satisfies the following properties is called an ordered field: for any $\alpha,b$, exactly one of $\alpha=b$, $\alpha< b$, $b< \alpha$ holds; and when $a< b,b< c$ then $a< c$; when $a< b$ then $a+c< b+c$; when $0< a,b$ then $a\cdot b> 0$.

**Proposition 1.1** (The Field of Rational Numbers Is an Ordered Field)

The field of rational numbers $\mathbb Q$ is an ordered field.

**Definition** (Density)

A number set $S$ is said to be everywhere dense on the number line if, for any interval $\left(a,b\right)$ on the number line, no matter where it lies or how small it is, there is at least one number of $S$ lying in $\left(a,b\right)$, i.e. $S\cap\left(a,b\right)\ne\varnothing$.

**Proposition 1.3** ($\sqrt2$ Is Irrational)

$\sqrt2$ is not a rational number.

**Example 1.1** (Operations on Irrational Numbers)

The sum of an irrational number and a rational number is irrational. The product of an irrational number and a rational number is irrational.

**Definition** (Completeness)

An ordered number field satisfying the following requirement is called complete (or continuous): for any monotonically increasing bounded sequence $\left\{x_n\right\}$, there exists a number $a$ in the field such that $x_n$ can approach $a$ arbitrarily closely.

**Proposition 1.5** (Completeness of the Real Number Field)

Let $\left\{x_n\right\}$ be any monotonically increasing sequence bounded above in the real number field $\mathbb R$. Then there exists a number $a$ in $\mathbb R$ such that $x_n\le a$, and $x_n$ can approach $a$ arbitrarily closely.

**Definition** (Bounded Set)

Let $E\subset\mathbb R$. If there exists $M$ such that every point $x$ in $E$ satisfies $x\le M$, then $E$ is said to be bounded above; if there exists $m$ such that every point $x$ in $E$ satisfies $x\ge m$, then $E$ is said to be bounded below; a set that is both bounded above and bounded below is called a bounded set.

**Proposition 1.6** (Properties of the Absolute Value)

For any $x,y\in\mathbb R$, we have:

(1) $\left|x\right|\ge0$, with equality if and only if $x=0$;

(2) $\left|-x\right|=\left|x\right|$;

(3) $\left|x+y\right|\le\left|x\right|+\left|y\right|$.

**Proposition 1.7** (Triangle Inequality)

For any real numbers $a,b,c$, we have:

(1) $\left|a-b\right|\ge0$, with equality if and only if $a=b$;

(2) $\left|a-b\right|=\left|b-a\right|$;

(3) $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

## The Concept of a Function

**Definition** (Function)

Let $x$ and $y$ be two variables taking values in the sets of real numbers $X$ and $Y$, respectively. If there is a rule $f$ such that to each value $x\in X$ there corresponds a uniquely determined $y\in Y$, then $f$ is called a function, denoted $f:X\to Y$, and $X$ is called the domain of $f$. The set of all possible function values taken from $Y$ is called the range of $f$, denoted $f\left(X\right)$.

**Definition** (Composite Function)

Suppose there are two functions $f:X\to Y$ and $g:Y^*\to Z$, and suppose $Y\subset Y^*$. For each point $x\in X$, there is a unique $y=f\left(x\right)\in Y$, and then $g$ gives $z=g\left(y\right)$. The correspondence $x\mapsto z$ from $X$ to $Z$ determined in this way, where $z=g\left(f\left(x\right)\right)$, is called the composite function of $f$ and $g$, denoted $z=g\left(f\left(x\right)\right)$.

**Definition** (Periodic Function)

Let $y=f\left(x\right)$ be defined on $\mathbb R$, and suppose there exists a number $T\ne 0$ such that $f\left(x+T\right)=f\left(x\right),\forall x\in\mathbb R$. Then $y=f\left(x\right)$ is called a periodic function, and $T$ is called a period of $f$.

**Proposition 2.1** (Necessary and Sufficient Condition for a Function to Be Bounded)

A function $f:X\to Y$ is bounded if and only if there exists $M> 0$ such that $\left|f\left(x\right)\right|\le M,\forall x\in X$.

## Limits of Sequences

**Definition** (Limit of a Sequence)

Let $\left\{a_n\right\}$ be a given sequence. If there exists a real number $l$ such that, for any given positive number $\epsilon$, no matter how small, there is a natural number $N$ such that $\left|a_n-l\right|< \epsilon$ whenever $n> N$, then $a_n$ is said to have limit $l$, denoted

$$
\lim\limits_{n\to\infty}a_n=l.
$$

**Example 3.3** (The $n$-th Root of a Positive Number Tends to $1$)

Let $a$ be any positive number. Then

$$
\lim\limits_{n\to\infty}a^{1/n}=1.
$$

**Theorem 3.1** (Arithmetic of Limits)

Let $\left\{a_n\right\}$ and $\left\{b_n\right\}$ both have limits, their limits being $l_1$ and $l_2$, respectively. Then

$$
\begin{aligned}
\lim\left(a_n\pm b_n\right)&=l_1\pm l_2,\\
\lim\left(a_n\cdot b_n\right)&=l_1\cdot l_2,\\
\lim\frac{a_n}{b_n}&=\frac{l_1}{l_2}.
\end{aligned}
$$

**Theorem 3.2** (Completeness of the Real Number Field)

Let $\left\{a_n\right\}$ be a monotonically increasing sequence of real numbers bounded above. Then there exists $l\in\mathbb R$ such that $\left\{a_n\right\}$ has limit $l$. In short, every monotonically increasing sequence bounded above has a limit.

## Basic Properties of Sequence Limits

**Theorem 4.2** (Squeeze Theorem)

Let $\left\{a_n\right\},\left\{b_n\right\},\left\{c_n\right\}$ be three sequences, and suppose there exists a natural number $N_0$ such that $c_n\le a_n\le b_n,\forall n\ge N_0$. If both $c_n$ and $b_n$ have limits and both equal $l$, then the limit of $a_n$ exists and also equals $l$.

**Important Limit** (The Number $e$)

$$
\lim\limits_{n\to\infty}\left(1+\frac1n\right)^n=e.
$$

where $e$ is irrational and $2< e< 3$.

**Definition** (Infinitesimal)

A variable whose limit is $0$ is called an infinitesimal.

## Limits of Functions

**Definition** (Limit of a Function)

Let $y=f\left(x\right)$ be defined in a deleted neighborhood $\left(a-r,a+r\right)\backslash\left\{a\right\}$ of the point $a$. If there exists a real number $l$ such that, for any given $\epsilon> 0$, no matter how small, there is a $\delta> 0$ such that $\left|f\left(x\right)-l\right|< \epsilon$ whenever $0< \left|x-a\right|< \delta$, then $f\left(x\right)$ is said to have limit $l$ as $x\to a$, denoted

$$
\lim\limits_{x\to a}f\left(x\right)=l.
$$

**Definition** (One-Sided Limit)

If $f\left(x\right)$ has limit $l$ as $x\to a+0$ (or $x\to a-0$), it is called the right-hand limit (or left-hand limit), denoted

$$
\begin{aligned}
\lim\limits_{x\to a+0}f\left(x\right)&=l,\\
\lim\limits_{x\to a-0}f\left(x\right)&=l.
\end{aligned}
$$

**Theorem 5.1** (Arithmetic of Function Limits)

If $\lim f\left(x\right)=l_1$ and $\lim g\left(x\right)=l_2$, then

$$
\begin{aligned}
\lim\left(f\pm g\right)&=l_1\pm l_2,\\
\lim\left(f\cdot g\right)&=l_1\cdot l_2,\\
\lim\frac{f}{g}&=\frac{l_1}{l_2}\left(l_2\ne0\right).
\end{aligned}
$$

**Proposition** (Sign-Preserving Property)

If $\lim\limits_{x\to a}f\left(x\right)=l$ and $l\ne0$, then there exists $\delta> 0$ such that $\left|f\left(x\right)\right|> \frac{\left|l\right|}{2}$ whenever $0< \left|x-a\right|< \delta$.

## Properties of Function Limits

**Proposition 6.1** (Important Limit $\lim\limits_{x\to0}\frac{\sin x}{x}=1$)

$$
\lim\limits_{x\to0}\frac{\sin x}{x}=1.
$$

**Important Limit** (The Functional Version of the Number $e$)

$$
\lim\limits_{x\to\infty}\left(1+\frac1x\right)^x=e.
$$

**Theorem 6.2** (Squeeze Theorem for Functions)

Let

$$
y=f\left(x\right),y=g\left(x\right),y=h\left(x\right)
$$

be defined in a deleted neighborhood of the point $a$, with $h\left(x\right)\le f\left(x\right)\le g\left(x\right)$. If $\lim g\left(x\right)=\lim h\left(x\right)=l$, then

$$
\lim f\left(x\right)=l.
$$

## Continuous Functions

**Definition** (Continuous Function)

Suppose $y=f\left(x\right)$ is defined on $\left(a,b\right)$. If at a point $x_0\in\left(a,b\right)$ we have $\lim\limits_{x\to x_0}f\left(x\right)=f\left(x_0\right)$, then $y=f\left(x\right)$ is said to be continuous at $x_0$. If $y=f\left(x\right)$ is continuous at every point of $\left(a,b\right)$, it is said to be continuous on $\left(a,b\right)$.

**Theorem 7.2** (Continuity of Composite Functions)

If $y=g\left(y\right)$ is continuous at $y_0$, $y=f\left(x\right)$ is continuous at $x_0$ and $f\left(x_0\right)=y_0$, then the composite function $y=g\left(f\left(x\right)\right)$ is continuous at $x_0$.

**Definition** (Elementary Functions)

Elementary functions are continuous on their domains.

## Properties of Continuous Functions on a Closed Interval

**Theorem 8.1** (Intermediate Value Theorem)

Let $y=f\left(x\right)$ be continuous on the closed interval $\left[a,b\right]$, and suppose $f\left(a\right)$ and $f\left(b\right)$ have opposite signs. Then there exists a point $c\in\left(a,b\right)$ such that $f\left(c\right)=0$. More generally, $f$ takes every value between $f\left(a\right)$ and $f\left(b\right)$.

**Theorem 8.2** (Boundedness Theorem)

A continuous function on a closed interval is bounded and attains its maximum and minimum values.

**Nested Interval Principle**

Let $\left\{\left[a_n,b_n\right]\right\}$ be a sequence of closed intervals satisfying $\left[a_{n+1},b_{n+1}\right]\subset\left[a_n,b_n\right]$ and $b_n-a_n\to0$. Then there exists a unique real number $l$ belonging to all the intervals.

## Derivatives of Composite and Inverse Functions

**Theorem 2.1** (Chain Rule)

Let $y=f\left(u\right)$ be differentiable at $u$, and $u=g\left(x\right)$ differentiable at $x$. Then the composite function $y=f\left(g\left(x\right)\right)$ is differentiable at $x$, and

$$
\frac{\mathrm dy}{\mathrm dx}=\frac{\mathrm dy}{\mathrm du}\cdot\frac{\mathrm du}{\mathrm dx}=f'\left(g\left(x\right)\right)g'\left(x\right).
$$

## The Concept of the Differential

**Definition** (Differential)

Let $y=f\left(x\right)$ be defined near $x_0$. If there exists a constant $A$ such that $\Delta y=A\Delta x+o\left(\Delta x\right)$, then $f$ is said to be differentiable at $x_0$, and $\mathrm dy=A\Delta x$ is called the differential, with $A=f'\left(x_0\right)$.

**Definition** (Higher-Order Infinitesimal)

If

$$
\lim\limits_{x\to0}\frac{\alpha\left(x\right)}{\beta\left(x\right)}=0,
$$

then $\alpha\left(x\right)=o\left(\beta\left(x\right)\right)$ is said to hold.

## Higher-Order Derivatives and Differentials

**Definition** (Higher-Order Derivatives)

If the derivative $f'\left(x\right)$ of $y=f\left(x\right)$ is itself differentiable at $x_0$, then its derivative is called the second derivative of $f$, denoted $f''\left(x_0\right)$ or $\frac{\mathrm d^2f}{\mathrm dx^2}$. In general, the $n$-th derivative $f^{\left(n\right)}\left(x\right)$ is obtained by differentiating the $n-1$-th derivative.

## Invariance of the Form of the First Differential

**Theorem 5.1** (Derivative of a Parametric Function)

Let $x=\varphi\left(t\right),y=\psi\left(t\right)$ be differentiable at $t_0$, with $\varphi'\left(t_0\right)\ne0$. Then the derivative of the parametric function is

$$
\frac{\mathrm dy}{\mathrm dx}=\frac{\psi'\left(t\right)}{\varphi'\left(t\right)}.
$$

## The Lagrange Mean Value Theorem

**Theorem 1.1** (Fermat's Theorem)

Let $f\left(x\right)$ be defined near a point $a$ and differentiable at $a$. If $a$ is an extremum point of $y=f\left(x\right)$, then $f'\left(a\right)=0$.

**Theorem 1.2** (Rolle's Theorem)

Let $y=f\left(x\right)$ be continuous on the closed interval $\left[a,b\right]$, differentiable everywhere in $\left(a,b\right)$, and satisfy $f\left(a\right)=f\left(b\right)$. Then there exists at least one point $c$ in $\left(a,b\right)$ such that $f'\left(c\right)=0$.

**Theorem 1.3** (Lagrange Mean Value Theorem)

Let $y=f\left(x\right)$ be continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$. Then there exists a point $c\in\left(a,b\right)$ such that
$$
f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}.
$$
**Theorem 1.4** (Constancy Theorem)

Let $y=f\left(x\right)$ be differentiable everywhere in $\left(a,b\right)$ and satisfy $f'\left(x\right)=0$($x\in\left(a,b\right)$). Then $y=f\left(x\right)$ must be constant on $\left(a,b\right)$.

**Theorem 1.5** (Monotonicity Criterion)

Let $y=f\left(x\right)$ be continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$. If $f'\left(x\right)> 0$($\ge 0$)$\forall x\in\left(a,b\right)$, then $y=f\left(x\right)$ is strictly increasing (increasing) on $\left[a,b\right]$; if $f'\left(x\right)< 0$($\le 0$)$\forall x\in\left(a,b\right)$, then $y=f\left(x\right)$ is strictly decreasing (decreasing) on $\left[a,b\right]$.

## Cauchy Mean Value Theorem and L'Hôpital's Rule

**Theorem 2.1** (Cauchy Mean Value Theorem)

Let $y=f\left(x\right)$ and $y=g\left(x\right)$ be continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$, with $g'\left(x\right)\ne0$($a< x< b$). Then there exists a point $c\in\left(a,b\right)$ such that
$$
\frac{f\left(b\right)-f\left(a\right)}{g\left(b\right)-g\left(a\right)}=\frac{f'\left(c\right)}{g'\left(c\right)}.
$$
**Theorem 2.2** (L'Hôpital's Rule, $\frac00$ Form)

Let $y=f\left(x\right)$ and $y=g\left(x\right)$ be defined and differentiable in a deleted neighborhood of the point $a$, with $g'\left(x\right)\ne0$. Suppose $\lim\limits_{x\to a}f\left(x\right)=\lim\limits_{x\to a}g\left(x\right)=0$, and $\lim\limits_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ exists. Then
$$
\lim_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}.
$$
**Theorem 2.3** (L'Hôpital's Rule, $\frac{\infty}{\infty}$ Form)

Let $y=f\left(x\right)$ and $y=g\left(x\right)$ be defined and differentiable in a deleted neighborhood of the point $a$, with $g'\left(x\right)\ne0$. Suppose

$$
\lim\limits_{x\to a}f\left(x\right)=\lim\limits_{x\to a}g\left(x\right)=\infty,
$$

and $\lim\limits_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ exists. Then
$$
\lim_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}.
$$
## Extrema Problems

**Theorem 3.1** (First Sufficient Condition for an Extremum Point)

Let $y=f\left(x\right)$ be differentiable on $\left(a,b\right)$, and let $x_0\in\left(a,b\right)$ be a stationary point of $f$, i.e. $f'\left(x_0\right)=0$. If there exists $r> 0$ such that the interval $\left(x_0-r,x_0+r\right)\subset\left(a,b\right)$, with $f'\left(x\right)> 0$ when $x\in\left(x_0-r,x_0\right)$ and $f'\left(x\right)< 0$ when $x\in\left(x_0,x_0+r\right)$, then $f\left(x_0\right)$ is a local maximum; if $f'\left(x\right)< 0$ when $x\in\left(x_0-r,x_0\right)$ and $f'\left(x\right)> 0$ when $x\in\left(x_0,x_0+r\right)$, then $f\left(x_0\right)$ is a local minimum.

**Theorem 3.2** (Second Sufficient Condition for an Extremum Point)

Let $y=f\left(x\right)$ be differentiable on $\left(a,b\right)$, let $x_0\in\left(a,b\right)$ be its stationary point, and suppose $f$ has a second derivative at $x_0$. If $f''\left(x_0\right)> 0$, then $x_0$ is a local minimum point; if $f''\left(x_0\right)< 0$, then $x_0$ is a local maximum point.

**Proposition 3.1** (The Unique Extremum Point Is the Global Extremum Point)

Let $y=f\left(x\right)$ be continuous on the interval $\left(a,b\right)$ (or $\left[a,b\right]$). If $x_0$ is the only extremum point in $\left(a,b\right)$, then when $x_0$ is a local maximum point, $f\left(x_0\right)$ is the maximum value of $y=f\left(x\right)$; and when $x_0$ is a local minimum point, $f\left(x_0\right)$ is the minimum value of $y=f\left(x\right)$.

## Taylor Formula

**Theorem 4.1** (Local Taylor Expansion)

Let $y=f\left(x\right)$ be defined near the point $x_0$, and suppose it has an $n$-th derivative $f^{\left(n\right)}\left(x_0\right)$. Then
$$
f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\frac{f''\left(x_0\right)}{2!}\left(x-x_0\right)^2+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right)\left(x\to x_0\right).
$$
**Theorem 4.2** (Taylor Formula with Lagrange Remainder)

Let $y=f\left(x\right)$ have $n$ continuous derivatives on $\left[a,b\right]$ and an $n+1$-th derivative on $\left(a,b\right)$. Then for any $x,x_0\in\left[a,b\right]$, there exists a point $\xi$ lying between $x_0$ and $x$ such that
$$
f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+\frac{f^{\left(n+1\right)}\left(\xi\right)}{\left(n+1\right)!}\left(x-x_0\right)^{n+1}.
$$
## Convexity and Concavity of Functions and Sketching Graphs

**Definition** (Convex Function)

Let $y=f\left(x\right)$ be defined on $\left(a,b\right)$. If for any two points $x_1$ and $x_2$ in $\left(a,b\right)$ ($x_1< x_2$) we always have
$$
f\left(tx_1+\left(1-t\right)x_2\right)\le tf\left(x_1\right)+\left(1-t\right)f\left(x_2\right),
$$
where $t$ is any number in $\left(0,1\right)$, then $y=f\left(x\right)$ is called a convex function on $\left(a,b\right)$. Conversely, if the above inequality holds in the reverse direction, then $y=f\left(x\right)$ is called a concave function on $\left(a,b\right)$.

**Theorem 5.1** (Second-Derivative Criterion for Convexity)

Let $y=f\left(x\right)$ be twice differentiable on $\left(a,b\right)$. Then $y=f\left(x\right)$ is convex on $\left(a,b\right)$ if and only if $f''\left(x\right)\ge0$ ($\forall x\in\left(a,b\right)$); $y=f\left(x\right)$ is concave on $\left(a,b\right)$ if and only if $f''\left(x\right)\le0$ ($\forall x\in\left(a,b\right)$).

## Antiderivatives and Indefinite Integrals

**Definition** (Antiderivative and Indefinite Integral)

Let $y=f\left(x\right)$ be defined on the interval $\left(a,b\right)$. If $F\left(x\right)$ is differentiable on $\left(a,b\right)$ and $F'\left(x\right)=f\left(x\right)$ ($\forall x\in\left(a,b\right)$), then $y=F\left(x\right)$ is called an antiderivative of $y=f\left(x\right)$. All antiderivatives $F\left(x\right)+C$ of $f\left(x\right)$ ($C$ being an arbitrary constant) are called the indefinite integral of $f\left(x\right)$, denoted
$$
\int f\left(x\right)\,\mathrm{d}x=F\left(x\right)+C.
$$
**Theorem 1.3** (Linearity of the Indefinite Integral)

Let $y=f\left(x\right)$ and $y=g\left(x\right)$ have antiderivatives on some interval. Then
$$
\int\left[af\left(x\right)+bg\left(x\right)\right]\mathrm{d}x=a\int f\left(x\right)\,\mathrm{d}x+b\int g\left(x\right)\,\mathrm{d}x,
$$
where $a,b$ are two arbitrary constants.

## Substitution Rules for Indefinite Integrals

**Theorem 2.1** (First Substitution Rule)

Let $F'\left(u\right)=f\left(u\right)$, and let $u=\varphi\left(x\right)$ be differentiable. Then
$$
\int f\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm{d}x=F\left(\varphi\left(x\right)\right)+C.
$$
**Theorem 2.2** (Second Substitution Rule)

Let $x=\varphi\left(t\right)$ be differentiable and have an inverse function, and suppose

$$
\int f\left(\varphi\left(t\right)\right)\varphi'\left(t\right)\,\mathrm{d}t=G\left(t\right)+C,
$$

then
$$
\int f\left(x\right)\,\mathrm{d}x=G\left(\varphi^{-1}\left(x\right)\right)+C.
$$
## Integration by Parts

**Theorem 3.1** (Integration by Parts Formula)

Let $u\left(x\right),v\left(x\right)$ be differentiable. Then
$$
\int u\left(x\right)\,\mathrm{d}v\left(x\right)=u\left(x\right)v\left(x\right)-\int v\left(x\right)\,\mathrm{d}u\left(x\right).
$$
## Integration of Rational Functions

**Theorem 4.1** (Decomposition of Rational Functions)

Any rational function $\frac{P\left(x\right)}{Q\left(x\right)}$ can be decomposed into the sum of a polynomial and several partial fractions, each partial fraction having the form $\frac{A}{\left(x-a\right)^k}$ or $\frac{Bx+C}{\left(x^2+px+q\right)^m}$ ($p^2-4q< 0$).

## Rationalization Methods for Indefinite Integrals

**Theorem 5.1** (Integration of Rational Expressions in Trigonometric Functions)

The indefinite integral of a rational expression in trigonometric functions $R\left(\sin x,\cos x\right)$ can always be reduced, through the universal substitution $t=\tan\frac{x}{2}$, to an indefinite integral of a rational function in $t$. In this case,

$$
\begin{aligned}
\sin x&=\frac{2t}{1+t^2},\\
\cos x&=\frac{1-t^2}{1+t^2},\\
\mathrm{d}x&=\frac{2\,\mathrm{d}t}{1+t^2}.
\end{aligned}
$$

## Supremum and Infimum of Sets of Real Numbers

**Definition** (Supremum and Infimum)

Let $E$ be a bounded set. If there exists a real number $\beta$ satisfying:
(1) $\beta$ is an upper bound of $E$ ($\forall x\in E,x\le\beta$);

(2) for any $\epsilon> 0$, there exists $x_0\in E$ such that $x_0> \beta-\epsilon$, then $\beta$ is called the supremum of $E$, denoted $\sup E$. The infimum $\inf E$ is defined similarly.

**Definition** (Oscillation)

Let $f\left(x\right)$ be defined and bounded on the interval $I$. The quantity

$$
\omega_f\left(I\right)=\sup\left\{f\left(x\right):x\in I\right\}-\inf\left\{f\left(x\right):x\in I\right\}
$$

is called the oscillation of $f$ on $I$.

**Theorem 1.3** (Necessary and Sufficient Condition for Continuity)

Let $y=f\left(x\right)$ be a bounded function near the point $x_0$. Then $f$ is continuous at $x_0$ if and only if $\omega_f\left(x_0\right)=0$.

## Limit Superior and Limit Inferior and the Cauchy Convergence Principle

**Theorem 2.1** (Limit Superior, Limit Inferior and Existence of a Limit)

Let $\left\{a_n\right\}$ be a bounded sequence. Then the sequence $\left\{a_n\right\}$ has a limit if and only if its limit superior and limit inferior are equal.

**Theorem 2.2** (Cauchy Convergence Principle)

The sequence $\left\{a_n\right\}$ has a limit if and only if: for any given $\epsilon> 0$, there exists a natural number $N$ such that $\left|a_n-a_m\right|< \epsilon$ (whenever $m\ge N,n\ge N$).

## Uniform Continuity of Continuous Functions on a Closed Interval

**Definition** (Uniform Continuity)

Let $y=f\left(x\right)$ be defined on an interval $X$. If, for any given $\epsilon> 0$, there exists a $\delta> 0$ such that for any two points $x_1$ and $x_2$ in $X$ we have $\left|f\left(x_1\right)-f\left(x_2\right)\right|< \epsilon$ (whenever $\left|x_1-x_2\right|< \delta$), then $y=f\left(x\right)$ is said to be uniformly continuous on $X$.

**Theorem 3.2** (Finite Cover Theorem)

Let $\mathcal{F}=\left\{I_\alpha:\alpha\in A\right\}$ be any open cover of the closed interval $\left[a,b\right]$. Then there exist finitely many elements $I_{\alpha_1},\cdots,I_{\alpha_n}$ of $\mathcal{F}$ such that

$$
\left[a,b\right]\subset\bigcup\limits_{k=1}^n I_{\alpha_k}.
$$

## The Basic Concept of the Definite Integral

**Definition** (Definite Integral)

Let $f\left(x\right)$ be defined on the interval $\left[a,b\right]$. Partition $\left[a,b\right]$ as

$$
T:a=x_0< x_1< \cdots< x_n=b,
$$
and set $\Delta x_k=x_k-x_{k-1}$, $\lambda\left(T\right)=\max_{1\le k\le n}\Delta x_k$. If there exists a constant $I$ such that, for any $\epsilon> 0$, there exists $\delta> 0$ such that, whenever $\lambda\left(T\right)< \delta$, no matter how the partition $T$ is chosen and no matter how the intermediate points $\xi_k\in\left[x_{k-1},x_k\right]$ are chosen, we always have

$$
\left|\sum_{k=1}^n f\left(\xi_k\right)\Delta x_k-I\right|< \epsilon,
$$

then $I$ is called the definite integral of $f\left(x\right)$ on $\left[a,b\right]$, denoted

$$
\int_a^b f\left(x\right)\,\mathrm{d}x.
$$

**Property** (Comparison Property of the Definite Integral)

Let $f,g$ be integrable on $\left[a,b\right]$, with $f\left(x\right)\le g\left(x\right)$ ($\forall x\in\left[a,b\right]$). Then

$$
\begin{aligned}
\int_a^b f\left(x\right)\,\mathrm{d}x&\le\int_a^b g\left(x\right)\,\mathrm{d}x,\\
\int_a^b f\left(x\right)\,\mathrm{d}x&\ge0.
\end{aligned}
$$

## Integrability of Continuous Functions

**Lemma 2.1** (Effect of Refining the Partition Points)

Let $T'$ be a partition obtained from the partition $T$ by adding finitely many partition points. Then $d\left(T\right)\le d\left(T'\right)$ and $D\left(T'\right)\le D\left(T\right)$, i.e. when the partition points are added, the Darboux lower sum does not decrease and the Darboux upper sum does not increase.

**Theorem 2.2** (Necessary and Sufficient Condition for Integrability)

Let $y=f\left(x\right)$ be bounded on $\left[a,b\right]$. Then $y=f\left(x\right)$ is Riemann integrable on $\left[a,b\right]$ if and only if

$$
\lim_{\lambda\left(T\right)\to0}\left[D\left(T\right)-d\left(T\right)\right]=0,
$$

where $D\left(T\right)$ and $d\left(T\right)$ are the Darboux upper sum and the Darboux lower sum, respectively.

## The Concept of the Double Integral

**Proposition 1.3** (Necessary and Sufficient Condition for Rectifiability of Area)

Let $E$ be a bounded set in the plane, and let $\partial E$ be the set of its boundary points. Then $E$ is rectifiable in area if and only if $m^*\left(\partial E\right)=0$, i.e. $\partial E$ is a set of zero area. In particular, a bounded region whose boundary is a piecewise smooth curve is rectifiable in area.

**Theorem 1.4** (Necessary and Sufficient Condition for Integrability)

Let $D$ be a bounded closed region rectifiable in area. Then $z=f\left(x,y\right)$ is integrable on $D$ if and only if

$$
\begin{aligned}
\lim_{\lambda\left(T\right)\to0}\left[D\left(T\right)-d\left(T\right)\right]&=0,\\
\lim_{\lambda\left(T\right)\to0}\sum_i\omega_i\Delta\sigma_i&=0.
\end{aligned}
$$

where $\omega_i$ is the oscillation of $f$ on the small region $D_i$.

**Theorem 1.5** (Continuous Functions Are Integrable)

Let $D$ be a bounded closed region in the plane whose boundary is a set of zero area, and let $z=f\left(x,y\right)$ be continuous on $D$. Then $z=f\left(x,y\right)$ is integrable on $D$.

**Property** (Basic Properties of the Double Integral)

Let $D$ be a bounded closed region rectifiable in area, and let $f,g$ be integrable on $D$. Then:

(2) additivity of the integral over the region: if $D$ is decomposed into two non-overlapping regions $D_1,D_2$ that are rectifiable in area, then

$$
\iint_D f=\iint_{D_1}f+\iint_{D_2}f;
$$

(3) the integral preserves inequalities: if $f\left(x,y\right)\le g\left(x,y\right)$ ($\forall\left(x,y\right)\in D$), then

$$
\iint_D f\le\iint_D g;
$$

(4) mean value theorem for integrals: if $f$ is continuous on $D$, then there exists $\left(x_0,y_0\right)\in D$ such that $\iint_D f=f\left(x_0,y_0\right)\cdot S$, where $S$ is the area of $D$.

## Computation of Double Integrals

**Theorem 2.1** (Reducing a Double Integral to an Iterated Integral)

Let $z=f\left(x,y\right)$ be continuous on the closed region $D$,

$$
D=\left\{\left(x,y\right):a\le x\le b,\varphi_1\left(x\right)\le y\le\varphi_2\left(x\right)\right\},
$$

where $\varphi_1,\varphi_2$ are continuous on $\left[a,b\right]$. Then

$$
\iint_D f\left(x,y\right)\,\mathrm{d}x\mathrm{d}y=\int_a^b\mathrm{d}x\int_{\varphi_1\left(x\right)}^{\varphi_2\left(x\right)}f\left(x,y\right)\,\mathrm{d}y.
$$

**Theorem 2.2** (Double Integrals in Polar Coordinates)

Let $D$ be a bounded closed region rectifiable in area, and let $z=f\left(x,y\right)$ be integrable on $D$. Then

$$
\iint_D f\left(x,y\right)\,\mathrm{d}x\mathrm{d}y=\iint_{D^*}f\left(r\cos\theta,r\sin\theta\right)\,r\,\mathrm{d}r\mathrm{d}\theta,
$$

where

$$
D^*=\left\{\left(r,\theta\right):\left(r\cos\theta,r\sin\theta\right)\in D\right\}.
$$

## General Change-of-Variables Rule for Double Integrals

**Theorem 3.1** (Change-of-Variables Formula for Double Integrals)

Let $z=f\left(x,y\right)$ be continuous on a bounded closed region $D$ rectifiable in area. Let the transformation

$$
F:\left(u,v\right)\mapsto\left(x\left(u,v\right),y\left(u,v\right)\right)
$$

be a one-to-one map from a bounded closed region $G$ onto $D$, where $x\left(u,v\right),y\left(u,v\right)$ have continuous first-order partial derivatives on $G$, and the Jacobian determinant $J\left(u,v\right)=\frac{\partial\left(x,y\right)}{\partial\left(u,v\right)}\ne0$. Then

$$
\iint_D f\left(x,y\right)\,\mathrm{d}x\mathrm{d}y=\iint_G f\left(x\left(u,v\right),y\left(u,v\right)\right)\left| J\left(u,v\right)\right|\,\mathrm{d}u\mathrm{d}v.
$$

In particular, the area of the region $D$ is

$$
m\left(D\right)=\iint_G\left| J\left(u,v\right)\right|\,\mathrm{d}u\mathrm{d}v.
$$

## The Concept and Computation of Triple Integrals

**Theorem 4.2** (Cross-Section Method for Triple Integrals)

Let

$$
\Omega=\left\{\left(x,y,z\right):\left(x,y\right)\in D,z_1\left(x,y\right)\le z\le z_2\left(x,y\right)\right\},
$$

where $D$ is a bounded closed region rectifiable in area in the $Oxy$ plane, $z_1,z_2$ are continuous on $D$, and $f$ is continuous on $\Omega$. Then

$$
\iiint_\Omega f\left(x,y,z\right)\,\mathrm{d}V=\iint_D\mathrm{d}x\mathrm{d}y\int_{z_1\left(x,y\right)}^{z_2\left(x,y\right)}f\left(x,y,z\right)\,\mathrm{d}z.
$$

**Theorem 4.4** (Change-of-Variables Formula for Triple Integrals)

Under the change of variables $x=x\left(u,v,w\right)$, $y=y\left(u,v,w\right)$, $z=z\left(u,v,w\right)$,

$$
\iiint_\Omega f\,\mathrm{d}x\mathrm{d}y\mathrm{d}z=\iiint_{\Omega'}f\left(x\left(u,v,w\right),y\left(u,v,w\right),z\left(u,v,w\right)\right)\left| J\left(u,v,w\right)\right|\,\mathrm{d}u\mathrm{d}v\mathrm{d}w,
$$

where $J=\frac{\partial\left(x,y,z\right)}{\partial\left(u,v,w\right)}$. In particular, in cylindrical coordinates $\left(r,\theta,z\right)$ we have $\left| J\right|=r$, and in spherical coordinates $\left(\rho,\varphi,\theta\right)$ we have $\left| J\right|=\rho^2\sin\varphi$.

## Examples of Applications of Multiple Integrals

**Proposition 5.1** (Surface Area Formula)

Let $z=f\left(x,y\right)$ have continuous first-order partial derivatives on a bounded closed region $D$ rectifiable in area. Then the area of the surface $z=f\left(x,y\right)$ ($\left(x,y\right)\in D$) is

$$
S=\iint_D\sqrt{1+f_x^2\left(x,y\right)+f_y^2\left(x,y\right)}\,\mathrm{d}x\mathrm{d}y.
$$

**Formula** (Coordinates of the Center of Mass)

Let a body occupy the region $\Omega$ with density $\rho\left(x,y,z\right)$ and mass $m=\iiint_\Omega\rho\,\mathrm{d}V$. Then the coordinates of the center of mass are

$$
\begin{aligned}
x_0&=\frac1m\iiint_\Omega x\rho\,\mathrm{d}V,\\
y_0&=\frac1m\iiint_\Omega y\rho\,\mathrm{d}V,\\
z_0&=\frac1m\iiint_\Omega z\rho\,\mathrm{d}V.
\end{aligned}
$$

**Formula** (Moment of Inertia)

The moment of inertia of the body about the $z$-axis is

$$
J_z=\iiint_\Omega\left(x^2+y^2\right)\rho\left(x,y,z\right)\,\mathrm{d}V.
$$

## Line Integrals of the First Kind

**Theorem 1.2** (Arc Length Formula for a Smooth Curve)

Let the parametric equations of a space curve $L$ be $x=x\left(t\right)$, $y=y\left(t\right)$, $z=z\left(t\right)$ ($\alpha\le t\le\beta$), with $x'\left(t\right),y'\left(t\right),z'\left(t\right)$ continuous on $\left[\alpha,\beta\right]$. Then $L$ is rectifiable, and its arc length is

$$
s=\int_\alpha^\beta\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm{d}t.
$$

The arc differential is

$$
\mathrm{d}s=\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm{d}t.
$$

**Theorem 1.3** (Computation of Line Integrals of the First Kind)

Let $L$ be a smooth curve with the parametric equations given above, and let $f\left(x,y,z\right)$ be continuous on $L$. Then

$$
\int_L f\left(x,y,z\right)\,\mathrm{d}s=\int_\alpha^\beta f\left(x\left(t\right),y\left(t\right),z\left(t\right)\right)\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm{d}t.
$$

Note that the upper limit $\beta$ must be greater than the lower limit $\alpha$.

## Line Integrals of the Second Kind

**Theorem 2.2** (Green's Formula)

Let $L$ be a piecewise smooth simple closed curve in the $Oxy$ plane, let $D$ be the bounded closed region enclosed by it, and let $P\left(x,y\right),Q\left(x,y\right)$ have first-order continuous partial derivatives on $D$. Then

$$
\oint_{L^+}P\left(x,y\right)\,\mathrm{d}x+Q\left(x,y\right)\,\mathrm{d}y=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y,
$$

where $L^+$ denotes the counterclockwise direction.

**Theorem 2.4** (Condition for Independence of the Integral from the Path)

Let $D$ be a simply connected region in the plane, and let $P,Q$ have first-order continuous partial derivatives inside $D$. Then the line integral $\int P\,\mathrm{d}x+Q\,\mathrm{d}y$ is independent of the path if and only if

$$
\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}
$$

holds everywhere inside $D$.

**Theorem 2.5** (Exact Differential Forms)

Under the above conditions, $P\,\mathrm{d}x+Q\,\mathrm{d}y$ is an exact differential form if and only if $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$ holds everywhere inside $D$.

## Surface Integrals

**Formula** (Computation of Surface Integrals of the First Kind)

Let a smooth surface $S$ be given by the parametric equations $x=x\left(u,v\right)$, $y=y\left(u,v\right)$, $z=z\left(u,v\right)$ ($\left(u,v\right)\in D$), and set $E=x_u^2+y_u^2+z_u^2$, $F=x_ux_v+y_uy_v+z_uz_v$, $G=x_v^2+y_v^2+z_v^2$. Then

$$
\iint_S f\left(x,y,z\right)\,\mathrm{d}S=\iint_D f\left(x\left(u,v\right),y\left(u,v\right),z\left(u,v\right)\right)\sqrt{EG-F^2}\,\mathrm{d}u\mathrm{d}v.
$$

In particular, when the surface is given by $z=g\left(x,y\right)$ ($\left(x,y\right)\in D$), we have $\mathrm{d}S=\sqrt{1+g_x^2+g_y^2}\,\mathrm{d}x\mathrm{d}y$.

**Formula** (Computation of Surface Integrals of the Second Kind)

Let the surface $S:z=g\left(x,y\right)$ ($\left(x,y\right)\in D$), taking the upper side. Then

$$
\iint_S P\,\mathrm{d}y\mathrm{d}z+Q\,\mathrm{d}z\mathrm{d}x+R\,\mathrm{d}x\mathrm{d}y=\iint_D\left[P\left(-g_x\right)+Q\left(-g_y\right)+R\right]\mathrm{d}x\mathrm{d}y.
$$

For the lower side, take the negative sign.

## The Gauss–Green Formula and Stokes' Formula

**Theorem 4.1** (Gauss–Green Formula)

Let $S$ be a piecewise smooth closed surface in space, let $\Omega$ be the closed region in space enclosed by it, and let $P,Q,R$ have first-order continuous partial derivatives on $\Omega$. Then

$$
\oiint_{S^+}P\,\mathrm{d}y\mathrm{d}z+Q\,\mathrm{d}z\mathrm{d}x+R\,\mathrm{d}x\mathrm{d}y=\iiint_\Omega\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)\mathrm{d}V,
$$

where $S^+$ denotes the outward side.

**Theorem 4.2** (Stokes' Formula)

Let $S$ be a piecewise smooth two-sided surface, let its boundary $L$ be a piecewise smooth closed curve, and let the orientation of $L$ and the normal vector of $S$ form a right-handed system. Then

$$
\oint_{L^+}P\,\mathrm{d}x+Q\,\mathrm{d}y+R\,\mathrm{d}z=\iint_{S^+}\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right)\mathrm{d}y\mathrm{d}z+\left(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}\right)\mathrm{d}z\mathrm{d}x+\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y.
$$

## Introduction to Field Theory

**Definition** (Divergence)

Let the vector field be $\boldsymbol{F}=\left(P,Q,R\right)$, where $P,Q,R$ have first-order continuous partial derivatives. Then

$$
\operatorname{div}\boldsymbol{F}=\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}.
$$

**Definition** (Curl)

The curl of the vector field $\boldsymbol{F}=\left(P,Q,R\right)$ is

$$
\operatorname{rot}\boldsymbol{F}=\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z},\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x},\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right).
$$

## The Basic Concept of Infinite Series

**Definition** (Convergence of a Series)

Given a sequence of numbers $\left\{a_n\right\}$, form the partial sums $S_n=\sum_{k=1}^{n}a_k$. If $\lim_{n\to\infty}S_n=S$ exists and is finite, then the series $\sum_{n=1}^{\infty}a_n$ is called convergent and $S$ is called its sum; otherwise the series is called divergent.

**Theorem 1.1** (Necessary Condition for Convergence of a Series)

If the series $\sum_{n=1}^{\infty}a_n$ converges, then

$$
\lim_{n\to\infty}a_n=0.
$$

## Series with Nonnegative Terms

**Theorem 2.2** (Comparison Test)

Let $\sum a_n$ and $\sum b_n$ be series with nonnegative terms, and suppose there exists a natural number $N_0$ such that $a_n\le b_n$ ($n\ge N_0$). If $\sum b_n$ converges, then $\sum a_n$ converges; if $\sum a_n$ diverges, then $\sum b_n$ diverges.

**Theorem 2.3** (Limit Form of the Comparison Test)

Let $\sum a_n$ and $\sum b_n$ be series with nonnegative terms, with $b_n\ne 0$, and

$$
\lim_{n\to\infty}\frac{a_n}{b_n}=l.
$$

When $0< l< +\infty$, the two series either both converge or both diverge.

**Theorem 2.6** (d'Alembert's Test)

Let $\sum a_n$ be a series with nonnegative terms, with $a_n> 0$. If

$$
\lim_{n\to\infty}\frac{a_{n+1}}{a_n}=r,
$$

then the series converges when $r< 1$ and diverges when $r> 1$.

**Theorem 2.9** (Integral Test)

Let $f\left(x\right)$ be positive and monotonically decreasing on $\left[1,+\infty\right)$. Then the series $\sum_{n=1}^{\infty}f\left(n\right)$ and the improper integral $\int_1^{+\infty}f\left(x\right)\,\mathrm{d}x$ either both converge or both diverge.

## Series with Arbitrary Terms

**Theorem 3.2** (Dirichlet's Test)

Let the sequence of numbers $\left\{b_n\right\}$ be monotone and tend to zero, and suppose the sequence of partial sums of the series $\sum a_n$ is bounded. Then the series $\sum a_nb_n$ converges.

**Theorem 3.3** (Abel's Test)

Let the sequence of numbers $\left\{b_n\right\}$ be monotone and bounded, and suppose the series $\sum a_n$ converges. Then the series $\sum a_nb_n$ converges.

## Infinite Products

**Theorem 4.1** (Relation Between Infinite Products and Series)

Let $p_n> 0$ ($n=1,2,\dots$). Then the infinite product $\prod_{n=1}^{\infty}p_n$ converges if and only if the series $\sum_{n=1}^{\infty}\ln p_n$ converges, and in that case
$$
\prod_{n=1}^{\infty}p_n=\exp\left(\sum_{n=1}^{\infty}\ln p_n\right).
$$
**Theorem 4.2** (Infinite Products with Terms of the Same Sign)

Let $\alpha_n\ge 0$ (or $\alpha_n\le 0$). Then the infinite product $\prod_{n=1}^{\infty}\left(1+\alpha_n\right)$ converges if and only if the series $\sum_{n=1}^{\infty}\alpha_n$ converges.

**Theorem 4.4** (Absolute Convergence)

Let $\alpha_n\ne -1$. Then the infinite product $\prod_{n=1}^{\infty}\left(1+\alpha_n\right)$ converges absolutely if and only if the series $\sum_{n=1}^{\infty}\left|\alpha_n\right|$ converges.

## Uniform Convergence of Sequences of Functions

**Definition** (Uniform Convergence of a Sequence of Functions)

Let $\left\{f_n\left(x\right)\right\}$ be defined on a set $X$, and let $f\left(x\right)$ be a function on $X$. If, for any $\epsilon> 0$, there exists a natural number $N$ such that, whenever $n> N$, we have $\left|f_n\left(x\right)-f\left(x\right)\right|< \epsilon$ for all $x\in X$, then $\left\{f_n\left(x\right)\right\}$ is said to converge uniformly to $f\left(x\right)$ on $X$.

**Theorem 1.1** (M-Test)

Suppose there exists a sequence of numbers $M_n> 0$ with $M_n\to 0$, such that $\left|f_n\left(x\right)-f\left(x\right)\right|\le M_n$ for all $x\in X$. Then $\left\{f_n\left(x\right)\right\}$ converges uniformly to $f\left(x\right)$ on $X$.

**Theorem 1.2** (Continuity of the Limit Function)

Let $\left\{f_n\left(x\right)\right\}$ converge uniformly to $f\left(x\right)$ on an interval $X$, and suppose each $f_n\left(x\right)$ is continuous on $X$. Then $f\left(x\right)$ is continuous on $X$.

## Series of Functions

**Theorem 2.2** (Weierstrass M-Test)

Let $\left|u_n\left(x\right)\right|\le a_n$ for all $x\in X$ and all sufficiently large $n$, and suppose $\sum a_n$ converges. Then the series of functions $\sum u_n\left(x\right)$ converges uniformly on $X$.

**Theorem 2.4** (Dirichlet's Test)

In the series of functions $\sum a_n\left(x\right)b_n\left(x\right)$, suppose the sequence of partial sums of $\sum a_n\left(x\right)$ is uniformly bounded on $X$, $b_n\left(x\right)$ is monotone in $n$ for each $x\in X$, and $b_n\left(x\right)$ tends uniformly to zero on $X$. Then $\sum a_n\left(x\right)b_n\left(x\right)$ converges uniformly on $X$.

**Theorem 2.5** (Continuity of the Sum Function)

Let $u_n\left(x\right)$ be continuous on an interval $X$, and suppose $\sum u_n\left(x\right)$ converges uniformly on $X$. Then its sum function $S\left(x\right)$ is continuous on $X$.

**Theorem 2.7** (Term-by-Term Differentiation Theorem)

Let $\sum u_n\left(x\right)$ converge to $S\left(x\right)$ on $\left[a,b\right]$, let $u_n\left(x\right)$ have continuous derivatives on $\left[a,b\right]$, and let $\sum u_n'\left(x\right)$ converge uniformly on $\left[a,b\right]$. Then $S\left(x\right)$ is differentiable on $\left[a,b\right]$, and

$$
S'\left(x\right)=\sum u_n'\left(x\right).
$$

## Power Series

**Theorem 3.2** (Cauchy's Formula for the Radius of Convergence)

For the power series $\sum_{n=0}^{\infty}a_nx^n$, its radius of convergence $R$ satisfies

$$
\frac{1}{R}=\limsup_{n\to\infty}\sqrt\left[n\right]{\left|a_n\right|}.
$$

**Theorem 3.3** (d'Alembert's Formula for the Radius of Convergence)

Let $a_n\ne 0$ and

$$
\lim_{n\to\infty}\left|\frac{a_n}{a_{n+1}}\right|=R,
$$

then the radius of convergence of this power series is $R$.

**Theorem 3.4** (Uniform Convergence on Closed Subintervals)

A power series converges uniformly on any closed subinterval inside its interval of convergence, and hence can be differentiated term by term and integrated term by term within the interval of convergence, with the radius of convergence unchanged.

## Taylor Series

**Theorem 4.1** (Taylor Series)

If the function $f\left(x\right)$ can be expanded as a power series on $\left(x_0-R,x_0+R\right)$,

$$
f\left(x\right)=\sum_{n=0}^{\infty}a_n\left(x-x_0\right)^n,
$$

then its coefficients must be
$$
a_n=\frac{f^{\left(n\right)}\left(x_0\right)}{n!},
$$
i.e. the power series expansion is unique and is called the Taylor series of $f$ at $x_0$.

**Definition** (Basic Expansions)

At $x=0$ we have:

$$
\begin{aligned}
e^x&=\sum_{n=0}^{\infty}\frac{x^n}{n!}\ \left(\left|x\right|< +\infty\right),\\
\ln\left(1+x\right)&=\sum_{n=1}^{\infty}\frac{\left(-1\right)^{n-1}x^n}{n}\ \left(\left|x\right|< 1\right),\\
\cos x&=\sum_{n=0}^{\infty}\frac{\left(-1\right)^n x^{2n}}{\left(2n\right)!}\ \left(\left|x\right|< +\infty\right).
\end{aligned}
$$

## Improper Integrals of the First Kind

**Definition** (Convergence of an Improper Integral)

Let the function $f\left(x\right)$ be defined on $\left[a,+\infty\right)$ and integrable on any closed interval $\left[a,A\right]$. If the limit $\lim_{A\to+\infty}\int_a^A f\left(x\right)\,\mathrm{d}x$ exists, then the improper integral $\int_a^{+\infty} f\left(x\right)\,\mathrm{d}x$ is called convergent, and this limit is defined as its value; otherwise it is called divergent.

**Example 1.2** ($p$-Integral)

The improper integral $\int_1^{+\infty}\frac{\mathrm{d}x}{x^p}$ converges when $p> 1$ and diverges when $p\le 1$.

**Theorem 1.1** (Cauchy Convergence Principle for Improper Integrals)

Let $f\left(x\right)$ be defined on $\left[a,+\infty\right)$ and integrable on any closed interval $\left[a,A\right]$. Then the improper integral $\int_a^{+\infty} f\left(x\right)\,\mathrm{d}x$ converges if and only if: for any $\epsilon> 0$, there exists $X> 0$ such that, whenever $A',A''> X$, we have $\left|\int_{A'}^{A''} f\left(x\right)\,\mathrm{d}x\right|< \epsilon$.

**Theorem 1.3** (Comparison Test)

Let $f\left(x\right)$ and $g\left(x\right)$ be defined on $\left[a,+\infty\right)$ and integrable on any closed interval $\left[a,A\right]$. Suppose there exists $X_0> a$ such that

$$
0\le f\left(x\right)\le g\left(x\right)\left(\forall x\ge X_0\right).
$$

Then if $\int_a^{+\infty}g\left(x\right)\,\mathrm{d}x$ converges, $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ must converge; if $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ diverges, $\int_a^{+\infty}g\left(x\right)\,\mathrm{d}x$ must diverge.

**Theorem 1.6** (Dirichlet's Test)

Let $f\left(x\right)$ and $g\left(x\right)$ be defined on $\left[a,+\infty\right)$ and integrable on any interval $\left[a,A\right]$. If $f\left(x\right)$ is monotone on $\left[a,+\infty\right)$ and $\lim_{x\to+\infty}f\left(x\right)=0$, and $\int_a^A g\left(x\right)\,\mathrm{d}x$ is bounded as a function of $A$, then $\int_a^{+\infty}f\left(x\right)g\left(x\right)\,\mathrm{d}x$ converges.

**Definition** (Absolute and Conditional Convergence)

If $\int_a^{+\infty}\left| f\left(x\right)\right|\,\mathrm{d}x$ converges, then the improper integral $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ is called absolutely convergent; if $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ converges but $\int_a^{+\infty}\left| f\left(x\right)\right|\,\mathrm{d}x$ diverges, then it is called conditionally convergent.

## Improper Integrals of the Second Kind

**Definition** (Convergence of an Improper Integral of the Second Kind)

Let $f\left(x\right)$ be defined on $\left(a,b\right]$ and integrable on any closed interval $\left[a+\eta,b\right]\subset\left(a,b\right]\left(\eta> 0\right)$, where $a$ is a singularity of $f\left(x\right)$. If the limit $\lim_{\eta\to0+0}\int_{a+\eta}^b f\left(x\right)\,\mathrm{d}x$ exists, then the improper integral $\int_a^b f\left(x\right)\,\mathrm{d}x$ is called convergent, and this limit is defined as its value; otherwise it is called divergent. When the singularity is the right endpoint or an interior point of the interval, the definition is completely analogous.

**Example 2.2** ($p$-Integral of the Second Kind)

The improper integral $\int_a^b\frac{\mathrm{d}x}{\left(x-a\right)^p}$ ($p> 0$) converges when $p< 1$ and diverges when $p\ge1$.

**Definition** (Absolute and Conditional Convergence)

Let $f\left(x\right)$ be defined on $\left(a,b\right]$, with $a$ being a singularity. If $\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x$ converges, then $\int_a^b f\left(x\right)\,\mathrm{d}x$ is called absolutely convergent; if $\int_a^b f\left(x\right)\,\mathrm{d}x$ converges but $\int_a^b\left| f\left(x\right)\right|\,\mathrm{d}x$ diverges, then it is called conditionally convergent.

**Definition** (Cauchy Principal Value)

Let $f\left(x\right)$ be defined on $\left[a,b\right]\setminus\left\{c\right\}$, with $c\in\left(a,b\right)$ being a singularity. Suppose the limit

$$
I=\lim_{\eta\to0+0}\left[\int_a^{c-\eta}f\left(x\right)\,\mathrm{d}x+\int_{c+\eta}^b f\left(x\right)\,\mathrm{d}x\right]
$$

exists. Then the improper integral $\int_a^b f\left(x\right)\,\mathrm{d}x$ is called convergent in the sense of the Cauchy principal value, and the limit $I$ is called its Cauchy principal value, denoted

$$
\mathrm{\left(CPV\right)}\int_a^b f\left(x\right)\,\mathrm{d}x.
$$

## Integrals Depending on a Parameter

**Theorem 3.3** (Differentiation Under the Integral Sign)

Let $f\left(x,y\right)$ and $f_y\left(x,y\right)$ be continuous on $\left[a,b\right]\times\left[c,d\right]$. Then the function $I\left(y\right)=\int_a^b f\left(x,y\right)\,\mathrm{d}x$ is differentiable on $\left[c,d\right]$, and
$$
I'\left(y\right)=\int_a^b f_y\left(x,y\right)\,\mathrm{d}x, \forall\,y\in\left[c,d\right].
$$
When the limits of integration also depend on $y$, i.e. $I\left(y\right)=\int_{a\left(y\right)}^{b\left(y\right)}f\left(x,y\right)\,\mathrm{d}x$, add the boundary terms using the Newton–Leibniz formula:
$$
I'\left(y\right)=f\left(b\left(y\right),y\right)b'\left(y\right)-f\left(a\left(y\right),y\right)a'\left(y\right)+\int_{a\left(y\right)}^{b\left(y\right)}f_y\left(x,y\right)\,\mathrm{d}x.
$$
## Improper Integrals Depending on a Parameter

**Theorem 4.3** (Weierstrass's Test)

Let $f\left(x,y\right)$ be defined on $\left[a,+\infty\right)\times Y$. If there exists $F\left(x\right)$ such that (i)

$$
\left| f\left(x,y\right)\right|\le F\left(x\right)\left(\forall x\in\left[a,+\infty\right),y\in Y\right);
$$

(ii) $\int_a^{+\infty}F\left(x\right)\,\mathrm{d}x$ converges, then the improper integral $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ converges uniformly with respect to $y\in Y$.

**Theorem 4.4** (Abel's Test)

Let $f\left(x,y\right),g\left(x,y\right)$ be defined on $\left[a,+\infty\right)\times Y$. If (i) $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ converges uniformly with respect to $y\in Y$; (ii) $g\left(x,y\right)$ is monotone in $x$ and uniformly bounded with respect to $y\in Y$, then $\int_a^{+\infty}f\left(x,y\right)g\left(x,y\right)\,\mathrm{d}x$ converges uniformly with respect to $y\in Y$.

**Theorem 4.7** (Interchange of the Order of Integration)

Let $f\left(x,y\right)$ be continuous on $\left[a,+\infty\right)\times\left[c,d\right]$, and let $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ converge uniformly with respect to $y\in\left[c,d\right]$. Then

$$
\int_c^d\mathrm{d}y\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x=\int_a^{+\infty}\mathrm{d}x\int_c^d f\left(x,y\right)\,\mathrm{d}y.
$$

**Theorem 4.8** (Differentiation Under the Integral Sign)

Let $f\left(x,y\right)$ and $f_y\left(x,y\right)$ be continuous on $\left[a,+\infty\right)\times\left[c,d\right]$, let $\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ converge uniformly with respect to $y\in\left[c,d\right]$, and let $\int_a^{+\infty}f_y\left(x,y\right)\,\mathrm{d}x$ also converge uniformly. Then $I\left(y\right)=\int_a^{+\infty}f\left(x,y\right)\,\mathrm{d}x$ is differentiable on $\left[c,d\right]$, and

$$
I'\left(y\right)=\int_a^{+\infty}f_y\left(x,y\right)\,\mathrm{d}x.
$$

**Example 4.5** (Dirichlet Integral)

$$
\int_0^{+\infty}\frac{\sin x}{x}\,\mathrm{d}x=\frac{\pi}{2}.
$$

More generally,

$$
\int_0^{+\infty}\frac{\sin\left(kx\right)}{x}\,\mathrm{d}x=\frac{\pi}{2}\operatorname{sgn}\left(k\right).
$$

## Improper Integrals of the Second Kind Depending on a Parameter

**Theorem 4.3** (Weierstrass's Test)

Let $f\left(x,y\right)$ be defined on $\left(a,b\right]\times Y$, with $a$ being a singularity. If there exists $F\left(x\right)$ such that (i)

$$
\left| f\left(x,y\right)\right|\le F\left(x\right)\left(\forall x\in\left(a,b\right],y\in Y\right);
$$

(ii) the improper integral $\int_a^b F\left(x\right)\,\mathrm{d}x$ converges, then the improper integral of the second kind $\int_a^b f\left(x,y\right)\,\mathrm{d}x$ converges uniformly with respect to $y\in Y$.

**Theorem 4.7** (Interchange of the Order of Integration)

Let $f\left(x,y\right)$ be continuous on $\left(a,b\right]\times\left[c,d\right]$ and keep a fixed sign, and let $\int_a^b f\left(x,y\right)\,\mathrm{d}x$ converge uniformly with respect to $y\in\left[c,d\right]$. Then

$$
\int_c^d\mathrm{d}y\int_a^b f\left(x,y\right)\,\mathrm{d}x=\int_a^b\mathrm{d}x\int_c^d f\left(x,y\right)\,\mathrm{d}y.
$$

## The Gamma and Beta Functions

**Definition** (Gamma Function)

$$
\Gamma\left(\alpha\right)=\int_0^{+\infty}t^{\alpha-1}e^{-t}\,\mathrm{d}t\ \left(\alpha> 0\right).
$$

It satisfies the recurrence $\Gamma\left(\alpha+1\right)=\alpha\Gamma\left(\alpha\right)$, $\Gamma\left(1\right)=1$, $\Gamma\left(n+1\right)=n!$, and

$$
\Gamma\!\left(\frac12\right)=\sqrt\pi.
$$

**Definition** (Beta Function)

$$
\begin{aligned}
\Beta\left(p,q\right)&=\int_0^1 t^{p-1}\left(1-t\right)^{q-1}\,\mathrm{d}t\left(p,q> 0\right),\\
\Beta\left(p,q\right)&=\frac{\Gamma\left(p\right)\Gamma\left(q\right)}{\Gamma\left(p+q\right)}.
\end{aligned}
$$

**Proposition** (Integral Forms of the Gamma and Beta Functions)

$$
\begin{aligned}
\int_0^{+\infty}\frac{x^{a-1}}{\left(1+x\right)^{a+b}}\,\mathrm{d}x&=\Beta\left(a,b\right),\\
\int_0^{\pi/2}\sin^m x\cos^n x\,\mathrm{d}x&=\frac12 \Beta\!\left(\frac{m+1}{2},\frac{n+1}{2}\right).
\end{aligned}
$$

## The Trigonometric System and Its Orthogonality

**Definition** (Inner Product and Norm)

Define the inner product in $R\left[-\pi,\pi\right]$ as

$$
\left\langle f,g\right\rangle=\frac1\pi\int_{-\pi}^\pi f\left(x\right)g\left(x\right)\,\mathrm{d}x,
$$
and the norm as

$$
\left| f\right|=\sqrt{\left\langle f,f\right\rangle}=\left(\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x\right)^{1/2}.
$$

**Proposition** (Orthogonality of the Trigonometric System)

The trigonometric system

$$
1,\cos x,\sin x,\cos2x,\sin2x,\cdots
$$

is pairwise orthogonal on $\left[-\pi,\pi\right]$, i.e. the integral over $\left[-\pi,\pi\right]$ of the product of any two distinct elements is $0$; and

$$
\begin{aligned}
\int_{-\pi}^\pi1\,\mathrm{d}x&=2\pi,\\
\int_{-\pi}^\pi\cos^2 nx\,\mathrm{d}x&=\int_{-\pi}^\pi\sin^2 nx\,\mathrm{d}x=\pi\left(n=1,2,\cdots\right).
\end{aligned}
$$

## Fourier Series of Periodic Functions

**Proposition** (Fourier Coefficients)

Let $f\left(x\right)$ be integrable and square-integrable on $\left[-\pi,\pi\right]$. Then its Fourier series is

$$
f\left(x\right)\sim\frac{a_0}{2}+\sum_{n=1}^\infty\left(a_n\cos nx+b_n\sin nx\right),
$$

where

$$
\begin{aligned}
a_n&=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\cos nx\,\mathrm{d}x\left(n=0,1,2,\cdots\right),\\
b_n&=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\sin nx\,\mathrm{d}x\left(n=1,2,\cdots\right).
\end{aligned}
$$

## Convergence of Fourier Series

**Theorem 3.1** (Dirichlet Convergence Theorem)

Let $f\left(x\right)$ be periodic with period $2\pi$ and piecewise monotone and bounded on $\left[-\pi,\pi\right]$. Then its Fourier series converges at every point $x$ to $\frac{f\left(x+0\right)+f\left(x-0\right)}{2}$; at points of continuity of $f$ it converges to $f\left(x\right)$, and at points of discontinuity it converges to the average of the left and right limits.

**Proposition** (Fourier Coefficients)

The Fourier coefficients of an integrable function $f\left(x\right)$ of period $2\pi$ are

$$
\begin{aligned}
a_n&=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\cos nx\,\mathrm{d}x,\\
b_n&=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\sin nx\,\mathrm{d}x.
\end{aligned}
$$

**Theorem** (Closure Equation)

Let the Fourier coefficients of $f\left(x\right)$ be $a_n,b_n$. Then

$$
\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x=\frac{a_0^2}{2}+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right).
$$

## Mean-Square Approximation and Bessel's Inequality

**Theorem 4.1** (Bessel's Inequality)

Let $f\left(x\right)$ be Riemann integrable on $\left[-\pi,\pi\right]$, with Fourier coefficients $a_n,b_n$. Then

$$
\frac{a_0^2}{2}+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right)\le\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x.
$$

Moreover, both $\sum_{n=1}^\infty a_n^2$ and $\sum_{n=1}^\infty b_n^2$ converge.

**Theorem 4.2** (Closure Equation / Parseval's Identity)

Let $f\left(x\right)$ be Riemann integrable and square-integrable on $\left[-\pi,\pi\right]$. Then

$$
\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x=\frac{a_0^2}{2}+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right).
$$
