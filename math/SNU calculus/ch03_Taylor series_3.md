 III. 테일러 전개 #3
===



#### 로피탈의 정리

구간 $(a,\,b)$ 에서 정의된 미분가능한 함수 $f(x),\, g(x)$ 에 대하여 극한값
$$
l :=\lim_{x \searrow a} \dfrac{f'(x)}{g'(x)}
$$
가 존재한다고 하자. 이 때, $\displaystyle \lim_{x \searrow a} f(x)=0,\, \lim_{x \searrow a} g(x)=0$ 이거나 $\lim_{x \searrow a} f(x) = \infty,\,m \lim_{x \searrow a} g(x) = \infty$ 이면,
$$
\lim_{x \searrow a} \dfrac{f(x)}{g(x)}=l
$$
이다.

---

*(proof)* (1) 코시의 평균값정리에 의하여, $x,\,y \in (a,\,b)$ 가 $a$ 에 가까우면,
$$
f(x)-f(y) = (g(x)-g(y))\dfrac{f'(c)}{g'(c)}
$$
가 되는 $c$ 가 $x,\,y$ 사이에 존재한다. 이 식을 $g(x)$ 로 나눈 다음 정리하면,
$$
\dfrac{f(x)}{g(x)}= \dfrac{f(y)}{g(x)} + \left(1-\dfrac{g(y)}{g(x)}\right) \dfrac{f'(c)}{g'(c)}\\
\dfrac{f(x)}{g(x)}-l = \dfrac{f(y)}{g(x)} + \left(1-\dfrac{g(y)}{g(x)}\right) \left(\dfrac{f'(c)}{g'(c)}-l\right)+ l \dfrac{g(y)}{g(x)}
$$
을 얻는다. $\displaystyle l :=\lim_{x \searrow a} \dfrac{f'(x)}{g'(x)}$ 이므로 임의의 $\varepsilon>0$ 에 대하여,

$$
|x-a|<{\delta_1} \implies  \left|\dfrac{f'(x)}{g'(x)}-l\,\right|<{\varepsilon}\,,\\
|y-a|<{\delta_2} \implies  \left|\dfrac{f'(y)}{g'(y)}-l\,\right|<{\varepsilon}\,,\\
$$

를 만족하는 $\delta_1,\,\delta_2$ 가 존재한다. 이 때 $\delta = \min \{\delta_1,\,\delta_2\}$ 라 하자. $c$ 가 $x$ 와 $y$ 사이에 있으므로, $|c-a|$ 는 $|x-a|$ 와 $|y-a|$ 중 큰 값보다 항상 작다. 즉 $|c-a|<{\delta}$ 이므로 $\left|\dfrac{f'(c)}{g'(c)}-l\,\right| <{\varepsilon}$ 이다. 

따라서,
$$
\left|\dfrac{f(x)}{g(x)}-l\,\right| \le \left|\dfrac{f(y)}{g(x)}\right| + \left|1-\dfrac{g(y)}{g(x)}\right| \cdot \varepsilon + |l|\cdot \left|\dfrac{g(y)}{g(x)}\right|
$$
이다. $f$ 와 $g$ 의 $x \to a$ 극한이 $0$ 인 경우 위 식에서 $y\to a$ 극한을 취해도 위 부등식은 성립한다. 즉,
$$
\left|\dfrac{f(x)}{g(x)}-l\,\right| \le \varepsilon
$$
이다. 즉 $\displaystyle \lim_{x \searrow a} \dfrac{f(x)}{g(x)}=l$ 이다. 

$f$ 와 $g$ 의 $x\to a$ 극한이 $\infty$ 인 경우 위 식에서 $x\to a$ 극한을 취하면,
$$
\lim_{x \searrow a} \left|\dfrac{f(x)}{g(x)} -l\,\right| \le \varepsilon
$$
을 얻는다. 따라서 이 경우도  $\displaystyle \lim_{x \searrow a} \dfrac{f(x)}{g(x)}=l$  이다.





## 제 3장 탐구문제.



