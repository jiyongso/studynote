II. 멱급수와 수렴반경 #3 
===



#### 멱급수의 기본정리

멱급수 $\displaystyle \sum_{n=0}^\infty a_n x^n$ 의 수렴반경이 $r>0$ 이면

(i) 멱급수 $\displaystyle \sum_{n=1}^\infty na_n x^{n-1}$ 의 수렴반경도 $r$ 이다.

(ii) 멱급수 $\sum_{n=0}^\infty\dfrac{a_n}{n+1}x^{n+1}$ 의 수렴반경도 $r$ 이다.

(iii) 구간 $-r<x<r$ 에서 $\displaystyle f(x):= \sum_{n=0}^\infty a_n x^n$ 으로 두면 함수 $f(x)$ 는 미분가능하며,

 (a) $\displaystyle f'(x) = \sum_{n=1}^\infty na_n x^{n-1}$   ($-r<x<r$)

(b) $\displaystyle \int_0^x f(t)\,dt = \sum_{n=0}^\infty \dfrac{a_n}{n+1}x^{n+1}$    ($-r<x<r$)

이다. 

---

*(proof)* (i) 우선 $0<t<c<r$ 이 되도록 $t,\,c$ 를 잡자. 우리는 $\displaystyle \lim_{n \to \infty} n^{1/n}= \lim _{n \to \infty} e^{\frac{1}{n}\ln n}=1$ 임을 안다.

큰 $n$ 에 대하여 $n^{1/n}t<c$ 이므로,
$$
\left|na_nt^{n-1}\right| = |a_n| (n^{1/n}t)^n\dfrac{1}{t} \le |a_n|c^n \dfrac{1}{t}
$$
이므로 $\displaystyle \sum_{n=0}^\infty na_n t^{n-1}$ 은 절대수렴한다. 즉 $\displaystyle \sum_{n =0}^\infty na_nt^{n-1}$ 의 수렴반경은 $r$ 보다 크거나 같다.

이제 $\displaystyle \sum_{n=0}^\infty na_nx^{n-1}$ 이 절대수렴하면 비교판정법에 의해 $\displaystyle \sum_{n=0}^\infty a_n x^{n-1}$ 이 절대수렴하므로 $\displaystyle \sum_{n=0}^\infty a_n x^n = x\left(\sum_{n=0}^\infty a_n x^{n-1}\right)$ 도 절대수렴한다. 따라서 $\displaystyle \sum_{n=0}^\infty na_n x^{n-1}$ 의 수렴반경은 $r$ 보다 작거나 같다. 두 결과를 합하면 $\displaystyle \sum_{n=0}^\infty a_n x^n$ 과 $\displaystyle \sum_{n=0}^\infty a_n x^{n-1}$ 의 수렴반경은 같다.



(ii) $\sum a_n x^n$ 과 $\sum na_n x^{n-1}$ 이 같은 수렴반경을 가지며 따라서 $\sum (n+1)a_{n+1}x^{n}$ 도 같은 수렴반경을 가진다. $na_n=b_{n-1}$ 이라 놓으면, $\sum \dfrac{b_{n-1}}{n}x^n$ 과 $\sum b_{n-1} x^n$ 은 같은 수렴반경을 가진다. 또한 $\sum \dfrac{b_n}{n+1}x^{n+1}$ 과 $x \left(\sum b_n x^n \right)$ 은 같은 수렴 반경을 가진다.



(iii-a) $f(x)= \displaystyle \sum_{n=0}^\infty a_n x^n$ 이라 할 때, $x\in (-r,\,r)$ 에서,
$$
\left(\lim_{h \to 0} \dfrac{f(x+h)-f(x)}{h}\right)-\sum_{n =0}^\infty a_n x^{n-1} =0
$$
임을 보이자. $|x|<c<r$ 인 $c$ 를 선택한다. $|h|$ 가 $|x+h|\le|x|+|h|<c$ 가 되도록 $h$ 를 충분히 작게 잡으면 $x+h$ 도 수렴반경에 포함된다. 따라서,
$$
\begin{align}
A(h)&:=\dfrac{f(x+h)-f(x)}{h}-\sum_{n=0}^\infty na_n x^{n-1} \\
&= \sum \dfrac{a_n (x+h)^n-a_n x^n}{h} - \sum na_n x^{n-1} \\
&= \sum a_n \left(\dfrac{(x+h)^n-x^n}{h}-nx^{n-1}\right)

