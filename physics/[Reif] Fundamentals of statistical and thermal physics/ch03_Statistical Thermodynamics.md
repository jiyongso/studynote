III. Statistical Thermodynamics
===



## 1. Two Systems with Thermal Contact



- 두 시스템 $A_1,\,A_2$ 가 서로 isolated and in equillibrium 이었다가 thermally contact 된다고 하자. $A \equiv A_1+A_2$ 라 하고 isolated 되어 있을 때의 에너지를 각각 $E_1,\,E_2$ 라 하자.

- Themal contact 이전 $A_1$ system 의 에너지가 $E_1$ 과 $\delta E_1$ 사이에 있을 때의 microstates 의 갯수를 $\Omega_1 (E_1)$ 이라 한다. $A_2$ 의 에너지가 $E_2$ 와 $\delta E_2$ 사이에 있을 때의 microstates 의 갯수를 $\Omega_2 (E_2) $ 라 한다. 이 때의  $A$ 의 총 microstates 의 갯수를 $\Omega_i (E=E_1+E_2)$ 라 할 때 이 macrostate에 존재할 확률 $P_i(E)$ 는 다음과 같다. 
  $$
  P_i(E_1)=\dfrac{\Omega_i(E)}{\Omega (E)}=\dfrac{\Omega_1(E_1)\Omega_2(E_2)}{\Omega (E)}=\dfrac{\Omega_1(E_1)\Omega_2(E-E_1)}{\Omega(E)} =C\Omega_1(E_1) \Omega_2(E_2)\tag{1.1}
  $$
  여기서 $C^{-1}=\displaystyle \Omega(E)=\sum_{\epsilon} \Omega_1 (\epsilon) \Omega_2 (E-\epsilon)$ 이다. 

- 두 시스템이 themally contact 되어 있지만 $A$ 는 isolated 되어 있다면 총 에너지는 변하지 않는다. 이를 $E$ 라 하면 $E=E_{1}+E_{2}$ 이다. Themally contact 된 후 equillibrium이 되었을 때 $A_1$ 의 energy를 $\overline {E_1}$, $A_2$ 의 에너지를 $\overline{E_2}$ 라 하자.

- $A=A_1+A_2$ 의 에너지가 $E$ 와 $E+\delta E$ 사이에 있을 때의 총 microstates의 갯수를 $\Omega (E)$ 라 하자. 그렇다면,
  $$
  P(\overline{E_1})=C\Omega_1 (\overline{E_1})\Omega_2(\overline{E_2})=C\Omega_1(\overline{E_1})\Omega_2 (E-\overline{E_1}) \tag{1.2}
  $$
  이 된다. 

- 우리가 익히 알고 있듯이 $\Omega(E)$ 는 $E$ 에 대해 급속히 증가하는 함수이다. 시스템의 자유도를 $f$ 라 할 때 대략 $\Omega \propto e^f$ 이다. 따라서 $\Omega_f$ 는 어떤 $\overline{E_1}=\widetilde{E}_1$ 에서 최대값을 가진다. 이 $\widetilde{E}_1$ 은 $\dfrac{\partial \ln P(\overline{E_1})}{\partial \overline{E_1}} =\dfrac{1}{P} \dfrac{\partial P (\overline{E_1})}{\partial \overline{E_1}} =0$ 이 되도록 하는 값이다. 이 식을 (2) 에 적용하면,

$$
\dfrac{\partial \ln \Omega_1 (\overline{E_1})}{\partial \overline{E_1}}=\dfrac{\partial \ln \Omega_2 (\overline{E_2})}{\partial \overline{E_2}} \tag{1.3}
$$

이다. 

- 우리는 여기서 시스템의 parameter $\beta(E)$ 를 다음과 같이 정의한다.
  $$
  \beta (E)=\dfrac{\partial \ln \Omega (E)}{\partial E} \tag{1.4}
  $$
  
- 식 (1.3) 이 의미하는 것은 시스템 $A=A_1+A_2$ 는 $\beta_1 (\widetilde{E}_1) = \beta_2 (\widetilde{E}_2)$ 인 조건에서 가장 많은 microstates를 가진다. 

- 열역학적인 온도 $T$ 와 $\beta$ 는 $\beta = \dfrac{1}{k_B T}$ 의 관계가 있으며 이 때 $k_B$ 를 Boltzmann constant 라 한다. 

