II. Functionals
===



#### Conventions

1. Vector component를 $x^{\mu}$ 로 표시한다. $\mu=1,\,2,\,3$ 이거나 $\mu=1,\,2,\,3,\,4$ 일 수 있다.
2. $a\equiv \text{bla...}$ 는 $a$의 정의.
3. $\dot{x}^\mu\equiv \dfrac{d x^{\mu}}{dt}$. 





#### Definition : Functional

최소한 이 책에서 관심있는 **functional** $J$는 closed interval $[a,\,b]$ 에서 정의된 $C^2$ 함수들의 집합에서 실수로의 mapping을 의미한다. 이 mapping은 다음과 같이 정의된다.
$$
J=\int_a^b \mathcal{L}(t,\,x^\mu,\, \dot{x}^{\mu})\,dt\;.
$$
여기서 $\mathcal{L}=\mathcal{L}(t,\, x^\mu,\, \dot{x}^\mu)$ 를 *Lagrangian of functional $J$* 라 한다. 



 <b>Note 1 : </b> 여기서는 Lagrangian $\mathcal{L}$ 이 $x^\mu$ 와 그 1차 미분값에만 의존하는것으로 표현되었으나 원리적으로는 2차 이상의 미분을 포함할 수도 있다. 



<b>Note 2 : </b> 물리학, 특히 역학에서는 Lagrangian을 운동에너지 - 위치에너지로 정의하지만 여기서는 functional의 integrand로 정의하도록 한다.



#### Exercises

<b>2.1.</b> refractive index $n=n_0 (1-x/a)$ 인 medium을 생각하자. 여기서 $n_0$ 와 $a$는 상수이다. 빛이 $(0,\,0)$ 에서 $(x,\,y )=(a,\, y(a))$ 까지 다음 경로로 진행할 때 걸리는 시간을 구하여라.

a. $y=x$

b. $y=a\cosh (x/a)$

---

