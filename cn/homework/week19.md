# 作业 19

> **定理 2.1**（第一换元法则）设 $F'\left(u\right)=f\left(u\right)$, 且 $u=\varphi\left(x\right)$ 可导, 则
> $$
> \int f\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm{d}x=F\left(\varphi\left(x\right)\right)+C.
> $$
> **定理 2.2**（第二换元法则）设 $x=\varphi\left(t\right)$ 可导且有反函数, 又设
> $$
> \displaystyle\int f\left(\varphi\left(t\right)\right)\varphi'\left(t\right)\,\mathrm{d}t=G\left(t\right)+C,
> $$
> 则
> $$
> \int f\left(x\right)\,\mathrm{d}x=G\left(\varphi^{-1}\left(x\right)\right)+C.
> $$
### 习题一

（习题 4.2-1-2）求不定积分 $\displaystyle\int\sqrt{2x+3}\,\mathrm{d}x$.

### 解答 习题一

令 $u=2x+3$, 则 $\mathrm{d}u=2\mathrm{d}x$, 即 $\mathrm{d}x=\frac12\mathrm{d}u$. 由**定理 2.1**（第一换元法则）, 
$$
\int\sqrt{2x+3}\,\mathrm{d}x=\frac12\int u^{1/2}\,\mathrm{d}u=\frac12\cdot\frac23u^{3/2}+C=\frac13\left(2x+3\right)^{3/2}+C.
$$

$\blacksquare$
### 习题二

（习题 4.2-1-4）求不定积分 $\displaystyle\int\frac{\mathrm{d}x}{\left(x-1\right)^5}$.

### 解答 习题二

令 $u=x-1$, 则 $\mathrm{d}u=\mathrm{d}x$. 由**定理 2.1**（第一换元法则）, 
$$
\int\frac{\mathrm{d}x}{\left(x-1\right)^5}=\int u^{-5}\,\mathrm{d}u=\frac{u^{-4}}{-4}+C=-\frac{1}{4\left(x-1\right)^4}+C.
$$

$\blacksquare$
### 习题三

（习题 4.2-1-6）求不定积分 $\displaystyle\int\mathrm{sh}\,x\,\mathrm{d}x$.

### 解答 习题三

由 $\left(\mathrm{ch}\,x\right)'=\mathrm{sh}\,x$, 及不定积分的定义, 
$$
\int\mathrm{sh}\,x\,\mathrm{d}x=\mathrm{ch}\,x+C.
$$

$\blacksquare$
### 习题四

（习题 4.2-1-8）求不定积分 $\displaystyle\int\frac{\mathrm{d}x}{a^2+b^2x^2}$($a> 0,b> 0$).

### 解答 习题四

变形被积函数: 
$$
\frac{1}{a^2+b^2x^2}=\frac{1}{a^2}\cdot\frac{1}{1+\left(\frac{bx}{a}\right)^2}.
$$

令 $u=\frac{bx}{a}$, 则 $\mathrm{d}u=\frac{b}{a}\mathrm{d}x$, 即 $\mathrm{d}x=\frac{a}{b}\mathrm{d}u$. 由**定理 2.1**（第一换元法则）, 
$$
\int\frac{\mathrm{d}x}{a^2+b^2x^2}=\frac{1}{a^2}\cdot\frac{a}{b}\int\frac{\mathrm{d}u}{1+u^2}=\frac{1}{ab}\arctan u+C=\frac{1}{ab}\arctan\frac{bx}{a}+C.
$$

$\blacksquare$
### 习题五

（习题 4.2-1-10）求不定积分 $\displaystyle\int\frac{\mathrm{d}x}{\sin x+\cos x}$.

### 解答 习题五

利用三角恒等式: 
$$
\sin x+\cos x=\sqrt2\sin\left(x+\frac{\pi}{4}\right).
$$

故
$$
\int\frac{\mathrm{d}x}{\sin x+\cos x}=\frac{1}{\sqrt2}\int\frac{\mathrm{d}x}{\sin\left(x+\frac{\pi}{4}\right)}.
$$

