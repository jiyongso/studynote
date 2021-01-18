I. The Wave Function
===



## 1.1 The Schroedinger Equation



## 1.2 The Statistical Interpretation



## 1.3 Probability



## 1.4 Normalization

<b>Problem 1.7 </b> $\dfrac{d\langle p\rangle}{dt}$를 계산하시오.

---

$$
\begin{align*}
\dfrac{d\langle p\rangle}{dt}&=\dfrac{d}{dt}\int \Psi^*(x,\,t) \left(-i\hbar\dfrac{\part}{\part x}\right)\Psi(x,\,t)\,dx \\
&=-i\hbar \int \left[\dfrac{\part \Psi^*}{\part t} \dfrac{\part \Psi}{\part x}+\Psi^* \dfrac{\part}{\part x}\left(\dfrac{\part \Psi}{\part t}\right)  \right]\,dx \\
&=-i\hbar \int \left[\left(-\dfrac{i\hbar}{2m}\dfrac{\part^2 \Psi^*}{\part x^2}+\dfrac{i}{\hbar}V\Psi^*\right) \dfrac{\part \Psi}{\part x}+\Psi^* \dfrac{\part }{\part x}\left(\dfrac{i\hbar}{2m} \dfrac{\part^2 \Psi}{\part x^2}-\dfrac{i}{\hbar}V\Psi\right) \right]\,dx \\
&=\dfrac{-\hbar^2}{2m} \int\left[\dfrac{\part^2 \Psi^*}{\part x^2}\dfrac{\part \Psi}{\part x} - \Psi^* \dfrac{\part^3 \Psi}{\part x^3}\right]dx+ \int\left[V\Psi^* \dfrac{\part \Psi}{\part x}-\Psi^* \dfrac{\part V}{\part x} \Psi -V\Psi^* \dfrac{\part \Psi}{\part x}\right]\,dx
\end{align*}
$$

여기서 두번째 적분이 $-\left\langle \dfrac{\part V}{\part x} \right\rangle$ 임은 쉽게 알 수 있다. 첫번째 적분의 두번째 term을 계속 부분적분 해 보자.
$$
\begin{align*}
\int_{-\infty}^{\infty} \Psi^* \dfrac{\part^3 \Psi}{\part x^3}dx &= \left[\Psi^* \dfrac{\part^2 \Psi}{\part x^2}\right]_{-\infty}^\infty - \int\dfrac{\part \Psi^*}{\part x}\dfrac{\part \Psi^2}{\part x^2}\, dx \\
&=-\left[\dfrac{\part \Psi^*}{\part x} \dfrac{\part \Psi}{\part x}\right]_{-\infty}^\infty + \int_{-\infty}^\infty \dfrac{\part^2 \Psi^*}{\part x^2} \dfrac{\part \Psi}{\part x}\, dx

\end{align*}
$$
이다. 따라서,
$$
\dfrac{d\langle p \rangle}{dt}=\left[\dfrac{\part \Psi^*}{\part x} \dfrac{\part \Psi}{\part x}\right]_{-\infty}^\infty +\left\langle -\dfrac{\part V}{\part x}\right\rangle
$$
이다.  $\Psi \to 0$ as $x \to \infty$ 이므로 $\part \Psi/\part x \to 0$ as $x \to \infty$ 이다. $-\infty$ 에 대해서도 $\Psi^*$ 에 대해서도 성립하므로,
$$
\dfrac{d\langle p \rangle}{dt}= +\left\langle -\dfrac{\part V}{\part x}\right\rangle
$$
이다.



<b>Problem 1.8</b> Potential energy에 constant term $V_0$ 를 포함시켰다고 하자. 고전역학에서는 아무 변화가 일어나지 않지만 양자역학에서도 그러할까? Show that the wave function picks up a time-independent phase factor : $\exp (-iV_ot/\hbar)$. What effect does this have on the expectation value of a dynamical variable?

---

Let $H_1 = -\dfrac{\hbar^2}{2m}\dfrac{\part^2}{\part x^2}+V(x)$ and $H_2 = H_1+V_0$. It is obvious that if $\psi_1 (x,\,t)= \phi (x)e^{-iE_1 t/\hbar}$ is a solution of $H_1$, then $\psi_2 (x,\,t) =\phi (x) e^{-i(E_1+V_0)t/\hbar}=\psi_1(x,\,t)e^{-iV_0t/\hbar}$ is a solution of $H_2$. 



<b>Problem 1.14</b> $P_{ab}(t)$ 는 시간 $t$ 일 때 입자를 $(a,\,b)$ 구간에서 발견할 확률이다. 

