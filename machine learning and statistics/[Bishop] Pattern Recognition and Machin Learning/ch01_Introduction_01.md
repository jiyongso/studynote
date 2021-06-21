I. Introduction #1
===



#### Example of Machine Learning - Supervised Learning

- 우리가 어떤 데이터를 입력하여 machine learning을 통해 어떤 결과를 보고자 한다. 컴퓨터를 학습시키기 위해서는 그 결과값을 알고 있는 입력값과 그 결과값을 함께 사용하는데 이 학습을 위해 사용한 입력값을 **training set**, 각 training set 의 결과값을 **target vector** 라 한다. 즉,
  - Training set : $\{\mathbf{x}_1,\ldots,\,\mathbf{x}_N\}$ ,  target vector : $\mathbf{t}=\{t_1,\ldots,\,t_N\}$ 
  - 예를 들어 손으로 쓴 숫자를 확인하는 machine learning model 을 위해 100 개의 데이터로 훈련시킨다고 하자. 훈련을 위해서는 100 개 각각의 데이터에 대해 정확한 숫자값을 알아야 하고 이를 학습시켜야 한다. 100 개의 데이터가 training set $\{\mathbf{x}_1,\ldots,\,\mathbf{x}_{100}\}$ 이며 각각의 $\mathbf{x}_i$ 에 대한 이미 알고 있는 결과값이 target vector $\mathbf{t}=\{t_1,\ldots,\,t_{100}\}$  이다.
- Training set은 가능한 전체 입력값의 일부이며 가능한 전체 입력값의 집합을 $X$ 라 하고 가능한 전체 결과의 집합을 $T$ 라 하자. $X$ 와 $T$ 사이에는 우리가 목표료하는 유일한 함수 $\mathbf{y}:X \to T$가 존재할 것이며,  Training set 과 target vector를 이용하여 이 함수 $\mathbf{y}$ 를 찾는 것이다. 



#### Machine learning 의 단계

- **Feature extraction** : training, 혹은 test 단계에 사용될 데이터는 raw 데이터 일 수 도 있고 데이터에 대한 pre-processing 을 거쳐, 학습에 효율적인 혹은 계산 속도를 높일수 있 데이터로 변환시켜야 할 필요가 있다. 이 단계를 feature extraction 이라 한다. 다만 feature extraction 단계에서는 정보가 손실되는 경우가 많으며, 여기서 손실된 정보가 시스템의 전체적인 정확도가 시스템의 전체적인 정확도를 손상시킬수 있으므로 주의해야 한다.

- Training 단계 (Learning 단계) : 모델 학습 단계

- Test 단계 : 그 결과값을 아는, training set 과는 다른 입력값을 사용하여 모델의 유효성을 확인하는 단계. 이를 **generalization** 이라 한다.   

  



#### Machine Learning 의 분류

- Supervised learning : input vectors 와 각각의 vector에 대한 target vector가 training set으로 주어지는 경우 이를 *supervised learning* 이라 한다. target vector가 주어지지 않을 경우 *unsupervised learning* 이라 한다. 
  - Supervised learning 에서 $\mathbf{y}(\mathbf{x})$ 가 가질 수 있는 값의 갯수가 countable 이면 이를 *classification* 문제라 한다. uncountable 이면 이를 *regression* 이라 한다.
- Unsupervised learning 은 input vector 만 있고 target 이 없는 경우이다.  목표가  입력 데이터 사이에 유사한 것 끼리 group화 하는 것이라면 이를 *clustering* 이라 하며, input space에서의 데이터의 분포를찾는것을 *density estimation* 이라 한다. 혹은 고차원 데이터를 2차원 혹은 3차원으로 projection 시키고자 할 수 있는데 이를 *visualization* 이라 한다. 
- 어떤 상황에서 최상의 결과(보상)를 갖는 행동을 trial and error를 통해 찾는 문제를 *reinforced learning* 이라 한다. 
  - 여기서는 학습 알고리즘이 주변환경과 상호작용하는 상태(states)와 행동(actions)의 과정이 존재한다.
  - 많은 경우 actions에 대한 보상은 즉각적 보상 뿐 아니라 차후의 상태에서 취할 수 있는 행동에 대한 지연된 보상에 대해서도 평가한다.
  - 각 action에 대한 보상을 배분하는 것을 *credit assignment* 라 한다. 
  - *exploration* (탐험) 은 새로운 action을 통해 이 action이 얼마나 효율적인지 알아보는 것을 수행하는것이며, *exploitation* (이용) 현 상태에서 가장 최대의 보상을 얻을 수 있는 행동을 수행하는 것을 의미한다. 강화학습의 일반적인 특징중의 하나는 이 둘 사이의 trade-off 이다. 
  - 이 책에서는 강화학습을 자세히 다루지는 않는다.



## 1.1 Example : Polynomial Curve Fitting



#### 구조

- $N$ Input variable $\{x_1,\ldots,\,x_N\}$ and target variable $\{t_1,\ldots,\,t_N\}$.

- vector로 표현하여 $\mathbf{x}\equiv (x_1,\ldots,\,x_N)^T$, $\mathbf{t}\equiv (t_1,\ldots,\,t_N)^T$. 

- Polynomial
  $$
  y(x,\,\mathbf{w})=\sum_{j=0}^M w_j x^j\;. \tag{1.1}
  $$
  with $\mathbf{w}=(w_0,\ldots,\,w_M)^T$. 이 때 $M$을 order of polynomial 이라 한다.

