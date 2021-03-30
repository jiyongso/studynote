I. Intruduction to statistical mechanics
===





 ## 1. Binomial distrubition for large $N$



#### Biomial probability distribution

$$
W(n_1)=\begin{pmatrix} N \\ n_1\end{pmatrix} p^{n_1}q^{N-n_1}
$$



$N\ge n_1 \gg1 $ 이며 $n_1$ 이 $W$ 의 maximum 근처에 있을 때 
$$
\left|W(n_1+1)-W(n_1) \right| \ll W(n_1)
$$
임을 보이자. 다른 말로 하면,
$$
\left|\dfrac{W(n_1+1)-W(n_1)}{W(n_1)} \right| \ll 1
$$
임을 보이면 된다. $n_1 \approx Np$ 이므로,
$$
\begin{aligned}
\left|\dfrac{W(n_1+1)-W(n_1)}{W(n_1)} \right| &= \left|\dfrac{n_1!(N-n_1)!}{(n_1+1)!(N-n_1-1)!} \dfrac{p}{q}-1\right| \\
&= \left| \dfrac{N-n_1}{n_1} \dfrac{p}{1-p}-1 \right| \\
&\approx \left|\dfrac{N-Np}{Np} \dfrac{p}{1-p}-1\right | =0\;.



\end{aligned}
$$





## Problems



<b>1.1 </b> 3개의 주사위를 던졌을 때 6점 이하의 점수를 얻을 확률은?

---

총 경우의 수는 $6^3=216$ 이며 6점 이하를 얻을 경우의 수는 (1,1,1), (1,1,2) (1,1,3), (1,1,4), (1,2,1), (1,2,2), (1,2,3), (1,3,1), (1,3,2), (1,4,1), (2,1,1), (2,1,2), (2,1,3), (2,2,1), (2,2,2), (2,3,1), (3,1,1), (3,1,2), (3,2,1), (4,1,1) 의 20가지 이므로 확률은 $20/216=5/54\approx 0.926$. 



<b>1.4</b> 취객이 거리의 가운데에 위치한 한 가로등에서 왼쪽 혹은 오른쪽으로 움직이는데 각각의 한 스텝의 길이와 확률이 같다고 하자. $N$ step을 걸었을 때 취객이 다시 원래의 가로등으로 돌아올 확률을 $N$ 이 짝수일 때와 홀수 일 때로 나누어서 구하시오.

---

가로등에서 왼쪽으로 움직인 횟수와 오른쪽으로 움직인 횟수를 각각 $n_1,\,n_2$, 한 스텝의 길이를 $l$ 이라 하자. $N=n_1+n_2$ 이며 총 움직인 거리 $L$ 은
$$
L=(n_1-n_2)l = (2n_1-N)l
$$
이다. 따라서 $N$ 이 홀수이면 $L\ne 0$ 이므로 짝수인 경우만 생각해 주면 된다. $n_1=n_2=N/2$ 이다.
$$
P(L=0)=\begin{pmatrix}N \\n_1\end{pmatrix}\dfrac{1}{2^{N}}=\dfrac{(2n_1)!}{n_1! n_1!}\dfrac{1}{2^{2n_1}}\;.
$$


<b>1.5</b> 러시안 룰렛 게임에서 총의 드럼에 하나의 카트리지만 채웟고 나머지 다섯개는 비어있었다. 이제 참석자는 드럼을 회전시킨후 자기 머리에 겨누고 방아쇠를 당긴다.

(a) $N$ 번의 게임을 하고도 살아 있을 확률은?

(b) $N-1$ 번째에서 살아 있고 $N$ 번째에서 발사될 확률은?

(c) 이 게임에서 방아쇠를 당기는 평균 횟수는?

---

(a) $\left(\dfrac{5}{6}\right)^N$.  

(b) $\left( \dfrac{5}{6}\right)^{N-1} \dfrac{1}{6}$. 

(c) $\displaystyle \overline{N}=\sum_{N=1}^\infty N \left(\dfrac{5}{6}\right)^{N-1} \dfrac{1}{6}=6$.



<b>1.6</b> $p=q$, $m=n_1-n_2$ 의 random work problem을 생각한다.  총 $N$ 스텝 후에 $\overline{m},\, \overline{m^2},\, \overline{m^3},\, \overline{m^4}$ 를 구하여라.

---

미리 계산.
$$
\begin{aligned}
\overline{n_1}&=pN=N/2\,,\\
\overline{n_1^2} &=\overline{n_1}^2+Npq = N^2/4+N/4\,,\\
\end{aligned}
$$

