# week23

> **基础知识: 上确界与下确界的定义**<br>设 $E$ 为有界集合. 若实数 $\beta$ 满足: (1) $\beta$ 是 $E$ 的上界; (2) 对任意 $\varepsilon> 0$, 存在 $x_0\in E$ 使得 $x_0> \beta-\varepsilon$, 则称 $\beta$ 为 $E$ 的上确界, 记作 $\sup E$. 类似地定义下确界 $\inf E$.

> **基础知识: 振幅的定义**<br>设 $f$ 在区间 $I$ 中有定义且有界. 称 $\omega_f\left(I\right)=\sup\left\{f\left(x\right):x\in I\right\}-\inf\left\{f\left(x\right):x\in I\right\}$ 为 $f$ 在 $I$ 上的振幅.

> **定理 1.3 (连续的充要条件)**<br>设 $y=f\left(x\right)$ 在 $x_0$ 点附近为有界函数. 则 $f$ 在 $x_0$ 点连续的充要条件是 $\omega_f\left(x_0\right)=0$.

---

## 5.1-4

设 $y=f\left(x\right)$ 及 $y=g\left(x\right)$ 为 $\left[a,b\right]$ 上的有界函数. 证明:

(1) $\sup_{\left[a,b\right]}\left\{f\left(x\right)+g\left(x\right)\right\}\le\sup_{\left[a,b\right]}f\left(x\right)+\sup_{\left[a,b\right]}g\left(x\right)$;

(2) $\inf_{\left[a,b\right]}\left\{f\left(x\right)+g\left(x\right)\right\}\ge\inf_{\left[a,b\right]}f\left(x\right)+\inf_{\left[a,b\right]}g\left(x\right)$.

### 解答 5.1-4

(1) 对任意 $x\in\left[a,b\right]$, $f\left(x\right)\le\sup f$, $g\left(x\right)\le\sup g$. 故 $f\left(x\right)+g\left(x\right)\le\sup f+\sup g$. 即 $\sup f+\sup g$ 是 $f+g$ 的一个上界. 由**基础知识: 上确界与下确界的定义**, 上确界是最小上界, 得 $\sup\left\{f+g\right\}\le\sup f+\sup g$.

(2) 同理, $f\left(x\right)+g\left(x\right)\ge\inf f+\inf g$, 故 $\inf\left\{f+g\right\}\ge\inf f+\inf g$. $\blacksquare$

---

## 5.1-5

证明: $\omega_f\left(I\right)=\sup\left\{\left|f\left(x_1\right)-f\left(x_2\right)\right|:x_1,x_2\in I\right\}$.

### 解答 5.1-5

记 $M=\sup\left\{f\left(x\right):x\in I\right\}$, $m=\inf\left\{f\left(x\right):x\in I\right\}$. 则 $\omega_f\left(I\right)=M-m$.

对任意 $x_1,x_2\in I$, $\left|f\left(x_1\right)-f\left(x_2\right)\right|\le M-m$. 故 $M-m$ 是该集合的一个上界.

另一方面, 对任意 $\varepsilon> 0$, 存在 $x_1,x_2\in I$ 使得 $f\left(x_1\right)> M-\frac\varepsilon2$, $f\left(x_2\right)< m+\frac\varepsilon2$. 于是 $\left|f\left(x_1\right)-f\left(x_2\right)\right|> M-m-\varepsilon$. 由**基础知识: 上确界与下确界的定义**, $\sup\left\{\left|f\left(x_1\right)-f\left(x_2\right)\right|\right\}\ge M-m$.

综合两方面, $\omega_f\left(I\right)=\sup\left\{\left|f\left(x_1\right)-f\left(x_2\right)\right|\right\}$. $\blacksquare$

---

## 5.1-6

设 $y=D\left(x\right)$ 为狄利克雷函数, 即 $D\left(x\right)=0$ ($x$ 为无理数), $D\left(x\right)=1$ ($x$ 为有理数). 证明: $D\left(x\right)$ 在任意区间中的振幅为 $1$, 且在每一点的振幅为 $1$.

### 解答 5.1-6

对任意区间 $I$, $I$ 中既有有理数又有无理数. 故 $\sup_{x\in I}D\left(x\right)=1$, $\inf_{x\in I}D\left(x\right)=0$. 因此 $\omega_D\left(I\right)=1$.

对任意点 $x_0$, 在 $x_0$ 的任意邻域内都既有有理数又有无理数. 故 $\omega_D\left(x_0\right)=1$. 由**定理 1.3 (连续的充要条件)**, $D\left(x\right)$ 在每一点都不连续. $\blacksquare$

---

## 5.1-7

试利用非空有上界必有上确界的定理推出: 单调递增有上界的序列一定有极限.

### 解答 5.1-7

设 $\left\{a_n\right\}$ 单调递增且有上界. 由上确界存在定理, $E=\left\{a_n:n\ge1\right\}$ 有上确界 $l=\sup E$.

对任意 $\varepsilon> 0$, 由**基础知识: 上确界与下确界的定义**, 存在 $N$ 使得 $a_N> l-\varepsilon$. 又因 $\left\{a_n\right\}$ 单调递增, 当 $n> N$ 时 $a_n\ge a_N> l-\varepsilon$. 另一方面 $a_n\le l< l+\varepsilon$. 故 $\left|a_n-l\right|< \varepsilon$. 由序列极限的定义, $\lim_{n\to\infty}a_n=l$. $\blacksquare$

---

## 5.1-9

设 $y=R\left(x\right)$ 为黎曼函数, 即 $R\left(x\right)=0$ ($x$ 为无理数), $R\left(x\right)=1/q$ ($x=p/q$ 为既约有理数). 证明:

(1) 对任意有理数 $x=p/q$, $\omega_R\left(x\right)=1/q$;

(2) 对任意无理数 $x$, $\omega_R\left(x\right)=0$.

### 解答 5.1-9

(1) 设 $x_0=p/q$ 为既约有理数, 则 $R\left(x_0\right)=1/q$. 在 $x_0$ 的任意邻域内, 既有无理数 $x$ 使得 $R\left(x\right)=0$, 又有 $x_0$ 本身. 故 $\sup R=1/q$, $\inf R=0$. 因此 $\omega_R\left(x_0\right)=1/q$.

(2) 设 $x_0$ 为无理数. 对任意 $\varepsilon> 0$, 满足 $1/q\ge\varepsilon$ 的正整数 $q$ 只有有限多个, 对应的既约有理数 $p/q$ 也只有有限多个. 因此在 $x_0$ 的某个足够小的邻域内, 其余有理点都满足 $1/q< \varepsilon$. 故 $\sup R-\inf R< \varepsilon$. 由 $\varepsilon$ 的任意性, $\omega_R\left(x_0\right)=0$. 由**定理 1.3 (连续的充要条件)**, 黎曼函数在无理点连续. $\blacksquare$
