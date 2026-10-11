# 作业 48

> **定理 3.3**（积分号下求导）设 $f\left(x,y\right)$ 与 $f_y\left(x,y\right)$ 在 $\left[a,b\right]\times\left[c,d\right]$ 上连续，则函数 $I\left(y\right)=\displaystyle\int_a^b f\left(x,y\right)\,\mathrm{d}x$ 在 $\left[c,d\right]$ 上可导，且
> $$I'\left(y\right)=\int_a^b f_y\left(x,y\right)\,\mathrm{d}x,\  \forall\,y\in\left[c,d\right].$$
> 当积分限也依赖于 $y$ 时，即 $I\left(y\right)=\displaystyle\int_{a\left(y\right)}^{b\left(y\right)}f\left(x,y\right)\,\mathrm{d}x$，再由牛顿–莱布尼茨公式补上边界项：
> $$I'\left(y\right)=f\left(b\left(y\right),y\right)b'\left(y\right)-f\left(a\left(y\right),y\right)a'\left(y\right)+\int_{a\left(y\right)}^{b\left(y\right)}f_y\left(x,y\right)\,\mathrm{d}x.$$

### 习题一

（习题 12.3-2-5）求函数 $\displaystyle I\left(y\right)=\int_{\sin y}^{\cos y}e^{y\sqrt{1-x^2}}\,\mathrm{d}x$（$y\in\left[0,\dfrac{\pi}{2}\right]$）的导数.

### 解答 习题一

被积函数 $f\left(x,y\right)=e^{y\sqrt{1-x^2}}$ 及其对 $y$ 的偏导数 $f_y=\sqrt{1-x^2}\,e^{y\sqrt{1-x^2}}$ 均连续，上下限 $a\left(y\right)=\sin y$，$b\left(y\right)=\cos y$ 均可导. 由**定理 3.3**（积分号下求导），

$$
I'\left(y\right)=f\left(\cos y,y\right)\cdot\left(-\sin y\right)-f\left(\sin y,y\right)\cdot\cos y+\int_{\sin y}^{\cos y}\sqrt{1-x^2}\,e^{y\sqrt{1-x^2}}\,\mathrm{d}x.
$$

当 $y\in\left[0,\pi/2\right]$ 时 $\sqrt{1-\cos^2 y}=\sin y$，$\sqrt{1-\sin^2 y}=\cos y$，代入得

$$
I'\left(y\right)=\int_{\sin y}^{\cos y}\sqrt{1-x^2}\,e^{y\sqrt{1-x^2}}\,\mathrm{d}x-e^{y\sin y}\sin y-e^{y\cos y}\cos y.
$$

$\blacksquare$

### 习题二

（习题 12.3-2-6）求函数 $\displaystyle I\left(y\right)=\int_0^{x/y}y\sin\left(xy\right)\,\mathrm{d}x$（$y>0$，$x$ 为固定常数）的导数.

### 解答 习题二

被积函数 $f\left(x,y\right)=y\sin\left(xy\right)$，$f_y=\sin\left(xy\right)+xy\cos\left(xy\right)$，上限 $a\left(y\right)=x/y$，$a'\left(y\right)=-x/y^2$. 由**定理 3.3**（积分号下求导），

$$
I'\left(y\right)=y\sin\!\left(y\cdot\frac{x}{y}\right)\!\left(-\frac{x}{y^2}\right)+\int_0^{x/y}\bigl[\sin\left(xy\right)+xy\cos\left(xy\right)\bigr]\,\mathrm{d}x.
$$

注意到 $\dfrac{\mathrm{d}}{\mathrm{d}x}\bigl[x\sin\left(xy\right)\bigr]=\sin\left(xy\right)+xy\cos\left(xy\right)$，故

$$
\int_0^{x/y}\bigl[\sin\left(xy\right)+xy\cos\left(xy\right)\bigr]\,\mathrm{d}x=\bigl[x\sin\left(xy\right)\bigr]_0^{x/y}=\frac{x}{y}\sin x.
$$

而边界项为 $-\dfrac{x}{y}\sin x$，两者相消，故

$$
I'\left(y\right)=-\frac{x}{y}\sin x+\frac{x}{y}\sin x=0.
$$

$\blacksquare$

### 习题三

（习题 12.3-2-7）求函数 $\displaystyle I\left(y\right)=\int_0^{y^2}\sin\left(x^2+y^2\right)\,\mathrm{d}x$ 的导数.

### 解答 习题三

被积函数 $f\left(x,y\right)=\sin\left(x^2+y^2\right)$，$f_y=2y\cos\left(x^2+y^2\right)$，上限 $b\left(y\right)=y^2$，$b'\left(y\right)=2y$. 由**定理 3.3**（积分号下求导），

$$
I'\left(y\right)=\sin\bigl(\left(y^2\right)^2+y^2\bigr)\cdot 2y+\int_0^{y^2}2y\cos\left(x^2+y^2\right)\,\mathrm{d}x,
$$

即

$$
I'\left(y\right)=\int_0^{y^2}2y\cos\left(x^2+y^2\right)\,\mathrm{d}x+2y\sin\left(y^4+y^2\right).
$$

$\blacksquare$

### 习题四

（习题 12.3-2-8）求函数 $\displaystyle I\left(y\right)=\int_0^y\frac{\ln\left(1+xy\right)}{x}\,\mathrm{d}x$（$y>0$）的导数.

### 解答 习题四