- Typical error function
  $$
  E(\mathbf{w})=\dfrac{1}{2}\sum_{n=1}^N \left\{y(x_n,\,\mathbf{w})-t_n\right\}^2\;.\tag{1.2}
  $$
  여기서 $1/2$ 는 편의를 위해 붙인 factor. (이유는 나중에). 목적은 $E(\mathbf{w})$ 를 최소로 하는 $\mathbf{w}$ 를 찾는 것이다. (이는 다항식을 결정하는것과 동치이다.) 이 때의 $\mathbf{w}$ 를 $\mathbf{w}^\ast$ 라 하자. 일단 우리는 $E(\mathbf{w})\ge 0$ 이며, $E(\mathbf{w})=0 \iff y(x_n,\,\mathbf{w})=t_n \;\forall n=1,\ldots,N$ 임을 안다.  

- 다항식의 order를 얼마로 할 것이냐 하는 문제는 소위 *model comparison* 혹은 *model selection* 문제이다. 

- Root-mean-square error
  $$
  E_{RMS}=\sqrt{\dfrac{2E(\mathbf{w^\ast})}{N}}\;.\tag{1.3}
  $$
  
- 



#### Regularization

Text 의 example에서 보았듯이, polynomial curve fitting 에서 parameters의 갯수가 많을 경우 항상 *over fitting* 문제가 발생한다. Bayesian approach 를 택할 경우 이러한 over-fitting을 피할 수 있으나 (왜 피할 수 있는지는 다음에..) polynomial curve fitting에서는 regularization 방법으로 over-fitting 문제를 회피한다. [회피라는 말이 가장 적당한 듯 하다.]



Regularization에서는 error function을 악간 고쳐서 사용하며 대표적인 형태는 다음과 같다.
$$
\widetilde{E}(\mathbf{w})=\dfrac{1}{2} \sum_{n=1}^N \left\{ y(x_n,\, \mathbf{w})-t_n\right\}^2+\dfrac{\lambda}{2}\| \mathbf{w}\|^2 \tag{1.4}
$$
여기서 $\|\mathbf{w}\|^2=\mathbf{w}^T \mathbf{w}$ 이다. $\lambda$ 는 일반적인 의미의 error function에  대해 추가되는 term $\|\mathbf{w}\|^2$ 의 가중치를 의미한다.  많은 경우 $w_0$ 를 제외하고 사용한다. 즉 $\|\mathbf{w}\|^2-w_0^2$ 를 사용한다. ($w_0$ 는 target variable의 origin의 위치의 선택문제이므로.) 통계학 문헌에서는 이러한 방법을 *shrinkage method* 라 부른다. 

> The particular case of a quadratic reguralizer is called *ridge regression*. In the context of neural networks, this approach is know asn *weight decay*

- Text 에서 보았듯이 $\ln \lambda = -18$ (즉 $\lambda=1.525\times 10^{-8})$ 일 때 over-fitting 이 사라진다, 





## 1.2. Probability Theory



- Uncertainty의 근원 : 측정에서의 noise + finite size of data set



<b>Joint Probability</b>

Random variable $X,\,Y$ 에 대해 $X$ 는 $x_1,\ldots,\,x_M$ 값을 가질 수 있으며, $Y$ 는 $y_1,\ldots,\,y_L$ 값을 가질 수 있다고 하자. 모두 $N$ 번의 시행에서 $X=x_i,\, Y=y_j$ 가 나온 횟수를 $n_{ij}$ 라 하자. $N$ 번의 시행에서 $X=x_i$ 인 횟수는 $c_i$, $Y=y_j$ 인 횟수는 $r_j$ 라 하자. 즉,
$$
p(X=x_i,\, Y=y_j)=\dfrac{n_{ij}}{N},\quad p(X=x_i)=\dfrac{c_i}{N},\quad p(Y=y_j)=\dfrac{r_j}{N}\;.
$$
이다. 이 때,
$$
p(X=x_i)=\sum_{j=1}^L p(X=x_i,\, Y=y_j)
$$
이며 (자명하다) 이를 **sum rule** 이라 한다. 여기서 $P(X=x_i)$ 를 *marginal probability* 라 하기도 한다.



<b>Conditional probability</b>

$X=x_i$ 인 상황에서 $Y=y_j$ 인 확률을 $p(Y=y_j \mid X=x_i)$ 라 쓰며 *conditional probability* of $Y=y_j$ given $X=x_i$ 라 하고 다음과 같이 주어진다.
$$
p(Y=y_j\mid X=x_i)=\dfrac{n_{ij}}{c_i}
$$



<b>Product rule of probability</b>
$$
p(X=x_i,\, Y=y_j)=\dfrac{n_{ij}}N=\dfrac{n_{ij}}{c_i}\dfrac{c_i}{N}=P(Y=y_j\mid X=x_i)\cdot p(X=x_i)\;.
$$



<b> Summary</b>
$$
\begin{align*}
 \textbf{sum rule}&\qquad p(X)=\sum_Y p(X,\,Y)\,, \\
 \textbf{product rule}& \qquad p(X,\,Y)=p(Y\mid X)p(X) 

\end{align*} \tag{1.10}
$$



<b>Bayes' theorem</b>
$$
p(Y\mid X)=\dfrac{p(X\mid Y) \, p(Y)}{p(X)}\;.\tag{1.12}
$$

With sum rule,
$$
P(X)=\sum_{Y}p(X \mid Y)\, p(Y)\,. \tag{1.13}
$$



<b>Independence of variable</b>

