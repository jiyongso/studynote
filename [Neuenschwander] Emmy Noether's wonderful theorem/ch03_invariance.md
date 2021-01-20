III. Invariance
===



## 3.1 Formal Definition of Invariance



#### Continuous transformation 

Continuous parameter $\varepsilon$ 을 생각하자. $\varepsilon$ 이 $0$ 부터 변화할 수 있으며 $\varepsilon=0$ 일 때 identity transformation 이 되도록 한다.

<b>Note : </b> Noether's theorem은 continuous transformations 만을 다룬다.



이 변환에 대해 original independent parameter $t$가 $t'$으로, generalized dependent variables $q^\mu$ 가 ${q^\mu}'$ 으로 바뀌면서 새로운 independent & dependent variables 가 된다고 하자. 즉,
$$
\begin{align*}
t\to t' &=T(t,\,q^\mu,\,\varepsilon) \,,\\
q^\mu \to {q^\mu}'&=Q^\mu (t,\,q^\nu,\,\varepsilon)\,. 

\end{align*}\tag{3.1.1}
$$

<b>Example 1: Rotation along $z$-axis in 3D Euclidean  space</b> 
$$
\begin{align*}
x'&=x \cos \varepsilon + y \sin \varepsilon\,,\\
y'&=-x \sin \varepsilon + y \cos \varepsilon\,,\\
z'&=z

\end{align*} \tag{3.1.2}
$$
<b>Example 2: Lorentz transformation</b> (with $c=1$)
$$
\begin{align*}
t'&=\gamma (t-vx)\,,\\
x'&=\gamma(x-vt)\,,\\
y'&=y\,,\\
z'&=z\;.

