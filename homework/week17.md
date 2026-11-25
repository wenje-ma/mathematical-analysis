# week17

> **定理 1.1 (收敛级数的必要条件)**
> 
> 若级数 $\sum{}a_n$ 收敛, 则 $\lim_{n\to\infty}a_n=0$.

> **定理 2.2 (比较判别法)**
> 
> 设 $\sum{}a_n$ 与 $\sum{}b_n$ 为正项级数, 且存在 $N_0$ 使 $a_n\le{}b_n$ ($n\ge{}N_0$). 若 $\sum{}b_n$ 收敛, 则 $\sum{}a_n$ 收敛.

> **定理 2.3 (比较判别法的极限形式)**
> 
> 设 $\sum{}a_n$ 与 $\sum{}b_n$ 为正项级数, 且 $\lim_{n\to\infty}\frac{a_n}{b_n}=l$. 当 $0<{}l<+\infty$ 时两级数同敛散.

> **定理 2.6 (达朗贝尔判别法)**
> 
> 设 $\sum{}a_n$ 为正项级数. 若 $\lim_{n\to\infty}\frac{a_{n+1}}{a_n}=r$, 则当 $r<1$ 时收敛, 当 $r>1$ 时发散.

> **定理 2.9 (积分判别法)**
> 
> 设 $f\left(x\right)$ 在 $\left[1,+\infty\right)$ 上正, 单调递减. 则 $\sum_{n=1}^\infty{}f\left(n\right)$ 与 $\int_1^{+\infty}f\left(x\right)\,\mathrm{d}x$ 同敛散.

## 9.4-8

求 $\oint_{L^+}\left(y^2+z^2-x^2\right)\,\mathrm{d}x+\left(x^2+z^2-y^2\right)\,\mathrm{d}y+\left(x^2+y^2-z^2\right)\,\mathrm{d}z$.

### 解答 9.4-8

旋度 $\nabla\times\boldsymbol{F}=2\left(y-z,z-x,x-y\right)$. 取曲面 $S$ 为上半球面. 由**定理 4.2 (斯托克斯公式)**, 化简后被积函数为 $2\left(R-\frac{Ry}{z}\right)$. 由对称性, $y/z$ 项积分为 $0$. 故 $\oint_{L^+}=2\pi{}Rr^2$.

$\blacksquare$

## 9.5-1

求下列向量场的散度与旋度:

(1) $\boldsymbol{F}=\left(4x,-2xy,z\right)$;

(2) $\boldsymbol{F}=\left(5x^2,y^2,z^2\right)$.

### 解答 9.5-1

(1) 由散度的定义, $\operatorname{div}\boldsymbol{F}=5-2x$. 由旋度的定义, $\operatorname{rot}\boldsymbol{F}=\left(0,0,-2y\right)$.

(2) $\operatorname{div}\boldsymbol{F}=10x+2y+2z$, $\operatorname{rot}\boldsymbol{F}=\left(0,0,0\right)$.

$\blacksquare$

## 9.5-2

证明: $\operatorname{div}\left(\Phi\boldsymbol{F}\right)=\Phi\operatorname{div}\boldsymbol{F}+\boldsymbol{F}\cdot\operatorname{grad}\Phi$.

### 解答 9.5-2

由散度的定义, 展开 $\frac{\partial\left(\Phi{}P\right)}{\partial{}x}+\frac{\partial\left(\Phi{}Q\right)}{\partial{}y}+\frac{\partial\left(\Phi{}R\right)}{\partial{}z}$, 合并同类项即得.

$\blacksquare$

## 9.5-3

证明: $\operatorname{rot}\left(\Phi\boldsymbol{F}\right)=\Phi\operatorname{rot}\boldsymbol{F}+\operatorname{grad}\Phi\times\boldsymbol{F}$.

### 解答 9.5-3

由旋度的定义, 计算第一个分量:

$$
\frac{\partial\left(\Phi{}R\right)}{\partial{}y}-\frac{\partial\left(\Phi{}Q\right)}{\partial{}z}=\Phi\left(\frac{\partial{}R}{\partial{}y}-\frac{\partial{}Q}{\partial{}z}\right)+\left(R\frac{\partial\Phi}{\partial{}y}-Q\frac{\partial\Phi}{\partial{}z}\right).
$$

第二项即为 $\operatorname{grad}\Phi\times\boldsymbol{F}$ 的第一个分量. 同理验证其余分量.

$\blacksquare$

## 9.5-4

证明: $\operatorname{rot}\left(\operatorname{grad}\Phi\right)=0$.

### 解答 9.5-4

由旋度的定义, $\operatorname{rot}\left(\operatorname{grad}\Phi\right)$ 的每个分量均为二阶混合偏导数之差. 因二阶混合偏导数连续, 与求导次序无关, 故各分量均为 $0$.