\end{align}
$$
인데, 평균값 정리에 의해 $(x+h)^n-x^n = hn{y_n}^{n-1}$ 을 만족하는 $y_n$ 이 $x+h$ 와 $x$ 사이에 존재한다. 따라서,
$$
A(h)=\sum na_n({y_n}^{n-1}-x^{n-1})
$$
이 되며, 역시 평균값 정리에 의해 ${y_n}^{n-1}-x^{n-1}=(n-1)(y_n-x){z_n}^{n-1}$ 을 만족하는 $z_n$ 이 $x$ 와 $y_n$ 사이에 존재한다. 

앞의 조건에 의해 $|y_n-x| \le |h|$ 이며 $|z_n |<c$ 이므로 (i) 에 의해
$$
|A(h)| = \left| \sum na_n (n-1)(y_n-x){z_n}^{n-1}\right| \le |h|\sum n(n-1) |c|^{n-1} <\infty
$$
이다. 따라서 $\displaystyle \lim_{h\to 0} A(h)=0$ 이다. 



(iii-b) 미적분학의 기본정리에 의해,
$$
\dfrac{d}{dx} \left(\int_{0}^x \sum_{n=0}^\infty a_n t^n\, dt\right) = \sum_{n=0}^\infty a_n x_n
$$
이며 (iii-a) 에 의해
$$
 \dfrac{d}{dx}\left( \sum_{n=0}^\infty \dfrac{a_n}{n+1}x^{n+1} \right) = \sum_{n=0}^\infty a_n x_n
$$
이므로, 
$$
\int_0^x \sum_{n=0}^\infty a_n t_n\, dt = \sum_{n=0}^\infty a_n x_n + \text{const}
$$
이다. $x=0$ 을 넣으면 $\text{const}=0$ 임을 안다. 따라서,
$$
\int_0^x \sum_{n=0}^\infty a_n t_n\, dt = \sum_{n=0}^\infty a_n x_n
$$
이다.



## 제 2장 탐구문제



<b>1. </b> 연속함수 $f(x)$ 가 모든 실수 $x$ 에 대하여
$$
x=(1-e^{-x})f(x)
$$
를 만족시킬 때,
$$
\lim_{x\to 0} \dfrac{f(x)-1-\dfrac{1}{2}x}{x^2}
$$
를 구하라.

---

$f(x)$ 는 베르누이 함수로 $f(x)=1-\dfrac{1}{2}x + \dfrac{1}{12}x^2 + \cdots$ 이므로 이 극한은 $\dfrac{1}{12}$ 이다.



<b>2. </b> (**멱급수와 복소수**) 지수함수의 멱급수전개 
$$
e^x = \sum \dfrac{x^n}{n!}
$$
을 살펴보면, 이 등식의 오른쪽 항은 $x$ 대신에 임의의 복소수를 대입하여도 수렴하는 것을 알 수 있다. 따라서 우리는 임의의 복소수 $z$ 에 대하여
$$
e^z := \sum_{n=0}^\infty \dfrac{z^n}{n!}
$$
으로 정의한다. 특히 임의의 실수 $\theta$ 에 대하여
$$
e^{i\theta}=\sum_{n=0}^\infty i^n\dfrac{\theta^n}{n!} = \sum_{k=0}^\infty (-1)^k \dfrac{\theta^{2k}}{(2k)!}+i \sum_{k=0}^\infty (-1)^k \dfrac{\theta^{2k+1}}{(2k+1)!} = \cos \theta +i\sin \theta
$$
가 성립한다 이 등식
$$
e^{i\theta}=\cos \theta + i \sin \theta
$$
를 **De Moivre-Euler 공식** 이라고 부른다. 이아 같이 복소수체 안에서는 삼각함수나 지수함수가 모두 한 가족이다. 이제 임의의 복소수 $z,\, w$ 에 대하여
$$
e^{z+w}=e^z \cdot e^w
$$
이 성립함을 보이라.

---