$$
\begin{aligned}
\overline{n_1^3} &= \sum_{n_1=0}^N (n_1)^3 \dfrac{N!}{n_1!(N-n_1)!}p^{n_1}q^{N-n_1} = \left(p\dfrac{\partial}{\partial p}\right)^3 \sum_{n_1=0}^N \dfrac{N!}{n_1!(N-n_1)!}p^{n_1}q^{N-n_1} \\
&=\left(p\dfrac{\partial}{\partial p}\right)^3 (p+q)^N =\left(p\dfrac{\partial }{\partial p} \right)\left[ pN(p+q)^{N-1} +p^2N(N-1)(p+q)^{N-2} \right] \\
&=p \left[ N(p+q)^{N-1}+pN(N-1)(p+q)^{N-2} +2pN(N-1)(p+q)^{N-2}+p^2N(N-1)(N-2)(p+q)^{N-3} \right]\\
&=pN(p+q)^{N-1}+p^2N(N-1)(p+q)^{N-2}+2p^2N(N-1)(p+q)^{N-2}+p^3N(N-1)(N-2)(p+q)^{N-3} \\
&=N/2+N(N-1)/4+N(N-1)/2+N(N-1)(N-2)\\
&=\dfrac{N^3+3N^2}{8}\,,\\
\overline{n_1}^4 &=\left(p\dfrac{\partial}{\partial p}\right)^4 (p+q)^N \\
&=p \dfrac{\partial}{\partial p}\left[pN(p+q)^{N-1}+3p^2N(N-1)(p+q)^{N-2}+p^3N(N-1)(N-2)(p+q)^{N-3}  \right] \\
&=p\left[ N(p+q)^{N-1}+N(N-1)p (p+q)^{N-2} + 6pN(N-1)(p+q)^{N-2}+6p^2N(N-1)(N-2)(p+q)^{N-3} \right. \\
& \quad \left. +p^3N(N-1)(N-2)(N-3)(p+q)^{N-4} \right] \\
&= Np+7N(N-1)p^2+6N(N-1)(N-2)p^3+N(N-1)(N-2)(N-3)p^4  \\
&=\dfrac{N^4+6N^3-N^2+N}{16}
\end{aligned}
$$


$$
\begin{aligned}
\overline{m} &= Np-Nq=0\,,\\
\overline{m^2} &=\overline{(2n_1-N)^2}=4\overline{n_1^2}-4\overline{n_1}N+N^2=N^2+N-2N^2+N^2=N^2\,,\\
\overline{m^3} &=\overline{(2n_1-N)^3} = 8\overline{n_1^3}-12\overline{n_1^2}N+6\overline{n_1}N^2-N^3=0 \,,\\
\overline{m^4} &= \overline{(2n_1-N)^4} = 3N^2-2N\,.
\end{aligned}
$$




<b>1.7 </b> Binomial distribution을 다음과 같은 대수적인 방법 (조합론적인 해석이 포함되지 않은) 으로 유도해보자. $N$ 번의 독립적인 시도에서 $n$ 번 성공할 확률 $W(n)$ 을 구한다고 하자.  성공확률이 $w_1\equiv p$ 이며 실패확률은 $w_2=1-p=q$ 이다. 이 때 $W(n)$ 은 
$$
W(n)=\sum_{i=1}^2 \sum_{j=1}^2 \sum_{k=1}^2 \cdots \sum_{m=1}^2 w_i w_j w_k \cdots w_m \tag{1}
$$
이다. 여기서 각각의 term은 $N$ factors 를 포함하며 특정한 실패와 성공의 조합의 확률인다.  모든 조합에 대한 합은 $w_1$ 이 $n$ 개 포함되는 것에 대해서만 취해져야 한다. 즉 ${w_1}^n$ 에 관계된 term에 대해서만 취해져야 한다. 

$(1)$ 의 합을 재조합하여, show that the unrestricted sum can be written in the form
$$
W(n)=(w_1+w_2)^N
$$
이것을 binomial theorem으로 재조합하여 ${w_1}^n$ 과 관련된 term 을 더하면 우리가 원하는 확률 $W(n)$ 은 is then simply given by the one binomial expansion term which involves ${w_1}^n$.

---

Binomial expansion에 의해,
$$
(w_1+w_2)^N = \sum_{n=0}^N \dfrac{N!}{n! (N-n)!}{w_1}^n {w_2}^{N-n}
$$
이다.  따라서,
$$
W(n)=\dfrac{N!}{n!(N-n)!}\;.
$$


<b>1.8</b>  두 취객이 원점에서 $x$ 축 방면으로 오른쪽(+) 혹은 왼쪽(-)으로 같은 확률로 움직인다. 이 때 $N$ step 이후 같은 위치에 있을 확률을 구하시오. 이 둘은 항상 동시에 step을 취한다.

---

두 취객이 둘 다 오른쪽으로 움직일 확률은 $1/4$, 두 취객이 모두 왼쪽으로 움직일 확률도 $1/4$, 두 취객이 서로 반대방향으로 움직일 확률은 $1/2$ 이다. 두 취객의 step의 크기를 $l$ 이라 할 때 한 step에서 두 취객사이의 거리가 $0$ 만큼 변할 확률이 $1/2$, $+2l$ 만큼 변할 확률이 $1/4$, $-2l$ 만큼 변할 확률이 $1/4$ 이다.