\end{align*}\tag{3.1.3}
$$
<b>Example 3: Length functional in xy plane</b>
$$
\begin{align*}
s&=\int_a^b \sqrt{1+\left(\dfrac{dy}{dx}\right)^2} \,dx\\
s'&=\int_{a'}^{b'}\sqrt{1+\left(\dfrac{dy'}{dx'}\right)^2}dx'

\end{align*}
$$
Notice the transformation does not change the structure of the functional, but merely the input stuffed into them.



#### Invariance of functional $J$ and Lie group

Functional $J$ 가 다음과 같이 주어졌다고 하자.
$$
J=\int_a^b \mathcal{L}\left(t,\,q^\mu(t),\,\dfrac{d}{dt}q^\mu(t)\right)\, dt
$$
variable transformation $t\to t',\, q^\mu \to {q^\mu}'$ 에 대해 transformed functional $J'$ 은 다음과 같다.
$$
J'=\int_{a'}^{b'}\mathcal{L}\left( t',\, {q^\mu}'(t'),\, \dfrac{d}{dt'}{q^\mu}'(t') \right)\,dt'
$$
앞으로 편의상 $J=\int \mathcal{L}\,dt,\,J'=\int\mathcal{L}'\,dt'$ 으로 쓰기로 한다.



$J$ 가 invariance라는 뜻은 엄격하게 말하자면 $\varepsilon$ 값이 무엇이든 간에 $J$ 의 값과 $J'$ 의 값이 같다는 뜻이다. But perhaps we do not have to be so rigid in our definition of the invariance of the functional. Perhaps we can distinguish matters of principle from what is detectable. <u>Rigidly requiring $J'$ to be exactly the same number as $J$ for all $\varepsilon$ means that we may be disqualifying a lot of transformations that have something to teach us</u>. 

우리는 invariance 의 정의로 infinitesimal change of $\varepsilon$ 에 대해 $|J-J'| \propto \varepsilon^s$ for some $s>1$ 일 때 $J$ 를 invariance라 하기로 하자.

Infinitesimal transformation을 $\varepsilon$ 에 대한 series로 나타내면,
$$
\begin{align*}
t'&=t+ \left(\dfrac{dT}{d\varepsilon}\right)_0 \varepsilon + O(\varepsilon^2)+\cdots\,,\\
{q^\mu}'&=q^\mu+\left(\dfrac{dQ^\mu}{d\varepsilon}\right)_0 \varepsilon + O(\varepsilon^2)+\cdots

\end{align*}\tag{3.1.4}
$$
이 때 series expansion에서 $\varepsilon$ 의 coefficient를 **generator** 라 한다. 이제 $\tau$ 와 $\zeta^\mu$ 를 다음과 같이 정의한다.
$$
\begin{align*}
\tau &\equiv \left( \dfrac{dT}{d\varepsilon} \right)_0 = \tau(t,\,q^\mu)\,,\\
\zeta^\mu&\equiv \left( \dfrac{dQ^\mu}{d\varepsilon} \right)_0 = \zeta^\mu (t,\, q^\nu)\,.

\end{align*}\tag{3.1.5}
$$
 그렇다면 식 (3.1.4) 는 다음과 같이 표현 할 수 있다.
$$
\begin{align*}
t'&=t+\tau\varepsilon + \cdots\,,\\
{q^\mu}'&=q^\mu + \zeta^\mu \varepsilon + \cdots\,.

\end{align*}\tag{3.1.6}
$$


<b>Example 4 : Rotation along $z$-axis in 3D Euclidean space </b>
$$
\begin{align*}
x'&=x+\varepsilon y\,,\\
y'&=-\varepsilon x + y\,,\\
z'&=z
\end{align*} \tag{3.1.7}
$$
<b> Example 5 : Lorentz transformation</b> (with $c=1$)
$$
\begin{align*}
t'&=t-vx\,,\\
x'&=x-vt\,,\\
y'&=y\,,\\
z'&=z

\end{align*}\tag{3.1.8}
$$




이러한 Invariants 들의 집합은 group을 이루며 이 group을 **Lie group** 이라 한다.



$J$ 는 $t,\,q^\mu(t),\,dq^\mu(t)/dt$ 의 함수이고 $J'$ 은 $t',\,{q^\mu}'(t'),\, d{q^\mu}'(t')/dt'$ 의 함수이다. 또한 $t'=T(t,\,q^\mu,\,\varepsilon)$, ${q^\mu}'=Q^\mu (t,\,q^\nu,\,\varepsilon)$ 이므로 $J'$ 을 $t$ 의 적분꼴로 나타 낼 수 있다. 즉,
$$
\begin{align*}
J'-J&=\int_{a'}^{b'}\mathcal{L \left(t',\,{q^\mu}'(t'),\,\dfrac{d{q^\mu}'(t')}{dt'}\right)}\,dt'-\int_a^b \mathcal{L}\left(t,\,q^\mu(t),\,\dfrac{dq^\mu (t)}{dt}\right)\,dt \\
&= \int_a^b \left[\mathcal{L \left(t',\,{q^\mu}'(t'),\,\dfrac{d{q^\mu}'(t')}{dt'}\right)}\left(\dfrac{dt'}{dt}\right)-\mathcal{L}\left(t,\,q^\mu(t),\,\dfrac{dq^\mu (t)}{dt}\right)\right]\,dt \\
&=\int_a^b \left[\mathcal{L}'\dfrac{dt'}{dt}-\mathcal{L}\right]\,dt

\end{align*}
$$
 이다. 따라서 invariance 조건은 다음과 동치이다.
$$
\mathcal{L}'\dfrac{dt'}{dt}-\mathcal{L}\sim \varepsilon^s,\quad \text{where }s>1\;.
$$


<b>Example 6. : Length functional</b>

Length functional $\displaystyle s=\int_a^b \sqrt{1+\left(\dfrac{dy}{dx}\right)^2}\,dx$ 를 생각하자. Example 1의 transformation에 대해,
$$
\mathcal{L}'\dfrac{dx'}{dx}-\mathcal{L}=\sqrt{1+\left(\dfrac{dy'}{dx'}\right)^2}\dfrac{dx'}{dx}-\sqrt{1+\left(\dfrac{dy}{dx}\right)^2}
$$
이다. (3.1.7) 로 부터,
$$
\begin{align*}
\dfrac{dx'}{dx}&=1+\dfrac{dy}{dx}\,,\\
\dfrac{dy'}{dx'}&=\dfrac{-\varepsilon dx+dy}{dx+\varepsilon dy}=\dfrac{-\varepsilon + (dy/dx)}{1+\varepsilon (dy/dx)}

\end{align*}
$$
이므로,
$$
\mathcal{L}'\dfrac{dx'}{dx}-\mathcal{L}=-\sqrt{1+\left(\dfrac{dy}{dx}\right)^2} \left(\dfrac{dy}{dx}\right)^2\varepsilon^2 + O(\varepsilon^3)
$$
이며 따라서 invariant 이다. 



## 3.2 Condition for Invariance : The Rund-Trautman Identity



#### Rund-Trautman Identity

만약 functional
$$
J=\int_a^b \mathcal{L}(t,\,q^\mu,\,\dot{q}^\mu)\,dt
$$
가 invariant under infinitesimal transformation 
$$
\begin{align*}
t'&=t+\varepsilon \tau + \cdots,\,\\
{q^\mu}' &=q^\mu + \varepsilon \zeta^\mu +\cdots

\end{align*}\tag{3.2.1}
$$
일 때 다음이 성립한다.
$$
\dfrac{\partial \mathcal{L}}{\partial q^\mu} \zeta^\mu + p_\mu \dot{\zeta^\mu} + \dfrac{\partial \mathcal{L}}{\partial t} \tau - \mathcal{H}\dot{\tau}=0\,. \tag{3.2.2}
$$

 <b>Note : </b> 여기서는 Rund-Trautman identity가 invariance의 필요조건이라고 기술되어 있으나 실제는 필요충분조건이고, 충분조건은 exercise에서 다룬다. 

----

*(proof)* (1) $J$ 가 invariant 이므로 $\mathcal{L}'\dfrac{dt'}{dt}-\mathcal{L}\sim \varepsilon^s$ for some $s>1$ 이다. 위 식을 $\varepsilon$ 에 대해 미분하고 $\varepsilon=0$ 으로 놓으면, 
$$
\begin{align*}
\left(\dfrac{d}{d\varepsilon}\left[\mathcal{L}'(t',\,{q^\mu}',\, \dot{q}^\mu) \dfrac{dt'}{dt}-\mathcal{L}(t,\,q^\mu,\,\dot{q}^\mu)\right] \right)_{\varepsilon=0}& =\mathcal{L}\dfrac{d}{d\varepsilon}\left[\dfrac{dt'}{dt}\right]_{\varepsilon=0} + \left[\dfrac{d\mathcal{L}'}{d\varepsilon}\cdot\left(1+\varepsilon\tau+\cdots\right)\right]_{\varepsilon=0} \\
&=\mathcal{L}\dfrac{d}{d\varepsilon}\left[1+\varepsilon \dot{\tau}+O(\varepsilon^2)\right]+\left[\dfrac{d\mathcal{L}'}{d\varepsilon}\right]_{\varepsilon=0} \\
&=\mathcal{L}\dot{\tau}+\left[\dfrac{d\mathcal{L}'}{d\varepsilon}\right]_{\varepsilon=0}\;, \\
\left(\dfrac{d\varepsilon^s}{d\varepsilon}\right)_{\varepsilon=0}&=\left(s\varepsilon^{s-1})\right)_{\varepsilon=0}=0\;.

\end{align*}
$$
이므로 다음 식을 얻는다.
$$
\mathcal{L}\dot{\tau}+\left[\dfrac{d\mathcal{L}'}{d\varepsilon}\right]_{\varepsilon=0}=0 \tag{a}
$$
(2) 여기서,
$$
\begin{align*}
\dfrac{d\mathcal{L}'}{d\varepsilon} &= \dfrac{\partial \mathcal{L}'}{\partial t'}\dfrac{dt'}{d\varepsilon}+\dfrac{\partial \mathcal{L}'}{\partial {q^\mu}'}\dfrac{d{q^\mu}'}{d\varepsilon}+ \dfrac{\partial \mathcal{L}'}{\partial {\dot{q}^\mu}'}\dfrac{d{\dot{q}^\mu}'}{d\varepsilon} \\
&= \dfrac{\partial \mathcal{L}'}{\partial t'}\tau+\dfrac{\partial \mathcal{L}'}{\partial {q^\mu}'}\zeta^\mu+ \dfrac{\partial \mathcal{L}'}{\partial {\dot{q}^\mu}'}\dfrac{d{\dot{q}^\mu}'}{d\varepsilon} \tag{b}


\end{align*}
$$
이며 $d{q^\mu}'=dq^\mu + \varepsilon d\zeta^\mu + O(\varepsilon^2)$ 이므로,
$$
{\dot{q}^\mu}' \equiv \dfrac{d{q^\mu}'}{dt'} = \dfrac{dq^\mu + \varepsilon d\zeta^\mu}{dt + \varepsilon d\tau} = \dfrac{ \dot{q}^\mu + \varepsilon \dot{\zeta}^\mu}{1+ \varepsilon\dot{\tau}}
$$
이다. 따라서,
$$
\left(\dfrac{d{\dot{q}^\mu}'}{d\varepsilon}\right)_{\varepsilon=0} =\left[\dfrac{d}{d\varepsilon} \left( \dfrac{ \dot{q}^\mu + \varepsilon \dot{\zeta}^\mu}{1+ \varepsilon\dot{\tau}}\right)\right]_{\varepsilon = 0} = \dot{\zeta}^\mu-\dot{q}^\mu\dot{\tau} \tag{c}
$$
(3) $\varepsilon\to 0$ 에서,
$$
\begin{align*}
\left(\dfrac{\partial \mathcal{L}'}{\partial t'} \right)_{\varepsilon=0} &= \dfrac{\partial \mathcal{L}}{\partial t} \,, \\
\left(\dfrac{\partial \mathcal{L}'}{\partial {q^\mu}'} \right)_{\varepsilon=0} &= \dfrac{\partial \mathcal{L}}{\partial q^\mu}\,,\\
\left(\dfrac{\partial \mathcal{L}'}{\partial {\dot{q}^\mu}'} \right)_{\varepsilon=0} &= \dfrac{\partial \mathcal{L}}{\partial \dot{q}^\mu}\,.

\end{align*}
$$
이므로 식 (b) 는,
$$
\left(\dfrac{d\mathcal{L}'}{d\varepsilon}\right)_{\varepsilon=0} = 
\dfrac{\partial \mathcal{L}}{\partial t}\tau+\dfrac{\partial \mathcal{L}}{\partial {q^\mu}}\zeta^\mu+ \dfrac{\partial \mathcal{L}}{\partial {\dot{q}^\mu}}\left(\dfrac{d{\dot{q}^\mu}'}{d\varepsilon}\right)_{\varepsilon=0} \tag{d}
$$
(4) From (a) and (d), and using $p_\mu = \dfrac{\partial \mathcal{L}}{\partial \dot{q}^\mu}$ and $\mathcal{H}=p_\mu \dot{q}^\mu -\mathcal{L}$  we get
$$
\begin{align*}
0&=\mathcal{L}\dot{\tau}+\dfrac{\partial \mathcal{L}}{\partial t}\tau + \dfrac{\partial \mathcal{L}}{\partial {q^\mu}}\zeta^\mu + p_{\mu}(\dot{\zeta}^\mu - \dot{q}^\mu\dot{\tau}) \\
&=\dfrac{\partial \mathcal{L}}{\partial q^\mu} \zeta^\mu + p_\mu \dot{\zeta^\mu} + \dfrac{\partial \mathcal{L}}{\partial t} \tau - \mathcal{H}\dot{\tau} \qquad \square

\end{align*}
$$



#### Two form of Rund-Trautman invariance

1. From 1,
   $$
   \dfrac{\partial \mathcal{L}}{\partial q^\mu} \zeta^\mu + p_\mu \dot{\zeta^\mu} + \dfrac{\partial \mathcal{L}}{\partial t} \tau - \mathcal{H}\dot{\tau}=0\,. \tag{3.2.2}
   $$

2. 

2. Form 2,

$$
-(\zeta^\mu-\dot{q}^\mu \tau)\left[\dfrac{\part \mathcal{L}}{\part q^\mu}-\dfrac{d}{dt}\dfrac{\part \mathcal{L}}{\part \dot{q}^\mu}\right] = \dfrac{d}{dt}\left[p_\mu\zeta^\mu-\mathcal{H}\tau\right] \tag{3.2.3}
$$

이 두 form은 equivalent 하다. (see exercises 4.3)





<b>Note : </b> Euler-Lagrange eq. 와 Rund-Trautman identity를 구별하라. Euler-Lagrange eq. 는 extremal of functional 에 대한 조건이고 Rund-Trautman identity는 invariance of functional에 대한 것이다.



<b>Example 1 : Length functional under rotation</b> 

Length functional $\mathcal{L}=\sqrt{1+\left(\dfrac{dy}{dx}\right)^2}$ 를 생각하자. Rotation의 generator (3.1.7)을 생각하면, $\tau = y,\,\zeta=-x$ 이며, $\part_x \mathcal{L}=0,\, \part_y \mathcal{L}=0$ 이다. $p=\part_{\dot{y}}\mathcal{L}=\dot{y}/\sqrt{1+\dot{y}^2}$ where $\dot{y}=dy/dx$  이므로 
$$
\mathcal{H}=p\dot{y}-\mathcal{L}=\dfrac{\dot{y}^2}{\sqrt{1+\dot{y}^2}}-\sqrt{1+\dot{y}^2}=-\dfrac{1}{\sqrt{1+\dot{y}^2}}
$$
이다.

Rund-Trautman identity를 적용하면,
$$
\dfrac{\partial \mathcal{L}}{\partial y} (-x) + p  + \dfrac{\partial \mathcal{L}}{\partial t} y - \mathcal{H}\dot{y}=p-\mathcal{H}\dot{y}=0
$$
이다. 따라서 length functional은 invariant 하다.



<b>Example 2  : time-independent potential</b> 1차원이고 time-independent potential $U(t,\,x)$ 에서 움직이는 Neutonian particle with mass $m$ 에 대한 Lagrangian은
$$
\mathcal{L}(t,\,x,\,\dot{x})=\dfrac{1}{2}m\dot{x}^2-U(t,\,x)
$$
이사 $t'=t+\varepsilon t,\, x'=x+\dfrac{\varepsilon}{2}x$ 의 rescaling을 생각하면 $\tau=t,\, \zeta = x/2$ 이다. $p=mv$ 이며 $\mathcal{H}=\dfrac{1}{2}m\dot{x}^2+U(t,\,x)$ 이므로 Rund-Trautman identity는
$$
\dfrac{\partial \mathcal{L}}{\part x} \zeta+ p \dot{\zeta} + \dfrac{\partial \mathcal{L}}{\partial t} \tau - \mathcal{H}\dot{\tau}= -(\part_x U)\dfrac{x}{2}+\dfrac{m\dot{x}^2}{2}-(\part_t U)t-\dfrac{1}{2}m\dot{x}^2-U=-U-\dfrac{1}{2}(\part_x U) x-(\part_t U)t
$$
이며 generally nonzero 이다.



## 3.3 A More Liberal Definition of Invariance



#### Divergence invariant

Functional $\mathcal{L}$ 이 어떤 function $F(t)$ 에 대해 
$$
\mathcal{L}' \dfrac{dt'}{dt}-\mathcal{L}= \varepsilon \dfrac{dF}{dt}+O(\varepsilon^s)\;\quad ,\,s>1 \tag{3.3.1}
$$
일 때 $\mathcal{L}$ 은 **divergence invariant** 하다고 한다.



#### Rund-Trantman condition

Rund-Trautman condition은 $\mathcal{L}'\dfrac{dt'}{dt}-\mathcal{L}=\varepsilon^s$ 의 양변을 $\varepsilon$으로 미분하고 $\varepsilon \to 0$ 을 취한 것이므로,
$$
\dfrac{\partial \mathcal{L}}{\partial q^\mu} \zeta^\mu + p_\mu \dot{\zeta^\mu} + \dfrac{\partial \mathcal{L}}{\partial t} \tau - \mathcal{H}\dot{\tau} = \dfrac{dF}{dt} \tag{3.3.2}
$$
이다.



## Exercises

<b>4.1.</b> 질량 $m$ , 전하량 $q$ 인 입자가 전자기장을 움직일 경우 potentials $V(t,\,\mathbf{r})$ 과 $\boldsymbol{A}(t,\,\mathbf{r})$ 로 기술 할 수 있다. 전기장과 자기장은 $\mathbf{E}=-\nabla V-\part_t \boldsymbol{A}$, $\mathbf{B}=\nabla \times \boldsymbol{A}$ 이다. 입자가 빛의 속도에 비해 느리게 움직일 경우 그 Lagrangian은 다음과 같다.
$$
\mathcal{L}=\dfrac{1}{2}m\dot{r}^2+q\boldsymbol{v} \cdot \boldsymbol{A}-qV\;.
$$
이 Lagrangian에 대한 time integral이 아래와 같은 Galilean transformation에 대해 invariant 한지 확인하시오.
$$
\begin{align*}
t'&=t\,,\\
x'&=x-vt\,,\\
y'&=y\,,\\
z'&=z\,.

\end{align*}
$$

---

Invariance 조건에서 $\tau=0,\, \zeta_1=-t,\, \zeta_2=\zeta_3=0,\,\,\varepsilon=v$ 로 볼 수 있다. Conjugate momentum $p_i$는
$$
p_i=\part_{\dot{x}_i}\mathcal{L}=m\dot{x}_i+qA_i
$$
이며 Hamiltonian $\mathcal{H}$ 는
$$
\mathcal{H}=\sum_ip_i \dot{x}_i-\mathcal{L}=\sum_i\dfrac{1}{2}m\dot{x}_i^2+qV
$$
이다. Rund-Trautman condition
$$
\begin{align*}
\dfrac{\partial \mathcal{L}}{\partial x^\mu} (-t) + p_\mu \dot{\zeta^\mu} - \mathcal{H}\dot{\tau} &=-t(qv_j\part_i A_j-q\part_iV)-(m\dot{x}_1)
\end{align*}
$$
이므로 generally not-invariant 하다.



<b>4.2. </b> 1D-damped harmonic oscillator with mass $m$ and time dependent spring constant $k$ 의 Lagrangian은
$$
\mathcal{L}=\left[\dfrac{1}{2}m\dot{x}^2-\dfrac{1}{2}k(t)x^2\right]e^{bt/m}
$$
이다. $t'=t+\varepsilon t$ , $x'=x+\dfrac{1}{2}\varepsilon x$ 로 놓고 $\mathcal{L}$ 이 time integral에 대해 invariant 한지 확인하시오. Invariant 하지 않다면 어떤 조건에서 invariant 할 수 있는가?

---

(1) $\tau=t$, $\zeta=x/2$ 이다. $p=m\dot{x}e^{bt/m}$ 이며 Hamiltonian은,
$$
\mathcal{H}=p\dot{x}-\mathcal{L}=\left[\dfrac{1}{2}m\dot{x}^2+\dfrac{1}{2}k(t)x^2\right]e^{bt/m}
$$
이고,
$$
\dfrac{\part \mathcal{L}}{\part t}=-\dfrac{1}{2}k'(t)x^2e^{bt/m}-\dfrac{b}{2m}k(t)x^2e^{bt/m}
$$
Rund-Trautman condition은 
$$
\begin{align*}
\dfrac{\partial \mathcal{L}}{\partial x} \dfrac{x}{2} + p \dfrac{\dot{x}}{2} + \dfrac{\partial \mathcal{L}}{\partial t} t - \mathcal{H}&= \left[-\dfrac{kx^2}{2}+\dfrac{m\dot{x}^2}{2} -\dfrac{k'x^2}{2}-\dfrac{bkx^2}{2m}-\dfrac{m\dot{x}^2}{2}-\dfrac{kx^2}{2}\right]e^{bt/m} \\
&=\left[-k(t)\left(1+\dfrac{b}{2m} \right)-\dfrac{k'(t)}{2}\right]x^2e^{bt/m}

\end{align*}
$$
이므로 generally nonzero 이다. 따라서 invariant 하다.

(2) 만약
$$
\dfrac{k'(t)}{k(t)}=-\left(2+\dfrac{b}{m}\right)
$$
이면, 즉 $k(t) = k_0 \exp \left[-\left(2+\dfrac{b}{m}\right)t\right]$ 이면 된다.



<b>4.3.</b> 식 (3.2.2)로부터  (3.2.3)을 유도하라.

---

$$
\dfrac{\partial \mathcal{L}}{\partial q^\mu} \zeta^\mu + p_\mu \dot{\zeta^\mu} + \dfrac{\partial \mathcal{L}}{\partial t} \tau - \mathcal{H}\dot{\tau}=0\,. \tag{3.2.2}
$$

$$
-(\zeta^\mu-\dot{q}^\mu \tau)\left[\dfrac{\part \mathcal{L}}{\part q^\mu}-\dfrac{d}{dt}\dfrac{\part \mathcal{L}}{\part \dot{q}^\mu}\right] = \dfrac{d}{dt}\left[p_\mu\zeta^\mu-\mathcal{H}\tau\right] \tag{3.2.3}
$$

이다. 
$$
\begin{align*}
\dfrac{d}{dt}\left[p_\mu \zeta^\mu-\mathcal{H}\tau\right] &= \dfrac{d}{dt}\left[\dfrac{\part \mathcal{L}}{\part \dot{q}^\mu} \zeta^\mu-\mathcal{H}\tau\right]\\
&=-\mathcal{H}\dot{\tau}+\left[\dfrac{d}{dt}\dfrac{\part \mathcal{L}}{\part \dot{q}^\mu} \zeta^\mu+\dfrac{\part \mathcal{L}}{\part \dot{q}^\mu}\dot{\zeta}^\mu-\dfrac{d\mathcal{H}}{dt} \tau\right]
\end{align*}
$$
이므로, $p_\mu  =\part \mathcal{L}/\part \dot{q}^\mu$ , ${d\mathcal{H}}/{dt}=-\part \mathcal{L}/\part t$ 임을 이용하면,
$$
\begin{align*}
-\mathcal{H}\dot{\tau}&=\dfrac{d}{dt}\left[p_\mu \zeta^\mu-\mathcal{H}\tau\right] -\left[\dfrac{d}{dt}\dfrac{\part \mathcal{L}}{\part \dot{q}^\mu}+\dfrac{\part \mathcal{L}}{\part \dot{q}^\mu}\dot{\zeta}^\mu - \dfrac{d\mathcal{H}}{d t} \tau\right] \\
&=-\dfrac{\partial \mathcal{L}}{\partial q^\mu} \zeta^\mu - \dfrac{\part \mathcal{L}}{\part \dot{q}^\mu} \dot{\zeta^\mu} - \dfrac{\partial \mathcal{L}}{\partial t} \tau
\end{align*}
$$
따라서,
$$
\begin{align*}

\dfrac{d}{dt}\left[p_\mu \zeta^\mu-\mathcal{H}\tau\right]&= \dfrac{d}{dt}\dfrac{\part \mathcal{L}}{\part \dot{q}^\mu}\zeta^\mu-\tau\dfrac{d}{dt}(p_\mu \dot{q}^\mu-\mathcal{L}) -\dfrac{\part\mathcal{L}}{\part q^\mu}\zeta^\mu-\dfrac{\part \mathcal{L}}{\part t}\tau \\
&=\dfrac{d}{dt} \dfrac{\part \mathcal{L}}{\part \dot{q}^\mu}\zeta^\mu-\tau \left(\dot{p_\mu} \dot{q}^\mu+p^\mu \ddot{q}^\mu -\dfrac{\part \mathcal{L}}{\part q^\mu} \dot{q}^\mu-\dfrac{\part \mathcal{L}}{\part \dot{q}^\mu}\ddot{q}^\mu - \dfrac{\part \mathcal{L}}{\part t}\right) -\dfrac{\part \mathcal{L}}{\part q^\mu} \zeta^\mu -\tau \dfrac{\part \mathcal{L}}{\part t} \\
&=(\zeta^\mu  - \tau \dot{q}^\mu) \dfrac{d}{dt}\dfrac{\part \mathcal{L}}{\part \dot{q}^\mu} + (\tau \dot{q}^\mu-\zeta^\mu)\dfrac{\part \mathcal{L}}{\part q^\mu} \\
&=-(\zeta^\mu-\tau \dot{q}^\mu)\left(\dfrac{\part \mathcal{L}}{\part q^\mu} -\dfrac{d}{dt}\dfrac{\part \mathcal{L}}{\part \dot{q}^\mu}\right)

\end{align*}
$$









<b>4.6. </b> Rund-Trautman identity에 의하면 central force motion은 latitude와 longitude coordinates의 변화에 대해 invariant 함을 보이시오.

---

Lagrangian for central force motion :
$$
\mathcal{L}=\dfrac{1}{2}m(\dot{r}^2 + r^2\dot \theta^2+r^2\sin^2\theta \dot{\phi^2})-U(t,\,r)\;.
$$
Transformation :
$$
\begin{align*}
t'&=t+\varepsilon \tau\,,\\
{\theta}'&=\theta + \varepsilon \zeta^\theta\,,\\
{\phi}'&=\phi+\varepsilon \zeta^\phi\,\\
r'&=r\,.

\end{align*}
$$
partial differentiation of $\mathcal{L}$ :
$$
\begin{align*}
\dfrac{\part \mathcal{L}}{\part \theta}&=mr^2\sin\theta \cos \theta \dot{\phi}^2\,,\\
\dfrac{\part \mathcal{L}}{\part \phi}&=0\,,\\
\dfrac{\part \mathcal{L}}{\part r}&=mr\dot{\theta}^2+mr\sin^2 \dot{\phi}^2-\dfrac{\part U}{\part r}\,,\\
\dfrac{\part \mathcal{L}}{\part \dot{\theta}}&=mr^2\dot{\theta}=p_{\theta}\,,\\
\dfrac{\part \mathcal{L}}{\part \dot{\phi}}&=mr\sin^2\theta \dot{\phi}=p_\phi\,,\\
\dfrac{\part \mathcal{L}}{\part \dot{r}} &= m\dot{r}=p_r

\end{align*}
$$
Hamiltonian becomes,
$$
\mathcal{H}=\dfrac{1}{2}m(\dot{r}^2 + r^2\dot \theta^2+r^2\sin^2\theta \dot{\phi^2})+U(t,\,r)\;.
$$
Rund-Trautman identity :
$$
\begin{align*}
0&=\dfrac{\partial \mathcal{L}}{\partial q^\mu} \zeta^\mu + p_\mu \dot{\zeta^\mu} + \dfrac{\partial \mathcal{L}}{\partial t} \tau - \mathcal{H}\dot{\tau}\\
&=\zeta^\theta\left(mr\sin\theta \cos \theta \dot{\phi}^2\right)+mr^2\dot{\theta} \dot{\zeta}^\theta+mr\sin^2\theta\dot{\phi}\dot{\zeta}^\phi -\dfrac{\part U}{\part t}\tau -



\end{align*}
$$
