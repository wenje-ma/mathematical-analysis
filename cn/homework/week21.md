# week21

> **定理 2.1 (第一换元法则)**<br>设 $F'\left(u\right)=f\left(u\right)$, 且 $u=\varphi\left(x\right)$ 可导, 则 $\int f\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm dx=F\left(\varphi\left(x\right)\right)+C$.

> **定理 4.1 (有理函数的分解)**<br>任何有理函数 $\frac{P\left(x\right)}{Q\left(x\right)}$ 都可以分解为一个多项式与若干部分分式之和, 其中每个部分分式形如 $\frac{A}{\left(x-a\right)^k}$ 或 $\frac{Bx+C}{\left(x^2+px+q\right)^m}$ ($p^2-4q< 0$).

---

## 4.4-2

求不定积分 $\int\frac{x^3}{x^2+x-6}\,\mathrm dx$.

### 解答 4.4-2

先做多项式除法: $\frac{x^3}{x^2+x-6}=x-1+\frac{7x-6}{x^2+x-6}$. 分解分母: $x^2+x-6=\left(x+3\right)\left(x-2\right)$. 由**定理 4.1 (有理函数的分解)**, 设 $\frac{7x-6}{\left(x+3\right)\left(x-2\right)}=\frac A{x+3}+\frac B{x-2}$. 解得 $A=\frac{27}5$, $B=\frac85$. 故

$$
\int\frac{x^3}{x^2+x-6}\,\mathrm dx=\frac{x^2}2-x+\frac{27}5\ln\left|x+3\right|+\frac85\ln\left|x-2\right|+C.
$$

$\blacksquare$

---

## 4.4-4

求不定积分 $\int\frac{4x^2}{x\left(x+2\right)}\,\mathrm dx$.

### 解答 4.4-4

化简: $\frac{4x^2}{x\left(x+2\right)}=\frac{4x}{x+2}=4-\frac8{x+2}$. 故

$$
\int\frac{4x^2}{x\left(x+2\right)}\,\mathrm dx=4x-8\ln\left|x+2\right|+C.
$$

$\blacksquare$

---

## 4.4-6

求不定积分 $\int\frac{2x^2-5}{x^4-5x^2+6}\,\mathrm dx$.

### 解答 4.4-6

分解分母: $x^4-5x^2+6=\left(x^2-2\right)\left(x^2-3\right)$. 由**定理 4.1 (有理函数的分解)**, 设 $\frac{2x^2-5}{\left(x^2-2\right)\left(x^2-3\right)}=\frac A{x^2-2}+\frac B{x^2-3}$. 解得 $A=1$, $B=1$. 故

$$
\int\frac{2x^2-5}{x^4-5x^2+6}\,\mathrm dx=\frac1{2\sqrt2}\ln\left|\frac{x-\sqrt2}{x+\sqrt2}\right|+\frac1{2\sqrt3}\ln\left|\frac{x-\sqrt3}{x+\sqrt3}\right|+C.
$$

$\blacksquare$

---

## 4.4-8

求不定积分 $\int\frac x{\left(x^2+2\right)^2}\,\mathrm dx$.

### 解答 4.4-8

令 $u=x^2+2$. 由**定理 2.1 (第一换元法则)**,

$$
\int\frac x{\left(x^2+2\right)^2}\,\mathrm dx=\frac12\int\frac{\mathrm du}{u^2}=-\frac1{2\left(x^2+2\right)}+C.
$$

$\blacksquare$

---

## 4.4-10

求不定积分 $\int\frac{x^3}{\left(x-1\right)^2}\,\mathrm dx$.

### 解答 4.4-10

令 $u=x-1$. 被积函数变为 $\frac{\left(u+1\right)^3}{u^2}=u+3+\frac3u+\frac1{u^2}$. 故

$$
\int\frac{x^3}{\left(x-1\right)^2}\,\mathrm dx=\frac{\left(x-1\right)^2}2+3\left(x-1\right)+3\ln\left|x-1\right|-\frac1{x-1}+C.
$$

$\blacksquare$

---

## 4.4-12

求不定积分 $\int\frac{e^t}{e^{2t}+5e^t+6}\,\mathrm dt$.

### 解答 4.4-12

令 $u=e^t$. 积分化为 $\int\frac{\mathrm du}{\left(u+2\right)\left(u+3\right)}$. 由**定理 4.1 (有理函数的分解)**, $\frac1{\left(u+2\right)\left(u+3\right)}=\frac1{u+2}-\frac1{u+3}$. 故

$$
\int\frac{e^t}{e^{2t}+5e^t+6}\,\mathrm dt=\ln\frac{e^t+2}{e^t+3}+C.
$$

$\blacksquare$

---

## 4.4-14

求不定积分 $\int\frac{\mathrm dx}{\left(x^2+4\right)^2\left(x+1\right)}$.

### 解答 4.4-14

由**定理 4.1 (有理函数的分解)**, 设

$$
\frac1{\left(x^2+4\right)^2\left(x+1\right)}=\frac A{x+1}+\frac{Bx+C}{x^2+4}+\frac{Dx+E}{\left(x^2+4\right)^2}.
$$

解得 $A=\frac1{25}$, $B=-\frac1{25}$, $C=\frac1{25}$, $D=-\frac15$, $E=\frac15$. 合并各项得

$$
\int\frac{\mathrm dx}{\left(x^2+4\right)^2\left(x+1\right)}=\frac1{25}\ln\left|x+1\right|-\frac1{50}\ln\left(x^2+4\right)+\frac{13}{400}\arctan\frac x2+\frac{x+4}{40\left(x^2+4\right)}+C.
$$

$\blacksquare$