<b>1. </b> 정적분
$$
\int_{0}^1 \arctan x^2 dx
$$
를 값의 오차의 한계가 $10^{-3}$ 이하가 되도록 구하라.

---

$\dfrac{d}{dx} \arctan x = \dfrac{1}{1+x^2}= \displaystyle \sum_{k=0}^\infty (-1)^{k}x^{2k}$ 임을 이용한다. 
$$
\begin{align}
\arctan x^2 &= \sum_{k=0}^\infty \dfrac{(-1)^k x^{4k+2}}{2k+1}\\
\int_0^1 \arctan x^2 \, dx&=\sum_{k=0}^\infty \dfrac{(-1)^k}{(2k+1)(4k+3)}

\end{align}
$$
Tayler series를 생각하면 $(2k+1)(4k+3)>10^3$ 이 되도록 하는 $k$ 값을 찾으면 된다.  $k>10$ 이므로 위 식을 10 차항 까지 구하면 된다. 이에 대한 python code 는 아래와 같다.

```python
import numpy as np
nn = np.arange(0,11)
pp = ((-1)**nn) /(2*nn+1)/(4*nn+3)
print(pp.sum())

0.2984047079489637
```





<b>2. </b> 원점 근방에서 정의된 $n+1$ 급 함수 $f(x)$ 의 테일러 전개에서 $n$ 차 나머지 항은
$$
R_n f(x) = \dfrac{1}{n!} \int_0^x (x-t)^n f^{(n+1)}(t)\,dt
$$
로 주어짐을 귀납법을 이용하여 보이라.

---

(1) $n=0$ 일 때,
$$
R_0 f(x) = \int_0^x f'(t) dt = f(t)-f(0)
$$
이므로 성립한다. 

(2) $n$ 일 때 성립함을 가정하자.
$$
\begin{align}
R_{n+1}f(x) &= \dfrac{1}{(n+1)!} \int_0^x (x-t)^{n+1} f^{(n+2)} (t)\, dt \\
&=\dfrac{1}{(n+1)!}\left[ (x-t)^{n+1} f^{(n+1)}(t)\right]_{t=0}^{t=x} - \dfrac{1}{(n+1)!} \int_0^x\left(-(n+1)(x-t)^{n} \right)f^{(n)}(t)\, dt \\
&=-\dfrac{f^{(n+1)}(t)}{(n+1)!} x^{n+1}  + R_n f(x)

\end{align}
$$
이다. 우리는,
$$
f(x) = f(0)+\cdots + \dfrac{f^{(n)}(0)}{n!}x^{n} +R_{n}f(x) = f(0) + \cdots +  \dfrac{f^{(n)}(0)}{n!}x^{n} + \dfrac{f^{(n+1)}(0)}{(n+1)!}x^{n+1} + R_{n+1}f(x)
$$
임을 알고 있으므로 $n$ 일 때 성립함을 가정하면 $n+1$ 에서도 성립함을 보였다.



<b>3. </b> (**Fourier** 급수) Fourier에 의하면 모든 주기함수는 사인함수와 코사인 함수의 (무한)합으로 나타난다. 좀 더 자세히 서술하면 다음과 같다. 함수
$$
\sin x,\, \sin 2x,\, \sin 3x,\ldots,\,\qquad,\,1,\, \cos x,\, \cos 2x,\, \cos 3x,\ldots
$$
는 모두 주기가 $2\pi$ 인 함수이다(최소주기가 아니라 일반적인 주기, 즉 어떤 $T\in \mathbb{R}$ 에 대해 모든 $x\in \mathbb{R}$ 에서 $f(x)=f(x+T)$ 일 때 $T$ 를 $f$ 의 주기라 한다.) 함수 $f(x)$ 가 주기가 $2\pi$ 인 함수이면,
$$
f(x) = a_0 + \sum_{n=1}^\infty (a_n \cos nx + b_n \sin nx)
$$
를 만족시키는 실수 $a_0,\,a_1,\,b_1,\,a_2,\,b_2,\ldots$ 가 (오직 하나) 존재한다. 이때 위 식의 오른쪽 항을 $f$ 의 Fourier 급수 전개라고 부른다. 이제 급수
$$
\sum_{n=1}^\infty \dfrac{\sin nx}{n}
$$
가 수렴하기 위한 $x$ 의 범위를 구하라.

