Chapter 6. Radioactive Decay
===



# 6.1 The Radioactive Decay Law



## 6.1.1. Simple Case : $A\to A'$​ decay and $A'$​ is stable

- 시간 $t$​​​ 에서의 $A$​​​ 입자의 갯수를 $N(t)$​​​ 라 하고 $N(0)=N_0$​​​ 라 하자. $t$​​​ 와 $t+dt$​​​ 시간동안의 decay 횟수는 남은 $A$​​ 의 갯수 $N(t)$​​​ 에 비례한다고 가정하는 것은 reasonable 하다. 이때의 감소하는 상수를 $\lambda>0$​​ 라 하면, 
  $$
  \dfrac{dN(t)}{dt}= -\lambda N(t)
  $$
  가 될 것이다. 이 미분방정식의 해는 
  $$
  N(t) = N_0 e^{-\lambda t}
  $$
  이다. 이제 $A$​ 입자의 평균 생존 시간 $\tau$​ 를 생각하자. $A$ 입자 하나가 $t$ 까지 decay 하지 않고 살아 있을 확률이 $e^{-\lambda t}$ 에 비례하므로, 
  $$
  \tau = \dfrac{\displaystyle \int_0^\infty te^{-\lambda t}\, dt}{\displaystyle \int_0^\infty e^{-\lambda t}\,dt}= \dfrac{1}{\lambda}
  $$
  이다. 따라서,
  $$
  N(t) = N_0 e^{-t/\tau}
  $$
  로 쓸 수 있다. 



- $A \to A'$ decay 만을 고려할 때 undecayed nuclei 의 숫자를 측정하고 싶다고 하자. 이것을 직접 측정하는 것은 매우 어려우므로 시간 $t$ 와 $t+\Delta t$ 동안 발생하는 decay process 의 숫자를 측정함으로서 $A$ 의 갯수를 예측 할 수 있다. 즉
  $$
  |\Delta N| = N(t)-N(t+\Delta t)=N_0 e^{-t/\tau } \left( 1- e^{-\Delta t/\tau}\right)
  $$
  를 이용한다. 그런도 보통 $\Delta t \ll \tau$​ 이며 이 경우, (테일러 전개를 이용하면)
  $$
  |\Delta N|= \dfrac{1}{\tau} N_0 e^{-t/\tau} (\Delta t)
  $$
  가 된다. 이 경우 $\Delta t \to 0$ 극한에서,
  $$
  \left|\dfrac{dN}{dt}\right|=\dfrac{1}{\tau}N_0 e^{-\lambda t}
  $$
  가 된다. 



#### Activity and unit Curie

단위 시간에 발생하는 decay process 의 홧수를 **activity** $\mathscr{A}$​​ 라 하며 단위는 베크렐 (Bq) 이다 . 당연히 
$$
\mathscr{A}(t) = \left|\dfrac{dN(t)}{dt}\right|=\dfrac{1}{\tau}N_0 e^{-t/\tau} \equiv \mathscr{A}_0 e^{-t/\tau}
$$
이다. 이 때 시간 $(t_1,\,t_2)$ 사이에 발생하는 decay 의 횟수 $\Delta N$ 은
$$
\Delta N = \int_{t_1}^{t_2} \mathscr{A}(t)\, dt
$$
가 된다. Activity 의 단위로 초당 $3.7 \times 10^{10}$  번의 decay 가 일어나는 activity 를 $1$ Curie 로 정의하여 사용하기도 한다. 

- Activity 는 단위 시간당 발생하는 decay 의 횟수에 대한 정보일 뿐 decay 의 종류, 방출되는 방사선의 종류 및 에너지와는 무관하다. 



#### Half life $t_{1/2}$

소위 반감기, 즉 $N(t_{1/2})=\frac{1}{2}N_0$​ 가 되는 시간 $t_{1/2}$ 를 반감기라 하며,
$$
t_{1/2}= 0.693 \,\tau
$$
이다. 



## 6.1.2. $A\to A_1,\, A\to A_2$​ case	

- 즉 initial nucleus $A$ 가 $A_1$ 으로 decay 하거나 $A_2$ 로 decay 할 경우를 살펴보자. $A$ 가 $A_1$ 혹은 $A_2$ 로 decay 하며, 시간 $t$  에서의 $A$ 입자의 갯수를 $N(t)$ 라 하고, $N(t=0)=N_0$​ 라 하자. 이 때, 

