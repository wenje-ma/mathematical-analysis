# week52

> **基础知识: 内积与范数的定义**<br>在 $R\left[-\pi,\pi\right]$ 中定义内积 $\left\langle f,g\right\rangle=\frac1\pi\int_{-\pi}^\pi f\left(x\right)g\left(x\right)\mathrm dx$, 范数 $\left|f\right|=\sqrt{\left\langle f,f\right\rangle}$.

> **命题 (三角函数系的正交性)**<br>三角函数系 $1,\cos x,\sin x,\cos2x,\sin2x,\cdots$ 在 $\left[-\pi,\pi\right]$ 上两两正交, 且 $\int_{-\pi}^\pi1\,\mathrm dx=2\pi$, $\int_{-\pi}^\pi\cos^2nx\,\mathrm dx=\int_{-\pi}^\pi\sin^2nx\,\mathrm dx=\pi$.

---

## 13.1-1

证明内积的对称性与线性性.

### 解答 13.1-1

由**基础知识: 内积与范数的定义** 及积分的线性性, $\left\langle f,g\right\rangle=\left\langle g,f\right\rangle$, $\left\langle\lambda f+\mu g,h\right\rangle=\lambda\left\langle f,h\right\rangle+\mu\left\langle g,h\right\rangle$. $\blacksquare$

---

## 13.1-2

证明柯西-施瓦茨不等式: $\left|\left\langle f,g\right\rangle\right|\le\left|f\right|\cdot\left|g\right|$.

### 解答 13.1-2

对任意 $\lambda$, $\left|f-\lambda g\right|^2\ge0$, 展开得关于 $\lambda$ 的二次三项式恒非负, 判别式不大于 $0$, 即得. $\blacksquare$

---

## 13.1-3

证明等号成立当且仅当 $f,g$ 线性相关.

### 解答 13.1-3

$(\Leftarrow)$ 若 $g=\lambda f$, 直接验证. $(\Rightarrow)$ 若等号成立, 判别式为 $0$, 存在 $\lambda_0$ 使 $\left|f-\lambda_0g\right|^2=0$. 由连续性, $f\equiv\lambda_0g$. $\blacksquare$

---

## 13.1-7

证明 $c_1+c_2\cos x+c_3\sin x\equiv0$ 蕴含 $c_1=c_2=c_3=0$, 并推广到任意有穷个元素线性无关.

### 解答 13.1-7

两端分别乘以 $1,\cos x,\sin x$ 并积分. 由**命题 (三角函数系的正交性)**, 交叉项为零, 得 $2\pi c_1=0$, $\pi c_2=0$, $\pi c_3=0$. 推广同理. $\blacksquare$
