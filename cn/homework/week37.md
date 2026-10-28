# week37

> **基础知识: 散度的定义**<br>设向量场 $\boldsymbol F=\left(P,Q,R\right)$, 则 $\operatorname{div}\boldsymbol F=\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}$.

> **基础知识: 旋度的定义**<br>$\operatorname{rot}\boldsymbol F=\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z},\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x},\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)$.

---

## 9.5-1

求下列向量场的散度与旋度:

(1) $\boldsymbol F=\left(4x,-2xy,z\right)$;

(2) $\boldsymbol F=\left(5x^2,y^2,z^2\right)$.

### 解答 9.5-1

(1) 由**基础知识: 散度的定义**, $\operatorname{div}\boldsymbol F=5-2x$. 由**基础知识: 旋度的定义**, $\operatorname{rot}\boldsymbol F=\left(0,0,-2y\right)$.

(2) $\operatorname{div}\boldsymbol F=10x+2y+2z$, $\operatorname{rot}\boldsymbol F=\left(0,0,0\right)$. $\blacksquare$

---

## 9.5-2

证明: $\operatorname{div}\left(\Phi\boldsymbol F\right)=\Phi\operatorname{div}\boldsymbol F+\boldsymbol F\cdot\operatorname{grad}\Phi$.

### 解答 9.5-2

由**基础知识: 散度的定义**, 展开 $\frac{\partial\left(\Phi P\right)}{\partial x}+\frac{\partial\left(\Phi Q\right)}{\partial y}+\frac{\partial\left(\Phi R\right)}{\partial z}$, 合并同类项即得. $\blacksquare$

---

## 9.5-3

证明: $\operatorname{rot}\left(\Phi\boldsymbol F\right)=\Phi\operatorname{rot}\boldsymbol F+\operatorname{grad}\Phi\times\boldsymbol F$.

### 解答 9.5-3

由**基础知识: 旋度的定义**, 计算第一个分量:

$$
\frac{\partial\left(\Phi R\right)}{\partial y}-\frac{\partial\left(\Phi Q\right)}{\partial z}=\Phi\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right)+\left(R\frac{\partial\Phi}{\partial y}-Q\frac{\partial\Phi}{\partial z}\right).
$$

第二项即为 $\operatorname{grad}\Phi\times\boldsymbol F$ 的第一个分量. 同理验证其余分量. $\blacksquare$

---

## 9.5-4

证明: $\operatorname{rot}\left(\operatorname{grad}\Phi\right)=0$.

### 解答 9.5-4

由**基础知识: 旋度的定义**, $\operatorname{rot}\left(\operatorname{grad}\Phi\right)$ 的每个分量均为二阶混合偏导数之差. 因二阶混合偏导数连续, 与求导次序无关, 故各分量均为 $0$. $\blacksquare$

---

## 9.5-5

证明: $\operatorname{div}\left(\operatorname{rot}\boldsymbol F\right)=0$.

### 解答 9.5-5

由**基础知识: 散度的定义** 与**基础知识: 旋度的定义**, 展开后各项两两抵消. 因二阶混合偏导数连续, 与求导次序无关, 故结果为 $0$. $\blacksquare$