$$
\begin{align}
e^z\cdot e^w &= \left(\sum_{n=0}^\infty \dfrac{z^n}{n!}\right) \left(\sum_{m=0}^\infty \dfrac{w^m}{m!}\right)=\sum_{n=0}^\infty \sum_{m=0}^\infty \dfrac{z^nw^m}{n!m!}\\
&=\sum_{k=0}^\infty \sum_{l=0}^k \dfrac{1}{l!(k-l)!}z^l w^{k-l} \\
&=\sum_{k=0}^\infty \dfrac{1}{k!}\sum_{l=0}^k \dfrac{k!}{l! (k-l)!}  z^l w^{k-l}=\sum_{k=0}^\infty \dfrac{1}{k!} (z+w)^k = e^{z+w}

\end{align}
$$



<b>3. </b> 임의의 실수 $\theta$ 에 대하여 등식
$$
(\cos \theta + i\sin \theta)^n=\cos n\theta + i \sin n\theta
$$
가 성립함을 보이라.

---

임의의 복소수 $z$ 와 자연수 $n$ 에 대해  $\left(e^{z}\right)^n=e^{nz}$ 임을 보이자. $z=1$ 일 때는 자명하다. $n$ 일 때 성립함을 가정하면,
$$
(e^z)^{n+1}=(e^{z})^n e^z = e^{nz}e^z = e^{nz+z}=e^{z(n+1)}
$$
이다. 따라서,
$$
(\cos \theta +i \sin \theta)^n=(e^{i})^n=e^{in}=\cos n\theta+i\sin n\theta
$$




<b>4. </b> 임의의 복소수 $z$ 에 대하여,
$$
\cosh iz=\cos z,\qquad \sinh iz =i\sin z
$$
임을 보이라.

---

$$
\begin{align}
\cosh iz &= \dfrac{e^{iz}+e^{-iz}}{2}=\dfrac{\cos z+i\sin z + \cos z-i\sin z}{2}=\cos z\,,\\
\sinh iz &= \dfrac{e^{iz}-e^{-iz}}{2}=\dfrac{\cos z +i\sin z-\cos z +i\sin z}{2}=i\sin z\,.
\end{align}
$$





<b>5. </b> 등식
$$
\tanh iz = i \tan z
$$
가 성립하는 복소수 $z$ 를 모두 구하라.

---

$$
\begin{align}
\tanh iz &= \dfrac{\sinh iz}{\cosh iz}= \dfrac{i\sin z}{\cos z}=i\tan z

\end{align}
$$

모든 복소수 $z$ 에 대해 성립한다.



<b>6. </b> 수렴반경이 $r$ 인 멱급수 $\sum a_n x^n$ 에서, 만약 $x>r$ 이면,
$$
\sup \left\{ |a_1 x|,\,|a_2 x^2|,\, |a_3 x^3|,\ldots\right\}=\infty
$$
를 보이라.

---

멱급수 $\sum a_n x^n$ 의 수렴반경이 $r$ 이면,  $x>r$ 일 때,  $\displaystyle \lim_{n \to \infty} |a_n x^n|=\infty$ 라는 뜻이다. $\displaystyle \lim_{n \to \infty} |a_n x^n| = c < \infty$ 임을 가정하자.  $x>y>r$  인 $y$ 를 선택한다. 그렇다면 $\displaystyle |a_n y^n|= |a_n x^n| \left|\dfrac{x}{y}\right|^n$  인데 충분히 큰 $n$ 에 대해 $|a_n y^n|<(c+1)\left(\dfrac{x}{y}\right)^n $ 이며 $0<x/y<1$ 이므로 $\sum a_n y^n$ 은 절대수렴한다. 따라서 $y>r$ 이라는 가정에 위배된다. 즉 $\lim_{n \to \infty} |a_n x^n|=\infty$ 이므로 증명 끝.  



<b>7. </b> (**Hadamard 정리**) 수열 $(a_n)$ 에 대하여,
$$
\limsup_{n \to \infty} (a_n):=\lim_{n \to \infty} \sup \{a_n,\,a_{n+1},\,a_{n+2},\ldots\}
$$
으로 정의한다.  이 때 급수 $\sum a_n x^n$ 의 수렴반경은
$$
\left( \limsup_{n \to \infty} |a_n|^{1/n}\right)^{-1}
$$
임을 보이라.

----