From (2.1.4), 
$$
\Delta t=\dfrac{1}{c}\int_0^a n(x,\,y)\sqrt{1+y'^2}\,dx
$$
이므로,

a. $y=a$ 의 경우
$$
\Delta t = \dfrac{n_0}{c}\int_0^a \left(1-\dfrac{x}{a}\right)\sqrt{2}\,dx=\dfrac{an_0}{c\sqrt{2}}\;.
$$
b. $y=a\cosh (x/a)$의 경우
$$
\begin{align*}
\Delta t &= \dfrac{n_0}{c} \int_0^a \left(1-\dfrac{x}{a}\right)\cosh \left(\dfrac{x}{a}\right)\,dx \\
&=\dfrac{an_0}{c} \left[2 \sinh 1- \cosh 1+2\right]

\end{align*}
$$


<b>2.2. </b> Hamilton's principle에 의하면 역학에서 **action** functional
$$
J=\int_{0}^t \left(K-U\right)\, dt
$$
가 최소화 되는 경로로 입자의 경로가 결정된다고 한다. 이때문에 Hamilton's principle 은 the principle of least action 으로 불리기도 한다. 총 에너지는 $E\equiv K+U$ 로 정의되며 여기서 $K\equiv \dfrac{1}{2}m\left(\dfrac{dx}{dt}\right)^2$ 이다.

a. 다음을 보이시오.
$$
J=\int_0^t 2K\, dt -\int_0^t E\,dt\;.
$$
b. $J$ 가 다음과 같음을 보이시오. 여기서 $p=mv$ 이다.
$$
J=\int_{x(0)}^{x(t)}p\,dx - \int_0^t E\,dt\;.
$$
c. $p=\dfrac{\partial J}{\partial x}$ 이고 $E=-\dfrac{\partial J}{\partial t}$ 임을 보이시오. 

d. 만약 우리가 $E=\text{const}$ 임을 안다면 Hamilton's principle 이 아래와 같이 주어진 action에 대한 the principle of least action 이 됨을 보이시오.
$$
\int_{x(0)}^{x(t)}p\,dx\;.
$$
<b>Note : </b>반대로 Hamilton's principle, 즉 the principle of least action $\displaystyle \int (K-U)\,dt=\text{min}$ 은 에너지보존을 부가적인 조건으로 요구하지 않는다. 어떤 저자들은 $\displaystyle \int p\, dx$ 를 $\displaystyle \int p,\,dx=\text{min}$ 이라는 의미에서 **abbreviated action** 으로 구별하여 부르기로 한다. 이 두 action은 에너지보존이라는 조건에서 같은 것을 말한다. Hamilton's principle이 역학적 에너지 보존을 요구하지 않으므로 더 일반적이라 볼 수 있다.

---

a. $E=K+U$ 이므로,
$$
J=\int_0^t (K-U)\, dt=\int_0^t (2K-E)\, dt
$$
b. $x=x(t),\, v=\dot{x}=dx/dt$ 이므로, $K$ 를 $t\to x$ 적분 parameter 변환하면,
$$
K=\int_0^t \dfrac{1}{2}m\dot{x}^2dt=\dfrac{1}{2}\int_{x(0)}^{x(t)}m\dfrac{dx}{dt}dx=\dfrac{1}{2}\int_{x(0)}^{x(t)}p\,dx
$$
이다. 따라서 $J=\displaystyle \int_{x(0)}^{x(t)} p\,dx -\int_0^t E\,dt$. 

c. $\displaystyle \int_{x(0)}^{x(t)}p\,dx = P(x(t))-P(x(0))=P(x)-P(x_0)$ 라 하면, $\dfrac{dP(x)}{dx}=p$ 이다. 따라서,
$$
\begin{align*}
\dfrac{\partial J}{\partial x}&= \dfrac{dP(x)}{dx}=p,\quad \dfrac{\partial J}{\partial t}=-E

\end{align*}
$$
d. $E=\text{const.}$  이면, $J=\displaystyle \int_{x(0)}^{x(t)}p\,dx -Et$ 이며 주어진 $0,\,t$ ㄹ르 생각하면 $Et$ 는 상수이다. 즉 $J$를 minimize 하는 것은 $\displaystyle \int_{x(0)}^{x(t)} p\,dx$ 를 minimize 하는 것이므로 abbreviated action을 minimize 하는 것이다.



<b>2.3 </b> 질량 $m$ 인 입자가 그 크기가 $g$로 균일한 중력장을 수직낙하한다고 하자. $y$축을 수직축으로 잡을 때 potential energy 는 $mgy$ 이다. functional 은 다음과 같다.
$$
J=\int_0^{t_0} \left(\dfrac{1}{2}m\dot{y}^2-mgy\right) \,dt\;.
$$
a.  $y(t)=At^n$, $A=\text{const.},\, n=\text{const.}$ 라 가정하고 정적분을 계산하여 $J$ 를 구하시오.

b. $y(t)=A(1-e^{-nt})$ 라 놓고 $J$ 를 계산하시오.

c. $y(t) = A \sinh (nt)$ 라 놓고 $J$를 계산하시오.

---

a. $\dot{y}(t) =nAt^{n-1}$ 이므로,
$$
\begin{align*}
J&=\int_0^{t_0} \left( \dfrac{mn^2A^2}{2} t^{2n-2}-mAg t^{n} \right)\,dt=\dfrac{mn^2A^2}{4(n-1)}{t_0}^{2n-1}-\dfrac{mgA}{n+1}{t_0}^{n+1}\;.
\end{align*}
$$
b. $\dot{y}(t) = nA\exp^{-nt}$ 이므로,
$$
\begin{align*}

J&=\int_0^{t_0}\left(\dfrac{mn^2A^2}{2}e^{-2nt}-mgAe^{-nt} \right)\,dt=\left[-\dfrac{mnA^2}{4}e^{-2nt}+\dfrac{mgA}{n}e^{-nt}\right]_0^{t_0}\\
&=\dfrac{mnA^2}{4}\left( 1-e^{-2nt_0} \right)-\dfrac{mgA}{n}\left(1-e^{-nt_0}\right)\;.

\end{align*}
$$
c. $\dot{y}(t) = nA\cosh(nt)$ 이므로,
$$
\begin{align*}
J&=\int_0^{t_0}\left(\dfrac{mn^2A^2}{2}\sinh^2nt-mgA\cosh(nt)\right)\, dt \\
&=\int_0^{t_0}\left( \dfrac{mn^2A^2}{2} \dfrac{e^{2nt}+e^{-2nt}-2}{4}-mgA\cosh (nt)\right)\, dt \\
&=\dfrac{mn^2A^2}{2}\left[\dfrac{e^{2nt}-e^{-2nt}-4nt}{8n}\right]_0^{t_0} -mgA(\cosh(nt_0)-1) \\
&=\dfrac{mnA^2}{16}(e^{2nt_0}-e^{-2nt_0}-4nt_0)-mgA(\cosh (nt_0)-1)

\end{align*}
$$



<b>2.4.</b> 주기 $T$의 주기운동을 하는 입자의 운동이 다음과 같은 functional 로 기술된다고 하자.
$$
J=\int_0^T \left(\dfrac{1}{2}m\dot{x}^2-\dfrac{1}{2}m\omega^2x^2\right)\,dt
$$
a. 첫번째 반주기는 $dx/dt=+v_0=\text{const.}$ 라 놓고, 나머지 반주기는 $dx/dt=-v_0=\text{const.}$ 라 놓고  해를 구하기를 시도한다고 하자. 위의 부정적분 $J$ 를 계산하라.

b. $x(t)=A \cos (\omega t)$ 로 놓고 $J$ 를 계산하라.

c. (a)와 (b) 의 $J$ 를 비교하여 어느 값이 더 적은지 비교하라.

---

a. 첫번째 반주기에서 $x(t) = x_1(t)=v_0t+x_0$, 두번째 반주기에서 $x(t) =x_2(t)= -v_0 t+v_0T+x_0$ 이어야 한다. 이 운동이 연속이어야 하므로 $x_1(0)=x_2(T)$ 이어야 하며 $x_1(T/2)=x_2(T/2)$ 이어야 한다. $x_2(t)=-v_0T+x_1$ 로 놓자. 


$$
\begin{align*}
J&=\int_0^{T/2}\left(\dfrac{1}{2}mv_0^2-\dfrac{1}{2}m\omega^2(v_0t+x_0)^2\right)\,dt+\int_{T/2}^{T}\left(\dfrac{1}{2}mv_0^2-\dfrac{1}{2}m\omega^2(-v_0t+x_1)^2\right)\, dt\\
&=\dfrac{mv_0^2 T}{2}-\dfrac{m\omega^2}{3v_0}\left[\left(\dfrac{v_0T}{2}+x_0\right)^3-{x_0}^3\right]


\end{align*}
$$
b. $\dot{x}(t) = -\omega A \sin (\omega t)$ 이므로,
$$
\begin{align*}
J&=\int_0^T \left(\dfrac{m\omega^2A^2\sin^2(\omega t)}{2} -\dfrac{m\omega^2\cos^2(\omega t)}{2}\right)\, dt\\
&= \dfrac{m\omega^2A^2}{2} \int_0^T -\cos (2 \omega t)\, dt=-\dfrac{m\omega A^2}{4}=0\, 
\end{align*}
$$