$n_1$ 을 두 취객이 둘 다 오른쪽으로 움직이거나 왼쪽으로 움직인 횟수, $n_2$ 는 첫번째가 오른쪽, 두번째가 왼쪽으로 움직인 횟수, $n_3$ 는 첫번째가 왼쪽 두번째가 오른쪽으로 움직인 횟수라 하자. 둘 사이의 상대적인 거리를 $L$ 이라 하면,
$$
\begin{aligned}
N &=n_1+n_2+n_3\,,\\
L&=2l \times(n_2-n_3)\,.
\end{aligned}
$$
임을 안다. Binomial expantion 을 이용하면
$$
\begin{aligned}
(w_1+w_2+w_3)^N &= \sum_{k=0}^N \dfrac{N!}{k!(N-k)!}(w_1+w_2)^k {w_3}^{N-k} \\
&=\sum_{k=0}^N \dfrac{N!}{k!(N-k)!}\sum_{m=0}^k \dfrac{k!}{m!(k-m)!}{w_1}^m{w_2}^{k-m}{w_3}^{N-k}\\
&=\sum_{k=0}^N\sum_{m=0}^k\dfrac{N!}{m! (k-m)! (N-k)!} {w_1}^m w_2 ^{k-m}w_3 ^{N-k}
\end{aligned}
$$
이므로 
$$
P(n_1,\, n_2,\,n_3)=\sum_{n_1+n_2+n_3=N} \dfrac{N!}{n_1! n_2! n_3!}\left(\dfrac{1}{2}\right)^{n_1}\left(\dfrac{1}{4}\right)^{n_2}\left(\dfrac{1}{4}\right)^{n_3} 
$$
이다. 이제 $n_2=n_3$ 일 확률은
$$
P(n_1,\, n_2=n_3=n)=\sum_{n=0}^N \dfrac{N!}{(N-2n)!(n!)^2} \left(\dfrac{1}{2}\right)^{N-2n} \left(\dfrac{1}{16}\right)^n=\left(\dfrac{1}{2}\right)^N \sum_{n=0}^N \dfrac{N!}{(N-2n)!(n!)^2} \left(\dfrac{1}{2}\right)^{2n}
$$


<b>1.9</b> 발생 확률이 $p$ 인 event가 $N$ 번의 시행에서 $n$ 번 발생할 확률 $W(n)$ 은 binomial distribution에 의해 다음과 같다.
$$
W(n) = \dfrac{N!}{n! (N-n)!}p^n (1-p)^{N-n}\tag{1}
$$
$p$ 가 $1$ 보다 매우 작으며 $n \ll N$ 인 경우에만 관심있다고 하자. 이 경우 몇가지 approximation을 사용하여 간단한 형태로 바꿀 수 있다.

(a) $\ln (1-p) \approx -p$  를 이용하여 $(1-p)^{N-n}\approx e^{Np}$ 임을 보여라.

(b) $N!/(N-n)! \approx N^n$.

(c) 식 (1) 이 다음으로 근사됨을 보여라.
$$
W(n) = \dfrac{\lambda^n}{n!}e^{-\lambda} \qquad \text{where } \lambda = Np \tag{2}
$$
$(2)$ 의 분포를 **Poisson distribution** 이라 한다.

---

(a) 우선 $n \ll N$ 이므로 $N-n \approx N$ 이다. $\ln (1-p)\approx -p$ 이므로 $1-p = e^{\ln (1-p)}\approx e^{-p}$ 이다. 따라서,
$$
(1-p)^{N-n} \approx (1-p)^N \approx e^{-Np}\,.
$$
(b) 
$$
\dfrac{N!}{(N-n)!} = N(N-1)\cdots (N-n+1) \approx N^n
$$
(c) for $\lambda = Np$, 
$$
W(n) \approx \dfrac{N^n}{n!} p^n e^{-Np}=\dfrac{(Np)^n}{n!} e^{-Np}= \dfrac{\lambda^n}{n!}e^{-\lambda}\;.
$$
<b>1.10. </b> 앞 문제의 Poisson distribution을 생각하자.

(a) $\displaystyle \sum_{n=0}^N W(n)=1$ 임을 보여라. ($N\to \infty$ approximation 이 reasonable 하다.)

(b) Poisson distribution 에서 $\overline{n}$ 을 계산하라.

(c) Poisoon distribution 에서 $\overline{(\Delta n)^2}= \overline{(n-\overline{n})^2}$ 를 계산하라.

---

(a) $\displaystyle e^{\lambda}=\sum_{n=0}^\infty \dfrac{\lambda^n}{n!}$ 을 이용하면 쉽게 보일 수 있다.

(b)
$$
\begin{aligned}
\overline{n}=\sum_{n=0}^\infty n \cdot W(n)= \sum_{n=1}^{\infty} \dfrac{\lambda^n}{(n-1)!}e^{-\lambda}=\lambda e^{-\lambda} \sum_{n=1}^{\infty}\dfrac{\lambda^{n-1}}{(n-1)!}=\lambda e^{-\lambda}e^\lambda =\lambda.

\end{aligned}
$$
(c)
$$
\begin{aligned}
\overline{(\Delta n)^2} &= \overline{(n-\overline{n})^2}=\overline{n^2-2n\overline{n}+\overline{n}^2}=\overline{n^2}-{\overline{n}}^2 \\
&=\sum_{n=0}^\infty n^2 \dfrac{\lambda^n}{n!}e^{-\lambda} - \lambda^2 = \sum_{n=1}^\infty \dfrac{n\lambda^n} {(n-1)!}e^{-\lambda} -\lambda^2 \\
&= e^{-\lambda} \left[ \sum_{n=1}^\infty \dfrac{(n-1)\lambda^n}{(n-1)!}+\sum_{n=1}^\infty\dfrac{\lambda^n}{(n-1)!} \right] -\lambda^2 \\
&=e^{-\lambda }\left[ \lambda^2e^\lambda +\lambda e^\lambda\right]-\lambda^2 = \lambda