---

$\sin nx = \dfrac{e^{inx}-e^{-inx}}{2i}$ 이 다. 위식은 
$$
\begin{align}
\sum_{n=1}^\infty \dfrac{\sin nx}{n} &=\dfrac{1}{2i}\sum_{n=1}^\infty \dfrac{\left(e^{inx}-e^{-inx}\right)}{n}  \\
&=-\dfrac{1}{2} \sum_{n=1}^\infty\left[  \int_{0}^x e^{int}\,dt +\int_0^x e^{-int}\, dt\right] \\
&=-\dfrac{1}{2} \int_0^x \left[\sum_{n=1}^\infty \left(e^{int}+e^{-int}\right)\right] \,dt

\end{align}
$$
이다. $\sum$  안이 수렴하려면 

---- to be done ----



<b>4. </b> 함수
$$
f(x):=\left\{ \begin{array}{ll} e^{-\tan^2 x} \,,\qquad &x \in \left(-\dfrac{\pi}{2},\, \dfrac{\pi}{2}  \right) \\ 0\,, & x \not\in \left(-\dfrac{\pi}{2},\, \dfrac{\pi}{2} \right)\end{array}\right.
$$
가 무한급 함수임을 보여라.

---

$x\not\in\left(-\dfrac{\pi}{2},\, \dfrac{\pi}{2}\right)$ 일 때는 무한급이므로 $x\in \left(-\dfrac{\pi}{2},\, \dfrac{\pi}{2} \right)$ 와 두 영역의 경계에서만 생각하자. $e^{-\tan^2 x}$ 함수의 $n$ 차 미분의 각 term은 모두 $e^{-\tan^2 x}$ 를 포함하고 있음을 알 수 있다. 이 때,
$$
\lim_{x \to -\pi/2} e^{-\tan^2 x}= \lim_{x \to \pi/2} e^{-\tan^2 x}=0
$$
이다. 
$$
\begin{align}
f'(x) &= -2\dfrac{\sin x}{\cos^3 x} e^{-\tan^2 x}
\end{align}
$$






<b>6. </b> (큰 $O$ ) 원점을 포함하는 구간 $I$ 에서 정의된 함수 $f$ 와 자연수 $n$ 에 대하여 어떤 상수 $B,\, \delta$ 가 존재하여, $|x|<\delta$ 이면 $|f(x)|\le B|x|^n$ 이라고 하자. 이 대 $f$ 를 원점 근방에서 $O(x^n)$ 이라 부르고 $f(x) \in O(x^n)$ 이라고 쓴다.

(1) $\sin x \in O(x)$ 임을 보이라.

(2)  $\sin x \not\in O(x^2)$ 임을 보이라.

(3) $f(x),\,g(x) \in O(x^n)$ 이면 $f(x)+g(x) \in O(x^n)$ 임을 보이라.

(4) 임의의 실수 $c$ 와 $f(x) \in O(x^n)$ 에 대하여 $cf(x) \in O(x^n)$ 임을 보이라.

---

(1) $\delta<1$ 이라 하자.  $\sin x = x-\dfrac{\sin (x_*) x^3}{6}$  을 만족하는  $x_* \in (-\delta,\,\delta)$  가 존재한다. $|\sin (x_*)|\le 1$, $|x| <\delta <1$ 을 이용하면, 
$$
\begin{align}
|\sin x| &= \left|x - \dfrac{\sin(x_*)}{6} x^3\right| \le |x|+\left|\dfrac{\sin (x_*)}{6}\right||x|^3 \\
& \le |x|+\dfrac{1}{6} |x|^3 < |x| + \dfrac{1}{6} |x|=\dfrac{7}{6}|x|

\end{align}
$$
(2) $\sin x\in O(x^2)$ 라 가정하자. 즉 $|x|<\delta \implies |\sin x| \le B|x|^2$ 를 만족하는 $B,\, \delta$ 가 존재함을 가정한다. 그렇다면 $-Bx^2 \le \sin x \le Bx^2$ 이므로, 양변을 $x^2$ 으로 나눈 후 $x \to 0$ 극한을 취하면, $\displaystyle \lim_{x \to 0 }\dfrac{\sin x}{x^2}$ 은 $(-B,\,B)$ 사이에 위치해야 하나 우리는 이 극한값이 발산함을 알고 있다.



(3) $|x|<\delta_1 \implies |f(x)|\le B_1 |x|^n$ 이고 $|x|<\delta_2 \implies |g(x)|\le B_2 |x|^n$ 이라 하자. $\delta = \min \{\delta_1,\,\delta_2\}$ 라 하면 $|x|<\delta \implies |f(x)|\le B_1 |x|^,\, g(x)\le B_2|x|^n$ 이다. 
$$
|x|<\delta \implies |f(x)+g(x)|\le |f(x)|+|g(x)|\le (B_1+B_2)|x|^n
$$


(4) $|x|<\delta \implies |f(x)|\le B|x|^n \implies |cf(x)|\le (|c|B) |x|^n$. 



<b>7. </b> 두 함수 $f,\,g : [2,\infty) \to \mathbb{R}$ 에 대하여
$$
\lim_{x \to \infty} \dfrac{f(x)}{g(x)} =1
$$
이며 $f\sim g$ 라고 나타내기로 하자. 이제 로피탈의 정리를 이용하여,
$$
\dfrac{x}{\ln x} \sim \int_2^x \dfrac{dt}{\ln t}
$$
임을 보이라.

---

$\displaystyle \lim_{x \to \infty} \dfrac{x}{\ln x}=\infty$ 와 $\displaystyle \lim_{x \to \infty}\int_2^x \dfrac{dt}{\ln t}=\infty$ 임은 쉽게 보일 수 있다. 이제 로피탈의 정리를 사용한다.
$$
\lim_{x\to \infty} \dfrac{\dfrac{x}{\ln x}}{\displaystyle \int_2^x \dfrac{dt}{\ln t}} = \lim_{x \to \infty} \dfrac{\dfrac{1}{\ln x} - \dfrac{1}{(\ln x)^2}}{1/\ln x}=\lim_{x \to \infty}\dfrac{1-\dfrac{1}{\ln x}}{1}=1
$$


<b>8. </b> 정수론을 연구하는 학자들은

> 주어진 자연수 $n$ 에 대하여, $n$ 이하의 소수의 개수가 과연 얼마나 될까?

하는 문제에 관심이 많다. 여기에서 $n$ 이하의 소수의 개수를 $\pi (n)$ 이라고 두면,
$$
\pi (1)=0,\, \quad \pi(2)=1,\quad \pi(3)=2,\quad \pi (4) =2,\quad \pi (5) =3,\ldots
$$
을 알 수 있다.

1896년 경에 Hadamard와 de la Vallée-Poussin 에 의하여 독자적으로 발견된 소수정리에 의하면,
$$
\pi (n) \sim \dfrac{n}{\ln n} \tag{1}
$$
임이, 즉,
$$
\lim_{n \to \infty} \dfrac{\pi (n) \ln n}{n}=1 \tag{2}
$$
이 알려졌다. 이를 이용하여 멱급수
$$
\sum_{n=0}^\infty \dfrac{1}{\pi (n)} x^n
$$
의 수렴반경을 구하라.

---

$\displaystyle \sum_n a_n x^n$ 에 대한 수렴반경은 $\rho:=\displaystyle \lim_{n \to \infty} \left| \dfrac{a_{n+1}}{a_n} \right|$ 일 때 $\dfrac{1}{\rho}$ 임을 안다.  

식 (2) 에 의하면 어떤 고정된 $\varepsilon>0$ 에 대해 $N\in \mathbb{N}$ 이 존재하여 $n\ge N \implies \left|\dfrac{\pi (n) \ln n}{n }-1\right|< \dfrac{\varepsilon}{2}$ 이다. 따라서, 
$$
\left(1-\dfrac{\varepsilon}{2}\right) \dfrac{n}{\ln n} < \pi (n) <\left(1+\dfrac{\varepsilon}{2}\right) \dfrac{n}{\ln n}
$$
이다. $0<\varepsilon \ll 1$ 이라도 잡아도 상관 없으므로,
$$
\dfrac{\left(1-\dfrac{\varepsilon}{2}\right) \dfrac{n}{\ln n}}{\left(1+\dfrac{\varepsilon}{2}\right) \dfrac{n+1}{\ln (n+1)}}<\dfrac{\pi (n)}{\pi(n+1)} <\dfrac{\left(1+\dfrac{\varepsilon}{2}\right) \dfrac{n}{\ln n}}{\left(1-\dfrac{\varepsilon}{2}\right) \dfrac{n+1}{\ln (n+1)}}
$$
$(1-x)/(1+x)$ 는 $0$ 근방에서 단조감소, $(1+x)/(1-x)$ 는 $0$ 근방에서 단조증가 함수이므로, 충분히 작은 $\varepsilon$ 에 대해,
$$
(1-\varepsilon)\dfrac{ \dfrac{n}{\ln n}}{\dfrac{n+1}{\ln (n+1)}}<\dfrac{\left(1-\dfrac{\varepsilon}{2}\right) \dfrac{n}{\ln n}}{\left(1+\dfrac{\varepsilon}{2}\right) \dfrac{n+1}{\ln (n+1)}}<\dfrac{\pi (n)}{\pi(n+1)} <\dfrac{\left(1+\dfrac{\varepsilon}{2}\right) \dfrac{n}{\ln n}}{\left(1-\dfrac{\varepsilon}{2}\right) \dfrac{n+1}{\ln (n+1)}}<(1+\varepsilon)\dfrac{ \dfrac{n}{\ln n}}{\dfrac{n+1}{\ln (n+1)}}
$$
이므로 $\displaystyle \lim_{n \to \infty} \dfrac{\pi (n)}{\pi (n+1)}= \lim_{n \to \infty} \dfrac{n\ln {n}}{(n+1)\ln (n+1)}$ 이며, 로피탈의 정리를 사용하면,


$$
\lim_{n \to \infty} \dfrac{n\ln {n}}{(n+1)\ln (n+1)}=\lim_{n \to \infty} \dfrac{\ln n+1}{\ln (n+1)+1}=\lim_{n \to \infty} \dfrac{n+1}{n}=1
$$
이다. 따라서 수렴반경은 $1$ 이다. 



<b>9. </b> 구간 $I$ 에서 정의된 미분가능함수 $f(x)$ 와 주어진 점 $c\in I$ 에 대하여
$$
f(x) =f(c)+(x-c)g(x)
$$
를 만족시키는 연속함수 $g(x)$ 가 존재함을 보여라. 이때 $g(c) =f'(c)$ 임을 보이라. 만약 $f(x)$ 의 $n$ 계 도함수 $f^{(n)}(x)$  가 존재하면, $g(x)$ 의 $(n-1)$ 계 도함수가 존재함을 보이라.

---

$h(x)=\dfrac{p(x)}{q(x)}$ 이며 $p(x),\,q(x)$ 가 어떤 구간 $I$ 에서 연속이고 이 구간에서 $p(x)\ne 0$ 이면 $h(x)$ 도 $I$ 에서 연속임을 보이자. $p(x),\, q(x)$ 가 $c\in I$ 에서 연속이므로, 임의의 $\varepsilon>0$ 에 대해 어떤 $\delta_1>0,\, \delta_2>0$ 이 존재하여 $0<|x-c|<\delta_1 \implies |p(x)-q(c)|<\varepsilon$ 이고 $0<|x-c|<\delta_2\implies |q(x)-q(c)|<\varepsilon$   이다. $\delta = \min \{\delta_1,\, \delta_2\}$ 라 하면 $0<|x-c|<\delta \implies |p(x)-p(c)|<\varepsilon,\, |q(x)-q(c)|<\varepsilon$ 이다.  우선 $\varepsilon < \min \{1,\,|q(c)|\}$ 라 선택한다고 하자. 
$$
\begin{align}
|h(x)-h(c)| &= \left|\dfrac{p(x)q(c)-q(x)p(c)}{q(x)q(c)}\right|=\left|\dfrac{q(c)(p(x)-p(c))-p(c)(q(x)-q(c))}{q(x)q(c)}\right| \\
&\le \dfrac{1}{|q(x)|}\left| p(x)-p(c)\right|+\dfrac{|p(c)|}{|q(c)|} \left|q(x)-q(c) \right| \\
&\le\left(\dfrac{1}{|q(x)|} + \left|\dfrac{p(c)}{q(c)}\right| \right) \varepsilon

\end{align}
$$
를 얻었다. $\varepsilon> |q(x)-q(c)|\ge \large \left| \normalsize |q(x)|-|q(c)|\large\right|$ 이므로 $|q(c)|-\varepsilon < |q(x)|<|q(c)|+\varepsilon$ 이며 $\varepsilon<q(c)$ 이므로, $|q(x)|>\dfrac{|q(c)|}{2}$ 이다. 따라서,
$$
|h(x)-h(c)|\le \left(\dfrac{2+|p(c)|}{|q(c)|} \right)\varepsilon
$$
이므로 $h(x)$ 는 연속이다. 주어진 식에 대해서는 $g(x) = \dfrac{f(x)-f(c)}{x-c}$ 이며 $f(x)-f(c)$ 와 $x-c$ 가 구간 $I$ 중 $c$ 를 제외한 구간에서 앞의 증명을 만족하므로 $c$ 를 제외한 영역에서 연속이다. 그리고 $g(c)=f'(c)$ 로 정의 한다면, $\displaystyle \lim_{x \to c} g(x) = f'(c)$ 이므로 $g(x)$ 는 구간 $I$ 에서 연속인 함수가 된다. 

즉,
$$
g(x) = \left\{\begin{array}{ll} \dfrac{f(x)-f(c)}{x-c}\,,\qquad & x \ne c \\ f'(c) \,, & x=c\end{array}\right.
$$
이며 $g(x)$ 는 연속함수이다.  



이제 $g' (x) = \dfrac{f'(x)(x-c)-f(x)-f(c)}{(x-c)^2}$ when $x\ne c$ 이며 로피탈의 정리를 이용하면 $\displaystyle \lim_{x \to c}g'(x) = \dfrac{f''(c)}{2}$ 임을 안다. 

이제 $F_n[x]$ 를 $f^{(k)}(x)(x-c)^l$ where $k,\, l = 0,\ldots,\,{n-1}$ and $k+l<n$ 꼴의 함수의 선형결합이으로 이루어진 함수의 집합이라고 하자. $f$ 가 $n$ 계 도함수일 때 $F_{n}[x]$ 에 속한 모든 함수는 구간 $I$ 에서 미분가능하다. $h(x)\in F_n[x]$ 라면 $h'(x)\in F_{n+1}[x]$ 임은 쉽게 알 수 있다.  즉 $h(x) =f(x)-f(c) \in F_0[x]$  에 대해 
$$
g'(x)=\dfrac{f'(x)(x-c)-h(x)}{(x-c)^2}
$$
이다. $h(x) \in F_{n-1}[x]$ 에 대해  $g^{(n)}(x) = \dfrac{f^{(n)}(x)(x-c)^{n}+h(x)}{(x-c)^{n+1}}$  일 때, 
$$
\begin{align}
g^{(n+1)}(x) &= \dfrac{(f^{(n+1)}(x)(x-c) +f^{(n)}(x) + h'(x))(x-c) - (n+1)(f^{(n)}(x)(x-c)+h(x))}{(x-c)^{n+2}}\\
&= \dfrac{f^{(n+1)}(x)(x-c) + q(x)}{(x-c)^{n+2}} =\dfrac{f^{(n+1)}(x)}{(x-c)^{n+1}} + \dfrac{q(x)}{(x-c)^{n+2}}& q(x)\in F_{n}[x]
\end{align}
$$
 이다. 즉 $f^{(n)}(x)$ 가 존재한다면 $x\ne c$ 에 대해 $g^{(n)}(x)$ 가 존재한다. 





<b>10. </b> 원점에서 함수가 $f(x)=\dfrac{1}{1+x+x^2}$ 의 테일러 급수가 수렴하는 $x$ 의 범위를 구하라.

---

우리는 $\dfrac{1}{1+y}$ 의 테일러 전개에서 수렴반경이 $1$ 임을 알고 있다. 따라서 $f(x)$ 의 수렴 조건은 $|x+x^2|<1$ 이다. 이 조건을 풀면
$$
\dfrac{-1-\sqrt{5}}{2} <x<\dfrac{-1+\sqrt{5}}{2}
$$
이므로 수렴반경은 $\dfrac{-1+\sqrt{5}}{2}$ 이다. 



<b>11. </b> 무한급 함수 $f: \mathbb{R}\to \mathbb{R}$ 에 대하여 점 $a\in \mathbb{R}$ 에서의 $n$ 차 테일러 다항식을 $T_{n}^a (f)$ 로 나타내기로 하자. 이제 임의의 $g,\, h \in  \mathcal{C}^\infty (\mathbb{R})$ 에 대하여,
$$
\begin{align}
T_n^a (gh) & \equiv (T_n^a g)(T_n^a h) & \mod\;(x-a)^{n+1}\\
T_n^a (g \circ h) &\equiv \left(T_n^{h(a)} \right) \circ T_{n}^a h & \mod \; (x-a)^{n+1}
\end{align}
$$
을 보이라.

----

(1) $T_n^a (gh)\equiv (T_n^a g)(T_n^a h) \; \mod \; (x-a)^{n+1}$ 임을 보이자. $gh$ 의 $n$ 차 도함수는 다음을 만족함을 보이자.

$$
\dfrac{d^n}{dx^n}(gh)=\sum_{k=0}^n \dfrac{n!}{k!(n-k)!} \dfrac{d^{k}g}{dx^k} \cdot \dfrac{d^{n-k}h}{dx^{n-k}}=\sum_{k=0}^k {}_nC_{k} g^{(k)}h^{(n-k)}
$$
Induction 을 사용하여 보이자. $n=1$ 일 때 $\dfrac{d}{dx}(gh)= g'h + h'g$ 이므로 성립한다. $n$ 일 때 성립함을 가정한다.
$$
\begin{align}
\dfrac{d^{n+1}}{dx^{n+1}}(gh)&= \dfrac{d}{dx}\left(\dfrac{d^{n}}{dx^n}(gh)\right) \\
&=\sum_{k=0}^n \dfrac{n!}{k!(n-k)!} \left(g^{(k)}h^{(n-k+1)}+g^{(k+1)} h^{(n-k)}  \right)\\
&= \left( g^{(0)}h^{(n+1)} + g^{(1)}h^{(n)}\right) + {}_nC_1 \left(g^{(1)}h^{(n)}+ g^{(2)}h^{(n-1)} \right) + \cdots +{}_nC_k \left(g^{(k)}h^{(n-k+1)} + g^{(k+1)}h^{(n-k)}\right) \\
& \qquad \qquad \qquad \qquad + {}_nC_{n-1} \left(g^{(n-1)} h^{(2)} + g^{(n)} h^{(1)}\right) + {}_nC_n \left(g^{(n)}h^{(1)}+g^{(n+1)}h^{(0)} \right) \\
&= g^{(0)}h^{(n+1)} + \left( g^{(1)}h^{(n)} +{}_nC_1 g^{(1)}h^{(n)}\right) + \cdots + \left( {}_nC_{k-1} g^{(k)}h^{(n-k-1)} +{}_nC_{k} g^{(k)}h^{(n-k+1)} \right)\\
&\qquad \qquad \qquad \qquad + \cdots + \left( {}_nC_{n-1} g^{(n)}h^{(1)} +  {}_nC_n g^{(n)} h^{(1)}\right) + {}_nC_n g^{(n+1)}h^{(0)} \\
&= g^{(0)}h^{(n+1)} + (n+1) g^{(1)}h^{(n)} + \cdots + \left({}_nC_{k-1}+{}_n C_k  \right) g^{(k)}h^{(n+k-1)} + \cdots (n+1) g^{(n)}h^{(1)} + g^{(n+1)}h^{(0)} \\
&={}_{n+1}C_{0} g^{(0)}h^{(n+1)} + {}_{n+1}C_{1} g^{(1)}h^{(n)} + \cdots + {}_{n+1}C_{k} g^{(k)} h^{(n+k-1) }+ \cdots +{}_{n+1}C_{n} g^{(n)} h^{1} + {}_{n+1}C_{n+1}g^{(n+1)}h^{(0)}\\
&= \sum_{k=0}^{n+1} \dfrac{(n+1)!}{k! (n-k+1)!} g^{(k)}h^{{(n-k+1)}}
\end{align}
$$


이제 $T_n^a (gh)$ 의 $k$ 차 항은 $\dfrac{(gh)^{(k)}(a)}{k!}(x-a)^k = \dfrac{1}{k!}\displaystyle \sum_{m=0}^k \dfrac{k!}{m!(k-m)!} g^{(m)}(a)h^{(k-m)}(a) (x-a)^k=\sum_{m=0}^k \dfrac{g^{(m)}(a) h^{(k-m)}(a)}{m! (k-m)!}(x-a)^k$ 임을 안다. $(T_n^a g)(T_n^ah)$ 의 $k$ 차 항은 $m=0,\,1\,\ldots,\, k$ 에 대해 $(T_n^a g)$ 의 $m$ 차항과 $(T_n^a h)$ 의 $k-m$ 차항의 곱이다. 따라서,
$$
\sum_{m=0}^{k} \dfrac{g^{(m)}(a)}{m!}(x-a)^{m} \dfrac{h^{(k-m)}(a)}{(k-m)!}(x-a)^{k-m}=\sum_{m=0}^k \dfrac{g^{(m)}(a) h^{(k-m)}(a)}{m!(k-m)!}(x-a)^k
$$
이다. 또한 $(T_n^a g)(T_n^a h)$ 중 $n$ 차 이상의 상은 $\mod\, (x-a)^{n+1}$ 에 의해 사라진다. 증명 끝.



(2) $T_n^a (g \circ h) \equiv \left(T_n^{h(a)g} \right) \circ T_{n}^a h \; \mod \; (x-a)^{n+1}$ 임을 보이자.

Induction을 사용한다. $n=1$ 이면,
$$
\begin{align}
T_1^a (g \circ h) &= g(h(a)) + h'(a)g'(h(a)) (x-a) \\
\left(T_1^{h(a)}g \right) \circ T_{1}^a h \; \mod \; (x-a)^{2} &= (g(h(a))+g'(h(a))(x-h(a))\circ(h(a)+h'(a)(x-a)) \mod (x-a)^2 \\
&= g(h(a)) +g'(h(a))(h(a)+h'(a)(x-a)-h(a)) \mod (x-a)^2\\
&= g(h(a)) +h'(a) g'(h(a))(x-a)
\end{align}
$$
이므로 두 식이 같다.

이제 $T_n^a (g \circ h) \equiv \left(T_n^{h(a)}g \right) \circ T_{n}^a h \; \mod \; (x-a)^{n+1}$ 임을 가정하자.
$$
\begin{align}
\left(T_{n+1}^{h(a)}g \right) \circ T_{n+1}^a h  \mod  (x-a)^{n+2} &= \left(\sum_{k=0}^{n+1} \right)\\

T_{n+1}^a (g \circ h) &= T_{n}^a (g \circ h) + \dfrac{d}{dx}

\end{align}
$$
--- to be done ---





<b>12. </b> 원점 근방에서 정의된 무한급 함수 $f$ 에 대하여 수열
$$
f_0 := f(0),\quad f_1 := f'(0),\quad f_2 := f''(0), \ldots
$$
를 대응시키는 사상을 생각하자. 이 사상은 전사임을 보여라.

---

