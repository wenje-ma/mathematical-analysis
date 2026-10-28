# week19

> **定理 2.1 (第一换元法则)**<br>设 $F'\left(u\right)=f\left(u\right)$, 且 $u=\varphi\left(x\right)$ 可导, 则 $\int f\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm dx=F\left(\varphi\left(x\right)\right)+C$.

> **定理 2.2 (第二换元法则)**<br>设 $x=\varphi\left(t\right)$ 可导且有反函数, 又设 $\int f\left(\varphi\left(t\right)\right)\varphi'\left(t\right)\,\mathrm dt=G\left(t\right)+C$, 则 $\int f\left(x\right)\,\mathrm dx=G\left(\varphi^{-1}\left(x\right)\right)+C$.

---

## 4.2-1-2

求不定积分 $\int\sqrt{2x+3}\,\mathrm dx$.

### 解答 4.2-1-2

令 $u=2x+3$, 则 $\mathrm du=2\mathrm dx$. 由**定理 2.1 (第一换元法则)**,

$$
\int\sqrt{2x+3}\,\mathrm dx=\frac12\int u^{1/2}\,\mathrm du=\frac13\left(2x+3\right)^{3/2}+C.
$$

$\blacksquare$

---

## 4.2-1-4

求不定积分 $\int\frac{\mathrm dx}{\left(x-1\right)^5}$.

### 解答 4.2-1-4

令 $u=x-1$. 由**定理 2.1 (第一换元法则)**,

$$
\int\frac{\mathrm dx}{\left(x-1\right)^5}=\int u^{-5}\,\mathrm du=-\frac1{4\left(x-1\right)^4}+C.
$$

$\blacksquare$

---

## 4.2-1-6

求不定积分 $\int\mathrm{sh}\,x\,\mathrm dx$.

### 解答 4.2-1-6

由 $\left(\mathrm{ch}\,x\right)'=\mathrm{sh}\,x$, $\int\mathrm{sh}\,x\,\mathrm dx=\mathrm{ch}\,x+C$. $\blacksquare$

---

## 4.2-1-8

求不定积分 $\int\frac{\mathrm dx}{a^2+b^2x^2}$ ($a> 0$, $b> 0$).

### 解答 4.2-1-8

变形: $\frac1{a^2+b^2x^2}=\frac1{a^2}\cdot\frac1{1+\left(\frac{bx}{a}\right)^2}$. 令 $u=\frac{bx}{a}$. 由**定理 2.1 (第一换元法则)**,

$$
\int\frac{\mathrm dx}{a^2+b^2x^2}=\frac1{ab}\arctan\frac{bx}{a}+C.
$$

$\blacksquare$

---

## 4.2-1-10

求不定积分 $\int\frac{\mathrm dx}{\sin x+\cos x}$.

### 解答 4.2-1-10

利用 $\sin x+\cos x=\sqrt2\sin\left(x+\frac\pi4\right)$. 令 $u=x+\frac\pi4$. 由**定理 2.1 (第一换元法则)**,

$$
\int\frac{\mathrm dx}{\sin x+\cos x}=\frac1{\sqrt2}\int\frac{\mathrm du}{\sin u}=\frac1{\sqrt2}\ln\left|\csc u-\cot u\right|+C.
$$

$\blacksquare$

---

## 4.2-2-1

求不定积分 $\int\sqrt{a^2-x^2}\,\mathrm dx$ ($a> 0$).

### 解答 4.2-2-1

令 $x=a\sin t$. 由**定理 2.2 (第二换元法则)**,

$$
\int\sqrt{a^2-x^2}\,\mathrm dx=a^2\int\cos^2t\,\mathrm dt=\frac{a^2}2\left(t+\sin t\cos t\right)+C.
$$

代回 $t=\arcsin\frac xa$, 得