확률변수 $X,\,Y$ 에 때해 $p(X,\,Y)=p(X)\, p(Y)$ 일 때 $X$ 와 $Y$ 는 *independent* 하다고 한다. $X,\,Y$ 가 independent 하다면 식 (1.10) 으로 부터 $p(Y|X)=P(Y)$ 임을 알 수 있다.



#### 1.2.1 Probability densities

연속확률변수일 때 $x\in (a,\,b)$ 일 확률 $p(x\in (a,\,b))$ 는
$$
p(x\in (a,\,b))=\int_a^b p(x)\,dx \tag{1.24}
$$
이다. 확률밀도함수 $p(x)$는 다음 두 조건을 만족해야 한다.
$$
\begin{align}
p(x) & \ge 0 \tag{1.25}\\
\int_{-\infty}^\infty p(x)\,dx &=1 \tag{1.26}
\end{align}
$$
<b>Change of variable</b>

$x=g(y)$ 이며 $y$ 에 대한 확률분포를 알고 싶을 때, 이 확률분포를 $p_y(y)$ 라 하면,
$$
p_y(y)=p(x)\left|\dfrac{dx}{dy}\right|=p(g(y))|g'(y) \tag{1.27}
$$
임을 쉽게 보일 수 있다.



<b>Cumulative distribution function</b>

$P(z)=p(x\in (-\infty,\,z))$ 를 cumulative distribution function 이라 하며,
$$
P(z) = \int_{-\infty}^z p(x)\, dx \tag{1.28}
$$
로 정의된다. $P'(x)=p(x)$ 임은 십게 알 수 있다.



다변수  $\mathbf{x}=(x_1,\ldots,\,x_D)$ 에 대한 확률분포는 $\mathbf{x}$ 를 포함하는 infinitesimal volume $\delta \mathbf{x}$ 에 대해 $p(\mathbf{x})\,\delta \mathbf{x}$ 로 주어지며 다음과 같은 성질을 만족한다.
$$
\begin{align}
p(\mathbf{x}) & \ge 0  \tag{1.29} \\
\int p(\mathbf{x})\,d\mathbf{x}&= 1\tag{1.30}

\end{align}
$$




연속적인 변수, 이산적인 변수 모두에 대한 확률 분포함수를 probability density function 이라 하기도 하고, 이산적인 변수에 대해서 probability mass function 이라고 구분하여 부르기도 한다.



Sum rule과 Bayes' theorem 을 생각하면 다음이 성립함을 알 수 있다.
$$
\begin{align}
p(x) &= \int p(x,\,y)\, dy \tag{1.31}\\
p(x,\,y)&=p(y| x)\,p(x) \tag{1.32}
\end{align}
$$




#### 1.2.2 Expectations and covariances



<b>Expectation </b> of $f$ 

확률변수 $X$ 에 대한 확률분포가 $p(x)$ 일 때 $x$ 에 대한 함수 $f(x)$ 의 평균값을 **expectation** of $f(x)$ 라 하며 다음과 같이 쓴다.
$$
\begin{align}
\mathbb{E}[f]&=\sum_x p(x) f(x) &&\text{for descrete distribution,} \tag{1.33}\\
&=\int  p(x) f(x)\, dx& &\text{for continuous distribution.} \tag{1.34}

\end{align}
$$

$N$ 개의 sample 이 주어졌을 때 expectation은 다음과 같이 근사 될 수 있다.
$$
\mathbb{E}[f] \approx \dfrac{1}{N} \sum_{i=1}^N f(x_n) \tag{1.35}
$$
(1.33)과 (1.34)는 (1.35)의 $N \to \infty$  극한과 동일하다.



다변수 확률분포에서 특정 변수에 대한 평균은 다음과 같이 쓴다. $\mathbb{E}_x [f(x,\,y)]$ 는 
$$
\mathbb{E}_x [f(x,\,y)]=\sum_x p (x,\,y) f(x,\,y) =\int p(x,\,y) f(x,\,y)\, dx \tag{1.36}
$$




<b>Conditional expectation value</b>

$p(x\,|\,y)$ 에 대한 $f(x)$ 의 기대값은 다음과 같다.
$$
\mathbb{E}_x [f \mid y\,]= \sum_x p(x\,|\, y)\, f(x) \tag{1.37}
$$



<b>Variance </b>

Variance of $f(x)$ is defined by
$$
\begin{align}
\operatorname{var}[f]&\equiv \mathbb{E}\left[(f(x)-\mathbb{E}[f(x)])^2\right] \tag{1.38} \\
&=\mathbb{E}[f(x)^2]-(\mathbb{E}[f(x)])^2\;. \tag{1.39}
\end{align}
$$

이다. 이 때  특히
$$
\operatorname{var}[x]=\mathbb{E}[x^2]-\mathbb{E}[x]^2\;\tag{1.40}
$$
dlek. 





<b>covariance</b>
$$
\begin{align}
\operatorname{cov}[x,\,y]&\equiv \mathbb{E}_{x,\,y} \left[(x-\mathbb{E}[x]) (y-\mathbb{E}[y])\right] \\
&=\mathbb{E}_{x,\,y}[xy] -\mathbb{E}[x] \mathbb{E}[y]\;.\tag{1.41}

\end{align}
$$
$X,\,Y$ 가 독립변수이면 $\operatorname{cov}[x,\,y]=0$ 이다.



