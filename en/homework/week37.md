# Assignment 37

> **Definition** (Divergence) Let $\boldsymbol{F}=\left(P,Q,R\right)$ be a vector field, where $P,Q,R$ have continuous first-order partial derivatives. Then

$$
\operatorname{div}\boldsymbol{F}=\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}.
$$

> **Definition** (Curl) The curl of a vector field $\boldsymbol{F}=\left(P,Q,R\right)$ is

$$
\operatorname{rot}\boldsymbol{F}=\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z},\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x},\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right).
$$

### Problem 1

(Problem 9.5-1) Find the divergence $\operatorname{div}\boldsymbol{F}$ and the curl $\operatorname{rot}\boldsymbol{F}$ of the following vector fields:
(1) $\boldsymbol{F}=\left(4x,-2xy,z\right)$;

(2) $\boldsymbol{F}=\left(5x^2,y^2,z^2\right)$.

### Solution to Problem 1

(1) $P=4x$, $Q=-2xy$, $R=z$. By **Definition** (Divergence),

$$
\operatorname{div}\boldsymbol{F}=\frac{\partial\left(4x\right)}{\partial x}+\frac{\partial\left(-2xy\right)}{\partial y}+\frac{\partial z}{\partial z}=4-2x+1=5-2x.
$$

By **Definition** (Curl),

$$
\operatorname{rot}\boldsymbol{F}=\left(0-0,0-0,-2y-0\right)=\left(0,0,-2y\right).
$$

(2) $P=5x^2$, $Q=y^2$, $R=z^2$.

$$
\operatorname{div}\boldsymbol{F}=10x+2y+2z,
$$

$$
\operatorname{rot}\boldsymbol{F}=\left(0-0,0-0,0-0\right)=\left(0,0,0\right).

$$

$\blacksquare$
### Problem 2

(Problem 9.5-2) Prove that

$$
\operatorname{div}\left(\Phi\boldsymbol{F}\right)=\Phi\operatorname{div}\boldsymbol{F}+\boldsymbol{F}\cdot\operatorname{grad}\Phi.
$$

### Solution to Problem 2

Let $\boldsymbol{F}=\left(P,Q,R\right)$. Then $\Phi\boldsymbol{F}=\left(\Phi P,\Phi Q,\Phi R\right)$. By **Definition** (Divergence),

$$
\operatorname{div}\left(\Phi\boldsymbol{F}\right)=\frac{\partial\left(\Phi P\right)}{\partial x}+\frac{\partial\left(\Phi Q\right)}{\partial y}+\frac{\partial\left(\Phi R\right)}{\partial z}=\left(\Phi\frac{\partial P}{\partial x}+P\frac{\partial\Phi}{\partial x}\right)+\left(\Phi\frac{\partial Q}{\partial y}+Q\frac{\partial\Phi}{\partial y}\right)+\left(\Phi\frac{\partial R}{\partial z}+R\frac{\partial\Phi}{\partial z}\right)=\Phi\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)+\left(P\frac{\partial\Phi}{\partial x}+Q\frac{\partial\Phi}{\partial y}+R\frac{\partial\Phi}{\partial z}\right)=\Phi\operatorname{div}\boldsymbol{F}+\boldsymbol{F}\cdot\operatorname{grad}\Phi.

$$

$\blacksquare$
### Problem 3

(Problem 9.5-3) Prove that

$$
\operatorname{rot}\left(\Phi\boldsymbol{F}\right)=\Phi\operatorname{rot}\boldsymbol{F}+\operatorname{grad}\Phi\times\boldsymbol{F}.
$$

### Solution to Problem 3

Let $\boldsymbol{F}=\left(P,Q,R\right)$. By **Definition** (Curl), the first component of $\operatorname{rot}\left(\Phi\boldsymbol{F}\right)$ is

$$
\frac{\partial\left(\Phi R\right)}{\partial y}-\frac{\partial\left(\Phi Q\right)}{\partial z}=\Phi\frac{\partial R}{\partial y}+R\frac{\partial\Phi}{\partial y}-\Phi\frac{\partial Q}{\partial z}-Q\frac{\partial\Phi}{\partial z}=\Phi\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right)+\left(R\frac{\partial\Phi}{\partial y}-Q\frac{\partial\Phi}{\partial z}\right).
$$

On the other hand,

$$
\operatorname{grad}\Phi\times\boldsymbol{F}=\left(\frac{\partial\Phi}{\partial y}R-\frac{\partial\Phi}{\partial z}Q,\frac{\partial\Phi}{\partial z}P-\frac{\partial\Phi}{\partial x}R,\frac{\partial\Phi}{\partial x}Q-\frac{\partial\Phi}{\partial y}P\right),
$$

whose first component equals the second term in the above expression. The second and third components are verified similarly, so the identity holds. $\blacksquare$

### Problem 4

(Problem 9.5-4) Prove that $\operatorname{rot}\left(\operatorname{grad}\Phi\right)=0$.

### Solution to Problem 4

$\operatorname{grad}\Phi=\left(\frac{\partial\Phi}{\partial x},\frac{\partial\Phi}{\partial y},\frac{\partial\Phi}{\partial z}\right)$. By **Definition** (Curl),

$$
\operatorname{rot}\left(\operatorname{grad}\Phi\right)=\left(\frac{\partial^2\Phi}{\partial z\partial y}-\frac{\partial^2\Phi}{\partial y\partial z},\frac{\partial^2\Phi}{\partial x\partial z}-\frac{\partial^2\Phi}{\partial z\partial x},\frac{\partial^2\Phi}{\partial y\partial x}-\frac{\partial^2\Phi}{\partial x\partial y}\right).
$$

Since the mixed second-order partial derivatives of $\Phi$ are continuous and hence independent of the order of differentiation, all three components are $0$. $\blacksquare$

### Problem 5

(Problem 9.5-5) Prove that $\operatorname{div}\left(\operatorname{rot}\boldsymbol{F}\right)=0$.

### Solution to Problem 5

Let $\boldsymbol{F}=\left(P,Q,R\right)$. By **Definition** (Curl),

$$
\operatorname{rot}\boldsymbol{F}=\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z},\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x},\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right).
$$

By **Definition** (Divergence),

$$
\operatorname{div}\left(\operatorname{rot}\boldsymbol{F}\right)=\frac{\partial}{\partial x}\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right)+\frac{\partial}{\partial y}\left(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}\right)+\frac{\partial}{\partial z}\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)=\frac{\partial^2R}{\partial x\partial y}-\frac{\partial^2Q}{\partial x\partial z}+\frac{\partial^2P}{\partial y\partial z}-\frac{\partial^2R}{\partial y\partial x}+\frac{\partial^2Q}{\partial z\partial x}-\frac{\partial^2P}{\partial z\partial y}=0,
$$

where the last step uses the continuity of the mixed second-order partial derivatives, which makes them independent of the order of differentiation. $\blacksquare$