\end{aligned}
$$


<b>1.11</b> typesetter 가 random 하게 식자 오류를 낸다고 가정하자. 600 페이지에서 그러한 오류가 600개가 발생하였다고 하자. Poisson distribution을 이용하여 다음 확률을 계산하라.

(a) 한 페이지에 오류가 하나도 없을 경우.

(b) 한 페이지에 최소한 3개의 오류가 있을 경우.

---

(a) $\lambda=1$ 이다. 따라서 $W(0)=e^{-1}=0.368$.

(b) $W(n\ge 3)=1-W(0)-W(1)-W(2)=0.080$. 



<b>1.12</b> Radioactive source로부터 어떤 시간 간격 $t$ 동안에 $\alpha$ 입자가 방출되었다고 하자. $\alpha$ 입자는 emitted at random times, the probability of a radioactive disintegration occurring during any such time $\Delta t$ is completely independent of whaterver disintegrations uccur at other times. 더우기 $\Delta t$ 는 매우 작아서 $\Delta t$ 동안에 두번 이상의 disintegration이 일어날 확률은 무시할 수 있을 정도로 작다고 하자. 이것은 $\Delta t$ 동안에 disintegration이 일어날 확률 $p$ 가 $1$ 보다 매주 작음을 의미하며 ($p \ll 1$), $1-p$ 는 $\Delta t$ 동안 disintegration이 일어나지 않을 확률인다. 각각의 이러한 time interval $\Delta t$ 는 독립시행(independent trial)로 간주될 수 있으며 주어진 시간 $t$ 동안 $N=t/\Delta t$ 번의 시행이 이루어졌다고 여겨질 수 있다.

(a) $W(n)$ 을 $t$ 동안 $n$ 번의 disintegration이 발생할 확률이라 할 때 $W(n)$ 은 Poisson 분포로 주어짐을 보여라.

(b) Radioactive source에서 dinsintegration이 평균적으로 분당 24번 일어난다고 하자. 이 때 10초동안 $n$ 번의 count를 얻을 확률은 무엇인가? $0$ 에서 $8$ 까지의 numberical value를 구하라.

---

(a) $N=t/\Delta t$ 의 시행에서 $n$ 번의 성공을 이룰 확률은 bionomial distribution에 의해
$$
W(n) = \dfrac{N!}{n! (N-n)!}p^n(1-p)^{N-n}
$$
임을 알 수 있다. 문제의 조건에 의해 $p \ll 1$ 이며, $\overline{n}= Np \ll N$ 이므로 문제 1.9 에 의해 poisson distribution으로 생각 할 수 있다. 즉,
$$
W(n)= \dfrac{(Np)^n}{n!}e^{-Np} = \dfrac{\lambda^n}{n!}e^{-\lambda} \quad \text{where }\lambda = Np
$$
 이다.

(b) 10초동안 평균 4번의 disintegration이 일어나므로 $\lambda = 4$ 임을 알 수 있다. 즉,
$$
W(n) = \dfrac{4^n}{n!}e^{-4}
$$
이다.

(b) $W(0)=0.0183$, $W(1)= 0.073$, $W(2)= 0.147$, $W(3)= 0.195$, $W(4)=0.195$, $W(5)= 0.156$,
$W(6)= 0.104$, $W(7) = 0.060$, $W(8)= 0.030$



<b>1.13 </b> 금속은 뜨거운 filamnet로부터 진공으로 evaporated 되며, 이 결과로 금속 원자는 어느 정도 떨어진 quartz plate 표면으로 가서 금속 박막이 된다. 이 quartz plate 는 저온으로 유지되어 quartz plate 표면으로 입사된 금속 원자가 더이상 이동하지 않고 고정되도록 한다. 금속 원자는 plate의 어느 위치에도 동등한 확률로 impinged 된다고 가정한다.

Substrate 를 이루는 원자의 면적이 $b^2$ 이고 $b$ 는 metal atom의 지름일 때, 이 면적에 쌓이는 (piled up)  metal atom의 갯수가 근사적으로 Poisson distribution을 이룸을 보여라. 

충분한 metal을 evaporate 시켜  평균 6 atomic layer에 달하는 metal film을 쌓았다고 하자.  전체 면적중 metal에 의해 cover 되지 않는 substrate area의 비율은 어느정도인가? 3 atom 두께로 쌓인 부분과 6 atom 두께로 쌓인 부분의 비율은 무엇인가?

---

(1) substrate 전체 면적에서 원자의 면적 $b^2$ 가 매우 작은것이 당연하므로 Poisson distribution.

(2) $\lambda = 6$. $W(0,\, \lambda =6)= 0.00247875$ , $W(3, \lambda=6)=0.08923508$ , $W(6,\, \lambda=6)=0.16062314$ 



<b>1.14</b> 동전을 400번 전졌을 때 215번 앞이 나올 확률을 구하시오. (gaussian 근사를 사용하시오.)