두 random variable vectors $\mathbf{x},\, \mathbf{y}$ 에 대한 covariance는
$$
\begin{align*}
\operatorname{cov}[\mathbf{x},\, \mathbf{y}]&= \mathbb{E}_{\mathbf{x},\, \mathbf{y}}\left[\left( \mathbf{x}-\mathbb{E}[\mathbf{x}]\right)\left( \mathbf{y}^T-\mathbb{E}[\mathbf{y}^T]\right)\right] \\
&=\mathbb{E}_{\mathbf{x},\,\mathbf{y}}[\mathbf{x}\mathbf{y}^T]-\mathbb{E}[\mathbf{x}]\,\mathbb{E}[\mathbf{y}^T]\,.\tag{1.42}

\end{align*}
$$
이다. $\operatorname{cov}[\mathbf{x}]\equiv \operatorname{cov}[\mathbf{x},\,\mathbf{x}]
$ 로 정의한다. 





#### 1.2.3 Bayesian Probabilities

- 지금까지 우리는 확률을 random, repeatable events의 빈도(frequencies)라는 관점에서 봤다. 이것을 확률에 대한 고전적인 (classical) 혹은 빈도주의자(frequentist) 해석이라 한다. 이제 우리는 확률이 uncertainty를 정량화하는 *Bayesian* 확률에 대한 관점을 학습할 것이다.

- Polynomial curve fitting example 을 생각하자.  측정된 값 $\mathcal{D}=\{t_1,\ldots,\,t_n\}$ 과 parameter $\mathbf{w}$ 에 대해 Bayes theorem은 다음과 같다.
  $$
  p(\mathbf{w}\,|\, \mathcal{D})=\dfrac{p(\mathcal{D}\,|\,\mathbf{w})\,p(\mathbf{w})}{p(\mathcal{D})}
  $$

  - 데이터를 보기 전에 $p(\mathbf{w})$ 에 대해 임시로 정한다. $\mathcal{D}=\{t_1,\ldots,\,t_N\}$ 는 $p(\mathcal{D}\,|\,\mathbf{w})$ 에 반영된다. 
  - 여기서 $p(\mathcal{D}\,|\,\mathbf{w})$ 를 **likelihood function**  하고  $p(\mathbf{w})$ 를 **prior distribution** 이라 한다. $p(\mathcal{D})$ 는 normalization constant 이다. 
  
- frequentist 든 Bayesian 이든 $p(\mathcal{D}|\mathbf{w})$ 가 중심적인 역할을 하지만 이에 대한 두 입장의 견해는 매우 다르다. 빈도주의 입장에서는 $\mathbf{w}$ 는 고정된 parameters 이며 그 값과 에러는 dataset $\mathcal{D}$ 의 분포를 고려하여 얻어진다. 그러나 Bayesian 입장에서는 유일한 data set $\mathcal{D}$ 가 존재하며 the uncertainty in the parameters is expressed through a probability distribution over $\mathbf{w}$. 

- 널리 사용되는 빈도주의자들의 estimator는 *maximum likelihood* 이다. 그들에게 $p(\mathbf{w})=1$ 이므로 $p(\mathcal{D}\,|\,\mathbf{w})$ 를 최대화하면 자연스럽게 $p(\mathbf{w}\,|\,\mathcal{D})$ 가 최대화 된다. ML 에서는 $-\ln p(D\,|\,\mathbf{w})$ 를 *error function* 이라 한다. 따라서 likelihood 를 최대화 하는것은 error function 을 최소화 하는 것이다.

- bootstrap 방법에 대한 설명... 생략.

- 동전을 던졌을 때 앞면이 나올 확률을 $q$ 라 하자. 세번의 동전을 던져 셋 다 앞면이 나왔을 때, 빈도주의적 접근에 의하면, Likelihood function 
  $$
  p(\text{3 up}\,|\,q)=q^3
  $$
   이므로 $p(\text{3 up}|q)$ 를 최대화  하는 것은 $q=1$ 이다. 그런데 베이지언에서는 reasonable 한 prior distribution을 부여하므로, 덜 극단적인 결론에 도달하게 된다.	

- 베이지언에 대한 가장 일반적인 비판중의 하나는 prior distribution 이 어떤 선험적인 믿음의 반영이라기 보다는 수학적인 편리에 기반하여 선택된다는 것이다. 또한 prior distribution을 선택하는데는 주관이 개입할 수 밖에 없다는것도 비판의 대상이다. 이러한 주관성을 개선하기 위해 소위 *non-informative priors* 가 도입되기도 한다.



#### 1.2.4 The Gaussian Distribution (Normal Distribution)

평균 (mean) $\mu$ 와 분산 $\sigma^2$ 에 대한 Gaussian distribution $\mathcal{N}(x\mid \mu,\,\sigma^2)$ 는 다음과 같다.
$$
\mathcal{N} (x\mid \mu,\,\sigma^2) = \dfrac{1}{\sigma \sqrt{2\pi }} \exp \left[-\dfrac{(x-\mu)^2}{2\sigma^2}\right] \tag{1.46}
$$
여기서 $\mu$ 를 평균, $\sigma^2$ 를 분산 이라고 하며, 가우시안 분포는 $\mu$ 와 $\sigma^2$ 에 의해 결정된다. Gaussian distribution $\mathcal{N}(x\mid \mu,\,\sigma^2)$ 는 다음과 같은 성질을 갖는다.
$$
\begin{align}
\mathcal{N}&(x\mid \mu,\,\sigma^2)  \ge 0\,, \tag{1.47}\\
\int_{-\infty}^\infty &\mathcal{N}(x\mid \mu,\,\sigma^2)\, dx = 1,\, \tag{1.48}\\
\mathbb{E}[x] &=\int_{-\infty}^\infty x\, \mathcal{N}(x\mid \mu,\,\sigma^2)\,dx=\mu\;, \tag{1.49}\\
\mathbb{E}[x^2] &= \int_{-\infty}^\infty x^2 \mathcal{N}(x\mid \mu,\,\sigma^2)\,dx=\mu^2+\sigma^2\;,\tag{1.50}\\
\operatorname{var}[f] &=\mathbb{E}[x^2]-\left(\mathbb{E}[x]\right)^2=\sigma^2 \;. \tag{1.51}

