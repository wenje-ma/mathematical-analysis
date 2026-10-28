# week20

> **定理 3.1 (分部积分公式)**<br>设 $u\left(x\right),v\left(x\right)$ 可导, 则 $\int u\left(x\right)\,\mathrm dv\left(x\right)=u\left(x\right)v\left(x\right)-\int v\left(x\right)\,\mathrm du\left(x\right)$.

---

## 4.3-1-11

求不定积分 $\int x\csc^2x\,\mathrm dx$.

### 解答 4.3-1-11

令 $u=x$, $\mathrm dv=\csc^2x\,\mathrm dx$, 则 $\mathrm du=\mathrm dx$, $v=-\cot x$. 由**定理 3.1 (分部积分公式)**,

$$
\int x\csc^2x\,\mathrm dx=-x\cot x+\int\cot x\,\mathrm dx=-x\cot x+\ln\left|\sin x\right|+C.
$$

$\blacksquare$

---

## 4.3-1-13

求不定积分 $\int\sqrt{1+9x^2}\,\mathrm dx$.

### 解答 4.3-1-13

令 $u=\sqrt{1+9x^2}$, $\mathrm dv=\mathrm dx$. 由**定理 3.1 (分部积分公式)**,

$$
\int\sqrt{1+9x^2}\,\mathrm dx=x\sqrt{1+9x^2}-\int\frac{9x^2}{\sqrt{1+9x^2}}\,\mathrm dx.
$$

将被积函数变形: $\frac{9x^2}{\sqrt{1+9x^2}}=\sqrt{1+9x^2}-\frac1{\sqrt{1+9x^2}}$. 代入得

$$
2\int\sqrt{1+9x^2}\,\mathrm dx=x\sqrt{1+9x^2}+\int\frac{\mathrm dx}{\sqrt{1+9x^2}}.
$$

而 $\int\frac{\mathrm dx}{\sqrt{1+9x^2}}=\frac13\ln\left(3x+\sqrt{1+9x^2}\right)+C$. 故

$$
\int\sqrt{1+9x^2}\,\mathrm dx=\frac x2\sqrt{1+9x^2}+\frac16\ln\left(3x+\sqrt{1+9x^2}\right)+C.
$$

$\blacksquare$

---

## 4.3-1-14

求不定积分 $\int\sec^3x\,\mathrm dx$.

### 解答 4.3-1-14

令 $u=\sec x$, $\mathrm dv=\sec^2x\,\mathrm dx$. 由**定理 3.1 (分部积分公式)**,

$$
\int\sec^3x\,\mathrm dx=\sec x\tan x-\int\sec x\tan^2x\,\mathrm dx.
$$

利用 $\tan^2x=\sec^2x-1$,

$$
\int\sec^3x\,\mathrm dx=\sec x\tan x-\int\sec^3x\,\mathrm dx+\int\sec x\,\mathrm dx.
$$

移项得 $2\int\sec^3x\,\mathrm dx=\sec x\tan x+\int\sec x\,\mathrm dx$. 而 $\int\sec x\,\mathrm dx=\ln\left|\sec x+\tan x\right|+C$. 故

$$
\int\sec^3x\,\mathrm dx=\frac12\left(\sec x\tan x+\ln\left|\sec x+\tan x\right|\right)+C.
$$

$\blacksquare$