$\displaystyle \rho = \left( \limsup_{n \to \infty} |a_n|^{1/n}\right)^{-1}$ 이라 하자. $|x|<\rho$ 이면 $ \displaystyle 1/|x|> \limsup_{n \to \infty} |a_n|^{1/n}$  이므로 $\displaystyle \limsup_{n \to \infty} |a_n x^n|^{1/n}<1$ 이므로 멱근판정법에 의해 멱급수는 수렴한다. $|x|>\rho$ 이면 역시 멱근판정법에 의해 멱급수가 발산한다.  



<b>8. </b> 다음 미분방정식을 풀어라 (단 $a>0$ 이다.)

---

(1) $\dfrac{dy}{dx}=\dfrac{1}{x^2+a^2}=\dfrac{1}{a^2}\dfrac{1}{(x/a)^2+1} \implies \dfrac{dy}{d(x/a)}=\dfrac{1}{a} \dfrac{1}{(x/a)^2+1} \implies y= \dfrac{1}{a} \arctan \dfrac{x}{a} +\text{const.}$ 

(2) $\dfrac{dy}{dx}=\dfrac{1}{(x^2+a^2)^2}$ 
$$
\begin{align}
y & =\int_0^x \dfrac{1}{(t^2+a^2)^2}\, dt + C= \dfrac{1}{a^3}\int_0^{\arctan (x/a)} \cos^2 \theta d\theta  +C\qquad \qquad &;\theta=a\tan t,\, C=\text{const} \\
&=\dfrac{1}{2a^3} \int_0^{\arctan (x/a)} (\cos 2\theta +1)\,d\theta = \dfrac{1}{4a^3} \left[ \,\sin 2\theta +2\theta\,\right]_{0}^{\arctan(x/a)}+C & \\
&=\dfrac{1}{2a^3} \left[\dfrac{ax}{(x^2+a^2)}+\arctan \left(\dfrac{x}{a}\right)\right] + C

\end{align}
$$
(3) $\dfrac{dy}{dx}=\dfrac{1}{\sqrt{x^2-1}}$ : 연습문제 2.6.10 으로 부터, $y=\cosh^{-1} (x)+\text{const}$

(4) $\dfrac{dy}{dx}=\dfrac{1}{\sqrt{(x-a)(x-b)}} \quad (a<b)$ :  $(x-a)(x-b)=x^2-(a+b)x+ab=\left(x-\dfrac{a+b}{2}\right)^2 -\left(\dfrac{a-b}{2}\right)^2$ 임을 이용한다. $c=\dfrac{a+b}{2},\, d=\dfrac{a-b}{2}$ 라 하면, $\dfrac{dy}{dx}= \dfrac{1}{\sqrt{(x-c)^2-d^2}}=\dfrac{1}{d}\dfrac{1}{\sqrt{(x-c)^2/d^2-1}}$ 이다. $z=(x-c)/d$ 라 하면,
$$
\dfrac{1}{d}\dfrac{1}{\sqrt{z^2-1}}=\dfrac{dy}{dx}=\dfrac{dy}{dz}\dfrac{dz}{dx}=\dfrac{1}{d} \dfrac{dy}{dz}
$$
 이므로 $y=\cosh^{-1}z+\text{const}=\cosh^{-1}\left(\dfrac{x-\dfrac{a+b}{2}}{\dfrac{a-b}{2}}\right) + \text{const}=\cosh^{-1}\left(\dfrac{2x-(a+b)}{(a-b)}\right)+\text{const}.$ 



<b>9. </b> $\displaystyle \int_0^1 \dfrac{dx}{(x^2+1)^2}$ 의 값을 구하라.

---

$$
\begin{align}
\displaystyle \int_0^1 \dfrac{dx}{(x^2+1)^2} &= \int_0^{\pi/4} \cos^2 \theta \, d\theta \qquad\qquad& x=\tan \theta \\
&=\dfrac{1}{2} \int_0^{\pi/4} (\cos 2\theta +1) \, d\theta\\
&=\dfrac{1}{2}\left[\dfrac{1}{2}\sin 2\theta +\theta\right]_0^{\pi/4}\\
&=\dfrac{1}{2} \left(\dfrac{1}{2}+\dfrac{\pi}{4}\right)=\dfrac{1}{4}+\dfrac{\pi}{8}