\end{align}
$$
$\mathbb{R}^\mathcal{D}$ 에서 평균 $\boldsymbol{\mu}$ 와 covariance $\boldsymbol{\Sigma}$ 를 갖는 Gaussian distribution은 다음과 같다.
$$
\mathcal{N}(\boldsymbol{x}\mid \boldsymbol{\mu},\,\boldsymbol{\Sigma}) = \dfrac{1}{(2\pi)^{\mathcal{D}/2}}\dfrac{1}{\left|\boldsymbol{\Sigma}\right|^{1/2}} \exp \left[-\dfrac{1}{2} (\boldsymbol{x}-\boldsymbol{\mu})^T \boldsymbol{\Sigma} (\boldsymbol{x}-\boldsymbol{\mu})\right]
$$



<b>1-변수 가우스분포에서의 $\mu$와 $\sigma^2$ 의 추정 -Maximum Likelyhood </b> 

- 어떤 scalar variable $x$ 에 대해 $N$ 번 측정한 것을 $\mathbf{x}=(x_1,\ldots,\,x_N)^T$ 라 하자. ($\mathbf{x}$는 $\boldsymbol{x}=(x_1,\ldots,\,x_\mathcal{D})^T$  와는 다르다!)  We shall suppose that the observations are drawn independently from a Gaussian distribution whose mean $\mu$ and variance $\sigma^2$ are unknown, and we would like to determine these parameters from the data set.
- <b>i.i.d </b> : independent and identically distributed.
- $N$ 번의 측정이 i.i.d. 로 이루어졌으며 $x$ 가 (아마도) 가우스 분포를 따른다고 할 때, 측정된 데이터로부터 $\mu$ 와 $\sigma^2$ 를 산출하는 것은 다음과 같다.

우선 $N$ 측정에서 $\mathbf{x}$ 가 관측될 확률은
$$
p(\mathbf{x}\mid \mu,\,\sigma^2)= \prod_{n=1}^N \mathcal{N}(x_n\mid \mu,\,\sigma^2) \tag{1.53}
$$
이며 *likelihood function for the Gaussian* (가우시안 우도 함수)이라 불리운다.

<u>One common criterion for determining the parameters in a probability distribution using an observed data set is to find the parameter values that maximize the likelihood function. This might seem like a strange criterion because, from our foregoing discussions of probability theory, it would seem more natural to maximize the probability of the parameters given the data, not the probability of the data given the parameters</u>. 관찰 된 데이터 세트를 사용하여 확률 분포에서의 매개변수를 결정하는 일반적인 기준 중 하나는 우도 함수를 최대화하는 파라미터 값을 찾는 것이다. 앞서 언급 한 확률 이론 논의에서 매개 변수가 주어졌을 때의 데이터의 확률이 아니라 데이터가 주어졌을 때 매개 변수 확률을 최대화하는 것이 더 자연스러워 보이기 때문에 이것은 이상한 기준처럼 보일 수 있다. 사실 이 두가지는 연관되어 있으며, curve fitting의 맥락에서 뒤에 논의하기로 하자. 



어쨋든, 식 (1.53) 의 우도함수를 최대화하는 $\mu,\,\sigma^2$ 를 정하자. 계산의 편의를 위해 로그함수를 사용한다.
$$
\ln p(\mathbf{x}\mid \mu,\,\sigma^2)= - \dfrac{1}{2\sigma^2}\sum_{n=1}^N (x_n-\mu)^2-\dfrac{N}{2} \ln \sigma^2 - \dfrac{N}{2} \ln 2\pi \tag{1.54}
$$
이다. 이 때 $p (\mathbf{x}\mid \mu,\,\sigma^2)$ 를 최대화 하는 $\mu$ 와 $\sigma^2$ 를 $\mu_{ML},\,\sigma_{ML}^2$ 라 할 때 다음과 같다.
$$
\begin{align}
\mu_{ML} &= \dfrac{1}{N}\sum_{n=1}^N x_n \;,\tag{1.55}\\
\sigma_{ML}^2 &= \dfrac{1}{N} \sum_{n=1}^N (x_n-\mu_{ML})^2\;.\tag{1.56}
\end{align}
$$
<b>Bias</b>

Maximum likelihood approach는 분포의 분산을 underestimate 하는데 이런 현상을 bias라 한다. Sample의 평균과 분산의 기대값은 다음과 같은데(이에 대한 증명은 Exercises 1.12를 참고하라.), 
$$
\begin{align}
\mathbb{E}[\mu_{ML}]& =\mu \,\tag{1.57}\\
\mathbb{E}\left[\sigma_{ML}^2\right] & =\left(\dfrac{N-1}{N}\right)\sigma^2 \tag{1.58}
\end{align}
$$

