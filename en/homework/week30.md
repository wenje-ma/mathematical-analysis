# Assignment 30

> **Theorem 3.1** (Change of Variables Formula for Double Integrals) Let $z=f\left(x,y\right)$ be continuous on a bounded closed region $D$ that is rectifiable. Let the transformation
> $$
> F:\left(u,v\right)\mapsto\left(x\left(u,v\right),y\left(u,v\right)\right)
> $$
> be a one-to-one mapping from a bounded closed region $G$ onto $D$, let $x\left(u,v\right),y\left(u,v\right)$ have continuous first-order partial derivatives on $G$, and let the Jacobian determinant $J\left(u,v\right)=\frac{\partial\left(x,y\right)}{\partial\left(u,v\right)}\ne0$. Then

$$
\iint_D f\left(x,y\right)\,\mathrm{d}x\mathrm{d}y=\iint_G f\left(x\left(u,v\right),y\left(u,v\right)\right)\left| J\left(u,v\right)\right|\,\mathrm{d}u\mathrm{d}v.
$$

In particular, the area of the region $D$ is

$$
m\left(D\right)=\iint_G\left| J\left(u,v\right)\right|\,\mathrm{d}u\mathrm{d}v.
$$

### Problem 1

(Problem 8.3-1) Using an appropriate coordinate transformation, evaluate $\displaystyle\iint_D\left(\sqrt{\frac yx}+\sqrt{xy}\right)\mathrm{d}x\mathrm{d}y$, where $D$ is the region bounded by the curves $xy=1$, $xy=9$, $y=x$, and $y=4x$.

### Solution to Problem 1

Make the change of variables $u=xy$, $v=\frac yx$; then $D$ becomes

$$
G=\left\{\left(u,v\right):1\le u\le9,1\le v\le4\right\}.
$$

The inverse transformation is $x=\sqrt{u/v}$, $y=\sqrt{uv}$. The Jacobian determinant

$$
\frac{\partial\left(u,v\right)}{\partial\left(x,y\right)}=\begin{vmatrix}y&x\\-y/x^2&1/x\end{vmatrix}=\frac{2y}{x}=2v,
$$

hence $\left| J\right|=\left|\frac{\partial\left(x,y\right)}{\partial\left(u,v\right)}\right|=\frac1{2v}$. The integrand

$$
\sqrt{y/x}+\sqrt{xy}=\sqrt v+\sqrt u.
$$

By **Theorem 3.1**,

$$
\iint_D\left(\sqrt{\frac yx}+\sqrt{xy}\right)\mathrm{d}x\mathrm{d}y=\int_1^9\mathrm{d}u\int_1^4\left(\sqrt v+\sqrt u\right)\frac1{2v}\,\mathrm{d}v=\frac12\int_1^9\left[2\sqrt v+\sqrt u\ln v\right]_1^4\mathrm{d}u=\frac12\int_1^9\left(2+\sqrt u\ln4\right)\,\mathrm{d}u=\frac12\left[2u+\frac23u^{3/2}\ln4\right]_1^9=8+\frac{26}{3}\ln4=8+\frac{52}{3}\ln2.

$$

$\blacksquare$
### Problem 2

(Problem 8.3-4) Evaluate $\displaystyle\iint_D\left(x+y\right)\mathrm{d}x\mathrm{d}y$, where $D$ is the region bounded by the curves $y=4x^2$, $y=9x^2$, $x=4y^2$, and $x=9y^2$.

### Solution to Problem 2

Make the change of variables $u=\frac y{x^2}$, $v=\frac x{y^2}$; then $D$ becomes

$$
G=\left\{\left(u,v\right):4\le u\le9,4\le v\le9\right\}.
$$
From

$$
y=ux^2=u\left(vy^2\right)^2=uv^2y^4
$$

we get $y^3=\frac1{uv^2}$, i.e. $y=u^{-1/3}v^{-2/3}$; similarly $x=u^{-2/3}v^{-1/3}$. The Jacobian determinant

$$
J=\frac{\partial\left(x,y\right)}{\partial\left(u,v\right)}=
\begin{vmatrix}
-\frac23u^{-5/3}v^{-1/3}&-\frac13u^{-2/3}v^{-4/3}\\
-\frac13u^{-4/3}v^{-2/3}&-\frac23u^{-1/3}v^{-5/3}
\end{vmatrix}
=\frac1{3u^2v^2}.
$$

By **Theorem 3.1**,

$$
\iint_D\left(x+y\right)\mathrm{d}x\mathrm{d}y=\int_4^9\!\!\int_4^9\left(u^{-2/3}v^{-1/3}+u^{-1/3}v^{-2/3}\right)\frac1{3u^2v^2}\,\mathrm{d}u\mathrm{d}v=\frac13\left(\int_4^9u^{-8/3}\mathrm{d}u\right)\left(\int_4^9v^{-7/3}\mathrm{d}v\right)+\frac13\left(\int_4^9u^{-7/3}\mathrm{d}u\right)\left(\int_4^9v^{-8/3}\mathrm{d}v\right).
$$

The two terms are symmetric and combine to

$$
\iint_D\left(x+y\right)\mathrm{d}x\mathrm{d}y=\frac23\left[-\frac35u^{-5/3}\right]_4^9\left[-\frac34v^{-4/3}\right]_4^9=\frac3{10}\left(9^{-5/3}-4^{-5/3}\right)\left(9^{-4/3}-4^{-4/3}\right).

$$

$\blacksquare$
### Problem 3

(Problem 8.3-6) Find the area of the region $D$ bounded by the curve $\left(\frac{x^2}{a^2}+\frac{y^2}{b^2}\right)^2=\frac{xy}{c^2}$ ($a> 0,b> 0,c> 0$).

### Solution to Problem 3

Make the generalized polar coordinate transformation $x=ar\cos\theta$, $y=br\sin\theta$; the Jacobian determinant is $\left| J\right|=abr$. Substituting into the curve equation:

$$
r^4=\frac{\left(ar\cos\theta\right)\left(br\sin\theta\right)}{c^2}=\frac{abr^2\sin\theta\cos\theta}{c^2},
$$

i.e. $r^2=\frac{ab\sin2\theta}{2c^2}$. Since $r^2\ge0$, we have $\sin2\theta\ge0$, i.e. $\theta\in\left[0,\pi/2\right]\cup\left[\pi,3\pi/2\right]$. The two parts are symmetric about the origin, so the area is

$$
m\left(D\right)=2\int_0^{\pi/2}\mathrm{d}\theta\int_0^{\sqrt{ab\sin2\theta/\left(2c^2\right)}}abr\,\mathrm{d}r=2\int_0^{\pi/2}ab\cdot\frac12\cdot\frac{ab\sin2\theta}{2c^2}\,\mathrm{d}\theta=\frac{a^2b^2}{2c^2}\int_0^{\pi/2}\sin2\theta\,\mathrm{d}\theta=\frac{a^2b^2}{2c^2}.

$$

$\blacksquare$