Exercises 2
===



<b>2.1</b> 식 (2.2) 의 베르누이 분포가 다음 성질을 만족함을 보이시오.
$$
\begin{align}
\sum_{x=0}^1 p(x|\mu) &= 1 \tag{2.257}\\
\mathbb{E}[x] &= \mu \tag {2.258}\\
\operatorname{var}[x] &=\mu(1-\mu) \tag{2.259}

\end{align}
$$
베르누이분포를 따르는 random binary varible $x$ 의 엔트로피 $H[x]$ 는 다음과 같이 주어짐을 보이시오.
$$
H[x]=-\mu \ln \mu - (1-\mu)\ln (1-\mu) \tag{2.260}
$$

---

$$
\begin{align}
\sum_{x=0}^1 p(x|\mu) &= p(x=1|\mu)+p(x=0|\mu)=\mu + 1-\mu =1\\
\mathbb{E}[x]&=1 \cdot p(x=1|\mu)+p (x=0|\mu)=\mu\\
\operatorname{var}[x] &= (1-\mu)^2 p(x=1|\mu)+(0-\mu)^2p(x=1|\mu)=(1-\mu)^2\mu + \mu^2(1-\mu)=\mu(1-\mu)\\
H[x]&=-\sum_{x=0}^1 p(x|\mu) \ln p(x|\mu)=-\mu\ln \mu -(1-\mu)\ln (1-\mu)
\end{align}
$$



<b>2.2</b> 식 (2.2) 로 주어진 베르누이 분포의 형태는 $x$ 의 두 값 사이에 대칭적이지 않다. 어떤 경우, $x\in \{-1,\,1\}$ 로 잡은 equivalent formulation 이 유용할 경우가 있으며 이 경우
$$
p(x|\mu)=\left(\dfrac{1-\mu}{2}\right)^{(1-x)/2}\left(\dfrac{1+\mu}{2}\right)^{(1+x)/2}\tag{2.261}
$$
의 분포를 갖고, $\mu\in [-1,\,1]$ 이다.  (2.261)의 분포는 normalized 되어 있음을 보이고, 이 때 평균, 분산, 엔트로피를 구하라.

---

$$
\begin{align}
\sum_{x\in\{-1,\,1\}} p(x|\mu) &= \left(\dfrac{1+\mu}{2}\right)+\left(\dfrac{1-\mu}{2}\right)=1 & (\text{normalized})\\
\mathbb{E}[x] &=-1 \cdot \left(\dfrac{1-\mu}{2}\right) +1 \left(\dfrac{1+\mu}{2}\right)=\mu\\
\operatorname{var}[x] &=(-1-\mu)^2 \left(\dfrac{1-\mu}{2}\right)+(1-\mu)^2\left(\dfrac{1+\mu}{2}\right) =(1-\mu)(1+\mu)\\
H[x] &= -\sum_{x\in \{-1,\,1\}} p(x|\mu)\ln p(x|\mu) = -\left(\dfrac{1-\mu}{2}\right)\ln \left(\dfrac{1-\mu}{2}\right)- \left(\dfrac{1+\mu}{2}\right) \ln \left(\dfrac{1+\mu}{2}\right)

\end{align}
$$



<b>2.3 </b> 이 문제에서 우리는 (2.9) 로 주어진 binomial distribution 이 normalized 되어있음을 보일것이다. 우선 (2.10) 에서 정의된 총 $N$ 개 중에서 $m$ 개의 같은 것을 뽑는 조합을 이용하여 다음을 보인다.
$$
\begin{pmatrix} N \\ m \end{pmatrix} + \begin{pmatrix} N \\ m-1 \end{pmatrix} = \begin{pmatrix} N+1 \\ m \end{pmatrix} \tag{2.262}
$$
이를 이용하여 다음 결과를 induction 을 이용하여 보인다.
$$
(1+x)^N = \sum_{m=0}^N \begin{pmatrix} N \\ m \end{pmatrix} x^m \tag{2.263}
$$
이것은 *binomial theorem* 으로 알려져 있으며 모든 실수값 $x$ 에서 성립한다. 마지막으로 binomial distribution이 normalized 되어 있음을 보인다. 즉,
$$
\sum_{m=0}^N \begin{pmatrix} N \\ m \end{pmatrix} \mu^m (1-\mu)^{N-m}=1 \tag{2.264}
$$


