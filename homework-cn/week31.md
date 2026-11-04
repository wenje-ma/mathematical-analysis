# week31

> **定理 1.1 (M 判别法)**
> 
> 若存在 $M_n> 0$, $M_n\to0$, 使 $\left|f_n\left(x\right)-f\left(x\right)\right|\le M_n$ 对一切 $x\in X$ 成立, 则 $\left\{f_n\right\}$ 在 $X$ 上一致收敛于 $f$.

> **定理 1.2 (极限函数的连续性)**
> 
> 若 $\left\{f_n\right\}$ 在区间 $X$ 上一致收敛于 $f$, 且每个 $f_n$ 连续, 则 $f$ 在 $X$ 上连续.

> **定理 2.2 (比较判别法)**
> 
> 设 $\sum a_n$ 与 $\sum b_n$ 为正项级数, 且存在 $N_0$ 使 $a_n\le b_n$ ($n\ge N_0$). 若 $\sum b_n$ 收敛, 则 $\sum a_n$ 收敛.

> **定理 2.3 (比较判别法的极限形式)**
> 
> 设 $\sum a_n$ 与 $\sum b_n$ 为正项级数, 且 $\lim_{n\to\infty}\frac{a_n}{b_n}=l$. 当 $0< l< +\infty$ 时两级数同敛散.

> **定理 3.2 (狄利克雷判别法)**
> 
> 设 $\left\{b_n\right\}$ 单调趋于零, 且 $\sum a_n$ 的部分和序列有界, 则 $\sum a_nb_n$ 收敛.

> **定理 3.3 (阿贝尔判别法)**
> 
> 设 $\left\{b_n\right\}$ 单调有界, 且 $\sum a_n$ 收敛, 则 $\sum a_nb_n$ 收敛.

> **定理 4.1 (无穷乘积与级数的关系)**
> 
> 设 $p_n> 0$, 则 $\prod p_n$ 收敛的充要条件是 $\sum\ln p_n$ 收敛, 且此时 $\prod p_n=\exp\left(\sum\ln p_n\right)$.

> **定理 4.2 (同号项无穷乘积)**
> 
> 设 $\alpha_n\ge0$ (或 $\alpha_n\le0$), 则 $\prod\left(1+\alpha_n\right)$ 收敛的充要条件是 $\sum\alpha_n$ 收敛.

> **定理 4.4 (绝对收敛)**
> 
> 设 $\alpha_n\ne-1$, 则 $\prod\left(1+\alpha_n\right)$ 绝对收敛的充要条件是 $\sum\left|\alpha_n\right|$ 收敛.

## 10.3-2

证明: $\sum_{n=1}^\infty\frac{\cos nx}{n^p}$ ($0< x< 2\pi$) 当 $p> 1$ 时绝对收敛, 当 $0< p\le1$ 时条件收敛.

### 解答 10.3-2

(1) $p> 1$ 时, $\left|\frac{\cos nx}{n^p}\right|\le\frac1{n^p}$, 由**定理 2.2 (比较判别法)** 及 $p$ 级数收敛, 原级数绝对收敛.

(2) $0< p\le1$ 时, 由 $\left|\cos nx\right|\ge\cos^2nx=\frac{1+\cos2nx}{2}$, 得 $\frac{\left|\cos nx\right|}{n^p}\ge\frac1{2n^p}+\frac{\cos2nx}{2n^p}$. 因 $\sum\frac1{n^p}$ 发散, 故原级数不绝对收敛. 又 $\sum\cos nx$ 部分和有界, $\frac1{n^p}$ 单调趋于零, 由**定理 3.2 (狄利克雷判别法)**, 原级数收敛. 故条件收敛. $\blacksquare$

## 10.3-4

证明狄利克雷级数 $\sum\frac{a_n}{n^x}$ 的收敛域为半无限区间.

### 解答 10.3-4

若 $\sum\frac{a_n}{n^{x_0}}$ 收敛且 $x> x_0$, 则 $\frac{a_n}{n^x}=\frac{a_n}{n^{x_0}}\cdot\frac1{n^{x-x_0}}$, 其中 $\frac1{n^{x-x_0}}$ 单调有界. 由**定理 3.3 (阿贝尔判别法)**, $\sum\frac{a_n}{n^x}$ 收敛. 发散情形同理反证. $\blacksquare$

## 10.3-5

设 $h_n=\sum_{k=1}^n\frac1k$, $S_n=\sum_{k=1}^n\frac{\left(-1\right)^{k-1}}k$. (1) 证明 $S_{2n}=h_{2n}-h_n$; (2) 利用 $h_n-\ln n\to\gamma$ 证明 $S_{2n}\to\ln2$; (3) 证明 $\sum\frac{\left(-1\right)^{n-1}}n=\ln2$.

### 解答 10.3-5

(1) 直接计算: $S_{2n}=h_{2n}-2\cdot\frac12h_n=h_{2n}-h_n$.

(2) $S_{2n}=h_{2n}-h_n=\ln\left(2n\right)+\gamma-\ln n-\gamma+o\left(1\right)=\ln2+o\left(1\right)$.

(3) $S_{2n-1}=S_{2n}+\frac1{2n}\to\ln2$. 偶数项与奇数项部分和均趋于 $\ln2$, 故 $\sum\frac{\left(-1\right)^{n-1}}n=\ln2$. $\blacksquare$

## 10.4-1-2

讨论 $\prod_{n=2}^\infty\sqrt{\frac{n^2+1}{n^2-1}}$ 的收敛性.

### 解答 10.4-1-2

