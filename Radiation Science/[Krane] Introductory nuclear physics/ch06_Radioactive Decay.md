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



## 6.1.2. $A\to B_1,\, A\to B_2$​​ case	

- 즉 initial nucleus $A$​ 가 $B_1$​ 으로 decay 하거나 $B_2$​ 로 decay 할 경우를 살펴보자. 시간 $t$​  에서의 $A$​ 입자의 갯수를 $N(t)$​ 라 하고, $N(t=0)=N_0$​ 라 하자. 이 때, $B_1$​  의 갯수를 $N_1(t),\, B_2$​ 의 갯수를 $N_2(t)$​ 라 하면,

$$
\begin{aligned}
\dfrac{1}{\tau_1}=\lambda_1 &= \dfrac{-dN_1/dt}{N} \\
\dfrac{1}{\tau_2}=\lambda_2 &= \dfrac{-dN_2/dt_2}{N}
\end{aligned}
$$

으로 정의하고 $\lambda_1,\,\lambda_2$​ 를 각각 *particle decay constant* 라 하자. 그렇다면 Total decay rate $\left(\dfrac{dN}{dt}\right)_{tot}$​ 는
$$
-\left(\dfrac{dN}{dt}\right)_{tot} = -\left(\dfrac{dN_1}{dt}\right)-\left(\dfrac{dN_2}{dt}\right)=(\lambda_1+\lambda_2)N
$$
이므로 
$$
\begin{aligned}
N(t) & = N_0 e^{-(\lambda_1+\lambda_2)t} = N_0 e^{-\lambda_t t}\\
N_1 (t) &= \dfrac{\lambda_1}{\lambda_{t}} N_0 \left(1-e^{-\lambda_t t}\right) \\
N_2 (t) &= \dfrac{\lambda_2}{\lambda_{t}} N_0 \left(1-e^{-\lambda_t t}\right) 
\end{aligned}
$$


# 6.2 Quantum Theory of Radiative Decays



흔한 perturbation theory



# 6.3 Production and Decay of Radioactivity



- Exponential decay 가 성립하지 않는 상황이 자주 있다. 예를 들어 원자로나 가속기에서 radioactive nucleus 를 생산할 때. 



- $N_0$ 개의 target atom 에 current $I$ 의 입자를 입사시키며 target atom 의 입사 입자에 대한 cross-section 이 $\sigma$ 라 하자. $N_0 \sim 10^{24}$ 이며 $I \sim 10^{14} /\text{cm}^2\cdot\text{s}$ 이고 $\sigma \sim 10^{-24} \text{cm}^2$​ 이다. 즉 초당 $10^{14}$ 개 정도 변환 될 수 있는데 이는 확률적으로 $10^{-10}$  이므로 매우 작다. 수시간 정도 입사시킨다 하더라도 10<sup>-6</sup> 이므로 매우 작아서 transition rate $R$ 을 상수로 놓을 수 있다. 즉,
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
​		역으로 $ t \gg 1/\lambda_1 \approx 1/t_{1/2}$​​ 이면, 다음 근사가 성립한다. 
$$
\mathscr{A}(t) \approx R
$$

# 6.4 Growth of Daughter Activity



- Radioactive decay 의 결과로 radioactive materials 가 생성될 때. 즉 $A_1 \to A_2 \to A_3  \to \cdots $ 라 하고 시간 $t$ 에서 $A_i$ 의 갯수를 $N_i(t)$ 라 하며, 
  $$
  N_1(t=0)=N_0,\qquad N_2(t=0)=N_3(t=0)=\cdots = 0
  $$

- $\lambda_i,\, \tau _i$ 를 다음과 같이 정의한다.
  $$
  \lambda_i = \dfrac{1}{\tau_i}= -\dfrac{dN_{i}/dt}{N_{i}}= \dfrac{dN_{i+1}/dt}{dN_i}
  $$

- 이로부터 다음과 같은 미분방정식을 얻는다.

$$
\begin{array}{rll}
\dfrac{dN_1}{dt} &= -\lambda_1 N_1 & i=1.\\
\dfrac{dN_i}{dt} & = -\lambda_iN_i +\lambda_{i-1}{N_{i-1}} \qquad& i=2,\,3,\,4,\ldots
\end{array}
$$

초기조건과 함께 위의 미분방정식을 풀면, 
$$
\begin{aligned}
N_1 (t) &= N_0e^{-\lambda_1t}  \\
N_2(t) &= \dfrac{\lambda_1 N_0}{\lambda_1-\lambda_2}\left(e^{-\lambda_2 t} - e^{-\lambda_1 t}\right)
\end{aligned}
$$
를 얻는다. 

- $\lambda_1 \ll \lambda_2$​  일 경우 $N_1(t) \approx N_0=\text{const.}$​ 이며 $N_2(t)  \simeq    N_0 \dfrac{\lambda_1}{\lambda_2}(1-e^{-\lambda_2 t})$​ 
- $\lambda_1 > \lambda_2$ 이며 $t \gg 1/\lambda_1$ 일 경우 $N_1 \approx 0$ 이므로 $N_2 (t) \eqsim N_0 \dfrac{\lambda_1}{\lambda_1-\lambda_2} (e^{-\lambda_2}t)$ 로 exponential decay 한다. 



