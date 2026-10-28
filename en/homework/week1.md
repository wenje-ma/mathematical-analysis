# week1

> **Basic Knowledge: The Concept of a Field**<br>Roughly speaking, if a set of numbers is closed under addition, subtraction, multiplication, and division (divisor nonzero), and satisfies the commutative, associative, and distributive laws, then it is called a field.

> **Basic Knowledge: The Concept of Completeness**<br>An ordered number field is called complete (or continuous) if it satisfies the following requirement: for any monotone increasing bounded sequence $\left\{x_n\right\}$, there exists a number $a$ in the field such that $x_n$ can approach $a$ arbitrarily closely.

> **Basic Knowledge: The Concept of Bounded Sets**<br>Let $E\subset\mathbb R$. If there exists $M$ such that $x\le M$ for all $x\in E$, then $E$ is said to be bounded above; if there exists $m$ such that $x\ge m$ for all $x\in E$, then $E$ is said to be bounded below; a set that is both bounded above and bounded below is called a bounded set.

> **Proposition 1.3 ($\sqrt2$ Is Irrational)**<br>$\sqrt2$ is not a rational number.

> **Proposition 1.6 (Properties of Absolute Value)**<br>For any $x,y\in\mathbb R$: (1) $\left|x\right|\ge0$, with equality if and only if $x=0$; (2) $\left|-x\right|=\left|x\right|$; (3) $\left|x+y\right|\le\left|x\right|+\left|y\right|$.

> **Proposition 1.7 (Triangle Inequality)**<br>For any real numbers $a,b,c$: (1) $\left|a-b\right|\ge0$, with equality if and only if $a=b$; (2) $\left|a-b\right|=\left|b-a\right|$; (3) $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

---

## 1.1-3

Prove that $\sqrt2+\sqrt3$ is irrational.

### Solution 1.1-3

By contradiction. Suppose $\sqrt2+\sqrt3$ is rational. Then there exists $r\in\mathbb Q$ such that $\sqrt2+\sqrt3=r$, so $\sqrt3=r-\sqrt2$. Squaring both sides gives

$$
3=r^2-2r\sqrt2+2,
$$

i.e. $\sqrt2=\frac{r^2-1}{2r}$. If $r\ne0$, then the right-hand side $\frac{r^2-1}{2r}$ is rational, so $\sqrt2\in\mathbb Q$, contradicting **Proposition 1.3 ($\sqrt2$ Is Irrational)**. If $r=0$, then $\sqrt2+\sqrt3=0$, which is also impossible. Hence $\sqrt2+\sqrt3$ is not rational, i.e. $\sqrt2+\sqrt3$ is irrational. $\blacksquare$

---

## 1.1-4

Prove that the set

$$
E=\left\{m+n\sqrt2:m,n\in\mathbb Q\right\}
$$

is a number field. Also determine whether this field is complete.

### Solution 1.1-4

(1) First prove that $E$ is a field. For any $m_1+n_1\sqrt2$, $m_2+n_2\sqrt2\in E$,

$$
\left(m_1+n_1\sqrt2\right)\pm\left(m_2+n_2\sqrt2\right)=\left(m_1\pm m_2\right)+\left(n_1\pm n_2\right)\sqrt2\in E,
$$

$$
\left(m_1+n_1\sqrt2\right)\left(m_2+n_2\sqrt2\right)=\left(m_1m_2+2n_1n_2\right)+\left(m_1n_2+m_2n_1\right)\sqrt2\in E.
$$

Thus $E$ is closed under addition, subtraction, and multiplication. If $m_2+n_2\sqrt2\ne0$, rationalizing gives

$$
\frac{m_1+n_1\sqrt2}{m_2+n_2\sqrt2}=\frac{m_1m_2-2n_1n_2}{m_2^2-2n_2^2}+\frac{n_1m_2-m_1n_2}{m_2^2-2n_2^2}\sqrt2\in E,
$$

where $m_2^2-2n_2^2\ne0$ (otherwise $\sqrt2=m_2/n_2\in\mathbb Q$, contradicting **Proposition 1.3 ($\sqrt2$ Is Irrational)**). These operations clearly satisfy the commutative, associative, and distributive laws; hence by **Basic Knowledge: The Concept of a Field**, $E$ is a number field.

(2) $E$ is not complete. Indeed, $\sqrt3\notin E$: if $\sqrt3=m+n\sqrt2$, squaring gives $3=m^2+2n^2+2mn\sqrt2$. If $mn\ne0$, then $\sqrt2=\frac{3-m^2-2n^2}{2mn}\in\mathbb Q$, a contradiction; if $n=0$, then $\sqrt3=m\in\mathbb Q$, a contradiction; if $m=0$, then $\sqrt3=n\sqrt2$, and squaring gives $n^2=\frac32\notin\mathbb Q$, a contradiction. Hence $\sqrt3\notin E$.

Take the $n$-digit truncation $x_n$ of $\sqrt3$. Then $x_n\in\mathbb Q\subset E$ (taking $m=x_n$, $n=0$), and $\left\{x_n\right\}$ is monotone increasing and bounded above (e.g. $x_n< 2$), but $\left\{x_n\right\}$ approaches $\sqrt3\notin E$. Thus by **Basic Knowledge: The Concept of Completeness**, $E$ is not complete. $\blacksquare$

---

## 1.1-6

Let

$$
E_1=\left\{x:\left|x-a\right|> r_1\right\},\quad E_2=\left\{x:\left|x-b\right|< r_2\right\}.
$$

