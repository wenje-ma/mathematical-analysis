# week51

> **基础知识: 伽马函数的定义**<br>$\Gamma\left(\alpha\right)=\int_0^{+\infty}t^{\alpha-1}e^{-t}\mathrm dt$ ($\alpha> 0$). 递推公式 $\Gamma\left(\alpha+1\right)=\alpha\Gamma\left(\alpha\right)$, $\Gamma\left(1\right)=1$, $\Gamma\left(n+1\right)=n!$, $\Gamma\left(\frac12\right)=\sqrt\pi$.

> **基础知识: 贝塔函数的定义**<br>$\Beta\left(p,q\right)=\int_0^1 t^{p-1}\left(1-t\right)^{q-1}\mathrm dt$ ($p,q> 0$), 且 $\Beta\left(p,q\right)=\frac{\Gamma\left(p\right)\Gamma\left(q\right)}{\Gamma\left(p+q\right)}$.

> **命题 (伽马与贝塔的积分形式)**<br>$\int_0^{+\infty}\frac{x^{a-1}}{\left(1+x\right)^{a+b}}\mathrm dx=\Beta\left(a,b\right)$; $\int_0^{\pi/2}\sin^m x\cos^n x\,\mathrm dx=\frac12\Beta\left(\frac{m+1}2,\frac{n+1}2\right)$.

---

## 12.6-1-1

计算 $\int_0^{+\infty}\frac{4\sqrt x}{\left(1+x\right)^2}\mathrm dx$.

### 解答 12.6-1-1

由**命题 (伽马与贝塔的积分形式)**, $a=\frac32$, $b=\frac12$. 由**基础知识: 伽马函数的定义**, $\Gamma\left(\frac32\right)=\frac{\sqrt\pi}2$, $\Gamma\left(\frac12\right)=\sqrt\pi$. 故原式 $=4\cdot\frac{\pi}2=2\pi$. $\blacksquare$

---

## 12.6-1-2

计算 $\int_0^{+\infty}x^{-1/2}e^{-\alpha x}\mathrm dx$ ($\alpha> 0$).

### 解答 12.6-1-2

代换 $t=\alpha x$, 由**基础知识: 伽马函数的定义**, 得 $\sqrt{\frac\pi\alpha}$. $\blacksquare$

---

## 12.6-1-3

计算 $\int_0^1 x^8\sqrt{1-x^3}\mathrm dx$.

### 解答 12.6-1-3

代换 $t=x^3$, 得 $\frac13\Beta\left(3,\frac32\right)=\frac{16}{315}$. $\blacksquare$

---

## 12.6-1-4

计算 $\int_0^{\pi/2}\sin^6x\cos^4x\,\mathrm dx$.

### 解答 12.6-1-4

由**命题 (伽马与贝塔的积分形式)**, $=\frac12\Beta\left(\frac72,\frac52\right)=\frac{3\pi}{512}$. $\blacksquare$

---

## 12.6-1-9

计算 $\int_0^1\frac{\mathrm dx}{\sqrt{1-x^4}}$.

### 解答 12.6-1-9

代换 $t=x^4$, 得 $\frac14\Beta\left(\frac14,\frac12\right)$. $\blacksquare$

---

## 12.6-1-10

计算 $\int_0^{+\infty}\frac{\mathrm dx}{1+x^3}$.

### 解答 12.6-1-10

代换 $u=x^3$, 得 $\frac13\Beta\left(\frac13,\frac23\right)=\frac13\Gamma\left(\frac13\right)\Gamma\left(\frac23\right)$. $\blacksquare$

---

## 12.6-2

证明 $\Gamma\left(\alpha\right)$ 在 $\left(0,+\infty\right)$ 上不一致收敛.

### 解答 12.6-2

取 $\alpha_n=\frac1n\to0+$, 则 $\int_0^{1/n}t^{\alpha_n-1}e^{-t}\mathrm dt\to1\ne0$. 故不满足一致收敛的柯西条件. $\blacksquare$
