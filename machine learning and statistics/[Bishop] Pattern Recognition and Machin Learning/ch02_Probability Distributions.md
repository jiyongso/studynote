II. Probability Distributions
===



## 2.1 Binary Distribution



#### Bernoulli Distribution

$x\in \{0,\,1\}$ and $p(x|\mu)$ is defined by
$$
\begin{align}
p(x=1|\mu)&=\mu\,,\\
p(x=0|\mu)&=1-\mu\,.
\end{align}
$$
Then, the probability distribution is called as **Bernoulli Disbribution** and can be written as
$$
\text{Bern}(x)=\mu^x (1-\mu)^{1-x}
$$


- $\mathbb{E}[x]=\mu$, $\operatorname{var}[x]=\mu(1-\mu)$ 임을 쉽게 알 수 있다. 



Dataset $\mathcal{D}=\{x_1,\ldots,\,x_N\}$ of observed value $x$ 에 대해 likelhood function $p(\mathcal{D}|\mu)$ 는 $\mu$ 에 대한 함수로 아래와 같다. 
$$
p(\mathcal{D}|\mu)=\prod_{i=1}^N p(x_i |\mu)=\prod_{i=1}^N \mu^{x_i}(1-\mu)^{1-x_i}
$$


Likelyhood 를 maximize 하기 위해 $\ln p(\mathcal{D}|\mu)$ 를 maximize 하자.
$$
\ln p(\mathcal{D}|\mu)=\sum_{i=1}^n \left[ x_i\ln\mu +(1-x_i)\ln (1-\mu) \right]
$$

$$
\begin{align}
&\dfrac{d}{d \mu} \ln p(\mathcal{D}|\mu)=\sum_{i=1}^N \left[\dfrac{x_i}{\mu}+\dfrac{1-x_i}{1-\mu}\right]=0 \\
\implies & \mu = \dfrac{1}{N} \sum_{i=1}^N x_i
\end{align}
$$

이 때의 $\mu$ 를 $\mu_{ML}$ 이라 하자. 즉 $\mu_{ML}=\mathbb{E}[x]$ 이다. 