\end{align}
$$



<b>10. </b> $\displaystyle \int_0^1 \dfrac{2\,dx}{(x+1)(x^2+1)}=\dfrac{1}{2} \ln 2 +\dfrac{\pi}{4}$ 임을 보이라.

---

$$
\begin{align}
\int_0^1 \dfrac{2\,dx}{(x+1)(x^2+1)} &= \int_0^1 \left[\dfrac{1}{x+1}- \dfrac{x}{x^2+1} +\dfrac{1}{x^2+1}  \right]dx \\
&=\left[\ln (x+1) - \dfrac{1}{2}\ln (x^2+1) + \arctan x\right]_0^1\\
&= \ln 2-\dfrac{1}{2}\ln 2+\arctan 1=\dfrac{1}{2}\ln 2 +\dfrac{\pi}{4}

\end{align}
$$





<b>11. </b> 이 문제에서는 탄젠트함수의 갑법정리를 이용하여 원주율 $\pi$ 의 근사값을 효과적으로 구하는 법을 살펴보기로 한다. 우선 등식
$$
\tan (A+B)=\dfrac{\tan A + \tan B}{1-\tan A \tan B}
$$
의 양변에 $\arctan$ 를 씌우면
$$
A+B = \arctan \left(\dfrac{\tan A+\tan B}{1-\tan A \tan B}\right)
$$
를 얻는다. 이제 $A=\arctan a,\, B=\arctan b$  로 두면,
$$
\arctan a + \arctan b = \arctan \left(\dfrac{a+b}{1-ab}\right)
$$
를 얻는다. 예를 들어 위 식에 $a=1/2,\, b=1/3$ 로 두면 $\dfrac{a+b}{1-ab}=1$ 이므로,
$$
\arctan \dfrac{1}{2}+\arctan\dfrac{1}{3}=\dfrac{\pi}{4}
$$
를 얻는다. 한편 86 쪽 식 (2.3) $\displaystyle \left|\arctan x - \sum_{k=0}^n (-1)^k \dfrac{x^{2k+1}}{2k+1}\right| \le \dfrac{x^{2n+3}}{2n+3}$  에서,
$$
\left|R_4 \left(\dfrac{1}{2}\right) \right| \le \dfrac{1}{5 \cdot 2^5} \, \qquad \left| R_4 \left( \dfrac{1} {3}\right)\right| \le \dfrac{1}{5\cdot 3^5} = \dfrac{1}{1215} \le 10^{-3}
$$
을 얻고, 따라서,
$$
\begin{align}
4 \cdot \arctan \dfrac{1}{2} &\approx  4 \left( \dfrac{1}{2}-\dfrac{1}{3}\left(\dfrac{1}{2}\right)^2  \pm \dfrac{1}{160}\right) = (2-0.1{\dot{6}}) \pm \dfrac{1}{40} = 1.8\dot{3}\pm 2.5 \times 10^{-2}\\
4 \cdot \arctan \dfrac{1}{3} &\approx 4 \left( \dfrac{1}{3}-\dfrac{1}{3} \left(\dfrac{1}{3}\right)^2 \pm 10^{-3}  \right)= \dfrac{4}{3} \left(1-\dfrac{1}{27}\right) \pm 0.4 \times 10^{-2} \approx 1.28 \pm 0.8 \times 10^{-2}
\end{align}
$$ {}}
가 된다. 이를 이용하여,
$$
\pi = 4\left(\arctan \dfrac{1}{2}+\arctan \dfrac{1}{3}\right) \approx 3.11\dot{3}\pm 3.3 \times 10^{-2}
$$
를 보이라.

---

$$
\begin{align}
\pi &= 4 \left(\arctan \dfrac{1}{2}+\arctan{1}{3}\right) \\
&\approx 1.8\dot{3} \pm 2.5 \times 10^{-2} + 1.28 \pm 0.8 \times 10^{-2}\\
&= 3.11\dot{3} \pm 3.3\times 10^{-2}
\end{align}
$$



<b>12. </b> 다음 등식을 보이라.

---

(1) $\arctan 1 + \arctan 2 + \arctan 3 = \pi$ 

