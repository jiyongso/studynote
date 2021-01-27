IV. Emmy Noether's Elegant Theorem
===



## 4.1 Extremal + Invariance = Noether's theorem



#### Summary

만약 functional $J$ 가 $\tau$ 와 $\zeta^\mu$ 를 generator로 하는 변환에 대해 invariant 하다면 Rund-Trautman identity가 성립함을 알았다. Rund-Trautman identity 는 아래와 같은 두가지 동등한 형식으로 기술된다.
$$
\begin{align*}
\text{RTI I:}&\quad \dfrac{\partial \mathcal{L}}{\part q^\mu} \zeta^\mu + p^\mu \dot{\zeta}^\mu + \dfrac{\part \mathcal{L}}{\part t}\tau - \mathcal{H}\dot{\tau}=\dfrac{dF}{dt}\,, \tag{4.1.1}\\
\text{RTI II:}& \quad -(\zeta^\mu-\dot{q}^\mu \tau)\left[\dfrac{\part \mathcal{L}}{\part q^\mu} - \dot{p}^\mu\right]= \dfrac{d}{dt}\left[p_\mu \zeta^\mu -\mathcal{H}\tau - F\right]\,. \tag{4.1.2}

\end{align*}
$$
여기서
$$
p_\mu =\dfrac{\part \mathcal{L}}{\part \dot{q}^\mu}\tag{4.1.3}
$$
은 $q^\mu$ 에 대한 momentum conjugate 이며, Hamiltonian $\mathcal{H}$ 는 다음과 같다.
$$
\mathcal{H}=p_\mu q^\mu -\mathcal{L}\;. \tag{4.1.4}
$$


우리는 또한 functional $J$ 가 extremal 이라면 아래와 같이 기술되는 Euler-Lagrange eq. 를 만족함을 안다.
$$
\begin{align*}
\text{ELE I :}&\quad \dfrac{\part \mathcal{L}}{\part t}=-\dot{\mathcal{H}}\,,\tag{4.1.5}\\
\text{ELE II :}& \quad \dfrac{\part \mathcal{L}}{\part q^\mu}=\dot{p}_\mu\,. \tag{4.1.6}


\end{align*}
$$

#### Noether's Theorem 

Functional $J$ 가
$$
J=\int_a^b \mathcal{L}(t,\,q^\mu,\, \dot{q}^\mu)\,dt \tag{4.1.7}
$$
가 extremal 이며 invariant under infinitesimal transformation
$$
\begin{align*}
t'&=t+\varepsilon \tau + \cdots \,,\tag{4.1.8} \\
{q^\mu}' &= q^\mu +\varepsilon \zeta^\mu + \cdots \,. \tag{4.1.9}

\end{align*}
$$
이면 , (4.1.6) 에 의해 (4.1.2) 의 우변의 $[\cdots]=0$ 이므로 다음이 성립한다.
$$
\begin{align*}
\dfrac{d}{dt}\left[p_\mu\zeta^\mu -\mathcal{H}\tau -F\right]&=0 \;, \tag{4.1.10} \\
p_\mu\zeta^\mu -\mathcal{H}\tau - F&= \text{const.}\tag{4.1.11}

\end{align*}
$$



<b>Example 1 :</b> 입자의 움직임을 cylindrical coordi. 에서 기술하면
$$
\mathcal{L}=\dfrac{1}{2}m(\dot{r}^2+r^2\dot{\theta}^2+\dot{z}^2)-U
$$
이다. $t'=t+\varepsilon,\, r'=r,\, \theta'=\theta,\, z'=z$ 인 변환에 대해 생각하면 $\tau=1,\, \zeta^\mu=0$ 이므로 (4.1.11)에 의해 
$$
\mathcal{H}=\text{const.}
$$
이다. 이는 에너지 보존이다.



<b>Example 2: </b> Example 1의 Lagrangian에 대해 $t'=t,\, r'=r,\, \theta'=\theta+\varepsilon,\, z'=z$ 변환을 생각하면 식 (4.1.11)에 의해,
$$
p_\theta=\text{const}
$$
이다. 이는 각운동량 보존이다.



<b>Example 3 :</b> 1D dampled oscillator with Lagrangian
$$
\mathcal{L}=\left[\dfrac{1}{2}m\dot{x}^2-\dfrac{1}{2}kx^2\right]e^{bt/m}
$$
을 생각하자. $t'\to t+\varepsilon\tau,\, x \to x+\varepsilon \zeta$ transformation with $\tau=1,\, \zeta=-bx/2m$ 이라 하면,
$$
\begin{align*}
p_x &=\dfrac{\part \mathcal{L}}{\part \dot{x}}=m\dot{x}e^{bt/m}\,,\\
\mathcal{H}&=p_x \dot{x}-\mathcal{L}=\left[\dfrac{1}{2}m\dot{x}^2+\dfrac{1}{2}kx^2\right] e^{bt/m}

\end{align*}
$$
이므로, (4.1.11) 에 의해,
$$
p_x\zeta-\mathcal{H}\tau=-\left[\dfrac{1}{2m}bx\dot{x}+\dfrac{1}{2}m\dot{x}^2+\dfrac{1}{2}kx^2 \right]e^{bt/m}=\text{const.}
$$
이다. 에너지도, 운동량도 보존되지 않지만 보존되는 양이 있음을 알 수 있다.



<b>Example 4 : </b> 질량 $m$, 전하량 $q$ 를 가진 입자가 scalar potential $V$ 와 vector potential $\boldsymbol{A}$ 의 영항에서 움직인다고 하자. Non-relativistic Lagrangian $\mathcal{L}$ 은
$$
\mathcal{L}=\dfrac{1}{2}m\dot{\boldsymbol{r}}^2+e\dot{\boldsymbol{r}}\cdot \boldsymbol{A}-eV
$$
이다. 운동량 $\boldsymbol{p}$ 와 Hamiltonian $\mathcal{H}$ 를 구하면,
$$
\begin{align*}
\boldsymbol{p}&=m\dot{\mathbf{r}}+e\boldsymbol{A}\,,\\
\mathcal{H}&=\boldsymbol{p}\cdot \dot{\boldsymbol{r}}-\mathcal{L}=\dfrac{(\boldsymbol{p}-e\boldsymbol{A})^2}{2m} +eV\,,
\end{align*}
$$
이다. 다음과 같은 transformation을 생각하자.
$$
\begin{align*}
t'&=t(1+\varepsilon )\,,\\
{x^\mu}'&=x^\mu \left(1+\dfrac{1}{2} \varepsilon\right)\,.
\end{align*}
$$
즉 $\tau = t,\, \zeta^\mu =\dfrac{1}{2}x^\mu$ 에 대해, 식 (4.1.11) 은,
$$
\dfrac{1}{2}\boldsymbol{p}\cdot \boldsymbol{r} -\mathcal{H}t=\text{const.}
$$
이다. 



<b>Example 5 : </b> chapter 4. 의 projectile example을 생각하자 Lagrangian은
$$
\mathcal{L}=\dfrac{1}{2}m(\dot{x}^2+\dot{y}^2)-mgy
$$
이며 Galilean transformation
$$
\begin{align*}
t'&=t\,,\\
x'&=x-vt\,,\\
y'&=y\,,

\end{align*}
$$
를 생각하면 $\tau=0,\, \zeta^x=-t,\, \zeta^y=0$ 이다. 