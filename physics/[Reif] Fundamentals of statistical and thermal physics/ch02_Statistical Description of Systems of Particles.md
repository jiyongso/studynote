II. Statistical Description of Systems of Particles
===



## 1. 기본 개념



#### Equillibrium

 어떤 *Isolated system* 에서 가능한 microstates 를 $r_1,\,r_2,\ldots$ 라 할 때, 이 시스템이  microstate에 존재할 확률이 시간에 따라 변하지 않는 상태를 **equillibrium** 이라 한다. 따라서 Macroscopic parameter의 값들이 시간에 따라 변하지 않는다.



#### Fundamental Postulate of Statistical Mechanics

An isolated system in equillibrium is equally likely to be in any of its accessible state



#### Relaxation Time

Unequillibrium 상태에서 equillibrium 상태로 가는데 필요한 시간.



#### Symbols and Probability

- $\Omega(E)$ : Isolated system이 그 에너지가 $[E,\, E+\delta E]$ 사이에 존재할 때의 상태의 갯수.
- $\Omega(E,\, y_k)$ : 시스템의 parameter $y$ 가 $y_k$ 의 값을 가지며 그 에너지가 $[E,\, E+\delta E]$ 에 존재할 때의 상태의 갯수.

Fundamental postulate 에 따라 시스템의 parameter $y$ 가 $y_k$ 값을 가질 확률은 다음과 같다.
$$
P(y_k) = \dfrac{\Omega (E,\, y_k)}{\Omega (E)}\;.
$$
따라서 앙상블에서의 $y$ 의 평균값 $\overline{y}$ 는 다음과 같다.
$$
\overline{y} = \dfrac{\displaystyle\sum_k y_k \Omega (E,\, y_k)}{\Omega(E)}\;.
$$


#### Macroscopic system

- Macroscopic system = degree of freedom이 매우 큰 시스템.



#### Density of State $\omega (E)$ 

$$
\Omega (E)= \omega (E) \,\delta E
$$





#### External Parameters

Hamiltonian 에 포함되는 macroscopically measurable indepedent parameters



#### Quasi-Static Process

반응이 relaxation time $\tau$ 보다 매우 느려서 process의 각 순간이 equillibrium과 매우 근접한 process.



## Problems



<b>2.3 </b> Classical 1D harmonic osciilators 의 ensemble을 생각한다.

(a) Oscillator의 displacement $x$ 가 시간 $t$ 의 함수로 $x=A \cos (\omega t + \varphi)$ 로 주어졌다. Phase angle $\varphi$ 는 oscillator 마다 $0<\varphi < 2 \pi$ 에서 equally likely 하다고 하자. 즉 phase angle $\varphi$ 의 확률밀도함수 $w(\varphi)d\varphi = \dfrac{1}{2\pi}d\varphi$ 이다. 어떤 fixed time $t$ 에 대해 $x$ 가 $x$ 와 $x+dx$ 사이에 존재할 확률 $P(x)dx$ 를 구하여라. $P(x)$ 를 $A$ 와 $x$ 의 함수로 나타내어라.

(b) Oscillators 의 에너지가 각각 $E$ 와 $E+\delta E$ 사이 일 때, 이 ensemble의 classical phase diagram 을 그려라. $P(x)dx$ 를 전체 면적에서 displacement 가 $x$ 와 $x+dx$ 사이에 존재할 면적의 비율을 통하여 구하고 $P(x)$ 를 $E$ 와 $x$ 로 표현하시오 이 값이 (a) 에서 구한 값과 같음을 보이시오.

----

(a) $t$ 가 $-\varphi/\omega$ 에서 $\pi/\omega-\varphi/\omega$ 까지 변할 때 $x$ 는 $A$ 에서 $-A$ 까지 변한다. $x$ 가 $x_0$ 와 $x_0+dx$ 사이에 있는 시간은 $\left|\left(\dfrac{dt}{dx}\right)_0\right| dx$ 이므로,
$$
P(x)dx = \dfrac{1}{\pi} \dfrac{dx}{A \sin (\omega t+\varphi)}=\dfrac{1}{\pi}\dfrac{dx}{\sqrt{A^2-x^2}} \,,\qquad (\varphi-\text{independent.})
$$
이다.