令 $\alpha_n=\frac2{n^2-1}> 0$. 因 $\alpha_n\sim\frac2{n^2}$, 及**定理 2.3 (比较判别法的极限形式)**, $\sum\alpha_n$ 收敛. 由**定理 4.2 (同号项无穷乘积)**, 原无穷乘积收敛. $\blacksquare$

## 10.4-1-4

讨论 $\prod_{n=1}^\infty\left(1+\frac{x^n}{2^n}\right)$ 的收敛性.

### 解答 10.4-1-4

令 $\alpha_n=\left(\frac x2\right)^n$. 当 $\left|x\right|< 2$ 时, $\sum\left|\alpha_n\right|$ 收敛, 由**定理 4.4 (绝对收敛)**, 原乘积收敛. 当 $\left|x\right|\ge2$ 时, $1+\alpha_n$ 不趋于 $1$, 发散. $\blacksquare$

## 10.4-1-6

讨论 $\prod_{n=1}^\infty\cos\frac1n$ 的收敛性.

### 解答 10.4-1-6

由**定理 4.1 (无穷乘积与级数的关系)**, 考察 $\sum\ln\cos\frac1n$. 因 $\ln\cos\frac1n\sim-\frac1{2n^2}$, 及**定理 2.3 (比较判别法的极限形式)**, $\sum\ln\cos\frac1n$ 收敛. 故原乘积收敛. $\blacksquare$

## 10.4-1-8

讨论 $\prod_{n=1}^\infty\left(1+\frac1{\sqrt n}\right)$ 的收敛性.

### 解答 10.4-1-8

令 $\alpha_n=\frac1{\sqrt n}> 0$. 因 $\sum\frac1{\sqrt n}$ 发散, 由**定理 4.2 (同号项无穷乘积)**, 原乘积发散. $\blacksquare$

## 10.4-2

设 $0< \alpha_n< \frac\pi2$, $\sum\alpha_n^2$ 收敛, 证明 $\prod\cos\alpha_n$ 收敛.

### 解答 10.4-2

因 $\ln\cos\alpha_n\sim-\frac{\alpha_n^2}{2}$, 及**定理 2.3 (比较判别法的极限形式)**, $\sum\ln\cos\alpha_n$ 收敛. 由**定理 4.1 (无穷乘积与级数的关系)**, 原乘积收敛. $\blacksquare$

## 10.4-3

设 $\left|\alpha_n\right|< \frac\pi4$, $\sum\left|\alpha_n\right|$ 收敛, 证明 $\prod\tan\left(\frac\pi4+\alpha_n\right)$ 绝对收敛.

### 解答 10.4-3

因 $\left|\tan\left(\frac\pi4+\alpha_n\right)-1\right|\sim2\left|\alpha_n\right|$, 及**定理 2.3 (比较判别法的极限形式)**, $\sum\left|\tan\left(\frac\pi4+\alpha_n\right)-1\right|$ 收敛. 由**定理 4.4 (绝对收敛)**, 原乘积绝对收敛. $\blacksquare$

## 10.4-5

证明: 若 $\prod\left(1+\left|\alpha_n\right|\right)$ 收敛, 则 $\prod\left(1+\alpha_n\right)$ 收敛.

### 解答 10.4-5

由**定理 4.2 (同号项无穷乘积)**, $\prod\left(1+\left|\alpha_n\right|\right)$ 收敛蕴含 $\sum\left|\alpha_n\right|$ 收敛. 由**定理 4.4 (绝对收敛)**, $\prod\left(1+\alpha_n\right)$ 绝对收敛, 从而收敛. $\blacksquare$

## 11.1-1-1

讨论 $f_n\left(x\right)=\frac1{1+nx}$ 在 $\left(0,1\right)$ 上的一致收敛性.

### 解答 11.1-1-1

极限函数 $f\left(x\right)\equiv0$. 取 $x_n=\frac1n$, 则 $\left|f_n\left(x_n\right)\right|=\frac12\not\to0$. 由函数序列一致收敛的定义, 不一致收敛. $\blacksquare$

## 11.1-1-3

讨论 $f_n\left(x\right)=\frac{\sin\left(nx+n\right)}n$ 在 $\mathbb R$ 上的一致收敛性.

### 解答 11.1-1-3

极限函数 $f\left(x\right)\equiv0$. 又 $\left|f_n\left(x\right)\right|\le\frac1n=M_n$, $M_n\to0$. 由**定理 1.1 (M 判别法)**, 一致收敛. $\blacksquare$

## 11.1-1-5

讨论 $f_n\left(x\right)=nxe^{-nx^2}$ 在 $\left[0,1\right]$ 上的一致收敛性.

### 解答 11.1-1-5

极限函数 $f\left(x\right)\equiv0$. 取 $x_n=\frac1{\sqrt{2n}}$, 则 $\left|f_n\left(x_n\right)\right|=\sqrt{\frac n{2e}}\to+\infty$. 由函数序列一致收敛的定义, 不一致收敛. $\blacksquare$

## 11.1-2

设 $f_n$ 在 $\left(a,b\right)$ 内一致收敛于 $f$, 且 $\lim_{x\to x_0}f_n\left(x\right)$ 存在. 证明 $\lim_{x\to x_0}f\left(x\right)=\lim_{n\to\infty}\lim_{x\to x_0}f_n\left(x\right)$.

### 解答 11.1-2

记 $A_n=\lim_{x\to x_0}f_n\left(x\right)$. 由一致收敛性, $\left\{A_n\right\}$ 为柯西列, 设极限为 $A$. 再由三角不等式得 $\left|f\left(x\right)-A\right|< \varepsilon$. 故等式成立. $\blacksquare$