식 (1.58)에서 보듯이 $\mathbb{E}\left[\sigma^2_{ML}\right]<\sigma^2$ 이다. 따라서 아래와 같이 정의된 $\widetilde{\sigma\,}^2$ 는 samples 로 부터 추정한 모집단의 분산과 같다. (즉 unbiased.) 이를 표본분산이라 한다.
$$
\widetilde{\sigma\,}^2 = \dfrac{N}{N-1}\sigma_{ML}^2 = \dfrac{1}{N-1} \sum_{n=1}^N\left(x_n-\mu_{ML}\right)^2 \tag{1.59}
$$
 $N\to \infty$ 일 때 $\sigma_{ML}^2 \to \sigma^2$ 임은 쉽게 알 수 있다. 실제로 $N$ 이 작지만 않으면 큰 문제는 되지 않는다.



Section 10.1.3 에서는 이 결과가 베이지안 접근법에서는 자동적으로 나오는 것을 볼 것이다.





#### 1.2.5 Curve Fitting Revisited



$N$ 개의 input values $\mathbf{x} = (x_1,\ldots,\,x_N)^T$ 와 target values $\mathbf{t}=(t_1,\ldots,\,t_N)^T$ 사이에 polynomial $t=y(x;\mathbf{w})=w_0 + w_1x+ \cdots +w_nx^n$ 의 관계를 가정한다. Target value의 uncertainty 를 확률분포로서 표현하자. 이를 위해 주어진 $x$ 에 대해 target value의 확률은 $y(x,\,\mathbf{w})$ 를 중심으로 분산이 $\beta^{-1}$ 인 가우시안분포를 따른다고 가정한다. 즉,
$$
p(t\mid x,\,\mathbf{w},\, \beta)=\mathcal{N}(t\mid y(x,\,\mathbf{w}),\,\beta^{-1}) \tag{1.60}
$$
 이다. 

훈련 데이터 $\{\mathbf{x},\,\mathbf{t}\}$ 를 이용하여 unknown parameters $\mathbf{w}$ 와 $\beta$ 를 결정하자. 그렇다면 likelihood function은 다음과 같이 주어진다.
$$
p(\mathbf{t}\mid \mathbf{x},\,\mathbf{w},\,\beta)=\prod_{n=1}^N \mathcal{N}(t_n\mid y(x_n,\, \mathbf{w}),\, \beta^{-1}) \tag{1.61}
$$
앞서와 같이 $\ln$ 을 취하면,
$$
\ln p(\mathbf{t}\mid \mathbf{x},\, \mathbf{w},\,\beta)= -\dfrac{\beta}{2} \sum_{n=1}^N \left[y(x_n,\,\mathbf{w})-t_n\right]^2+\dfrac{N}{2} \ln \beta - \dfrac{N}{2} \ln (2\pi) \tag{1.62}
$$
이 된다. 여기서 (고정된 $\beta$ 에 대해) $p(\mathbf{t}\mid \mathbf{x},\, \mathbf{w},\,\beta)$ 를 maximize 하는 것과 $\displaystyle \dfrac{1}{2}\sum_{n=1}^N \left[ y(x_n,\,\mathbf{w})-t_n\right]^2$ 를 minimize 하는 것은  동치이며 이렇게 하는 $\mathbf{w}$ 를 $\mathbf{w}_{ML}$이라 하자. 또한 $\beta$ 에 대해 미분하여 $p$ 를 maximize 하는 $\beta$ 를 찾아 $\beta_{ML}$ 이라 하면,
$$
\dfrac{1}{\beta_{ML}}=\dfrac{1}{N}\sum_{n=1}^N \left[ y(x_n,\, \mathbf{w})-t_n\right]^2 \tag{1.63}
$$
이다. 이제 우린는 maximum likely 한 확률 분포를 다음과 같이 얻는다.
$$
p(t\mid x,\,\mathbf{w}_{ML},\, \beta_{ML})=\mathcal{N}(t\mid  y(x,\,\mathbf{w}_{ML}),\,\beta_{ML}^{-1}) \tag{1.64}
$$





- 베이즈 통계를 위한 짧은 formulas

$$
\begin{align}
p(a|x)&=\sum_y p(a| x,\,y)\, p(y| x)  \tag{B1} \\
p(a|x,\,y) &= \dfrac{p(x|a,\,y)\, p(a|y)} {p(y|x)}  \tag{B2}
\end{align}
$$

---

*proof*
$$
\begin{align}
\sum_y p (a\,|\, x,\,y)\, p(y\mid x)&=\sum_y \dfrac{p(a,\,x,\,y)}{p(x,y)} \cdot \dfrac{p(x,\,y)}{p(x)} =\sum_y \dfrac{p(a,\,x,\,y)}{p(x)} \\
&=\dfrac{1}{p(x)}\sum_{y}p(a,\,x,\,y) = \dfrac{p(a,\,x)}{p(x)} \\
&=p(a|x)
\end{align}
$$

$$
\begin{align}
\dfrac{p(x|a,\,y)\, p(a|y)}{p(y|x)} &= \dfrac{p(a,\,x,\,y)}{p(a,\,y)} \cdot \dfrac{p(a,\,y)}{p(y)} \cdot \dfrac{p(y)}{p(x,\,y)}=\dfrac{p(a,\,x,\,y)}{p(x,\,y)}=p(a|x,\,y)
\end{align}
$$



이제 Bayesian 접근법을 좀 알아보자. $\mathbf{w}$ 가 $\alpha$ 의 정확도를 갖는 Gaussian 분포를 따른다고 하자. 그렇다면,
$$
p(\mathbf{w}|\alpha)=\mathcal{N}(\mathbf{w}|0,\,\alpha^{-1}\mathbf{I})=\left(\dfrac{\alpha}{2\pi}\right)^{(M+1)/2} \exp \left(-\dfrac{\alpha}{2}\mathbf{w}^T \mathbf{w}\right) \tag{1.65}
$$
이다. 여기서 $M$은 degree of polynomial 이며 따라서 $\mathbf{w}$ 는 $M+1$ 개의 elements를 가진다. $\alpha$ 와 같이 모델 파라메터의 분포를 제어하는 변수를 *hyperparameters* 라 한다. 

