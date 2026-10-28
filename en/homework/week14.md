# week14

> **Theorem 2.1 (Cauchy Mean Value Theorem)**<br>If $f$ and $g$ are continuous on $\left[a,b\right]$, differentiable on $\left(a,b\right)$, and $g'\left(x\right)\ne0$ for $a< x< b$, then there exists $c\in\left(a,b\right)$ such that $\frac{f\left(b\right)-f\left(a\right)}{g\left(b\right)-g\left(a\right)}=\frac{f'\left(c\right)}{g'\left(c\right)}$.

> **Theorem 2.2 (L'Hôpital's Rule, $\frac00$ Case)**<br>If $f$ and $g$ are defined and differentiable in a punctured neighborhood of $a$, $g'\left(x\right)\ne0$, $\lim_{x\to a}f\left(x\right)=\lim_{x\to a}g\left(x\right)=0$, and $\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ exists, then $\lim_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$.

> **Theorem 2.3 (L'Hôpital's Rule, $\frac{\infty}{\infty}$ Case)**<br>If $f$ and $g$ are defined and differentiable in a punctured neighborhood of $a$, $g'\left(x\right)\ne0$, $\lim_{x\to a}f\left(x\right)=\lim_{x\to a}g\left(x\right)=\infty$, and $\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ exists, then $\lim_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$.

---

## 3.2-1

Find the limits:

(1) $\lim_{x\to0}\frac{\ln\left(\cos ax\right)}{\ln\left(\cos bx\right)}$ ($a\ne0$, $b\ne0$);

(2) $\lim_{x\to0}\frac{a^x-1}{x}$ ($a> 0$);

(3) $\lim_{x\to0}\frac{\tan x-x}{x-\arcsin x}$;

(4) $\lim_{x\to0+}x^x$;

(5) $\lim_{x\to0+}x\ln x$;

(6) $\lim_{x\to0+}\frac{\ln\left(\sin x\right)}{x^2}$;

(7) $\lim_{x\to0+}\left(\sin x\right)^{\sin x}$.

### Solution 3.2-1

(1) This is $\frac00$. By **Theorem 2.2 (L'Hôpital's Rule, $\frac00$ Case)**,

$$
\lim_{x\to0}\frac{\ln\left(\cos ax\right)}{\ln\left(\cos bx\right)}=\lim_{x\to0}\frac{\frac{-a\sin ax}{\cos ax}}{\frac{-b\sin bx}{\cos bx}}=\frac{a^2}{b^2}.
$$

(2) This is $\frac00$. By **Theorem 2.2 (L'Hôpital's Rule, $\frac00$ Case)**,

$$
\lim_{x\to0}\frac{a^x-1}{x}=\lim_{x\to0}\frac{a^x\ln a}{1}=\ln a.
$$

(3) This is $\frac00$. By **Theorem 2.2 (L'Hôpital's Rule, $\frac00$ Case)**,

$$
\lim_{x\to0}\frac{\tan x-x}{x-\arcsin x}=\lim_{x\to0}\frac{\tan^2x}{1-\frac1{\sqrt{1-x^2}}}.
$$

The numerator $\sim x^2$ and the denominator $\sim-\frac{x^2}{2}$, so the limit is $-2$.

(4) This is $0^0$. Let $y=x^x$; $\ln y=x\ln x$. By (5), $\lim_{x\to0+}x\ln x=0$, so $\lim_{x\to0+}x^x=1$.

(5) This is $0\cdot\infty$. Rewriting and applying **Theorem 2.3 (L'Hôpital's Rule, $\frac{\infty}{\infty}$ Case)**,

$$
\lim_{x\to0+}x\ln x=\lim_{x\to0+}\frac{\ln x}{1/x}=\lim_{x\to0+}\frac{1/x}{-1/x^2}=0.
$$

(6) This is $\frac{\infty}{\infty}$. By **Theorem 2.3 (L'Hôpital's Rule, $\frac{\infty}{\infty}$ Case)**,

$$
\lim_{x\to0+}\frac{\ln\left(\sin x\right)}{x^2}=\lim_{x\to0+}\frac{\cot x}{2x}=+\infty.
$$

(7) This is $0^0$. Let $y=\left(\sin x\right)^{\sin x}$; $\ln y=\sin x\ln\left(\sin x\right)$. By (5) with $x$ replaced by $\sin x$, the limit is $e^0=1$. $\blacksquare$

---

## 3.2-2

If $\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ does not exist, does it follow that $\lim_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}$ does not exist? Consider $f\left(x\right)=x^2\sin\frac1x$ and $g\left(x\right)=x$ as $x\to0$.

### Solution 3.2-2

No. Take $f\left(x\right)=x^2\sin\frac1x$, $g\left(x\right)=x$.

$$
\lim_{x\to0}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to0}x\sin\frac1x=0.
$$

But

$$
f'\left(x\right)=2x\sin\frac1x-\cos\frac1x,\quad g'\left(x\right)=1.
$$

Thus $\frac{f'\left(x\right)}{g'\left(x\right)}=2x\sin\frac1x-\cos\frac1x$. As $x\to0$, $2x\sin\frac1x\to0$ but $\cos\frac1x$ oscillates without limit. Hence $\lim\frac{f'}{g'}$ does not exist while $\lim\frac{f}{g}$ does. The converse of L'Hôpital's rule is false. $\blacksquare$

---

## 3.2-4

Let $f$ have a second derivative at $a$ and set

$$
T\left(x\right)=f\left(a\right)+f'\left(a\right)\Delta x+\frac{f''\left(a\right)}2\left(\Delta x\right)^2,
$$

where $\Delta x=x-a$. Prove that $g\left(x\right)=f\left(x\right)-T\left(x\right)$ satisfies $g\left(a\right)=g'\left(a\right)=g''\left(a\right)=0$ and $f\left(x\right)=T\left(x\right)+o\left(\left(\Delta x\right)^2\right)$ as $x\to a$.

### Solution 3.2-4

From the definition, $T\left(a\right)=f\left(a\right)$, $T'\left(x\right)=f'\left(a\right)+f''\left(a\right)\Delta x$, $T''\left(x\right)=f''\left(a\right)$.

Thus

$$
g\left(a\right)=0,\quad g'\left(a\right)=0,\quad g''\left(a\right)=0.
$$

To show $g\left(x\right)=o\left(\left(\Delta x\right)^2\right)$, we compute $\lim_{\Delta x\to0}\frac{g\left(x\right)}{\left(\Delta x\right)^2}$, which is $\frac00$. By **Theorem 2.2 (L'Hôpital's Rule, $\frac00$ Case)**,

$$
\lim\frac{g\left(x\right)}{\left(\Delta x\right)^2}=\lim\frac{g'\left(x\right)}{2\Delta x}=\lim\frac{g''\left(x\right)}2=\frac{g''\left(a\right)}2=0.
$$

Hence $f\left(x\right)=T\left(x\right)+o\left(\left(x-a\right)^2\right)$. $\blacksquare$

---

## 3.2-6

Find $c$ such that $\lim_{x\to\infty}\left(\frac{x+c}{x-c}\right)^x=e^2$.

### Solution 3.2-6

This is $1^\infty$. Let $y=\left(\frac{x+c}{x-c}\right)^x$. Then

$$
\ln y=x\ln\left(1+\frac{2c}{x-c}\right)\sim x\cdot\frac{2c}{x-c}\to2c.
$$

Thus $\lim y=e^{2c}$. Setting $e^{2c}=e^2$ gives $c=1$. $\blacksquare$
