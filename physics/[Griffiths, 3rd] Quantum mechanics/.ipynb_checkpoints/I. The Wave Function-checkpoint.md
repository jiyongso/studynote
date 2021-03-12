I. The Wave Function
===



## 1.1 The Schroedinger Equation



## 1.2 The Statistical Interpretation



## 1.3 Probability



## 1.4 Normalization

<b>Problem 1.7 </b> $\dfrac{d\langle p\rangle}{dt}$를 계산하시오.

---

$$
\begin{aligned}
\dfrac{d\langle p\rangle}{dt}&=\dfrac{d}{dt}\int \Psi^*(x,\,t) \left(-i\hbar\dfrac{\partial}{\partial x}\right)\Psi(x,\,t)\,dx \\
&=-i\hbar \int \left[\dfrac{\partial \Psi^*}{\partial t} \dfrac{\partial \Psi}{\partial x}+\Psi^* \dfrac{\partial}{\partial x}\left(\dfrac{\partial \Psi}{\partial t}\right)  \right]\,dx \\
&=-i\hbar \int \left[\left(-\dfrac{i\hbar}{2m}\dfrac{\partial^2 \Psi^*}{\partial x^2}+\dfrac{i}{\hbar}V\Psi^*\right) \dfrac{\partial \Psi}{\partial x}+\Psi^* \dfrac{\partial }{\partial x}\left(\dfrac{i\hbar}{2m} \dfrac{\partial^2 \Psi}{\partial x^2}-\dfrac{i}{\hbar}V\Psi\right) \right]\,dx \\
&=\dfrac{-\hbar^2}{2m} \int\left[\dfrac{\partial^2 \Psi^*}{\partial x^2}\dfrac{\partial \Psi}{\partial x} - \Psi^* \dfrac{\partial^3 \Psi}{\partial x^3}\right]dx+ \int\left[V\Psi^* \dfrac{\partial \Psi}{\partial x}-\Psi^* \dfrac{\partial V}{\partial x} \Psi -V\Psi^* \dfrac{\partial \Psi}{\partial x}\right]\,dx
\end{aligned}
$$

여기서 두번째 적분이 $-\left\langle \dfrac{\partial V}{\partial x} \right\rangle$ 임은 쉽게 알 수 있다. 첫번째 적분의 두번째 term을 계속 부분적분 해 보자.
$$
\begin{aligned}
\int_{-\infty}^{\infty} \Psi^* \dfrac{\partial^3 \Psi}{\partial x^3}dx &= \left[\Psi^* \dfrac{\partial^2 \Psi}{\partial x^2}\right]_{-\infty}^\infty - \int\dfrac{\partial \Psi^*}{\partial x}\dfrac{\partial \Psi^2}{\partial x^2}\, dx \\
&=-\left[\dfrac{\partial \Psi^*}{\partial x} \dfrac{\partial \Psi}{\partial x}\right]_{-\infty}^\infty + \int_{-\infty}^\infty \dfrac{\partial^2 \Psi^*}{\partial x^2} \dfrac{\partial \Psi}{\partial x}\, dx
\end{aligned}
$$
이다. 따라서,
$$
\dfrac{d\langle p \rangle}{dt}=\left[\dfrac{\partial \Psi^*}{\partial x} \dfrac{\partial \Psi}{\partial x}\right]_{-\infty}^\infty +\left\langle -\dfrac{\partial V}{\partial x}\right\rangle
$$
이다.  $\Psi \to 0$ as $x \to \infty$ 이므로 $\partial \Psi/\partial x \to 0$ as $x \to \infty$ 이다. $-\infty$ 에 대해서도 $\Psi^*$ 에 대해서도 성립하므로,
$$
\dfrac{d\langle p \rangle}{dt}= +\left\langle -\dfrac{\partial V}{\partial x}\right\rangle
$$
이다.



<b>Problem 1.8</b> Potential energy에 constant term $V_0$ 를 포함시켰다고 하자. 고전역학에서는 아무 변화가 일어나지 않지만 양자역학에서도 그러할까? Show that the wave function picks up a time-independent phase factor : $\exp (-iV_ot/\hbar)$. What effect does this have on the expectation value of a dynamical variable?

---

Let $H_1 = -\dfrac{\hbar^2}{2m}\dfrac{\partial^2}{\partial x^2}+V(x)$ and $H_2 = H_1+V_0$. It is obvious that if $\psi_1 (x,\,t)= \phi (x)e^{-iE_1 t/\hbar}$ is a solution of $H_1$, then $\psi_2 (x,\,t) =\phi (x) e^{-i(E_1+V_0)t/\hbar}=\psi_1(x,\,t)e^{-iV_0t/\hbar}$ is a solution of $H_2$. 



<b>Problem 1.14</b> $P_{ab}(t)$ 는 시간 $t$ 일 때 입자를 $(a,\,b)$ 구간에서 발견할 확률이다. 

(a) **probability current** $J(x,\,t)$ 를 다음과 같이 정의한다.
$$
J(x,\,t)\equiv \dfrac{i\hbar}{2m}\left(\Psi \dfrac{\partial \Psi^{\ast}}{\partial x}-\Psi^* \dfrac{\partial \Psi}{\partial x}\right)
$$
이 때 다음을 보이시오.
$$
\dfrac{dP_{ab}(t)}{dt}=J(a,\,t)-J(b,\,t)\;.
$$
(b) Problem 1.9에 나온 wave function의 probability current를 구하시오.

---

