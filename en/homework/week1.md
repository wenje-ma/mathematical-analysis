# Assignment 1

> **Definition** (Field) Roughly speaking, a set of numbers that is closed under addition, subtraction, multiplication and division (where the divisor is not $0$), and that satisfies the commutative, associative and distributive laws, is called a field.

> **Definition** (Ordered Field) A number field on which an order relation is defined and which satisfies the following properties is called an ordered field: for any $\alpha,b$, exactly one of $\alpha=b$, $\alpha< b$, $b< \alpha$ holds; and when $a< b,b< c$ then $a< c$; when $a< b$ then $a+c< b+c$; when $0< a,b$ then $a\cdot b> 0$.

> **Proposition 1.1** (The Field of Rational Numbers Is an Ordered Field) The field of rational numbers $\mathbb Q$ is an ordered field.

> **Definition** (Density) A number set $S$ is said to be everywhere dense on the number line if, for any interval $\left(a,b\right)$ on the number line, no matter where it lies or how small it is, there is at least one number of $S$ lying in $\left(a,b\right)$, i.e. $S\cap\left(a,b\right)\ne\varnothing$.

> **Proposition 1.3** ($\sqrt2$ Is Irrational) $\sqrt2$ is not a rational number.

> **Example 1.1** (Operations on Irrational Numbers) The sum of an irrational number and a rational number is irrational. The product of an irrational number and a rational number is irrational.

> **Definition** (Completeness) An ordered number field satisfying the following requirement is called complete (or continuous): for any monotonically increasing bounded sequence $\left\{x_n\right\}$, there exists a number $a$ in the field such that $x_n$ can approach $a$ arbitrarily closely.

> **Proposition 1.5** (Completeness of the Real Number Field) Let $\left\{x_n\right\}$ be any monotonically increasing sequence bounded above in the real number field $\mathbb R$. Then there exists a number $a$ in $\mathbb R$ such that $x_n\le a$, and $x_n$ can approach $a$ arbitrarily closely.

> **Definition** (Bounded Set) Let $E\subset\mathbb R$. If there exists $M$ such that every point $x$ in $E$ satisfies $x\le M$, then $E$ is said to be bounded above; if there exists $m$ such that every point $x$ in $E$ satisfies $x\ge m$, then $E$ is said to be bounded below; a set that is both bounded above and bounded below is called a bounded set.

> **Proposition 1.6** (Properties of the Absolute Value) For any $x,y\in\mathbb R$, we have:
> (1) $\left|x\right|\ge0$, with equality if and only if $x=0$;
> 
> (2) $\left|-x\right|=\left|x\right|$;
> 
> (3) $\left|x+y\right|\le\left|x\right|+\left|y\right|$.

> **Proposition 1.7** (Triangle Inequality) For any real numbers $a,b,c$, we have:
> (1) $\left|a-b\right|\ge0$, with equality if and only if $a=b$;
> 
> (2) $\left|a-b\right|=\left|b-a\right|$;
> 
> (3) $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

### Problem 1

(Problem 1.1-3) Prove that $\sqrt2+\sqrt3$ is irrational.

### Solution to Problem 1

Use proof by contradiction. Suppose $\sqrt2+\sqrt3$ is rational. Then there exists $r\in\mathbb Q$ such that $\sqrt2+\sqrt3=r$, so $\sqrt3=r-\sqrt2$. Squaring both sides gives

$$
3=r^2-2r\sqrt2+2,
$$

i.e. $\sqrt2=\frac{r^2-1}{2r}$. If $r\ne0$, then the right-hand side $\frac{r^2-1}{2r}$ is rational, so $\sqrt2\in\mathbb Q$, contradicting **Proposition 1.3** ($\sqrt2$ Is Irrational). If $r=0$, then $\sqrt2+\sqrt3=0$, which is even more impossible. Hence $\sqrt2+\sqrt3$ is not rational, i.e. $\sqrt2+\sqrt3$ is irrational. $\blacksquare$

### Problem 2

(Problem 1.1-4) Prove that the set of numbers

$$
E=\left\{m+n\sqrt2:m,n\in\mathbb Q\right\}
$$

is a number field. Also determine whether this number field is complete.

### Solution to Problem 2

(1) First prove that $E$ is a number field. For any