令 $u=x+\frac{\pi}{4}$, 则 $\mathrm{d}u=\mathrm{d}x$. 由**定理 2.1**（第一换元法则）, 
$$
\int\frac{\mathrm{d}u}{\sin u}=\int\csc u\,\mathrm{d}u=\ln\left|\csc u-\cot u\right|+C.
$$

因此
$$
\int\frac{\mathrm{d}x}{\sin x+\cos x}=\frac{1}{\sqrt2}\ln\left|\csc\left(x+\frac{\pi}{4}\right)-\cot\left(x+\frac{\pi}{4}\right)\right|+C.
$$

$\blacksquare$
### 习题六

（习题 4.2-2-1）求不定积分 $\displaystyle\int\sqrt{a^2-x^2}\,\mathrm{d}x$($a> 0$).

### 解答 习题六

令 $x=a\sin t$($-\frac{\pi}{2}\le t\le\frac{\pi}{2}$), 则 $\mathrm{d}x=a\cos t\,\mathrm{d}t$, 且 $\sqrt{a^2-x^2}=a\cos t$. 由**定理 2.2**（第二换元法则）, 
$$
\int\sqrt{a^2-x^2}\,\mathrm{d}x=\int a\cos t\cdot a\cos t\,\mathrm{d}t=a^2\int\cos^2t\,\mathrm{d}t.
$$

利用 $\cos^2t=\frac{1+\cos2t}{2}$, 
$$
a^2\int\cos^2t\,\mathrm{d}t=\frac{a^2}{2}\left(t+\frac{\sin2t}{2}\right)+C=\frac{a^2}{2}\left(t+\sin t\cos t\right)+C.
$$

代回 $t=\arcsin\frac{x}{a}$, $\sin t=\frac{x}{a}$, $\cos t=\frac{\sqrt{a^2-x^2}}{a}$, 得
$$
\int\sqrt{a^2-x^2}\,\mathrm{d}x=\frac{a^2}{2}\arcsin\frac{x}{a}+\frac{x}{2}\sqrt{a^2-x^2}+C.
$$

$\blacksquare$
### 习题七

（习题 4.2-2-3）求不定积分 $\displaystyle\int\frac{\mathrm{d}x}{\sqrt{x^2+a^2}}$($a> 0$).

### 解答 习题七

令 $x=a\tan t$($-\frac{\pi}{2}< t< \frac{\pi}{2}$), 则 $\mathrm{d}x=a\sec^2t\,\mathrm{d}t$, 且 $\sqrt{x^2+a^2}=a\sec t$. 由**定理 2.2**（第二换元法则）, 
$$
\int\frac{\mathrm{d}x}{\sqrt{x^2+a^2}}=\int\frac{a\sec^2t}{a\sec t}\,\mathrm{d}t=\int\sec t\,\mathrm{d}t=\ln\left|\sec t+\tan t\right|+C.
$$

代回 $\tan t=\frac{x}{a}$, $\sec t=\frac{\sqrt{x^2+a^2}}{a}$, 得
$$
\int\frac{\mathrm{d}x}{\sqrt{x^2+a^2}}=\ln\left|\frac{x+\sqrt{x^2+a^2}}{a}\right|+C=\ln\left(x+\sqrt{x^2+a^2}\right)+C'.
$$

$\blacksquare$
### 习题八

（习题 4.2-2-5）求不定积分 $\displaystyle\int\sqrt{x^2-a^2}\,\mathrm{d}x$($a> 0$).

### 解答 习题八

令 $x=a\sec t$($0< t< \frac{\pi}{2}$), 则 $\mathrm{d}x=a\sec t\tan t\,\mathrm{d}t$, 且 $\sqrt{x^2-a^2}=a\tan t$. 由**定理 2.2**（第二换元法则）, 
$$
\int\sqrt{x^2-a^2}\,\mathrm{d}x=\int a\tan t\cdot a\sec t\tan t\,\mathrm{d}t=a^2\int\tan^2t\sec t\,\mathrm{d}t.
$$

利用 $\tan^2t=\sec^2t-1$, 
$$
a^2\int\left(\sec^3t-\sec t\right)\,\mathrm{d}t.
$$

由分部积分可得

$$
\displaystyle\int\sec^3t\,\mathrm{d}t=\frac12\left(\sec t\tan t+\ln\left|\sec t+\tan t\right|\right)+C.
$$