What conditions must $a,b,r_1,r_2$ satisfy for $E_1\cap E_2\ne\varnothing$?

### Solution 1.1-6

$E_1$ is the set of points on the number line whose distance from $a$ exceeds $r_1$, and $E_2$ is the open interval $\left(b-r_2,b+r_2\right)$ whose distance from $b$ is less than $r_2$.

First find the condition for $E_1\cap E_2=\varnothing$. $E_2$ is disjoint from $E_1$ if and only if $E_2\subset\left[a-r_1,a+r_1\right]$, i.e.

$$
a-r_1\le b-r_2,\quad b+r_2\le a+r_1,
$$

equivalently $r_2\le r_1-\left|a-b\right|$. Hence $E_1\cap E_2\ne\varnothing$ if and only if

$$
r_2> r_1-\left|a-b\right|.
$$

$\blacksquare$

---

## 1.1-7

Solve the following inequalities:

(1) $\left|x^2-1\right|< 8$;

(2) $\left|x-1\right|< \left|x\right|$;

(3) $\left|x-1\right|< \left|x+1\right|$;

(4) $\left|x+2\right|< 1$.

### Solution 1.1-7

(1) From $\left|x^2-1\right|< 8$ we get $-8< x^2-1< 8$, i.e. $-7< x^2< 9$. Since $x^2\ge0$ always, it suffices that $x^2< 9$; by **Proposition 1.6 (Properties of Absolute Value)**, $\left|x\right|< 3$, i.e. $-3< x< 3$.

(2) By **Proposition 1.6 (Properties of Absolute Value)**(3) and the equivalence of squaring both sides, $\left|x-1\right|< \left|x\right|$ if and only if $\left(x-1\right)^2< x^2$, i.e. $x^2-2x+1< x^2$, giving $x> \frac12$.

(3) Similarly, $\left|x-1\right|< \left|x+1\right|$ if and only if $\left(x-1\right)^2< \left(x+1\right)^2$, i.e.

$$
x^2-2x+1< x^2+2x+1,
$$

giving $x> 0$.

(4) By **Proposition 1.6 (Properties of Absolute Value)**(1)(3), $\left|x+2\right|< 1$ means $-1< x+2< 1$, giving $-3< x< -1$. $\blacksquare$

---

## 1.1-9

Prove the following inequalities:

(1)

$$
\left|a+2b+c\right|\le\left|a+b\right|+\left|b+c\right|;
$$

(2)

$$
\left|a-b\right|\ge\left|\left|a-c\right|-\left|b-c\right|\right|.
$$

### Solution 1.1-9

(1) Write $a+2b+c=\left(a+b\right)+\left(b+c\right)$. By **Proposition 1.6 (Properties of Absolute Value)**(3),

$$
\left|a+2b+c\right|=\left|\left(a+b\right)+\left(b+c\right)\right|\le\left|a+b\right|+\left|b+c\right|.
$$

(2) By **Proposition 1.6 (Properties of Absolute Value)**(3) and **Proposition 1.7 (Triangle Inequality)**(2),

$$
\left|a-c\right|=\left|\left(a-b\right)+\left(b-c\right)\right|\le\left|a-b\right|+\left|b-c\right|,
$$

so $\left|a-b\right|\ge\left|a-c\right|-\left|b-c\right|$. Similarly, swapping $a$ and $c$ gives $\left|a-b\right|\ge\left|c-b\right|-\left|a-b\right|$, i.e. $\left|a-b\right|\ge\left|b-c\right|-\left|a-c\right|$. Combining both,

$$
\left|a-b\right|\ge\left|\left|a-c\right|-\left|b-c\right|\right|.
$$

$\blacksquare$

---

## 1.1-11

Determine whether the following sets $E$ are bounded above, bounded below, or bounded:

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

### Solution 1.1-11

(1) $E=\left\{e,e^2,e^3,\dots\right\}$. Since $e^n\ge e$, $E$ is bounded below (e.g. $m=e$); since $e^n$ grows without bound as $n$ increases, $E$ is not bounded above. By **Basic Knowledge: The Concept of Bounded Sets**, $E$ is bounded below but not above, and is not a bounded set.

(2) For $n\in\mathbb N$, $\frac{n^2+10^{10}}{n^2+1}=1+\frac{10^{10}-1}{n^2+1}$. Since $n^2+1\ge1$, $1< \frac{n^2+10^{10}}{n^2+1}\le10^{10}$, i.e. $E\subset\left(1,10^{10}\right]$. Thus $E$ is both bounded above and below; by **Basic Knowledge: The Concept of Bounded Sets**, $E$ is a bounded set.

(3) For $x\ge1$, rationalizing gives

$$
\sqrt{x+1}-\sqrt{x}=\frac{1}{\sqrt{x+1}+\sqrt{x}}.
$$

Since $x\ge1$ implies $0< \sqrt{x+1}+\sqrt{x}$,

$$
0< \sqrt{x+1}-\sqrt{x}\le\sqrt2-1\ \text{(maximum at }x=1\text{)},
$$

so $E\subset\left(0,\sqrt2-1\right]$, which is bounded above and below; $E$ is a bounded set.

(4) When $n$ is even, $\left(-1\right)^nn^2-n=n^2-n$, with absolute value $n^2-n$; when $n$ is odd, $\left(-1\right)^nn^2-n=-n^2-n$, with absolute value $n^2+n$. In either case, the absolute value grows without bound as $n$ increases, so $E$ is neither bounded above nor below, and is not a bounded set. $\blacksquare$
