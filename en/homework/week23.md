# week23

> **Basic Knowledge: Definition of Supremum and Infimum**<br>If $\beta$ is an upper bound of $E$ and for every $\varepsilon> 0$ there exists $x_0\in E$ with $x_0> \beta-\varepsilon$, then $\beta=\sup E$. Similarly for $\inf E$.

> **Basic Knowledge: Definition of Oscillation**<br>$\omega_f\left(I\right)=\sup\left\{f\left(x\right):x\in I\right\}-\inf\left\{f\left(x\right):x\in I\right\}$.

> **Theorem 1.3 (Necessary and Sufficient Condition for Continuity)**<br>$f$ is continuous at $x_0$ iff $\omega_f\left(x_0\right)=0$.

---

## 5.1-4

Prove:

(1) $\sup\left\{f+g\right\}\le\sup f+\sup g$;

(2) $\inf\left\{f+g\right\}\ge\inf f+\inf g$.

### Solution 5.1-4

(1) Since $f\left(x\right)\le\sup f$ and $g\left(x\right)\le\sup g$, their sum is bounded above by $\sup f+\sup g$. By **Basic Knowledge: Definition of Supremum and Infimum**, $\sup\left\{f+g\right\}\le\sup f+\sup g$.

(2) Similarly, $\inf\left\{f+g\right\}\ge\inf f+\inf g$. $\blacksquare$

---

## 5.1-5

Prove: $\omega_f\left(I\right)=\sup\left\{\left|f\left(x_1\right)-f\left(x_2\right)\right|:x_1,x_2\in I\right\}$.

### Solution 5.1-5

Let $M=\sup f$, $m=\inf f$. Then $\omega_f=M-m$. Every $\left|f\left(x_1\right)-f\left(x_2\right)\right|\le M-m$. Conversely, for any $\varepsilon> 0$, there exist $x_1,x_2$ with $f\left(x_1\right)> M-\frac\varepsilon2$, $f\left(x_2\right)< m+\frac\varepsilon2$, giving $\left|f\left(x_1\right)-f\left(x_2\right)\right|> M-m-\varepsilon$. Hence equality. $\blacksquare$

---

## 5.1-6

Let $D\left(x\right)$ be the Dirichlet function. Prove $\omega_D\left(I\right)=1$ for any interval $I$, and $\omega_D\left(x_0\right)=1$ at every point.

### Solution 5.1-6

Any interval contains both rational and irrational points, so $\sup D=1$, $\inf D=0$. Thus $\omega_D\left(I\right)=1$. By **Theorem 1.3 (Necessary and Sufficient Condition for Continuity)**, $D$ is discontinuous everywhere. $\blacksquare$

---

## 5.1-7

Prove that a monotone increasing sequence bounded above has a limit.

### Solution 5.1-7

Let $l=\sup E$ where $E=\left\{a_n\right\}$. For any $\varepsilon> 0$, there exists $N$ with $a_N> l-\varepsilon$. Since $\left\{a_n\right\}$ is increasing, for $n> N$, $l-\varepsilon< a_n\le l$. Hence $\lim_{n\to\infty}a_n=l$. $\blacksquare$

---

## 5.1-9

Let $R\left(x\right)$ be the Riemann function. Prove:

(1) $\omega_R\left(x\right)=1/q$ for rational $x=p/q$;

(2) $\omega_R\left(x\right)=0$ for irrational $x$.

### Solution 5.1-9

(1) Any neighborhood of $x_0=p/q$ contains both irrationals ($R=0$) and $x_0$ itself ($R=1/q$). Hence $\omega_R\left(x_0\right)=1/q$.

(2) For any $\varepsilon> 0$, only finitely many rationals $p/q$ satisfy $1/q\ge\varepsilon$. Hence in a small enough neighborhood of irrational $x_0$, all rationals have $R< \varepsilon$. Thus $\omega_R\left(x_0\right)=0$. By **Theorem 1.3 (Necessary and Sufficient Condition for Continuity)**, $R$ is continuous at irrationals. $\blacksquare$