(b) $E =\dfrac{m\omega ^2 A^2}{2} = \dfrac{p^2}{2m}+\dfrac{m\omega^2}{2}x^2$ 이며 $x,\,p$-space 에서 그 면적이 $A_E=2\pi E/\omega$ 인 타원이다. Phase space 에서 에너지가 $E$ 와 $E+\delta E$ 인 부분의 면적은 $A_{E+\delta E}-A_E=2\pi \delta E/\omega$ 이다. 에너지가 $E$ 일 때의 $p$ 를 $x$ 에 대한 함수로 표한현 것을 $p_{E}(x)$ 라 하면,
$$
\begin{aligned}
P(x)dx &= \dfrac{2(p_{E+\delta E}(x)-p_E(x))}{2\pi \delta E/\omega} dx \\
&= \dfrac{\omega \sqrt{2m}}{\pi \delta E} \left(\sqrt{(E+\delta E)- \dfrac{m\omega^2}{2}x^2} - \sqrt{E-\dfrac{m\omega^2}{2}x^2}\right) dx \\
&= \dfrac{\omega \sqrt{2m}}{\pi \delta E} \dfrac{\delta E}{2\sqrt{E-\dfrac{m\omega^2}{2}x^2}} dx \\
&=\dfrac{\omega}{2\pi} \dfrac{\sqrt{2m}}{\sqrt{\dfrac{m\omega^2}{2}(A^2-x^2)}} dx \\
&= \dfrac{1}{\pi}\dfrac{1}{\sqrt{A^2-x^2}}\,dx

\end{aligned}
$$


<b>2.4 </b> 스핀 $1/2$ 이며 서로 interaction이 매우 작은 localized 된 $N$ 개의 입자로 이루어진 isolated system을 생각한다.  각각의 입자는 magnetic moment $\mu$ 를 가지며 applied field $H$ 에 parallel 하거나 antiparallel 하다. $n_1$ 을 $H$ 와 parallel 한 입자의 갯수, $n_2$ 를 antiparalle 한 입자의 갯수라 하면 시스템의 에너지 $E$ 는 $E=-(n_1-n_2)\mu H$ 로 주어진다.

(a) $E$ 와 $E+\delta E$ 사이의 에너지 영역을 생각하자. 여기서 $|\delta E| \ll |E|$ 이며 $|\delta E | \ll |\mu H|$ 이다. 이 에너지 영역에서의 total number of states $\Omega (E)$ 는 무엇인가?

(b) $\ln \Omega (E)$ 를 $E$ 의 함수로 표현하고 Stirling's formula 를 사용하여 간단히 하라.

(c) 에너지 $E$ 가 $\ln \Omega (E)$ 가 appriciable 한 영역에 있다고 가정하자. 즉 $E$ 가 $-N\mu H$ 나 $N\mu H$ 와 너무 가깝지 않다. 이 경우 Gaussian approximation을 사용하여 $\Omega(E)$ 를 $E$ 에 대한 간단한 함수꼴로 나타내시오.

---

(a) $E=-(n_1-n_2)\mu H = -(2n_1-N)\mu H$. 즉, $n_1= \dfrac{1}{2}\left(N-\dfrac{E}{\mu H}\right)$.  $\Omega (n_1)=\dfrac{N!}{n_1!(N-n_1)!} $  이므로,
$$
\Omega(E)=\dfrac{N!}{\left(\dfrac{N}{2}-\dfrac{E}{2\mu H}\right)! \left( \dfrac{N}{2}+\dfrac{E}{2\mu H} \right)!} \dfrac{\delta E}{2 \mu H}
$$
(b) Stirling's formula : $n \gg 1 \implies \ln (n!)=n \ln n - n$ 
$$
\begin{aligned}
\ln \Omega(E) &= N\ln N-N-\left(\dfrac{N}{2}-\dfrac{E}{2\mu H}\right)\ln \left(\dfrac{N}{2}-\dfrac{E}{2\mu H}\right) +\left(\dfrac{N}{2}-\dfrac{E}{2\mu H}\right) \\ &\quad-\left(\dfrac{N}{2}+\dfrac{E}{2\mu H}\right)\ln \left(\dfrac{N}{2}+\dfrac{E}{2\mu H}\right) +\left(\dfrac{N}{2}+\dfrac{E}{2\mu H}\right) +\ln \left(\dfrac{\delta E}{2\mu H}\right) \\
&= N\ln N + \ln \left(\dfrac{\delta E}{2\mu H}\right)-\left(\dfrac{N}{2}-\dfrac{E}{2\mu H}\right)\ln \left(\dfrac{N}{2}-\dfrac{E}{2\mu H}\right)-\left(\dfrac{N}{2}+\dfrac{E}{2\mu H}\right)\ln \left(\dfrac{N}{2}+\dfrac{E}{2\mu H}\right)

