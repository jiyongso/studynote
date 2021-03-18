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