#### Series of Decays

$A_1 \to A_2 \to \cdots \to A_n$​ 까지의 series of decays 와 초기조건 $N_1(0)=N_0,\,N_2(0)=\cdots = N_n(0)=0$  에 대한 해는 Bateman equation 이며 다음과 같다. 
$$
N_n (t) = N_0 \times \left(\prod _{i=1}^{n-1} \lambda_i\right) \times \sum_{k=1}^n \dfrac{e^{-\lambda_k t}}{\displaystyle \prod_{j=1,\, j \ne k} (\lambda_j-\lambda_k)} =\sum_{k=1}^n \dfrac{c_k N_0}{\lambda_n} e^{-\lambda_k t} \qquad\text{where} \, c_k = \dfrac{\displaystyle \prod _{i=1}^{n} \lambda_i}{\displaystyle \prod_{j=1,\, j \ne k} (\lambda_j-\lambda_k)}
$$
이때의 $n$-th member 에 대한 radioactivity $\mathscr{A}_n$​ 은
$$
\mathscr{A}_n = \lambda_n N_n (t) = N_0 \left(\sum_{k=1}^n c_k e^{-\lambda_k t}\right)  
$$
이다.



# 6.5 Types of Decays



## 6.5.1 $\alpha$-decay

$$
{}^A_Z\text{X}_N \to {}^{A-4}_{Z-2}\text{X}'_{N-2} + {}^{4}_2 \text{He}_{2}
$$

- Example 

$$
^{226}_{\,\;88}\text{Ra}_{138} \to ^{222}_{\,\;86}\text{Rn}_{136}+\alpha
$$

이 때 반감기는 1,600 년 정도이며 알파 입자 에너지는 대략 4.8 MeV 정도 이다. 



## 6.5.2 $\beta$​-decay

$$
\begin{aligned}
\text{n}& \to \text{p}+e^- \qquad & \beta^- \text{ decay}\qquad\qquad\; \\
\text{p}& \to \text{n}+e^+ & \beta^+ \text{ decay} \qquad \qquad\;\\
\text{p}+e^- &\to \text{n} & \text{electron capture} (\varepsilon)

\end{aligned}
$$



- 위의 세 과정에서는 *neutrino* 가 방출되지만 neutrino 는 전하가 없므로 최종 산물에 영향을 끼치지 않는다. 그래서 표기하지 않는다. 
- 여기서의 전자 혹은 반전자는 원래 원자에 있던 것이 아닌 새롭게 생성된 것이다. 



- Representative $\beta$-decay
  $$
  \begin{aligned}
  {}^{131}_{\;\,53}\text{I}_{78} &\xrightarrow[\beta^-]{} {}^{131}_{\;\,54}\text{Xe}_{77}  & t_{1/2}=8.0\,\text{d} \\
  ^{25}_{13}\text{Al}_{12} &\xrightarrow[\beta^+]{} {}^{25}_{12}\text{Mg}_{13}   & t_{1/2}= 7.2\,\text{d} \\
  ^{54}_{25}\text{Mn}_{29} &\xrightarrow[\varepsilon]{} {}^{54}_{24}\text{Cr}_{30}    & t_{1/2}= 312\, \text{d}
  \end{aligned}
  $$
  

## 6.5.3 $\gamma$-decay

- $\gamma$​ emission 은 excited bound states ($A>5$) 를 가진 모든 핵에서 발견되며 보통 $\alpha$ or $\beta$ decay 이후에 발생한다. 
- $\gamma$ emission 의 반감기는 매우 짧아서 보통 $10^{-9}$ 초 이하이지만 때때로 시간, 혹은 일 단위 일 때도 있다. 이렇게 긴 transition 을 *isomeric transitions* 라 하고 이 때의 excited states 를 *isomeric states* 혹은 *isomer*, *metastable states* 라 하기도 한다. 
- $\gamma$- decay 와 경쟁하는 것은 **internal conversion** 인데 이것은 핵의 transition energy 가 전자로 옮겨져서 자유전자로 방출되는 것을 말한다. ($\beta$- decay 는 전자가 생성되는것, internal conversion 은 기존의 전자가 방출되는것 이다.) 따라서 internal conversion 은 핵종을 바꾸지 않고 원자가 이온화 된다.



## 6.5.4 Spontaneous Fission



## 6.5.5 Nucleon Emission



## 6.5.6 Branching Ratios and Partial Half-lives

- 어떤 핵은 하나의 프로세스로 decay 하지만 어떤 핵은 여러 decay modes 가 경쟁적으로 발생한다. 이 상대적인 퍼센트 비율을 **branching ratio** 라 한다. 혹은 decay constant (or partial half-life) 로 표현할 수도 있다. 



# 6.6 Natural Radioactivity





# 6.7 Radioactive Dating