\end{aligned}
$$
(c) $\dfrac{d}{dE}\ln \Omega (E)=0 \implies E=0 \implies n_1=n_2=\dfrac{N}{2}$. 
$$
\begin{aligned}
\dfrac{d}{dE}\ln \Omega (E) &= \dfrac{1}{2\mu H} \left[\ln \left(N-\dfrac{E}{\mu H}  \right)- \ln \left(N+\dfrac{E}{\mu H}  \right)  \right] \,,\\
\dfrac{d^2}{dE} \ln \Omega (E) &= -\dfrac{1}{2\mu^2H^2} \left[\dfrac{1}{N-E/\mu H}+ \dfrac{1}{N+E/\mu H}\right]\;.

\end{aligned}
$$
 $\left(\dfrac{d^2}{dE^2} \ln \Omega (E)\right)_{E=0}=-\dfrac{1}{N\mu^2H^2}$ 이므로
$$
\ln \Omega(E) \approx \ln \left( \Omega(0)\right) -\dfrac{1}{2N\mu^2H^2}E^2 = \ln \left[ \Omega (0) \exp \left(-\dfrac{E^2}{2N\mu^2H^2}\right) \right ]
$$
여기서 $\Omega(0)$ 를 Stirling's formulae $n! = \sqrt{2 \pi n}\,n^n e^{-n}$ 을 사용하여 계산하면,
$$
\Omega(0)=\dfrac{N!}{(N/2)!(N/2)!}\dfrac{\delta E}{2 \mu H}=\dfrac{\sqrt{2\pi N}\, N^N e^{-N}}{ 2 \pi (N/2) (N/2)^N e^{-N}}\dfrac{\delta E}{2\mu H}= \sqrt{\dfrac{2}{N\pi}}2^N \dfrac{\delta E}{2\mu H}
$$
따라서,
$$
\Omega (E)=\sqrt{\dfrac{2}{\pi N}}2^N \exp\left(- \dfrac{E^2}{2 N \mu^2 H^2}\right)\dfrac{\delta E}{2 \mu H}\;.
$$


<b>2.7 </b> 각 변의 길이가 $L_x,\,L_y,\,L_z$ 인 직육면체 potential box를 생각하자. 입자가 $L_x=L_y=L_z$ 인 정육면체에서 움직이며 가능한 에너지 레벨은 다음과 같다.
$$
E=\dfrac{\hbar^2}{2m} \pi^2 \left(\dfrac{{n_x}^2}{{L_x}^2}+\dfrac{{n_y}^2}{{L_y}^2}+ \dfrac{{n_z}^2}{{L_z}^2}\right)\;.
$$
(a) 입자는 세 정수 $n_x,\,n_y,\,n_z$ 에 의해 상태가 특정된다고 하자.  $L_x$ 가 quasitstatically 변할 때 에너지가 어떻게 변하는지 고려하여 $x$ 축에 수직인 방향으로 가해지는 힘은 $F_x = - \partial E/\partial L_x$ 로 주어짐을 보이시오.

(b) 벽에 가해지는 압력(force per unit area) 를 계산하라. 모든 가능한 상태를 평균하여 벽에 가해지는 평균 압력에 대한 식을 구하라. 이 평균 압력이 평균 에너지 $\overline{E}$ 와 box 의 부피  $V=L_xL_yL_z$ 로 표현 될 수 있음을 보여라.