from text, $\arctan a+\arctan b = \arctan \left( \dfrac{a+b}{1-ab}\right)$. Let $a=1,\, b=2$. Then, $\arctan 1 + \arctan 2 = \arctan (-3)=\pi - \arctan 3$  because $\pi/2 < 3 <\pi$.   따라서 $\arctan 1 + \arctan 2 +\arctan 3 = \pi$. 

(2) (Machin 등식) $\dfrac{\pi}{4} = 4 \arctan \dfrac{1}{5} - \arctan \dfrac{1}{239}$ 
$$
\begin{align}
4 \arctan \dfrac{1}{5} &=\arctan \dfrac{1}{5}+\arctan\dfrac{1}{5}+\arctan \dfrac{1}{5}+\arctan\dfrac{1}{5} \\
&= \arctan\dfrac{5}{12} + \arctan \dfrac{5}{12} = \arctan \dfrac{120}{119} \\
4\arctan \dfrac{1}{5}-\arctan \dfrac{1}{239} &=\arctan \dfrac{120}{119} - \arctan\dfrac{1}{239} \\
&= \arctan \left(\dfrac{\dfrac{120}{119}-\dfrac{1}{239}}{1+ \dfrac{120}{119}\dfrac{1}{239}}\right) = \arctan(1) = \dfrac{\pi}{4}
\end{align}
$$
(3) (**가우스 등식**) : $\dfrac{\pi}{4} = 12 \arctan \dfrac{1}{18} + 8 \arctan\dfrac{1}{57} - 5 \arctan\dfrac{1}{239}$
$$
\begin{align}
2 \arctan a &= \arctan\dfrac{2a}{1-a^2}\\
3 \arctan a &= \arctan a + 2\arctan a = \arctan \dfrac{3a-a^3}{1-3a^2}\\
4 \arctan a &=\arctan \dfrac{4a(1-a^2)}{a^4-6a^2+1}
\end{align}
$$
를 이용하여 계산하면,
$$
\begin{align}
12 \arctan \dfrac{1}{18} &= \arctan \left(\dfrac{728,065,260,080,136}{926,604,049,600,873}\right)\,,\\
8 \arctan \dfrac{1}{57} &= \arctan \left(\dfrac{975,343,472,544}{6,904,349,713,633} \right)\,,\\
5 \arctan \dfrac{1}{239} &=\arctan \left(\dfrac{4,078,367,999}{194,918,686,801} \right)\,,\\
12 \arctan \dfrac{1}{8} + 8 \arctan\dfrac{1}{57} &= \arctan \left(\dfrac{99,498,527,400}{95,420,159,401}\right)\,,\\
12 \arctan \dfrac{1}{18} + 8 \arctan\dfrac{1}{57} - 5 \arctan\dfrac{1}{239} &= \arctan (1) = \dfrac{\pi}{4}\;.

\end{align}
$$


(4) (샹크스 등식) : $\dfrac{\pi}{4} = 6 \arctan \dfrac{1}{8} + 2 \arctan \dfrac{1}{57} + \arctan \dfrac{1}{239}$ :
$$
\begin{align}
6 \arctan\dfrac{1}{8} &= \arctan \left(\dfrac{186,416}{201,663}\right) \,,\\
2 \arctan \dfrac{1}{57} &= \arctan \left( \dfrac{57}{1,624}\right)\,,\\
6 \arctan\dfrac{1}{8} +2 \arctan \dfrac{1}{57} &= \arctan \left(\dfrac{119}{120}\right)\,,\\
6 \arctan \dfrac{1}{8} + 2 \arctan \dfrac{1}{57} + \arctan \dfrac{1}{239} &= \arctan(1) = \dfrac{\pi}{4}\,.


\end{align}
$$


<b>13. </b> 다음 등식을 보이라.
$$
\begin{align}
\pi &= \sum_{k=0}^\infty \dfrac{(-1)^k}{4^k} \left( \dfrac{2}{4k+1}+\dfrac{2}{4k+2} + \dfrac{1}{4k+3}\right) \\
&=\sum_{k=0}^\infty \dfrac{1}{16^k} \left(\dfrac{4}{8k+1} -\dfrac{2}{8k+2}- \dfrac{1}{8k+5} - \dfrac{1}{8k+6}\right)

\end{align}
$$

---

--to be done--