또한 Bayes' theorem으로 부터,
$$
[\text{posterior distribution for }\mathbf{w}] \propto [\text{likelihood function}]\times[\text{prior distribution}]
$$
임을 알고 있으므로,
$$
p(\mathbf{w}\,|\,\mathbf{x},\,\mathbf{t},\,\alpha,\,\beta) \propto p(\mathbf{t}\,|\,\mathbf{x},\,\mathbf{w},\,\beta)\cdot p(\mathbf{w}\,|\,\alpha) \tag{1.66}
$$
이다. 식 (1.66) 을 $-\ln$ 을 취하고 식 (1.62), (1,65)을 대입하면, maximum of the posterior 는 다음 식을 minimize 하는 것으로 으로 주어진다.
$$
\dfrac{\beta}{2}\sum_{n=1}^N \{y(x_n,\,\mathbf{w})-t_n\}^2+\dfrac{\alpha}{2} \mathbf{w}^T \mathbf{w} \tag{1.67}
$$
즉 Bayesian에서 posterior distribution을 maximizing 하는 것은 regularized sum of square error 함수의 minimization 과 동일하다. 



#### 1.2.6 Bayesian Curve Fitting

- 앞서 우리는 prior distribution $p(\mathbf{w}|\alpha)$ 에 대한 추정을 포함시켰지만, $\mathbf{w}$ 에 대한 point estimate 이므로 이것은 제대로 된 Bayesian treatment 가 아니다. 제대로 된 베이지언에서는 확률에 대한 합과 곱의 규칙들을 일관되게 적용해야 하며, 이는 $\mathbf{w}$ 에 대한 모든 값에 대해 적분해야 함을 의미한다. 이러한 marginalizations가 페턴 인식에서의 베이지언 방법의 핵심이다.
- 일단 $\alpha,\,\beta$ 를 고정시키고 (편의를 위해 식에서는 일단 빼자.), test set $\{\mathbf{x},\,\mathbf{t}\}$ 만을 생각하자. 베이지안 방법은

$$
p(t\,|\,x,\,\mathbf{x},\,\mathbf{t})=\int p(t\mid x,\,\mathbf{w})\, p(\mathbf{w}\mid\mathbf{x},\,\mathbf{t})\,d\mathbf{w} \tag{1.68}
$$

을 생각한다. 여기서 $p(t\mid x,\,\mathbf{w})$ 는 식 (1.60) 에 나와 있으며 $p(\mathbf{w}\mid \mathbf{x},\,\mathbf{t})$ 는 posterior distribution 이다. (식 (1.66) 을 보라.) 

- Section 3.3 에서 보겠지만, curve fitting example 과 같은 문제에서 이 posterior distribution 은 Gaussian 이며 해석적으로 계산 할 수 있다. 비슷하게 식 (1.68) 도 해석적으로 적분될 수 있으며 그 결과는 아래와 같은 가우시한 형태로 주어진다.

$$
\begin{align}
&p(t\mid x,\,\mathbf{x},\,\mathbf{t})=\mathcal{N}(t\mid m(x),\, s^2(x)) \tag{1.69}\\
\text{where} \qquad &m(x) =\beta \phi(x)^T \mathbf{S} \sum_{n=1}^N \phi (x_n) t_n \tag{1.70}\\
& s^2(x)=\beta^{-1}+ \phi(x)^T\mathbf{S}\phi(x) \tag{1.71}\\
&\mathbf{S}^{-1}= \alpha \mathbf{I} + \beta \sum_{n=1}^N \phi(x_n) \phi(x)^T \tag{1.72}\\
&\phi_i (x)=x^i \;(i\text{-th component of vector }\mathbf{x})
\end{align}
$$







## 1.3. Model Selection

- 최소자승법을 이용한 Polynomial curve fitting 에서 보았듯이 best generalization을 주는 최적의 다항식의 order $M$ 이 존재한다. 다항식의 order는 모델에서 free parameters의 갯수를 제어한다. Regularization 을 사용하면 regularization coefficient $\lambda$ 는 모델의 유효 복잡도(effiective complexcity) 를 통제한다. 
- 실제 응용에서 우리는 이러한 parameters 들을 결정해야 하며 이렇게 하는 주요 목적은 새로운 데이터에 대한 최소의 predictive performance를 얻기 위함이다. 또한 이렇게 complexicity parameters 에 대한 적당한 값을 찾는 것 뿐만 아니라, 특정 목표에 적합한 모델을 찾기 위해 다양한 모델을 고려할 필요가 있다.
- MLA (maximum likelihood approach) 에서 보았듯이 training set 에 대한 performance 가 다른 데이터에 대한 예측력을 보장해주지 않는다. (overfitting). 만약 데이터가 많다면 가용한 데이터중 일부를 다양한 모델을 학습시키거나, 주어진 모델에 대해 complexicity parameters 를 다양한 범위에서 학습시키는데 사용하고 이것을 독립적인 데이터를 사용하여 predictive performance를 비교하여 수 도 있다. 이렇게 학습데이터와 독립적으로 사용되는 데이터를 **validation set** 이라 한다. 이렇게 수차례 반복한 다음에 **test set** 이라 불리는 별도의 독립적인 데이터를 사용하여 최종적으로 평가할 수도 있다.
-  보통은 training과 testing에 사용될 수 있는 데이터가 부족한데, 이 경우 좋은 모델을 만들기 위해 training에 가능한 많은 데이터를 사용하고자 할 수 있다. 그러나 만약 validation set이 부족하면 it will give a relatively noisy estimate of predictive performance. 이 딜레마에 대한 해결방법중 하나로 cross validation 방법이 있다.



