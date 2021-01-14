III. Invariance
===



## 3.1 Formal Definition of Invariance



#### Continuous transformation 

Continuous parameter $\varepsilon$ 을 생각하자. $\varepsilon$ 이 $0$ 부터 변화할 수 있으며 $\varepsilon=0$ 일 때의 변화가 identity transformation 이라 하자. 

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
J'=\int_{a'}^{b'}\mathcal{L}\left( t',\, {q^\mu}'(t'),\, \dfrac{d}{dt'}{q^\mu}'(t') \right)
$$
앞으로 편의상 $J=\int \mathcal{L}\,dt,\,J'=\int\mathcal{L}'\,dt'$ 으로 쓰기로 한다.



$J$ 가 invariance라는 뜻은 엄격하게 말하자면 $\varepsilon$ 값이 무엇이든 간에 $J$ 의 값과 $J'$ 의 값이 같다는 뜻이다. But perhaps we do not have to be so rigid in our definition of the invariance of the functional. Perhaps we can distinguish matters of principle from what is detectable. <u>Rigidly requiring $J'$ to be exactly the same number as $J$ for all $\varepsilon$ means that we may bbe disqaulifying a lot of transformations that have something to teach us</u>. 

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

\end{align*}\tag{3.1.9}
$$
일 때 다음이 성립한다.
$$
\dfrac{\partial \mathcal{L}}{\partial q^\mu} \zeta^\mu + p_\mu \dot{\zeta^\mu} + \dfrac{\partial \mathcal{L}}{\partial t} \tau - \mathcal{H}\dot{\tau}=0\,. \tag{3.1.10}
$$

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
 