---

$N=400$, $p=0.5$, $\overline{n}=Np=200$, $\sigma^2 = npq=100$. $Z=\dfrac{X-\overline{n}}{\sigma}$ 이므로 정규분포에서 $(1.45, 1.55)$ 사이에 있을 확률을 구하면 된다. $0.130$



<b>1.15 </b> 전화선이 마을 $A$ 에서 마을 $B$ 로 연결되었다. 마을 $A$ 에는 2,000 개의 전화기가 있다. 만악 $A$ 마을의 전화기 사용자가 $B$ 로 즉각 전화 통화하는 것이 보장되기 위해서는 2000 개의 전화선이 필요한데 이는 상당한 낭비이다. 가장 전화선이 붐비는 한 시간동안에 $A$ 에서 $B$ 로 전화를 걸 때 평균 2분을 통화한다고 하자. 최대 1 퍼센트의 통화시도만이 즉각적인 통화에 실패하도록 하려면 $A$ 와 $B$ 사이의 회선은 최소 $M$ 회선 이상이어야 할 때 $M$ 을 구하여라. (Approximate the distribution by a Gaussian distribution to facilitate the arithmetic).

---

가장 바쁜 한 시간동안 평균 2분을 통화하므로 가장 바쁜 한 시간동안 어떤 회선이 통화중일 확률은 $p=2/60=1/30$ 이다. 2,000 개의 전화가 있으므로 평균 $\mu=2000 p \approx 66.67$ 개의 전화가 통화중이다.  통화 갯수의 표준편차 $\sigma = \sqrt{Npq} \approx 8.03$.
$$
\int_{-1/2}^{M+1/2} \exp \left( -\dfrac{x-\mu}{2\sigma^2} \right)dx > 0.99 \implies M>84.84 \implies M>85   
$$


<b>1.16</b> 부피 $V_0$ 의 콘테이너 안에 있는 $N_0$ 개의 non-interacting molecule gas 를 생각한다. 이 콘테이너 안의 subvolume $V$ 와 $V$ 안의 기체 $N$ 에 주목한다. 각각의 분자들은 이 콘테이너 안의 어디에나 확률로 존재할 수 있다고 하자. 따라서 분자가 $V$ 안에 존재할 확률은 $V/V_0$ 이다.

(a) $V$ 안에 존재하는 분자의 평균값 $\overline{N}$ 은 무엇인가? 이를 $N_0,\, V_0,\,V$ 를 이용하여 표현하시오.

(b) $V$ 안에 존재하는 분자의 갯수의 Relative dispersion $\overline{(N-\overline{N})^2}/\overline{N}^2$ 을 구하시오. 이를 $\overline{N},\,V,\,V_0$ 로 표현하시오.

(c) (b) 에서 $V \ll V_0$ 일 경우는 어떻게 되는가?

(d) $V\to V_0$ 의 경우 dispersion $\overline{(N-\overline{N})^2}/\overline{N}^2$ 는 어떻게 되어야 하는가? (b) 의 결과는 이에 일치하는가?

---

(a) $\overline{N}=\dfrac{N_0 V}{V_0}$

(b) $\overline{(N-\overline{N})^2}=N_0 \times \dfrac{V}{V_0}\times \left(1-\dfrac{V}{V_0}\right)$ 이므로 $\dfrac{\overline{(N-\overline{N})^2}}{\overline{N}^2} = \dfrac{1-V/V_0}{\overline{N}}=\dfrac{V_0-V}{\overline{N}V_0}$

(c) $V \ll V_0 \implies \overline{(N-\overline{N})^2} \to 1/\overline{N}$ 

(d) $0$



<b>1.17 </b> 문제 1.16 에서 $0 \ll V/V_0 \ll 1$ 을 가정하자. 이 때 $V$ 안에 존재하는 분자의 갯수가 $N$ 과 $N+dN$ 사이에 존재할 확률은 얼마인가?

---

Gaussian distribution $G(N)dN =\dfrac{1}{\sqrt{ 2 \pi \sigma^2}}\exp \left[- \dfrac{(N-\overline{N})^2}{2 \sigma^2}\right] dN$ where $\overline{N}=\dfrac{N_0 V}{V_0}$ and $\sigma = \sqrt{\overline{N}\left(1-\dfrac{V}{V_0}\right)}$, 



<b>1.18 </b> 가스 분자가 충돌 사이에 같은 거리 $l$ 을 가며 방향은 모든 방향에 대해 같은 확률이라고 하자. 이런 $N$ 번의 이동 후에 시작점으로 부터의 이동거리의 제곱의 평균 $\overline{R^2}$ 는 무엇인가?

---

$j$ 번째 이동에서는 $l\hat{e}_j$ 만큼 움직인다. 여기서 $\hat{e}_j$ 는  $j$ 번째 이동 방향의 단위벡터이다. $N$ 번의 이동에서의 변위는  $\displaystyle \mathbf{R} = \sum_{j=1}^N \left( l\hat{e}_j\right) $ 이며,
$$
R^2= \mathbf{R}\cdot \mathbf{R} = l^2\sum_{i,\,j=1}^N (\hat{e}_i\cdot \hat{e}_j) = Nl^2 + l^2 \sum_{i\ne j=1}^N(\hat e_i \cdot \hat e_j)
$$
이다. second term의 기대값이 $0$ 임은 자명하므로 $\overline{R^2}=Nl^2$ 이다.