$$
m_1+n_1\sqrt2,m_2+n_2\sqrt2\in E,
$$

we have

$$
\begin{aligned}\left(m_1+n_1\sqrt2\right)\pm\left(m_2+n_2\sqrt2\right)&=\left(m_1\pm m_2\right)+\left(n_1\pm n_2\right)\sqrt2\in E,\\\left(m_1+n_1\sqrt2\right)\left(m_2+n_2\sqrt2\right)&=\left(m_1m_2+2n_1n_2\right)+\left(m_1n_2+m_2n_1\right)\sqrt2\in E.\end{aligned}
$$

Hence $E$ is closed under addition, subtraction and multiplication. If $m_2+n_2\sqrt2\ne0$, rationalizing gives

$$
\frac{m_1+n_1\sqrt2}{m_2+n_2\sqrt2}=\frac{m_1m_2-2n_1n_2}{m_2^2-2n_2^2}+\frac{n_1m_2-m_1n_2}{m_2^2-2n_2^2}\sqrt2\in E,
$$

where $m_2^2-2n_2^2\ne0$ (otherwise $\sqrt2=m_2/n_2\in\mathbb Q$, contradicting **Proposition 1.3**). Moreover, these operations obviously satisfy the commutative, associative and distributive laws, so by **Definition** (Field), $E$ is a number field.

(2) $E$ is not complete. In fact, $\sqrt3\notin E$: if $\sqrt3=m+n\sqrt2$, squaring gives $3=m^2+2n^2+2mn\sqrt2$. If $mn\ne0$, then $\sqrt2=\frac{3-m^2-2n^2}{2mn}\in\mathbb Q$, a contradiction; if $n=0$, then $\sqrt3=m\in\mathbb Q$, a contradiction; if $m=0$, then $\sqrt3=n\sqrt2$, and squaring gives $n^2=\frac32\notin\mathbb Q$, a contradiction. Hence $\sqrt3\notin E$.

Take $x_n$ to be the $n$-digit lower (deficient) decimal approximation of $\sqrt3$. Then $x_n\in\mathbb Q\subset E$ (take $m=x_n,n=0$), and $\left\{x_n\right\}$ is monotonically increasing and bounded above (e.g. $x_n< 2$), but $\left\{x_n\right\}$ approaches arbitrarily close to $\sqrt3\notin E$. Thus by **Definition** (Completeness), $E$ is not complete. $\blacksquare$

### Problem 3

(Problem 1.1-6) Let

$$
E_1=\left\{x:\left|x-a\right|> r_1\right\},E_2=\left\{x:\left|x-b\right|< r_2\right\}.
$$

Under what conditions on $a,b,r_1,r_2$ do we have $E_1\cap E_2\ne\varnothing$?

### Solution to Problem 3

$E_1$ is the set of points on the number line whose distance from $a$ is greater than $r_1$, and $E_2$ is the open interval $\left(b-r_2,b+r_2\right)$ of points whose distance from $b$ is less than $r_2$.

First find the condition for $E_1\cap E_2=\varnothing$. $E_2$ is disjoint from $E_1$ if and only if $E_2\subset\left[a-r_1,a+r_1\right]$, i.e.

$$
a-r_1\le b-r_2, b+r_2\le a+r_1,
$$

i.e. $r_2\le r_1-\left|a-b\right|$. Hence $E_1\cap E_2\ne\varnothing$ if and only if

$$
r_2> r_1-\left|a-b\right|.

$$

$\blacksquare$
### Problem 4

(Problem 1.1-7) Solve the following inequalities:
(1) $\left|x^2-1\right|< 8$;

(2) $\left|x-1\right|< \left|x\right|$;

(3) $\left|x-1\right|< \left|x+1\right|$;

(4) $\left|x+2\right|< 1$.

### Solution to Problem 4

(1) From $\left|x^2-1\right|< 8$ we get $-8< x^2-1< 8$, i.e. $-7< x^2< 9$. Since $x^2\ge0$ always holds, we only need $x^2< 9$, and by **Proposition 1.6** we get $\left|x\right|< 3$, i.e. $-3< x< 3$.

(2) By **Proposition 1.6** (3) and the equivalence of squaring both sides, $\left|x-1\right|< \left|x\right|$ if and only if $\left(x-1\right)^2< x^2$, i.e. $x^2-2x+1< x^2$, which solves to $x> \frac12$.