$$
\int\sqrt{a^2-x^2}\,\mathrm dx=\frac{a^2}2\arcsin\frac xa+\frac x2\sqrt{a^2-x^2}+C.
$$

$\blacksquare$

---

## 4.2-2-3

求不定积分 $\int\frac{\mathrm dx}{\sqrt{x^2+a^2}}$ ($a> 0$).

### 解答 4.2-2-3

令 $x=a\tan t$. 由**定理 2.2 (第二换元法则)**,

$$
\int\frac{\mathrm dx}{\sqrt{x^2+a^2}}=\int\sec t\,\mathrm dt=\ln\left|\sec t+\tan t\right|+C.
$$

代回得

$$
\int\frac{\mathrm dx}{\sqrt{x^2+a^2}}=\ln\left(x+\sqrt{x^2+a^2}\right)+C'.
$$

$\blacksquare$

---

## 4.2-2-5

求不定积分 $\int\sqrt{x^2-a^2}\,\mathrm dx$ ($a> 0$).

### 解答 4.2-2-5

令 $x=a\sec t$. 由**定理 2.2 (第二换元法则)**,

$$
\int\sqrt{x^2-a^2}\,\mathrm dx=a^2\int\left(\sec^3t-\sec t\right)\,\mathrm dt.
$$

由分部积分可得 $\int\sec^3t\,\mathrm dt=\frac12\left(\sec t\tan t+\ln\left|\sec t+\tan t\right|\right)+C$. 故

$$
\int\sqrt{x^2-a^2}\,\mathrm dx=\frac x2\sqrt{x^2-a^2}-\frac{a^2}2\ln\left|x+\sqrt{x^2-a^2}\right|+C.
$$

$\blacksquare$

---

## 4.2-2-7

求不定积分 $\int\frac{\mathrm dx}{x\sqrt{a^2-x^2}}$ ($a> 0$).

### 解答 4.2-2-7

令 $x=a\sin t$. 由**定理 2.2 (第二换元法则)**,

$$
\int\frac{\mathrm dx}{x\sqrt{a^2-x^2}}=\frac1a\int\frac{\mathrm dt}{\sin t}=\frac1a\ln\left|\csc t-\cot t\right|+C.
$$

代回得

$$
\int\frac{\mathrm dx}{x\sqrt{a^2-x^2}}=\frac1a\ln\left|\frac{a-\sqrt{a^2-x^2}}x\right|+C.
$$

$\blacksquare$

---

## 4.2-2-9

求不定积分 $\int\sqrt{7+x-x^2}\,\mathrm dx$.

### 解答 4.2-2-9

配方: $7+x-x^2=\frac{29}4-\left(x-\frac12\right)^2$. 令 $u=x-\frac12$. 由**定理 2.1 (第一换元法则)** 及 4.2-2-1 的结果,

$$
\int\sqrt{7+x-x^2}\,\mathrm dx=\frac{29}8\arcsin\frac{2x-1}{\sqrt{29}}+\frac{2x-1}4\sqrt{7+x-x^2}+C.
$$

$\blacksquare$

---

## 4.2-2-11

求不定积分 $\int\frac{\mathrm dx}{x^2\sqrt{x^2+a^2}}$ ($a> 0$).

### 解答 4.2-2-11

令 $x=a\tan t$. 由**定理 2.2 (第二换元法则)**,

$$
\int\frac{\mathrm dx}{x^2\sqrt{x^2+a^2}}=\frac1{a^2}\int\frac{\cos t}{\sin^2t}\,\mathrm dt.
$$

令 $u=\sin t$, 则 $\frac1{a^2}\int\frac{\mathrm du}{u^2}=-\frac1{a^2u}+C$. 代回 $u=\frac{x}{\sqrt{x^2+a^2}}$, 得

$$
\int\frac{\mathrm dx}{x^2\sqrt{x^2+a^2}}=-\frac{\sqrt{x^2+a^2}}{a^2x}+C.
$$

$\blacksquare$