故
$$
\int\sqrt{x^2-a^2}\,\mathrm{d}x=\frac{x}{2}\sqrt{x^2-a^2}-\frac{a^2}{2}\ln\left|x+\sqrt{x^2-a^2}\right|+C.
$$

$\blacksquare$
### 习题九

（习题 4.2-2-7）求不定积分 $\displaystyle\int\frac{\mathrm{d}x}{x\sqrt{a^2-x^2}}$($a> 0$).

### 解答 习题九

令 $x=a\sin t$, 则 $\mathrm{d}x=a\cos t\,\mathrm{d}t$, $\sqrt{a^2-x^2}=a\cos t$. 由**定理 2.2**（第二换元法则）, 
$$
\int\frac{\mathrm{d}x}{x\sqrt{a^2-x^2}}=\int\frac{a\cos t\,\mathrm{d}t}{a\sin t\cdot a\cos t}=\frac1a\int\frac{\mathrm{d}t}{\sin t}=\frac1a\ln\left|\csc t-\cot t\right|+C.
$$

代回 $\csc t=\frac{a}{x}$, $\cot t=\frac{\sqrt{a^2-x^2}}{x}$, 得
$$
\int\frac{\mathrm{d}x}{x\sqrt{a^2-x^2}}=\frac1a\ln\left|\frac{a-\sqrt{a^2-x^2}}{x}\right|+C.
$$

$\blacksquare$
### 习题十

（习题 4.2-2-9）求不定积分 $\displaystyle\int\sqrt{7+x-x^2}\,\mathrm{d}x$.

### 解答 习题十

配方: 
$$
7+x-x^2=\frac{29}{4}-\left(x-\frac12\right)^2.
$$

令 $u=x-\frac12$, 则 $\mathrm{d}u=\mathrm{d}x$. 由**定理 2.1**（第一换元法则）, 
$$
\int\sqrt{7+x-x^2}\,\mathrm{d}x=\int\sqrt{\frac{29}{4}-u^2}\,\mathrm{d}u.
$$

由习题六(2-1)的结果, 
$$
\int\sqrt{a^2-u^2}\,\mathrm{d}u=\frac{a^2}{2}\arcsin\frac{u}{a}+\frac{u}{2}\sqrt{a^2-u^2}+C,
$$

其中 $a=\frac{\sqrt{29}}{2}$. 代回即得
$$
\int\sqrt{7+x-x^2}\,\mathrm{d}x=\frac{29}{8}\arcsin\frac{2x-1}{\sqrt{29}}+\frac{2x-1}{4}\sqrt{7+x-x^2}+C.
$$

$\blacksquare$
### 习题十一

（习题 4.2-2-11）求不定积分 $\displaystyle\int\frac{\mathrm{d}x}{x^2\sqrt{x^2+a^2}}$($a> 0$).

### 解答 习题十一

令 $x=a\tan t$, 则 $\mathrm{d}x=a\sec^2t\,\mathrm{d}t$, $\sqrt{x^2+a^2}=a\sec t$. 由**定理 2.2**（第二换元法则）, 
$$
\int\frac{\mathrm{d}x}{x^2\sqrt{x^2+a^2}}=\int\frac{a\sec^2t\,\mathrm{d}t}{a^2\tan^2t\cdot a\sec t}=\frac{1}{a^2}\int\frac{\sec t}{\tan^2t}\,\mathrm{d}t.
$$

化简: 
$$
\frac{\sec t}{\tan^2t}=\frac{\cos t}{\sin^2t}.
$$

令 $u=\sin t$, 则

$$
\mathrm{d}u=\cos t\,\mathrm{d}t,
$$
$$
\frac{1}{a^2}\int\frac{\cos t}{\sin^2t}\,\mathrm{d}t=\frac{1}{a^2}\int\frac{\mathrm{d}u}{u^2}=-\frac{1}{a^2u}+C.
$$

代回 $u=\sin t=\frac{x}{\sqrt{x^2+a^2}}$, 得
$$
\int\frac{\mathrm{d}x}{x^2\sqrt{x^2+a^2}}=-\frac{\sqrt{x^2+a^2}}{a^2x}+C.
$$

$\blacksquare$