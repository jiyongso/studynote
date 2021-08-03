IX. 곡선 #2
===

## 연습문제 : 제 9 장 8 절



<b>1. </b> 정규곡선 $X(t)\in \mathbb{R}^3$ 에 대하여
$$
\dfrac{d}{dt} |X'(t)| = \dfrac{X'(t) \cdot X''(t)}{|X'(t)|}
$$
를 유도하고, 이로부터
$$
\kappa:= \dfrac{\sqrt{|X'|^2|X''|^2-(X'\cdot X'')^2}}{|X'|^3} = \dfrac{|X' \times X''|}{|X'|^3}
$$
을 유도하라. 이때 벡터 $X'$ 과 $X''$ 이 이루는 각의 크기를 $\alpha$ 라고 두면
$$
\kappa = \dfrac{|X''||\sin \alpha|}{|X'|^2}
$$
임을 보이라.

----

$$
\dfrac{d}{dt}|X'(t)|=\dfrac{d}{dt} \sqrt{\sum_{i=1}^3 (x_i' (t))^2}=\dfrac{\sum_{i=1}^3 x'_i (t) x''_i(t)}{\sqrt{\sum_{i=1}^3(x_i'(t))^2}}=\dfrac{X'(t) \cdot X''(t)}{|X'(t)|}
$$