<b>1.19 </b> total emf가  $V$ 인 전지가 저항 $R$  에 연결되었다면 저항에 dissipated 되는 power $P= V^2/R$ 이다.  베터리는  $N$ 개의 개별적인 cell 로 이루어져 직렬 연결되어있다.전지가 오래되어 모든 cell이 정상적이지는 않다고 가정하자. 그렇다면 각 cell이 정상적인  emf $v$ 를 가질 확률을 $p$ 라 놓고 emf 가 $0$  일 확률을 $1-p$  라 놓자. 각각의 cell은  statistically independent 하다. 이 조건에서 저항에서 dissipate 되는 평균 power $\overline{P}$ 를 구하여 $ N,\,v,\,p$ 로 표현하라.

---

정상적인  emf $v$ 를 갖는 cell 이  $n$ 개일 확률  $W(n)$은 $W(n)=\dfrac{N!}{n!(N-n)!}p^n (1-p)^{N-n}$ 이다. $V^2=n^2v^2$ 이므로,
$$
\overline{P}=\overline{V^2}/R,\, \quad\text{where } \overline{V^2}=\overline{n^2}v^2
$$
 임을 이용한다. Reif의 16 페이지에 나왔듯이 $\overline{n^2}=\overline{n}^2+Np(1-p)=N^2p^2+Np(1-p)$  이므로,
$$
\overline{P}=\dfrac{Npv^2}{R}\left(Np+1-p\right)
$$


<b>1.20 </b> 파장  $\lambda$, 속도 $c$ 의 linearly polarized electromagnetic radiation을 방출하는 $N$ 개의 유사한 안테나들을 생각한다. 이 안테나들은  $x$ 축을 따라  서로 $\lambda$ 간격으로 위치하고 있다. 한 observer 가 안테나들로부터 아주 멀리 떨어진 $x$ 축상에 위치하고 있다.  한 안테나가 radiates 하면 observer가 그  intensity (mean-square electric filed amplitude) $I$ 를 측정한다.

(a) 모든 안테나가 하나의 generator로 부터 진동수 $\nu=c/\lambda$ 로 모두 같은 phase 가 되도록 driven 된다고 할 때 observer로 부터 측정되는  intensity는 얼마인가?

(b) 모든 안테나가 같은 진동수($\nu = c/\lambda$) 이지만 random phase 가 되도록 driven 된다고 할 때 observer 로부터 측정되는 intensity는 얼마인가?

---

(a) $n^2I$. 

(b) 1.18과 같은 문제 $nI$. 



<b>1.21 </b> 일단 생략. 문제가 너무 길어...



<b>1.22</b> 1차원 random work 문제를 생각한다. Displacement가  $s$ 와 $s+ds$ 사이에 잇을 확률이 다음과 같이 주어진다.
$$
w(s)\,ds = \dfrac{e^{(s-l)^2/2\sigma^2}}{\sqrt{2\pi} \sigma}\,ds\,.
$$
$N$ 스텝 이후

(a) 원점으로부터의 mean displacement $\overline{x}$ 는 무엇인가?

(b) Dispersion $\overline{(x-\overline{x})^2}$ 는 무엇인가?

---

(a) $x=\sum_{i=1}^N s_i$. 
$$
\begin{aligned}
\overline{s} &= \int_{-\infty}^\infty s\, w(x)\,ds =\dfrac{1}{\sqrt{2\pi}\sigma} \int_{-\infty}^\infty  s\, e^{(s-l)^2/2\sigma^2}\, dx=l
\end{aligned}
$$
이므로 $\overline{x} = \sum_{i=1}^N \overline{s_i}= Nl$

(b) $\overline{(x-\overline{x})^2}=\overline{(x-Nl)^2}=\overline{x^2}-(Nl)^2$ 이므로,
$$
\overline{x^2}=\sum_{i=1}^N (s_i)^2 + \sum_{i=1}^N s_i \sum_{j\ne i, j=1}^N s_j = N\overline{s^2}+Nl(N-1)l 
$$
이다. 
$$
\overline{s^2}=\dfrac{1}{\sqrt{2\pi}\sigma}\int_{-\infty}^\infty s^2 e^{(s-l)^2/2\sigma^2}\,ds= \dfrac{1}{\sigma \sqrt{2\pi}} \left[\int_{-\infty}^\infty (t+l)^2e^{t^2/2\sigma^2} \, dt\right]=\sigma^2+l^2 
$$
이므로,
$$
\overline{(x-\overline{x})^2}=N(\sigma^2+l^2)-N(N-1)l^2-N^2l^2 =N\sigma^2\,.
$$



<b>1.23</b> 1차원에서의  random work problem 을 생각한다. $l>b$ 이며 각각의 step 에서 displacement는 $l+b$ 와 $l-b$ 사이에서 똑같은 확률을 가진다. $N$ step 이후 다음을 구하라.

(a) mean displacement $\overline{x}$.

(b) Dispersion $\overline{(x-\overline{x})^2}$. 

