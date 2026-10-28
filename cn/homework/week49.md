# week49

> **定理 4.3 (魏尔斯特拉斯判别法)**<br>若 $\left|f\left(x,y\right)\right|\le F\left(x\right)$ 且 $\int_a^{+\infty}F\left(x\right)\mathrm dx$ 收敛, 则 $\int_a^{+\infty}f\left(x,y\right)\mathrm dx$ 关于 $y$ 一致收敛.

> **定理 4.4 (阿贝尔判别法)**<br>若 $\int_a^{+\infty}f\left(x,y\right)\mathrm dx$ 一致收敛, $g\left(x,y\right)$ 关于 $x$ 单调且一致有界, 则 $\int_a^{+\infty}fg\,\mathrm dx$ 一致收敛.

> **例 4.5 (狄利克雷积分)**<br>$\int_0^{+\infty}\frac{\sin x}{x}\mathrm dx=\frac\pi2$. 一般地, $\int_0^{+\infty}\frac{\sin\left(kx\right)}x\mathrm dx=\frac\pi2\operatorname{sgn}\left(k\right)$.

> **定理 4.7 (积分次序交换定理)**<br>若 $f$ 连续且 $\int_a^{+\infty}f\left(x,y\right)\mathrm dx$ 关于 $y\in\left[c,d\right]$ 一致收敛, 则 $\int_c^d\mathrm dy\int_a^{+\infty}f\,\mathrm dx=\int_a^{+\infty}\mathrm dx\int_c^d f\,\mathrm dy$.

> **定理 4.8 (积分号下求导)**<br>若 $f$ 与 $f_y$ 连续, $\int_a^{+\infty}f$ 收敛, $\int_a^{+\infty}f_y$ 一致收敛, 则 $I'\left(y\right)=\int_a^{+\infty}f_y\,\mathrm dx$.

---

## 12.4-1-1

讨论 $\int_0^{+\infty}e^{-\alpha x^2}\mathrm dx$ 在 $\alpha\in\left[\alpha_0,+\infty\right)$ 上的一致收敛性.

### 解答 12.4-1-1

因 $e^{-\alpha x^2}\le e^{-\alpha_0x^2}$, 及**定理 4.3 (魏尔斯特拉斯判别法)**, 一致收敛. $\blacksquare$

---

## 12.4-1-3

讨论 $\int_1^{+\infty}e^{-xy}\frac{\cos x}{x}\mathrm dx$ 在 $y\in\left[0,+\infty\right)$ 上的一致收敛性.

### 解答 12.4-1-3

$\int_1^{+\infty}\frac{\cos x}{x}\mathrm dx$ 收敛且不含 $y$, $e^{-xy}$ 单调且一致有界. 由**定理 4.4 (阿贝尔判别法)**, 一致收敛. $\blacksquare$

---

## 12.4-1-5

讨论 $\int_0^{+\infty}e^{-x^2y^2}\cos x\,\mathrm dx$ 在 $y\in\left[y_0,+\infty\right)$ 上的一致收敛性.

### 解答 12.4-1-5

因 $\left|e^{-x^2y^2}\cos x\right|\le e^{-x^2y_0^2}$, 及**定理 4.3 (魏尔斯特拉斯判别法)**, 一致收敛. $\blacksquare$

---

## 12.4-2-1

求 $\int_0^{+\infty}\frac{e^{-ax}-e^{-bx}}x\mathrm dx$ ($0< a< b$).

### 解答 12.4-2-1

由 $\frac{e^{-ax}-e^{-bx}}x=\int_a^b e^{-xy}\mathrm dy$, 及**定理 4.7 (积分次序交换定理)**, $I=\int_a^b\frac{\mathrm dy}y=\ln\frac ba$. $\blacksquare$

---

## 12.4-2-2

求 $\int_0^{+\infty}\frac{\sin\left(\alpha x\right)\cos\left(\beta x\right)}x\mathrm dx$.

### 解答 12.4-2-2

利用三角恒等式及**例 4.5 (狄利克雷积分)**, 得 $I=\begin{cases}0,&\alpha< \beta\\ \frac\pi4,&\alpha=\beta\\ \frac\pi2,&\alpha> \beta\end{cases}$. $\blacksquare$

---

## 12.4-2-4

求 $\int_0^{+\infty}\frac{1-\cos\left(\alpha x\right)}x e^{-x}\mathrm dx$.

### 解答 12.4-2-4

由**定理 4.8 (积分号下求导)**, $I'\left(\alpha\right)=\int_0^{+\infty}e^{-x}\sin\left(\alpha x\right)\mathrm dx=\frac{\alpha}{1+\alpha^2}$. 积分并利用 $I\left(0\right)=0$, 得 $I\left(\alpha\right)=\frac12\ln\left(1+\alpha^2\right)$. $\blacksquare$

---

## 12.4-5

证明迪尼定理: 若 $u_n\left(x\right)\ge0$ 连续, $\sum u_n\left(x\right)$ 点态收敛于连续函数 $S\left(x\right)$, 则一致收敛.

### 解答 12.4-5

令余项 $R_N\left(x\right)=S\left(x\right)-S_N\left(x\right)$. 反证: 若不一致收敛, 则存在 $x_k\to x_0$ 使 $R_{N_k}\left(x_k\right)\ge\varepsilon_0$. 由单调性与连续性, 对任意 $m$, $R_m\left(x_0\right)\ge\varepsilon_0$, 与 $R_m\left(x_0\right)\to0$ 矛盾. $\blacksquare$
