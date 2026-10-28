# week25

> **Basic Knowledge: Definition of Uniform Continuity**<br>$f$ is uniformly continuous on $X$ if for every $\varepsilon> 0$ there exists $\delta> 0$ such that $\left|f\left(x_1\right)-f\left(x_2\right)\right|< \varepsilon$ whenever $\left|x_1-x_2\right|< \delta$.

> **Theorem 1.3 (Lagrange Mean Value Theorem)**<br>If $f$ is continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$, then there exists $c\in\left(a,b\right)$ such that $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

> **Theorem 3.2 (Heine-Borel Covering Theorem)**<br>Any open cover of a closed interval $\left[a,b\right]$ has a finite subcover.

---

## 5.3-2

Prove $f\left(x\right)=\frac1x$ is not uniformly continuous on $\left(0,1\right)$.

### Solution 5.3-2

Take $\varepsilon_0=1$. For any $\delta> 0$, take $x_1=\frac\delta2$, $x_2=\frac\delta3$. Then $\left|x_1-x_2\right|< \delta$ but $\left|f\left(x_1\right)-f\left(x_2\right)\right|=\frac1\delta> 1$ when $\delta< 1$. $\blacksquare$

---

## 5.3-3

Construct an open cover of $E=\left\{\frac1n\right\}$ with no finite subcover.

### Solution 5.3-3

Take $I_n=\left(\frac1n-\frac1{4n^2},\frac1n+\frac1{4n^2}\right)$. Any finite subcollection covers only finitely many points. $\blacksquare$

---

## 5.3-4

Prove every open cover of $E=\left\{\frac1n\right\}\cup\left\{0\right\}$ has a finite subcover.

### Solution 5.3-4

Since $0\in E$, some open set $I_0$ contains a neighborhood $\left(-\delta,\delta\right)$ of $0$. Choose $N$ with $\frac1N< \delta$. Then $I_0$ covers all $\frac1n$ for $n> N$. The remaining finitely many points are covered by finitely many additional sets. $\blacksquare$

---

## 5.3-5

Prove $\sin x$ is uniformly continuous on $\mathbb R$.

### Solution 5.3-5

By **Theorem 1.3 (Lagrange Mean Value Theorem)**, $\left|\sin x_1-\sin x_2\right|\le\left|x_1-x_2\right|$. Take $\delta=\varepsilon$. $\blacksquare$

---

## 5.3-6

Prove $\cos x$ is uniformly continuous on $\mathbb R$.

### Solution 5.3-6

By **Theorem 1.3 (Lagrange Mean Value Theorem)**, $\left|\cos x_1-\cos x_2\right|\le\left|x_1-x_2\right|$. Take $\delta=\varepsilon$. $\blacksquare$

---

## 5.3-7

Prove $f\left(x\right)=\sin 3x+5x+1$ is uniformly continuous on $\mathbb R$.

### Solution 5.3-7

$\left|f\left(x_1\right)-f\left(x_2\right)\right|\le8\left|x_1-x_2\right|$. Take $\delta=\frac\varepsilon8$. $\blacksquare$

---

## 5.3-8

Prove:

(1) A Holder continuous function is uniformly continuous;

(2) If $f$ is differentiable with bounded derivative, then $f$ satisfies the Holder condition with $\alpha=1$.

### Solution 5.3-8

(1) Take $\delta=\left(\frac\varepsilon H\right)^{1/\alpha}$. Then $\left|f\left(x_1\right)-f\left(x_2\right)\right|< \varepsilon$.

(2) By **Theorem 1.3 (Lagrange Mean Value Theorem)**, $\left|f\left(x_1\right)-f\left(x_2\right)\right|\le M\left|x_1-x_2\right|$. $\blacksquare$
