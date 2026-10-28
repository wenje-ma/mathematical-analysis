# week41

> **定理 2.3 (比较判别法的极限形式)**<br>设 $\sum a_n$ 与 $\sum b_n$ 为正项级数, 且 $\lim_{n\to\infty}\frac{a_n}{b_n}=l$. 当 $0< l< +\infty$ 时两级数同敛散.

> **定理 4.1 (无穷乘积与级数的关系)**<br>设 $p_n> 0$, 则 $\prod p_n$ 收敛的充要条件是 $\sum\ln p_n$ 收敛, 且此时 $\prod p_n=\exp\left(\sum\ln p_n\right)$.

> **定理 4.2 (同号项无穷乘积)**<br>设 $\alpha_n\ge0$ (或 $\alpha_n\le0$), 则 $\prod\left(1+\alpha_n\right)$ 收敛的充要条件是 $\sum\alpha_n$ 收敛.

> **定理 4.4 (绝对收敛)**<br>设 $\alpha_n\ne-1$, 则 $\prod\left(1+\alpha_n\right)$ 绝对收敛的充要条件是 $\sum\left|\alpha_n\right|$ 收敛.

---

## 10.4-1-2

讨论 $\prod_{n=2}^\infty\sqrt{\frac{n^2+1}{n^2-1}}$ 的收敛性.

### 解答 10.4-1-2

令 $\alpha_n=\frac2{n^2-1}> 0$. 因 $\alpha_n\sim\frac2{n^2}$, 及**定理 2.3 (比较判别法的极限形式)**, $\sum\alpha_n$ 收敛. 由**定理 4.2 (同号项无穷乘积)**, 原无穷乘积收敛. $\blacksquare$

---

## 10.4-1-4

讨论 $\prod_{n=1}^\infty\left(1+\frac{x^n}{2^n}\right)$ 的收敛性.

### 解答 10.4-1-4

令 $\alpha_n=\left(\frac x2\right)^n$. 当 $\left|x\right|< 2$ 时, $\sum\left|\alpha_n\right|$ 收敛, 由**定理 4.4 (绝对收敛)**, 原乘积收敛. 当 $\left|x\right|\ge2$ 时, $1+\alpha_n$ 不趋于 $1$, 发散. $\blacksquare$

---

## 10.4-1-6

讨论 $\prod_{n=1}^\infty\cos\frac1n$ 的收敛性.

### 解答 10.4-1-6

由**定理 4.1 (无穷乘积与级数的关系)**, 考察 $\sum\ln\cos\frac1n$. 因 $\ln\cos\frac1n\sim-\frac1{2n^2}$, 及**定理 2.3 (比较判别法的极限形式)**, $\sum\ln\cos\frac1n$ 收敛. 故原乘积收敛. $\blacksquare$

---

## 10.4-1-8

讨论 $\prod_{n=1}^\infty\left(1+\frac1{\sqrt n}\right)$ 的收敛性.

### 解答 10.4-1-8

令 $\alpha_n=\frac1{\sqrt n}> 0$. 因 $\sum\frac1{\sqrt n}$ 发散, 由**定理 4.2 (同号项无穷乘积)**, 原乘积发散. $\blacksquare$

---

## 10.4-2

设 $0< \alpha_n< \frac\pi2$, $\sum\alpha_n^2$ 收敛, 证明 $\prod\cos\alpha_n$ 收敛.

### 解答 10.4-2

因 $\ln\cos\alpha_n\sim-\frac{\alpha_n^2}{2}$, 及**定理 2.3 (比较判别法的极限形式)**, $\sum\ln\cos\alpha_n$ 收敛. 由**定理 4.1 (无穷乘积与级数的关系)**, 原乘积收敛. $\blacksquare$

---

## 10.4-3

设 $\left|\alpha_n\right|< \frac\pi4$, $\sum\left|\alpha_n\right|$ 收敛, 证明 $\prod\tan\left(\frac\pi4+\alpha_n\right)$ 绝对收敛.

### 解答 10.4-3

因 $\left|\tan\left(\frac\pi4+\alpha_n\right)-1\right|\sim2\left|\alpha_n\right|$, 及**定理 2.3 (比较判别法的极限形式)**, $\sum\left|\tan\left(\frac\pi4+\alpha_n\right)-1\right|$ 收敛. 由**定理 4.4 (绝对收敛)**, 原乘积绝对收敛. $\blacksquare$

---

## 10.4-5

证明: 若 $\prod\left(1+\left|\alpha_n\right|\right)$ 收敛, 则 $\prod\left(1+\alpha_n\right)$ 收敛.

### 解答 10.4-5

由**定理 4.2 (同号项无穷乘积)**, $\prod\left(1+\left|\alpha_n\right|\right)$ 收敛蕴含 $\sum\left|\alpha_n\right|$ 收敛. 由**定理 4.4 (绝对收敛)**, $\prod\left(1+\alpha_n\right)$ 绝对收敛, 从而收敛. $\blacksquare$