- **Entropy** $S$ 는 다음과 같이 정의된다.
  $$
  S \equiv k_B \ln \Omega \tag{1.5}
  $$



#### Some Properties of Absolute Temperature

- 식 (4) 를 보자. Degree of freedom이 $f$ 인 system은 보통 $\Omega (E) \propto E^f$ 이므로 $\beta > 0$ 이다. 그러나 $\Omega (E)$ 가 어떤 영역에서 $E$ 에 대해 감소하는 영역이 존재한다면 이 영역에서 $\beta<0 \implies T<0$ 이 된다. 

- $\Omega (E) \propto e^f$ 일 경우 $\beta \approx \dfrac{f}{\overline{E}}$ , $\dfrac{1}{\beta}=k_B T \approx \dfrac{\overline{E}}{f}$ 가 된다. 즉 Temperature 는 자유도 당 에너지의 한 척도이다. 

- 따라서, thermal equillibrium 인 두 시스템은 자유도당 평균 에너지가 서로 같아진다. 

- $\Omega_f(E) \ge \Omega_i (E)$ 이므로 $\Delta S = S_f-S_i = S_1(\overline{E_1})+S_2(\overline{E_2})- S_1(E_1) - S_2(E_2)\ge 0$ 이다. 따라서,
  $$
  0 \le \dfrac{\partial S_1}{\partial E_1}(\overline{E_1}-E_1)+\dfrac{\partial S_2}{\partial E_2}(\overline{E_2}-E_2)=\beta_1 Q_1+\beta_2 Q_2
  $$
   Where $Q_1 = \overline{E_1}-E_1,\, Q_2=\overline{E_2}-E_2$ 이다. $Q_1-Q_2=0$ 이므로 $(\beta_1-\beta_2)Q\ge 0$ 이다. 여기서 $\beta_1,\,\beta_2$ 는 thermal contact 이전의 system $A_1,\,A_2$ 의 온도이다. 

  $\beta_1>0,\, \beta_2>0$ 인 경우만을 생각한다. $Q>0$ 이면 $\beta_1 > \beta_2$ 이므로 $T_1<T_2$ 이다. 즉 온도가 낮은 쪽에서 열을 흡수한다. 



## 2. Heat Reservior

Thermally contacted 된 시스템 $A,\,A'$ 을 생각한다. 여기서 $A'$ 이 $A$ 에 비해 매우 클 때, $A'$ 을 $A$ 에 대한 **heat reservoir** 혹은 **heat bath** 라 한다. 수학적으로, 
$$
\left|\dfrac{\partial \beta'}{\partial E'}Q\right| \ll \beta' \tag{2.1}
$$
을 만족하는 시스템을 말한다. 