(3) Similarly, $\left|x-1\right|< \left|x+1\right|$ if and only if $\left(x-1\right)^2< \left(x+1\right)^2$, i.e.

$$
x^2-2x+1< x^2+2x+1,
$$

which solves to $x> 0$.

(4) By **Proposition 1.6** (1)(3), $\left|x+2\right|< 1$ means $-1< x+2< 1$, which solves to $-3< x< -1$. $\blacksquare$

### Problem 5

(Problem 1.1-9) Prove the following inequalities:
(1)

$$
\left|a+2b+c\right|\le\left|a+b\right|+\left|b+c\right|;
$$

(2)

$$
\left|a-b\right|\ge\left|\left|a-c\right|-\left|b-c\right|\right|.
$$

### Solution to Problem 5

(1) Write $a+2b+c$ as $\left(a+b\right)+\left(b+c\right)$. By **Proposition 1.6** (3) (triangle inequality) we get

$$
\left|a+2b+c\right|=\left|\left(a+b\right)+\left(b+c\right)\right|\le\left|a+b\right|+\left|b+c\right|.
$$

(2) By **Proposition 1.6** (3) and **Proposition 1.7** (2), we have

$$
\left|a-c\right|=\left|\left(a-b\right)+\left(b-c\right)\right|\le\left|a-b\right|+\left|b-c\right|,
$$

Hence $\left|a-b\right|\ge\left|a-c\right|-\left|b-c\right|$. Similarly, swapping the positions of $a,c$ gives $\left|a-b\right|\ge\left|c-b\right|-\left|a-b\right|$, i.e. $\left|a-b\right|\ge\left|b-c\right|-\left|a-c\right|$. Combining the two inequalities,

$$
\left|a-b\right|\ge\left|\left|a-c\right|-\left|b-c\right|\right|.

$$

$\blacksquare$
### Problem 6

(Problem 1.1-11) Determine whether the following sets $E$ are bounded above, bounded below, and bounded:
(1) $E=\left\{e^n:n\in\mathbb N_+\right\}$;

(2) $E=\left\{\frac{n^2+10^{10}}{n^2+1}:n\in\mathbb N\right\}$;

(3)

$$
E=\left\{\sqrt{x+1}-\sqrt{x}:x\ge1\right\};
$$

(4)

$$
E=\left\{\left(-1\right)^nn^2-n:n\in\mathbb N\right\}.
$$

### Solution to Problem 6

(1) $E=\left\{e,e^2,e^3,\dots\right\}$. Since $e^n\ge e$, $E$ is bounded below (e.g. $m=e$); but $e^n$ grows without bound as $n$ increases, so $E$ is not bounded above. By **Definition** (Bounded Set), $E$ is bounded below and not bounded above, and is not a bounded set.

(2) For $n\in\mathbb N$, $\frac{n^2+10^{10}}{n^2+1}=1+\frac{10^{10}-1}{n^2+1}$. Since $n^2+1\ge1$, we have $1< \frac{n^2+10^{10}}{n^2+1}\le10^{10}$, i.e. $E\subset\left(1,10^{10}\right]$. Hence $E$ is bounded above and bounded below, and by **Definition** (Bounded Set), $E$ is a bounded set.

(3) For $x\ge1$, rationalizing gives

$$
\sqrt{x+1}-\sqrt{x}=\frac{1}{\sqrt{x+1}+\sqrt{x}}.
$$

Since $0< \sqrt{x+1}+\sqrt{x}$ when $x\ge1$, we have

$$
0< \sqrt{x+1}-\sqrt{x}\le\sqrt2-1\ \left(x=1\text{时取最大值}\right),
$$

Hence $E\subset\left(0,\sqrt2-1\right]$, bounded above and bounded below; $E$ is a bounded set.

(4) When $n$ is even, $\left(-1\right)^nn^2-n=n^2-n$, whose absolute value is $n^2-n$; when $n$ is odd, $\left(-1\right)^nn^2-n=-n^2-n$, whose absolute value is $n^2+n$. In any case, the absolute value grows without bound as $n$ increases and tends to infinity, so $E$ is neither bounded above nor bounded below, and is not a bounded set. $\blacksquare$