(a) **probability current** $J(x,\,t)$ 를 다음과 같이 정의한다.
$$
J(x,\,t)\equiv \dfrac{i\hbar}{2m}\left(\Psi \dfrac{\part \Psi^{\ast}}{\part x}-\Psi^* \dfrac{\part \Psi}{\part x}\right)
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
\begin{align*}
\dfrac{dP_{ab}}{dt} &=\dfrac{d}{dt}\int_a^b \Psi^* \Psi \,dx = \int_a^b \left[(\part_t \Psi^*)\Psi + \Psi^*(\part_t \Psi)
\right]\,dx \\
&=\int_a^b \left[\left(-\dfrac{i\hbar}{2m}\part_x^2 \Psi^*+\dfrac{i}{\hbar}V\Psi^* \right)\Psi + \Psi^*\left( \dfrac{i\hbar}{2m} \part_x^2 \Psi-\dfrac{i}{\hbar}V\Psi \right)   \right]\,dx \\
&=\dfrac{i\hbar}{2m}\int_a^b \left[\Psi^*(\part_x^2 \Psi)-\Psi (\part_x^2 \Psi^*)\right] \,dx\\
&= \dfrac{i\hbar}{2m} \left[ \Psi^* (\part_x \Psi)-\Psi (\part_x \Psi^*)\right]_a^b -\dfrac{i\hbar}{2m}\int \left[ (\part_x \Psi^*) (\part_x \Psi) - (\part_x \Psi)(\part_x \Psi^*)\right]\,dx \\
&= J(a,\,t)-J(b,\,t)\,.

\end{align*}
$$


<b>Problem 1.15 </b>

어떤 Schroedinger 방정식의 두 solutions $\Psi_1,\,\Psi_2$ 에 대해 다음이 성립함을 보이시오.
$$
\begin{align*}
\dfrac{d}{dt} \int_{-\infty}^{\infty} \Psi^*_1 \Psi_2 dx=0

\end{align*}
$$

---

Let the Schroedinger eq. : $i\hbar \part_t \Psi= - \dfrac{\hbar^2}{2m} \part_x^2 \Psi + V\Psi$. Then,
$$
\begin{align*}
\dfrac{d}{dt}\int_{-\infty}^\infty \Psi_1^* \Psi_2 dx &= \int_{-\infty}^{\infty} \left[ (\part_t \Psi_1^*) \Psi_2 + \Psi_1^* (\part_t \Psi_2)\right] \\
&= \dfrac{i\hbar}{2m} \int_{-\infty}^\infty \left[\Psi_1^* (\part_x^2 \Psi_2)-(\part_x^2\Psi_1^*)\Psi_2\right]\,dx \\
&=\dfrac{i\hbar}{2m} \left[\Psi_1^* (\part_x \Psi_2)-\Psi_2 (\part_x \Psi_1)\right]_{-\infty}^\infty \\
&\qquad\qquad - \dfrac{i\hbar}{2m} \int_{-\infty}^\infty \left[(\part_x \Psi_1^*)(\part_x \Psi_2)-(\part_x \Psi_1^*)(\part_x \Psi_2)\right]\,dx \\
&=0


\end{align*}
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

(a) Schroedinger eq. becomes : $i\hbar \part_t \Psi= - \dfrac{\hbar^2}{2m} \part_x^2 \Psi + (V_0-i\Gamma)\Psi$.

Then,
$$
\begin{align*}
\part_t \Psi &=\dfrac{i\hbar}{2m} \part_x^2 \Psi -\dfrac{i}{\hbar}(V_0 -i\Gamma)\Psi\,,\\
\part_t \Psi^* &= -\dfrac{i\hbar}{2m}\part_x^2 \Psi^*+\dfrac{i}{\hbar}(V_0+i\Gamma)\Psi^*\,.

\end{align*}
$$
따라서,
$$
\begin{align*}
\dfrac{dP}{dt}
&=\dfrac{d}{dt}\int_{-\infty}^\infty |\Psi|^2\,dx \\
&=\int_{-\infty}^{\infty} \left[\Psi (\part_t \Psi^*)+ \Psi^* (\part_t \Psi)\right]\,dx \\
&=-\dfrac{2\Gamma}{\hbar}\int_{-\infty}^{\infty}\Psi\Psi^*\,dx = -\dfrac{2\Gamma}{\hbar}P(t)\;.
\end{align*}
$$
(b) $P(t) = P(t=0)\exp \left(-\dfrac{2\Gamma}{\hbar} t\right)$ .