---

$j$-th step의 displacement를 $s_j$ 라 할 때 각각의 $s_j$ 는 다음과 같이 동일한 확률을 가진다.
$$
W(s)ds = \dfrac{1}{2b}ds\,,\quad \text{where }l-b\le s\le l+b
$$
그리고 각  step의 평균을  $\overline{s}$  라 하면,
$$
\overline{s}=\int_{l-b}^{l+b}\dfrac{s}{2b}ds=\dfrac{1}{4b}\left[(l+b)^2-(l-b)^2\right]=l
$$
이다.

(a) $\displaystyle x=\sum_{j=1}^N s_j$, $\displaystyle \overline{x} = Nl$. 

(b) $\overline{(x-\overline{x})^2}=\overline{(x-Nl)^2}=\overline{x^2}-(Nl)^2$ 이므로,
$$
\begin{aligned}
\overline{s^2} &= \dfrac{1}{2b} \int_{l-b}^{l+b} s^2 ds=\dfrac{1}{6b}\left[(l+b)^3-(l-b)^3\right]=\dfrac{1}{6b}(6l^2b+2b^3)=\dfrac{1}{3}(3l^2+b^2)\,, \\
\overline{x^2}&=\sum_{j=1}^N {s_j}^2+\sum_{i=1}^N \sum_{j\ne i, j=1}^N s_i s_j =N\overline{s^2}+N(N-1)\overline{s}^2 \\
&= Nl^2+\dfrac{Nb^2}{3} +N^2l^2-Nl^2= N^2l^2+\dfrac{Nb^2}{3}\,,\\
\overline{(x-\overline{x})^2} &=\overline{x^2}-(Nl)^2=\dfrac{Nb^2}{3}\;.
\end{aligned}
$$

<b>1.24</b> (a) 한 입자가 어떤 원의 원주에 equally likely 위치할 수 있다고 하자. $z$ 축이 원을 포함하는 평면에 위치하며 원의 중심을 지난다고 하자. $\theta$ 는 $z$ 축과 입자의 위치와 원의 중심을 잇는 직선의 사잇각이라고 하자. 이 angle이 $\theta$ 와  $\theta+d\theta$ 사이에 있을 확률은?

(b) 한 입자가 어떤 구의 표면에 equally likely 위치할 수 있다고 하자.  구의 중심을 지나는 한 직선을 $z$ 축으로 삼고 $\theta$ 를 입자의 위치와 원을 지나는 직선과 $z$ 축이 이루는 각이라고 하자. 이 때 입자가 $\theta$  와 $\theta+d\theta$ 사이에 위치할 확률은?

---

(a) $W(\theta)d\theta = \dfrac{1}{2\pi}d\theta$ 

(b) $W(\theta)d\theta = \dfrac{1}{2} \sin\theta d\theta$ 



<b>1.25 </b> $\text{CaSo}_4 \cdot 2\text{H}_2\text{O}$ 다결정이 $z$ 방향의 외부 자기장 $\boldsymbol{B}$ 에 노출되어 있다고 하자. $\text{H}_2\text{O}$ 의  proton 위치에서의 내부자기장은 주변의  proton 에 의해 생성되며 주변의 proton의 스핀이 외부자기장 방향으로 정렬되었을 때 내부자기장의 크기가  $z$ 축 방향으로 $\dfrac{\mu}{a^3}(3 \cos^2 \theta -1)$ 이다.  만약 주변 proton의  스핀이 외부자기장과 반대방향으로 정렬되었다면 proton 위치에서의 내부자기장의 크기는 $-\dfrac{\mu}{a^3}(3\cos^2 \theta -1)$  이다. 여기서 $\mu$ 는  proton의 magnetic moment 이며 $a$ 는 두  protons 사이의 거리 이고  $\theta$ 는 두  proton 사이를 잇는 직선과  $z$ 축이 이루는 각이다. 이 randomly oriented crystals 로 이루어진 시료에서 이웃하는  proton은 주어진 proton을 중심으로하는 반경 $a$ 의 구 표면의 어디든지 같은 확률로 존재할 수 있다고 하자.

(a) Neighboring proton의  spin이  $\boldsymbol{B}$ 와 평행 할 때, Internal field $b$ 가  $b$ 와  $b+db$ 사이에 있을 확률 $W(b)db$  는?

(b) Neighboring proton의 spin이  $\boldsymbol{B}$ 와 평행할 확률과 antiparallel 할 확률이 같을 때,  Internal field $b$ 가  $b$ 와  $b+db$ 사이에 있을 확률 $W(b)db$  는?

---

(a) $\theta$ 가 $[0,\, \pi/2]$ 에서 변할 때 $b$ 는 $[2\mu/a^3, -\mu/a^3]$, $\theta$ 가 $[\pi/2,\, \pi]$ 에서 $b$ 는 $[-\mu/a^3,\, 2\mu/a^3]$ 이므로 $W(b)db = 2\cdot W(\theta(b)) \left|\dfrac{d\theta}{db} \right|db$ 이다. 
$$
\begin{aligned}
W(\theta) d\theta &= \dfrac{1}{2}\sin\theta d\theta \,, \\
b &=\dfrac{\mu}{a^3}(3\cos^2 \theta -1) \,,\\ 
\left|\dfrac{db}{d\theta}\right| &= \dfrac{6\mu}{a^3} \sin\theta\cos \theta \,,\\
W(b)db &= 2\cdot W(\theta(b))\left|\dfrac{d\theta}{db}\right|db=\dfrac{a^3}{6}\sqrt{\dfrac{3}{a^3b\mu+\mu^2}} db