$$
\begin{aligned}
\dfrac{1}{\tau_1}=\lambda_1 &= \dfrac{-(dN/dt)_1}{N} \\
\dfrac{1}{\tau_2}=\lambda_2 &= \dfrac{-(dN/dt)_2}{N}
\end{aligned}
$$

으로 정의하고 $\lambda_1,\,\lambda_2$ 를 각각 *partical decay constant* 라 하자. 그렇다면 Total decay rate $\left(\dfrac{dN}{dt}\right)_{tot}$ 는
$$
-\left(\dfrac{dN}{dt}\right)_{tot} = -\left(\dfrac{dN}{dt}\right)_1-\left(\dfrac{dN}{dt}\right)_2=(\lambda_1+\lambda_2)N
$$
이므로 
$$
N(t)=N_0 e^{-(\lambda_1+\lambda_2)t} = N_0 e^{-\lambda_t t}
$$
이다. 이 때 $\lambda_t=\lambda_1+\lambda_2$  를 *total decay rate* 라 부른다. $A_1$  의 갯수를 $N_1(t),\, A_2$ 의 갯수를 $N_2(t)$ 라 하면,
$$
-\left(\dfrac{dN}{dt}\right)_1 = \dfrac{dN_1}{dt},\qquad -\left(\dfrac{dN}{dt}\right)_2 = \dfrac{dN_2}{dt}
$$
이므로, 
$$
\begin{aligned}
N_1 (t) &= \dfrac{\lambda_1}{\lambda_{t}} N_0 \left(1-e^{-\lambda_t t}\right) \\
N_2 (t) &= \dfrac{\lambda_2}{\lambda_{t}} N_0 \left(1-e^{-\lambda_t t}\right)
\end{aligned}
$$
이다.



# 6.2 Quantum Theory of Radiative Decays



흔한 perturbation theory



# 6.3 Production and Decay of Radioactivity



- Exponential decay 가 성립하지 않는 상황이 자주 있다. 예를 들어 원자로나 가속기에서 radioactive nucleus 를 생산할 때. 



- $N_0$ 개의 target atom 에 current $I$ 의 입자를 입사시키며 target atome 의 입사 입자에 대한 cross-section 이 $\sigma$ 라 하자. $N_0 \sim 10^{24}$ 이며 $I \sim 10^{14} /\text{cm}^2\cdot\text{s}$ 이고 $\sigma \sim 10^{-24} \text{cm}^2$​ 이다. 즉 초당 $10^{14}$ 개 정도 변환 될 수 있는데 이는 확률적으로 $10^{-10}$  이므로 매우 작다. 수시간 정도 입사시킨다 하더라도 10<sup>-6</sup> 이므로 매우 작아서 transition rate $R$ 을 상수로 놓을 수 있다. 즉,
  $$
  R=N_0 \sigma I
  $$
  로 놓을 수 있다.

- 이 반응으로 생성되는 radioactive nuclei 의 갯수를 $N_1$ 이라 하자. 이 nuclei가 $\lambda_1$ 의 decay constant 로 stable nuclei 로 변환된다고 하고 이 때 stable nuclei 의 갯수를 $N_2$ 라 하면, 

$$
dN_1 = Rdt-\lambda_1N_1dt
$$

​		의 미분방정식을 만족하므로, $N_1(t)$  와 $\mathscr{A}(t)$ 는 아래와 같이 쓸 수 있다.
$$
\begin{aligned}
N_1 (t) &= \dfrac{R}{\lambda_1} \left(1-e^{-\lambda_1 t}\right) \\
\mathscr{A}(t) &= \lambda_1 N_1(t) = R\left(1-e^{-\lambda_1 t}\right)

\end{aligned}
$$
​		$t\ll 1/\lambda_1 \approx 1/t_{1/2}$ 이면, 다음과 같은 근사가 성립한다. 
$$
\mathscr{A}(t) \approx R\lambda_1 t
$$
​		역으로 $ t \gg 1/\lambda_1 \approx 1/t_{1/2}$​​ 이면, 다음 근사가 ㅅㅓㅇ립한다. 
$$
\mathscr{A}(t) \approx R
$$