이다. 
$$
\begin{align}
\left(\dfrac{X'}{|X'|}\right)' &=\dfrac{X''|X'|-X'|X'|'}{|X'|^2} =\dfrac{X''|X'|^2-X'(X' \cdot X'')}{|X'|^3} = \dfrac{X' \times (X'' \times X')}{|X'|^3} \\
\kappa &=\dfrac{1}{|X'|}\left|\left(\dfrac{X'}{|X'|}\right)'\right|= \dfrac{1}{|X'|}\dfrac{|X'\times (X'' \times X')|}{|X'|^3}=\dfrac{|X'\times X''|}{|X'|^3}
\end{align}
$$
여기서 우리는 $\mathbf{a} \times (\mathbf{b} \times \mathbf{c})=\mathbf{b}(\mathbf{a}\cdot \mathbf{c})+\mathbf{c}(\mathbf{a}\cdot \mathbf{b})$ 와 $|\mathbf{a} \times (\mathbf{b}\times \mathbf{a})|=|\mathbf{a}||\mathbf{a}\times \mathbf{b}|$ 임을 이용하였다. 

$X'$ 과 $X''$ 이 이루는 각의 크기를 $\alpha$ 라고 두면
$$
\kappa = \dfrac{|X''||\sin \alpha|}{|X'|^2}
$$
임은 쉽다.





<b>2. </b> 평면곡선 $X(t) = (x(t),\, y(t))$ 의 곡률은
$$
\kappa (t) = \dfrac{|x'(t)y''(t)-x''(t)y'(t)|}{((x'(t))^2+(y'(t))^2)^{3/2}}
$$
임을 보이라. 또 평면곡선 $y=f(x)$ 의 곡률은
$$
\kappa (x) = \dfrac{|y''|}{(1+y'^2)^{3/2}}
$$
임을 보이라.

---

문제 1로부터,
$$
\kappa = \dfrac{\sqrt{|X'|^2|X''|^2-(X'\cdot X'')^2}}{|X'|^3}=\dfrac{\sqrt{(x'^2+y'^2)(x''^2+y''^2)-(x'x''-y'y'')^2}}{(x'^2+y'^2)^{3/2}} = \dfrac{|x'y''-x''y'|}{(x'^2+y'^2)^{3/2}} 
$$
이며 $x(t)=t$ 로 놓으면,
$$
\kappa =\dfrac{|y''|}{(1+y'^2)^{3/2}}
$$
이다.



<b>3. </b> 타원 $X(t)=(a\cos t,\, b \sin t)$ 의 각 점에서의 곡률을 구하라. ($a,\,b>0$ 이다.)

---

$$
\begin{align}
X'(t) &=(-a \sin t,\, b \cos t)\\
X''(t) &=(-a \cos t,\, -b \sin t)\\
\kappa &=\dfrac{|ab\sin^2 t+ab\cos^2 t|}{(a^2\sin^2t + b^2 \cos ^2 t)^{3/2}}=\dfrac{ab}{(a^2\sin^2t + b^2 \cos ^2 t)^{3/2}}
\end{align}
$$



<b>4. </b> 좌표평면에서 포물선 $y=x^2$ 의 각 점에서의 곡률을 구하라.

---

문제 2. 로 부터,
$$
\kappa = \dfrac{|y''|}{(1+y'^2)^{3/2}}=\dfrac{2}{(1+4x^2)^{3/2}}
$$


<b>5. </b> 좌표평면에서 포물선 $y=ax^2$ 상의 세 점 $(-t,\,at^2),\, (0,\,0),\, (t,\,at^2)$ 을 지나는 원의 반지름의 길이를 $r(t)$ 라 두었을 때, $\displaystyle \lim_{t \to 0} r(t)$ 의 값을 구하라.

----

대칭에 의해 원의 중심은 $y$ 축상에 있으니 이를 $(0,\,y)$ 라 하면,  $y>0$ 이어야 하며, $r(t)=y$ 이고,
$$
y^2=t^2+(y-at^2)^2 \implies y=\dfrac{1+a^2t^2}{2a}
$$
이다. 따라서 $\displaystyle \lim_{t\to 0} r(t)=\dfrac{1}{2a}$ 이다.



<b>6. </b> 좌표공간에서 곡선 $X(t)$ 의 곡률이 $\kappa (t)$ 일 때, 곡선 $Y(t):=c X(t)$ 의 곡률은 $\kappa(t)/c$ 임을 보이라. (단 $c>0$.)

---

$Y=cX$ 이므로 $Y'=cX',\, Y'' = cX''$ 이다. 따라서, 
$$
\kappa_Y (t) = \dfrac{1}{|Y'|}\left|\left(\dfrac{Y'}{|Y'|}\right)'\right|=\dfrac{1}{c} \kappa (t)
$$


<b>7. </b> 곡선 $X(t)=(t,\, t^2,\,t^3)$ 에서 $t=1,\, t=-1$ 일 때의 곡률을 구하라.

---

$$
\begin{align}
X'(t)&=(1,\,2t,\,3t^2)\\
X''(t)&=(0,\,2,\,6t)\\
\kappa(t) &= \dfrac{|X'\times X''| }{|X'|^3}=\dfrac{2\sqrt{9t^2+9t+1}}{(9t^4+4t^2+1)^{3/2}}\\
\kappa(1) &=\dfrac{2\sqrt{19}}{14\sqrt{14}}\\
\kappa(-1)&=\dfrac{2}{14\sqrt{14}}

\end{align}
$$



<b>8. </b> 곡선 $X(t)=(t,\, \ln t)$ 에서 곡률반경이 최소인 점을 구하라.

---

$$
\begin{align}
\kappa(t) &= \dfrac{1/t^2}{(1+1/t^2)^{3/2}}=\dfrac{t}{(t^2+1)^{3/2}}\\
\kappa'(t) &=\dfrac{1-2t^2}{(1+t^2)^{5/2}}  \implies \left(\kappa'(t)=0 \iff t^2=\dfrac{1}{2}\right)\\
\lim_{t \to 0} \kappa (t) &= +\infty \\
\kappa(t=1/\sqrt{2})&= \dfrac{2\sqrt{3}}{9} \\
X\left( \dfrac{1}{\sqrt{2}}\right) & =\left( \dfrac{1}{\sqrt{2}},\, -\dfrac{1}{2} \ln 2 \right) 

\end{align}
$$





<b>9.</b>  사이클로이드
$$
x(t)=t-\sin t,\quad y(t)=1-\cos t = 2\sin^2 \dfrac{t}{2} \quad (0\le t \le 2\pi)
$$
의 곡률은
$$
\kappa (t) = \dfrac{1}{4\sin \dfrac{t}{2}} =\dfrac{\sqrt{2}}{4\sqrt{y}}
$$
임을 보이라.

---

$\sin \dfrac{t}{2}\ge 0$ for $0 \le t \le 2\pi$ 이다. 
$$
\begin{align}
X(t) &= (t-\sin t,\, 1-\cos t)\\
X'(t) &= (1-\cos t,\, \sin t)\\
X''(t) &= (\sin t,\, \cos t)\\
\kappa(t)&= \dfrac{|X' \times X''|}{|X'|^3}=\dfrac{2\sin^2 \dfrac{t}{2}}{8 \sin^3 \dfrac{t}{2}}=\dfrac{1}{4 \sin \dfrac{t}{2}}=\dfrac{\sqrt{2}}{4 \sqrt{y}}
\end{align}
$$


<b>10. </b> 곡선
$$
X(t)=\left(\int_0^t \cos \dfrac{\pi u^2}{2}\, du ,\, \int_0^t \sin \dfrac{\pi u^2}{2} \, du\right)
$$
의 곡률을 구하라.

---

$$
\begin{align}
X'(t) &= \left(\cos \dfrac{\pi t^2}{2} ,\sin \dfrac{\pi t^2}{2} \right) \\
X''(t) &= \left( -\pi t \sin \dfrac{\pi t^2}{2},\,  \pi t \cos \dfrac{\pi t^2}{2} \right)\\
|X'(t)|^2&= 1 \\
\kappa(t) &= \pi t 

\end{align}
$$



<b>11. </b> 곡선 $X(t)$ 의 곡률 $\kappa (t)$ 의 적분 $\displaystyle \int_X \kappa \,ds$  를 $X$ 의 전곡률(total curvature) 라고 한다. 타원 $x^2+4y^2=1$ 의 전곡률은 얼마인가.

---

$$
\begin{align}
X(t) &=\left( \cos t,\, \dfrac{1}{2} \sin t \right) \\
X'(t)&= \left(-\sin t,\, \dfrac{1}{2} \cos t \right) \\
X''(t) &= \left(-\cos t,\, -\dfrac{1}{2} \sin t\right) \\
\kappa (t) &= \dfrac{\dfrac{1}{2}\sin^2 t + \dfrac{1}{2}\cos^2 t}{(\sin^2 t+\cos^2t/4 )^{3/2}} = \dfrac{1/2}{(\sin^2 t + \cos^2 t/4)^{3/2}}\\
\int_X \kappa \, ds &=\int_0^{2\pi} \kappa(t) |X'(t)| dt = \int_0^{2\pi} \dfrac{2}{4\sin^2 t+ \cos ^2 t}\, dt 
\end{align}
$$

이 때,
$$
\begin{align}
\int_\pi^{2\pi} \dfrac{2}{4\sin^2 t +\cos ^2 t}\, dt& \overset{s=2\pi-t}{=} \int_0^{\pi} \dfrac{2}{4 \sin^2 s + \cos^2 s}\, ds\\
\int_{\pi/2}^{\pi} \dfrac{2}{4\sin^2 t +\cos ^2 t}\, dt& \overset{s=\pi-t}{=}\int_0^{\pi/2} \dfrac{2}{4 \sin^2 s + \cos^2 s}\, ds

\end{align}
$$
이므로,
$$
\begin{aligned}
\int_X \kappa \, ds &= 4 \int_0^{\pi/2} \dfrac{2}{4 \sin^2 t+  \cos^2 t}\, dt = \int_0^{\pi/2} \dfrac{8}{4 \tan^2 t+1} \dfrac{1}{\cos^2t}\, dt  \\
&\overset{s=\tan t}{=} \int_0^\infty \dfrac{8}{4s^2+1}ds  \overset{s=(\tan \theta)/2}{=} \int_0^{\pi/2} 4 \, d\theta = 2\pi
\end{aligned}
$$




<b>12. </b> 좌표평면상의 정규곡선 $X:[a,\,b]\to \mathbb{R}^2$ 에 대하여,
$$
\dfrac{X'(t)}{|X'(t)|} = (\cos \theta(t),\, \sin \theta(t)) \qquad (a \le t \le b)
$$
로 두면 $X$ 의 전곡률은
$$
\int_X \kappa \, ds = \int_a^b |\theta'(t)|\, dt
$$
임을 보이라. 특히 $\theta(t)$ 가 증가함수이면
$$
\int_X \kappa \, ds.= \theta(b)-\theta(a)
$$
임을 보이라.

---

$$
\int_X \kappa \, ds = \int_a^b \dfrac{1}{|X'|}\left|\left(\dfrac{X'}{|X'|}\right)'\right|\, |X'|\, dt = \int_a^b \left|\left(\dfrac{X'}{|X'|}\right)'\right| \, dt = \int_a^b|\theta'(t)(-\sin \theta(t),\, \cos \theta(t))|\, dt=\int_a^b |\theta'(t)|\, dt
$$

$\theta(t)$ 가 증가함수이면 $\theta'(t)>0$ 이다. 따라서,
$$
\int_X \kappa \, ds = \int_a^b \theta'(t)\, dt = \theta(b)-\theta(a)
$$


<b>13. </b> 차를 몰고 반지름의 길이가 100 미터인 원호 모양의 도로 위를 일정한 속력 $v$ 로 움직일 때 편안함을 느낀다고 하자. 반지름의 길이가 10 미터인 원호 모양의 도로 위를 움직일 때의 속력이 얼마이면 같은 정도의 편안함을 느끼는가?

---

반지름의 길이가 $R$ 미터인 원호를 일정한 속력 $v$ 로 움직일 때의 경로 $X(t)$ 는
$$
\begin{align}
X(t) &= R (\cos \dfrac{vt}{R},\, \sin \dfrac{vt}{R})\\
X'(t) &= v(-\sin \dfrac{vt}{R},\, \cos \dfrac{vt}{R})\\
|X'(t)|&=v\\
X''(t) &= -\dfrac{v^2}{R}(\cos \dfrac{vt}{R},\, \sin \dfrac{vt}{R})
\end{align}
$$
이며 가속력의 크기는 $\dfrac{v^2}{R}$ 이다. 같은 정도의 편안함을 느끼려면 가속력이 같아야 하므로, 반지름이 $1/10$ 이 되면 속력은 $1/\sqrt{10}$ 이 되어야 한다.



<b>14. </b> 호의 길이로 매개화된 곡선 $X(s)$ 의 곡률이 $\kappa (s)$ 로 주어졌을 때 $\kappa'(s)=0$ 이 되는 점을 **꼭지점** 이라고 부른다. 타원
$$
\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}=1
$$
의 꼭지점을 구하라.

---

(1) 일단 처음 생각대로 해보면....
$$
\begin{align}
X(t) &= (a \cos t,\, b \sin t)\\
X'(t) &= (-a \sin t,\, b \cos t ) \\
|X'(t) |&=\sqrt{a^2 \sin^2 t+ b^2 \cos^2 t}\\
X''(t) &=(-a \cos t,\, - b \sin t)


\end{align}
$$

 이므로 $|X'(t)|>0\;\forall t\in \mathbb{R}$ 이다. 호의 길이로 매개화하면,
$$
s(t)=\int_0^t |X'(t')|\,dt'=\int_0^t\sqrt{a^2 \sin^2 t'+ b^2 \cos^2 t'}\, dt'
$$
인데..<u>이거 적분으로 어쩌구 하려면 잘 안된다.</u> 이렇게 하지 말고,

(2) 정규곡선 $X(t)$ 를 호의 길이로 매개화한 곡선을 $Y(s)$ 라 하자. 즉 $s=s(t)=\displaystyle \int_0^t |X'(t')|\, dt'$ 이며 $t=g(s)$ 라 할 때 $Y(s)=X(g(s))$ 이다. 

이제 $Y$ 의 꼭지점은 $Y$ 의 곡률 $\kappa_Y(s)$ 에 대해
$$
\dfrac{d}{ds}\kappa_Y (s)=\dfrac{d}{ds}|Y''(s)|
$$
 이 되는 점 이며, $X(t)$ 의 곡률을 $\kappa_X(t)$ 라 할 때, 
$$
\begin{align}
Y(s) &=X(g(s)) \\
Y'(s) &= \dfrac{dg}{ds} \cdot \dfrac{d X}{dt}(g(s))\\
Y''(s) &= \dfrac{d^2 g}{ds^2}\cdot \dfrac{dX}{dt}(g(s)) + \left(\dfrac{dg}{ds}\right)^2 \cdot \dfrac{d^2X}{dt^2}(g(s))


\end{align}
$$
이 때 문제 1 로 부터, $|Y'|=1$ 을 이용하면, 
$$
\kappa_Y(s)=\dfrac{|Y' \times Y''|}{|Y'|^3}=\left|\left(\dfrac{dg}{ds}\right)^3\right| \left|X'(g(s))\times X''(g(s))\right|
$$
우리는 $t=g(s)$ 이며 $g^{-1}(t) = s =\int_0^t |X'(t')|\, dt$ 임을 알고 있다. 역함수의 미분으로 부터 $\dfrac{dg}{ds}=\dfrac{1}{X'}(g(s))$ 임을 알고 있다. 따라서,
$$
\kappa_Y (s) = \dfrac{|X'(g(s))\times X''(g(s))|}{|X'(g(s))|^3}=\kappa_X (g(s))
$$
이다. 따라서,
$$
\dfrac{d}{ds}\kappa_Y(s)=0 \implies \dfrac{dg(s)}{ds}=0 \text{ or } \dfrac{d\kappa_X}{dt}(t)=0
$$
이다. 그런데 $g'(x)>0$ 이므로 $\kappa_X'(t)=0$  뿐이다. 
$$
\begin{align}
\kappa_X (t)&= \dfrac{|X'\times X''|}{|X'|^3} = \dfrac{|ab|}{(a^2 \sin^2 t + b^2 \cos^2 t)^{3/2}}\\
\kappa_X'(t) &= \dfrac{-3|ab|\sin t \cos t (a^2-b^2)}{(a^2 \sin^2 t + b^2 \cos^2 t)^{5/2}}
\end{align}
$$
이므로 $\kappa'_X(t)=0$ 이면 $t=0,\, \pi/2,\, \pi/\, \pi/3$ 이다. 즉 $(\pm a,\,0)$ 과 $(0,\, \pm b)$ 가 꼭지점이다.



<b>15. </b> 곡선 
$$
X(t) = \left(\cos t,\, \sin^2 t,\, \dfrac{1}{2} \sin 2t\right)
$$
에서 $t=\pi$ 일 때의 곡률과 접촉평면의 식을 구하라.

---

$$
\begin{align}
X'(t) &= \left(-\sin t,\, \sin 2t,\, \cos 2t\right)\\
X''(t) &= \left(- \cos t,\, 2 \cos 2t,\, -2 \sin 2t\right)\\
|X'(t) | &=\sqrt{1+\sin^2 t}\\
\kappa(t) &=\dfrac{\sqrt{4 + \cos^2 t+ 4 \sin^2 t -8 \sin t \cos t \sin 2t \cos 2t}}{(1+\sin^2t)^{3/2}} \\
X(\pi) &= (-1,\, 0,\, 0)\\
X'(\pi)&=(0,\, 0,\, 1)\\
X''(\pi)&=(1,\, 2,\, 0) \\
\kappa (\pi) &=\sqrt{5}
\end{align}
$$

접촉평면의 식은
$$
0 = \det \begin{pmatrix}  x+1 & y & z \\ 0 & 0 & 1 \\ 1 & 2 & 0\end{pmatrix} =-2(x+1)+y \implies 2x-y+2=0
$$
이다. 



<b>16. </b> 삼차원 공간에서 곡률이 항등적으로 $0$ 인 정규곡선은 직선운동을 하는 곡선임을 보이라.

---

문제 1로부터, 곡률이 항등적으로 $0$ 이면
$$
0=\kappa = \dfrac{|X'\times X''|}{|X'|^3} \implies X'\times X''=0
$$
이다. $X'(t)\ne 0$ 이므로 $X''(t) = f(t)X'(t)$ 이며 연습문제 9.2.2 로부터 $X(t)$ 는 직선운동임을 안다.



<b>17.</b> 곡선 $X(t)=e^t(\cos t,\, \sin t)$ 의 곡률함수를 구하라.

---

$$
\begin{align}
X'(t) &= e^t(\cos t- \sin t,\, \sin t + \cos t)\\
X''(t) &=e^t(-2\sin t,\, 2 \cos t) \\
\kappa(t) &= \dfrac{2e^{2t}}{|2e^{2t}|^{3/2}}=\dfrac{1}{\sqrt{2}e^t}
 
 \end{align}
$$





<b>18. </b> 로그와선 $r=r_0 e^{k\theta}$ 의 각 점에서의 곡률은
$$
\kappa = \dfrac{1}{r} \dfrac{1}{\sqrt{1+k^2}}
$$
임을 보이라. 이로부터 로그와선의 곡률은 원점에서의 거리에 반비례함을 설명하라.

---

$$
\begin{align}
X(\theta) &= r_0 e^{k\theta}(\cos \theta,\,\sin \theta)\\
X'(\theta) &=r_0 e^{k\theta}(k\cos \theta-\sin \theta,\, k\sin \theta + \cos \theta)
\\
X''(\theta) &= r_0 e^{k \theta}((k^2-1) \cos \theta - 2k \sin \theta ,\,(k^2 -1)\sin \theta + 2k\cos \theta ) \\
|X'(\theta)| &=r_0 e^{k\theta}\sqrt{k^2+1}\\
|X' \times X''| &= r_0^2 e^{2k\theta} (k^2+1)\\
\kappa(\theta) &= \dfrac{|X'\times X''|}{|X'|^{3}}= \dfrac{r_0^2e^{2k\theta}(k^2+1)}{r_0^3 e^{3k\theta} (k^2+1)^{3/2} }=\dfrac{1}{r_0e^{k\theta}}\dfrac{1}{\sqrt{k^2+1}}=\dfrac{1}{r} \dfrac{1}{\sqrt{k^2+1}}


\end{align}
$$

$k$ 는 상수이므로 $k(\theta) \propto \dfrac{1}{r}$ .





## 제 9 장 탐구문제



<b>1. </b> 한 변의 길이가 $1$ m 인 정사각형 모양 탁지의 각 귀퉁이에 개미가 한마리씩 있다. 이들 개미가 각자 자기 왼쪽에 있는 개미를 향하여 동시에 같은 속력으로 움직이면 그 자취는 로그와선이 된다. 이 때 개미들이 만날 때가지 움직인 거리를 구하라.

---

$A,\,B,\,C,\,D$ 에서 출발한 개미의 자취를 $A(t),\, B(t),\, C(t),\, D(t)$ 라 하자. $A$ 는 $B$ 를 따라, $B$ 는 $C$ 를 따라, $C$ 는 $D$ 를 따라, $D$ 는 $A$ 를 따라 움직인다고 하자. 그렇다면,
$$
\begin{align}
A'(t) &= v\dfrac{B(t)-A(t)}{|B(t)-A(t)|}\\
B'(t) &= v\dfrac{C(t)-B(t)}{|C(t)-B(t)|}\\
C'(t) &= v \dfrac{D(t)-C(t)}{|D(t)-C(t)|}\\
D'(t) &=  v\dfrac{A(t)-D(t)}{|A(t)-D(t)|}\\
A(0) &= \left( -\dfrac{1}{2},\, \dfrac{1}{2}\right)\\
B(0) &=  \left( \dfrac{1}{2},\, \dfrac{1}{2}\right)\\
C(0) &=  \left( \dfrac{1}{2},\, -\dfrac{1}{2}\right)\\
D(0) &=  \left( -\dfrac{1}{2},\, -\dfrac{1}{2}\right)
\end{align}
$$
$A(t)=(x(t),\, y(t))$ 라 하자. $A,\,B,\,C,\,D$ 의 대칭성으로부터, $B(t)$ 는 $A$ 를 시계방향으로 $\pi/2$ 만큼 $C(t)$ 는 $\pi$ 만큼, $D(t)$ 는 $3\pi/2$ 만큼 회전한 것임을 알 수 있다. 따라서,
$$
A(t)=(x(t),\, y(t)), \quad B(t)=(y(t),\, -x(t)),\quad C(t) = (-x(t),\, -y(t)),\quad D(t) = (-y(t),\, x(t))
$$
이며 $x(0)=-1/2,\, y(0)=1/2$ 임을 안다. 그렇다면,
$$
\begin{align}
x'(t)=v\dfrac{y-x}{\sqrt{(y-x)^2+(x+y)^2}}=v\dfrac{y-x}{\sqrt{2}r},\qquad y'(t) =-v\dfrac{x+y}{\sqrt{2}r}

\end{align}
$$
이다. 
$$
v^2=\left(\dfrac{dx}{dt}\right)^2+\left(\dfrac{dy}{dt}\right)^2 = \left(\dfrac{dr}{dt}\right)^2+ r^2 \left(\dfrac{d\theta}{dt}\right)^2 = \dot{r}^2+r^2\dot{\theta}^2
$$


이다. (물리학에서 많이 쓰는 시간에 대한 미분을 문자 위의 도트로 쓰는 표현을 사용하였다.) 이 곡선이 로그와선을 이루므로 
$$
r(t) = r_0 e^{k\theta(t)}
$$
로 놓을 수 있는데, 우선 $\theta (0)=\dfrac{3\pi}{4}$ 이며 $r(0)=\dfrac{1}{\sqrt{2}}$ 이다. 또한 $\dfrac{d\theta}{dt}<0$ 이며 $\dfrac{dr}{dt}<0$ 이므로 $k>0$ 이다. 
$$
\dot{r}=r_0 (k\dot{\theta})e^{k\theta(t)}=k\dot{\theta}r
$$


- 속력이 일정한가?

-- to be done--



<b>2. </b> 평면에서 곡선 $X(t)$ 와 한 점 $P$ 가 주어졌다고 하자. 만약 $Q:=X(0)$ 가 곡선 $X(t)$ 의 점 중에서 $P$ 에 가장 가까운 거리에 있으면 벡터 $\overrightarrow{PQ}$ 와 $X'(0)$ 은 서로 수직임을 보이라. 또 두 평면곡선 $x^2y+y^3=8$ 과 $x^2+y^2=1$ 사이의 최단거리를 구하라.

---

$t\in \mathbb{R}$ 이라고 가정한다. 원점에서의 거리의 제곱 함수를 $L(t)$ 라 하면,
$$
L(t)=|X(t)-P|^2
$$
이다 원점에서 가장 가까운 거리가 $t=0$ 일 때 이면 ,
$$
L'(0)=X'(0)\cdot (X(0)-P)=0 \implies X'(0)\cdot (Q-P)=0
$$
이므로 $X'(0)$ 과 $\overrightarrow{PQ}$ 는 수직이다. 

두 평면곡선 $x^2y+y^3=8$ 과 $x^2+y^2=1$ 사이의 최단거리를 구하자. 만약 두 곡선이 교점이 없으면 원점에서의 최단거리에서 $1$ 을 빼주면 된다. 두 점의 교점이 존재한다면 $x=\cos \theta,\, y = \sin \theta$ 로 놓았을 때 두 식을 만족하는 $\theta$ 가 존재해야 한다. 그러나,
$$
8=x^2y+y^3=\cos^2 \theta \sin \theta + \sin ^3 \theta =  \sin \theta\le 1
$$
이므로 모순. 따라서 교점이 존재하지 않는다.  $x^2y+y^3=8$ 을 정리하면,
$$
x^2= \dfrac{8-y^3}{y}
$$
이며 $(8-y^3)/y=x^2\ge 0$ 이어야 하므로, $ 0<y\le 2$ 에서만 존재한다. 이 곡선은
$$
X(t) = \left(\sqrt{\dfrac{8-t^3}{t}},\, t\right)\qquad 0<t\le 2
$$
로 매개화 할 수 있으며, 원점에서의 거리는, $8/t$ 이므로 최단거리는 $4$ 이다. 따라서 $x^2+y^2=1$ 와의 최단거리는 $3$ 이다. 



<b>3. </b> 극좌표계로,
$$
r=\dfrac{k\epsilon}{1+\epsilon \cos \theta}
$$
로 주어진 곡선은

(i) $0<\epsilon < 1$ 이면 타원

(ii) $\epsilon =1$ 이면 포물선

(iii) $\epsilon>1$ 이면 쌍곡선을 나타냄을 보이라.

----

$$
\sqrt{x^2+y^2}=\dfrac{k\epsilon}{1+\epsilon \dfrac{x}{\sqrt{x^2+y^2}}} \implies (1-\epsilon)x^2-2\epsilon kx + y^2 = \epsilon k^2
$$

이다. 

이므로 $0 <\epsilon <1$ 이면 타원, $\epsilon = 1$ 이면 포물선, $\epsilon>1$ 이면 쌍곡선이다.



<b>4. </b> 일급 곡선 $X:[a,\,b]\to \mathbb{R}^n$ 의 에너지를
$$
E(X):=\int_a^b |X'(t)|^2\, dt
$$
로 정의한다.

이 때,
$$
\dfrac{(\text{length}(X))^2}{b-a} \le E(X)
$$
를 보이라. 

이제 공간에 주어진 두 점 $P,\,Q$ 를 잇는 모든 일급곡선중에서 에너지가 최소인 곡선은 등속운동을 하는 직선임을 보이라.

---

임의의 실수함수 $f,\, g$ 에 대해 
$$
\left(\int f(t)g(t)\, dt\right)^2 \le \int f(t)^2\, dt \int g(t)^2\, dt
$$
임을 보이자. 
$$
0 \le \int (f(t)-\lambda g(t))^2 \, dt  = \int f(t)^2\, dt -2 \lambda \int f(t) g(t)\, dt + \lambda^2 \int g(t)^2\, dt
$$
는 $\lambda$ 와 무관하게 항상 성립해야 한다. 따라서, (2차함수의 판별식을 이용하면) 위의 식이 성립하며 등호는 $f(t)$ 가 $g(t)$ 의 상수배일 때 성립한다. 

이제 $f(t)=1,\, g(t) = |X'(t)|$ 를 대입하고 $(a,\,b)$ 구간에서 적분하면,
$$
(b-a)\int|X'(t)|^2\, dt \le \left(\int|X'(t)|\, dt\right)^2 = \text{length(X)}^2
$$
이므로, 주어진 식을 보였다. 등호는 $|X'(t)|=v=\text{const}$ 일 때 이므로 등속운동을 할 때 성립하며, 두 점을 잇는 가장 짧은 곡선은 직선이다.