\end{aligned}
$$
(b) 만약 antiparallel 하다면, 
$$
W(b) db = \dfrac{a^3}{6} \sqrt{\dfrac{3}{\mu^2-a^3b\mu}} db
$$
이다. Parallel  한 경우를 $W_p$, antiparallel 한 경우를 $W_a$ 라 하자. Paralle 한 경우 $b$ 값의 범위는 $[-\mu/a^3, 2\mu/a^a]$ 이며 antiparallel 한 경우 $b$ 값 범위는 $[-2\mu/a^3,\, \mu/a^3]$ 이다. 이중 중복되는 값의 범위는 $[-\mu/a^3,\, \mu/a^3]$ 이므로,
$$
W(b) = \left\{\begin{array}{ll} \dfrac{a^3}{12}\sqrt{\dfrac{3}{a^3b\mu+\mu^2}} &, b>\dfrac{\mu}{a^3} \, \\ \dfrac{a^3}{12}\left[\sqrt{\dfrac{3}{\mu^2+a^3b\mu}} +\sqrt{\dfrac{3}{\mu^2-a^3b\mu}}\right]\qquad &, -\dfrac{\mu}{a^3}\le b \le \dfrac{\mu}{a^3} \\ \dfrac{a^3}{6}\sqrt{\dfrac{3}{\mu^2-a^3b\mu}} &, b<-\dfrac{\mu}{a^3} \;.\end{array} \right.
$$

<b>1.26 </b> 일차원 random wor problem 을 생각하자.  Single displacement가 $s$ 와 $s+ds$ 사이에 있을 확률 $w(s)ds$ 는 다음과 같다.
$$
w(s)ds = \dfrac{1}{\pi} \dfrac{b}{s^2+b^2}\,ds\;.
$$
$N$ step 이후 total displacement가 $x$ 와 $x+dx$ 사이에 있을 확률 $\mathcal{P}(x)dx$ 를 구하라.  $N$ 이 매우 클 때 Gaussian이 되는가? 그렇지 않다면 section 1.11의 central limit theorem을 위배하는가?

---
$$
\begin{aligned}
Q(k) &= \int_{-\infty}^\infty ds e^{iks} w(s)=\dfrac{b}{\pi} \int_{-\infty}^\infty \dfrac{e^{iks}}{s^2+b^2}ds  = \left\{\begin{array}{ll} e^{-kb} \,,\qquad &\text{if } k \ge 0, \\ e^{kb}\,, &\text{if } k < 0\,. \end{array} \right.
\end{aligned}
$$

이므로,
$$
\begin{aligned}
\mathcal{P}(x) &= \dfrac{1}{2\pi} \int_{-\infty}^\infty e^{-ikx}Q^N(k)\, dk = \dfrac{1}{2\pi} \left[\int_{-\infty}^0 e^{(Nb-ix)k}\, dk  + \int_{0}^\infty e^{-(Nb+ix)k} \, dk \,\right]\\
&=\dfrac{1}{2\pi}  \dfrac{Nb}{(Nb)^2+x^2}

\end{aligned}
$$


<b>1.27 </b> A very general 1D random work 을 생각한다. $i$-th displacement가 $s_i$ 와 $s_i + ds_i$ 사이에 있을 확률은 $w_i (s_i)ds_i$ 로 주어진다. 여기서  확률밀도 $w_i$ 는 $i$ 마다 서로 다를 수 있으며, 따라서 $i$-dependent 하다. 그러나 different displacement는 이외의 다른 어떠한 displacement와 statistically independent 할 수 있다. Sec 1.11의 논리를 이용하여 displacement number $N$ 이 매우 크면 total displacement가 $x$ 와 $x+dx$ 사이에 있을 확률 $\mathcal{P}(x)$ 가 Gaussian form에 근접하며 그 때 평균은 $\overline{x}=\sum \overline{s}_i$ 이고 dispersion은 $\overline{(\Delta x)^2}= \sum \overline{(\Delta s_i)^2}$ 이다. 이것은 a very general form of the central limit theorem 이다.

---

식 (1.10.6) 으로 부터
$$
\begin{aligned}
\mathcal{P}(x) &= \dfrac{1}{2\pi} \int_{-\infty}^\infty dk\, e^{-ikx} \int_{-\infty}^\infty ds_1 w_1(s_1)e^{iks_1}\cdots \int_{-\infty}^\infty ds_N w_N(s_N)e^{iks_N}  \\
&=\dfrac{1}{2\pi} \int_{-\infty}^\infty dk\, e^{ikx} Q_1(k) \cdots Q_N(k) \qquad \text{where } Q_i(k) = \int_{-\infty}^\infty ds_i w_i (s_i)e^{iks_i}\;.


\end{aligned}
$$
로 표현 할 수 있음을 알 수 있다.