$A'$ 의 macroscopic system의 number of accessible states 를 $\Omega'(E')$ 이라 하면,
$$
\begin{aligned}
\ln \Omega'(E'+Q')-\ln \Omega' (E') & =\left(\dfrac{\partial \ln \Omega'}{\partial E'}\right)Q'+\dfrac{1}{2} \left(\dfrac{\partial^2\ln \Omega'}{\partial E'^2}\right)Q'^2 + \cdots \\
&=\beta'Q' + \dfrac{1}{2}\dfrac{\partial \beta'}{\partial E'} Q'^2 + \cdots  \\
&\approx \beta'Q' \\

\end{aligned}
$$
이므로 $\Delta S = k_B\ln \Omega'(E'+Q') - k_B\ln \Omega'(E')$ 을 생각하면,
$$
\Delta S =\dfrac{Q'}{T'} \tag{2.2}
$$
이다. 



## 3. Sharpness of the Probability Distribution

역시 Thermally contacted 된 시스템 $A_1,\,A_2$ 을 생각하자. 

시스템 $A_1$ 의 probability distribution $P_1(E_1)$ 가 어떤 값 $\widetilde{E}_1$ 에서 maximum을 갖는다고 하자. $\eta = E_1-\widetilde{E}_1$ 로 놓고 $\widetilde{E}_1$ 주위에서 Taylor 전개를 하면,
$$
\begin{align}
\ln \Omega_1 (E_1) & =\ln \Omega_1 (\widetilde{E}_1)+ \left(\dfrac{d \ln \Omega_1 (E_1)}{dE_1}\right)_{\widetilde{E}_1} \eta + \dfrac{1}{2} \left(\dfrac{d^2 \ln \Omega_1 (E_1)}{dE_1^2}\right)_{\widetilde{E}_1}\eta^2+\cdots \\
& = \ln \Omega_1 (\widetilde{E}_1) + \beta_1\eta  - \dfrac{1}{2}{\lambda_1} \eta^2 +\cdots
 
\end{align} \tag {3.1}
$$
Where $\beta_1 = \left(\dfrac{d \ln \Omega_1 (E_1)}{dE_1}\right)_{\widetilde{E}_1}$ and $\lambda = -\left(\dfrac{d^2 \ln \Omega_1 (E_1)}{dE_1^2}\right)_{\widetilde{E}_1}$ . 

이제 system $A_2$ 을 생각하자.  $E_1+E_2 = \widetilde{E}_1+\widetilde{E}_2$ 이므로 $E_2-\widetilde{E}_2 = -(E_1-\widetilde{E}_1)=-\eta$ 이다. 식 (3.1) 로 부터, 
$$
\ln \Omega_2(E_2)= \ln \Omega_2 (\widetilde{E}_2) - \beta_2 \eta - \dfrac{1}{2}{\lambda_2} \eta^2+ \cdots \tag{3.2}
$$
식 (3.1), (3.2) 로 부터,
$$
\ln \left[\Omega_1(E_1) \Omega_2 (E_2)\right] = \ln \left[ \Omega_1 (\widetilde{E}_1) \Omega_2 (\widetilde{E}_2)\right] + (\beta_1-\beta_2)\eta - \dfrac{1}{2} ({\lambda_1}+{\lambda_2})\eta^2 + \cdots
$$
이다. 위 식이 maximum을 가지면 $\beta_1=\beta_2$ 이며, $\lambda = \lambda_1+\lambda_2$ 로 놓자. 
$$
\ln  P_1(E_1)=\ln P_1(\widetilde{E}) - \dfrac{1}{2}\lambda\eta^2 \implies P_1(E)=P_1(\widetilde{E}_1)\exp\left(-\dfrac{1}{2}\lambda(E-\widetilde{E})^2\right)\tag{3.3}
$$

$P_1(E_1)$ 이 maximum 을 갖기 위해서는 $\lambda\ge 0$ 이어야 한다. ($\lambda =0$, 즉 $\dfrac{\partial \beta}{\partial E}=0$ 인 경우는 예를 들어 상전환 인 경우에 발생 할 수 있다. See Reif p.109) 

- 우리가 많이 썼던 approx, $\Omega \propto E^f$ 를 가정하면, $\lambda = \dfrac{f}{\widetilde{E}^2}>0$ where $f$ is a degree of freedom of the system.
- 식 (3.3)을 보면 $P_1(E_1)$ 은 $\widetilde{E}_1$ 을 중심으로 하는 가우스분포를 가진다.  $\lambda \approx f/\widetilde{E}^2$ 와 $f \approx 10^{24}$ 를 생각하면 매우 sharp 한 가우스 분포임을 유추 할 수 있다.
- $\lambda >0 \implies \dfrac{\partial \beta}{\partial E} < 0 \implies \dfrac{\partial T}{\partial E}>0$ . 따라서 시스템의 에너지가 증가하면 온도가 증가한다. (우리는 themal contact 만 존재하는 시스템을 고려한다.)



## 4. Dependence of the Density of States on The External Parameters



External parameter $x$ 를 생각하자. $x$ 가 $dx$ 만큼 변하면 (다른 external parameters 가 일정하다는 조건에서) microstate $r$ 의 에너지 $E_r$ 은 $\dfrac{\partial E_r}{\partial x}dx$ 만큼 변할 것이다. 이제 에너지가 $E$ 와 $E+\delta E$, 그리고 $\dfrac{\partial E_r}{\partial x}$ 가 $Y$ 와 $Y + \delta Y$ 사이에 존재할 경우의 수를 $\Omega_Y (E,\,x)$ 라 하고, 에너지와 external parameter $x$ 에 의해 정해지는 microstates 의 갯수를 $\Omega(E,\,x)$ 라 하면,
$$
\Omega (E,\, x)= \sum_Y \Omega _Y (E,\,x) \tag{4.1}
$$
이다. 

External parameter $x$ 가 $x+dx$ 로 변할 때 에너지가 $E$ 보다 작은 에너지에서 $E$ 보다 큰 에너지로 변하는 states의 총 갯수를 $\sigma(E)$ 라 하자. 이러한 states 에서의 총 에너지 변화는 $Ydx$ 이므로 microstates의 에너지가 $E-Ydx \le E_r \le E$ 사이에 있는 microstates의 갯수가 $\sigma (E)$ 일 것이다. 특정 에너지 range $Ydx$ 값을 갖는 microstates의 갯수 $\sigma_Y (E)$ 는 다음과 같다.
$$
\sigma_Y (E)=\dfrac{\Omega_Y(E,\,x)}{\delta E} Ydx \tag{4.2}
$$
따라서, 
$$
\sigma(E)=\sum_Y \sigma_Y(E)=\sum_Y \dfrac{\Omega_Y (E,\,x)}{\delta E}Ydx = \dfrac{\Omega(E,\,x)}{\delta E} \bar{Y}dx  \,,\\
\text{if we define }\bar{Y}=\dfrac{1}{\Omega(E,\,x)} \sum_Y \Omega_Y(E,\,x)Y \,. \tag{4.3}
$$
이다. $Y=\partial E_r/\partial x$ 이므로,
$$
\bar{Y}=\overline{\dfrac{\partial E_r}{\partial x}}=-\bar{X} \tag{4.4}
$$
이다. 

External perameter $x$ 가 $x+dx$ 로 변하며 이에 따라 microstates 의 에너지가 $Y dx$ 만큼 변할 때 , 에너지 영역이 $(E,\, E+\delta E)$ 안에 포함되는 microstates 의 총 변화량은 $\dfrac{\partial \Omega (E,\,x)}{\partial x}dx$ 이다.  $\omega (E)$ 를 density of states with energy $E$ 라 하면 
$$
\begin{align}
\dfrac{\partial \Omega (E,\,x)}{\partial x}dx  &= \left[\int_{E-Ydx}^E \omega (E)\,dE'-\int_{E +\delta E -Ydx}^{E+\delta E} \omega(E)\,dE'\right]dx \\
&=\sigma(E) -\sigma(E+\delta E)=-\dfrac{\partial \sigma}{\partial E}\delta E
\end{align}
$$
식 (4.3) 을 이용하면,
$$
\dfrac{\partial \Omega}{\partial x}=-\dfrac{\partial}{\partial E} (\Omega \bar{Y}) = -\dfrac{\partial \Omega}{\partial E}\bar{Y}-\Omega \dfrac{\partial \bar{Y}}{\partial E}\;. \tag{4.5}
$$
이며,
$$
\dfrac{\partial \ln \Omega}{dx}=\dfrac{1}{\Omega}\dfrac{\partial \Omega}{dx}=-\bar{Y}\left(\dfrac{1}{\Omega}\dfrac{\partial \Omega}{\partial E}\right)-\dfrac{\partial \bar{Y}}{\partial E}=-\bar{Y}\dfrac{\partial \ln \Omega}{\partial E}-\dfrac{\partial \bar{Y}}{\partial E} \tag{4.6}
$$
Macroscopic system 에서 $\Omega \propto E^f$ where $f$ is the degree of freedom of system 이므로 $f \sim 10^{24}$ 이다. 따라서
$$
\begin{align}
O\left(\bar{Y} \dfrac{\partial \ln \Omega}{\partial E}\right) &\sim f \cdot O\left(\dfrac{\bar{Y}}{E}\right) \,,\\
O\left(\dfrac{\partial {\bar{Y}}}{\partial E} \right) &\sim O\left(\dfrac{\bar{Y}}{E}\right) 

\end{align}
$$
이므로 식 (4.6) 에서 첫번째 term이 두번째보다 훨씬 크다. 따라서, $\dfrac{\partial \ln \Omega}{\partial x}=-\beta \bar{Y} = \beta \bar {X}$ 이다. 만약 다수의 external parameters $x_1,\ldots,\,x_n$ 를 고려한다면 다음 식이 성립한다.
$$
\dfrac{\partial \ln \Omega}{\partial x_\alpha}=-\beta \bar{Y}_\alpha = \beta \bar {X}_\alpha \tag{4.7}
$$


## 5. Equillibrium between Interacting Systems

- 이제 System $A_1,\,A_2$ 가 열 뿐만 아니라 일(work) 도 교환한다고 하자. 전체 시스템 $A=A_1+A_2$ 는 isolated 되었다. System $A_1$ 는 에너지 $E_1$ 과 external parameters $x_1,\ldots,\, x_n$ 으로 기술 할 수 있으며 system $A_2$ 는 에너지 $E_2$ 와 external parameters $y_1,\ldots,\,y_n$ 으로 기술 할 수 있다고 하자. 그렇다면  $A$ 의 에너지 $E$ 는 $E=E_1+E_2 = \text{const}$ 이다. $E_1$ 을 알고 있다면 $E_2=E-E_1$ 으로 결정되며 $y_i = y_i (x_1,\ldots,\,x_n)$ 임은 쉽게 알 수 있다. 따라서 $A$ 의 total number of accessible states $\Omega$ 는 $E_1$ 과 $x_1,\ldots,\,x_n$ 의 함수이며 어떤 $E_1=\widetilde{E}_1$ 과 $x_i =\widetilde{x}_i$ 에서 sharp maximum 을 갖는다. 따라서 $E_1$ 의 평균값 $\bar{E}_1$ 과 $x_i$ 의 평균값 $\bar{x}_i$ 는 각각 $\widetilde{E}_1$ 과 $\widetilde{x}_i$ 와 매우 가까운 값 일 것이다.



#### 5.1 Infinitesimal quasi-static process

$A_1$ 이 $A_2$ 와의 interaction을 통해 equilibrium states $(\bar{E}_1, \{\bar{x}_\alpha\})$ 로부터 equillibrium states $(\bar{E}_1+\delta \bar{E}_1,\, \{\bar{x}_\alpha+d\bar{x}\})$ 로 infinitesimaly 변했다고 가정하자. 그렇다면,
$$
d\ln \Omega_1 = \dfrac{\partial \Omega_1}{\partial E_1}d\bar{E}_1+ \sum_{\alpha=1}^n \dfrac{\partial \Omega_1}{\partial x_\alpha}\,d\bar{x}_\alpha = \beta \left(d\bar{E}_1+\sum_{\alpha} \bar{X}_\alpha d\bar{x}_\alpha\right) = \beta (d\bar{E}_1+dW_1)=\beta \,dQ_1
$$
이다. 이로부터 $d\ln \Omega = \beta \,dQ$ 를 얻었는데 이는 어떠한 quasi-static infinitesimal process 에서도 성립한다.  또한 이로부터,  $dS=\dfrac{dQ}{T}$ 를 얻을 수 있다. 이를 정리하면 다음과 같다.

<b> Fundamental relations for infinitesimal quasi-static process</b>
$$
\begin{align}
d\ln \Omega_1 &= \beta \, dQ_1\,,\\
dS_1&=\dfrac{dQ_1}{T}\;. 
\end{align} \tag{5.1}
$$


- $A_1,\,A_2$ 가 thermally insulated 되었다면 $dS_1=0$. 즉 $d\Omega_1 =0$  
- 당연히 non quasi-static process 에서는 thermally instulated 되어 있다고 해도 $dS\ne 0$ 일 수 있지.



#### 5.2 Equillibrium conditions

- External parameter가  systeam $A_1$ 의 부피  $V_1$ 와  $A_2$ 의 부피 $ V_2$ 뿐이라고 하자. 전체 시스템 $A$ 의 number of accessible states $\Omega$ 는 다음과 같다.

$$
\Omega(E,\,V) = \Omega_1(E_1,\, V_1) \,\Omega_2 (E_2,\,V_2)
$$

- 따라서,

$$
\begin{align}
\ln \Omega &= \ln \Omega_1 + \ln \Omega_2 \,,\\
S&=S_1+S_2 \;.
\end{align}
$$

- $\Omega$ 가 maximum 값을 가지면  $d\Omega =0$ 이므로,
  $$
  d\ln \Omega = d(\ln \Omega_1 + \ln \Omega_2)=0
  $$
  이며,
  $$
  d\ln \Omega_1 = \dfrac{\partial \ln \Omega_1}{\partial E_1}dE_1 + \dfrac{\partial \Omega_1}{\partial V_1}dV_1=\beta_1 \, dE_1 +\beta_1 \bar{p}_1\, dV_1 \quad \text{where } \bar{p}_1=- \overline{\dfrac{\partial E_1}{\partial V_1}}
  $$
  이다. 이 식을 system $A_2$ 에도 적용하면,
  $$
  (\beta_1-\beta_2)\,dE_1+ (\beta_1\bar{p}_1-\beta_2 \bar{p}_2) \, dV_1 =0 
  $$
  이다. 이 식은 임의의 $ dE_1,\, dV_1$ 에 대해 성립해야 하므로 
  $$
  \begin{align}
  \beta_1&=\beta_2\,,\\
  \bar{p}_1 &=\bar{p}_2\,.
  \end{align} \tag{5.2}
  $$
  



## 6. Properties of the Entropy



- $dQ$ 는  exact differential 이 아니지만 $dQ/T=dS$ 는  exact differential 이다. 따라서,
  $$
  \Delta S = S_f - S_i = \int_i^f dS = {\int_i ^f} \dfrac{dQ}{T}\quad\text{for quasi-statistical process}. \tag{6.1}
  $$
  는 <b>process independent</b> 하다.



#### 6.1 Implications of the statistical definition of entropy

$$
S\equiv k_B \ln \Omega
$$



## Probblems



<b>3.1 </b> Box가 파티션에 의해 그 부피비가 3:1 이 되도록 나누어져 있다. 큰 부분에는 1000개 의 Ne 분자가, 작은 부분에는 100개의 He 분자가 있다. 이 때 파티션에 작은 구명이 뚫렸고 평행상태에 도달했다.

(a) 각각의 부분에 있는 각각 분자의 평균 분자수를 구하여라.

(b) 1000 개의  Ne 분자를 큰  partition에서, 100 개의  He 분자를 작은 partition에서 발견할 확률을 구하여라.

---

(a) 큰 파티션을 1, 작은 파티션을 2라 하자. 각각의 분자가 큰 partition에 있을 확률이 $3/4$, 작은 부분에 있을 확률이 $ 1/4$ 이다. Ne 분자가 큰 파티션에 $n$ 개 존재할 확률은 다음과 같다.
$$
P_{Ne, 1}(n)=\dfrac{3000 !}{n!(1000-n)!}\left(\dfrac{3}{4} \right)^n \left(\dfrac{1}{4}\right)^{1000-n}
$$
이로부터,
$$
\overline{n}_{Ne,\,1}= \sum_{n=0}^{1000} n P_{Ne,\,1}(n) = 1000 \times \dfrac{3}{4}=750.
$$
같은 방법으로 $\overline{n}_{Ne,\,2}=250\, \overline{n}_{He,\,1}=75,\, \overline{n}_{He,\,2}=25$.

(b)
$$
P=\left(\dfrac{3}{4} \right)^{1000} \left(\dfrac{1}{4}\right)^{100} \sim 7.17\times10^{-186}\;.
$$


<b>3.2 </b> $N$ 개의 localized weakly interacting particles 로 이루어져 있으며 각각의 입자는 스핀 $1/2$ , 자기모멘트 $\mu$ 를 갖는 시스템을 생각하자. 이 스스템에 외부자기장 $H$  가 걸려있다. 이 시스템은  Problem 2.4 에서 다루었다.

(a) problem 2.4 (b) 에서 계산하였던 $\ln \Omega (E)$ 와 정의 $\beta = \partial \ln \Omega / \partial E$ 를 사용하여 시스템의 온도 $ T$ 와 총 에너지 $E$ 의 관계를 구하시오.

(b) 어떤 조건에서  $T$ 가  negative 인가?

(c) 시스템의 total magnetic moment $M$ 은 에너지와 관계가 있다. (a) 의 결과를 이용하여 $M$ 을 $H$ 와 $T$ 의 함수로 구하시오.

---

(a) From problem 2.4(b), 
$$
\begin{aligned}
\ln \Omega(E) &= N\ln N + \ln \left(\dfrac{\delta E}{2\mu H}\right)-\left(\dfrac{N}{2}-\dfrac{E}{2\mu H}\right)\ln \left(\dfrac{N}{2}-\dfrac{E}{2\mu H}\right)-\left(\dfrac{N}{2}+\dfrac{E}{2\mu H}\right)\ln \left(\dfrac{N}{2}+\dfrac{E}{2\mu H}\right)\;,\\
\beta&=\dfrac{\partial \ln \Omega(E)}{\partial E}=\dfrac{1}{2\mu H} \ln \left(\dfrac{N}{2}-\dfrac{E}{2\mu H}\right)+\dfrac{1}{2\mu H}-\dfrac{1}{2\mu H}\ln \left(\dfrac{N}{2}+\dfrac{E}{2\mu H}\right) - \dfrac{1}{2\mu H} \\
&=\dfrac{1}{2\mu H} \ln \left(\dfrac{N}{2}-\dfrac{E}{2\mu H}\right)-\dfrac{1}{2\mu H}\ln \left(\dfrac{N}{2}+\dfrac{E}{2\mu H}\right)  \\
&= \dfrac{1}{2\mu H} \ln \left(\dfrac{ \mu H N -E}{ \mu H N+E}\right)
\end{aligned}
$$
$\beta = 1/k_B T$ 를 이용하면,
$$
E=-\mu N H \tanh\left(\dfrac{ \mu H}{k_B T}\right)
$$
(b) $E>0 \implies T<0$ 

(c) $E=-(n_1-n_2)\mu H$, $M=(n_1-n_2)\mu$ 이므로 
$$
M=-\dfrac{E}{H}=\mu H \tanh\left(\dfrac{ \mu H}{k_B T}\right)\;.
$$


<b>3.3 </b> External field $H$ 가 가해진 두 spin systems $A,\,A'$ 을 생각한다. $A$ 는  $N$ 개의 weakly interacting localized particles of spin $1/2$ and magnetic moment $\mu$ 로 이루어졌고 $A'$ 은  $N'$ 개의 weakly interacting localized particles of spin $1/2$ and magnetic moment $\mu'$ 으로 이루어졌다. 두 시스템은 처음에는 각각 총 에너지 $bN\mu H$ 와 $b'N'\mu' H$ 를 갖고 isolated 되어 있다가 thermal contact 되었다. $|b|\ll 1$ and $|b'|\ll 1$ 을 가정하여 problem 2.4 (c) 의 densities of states 를 사용하도록 하자.

(a) 최종적인  thermal situation 에 따른 most probabile situation 에서 system $A$ 의 에너지 $\widetilde{E}$  와  system $A'$ 의 에너지 $\widetilde{E}'$ 의 관계는?

(b) $\widetilde{E}$ 는 얼마인가?

(c) System $A$ 가 $A'$ 과  thermal contact 된 후 평형상태에 도달했을 때 system $A$ 가 흡수한 열 $Q$  는?

(d) $A$ 의 최종 에너지가 $E$ 와 $E+d E$ 사이에 존재할 확률  $P(E)$ 는 ?

(e) 최종 평형 상태에서 시스템 $ A$ 의 에너지 dispersion $(\Delta^\ast E)^2 \equiv \overline{(E-\bar{E})^2}$ 는?

(f) $N' \gg N$ 일 때 relative energy spread $|\Delta^\ast E/\widetilde{E}|$ 는?

---

According to problem 2.4(c), 
$$
\Omega (E)=\sqrt{\dfrac{2}{\pi N}}2^N \exp\left(- \dfrac{E^2}{2 N \mu^2 H^2}\right)\dfrac{\delta E}{2 \mu H}\;.
$$
Then,
$$
\ln \Omega (E) = -\dfrac{E^2}{2N\mu^2H^2}+N\ln 2 - \dfrac{1}{2}\ln \left(\dfrac{\pi N}{2}\right)+\ln \left(\dfrac{\delta E}{2\mu H}\right) \tag{1}
$$
이다. 

(a) Equillibrium 에 $\beta = \left(\dfrac{\partial \ln \Omega(E)}{\partial E}\right)_{\widetilde{E}}= \left(\dfrac{\partial \ln \Omega'(E')}{\partial E'}\right)_{\widetilde{E}'}$ 이므로, $\dfrac{\widetilde{E}}{N\mu^2}=\dfrac{\widetilde{E}'}{N'\mu'^2}$ 

(b) 에너지 보존에 따라, $\widetilde{E}+\widetilde{E}'=bN\mu H+b'N'\mu'H$ 이므로,
$$
\widetilde{E} = N\mu^2 \dfrac{(bN\mu + b'N'\mu')H}{N\mu^2+N'\mu'^2}
$$
(c) $Q=\widetilde{E}-bN\mu H$ 이므로,
$$
Q= \dfrac{NN'\mu\mu'(b'\mu-b\mu')H}{N\mu^2+N'\mu'^2}
$$
(d) 식 (1) 에서 마지막  term 은 무시 할 수 있으며, $P(E)=C \Omega(E) \Omega(E_0-E)$ where $E_0 = (bN\mu+b'N'\mu')H$ 이며 $C$ 는 normalizatin constat 이다. 
$$
\begin{align}
P(E)&= C \exp\left( - \dfrac{E^2}{2N\mu^2H^2}\right) \exp \left(-\dfrac{(E_0-E)^2}{2N'\mu'^2H^2}\right)\\
&= C\exp (-aE^2) \exp (-b(E_0-E)^2) \qquad \qquad \text{where }a=\dfrac{1}{2N\mu^2H^2} \text{ and }b=\dfrac{1}{2N'\mu'^2H^2} \\
&=C \exp (-(a+b)E^2 + 2bE_0 E -bE_0^2) \\
&=C \exp \left[ - (a+b)\left( E^2- \dfrac{2bE_0}{a+b}E \right) -bE_0^2 \right] \\
&=C' \exp \left[-(a+b) \left( E-\dfrac{b}{a+b}E_0 \right)^2\right] \\
&=C_0 \exp \left[-\dfrac{(E-\alpha E_0)^2}{2\sigma^2}\right] \qquad\qquad\text{where } \alpha = \dfrac{b}{a+b}\,, \sigma^2=\dfrac{1}{2(a+b)}\text{ and } C_0 = \dfrac{1}{\sqrt{2\pi \sigma^2}}


\end{align}
$$
 (e) From (d) and propertios of Gaussian distribution,
$$
\begin{align}
(\Delta^\ast E)^2 &= \sigma^2 =  \dfrac{1}{2(a+b)}=\dfrac{1}{2 \left(\dfrac{1}{2N\mu^2H^2}+ \dfrac{1}{2N'\mu'H^2}\right)}\\
&=\dfrac{NN'\mu^2\mu'^2H^2}{N\mu^2+N'\mu'^2}

\end{align}
$$
(f) From (d), $N' \gg N$ implies $\widetilde{E} =N\mu^2\dfrac{(b\mu(N/N')+b'\mu')H}{\mu^2(N/N')+\mu'^2} \approx Nb'\mu'H$ and $(\Delta^\ast E)^2 =\dfrac{N\mu^2\mu'^2H^2}{\mu^2(N/N')+\mu'^2} \approx N\mu^2H^2$ . 따라서,
$$
\left|\dfrac{\Delta^\ast E}{\widetilde{E}}\right| \approx \dfrac{\sqrt{N}\mu H}{Nb'\mu'H}=\dfrac{1}{\sqrt{N}} \dfrac{\mu}{b'\mu'}
$$


<b>3.4 </b> System $A$ 가  heat reservior $A'$ 과 thermal contact 하고 있으며 $A'$ 의 온도는 $ T'$ 이고 $A$ 는 $ Q$ 만큼의 열을 흡수했다. 이  process 에서 $A$ 의 entropy 증가  $\Delta S$ 는  $\Delta S \ge Q/T'$ 을 만족하며, 등호는 $ A'$ 의 온도 $T'$ 과 infinitesimally different 할 때에만 성립함을 보여라. 

---

Quasi-static process 임을 가정하면  $\Delta S= \displaystyle \int_i^f \dfrac{dQ}{T}$ 이며 이 프로세스에서의 온도 $T$ 는  $T_i \le T\le T_f \approx T'$ 이므로  
$$
\Delta S =\int_i^f \dfrac{dQ}{T}\ge \int_{i}^f \dfrac{dQ}{T'}=\dfrac{1}{T'}\int_i^f dQ=\dfrac{Q}{T'}
$$
 등호에 관해서는 자명하다.



<b>3.5 </b> 부피 $V$ 의 box 에 $N_1$ 개의  type 1 분자와 $N_2$ 개의 type 2 분자가 있는 system을 생각한다. 이 분자들은 very weakly interacting particles 이어서 ideal gas mixture를 이룬다고 가정하자. 

(a) 에너지 영역이 $E$ 와 $E+\delta E$ 사이에 있는 total number of states $\Omega (E)$ 의 부피에의 의존성을 설명하라. 이 문제를 고전적으로 간주 할 수 있다.

(b) 이 결과를 이용하여 이 시스템의 상태방적식을 구하고 평균 압력 $\bar{p}$ 를 $V$ 와 $T$ 의 함수로 구하시오.

---