----

우선, (2.262) 를 보인다.
$$
\begin{pmatrix} N \\ m \end{pmatrix} + \begin{pmatrix} N \\ m-1 \end{pmatrix} = \dfrac{N!}{m!(N-m)!}+\dfrac{N!}{(m-1)!(N-m+1)!}=\dfrac{N!(N-m+1)+N!m}{m!(N-m+1)!}=\dfrac{(N+1)!}{m!(N-m+1)!}=\begin{pmatrix} N+1 \\ m \end{pmatrix}
$$
이제 (2.263) 을 보인다. $N=1$ 일 때 좌변은 $1+x$ 이며 우변도 $1+x$ 이므로 성립한다. 이제 $N$ 에서 성립함을 보이자.
$$
\begin{align}
(1+x)^{N+1} &= (1+x)(1+x)^N=\sum_{m=0}^N \begin{pmatrix} N \\ m \end{pmatrix}x^m + \sum_{m=0}^N \begin{pmatrix} N \\ m \end{pmatrix}x^{m+1} \\
&=\sum_{m=0}^{N} \begin{pmatrix} N \\ m \end{pmatrix}x^{m} + \sum_{m=1}^{N} \begin{pmatrix} N \\ m-1 \end{pmatrix}x^{m}  +x^{N+1}\\
&=1+ \sum_{m=1}^N \begin{pmatrix} N+1 \\ m \end{pmatrix} x^m +x^{N+1} \\
&= \sum_{m=0}^{N+1} \begin{pmatrix} N+1 \\ m\end{pmatrix}x^m
\end{align}
$$
이다. 따라서 식 (2.263) 이 성립한다. 이제 (2.264) 를 보이자.
$$
\sum_{m=0}^N \begin{pmatrix} N \\ m \end{pmatrix} \mu^m (1-\mu)^{N-m}= (1-\mu)^N \sum_{m=0}^N \begin{pmatrix} N \\ m \end{pmatrix} \mu^m (1-\mu)^{-m}=(1-\mu)^N \left( 1+ \dfrac{\mu}{1-\mu}\right)^N=1
$$




<b>2.4 </b> binomial distribution 의 평균이 식 (2.11) 로 주어짐을 보이라. 이를 위해 normalization condition (2.264) 의 양변을 $\mu$ 에 대해 미분하고 재배치하여 $n$ 의 평균을 구하라. 비슷한 방법으로 식 (2.264) 를 다시 한번 미분하고 (2.11) 의 결과를 이용하여 binomial distribution의 분산에 대한 식 (2.12)를 얻으라.

---

식 (2.264)의 양변을 $\mu$ 에 대해 미분하면,
$$
\begin{align}
0 &= \sum_{m=1}^N \begin{pmatrix} N \\ m \end{pmatrix} m \mu^{m-1}(1-\mu)^{N-m} - \sum_{m=0}^{N-1} \begin{pmatrix} N \\ m \end{pmatrix} (N-m)\mu^m (1-\mu)^{N-m-1} \\
&=\sum_{m=1}^{N-1} \begin{pmatrix} N\\m \end{pmatrix}\mu^{m-1} (1-\mu)^{N-m-1}\left(m-m\mu -N\mu+ m\mu \right) + N\mu^{N-1} - N(1-\mu)^{N-1}\\
&= \sum_{m=1}^{N-1} \begin{pmatrix} N\\m \end{pmatrix}  m\mu^{m-1}(1-\mu)^{N-m-1}-N\sum_{m=1}^{N-1} \mu^m (1-\mu)^{N-m-1} +N\mu^{N-1}-N(1-\mu)^{N-1}\\
&= \sum_{m=0}^{N-1}\begin{pmatrix} N\\m \end{pmatrix}  m\mu^{m-1}(1-\mu)^{N-m-1}


\end{align}
$$

$$
\begin{pmatrix}m \\ n \end{pmatrix}
$$

