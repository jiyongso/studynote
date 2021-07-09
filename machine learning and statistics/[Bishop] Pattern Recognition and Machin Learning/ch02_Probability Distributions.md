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
\text{Bern}(x|\mu)=\mu^x (1-\mu)^{1-x} \tag{2.2}
$$

베르누이 분포에서의 기대값과 분산은 다음과 같다.
$$
\begin{align}
\mathbb{E}[x]& =\mu\,,\tag{2.3}\\
\operatorname{var}[x] &= \mu (1-\mu)\,.\tag{2.4}

\end{align}
$$




Dataset $\mathcal{D}=\{x_1,\ldots,\,x_N\}$ of observed value $x$ 에 대해 likelhood function $p(\mathcal{D}|\mu)$ 는 $\mu$ 에 대한 함수로 아래와 같다. 
$$
p(\mathcal{D}|\mu)=\prod_{i=1}^N p(x_i |\mu)=\prod_{i=1}^N \mu^{x_i}(1-\mu)^{1-x_i} \tag{2.5}
$$


Likelihood 를 maximize 하기 위해 $\ln p(\mathcal{D}|\mu)$ 를 maximize 하자.
$$
\ln p(\mathcal{D}|\mu)=\sum_{i=1}^n \left[ x_i\ln\mu +(1-x_i)\ln (1-\mu) \right] \tag{2.6}
$$

이 log likelihood 함수는 $\sum_{i=1}^n$ 을 통해서 $\{x_n\}$ 에만 의존한다. 이 sum은 *sufficient statistic* for the data under distribution 의 example 을 제공한다. (일단 넘어간다. sffucient statistic 은 나중에 설명한다고 나온다.) 
$$
\dfrac{d}{d \mu} \ln p(\mathcal{D}|\mu)=\sum_{i=1}^N \left[\dfrac{x_i}{\mu}+\dfrac{1-x_i}{1-\mu}\right]=0\implies  \mu = \dfrac{1}{N} \sum_{i=1}^N x_i \tag{2.7}
$$

이 때의 $\mu$ 를 $\mu_{ML}$ 이라 하자. 즉 $\mu_{ML}$ 은 *sample mean* 이다.  



- 동전던지기에서 3번 연속으로 앞면이 나왔다고 하자 (충분히 나올 수 있을만한  상황이다). 앞면을 $x=1$, 뒷면을 $x=0$ 으로 하면 $\mu_{ML}=1$  이며.. (확률분포가 dirac delta function 이 되어야 한다. 이 책에선 소개 안하지만.) .. 이것은 maximum likelihood 의 overfitting 현상이다.



#### Binomial Distribution

- Bernoulli distribution을 따르는 확률변수 $x$ 에 대해  $N$ 개의 data 중 $x=1$ 인 것이 $m$ 번일 확률분포를  **bionomial distribution** 이라 하며 다음과 같은 형태를 갖는다.
  $$
  \operatorname{Bin}(m|N,\, \mu)=\begin{pmatrix} N \\ m \end{pmatrix}\mu^m (1-\mu)^{N-m} \qquad \text{where} \begin{pmatrix}N\\m \end{pmatrix}=\dfrac{N!}{m!(N-m)!}\tag{2.9}
  $$

- 

- Binomial distribution 의 기대값과 분산은 다음과 같다. (Exercise 2.4)

$$
\begin{align}
\mathbb{E}[m] &\equiv \sum_{m=0}^N m \operatorname{Bin}(m|N,\, \mu)=N\mu \tag{2.11}\\
\operatorname{var}[m] &\equiv \sum_{m=0}^N \left( m-\mathbb{E}[m] \right)^2\operatorname{Bin}(m|N,\,\mu)=N\mu(1-\mu) \tag{2.12}
\end{align}
$$