<b>Cross Validation</b>

- 전체 데이터를 $S$ 개의 group으로 나눈다. $S$ 개의 training group 으로 각 training group 마다 $S-1$ 개의 데이터 그룹을 training set으로 나머지 하나를 validation set으로 사용한다.

- Training group 마다 각자의 모델 (혹은 별도의 parameters set) 을 사용하므로 computationally expensive 하다. 또한 하나의 모델에 대한 다수의 complexcity parameter 를 갖게 될 수 있다. 이런 조합들을 탐색하다보면 최악의 경우 training run 이 parameter 갯수의 지수승으로 증가할수도 있다.!!!

- 우리는 더 좋은 접근법을 사용해야 한다. 이상적으로 이 접근법은 training data 에 의존해야 하며, 한번의 training run을 통해 비교 할 수 있는 다수의 hyperparameters와 model types 를 허용해야 하는데....

- 이를 위해 training data 에만 의존하며 over fitting에 의한 bias로부터 자유로운 성능 척도를 찾아야 한다.

- 역사적으로 복잡한 모델에서의 over fitting을 보상하는 penalty term을 추가함으로서 maximum likelihood의 bais를 교정하고자 하는 다양한 'information criteria' 가 제안되었다. 예를 들어 *Akaike information criterion* (AIC) 의 경우 
  $$
  \ln p(\mathcal{D}\mid \mathbf{w}_{ML})-M
  $$
  을 최대화 하는 모델을 선택한다. 여기서 $p(\mathcal{D}\mid \mathbf{w}_{ML})$ 은 best-fit log likelihood 이며 $M$ 은 모델에서 adjustable 한 parameter의 갯수이다. 이의 변형으로서 *Bayesian information criterion* 이 있는데 이는 section 4.4.1 에서 소개될 것이다. 이러한 criteria는 model parameter의 불확실성을 고려하지 않으며, 실제적으로는 과하게 간단한 모델을 선호한다. 

- 따라서 우리는 section 3.4 에서 fully Bayesian approach 로 전환할 것이며 이러한 complexity penalty 가 자연스럽고 원칙적인 방법으로 발생하는지 볼 것이다.

  



## 1.4 The Curse of Dimensionality

- Oil examples은 그냥 읽으면 되고..

- 우리가 다루고자 하는 입력 데이터가 고차원의 데이터 ($\mathcal{D}-\dim$)라고 가정해보자. 다항식 근사에서 order $3$ 까지 전개해보면,
  $$
  y(\mathbf{x},\,\mathbf{w})=w_0+\sum_{i=1}^\mathcal{D} w_i x_i + \sum_{i=1}^\mathcal{D}\sum_{j=1}^\mathcal{D} w_{ij}x_ix_j + \sum_{i=1}^\mathcal{D}\sum_{j=1}^\mathcal{D} \sum_{k=1}^\mathcal{D} w_{ijk}x_i x_j x_k \tag{1.74}
  $$
  이다. $\mathcal{D}$ 에 따라 3차항의 계수의 갯수는 $\mathcal{D}^3$ 개 만큼 증가하는 것처럼 보인다.(실제로는 interchange symmetry 로 인해 이것보다는 작지만 그래도 $\mathcal{D}\gg M$ 일 경우는 $\mathcal{D}^M$ 와 같이 증가한다. see exercise 1.16. 이것도 아주 급격하게 증가하는 것이다. )

- ${D}$ 차원의 구를 생각하자. ${D}$ 가 커질수록 구의 대부분의 부피는 표면에 분포한다. ${D}$ 차원에서 반경 $r$ 인 구의 부피 $V_D(r)=K_D r^D$ 이다 여기에 작은 $0<\epsilon\ll 1$ 을 생각하면 구 표면의 두께 $\epsilon$ 만큼의 껍질의 부피와 $D$ 차원에서의 unit sphere 의 부피의 비는,
  $$
  \dfrac{V_D(1)-V_D(1-r)}{V_D(1)}=1-(1-\epsilon)^D
  $$
  임을 안다. ${D}$ 가 커질 수록 작은 $\epsilon$ 에서의 값이 크다. 

- $D$ 차원 가우시안 분포에서 이 데이터를 polar coordinate 로 바꾸어 보자. 차원이 늘어날수록 $p(r)$ 에서 가장 높은 확률을 가진 값이 점점 커진다. 이는 고차원 구에서 대부분의 부피가 spherical shell에 위치한다는 앞의 논리와 상응한다. 

- 차원의 저주는 저차원에서의 직관이 고차원에서도 통용되지 않는 경우가 많음을 의미한다. 이 차원의 저주는 패턴 인식의 응용에 있어서 중요한 문제를 제기하지만 고차원을 다루는 효율적인 테크닉이 부족하거나 없다는 것을 의미하지는 않는다. 

  - 고차원의 데이터라도 실제로는 보다 낮은 차원의 특정 영역에 데이터가 제한되어 있는 경우가 흔하며,
  - 실제 데이터는 전형적으로 어떤 smoothness properties 를 (최소한 국소적으로라도) 가지고 있는 경우가 많다. 