$\blacksquare$

## 9.5-5

证明: $\operatorname{div}\left(\operatorname{rot}\boldsymbol{F}\right)=0$.

### 解答 9.5-5

由散度的定义 与旋度的定义, 展开后各项两两抵消. 因二阶混合偏导数连续, 与求导次序无关, 故结果为 $0$.

$\blacksquare$

## 10.1-1

证明等比级数 $a_0+a_0q+\cdots$ 当 $\left|q\right|<1$ 时收敛且和为 $\frac{a_0}{1-q}$, 当 $\left|q\right|\ge1$ 时发散.

### 解答 10.1-1

部分和 $S_n=a_0\frac{1-q^{n+1}}{1-q}$. 当 $\left|q\right|<1$ 时, $q^{n+1}\to0$, 由级数收敛的定义, 级数收敛且和为 $\frac{a_0}{1-q}$. 当 $q=1$ 时 $S_n\to\infty$. 当 $\left|q\right|>1$ 时通项不趋于 $0$, 由**定理 1.1 (收敛级数的必要条件)**, 发散.

$\blacksquare$

## 10.1-2-1

讨论 $\sum_{n=1}^\infty\left(\sqrt{n+1}-\sqrt{n}\right)$ 的收敛性.

### 解答 10.1-2-1

部分和 $S_N=\sqrt{N+1}-1\to+\infty$. 由级数收敛的定义, 级数发散.

$\blacksquare$

## 10.1-2-2

讨论 $\sum_{n=1}^\infty\frac1{\left(2n-1\right)\left(2n+1\right)}$ 的收敛性.

### 解答 10.1-2-2

裂项: $\frac1{\left(2n-1\right)\left(2n+1\right)}=\frac12\left(\frac1{2n-1}-\frac1{2n+1}\right)$. 部分和 $S_N=\frac12\left(1-\frac1{2N+1}\right)\to\frac12$. 由级数收敛的定义, 级数收敛.

$\blacksquare$

## 10.1-2-3

讨论 $\sum_{n=1}^\infty\ln\frac{n}{n+5}$ 的收敛性.

### 解答 10.1-2-3

裂项相消后 $S_N=\ln\left(1\cdot2\cdot3\cdot4\cdot5\right)-\ln\left(\left(N+1\right)\cdots\left(N+5\right)\right)\to-\infty$. 由级数收敛的定义, 级数发散.

$\blacksquare$

## 10.1-2-7

讨论 $\sum_{n=1}^\infty\cos^2\frac\pi{}n$ 的收敛性.

### 解答 10.1-2-7

通项 $\cos^2\frac\pi{}n\to1\ne0$. 由**定理 1.1 (收敛级数的必要条件)**, 级数发散.

$\blacksquare$

## 10.1-2-8

讨论 $\sum_{n=1}^\infty\arctan\frac1{2n^2}$ 的收敛性.

### 解答 10.1-2-8

因 $0\le\arctan\frac1{2n^2}\le\frac1{2n^2}$, 且 $\sum\frac1{2n^2}$ 收敛, 故部分和单调递增且有上界. 由级数收敛的定义, 级数收敛.

$\blacksquare$

## 10.2-1-15

讨论 $\sum_{n=1}^\infty\frac{\left(n!\right)^2}{\left(2n\right)!}$ 的收敛性.

### 解答 10.2-1-15

$\frac{a_{n+1}}{a_n}=\frac{n+1}{2\left(2n+1\right)}\to\frac14<1$. 由**定理 2.6 (达朗贝尔判别法)**, 级数收敛.

$\blacksquare$

## 10.2-1-18

讨论 $\sum_{n=3}^\infty\frac1{n\left(\ln\ln{}n\right)^q}$ ($q>0$) 的收敛性.

### 解答 10.2-1-18

因 $\frac1{n\left(\ln\ln{}n\right)^q}>\frac1{n\ln{}n}$, 而 $\sum\frac1{n\ln{}n}$ 由**定理 2.9 (积分判别法)** 发散. 由**定理 2.2 (比较判别法)**, 原级数发散.

$\blacksquare$

## 10.2-2

用积分判别法讨论 $\sum_{n=3}^\infty\frac1{n\ln^pn\left(\ln\ln{}n\right)^q}$ ($p>0,q>0$) 的收敛性.

### 解答 10.2-2

令 $t=\ln{}x$, 由**定理 2.9 (积分判别法)**, 原级数与 $\int_{\ln3}^{+\infty}\frac{\mathrm{d}t}{t^p\left(\ln{}t\right)^q}$ 同敛散.

(i) $p>1$ 时收敛; (ii) $p<1$ 时发散; (iii) $p=1,q>1$ 时收敛; (iv) $p=1,q\le1$ 时发散.

$\blacksquare$