(a) Wave-function 및 확률의 정의에 의해
$$
P_{ab}(t) = \int_a^b |\Psi(x,\,t)|^2dx
$$
이다. 따라서,
$$
\begin{aligned}
\dfrac{dP_{ab}}{dt} &=\dfrac{d}{dt}\int_a^b \Psi^* \Psi \,dx = \int_a^b \left[(\partial_t \Psi^*)\Psi + \Psi^*(\partial_t \Psi)
\right]\,dx \\
&=\int_a^b \left[\left(-\dfrac{i\hbar}{2m}\partial_x^2 \Psi^*+\dfrac{i}{\hbar}V\Psi^* \right)\Psi + \Psi^*\left( \dfrac{i\hbar}{2m} \partial_x^2 \Psi-\dfrac{i}{\hbar}V\Psi \right)   \right]\,dx \\
&=\dfrac{i\hbar}{2m}\int_a^b \left[\Psi^*(\partial_x^2 \Psi)-\Psi (\partial_x^2 \Psi^*)\right] \,dx\\
&= \dfrac{i\hbar}{2m} \left[ \Psi^* (\partial_x \Psi)-\Psi (\partial_x \Psi^*)\right]_a^b -\dfrac{i\hbar}{2m}\int \left[ (\partial_x \Psi^*) (\partial_x \Psi) - (\partial_x \Psi)(\partial_x \Psi^*)\right]\,dx \\
&= J(a,\,t)-J(b,\,t)\,.
\end{aligned}
$$


<b>Problem 1.15 </b>

어떤 Schroedinger 방정식의 두 solutions $\Psi_1,\,\Psi_2$ 에 대해 다음이 성립함을 보이시오.
$$
\begin{aligned}
\dfrac{d}{dt} \int_{-\infty}^{\infty} \Psi^*_1 \Psi_2 dx=0
\end{aligned}
$$

---

Let the Schroedinger eq. : $i\hbar \partial_t \Psi= - \dfrac{\hbar^2}{2m} \partial_x^2 \Psi + V\Psi$. Then,
$$
\begin{aligned}
\dfrac{d}{dt}\int_{-\infty}^\infty \Psi_1^* \Psi_2 dx &= \int_{-\infty}^{\infty} \left[ (\partial_t \Psi_1^*) \Psi_2 + \Psi_1^* (\partial_t \Psi_2)\right] \\
&= \dfrac{i\hbar}{2m} \int_{-\infty}^\infty \left[\Psi_1^* (\partial_x^2 \Psi_2)-(\partial_x^2\Psi_1^*)\Psi_2\right]\,dx \\
&=\dfrac{i\hbar}{2m} \left[\Psi_1^* (\partial_x \Psi_2)-\Psi_2 (\partial_x \Psi_1)\right]_{-\infty}^\infty \\
&\qquad\qquad - \dfrac{i\hbar}{2m} \int_{-\infty}^\infty \left[(\partial_x \Psi_1^*)(\partial_x \Psi_2)-(\partial_x \Psi_1^*)(\partial_x \Psi_2)\right]\,dx \\
&=0
\end{aligned}
$$


<b>Problem 1.17</b> 우리가 **unstable particle** 을 기술하고자 한다고 하자. 즉 "lifetime" $\tau$ 를 가지고 즉시 붕괘하는 입자를 기술한다고 하자. 이 경우 그 입자를 발견할 확률은 상수가 아니며 시간에 따라 지수적으로 감소한다. 즉,
$$
P(t) \equiv \int_{-\infty}^\infty |\Psi(x,\,t)|^2\,dx=e^{t/\tau}
$$
이다. 지금까지 우리는 potential $V$가 실함수 임을 가정해 왔다. 만약 $V=V_0-i\Gamma$ where $V_0,\,\Gamma$ are real 꼴의 복소 potential을 생각한다면 어떻게 될 것인가?

(a) 이 경우 
$$
\dfrac{dP}{dt}=-\dfrac{2\Gamma}{\hbar}P
$$
임을 보이시오.

(b) $P(t)$를 풀고 particle의 lifetime을 $\Gamma$ 를 이용하여 구하시오.

---

(a) Schroedinger eq. becomes : $i\hbar \partial_t \Psi= - \dfrac{\hbar^2}{2m} \partial_x^2 \Psi + (V_0-i\Gamma)\Psi$.

Then,
$$
\begin{aligned}
\partial_t \Psi &=\dfrac{i\hbar}{2m} \partial_x^2 \Psi -\dfrac{i}{\hbar}(V_0 -i\Gamma)\Psi\,,\\
\partial_t \Psi^* &= -\dfrac{i\hbar}{2m}\partial_x^2 \Psi^*+\dfrac{i}{\hbar}(V_0+i\Gamma)\Psi^*\,.
\end{aligned}
$$
따라서,
$$
\begin{aligned}
\dfrac{dP}{dt}
&=\dfrac{d}{dt}\int_{-\infty}^\infty |\Psi|^2\,dx \\
&=\int_{-\infty}^{\infty} \left[\Psi (\partial_t \Psi^*)+ \Psi^* (\partial_t \Psi)\right]\,dx \\
&=-\dfrac{2\Gamma}{\hbar}\int_{-\infty}^{\infty}\Psi\Psi^*\,dx = -\dfrac{2\Gamma}{\hbar}P(t)\;.
\end{aligned}
$$
(b) $P(t) = P(t=0)\exp \left(-\dfrac{2\Gamma}{\hbar} t\right)$ .



