# 作业 37

> **定义**（散度）设向量场 $\boldsymbol{F}=\left(P,Q,R\right)$, 其中 $P,Q,R$ 有一阶连续偏导数. 则

$$
\operatorname{div}\boldsymbol{F}=\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}.
$$

> **定义**（旋度）向量场 $\boldsymbol{F}=\left(P,Q,R\right)$ 的旋度为

$$
\operatorname{rot}\boldsymbol{F}=\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z},\ \frac{\partial P}{\partial z}-\frac{\partial R}{\partial x},\ \frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right).
$$

### 习题一

（习题 9.5-1）求下列向量场的散度 $\operatorname{div}\boldsymbol{F}$ 与旋度 $\operatorname{rot}\boldsymbol{F}$:
(1) $\boldsymbol{F}=\left(4x,-2xy,z\right)$;

(2) $\boldsymbol{F}=\left(5x^2,y^2,z^2\right)$.

### 解答 习题一

（1）$P=4x$, $Q=-2xy$, $R=z$. 由**定义**（散度）,

$$
\operatorname{div}\boldsymbol{F}=\frac{\partial\left(4x\right)}{\partial x}+\frac{\partial\left(-2xy\right)}{\partial y}+\frac{\partial z}{\partial z}=4-2x+1=5-2x.
$$

由**定义**（旋度）,

$$
\operatorname{rot}\boldsymbol{F}=\left(0-0,\ 0-0,\ -2y-0\right)=\left(0,0,-2y\right).
$$

（2）$P=5x^2$, $Q=y^2$, $R=z^2$.

$$
\operatorname{div}\boldsymbol{F}=10x+2y+2z,
$$

$$
\operatorname{rot}\boldsymbol{F}=\left(0-0,\ 0-0,\ 0-0\right)=\left(0,0,0\right).
$$

$\blacksquare$

### 习题二

（习题 9.5-2）证明 $\operatorname{div}\left(\Phi\boldsymbol{F}\right)=\Phi\operatorname{div}\boldsymbol{F}+\boldsymbol{F}\cdot\operatorname{grad}\Phi$.

### 解答 习题二

设 $\boldsymbol{F}=\left(P,Q,R\right)$, 则 $\Phi\boldsymbol{F}=\left(\Phi P,\Phi Q,\Phi R\right)$. 由**定义**（散度）,

$$
\begin{aligned}\operatorname{div}\left(\Phi\boldsymbol{F}\right)&=\frac{\partial\left(\Phi P\right)}{\partial x}+\frac{\partial\left(\Phi Q\right)}{\partial y}+\frac{\partial\left(\Phi R\right)}{\partial z}\\&=\left(\Phi\frac{\partial P}{\partial x}+P\frac{\partial\Phi}{\partial x}\right)+\left(\Phi\frac{\partial Q}{\partial y}+Q\frac{\partial\Phi}{\partial y}\right)+\left(\Phi\frac{\partial R}{\partial z}+R\frac{\partial\Phi}{\partial z}\right)\\&=\Phi\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)+\left(P\frac{\partial\Phi}{\partial x}+Q\frac{\partial\Phi}{\partial y}+R\frac{\partial\Phi}{\partial z}\right)\\&=\Phi\operatorname{div}\boldsymbol{F}+\boldsymbol{F}\cdot\operatorname{grad}\Phi.\end{aligned}
$$

$\blacksquare$

### 习题三

（习题 9.5-3）证明 $\operatorname{rot}\left(\Phi\boldsymbol{F}\right)=\Phi\operatorname{rot}\boldsymbol{F}+\operatorname{grad}\Phi\times\boldsymbol{F}$.

### 解答 习题三

设 $\boldsymbol{F}=\left(P,Q,R\right)$. 由**定义**（旋度）, $\operatorname{rot}\left(\Phi\boldsymbol{F}\right)$ 的第一个分量为

$$
\frac{\partial\left(\Phi R\right)}{\partial y}-\frac{\partial\left(\Phi Q\right)}{\partial z}=\Phi\frac{\partial R}{\partial y}+R\frac{\partial\Phi}{\partial y}-\Phi\frac{\partial Q}{\partial z}-Q\frac{\partial\Phi}{\partial z}=\Phi\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right)+\left(R\frac{\partial\Phi}{\partial y}-Q\frac{\partial\Phi}{\partial z}\right).
$$

而 $\operatorname{grad}\Phi\times\boldsymbol{F}=\left(\frac{\partial\Phi}{\partial y}R-\frac{\partial\Phi}{\partial z}Q,\ \frac{\partial\Phi}{\partial z}P-\frac{\partial\Phi}{\partial x}R,\ \frac{\partial\Phi}{\partial x}Q-\frac{\partial\Phi}{\partial y}P\right)$, 其第一个分量与上式第二项相同. 同理可验证第二、三分量, 故等式成立. $\blacksquare$

### 习题四

（习题 9.5-4）证明 $\operatorname{rot}\left(\operatorname{grad}\Phi\right)=0$.

### 解答 习题四

$\operatorname{grad}\Phi=\left(\frac{\partial\Phi}{\partial x},\frac{\partial\Phi}{\partial y},\frac{\partial\Phi}{\partial z}\right)$. 由**定义**（旋度）,

$$
\operatorname{rot}\left(\operatorname{grad}\Phi\right)=\left(\frac{\partial^2\Phi}{\partial z\partial y}-\frac{\partial^2\Phi}{\partial y\partial z},\ \frac{\partial^2\Phi}{\partial x\partial z}-\frac{\partial^2\Phi}{\partial z\partial x},\ \frac{\partial^2\Phi}{\partial y\partial x}-\frac{\partial^2\Phi}{\partial x\partial y}\right).
$$

由于 $\Phi$ 的二阶混合偏导数连续, 与求导次序无关, 故三个分量均为 $0$. $\blacksquare$

### 习题五

（习题 9.5-5）证明 $\operatorname{div}\left(\operatorname{rot}\boldsymbol{F}\right)=0$.

### 解答 习题五

设 $\boldsymbol{F}=\left(P,Q,R\right)$. 由**定义**（旋度）,

$$
\operatorname{rot}\boldsymbol{F}=\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z},\ \frac{\partial P}{\partial z}-\frac{\partial R}{\partial x},\ \frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right).
$$

由**定义**（散度）,

$$
\begin{aligned}\operatorname{div}\left(\operatorname{rot}\boldsymbol{F}\right)&=\frac{\partial}{\partial x}\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right)+\frac{\partial}{\partial y}\left(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}\right)+\frac{\partial}{\partial z}\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\\&=\frac{\partial^2R}{\partial x\partial y}-\frac{\partial^2Q}{\partial x\partial z}+\frac{\partial^2P}{\partial y\partial z}-\frac{\partial^2R}{\partial y\partial x}+\frac{\partial^2Q}{\partial z\partial x}-\frac{\partial^2P}{\partial z\partial y}=0,\end{aligned}
$$

最后一步用到二阶混合偏导数连续, 与求导次序无关. $\blacksquare$