---

(a) trivial

(b) $F_x = -\dfrac{\hbar^2}{2m}\pi ^2 \cdot \left(-2 \dfrac{{n_x}^2}{{L_x}^3}\right)$ , $p= \dfrac{F_x}{L_yL_z}=\dfrac{\pi^2\hbar^2 }{mV} \left(\dfrac{{n_x}^2}{{L_x}^2}\right)$. $L_x=L_y=L_z,\, \overline{n_x}=\overline{n_y}=\overline{n_z}=\overline{n}$ 이면,
$$
\overline{E}=\dfrac{3\pi^2\hbar^2}{2m}\dfrac{\overline{n}^2}{L^2}=\dfrac{3}{2}\overline{p}V\implies \overline{p}=\dfrac{2}{3} \dfrac{\overline{E}}{V} 
$$
<b>2.10</b> Thermall insulated amount of gas 의 평균 압력 $\overline{p}$ 와 부피 $V$ 가 어떤 상수 $\gamma,\, K$ 에 대해  $\overline{p}V^\gamma=K$ 를 만족한다. 압력 $\overline{p}_i$ 부피  $V_i$ 에서 압력 $\overline{p}_f$, 부피 $V_f$ 로 quasi static process 를 거쳤을 때 이 gas가 한 일을 구하시오.

---

$$
W=\int_{V_i}^{V_f} \overline{p}\,dV=\int_{V_i}^{V_f} KV^{-\gamma}\,dV= \dfrac{K}{1-\gamma}\left(V_f^{1-\gamma}-V_i^{1-\gamma}\right)=\dfrac{1}{1-\gamma} \left(\overline{p}_f V_f-\overline{p}_i V_i \right)
$$



<b>2.11 </b> (see the figure in the text) 주변과의 열교환이 없는 Quasi-static process $A \to B$ 에서는 평균 압력 $\overline{p}$ 와 부피 $V$ 는 어떤 상수  $\alpha$ 에 대해 $\overline{p}=\alpha V^{-5/3}$ 의 관계를 갖는다고 한다. 아래의 세가지 프로세스 각각에 대해 quasi-static work과 net heat absorbed  by this system 을 구하시오.

(a) 이 시스템이 원래 부피에서 마지막 부피까지 압력이 일정하게 유지된 상태에서 팽창한후, 부피가 일정하게 유지된 상태에서 압력이 $10^6 \text{dynes cm}^{-2}$ 까지 변한다.

(b) 부피가 감소하는데 압력이 부피에 비례하도록 열이 공급된다.

(c) (a) 의 두 과정의 전후가 바뀐 순서로 진행된다.

---

$1 \text{dynes} = 10^{-5} \text{N}$, $1 \text{cm}^{-2}= 10^4 \text{m}^{-2}$ , $1 \text{cm}^{3}=10^6 \text{m}^3$.

Diagram in the text 로부터  $\overline{p}=\alpha V^{-5/3}$ 의 $\alpha$ 를 구하면 $\alpha=32$ 

For the adiabatic process, $W_{adiabatic}= \int_{V_i}^{V_f} \overline{p}dV=\int_{V_i}^{V_f} \alpha V^{-5/3}\,dV=-\dfrac{3}{2}\alpha ({V_f}^{-2/3}-{V_i}^{-2/3} )=-3600 \text{ J}$ . $\Delta Q=0$ 이므로 $\Delta E=-3,600 J$ 

(a)  $\Delta W_a=3.2\times 7 \times 10^3 \textrm{J} = 22400 \textrm{ J} $, $\Delta Q_a = \Delta E + \Delta W_a=-3600+22400=1800 \textrm{ J}$

(b) $\overline{p}=-\dfrac{31}{7}(V-1)+32=-\dfrac{31}{7}V+\dfrac{255}{7}$, $\Delta W_b= \displaystyle \int_{32}^1 \left(\dfrac{255-31V}{7}\right)   dV=11550 \textrm{ J}$.

 

 