被积函数 $f\left(x,y\right)=\dfrac{\ln\left(1+xy\right)}{x}$，$f_y=\dfrac{1}{1+xy}$，上限 $b\left(y\right)=y$，$b'\left(y\right)=1$. 由**定理 3.3**（积分号下求导），

$$
I'\left(y\right)=\frac{\ln\left(1+y^2\right)}{y}\cdot 1+\int_0^y\frac{\mathrm{d}x}{1+xy},
$$

即

$$
I'\left(y\right)=\frac{\ln\left(1+y^2\right)}{y}+\int_0^y\frac{\mathrm{d}x}{1+xy}.
$$

$\blacksquare$

### 习题五

（习题 12.3-4-1）利用积分号下求导的方法计算定积分 $\displaystyle I\left(r\right)=\int_0^\pi\ln\left(1-2r\cos x+r^2\right)\,\mathrm{d}x$（$\left|r\right|<1$）.

### 解答 习题五

对任意 $r\in\left(-1,1\right)$，被积函数及其对 $r$ 的偏导数在 $\left[0,\pi\right]\times\left(-1,1\right)$ 上连续，由**定理 3.3**（积分号下求导），

$$
I'\left(r\right)=\int_0^\pi\frac{-2\cos x+2r}{1-2r\cos x+r^2}\,\mathrm{d}x.
$$

记 $D=1-2r\cos x+r^2$，则

$$
\frac{2r-2\cos x}{D}=\frac1r-\frac{1-r^2}{rD},
$$

两端乘以 $r$ 即可验证. 于是

$$
I'\left(r\right)=\frac{\pi}{r}-\frac{1-r^2}{r}\int_0^\pi\frac{\mathrm{d}x}{1-2r\cos x+r^2}.
$$

作代换 $t=\tan\dfrac{x}{2}$，可得标准积分

$$
\int_0^\pi\frac{\mathrm{d}x}{1-2r\cos x+r^2}=\frac{\pi}{1-r^2}\ \left(\left|r\right|<1\right).
$$

代入得

$$
I'\left(r\right)=\frac{\pi}{r}-\frac{1-r^2}{r}\cdot\frac{\pi}{1-r^2}=0.
$$

故 $I\left(r\right)$ 为常数. 又 $I\left(0\right)=\int_0^\pi\ln1\,\mathrm{d}x=0$，所以

$$
I\left(r\right)=0\ \left(\left|r\right|<1\right).
$$

$\blacksquare$

### 习题六

（习题 12.3-6）设 $\displaystyle I\left(\alpha\right)=\int_0^{2\pi}\ln\left(1-\alpha\cos\theta\right)\,\mathrm{d}\theta$（$\left|\alpha\right|<1$）. 证明 $\displaystyle I'\left(\alpha\right)=\frac{2\pi\bigl(\sqrt{1-\alpha^2}-1\bigr)}{\alpha\sqrt{1-\alpha^2}}$，并由此推出 $\displaystyle I\left(\alpha\right)=2\pi\ln\frac{1+\sqrt{1-\alpha^2}}{2}$.

### 解答 习题六

由**定理 3.3**（积分号下求导），

$$
I'\left(\alpha\right)=\int_0^{2\pi}\frac{-\cos\theta}{1-\alpha\cos\theta}\,\mathrm{d}\theta.
$$

将被积函数分解：

$$
\frac{-\cos\theta}{1-\alpha\cos\theta}=\frac1\alpha-\frac{1}{\alpha\left(1-\alpha\cos\theta\right)}.
$$

作代换 $t=\tan\dfrac{\theta}{2}$，可得标准积分

$$
\int_0^{2\pi}\frac{\mathrm{d}\theta}{1-\alpha\cos\theta}=\frac{2\pi}{\sqrt{1-\alpha^2}}\ \left(\left|\alpha\right|<1\right).
$$

于是

$$
I'\left(\alpha\right)=\frac{2\pi}{\alpha}-\frac{1}{\alpha}\cdot\frac{2\pi}{\sqrt{1-\alpha^2}}
=\frac{2\pi}{\alpha}\left(1-\frac1{\sqrt{1-\alpha^2}}\right)
=\frac{2\pi\bigl(\sqrt{1-\alpha^2}-1\bigr)}{\alpha\sqrt{1-\alpha^2}}.
$$

现对 $\alpha$ 积分. 注意到

$$
\frac{\mathrm{d}}{\mathrm{d}\alpha}\ln\frac{1+\sqrt{1-\alpha^2}}{2}
=\frac{1}{1+\sqrt{1-\alpha^2}}\cdot\frac{-\alpha}{\sqrt{1-\alpha^2}}
=\frac{\sqrt{1-\alpha^2}-1}{\alpha\sqrt{1-\alpha^2}},
$$

（末步有理化：$\dfrac{1}{1+\sqrt{1-\alpha^2}}=\dfrac{1-\sqrt{1-\alpha^2}}{\alpha^2}$），故

$$
I\left(\alpha\right)=2\pi\ln\frac{1+\sqrt{1-\alpha^2}}{2}+C.
$$

又 $I\left(0\right)=\int_0^{2\pi}\ln1\,\mathrm{d}\theta=0$，而右端在 $\alpha=0$ 时为 $2\pi\ln1+C=C$，故 $C=0$. 因此

$$
I\left(\alpha\right)=2\pi\ln\frac{1+\sqrt{1-\alpha^2}}{2}.
$$

$\blacksquare$
