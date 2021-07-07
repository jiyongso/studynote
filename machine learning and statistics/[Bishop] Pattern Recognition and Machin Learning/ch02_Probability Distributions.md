II. Probability Distributions
===



#### Density Estimation

Random variable $\mathbf{x}$ 에 대해 $\mathbf{x}_1,\ldots,\,\mathbf{x}_N$ 번의 측정을 통해 확률분포 $p(\mathbf{x})$ 를 modelling 하는 것.

- 일단 여기서는 각각의 data points가 독립적이며 동일하게 분포되어있음을 가정한다. (즉 이전 측정의 영향을 받지 않는다.)

- 이러한 density estimation은 근본적으로 취약하다는것을 명심해야 한다. 왜냐하면 유한한 데이터셋을 만족시키는 확률분포는 무한히 많기 때문이다.




#### Patametric distrubition & Non parametric density estimation

- Gaussian 분포같이 몇개의 parameter 에 의해 정해지는 분포를 **parametric distribution** 이라 한다. 
- 이에 반해 분포가 데이터의 크기에 의존하면 이를 **non parametric density estimation**  이라 한다. 이 경우에도 parameters는 존재하지만 parameter 가 model의 복잡도(complexity) 만 제어할 뿐 분포의 형태를 제어하지는 않는다. 



## 2.1 Binary Distribution



#### Bernoulli Distribution

$x\in \{0,\,1\}$ 이며 $0\le \mu \le 1$ 에 대해  $p(x|\mu)$ 가 다음과 같은 분포를 **Bernoulli distribution** 이라 한다. 
$$
\begin{align}
p(x=1|\mu)&=\mu\,,\\
p(x=0|\mu)&=1-\mu\,.
\end{align} \tag{2.1}
$$
따라서, **Bernoulli Disbribution** 는 다음과 같이 쓸 수 있다. 
$$
\text{Bern}(x)=\mu^x (1-\mu)^{1-x} \tag{2.2}
$$

베르누이 분포에서의 기대값과 분산은 다음과 같다.
$$
\begin{align}
\mathbb{E}[x]& =\mu\,,\\
\operatorname{var}[x] &= \mu (1-\mu)\,.

\end{align}\tag{2.3}
$$




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