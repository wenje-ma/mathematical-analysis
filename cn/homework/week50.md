# week50

> **定理 4.3 (魏尔斯特拉斯判别法)**<br>若 $\left|f\left(x,y\right)\right|\le F\left(x\right)$ 且瑕积分 $\int_a^b F\left(x\right)\mathrm dx$ 收敛, 则 $\int_a^b f\left(x,y\right)\mathrm dx$ 关于 $y$ 一致收敛.

> **定理 4.7 (积分次序交换定理)**<br>若 $f\left(x,y\right)$ 连续且保持固定符号, $\int_a^b f\left(x,y\right)\mathrm dx$ 关于 $y\in\left[c,d\right]$ 一致收敛, 则 $\int_c^d\mathrm dy\int_a^b f\,\mathrm dx=\int_a^b\mathrm dx\int_c^d f\,\mathrm dy$.

---

## 12.5-1-1

讨论 $\int_0^1\frac{\sin x}{x^\alpha}\mathrm dx$ 在 (i) $\alpha\le\alpha_0< 2$; (ii) $\alpha< 2$ 上的一致收敛性.

### 解答 12.5-1-1

(i) 因 $\left|\frac{\sin x}{x^\alpha}\right|\le x^{1-\alpha_0}$, 及**定理 4.3 (魏尔斯特拉斯判别法)**, 一致收敛.

(ii) 取 $\alpha_n=2-\frac1n$, 则 $\int_0^{1/n}\frac{\sin x}{x^{\alpha_n}}\mathrm dx\to1\ne0$. 故在 $\alpha< 2$ 上不一致收敛. $\blacksquare$

---

## 12.5-1-2

讨论 $\int_0^1 x^{p-1}\mathrm dx$ 在 (i) $p\ge p_0> 0$; (ii) $p> 0$ 上的一致收敛性.

### 解答 12.5-1-2

(i) 因 $x^{p-1}\le x^{p_0-1}$, 及**定理 4.3 (魏尔斯特拉斯判别法)**, 一致收敛.

(ii) 取 $p_n=\frac1n$, 则 $\int_0^{1/n}x^{p_n-1}\mathrm dx\to1\ne0$. 故在 $p> 0$ 上不一致收敛. $\blacksquare$

---

## 12.5-2-1

求 $\int_0^1\frac{x^b-x^a}{\ln x}\mathrm dx$ ($a> -1,b> -1$).

### 解答 12.5-2-1

由 $\frac{x^b-x^a}{\ln x}=\int_a^b x^y\mathrm dy$, 及**定理 4.7 (积分次序交换定理)**, $I=\int_a^b\frac{\mathrm dy}{y+1}=\ln\frac{1+b}{1+a}$. $\blacksquare$
