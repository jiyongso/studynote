I. Introduction
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
p(\mathbf{x}\mid \mu,\,\sigma^2)= \prod_{n=1}^N \mathcal{N}(x_n\mid \mu,\,\sigma^2)
$$
이며, 계산의 편의를 위해,
$$
\ln p(\mathbf{x}\mid \mu,\,\sigma^2)= - \dfrac{1}{2\sigma^2}\sum_{n=1}^N (x_n-\mu)^2-\dfrac{N}{2} \ln \sigma^2 - \dfrac{N}{2} \ln 2\pi
$$
이다. 이 때 $p (\mathbf{x}\mid \mu,\,\sigma^2)$ 를 최대화 하는 $\mu$ 와 $\sigma^2$ 를 $\mu_{ML},\,\sigma_{ML}^2$ 라 할 때 다음과 같다.
$$
\begin{align}
\mu_{ML} &= \dfrac{1}{N}\sum_{n=1}^N x_n \;,\\
\sigma_{ML}^2 &= \dfrac{1}{N} \sum_{n=1}^N (x_n-\mu_{ML})^2\;.
\end{align}
$$
Sample의 평균과 분산은 다음과 같으며 이에 대한 증명은 Exercises 1.12를 참고하라.

$$
\begin{aligned}
\mathbb{E}[\mu_{ML}]& =\mu \,\\
\mathbb{E}\left[\sigma_{ML}^2\right] & =\left(\dfrac{N-1}{N}\right)\sigma^2
\end{aligned}
$$

따라서 다음 값 $\widetilde{\sigma\,}^2$ 는 samples 로 부터 추정한 모집단의 분산과 같다. (즉 unbiased.) 이를 표본분산이라 한다.
$$
\widetilde{\sigma\,}^2 = \dfrac{N}{N-1}\sigma_{ML}^2 = \dfrac{1}{N-1} \sum_{n=1}^N\left(x_n-\mu_{ML}\right)^2
$$
 $N\to \infty$ 일 때 $\sigma_{ML}^2 \to \sigma^2$ 임은 쉽게 알 수 있다.



#### 1.2.5 Curve Fitting Revisited

$N$ 개의 input values $\mathbf{x} = (x_1,\ldots,\,x_N)^T$ 와 target values $\mathbf{t}=(t_1,\ldots,\,t_N)^T$ 사이에 polynomial $t=y(x;\mathbf{w})=w_0 + w_1x+ \cdots +w_nx^n$ 의 관계를 가정한다. Target value의 uncertainty 를 확률분포로서 표현하자. 이를 위해 주어진 $x$ 에 대해 target value의 확률은 $y(x,\,\mathbf{w})$ 를 중심으로 분산이 $\beta^{-1}$ 인 가우시안분포를 따른다고 가정한다. 즉,
$$
p(t\mid x,\,\mathbf{w},\, \beta)=\mathcal{N}(t\mid y(x,\,\mathbf{w}),\,\beta^{-1})
$$
 이다. 

$\{\mathbf{x},\,\mathbf{t}\}$ 를 이용하여 unknown parameters $\mathbf{w}$ 와 $\beta$ 를 결정하자. 그렇다면 likelyhood function은 다음과 같이 주어진다.
$$
p(\mathbf{t}\mid \mathbf{x},\,\mathbf{w},\,\beta)=\prod_{n=1}^N \mathcal{N}(t_n\mid y(x_n,\, \mathbf{w}),\, \beta^{-1})
$$
앞서와 같이 $\ln$ 을 취하면,
$$
\ln p(\mathbf{t}\mid \mathbf{x},\, \mathbf{w},\,\beta)= -\dfrac{\beta}{2} \sum_{n=1}^N \left[y(x_n,\,\mathbf{w})-t_n\right]^2+\dfrac{N}{2} \ln \beta - \dfrac{N}{2} \ln (2\pi)
$$
이 된다. 여기서 (고정된 $\beta$ 에 대해) $p(\mathbf{t}\mid \mathbf{x},\, \mathbf{w},\,\beta)$ 를 maximize 하는 것과 $\displaystyle \dfrac{1}{2}\sum_{n=1}^N \left[ y(x_n,\,\mathbf{w})-t_n\right]^2$ 를 minimize 하는 것은  동치이며 이렇게 하는 $\mathbf{w}$ 를 $\mathbf{w}_{ML}$이라 하자. 또한 $\beta$ 에 대해 미분하여 $p$ 를 maximize 하는 $\beta$ 를 찾아 $\beta_{ML}$ 이라 하면,,
$$
\dfrac{1}{\beta_{ML}}=\dfrac{1}{N}\sum_{n=1}^N \left[ y(x_n,\, \mathbf{w})-t_n\right]^2
$$
이다. 이제 우린는 maximum likely 한 확률 분포를 다음과 같이 얻는다.
$$
p(t\mid x,\,\mathbf{w}_{ML},\, \beta_{ML})=\mathcal{N}(t\mid  y(x,\,\mathbf{w}_{ML}),\,\beta_{ML}^{-1})
$$





- 베이즈 통계를 위한 짧은 formulas

$$
\begin{align}
p(a|x)&=\sum_y p(a| x,\,y)\, p(y| x) & (\text{B}1) \\
p(a|x,\,y) &= \dfrac{p(x|a,\,y)\, p(a|y)} {p(y|x)} & (\text{B}2)
\end{align}
$$

*proof*

(1)
$$
\begin{align}
\sum_y p (a\mid x,\,y)\, p(y\mid x)&=\sum_y \dfrac{p(a,\,x,\,y)}{p(x,y)} \cdot \dfrac{p(x,\,y)}{p(x)} =\sum_y \dfrac{p(a,\,x,\,y)}{p(x)} \\
&=\dfrac{1}{p(x)}\sum_{y}p(a,\,x,\,y) = \dfrac{p(a,\,x)}{p(x)} \\
&=p(a|x)
\end{align}
$$
(2)
$$
\begin{align}
\dfrac{p(x|a,\,y)\, p(a|y)}{p(y|x)} &= \dfrac{p(a,\,x,\,y)}{p(a,\,y)} \cdot \dfrac{p(a,\,y)}{p(y)} \cdot \dfrac{p(y)}{p(x,\,y)}=\dfrac{p(a,\,x,\,y)}{p(x,\,y)}=p(a|x,\,y)
\end{align}
$$


이제 Bayesian 접근법을 좀 알아보자. $\mathbf{w}$ 가 $\alpha$ 의 정확도를 갖는 Gaussian 분포를 따른다고 하자. 그렇다면,
$$
p(\mathbf{w}|\alpha)=\mathcal{N}(\mathbf{w}|0,\,\alpha^{-1}\mathbf{I})=\left(\dfrac{\alpha}{2\pi}\right)^{(M+1)/2} \exp \left(-\dfrac{\alpha}{2}\mathbf{w}^T \mathbf{w}\right)
$$
이다. 여기서 $M$은 degree of polynomial 이며 따라서 $\mathbf{w}$ 는 $M+1$ 개의 elements를 가진다.

또한 식 (B2) 로부터 다음을 알 수 있다.
$$
\begin{align}
p(\mathbf{w}|\mathbf{x},\,\mathbf{t},\,\alpha,\,\beta) &=\dfrac{p(\mathbf{t}|\mathbf{x},\,\mathbf{w},\,\alpha,\,\beta)\, p(\mathbf{w}|\mathbf{x},\alpha,\,\beta)}{p(\mathbf{x},\,\alpha,\,\beta |\mathbf{t})} 
\end{align}
$$
 우리는 $\mathbf{t}$ 가 $\alpha$-independent 하며, $\mathbf{w}$ 가 $\beta$-independent 함을 알고 있다. 



## 1.5 Decision Theory

#### 1.5.0 Introduction

$X$-선 사진 촬영을 통해 암인지 아닌지 판별하는 의사라고 하자. 이는 Classification 문제이며 암인 경우 $C_1$, 암이 아닌 경우를 $C_2$ 라 하자. $X$ 선 사진을 vector $\mathbf{x}$ 이고 그 결과를 $\mathbf{t}$ 라 하자.

Bayes' theorem 에 따라
$$
p(C_k|\mathbf{x})=\dfrac{p(\mathbf{x}|C_k)\, p(C_k)}{p(\mathbf{x})}
$$
가 성립한다. 여기서 

- $p(C_k)$ 는 prior probability for $C_k$  로서 암일 확률 $p(C_1)$ 과 암이 아닐 확률 $p(C_2)$ 의 2가지이다.
- $p(\mathbf{x}|C_k)$ 는 학습에 의해 얻는 likelihood function 이다.



#### 1.5.1 Minimizing the Misclassification Rate

- 우리의 목표가 misclassification을 최소화 하는 것이라고 하자. 이 때 우리는 input space를 어떤 규칙에 따라 몇개의 영역으로 분할할 필요가 있다. 각각의 영역 $R_k$ 를 **decision region** 이라 한다. 각각의 $\{R_k\}$ 는 서로 disjoint 하다.  Decision regions 사이의 경계를 **decision boundary** 혹은 **decision surface** 라 한다.

- Inputs 를 그 결과가 되는 $C_1,\,C_2$ 에 따라 $R_1,\,R_2$ 의 decision region으로 나누자. 그렇다면 위의 암 판정에서 에러가 발생할 확률 $p(\text{mistake})$ 는 다음과 같다.
  $$
  \begin{align}
  p(\text{mistake})=p(\mathbf{x}\in R_1,\, C_2)+p(\mathbf{x}\in R_2,\,C_1)&=\int_{R_1} p(\mathbf{x},\,C_2)\,d\mathbf{x} +\int_{R_2}p(\mathbf{x},\,C_1)\,d\mathbf{x} \\
  
  &=\int_{R_1}p(C_2|\mathbf{x})\,p(\mathbf{x})\,d\mathbf{x} + \int_{R_2}p(C_1|\mathbf{x})\,p(\mathbf{x})\,d\mathbf{x}
  \end{align}
  $$

- 만약 $K$ 개의 classes 로 분류하는 문제의 경우는 에러가 발생학 확률을 최소화 하는 것보다 맞을 확률을 최대화 하는 것이 계산이 더 편하다. 이 확률을 $p(\text{correct})$ 라 하면,

$$
p(\text{correct})=\sum_{k=1}^K p(\mathbf{x}\in R_k,\,C_k)=\sum_{k=1}^K \int_{R_k} p(\mathbf{x},\, C_k)\, d\mathbf{x}
$$

이다. 

#### 1.5.2 Minimizing the Expected Loss

- 위의 결과는 암 환자를 건강하다고 판정했을 때와, 건강한 환자를 암환자로 판정했을 때의 상대적인 비중이 등가이지만, 실제에서는 암 환자를 건강하다고 판정하는 것이 더 큰 문제이다. 

- Minimization process 에서는 이것을 방지하기 위해 **loss function** 혹은 **cost function** 이라 불리는 함수를 도입한다. 여기서는 어떤 오류가 있었을 때의 cost를 차등적으로 둔다. 만약 Maximization process 를 수행하고자 할 때 이러한 역할을 하는 함수는 **utility function** 이라 불린다.

- 실제 $C_k$ class로 분류되어야 할 input $\mathbf{x}$ 가 $C_j$ class로 분류되었을 때의 차등적인 cost를 나타내는 행렬 $L_{kj}$ 로 쓴다. 예를 들어, 암인 경우의 $C_1$, 암이 아닌 경우 $C_2$ 로 했을 때 $L_{kj}$ 를 
  $$
  \begin{bmatrix}
  0 & 1000 \\ 1 & 0
  \end{bmatrix}
  $$
  으로 표현 할 수 있다. 

-   $p(\text{mistake})$ 를 생각하면 $L_{kj}$ 의 대각성분은 $0$ 이어야 할 것이다. 그렇다면 loss function은 다음과 같다.
  $$
  \begin{align}
  \mathbb{E}[L]&=\sum_k \sum_j \int_{R_j} L_{kj} p(\mathbf{x},\,C_k)\,d\mathbf{x} \\
  &=\sum_k \sum_j \int_{R_j}L_{kj}\, p(C_k|\mathbf{x})\, p(\mathbf{x})\, d\mathbf{x}
  \end{align}
  $$
  이 때 우리의 목표는 $\mathbb{E}[L]$ 을 최소로 하는 decision region $\{R_j\}$ 를 찾는 것이다. 



#### 1.5.3 The Rejection Option

- 어떤 특정한 영역에서 모든 $p(C_k|\mathbf{x}) \ll 1$ 이거나 가장 큰  $p(C_k|\mathbf{x})$  값이 그 이후의 값과 comparable 할 경우 문제가 된다. 이 경우 결정을 피할 수 있는데 이를 **reject option** 이라 한다. 
- 이것을 구현하는 방법 중의 하나는 확률에 대한 threshold $\theta$ 를 부여하여 가장 큰 $p(C_k|\mathbf{x})$ 에 대해 $p(C_k|\mathbf{x})\le\theta$ 일 때 reject option을 발동시키는 것이다.  



#### 1.5.4 Inference and Decision

- 지금까지는 classification problem 을 두단계로 나누었다. *Inference* 단계에서는 훈련 데이터를 이용하여 $p(C_k|\mathbf{x})$ model 을 학습하였고, *decision* 단계에서는 이 posterior probabilities 를 이용하여 optimal class assignment를 수행하였다. 
- Inference와 decision을 한 단계에 모두 수행하는 함수를 **discriminant function** 이라 한다.



##### 3 approaches for decision problems

<b>(a) 1-st Approach</b>

- 우선 각각의 class $C_k$ 에 대해 class-conditional density $p(\mathbf{x}|C_k)$ 를 구한다. 또한 별도로 prior class probabilities $p(C_k)$ 를 추정한다. 이를 바탕으로 아래와 같은 Bayes' theorem 을 사용하여 posterior class probabilities $p(C_k|\mathbf{x})$ 를 계산한다. 

$$
p(C_k|\mathbf{x} )=\dfrac{p(\mathbf{x}|C_k)\,p(C_k)}{p(\mathbf{x})}
$$

- 보통은 위 식의 분모  $p(\mathbf{x})$ 는 $p(\mathbf{x})=\sum_k p(\mathbf{x}|C_k)\,p(C_k)=\sum_k p(\mathbf{x},\,C_k)$ 를 이용하여 계산 할 수 있다. 
- 이제 posterior probability $p(C_k|\mathbf{x})$ 를 구했다면 새로운 input $\mathbf{x}$ 에 대해 decision theory를 사용하여 classification 을 수행한다. 
- 이렇게 명시적으로든 묵시적으로든 input과 output의 분포를 modeling 하는 것을 **generative models** 라 한다. (Because by sampling from them it is possible to generate synthetic data points in the input space)
- $p(\mathbf{x}|C_k),\, p(C_k) \longrightarrow p(C_k|\mathbf{x}),\, p(\mathbf{x})\longrightarrow [\text{decision}]$ 



<b>(b) 2-nd Approach</b>

- 우선 posterior probabilities $p(C_k|\mathbf{x})$ 을 구한다.(inference problem) 이후 decision theory 를 이용하여 새로운 $\mathbf{x}$ 를 classification 할 수 있도록 한다. 이렇게 직접적으로 posterior probabilities 를 모델링 하는 접근법을 **discriminative models** 라 한다.
- $p(C_k|\mathbf{x})\longrightarrow [\text{decision}]$ 



<b>(c) 3-rd Approach</b>

- 각각의 input $\mathbf{x}$를 classification 하는 함수 $f$ 를 구한다. 이 경우 확률은 역할을 하지 않는다.



##### 3가지 방법들의 장단점들

- (a) 방법은 $\mathbf{x}$ 와 $C_k$ 에 관한  joint distribution $p(\mathbf{x},\,C_k)$ 를 구한다. 그런데 일반적으로 $\mathbf{x}$는 큰 차원을 가지고 있으므로 제대로 class-conditional density를 구하려면 다수의 training set 이 필요하다. 일반적으로 $p(C_k)$ 는 간단한 함수로 추정한다. (예를들어 $N$-classes 문제의 경우 $p(C_k)=1/N$ )
- (a) 방법을 통해 $p(\mathbf{x})$ 를 구할 수 있는데 이를 통해 input $\mathbf{x}$ 가 확률이 낮아 예측의 정확도가 떨어지는지 아닌지 확인 할 수 있다. 이를 *outlier detection* 혹은 *novelity detection* 이라 한다.
- 그러나 (a) 방법은 computational power를 가장 크게 소모하며 (특히 $p(\mathbf{x},\,C_k)$ 를 구할 때), 상당수의 경우 우리는  $p(C_k|\mathbf{x})$ 만을 필요로 하는데, 이 경우 (a) 방법은 불필요하게 자원을 소모할 수 있다. (a) 와 (b) 의 상대적인 장단점이나 결합 이용에 대한 references 가 존재한다.
- (c) 의 방법은 posterior probability $p(C_k|\mathbf{x})$ 를 계산하지 않는다. $p(C_k|\mathbf{x})$ 가 필요한 경우가 많이 있을 수 있다. 
  - Minimizing risk
  - Reject option
  - Compensating for class priors
  - Combining models



#### 1.5.5 Loss Function for Regression

- 지금까지는 classification을 다루었는데 여기서는 regression을 생각한다. 

Input $\mathbf{x}$ 에 대해 target $t$ (1-D target) 를 estimate 하는 $y(\mathbf{x})$ 에 대해 loss function $L(t,\,y(\mathbf{x}))$ 를 생각하자. 이 때 expected loss $\mathbb{E}[L]$ 은 
$$
\mathbb{E}[L]=\iint L(t,\,y(\mathbf{x}))\,p(\mathbf{x},\,t)\,d\mathbf{x}\,dt
$$
이다 많은 경우 $L(t,\,y(\mathbf{x}))=\{t-y(\mathbf{x})\}^2$ 로 주어지며, 이 때,
$$
\mathbb{E}[L]=\iint \{t-y(\mathbf{x})\}^2 \, p(\mathbf{x},\,t)\,d\mathbf{x}\,dt
$$
이다. 우리는 $\mathbb{E}[L]$ 을 최소화 하는 $y(\mathbf{x})$ 를 얻고자 한다. 만약 $y(\mathbf{x})$ 가 completely flexible function 이라고 가정하면 변분법을 이용하여
$$
\dfrac{\delta \mathbb{E}[L]}{\delta y(\mathbf{x})}=2\int \{t-y(\mathbf{x})\}p(\mathbf{x},\,t)\,dt =0
$$
일 때 최소화 됨을 알 수 있다. 이 식을 정리하면,
$$
y(\mathbf{x})=\dfrac{\int tp(\mathbf{x},\,t)dt}{\int p(\mathbf{x},\,t)dt}=\dfrac{\int tp(\mathbf{x},\,t)dt}{p(\mathbf{x})} =\int tp(t|\mathbf{x})\,dt=\mathbb{E}_t[t|\mathbf{x}]
$$
 임을 알 수 있다. 

만약 target이 multi dimensional $\mathbf{t}$ 라면,
$$
y(\mathbf{x})=\mathbb{E}_{\mathbf{t}}[\mathbf{t}|\mathbf{x}]
$$
이다. 



## 1.6 Information Theory



#### 1.6.1 Entropy of Random Variable $x$

$x$ 가 $M$ 가지의 값을 취할 수 있으며 이 값을 $x_1,\ldots,\,x_M$ 이라 하자. $N$ 개의 배치에서 $x=x_i$ 인 것의 갯수를 $n_i$ 라 할 때 경우의 수 $W$는 
$$
W=\dfrac{N!}{\prod_{i=1}^M (n_i)!}
$$
이다. 이 때 entropy $H$ 를 $H=\dfrac{1}{N}\ln W$ 로 정의하고 Stirling 근사 $\ln N \approx N\ln N - N$ for $N\gg 1$ 과 $p_i = \dfrac{n_i}{N}$ 를 사용하면,
$$
\begin{align}
H &= \dfrac{1}{N}\ln W \\
&\approx \dfrac{1}{N}\left(N \ln N - \sum_{i=1}^M n_i \ln n_i -N + \sum_{i=1}^M n_i\right)\\
&=\dfrac{\sum_{i=1}^M n_i}{N}\ln N-\sum_{i=1}^M \dfrac{n_i}{N} \ln n_i\\
&=-\sum_{i=1}^N \dfrac{n_i}{N}\ln \dfrac{n_i}{N}\\
&=-\sum_i p_i \ln p_i\;.
\end{align}
$$
즉 random variable $x$ 의 확률분포 $p(x)$ 가 주어졌을 때, 이에 대한 entropy $H[p]$ 는
$$
H[p]=-\sum_{x} p(x) \ln p(x) \tag{1.6.1}
$$
로 정의된다. 만약 $x$ 가 연속 확률변수라면, differential entropy $H[p]$ 를 다음과 같이 정의할 수 있다.
$$
H[p]=-\int p(x) \ln p(x)\, dx \tag{1.6.2}
$$


#### 1.6.2 이산확률분포에서의 entropy 최대화

일단 이산확률분포에서 entropy를 최대화 하는 분포를 알아보자. Lagrange multiplier 방법을 사용하기 위해 다음과 같이 정의한다.
$$
\widetilde{H} = -\sum_{i}p_i \ln p_i-\lambda (\sum_i p_i-1)
$$
이 때,
$$
\dfrac{\partial \widetilde{H}}{\partial p_i}=0 \implies -\ln p_i -1-\lambda=0
$$
이므로 $\lambda = -1-\ln p_i$ for each $i$. 즉 $p_i=\text{const}$ 이어야 하므로 $p_i = \dfrac{1}{M}$ 이어야 한다. 또한 $\widetilde{H}$ 에 대한 2차 편미분을 구하면,
$$
\dfrac{\partial^2 \widetilde{H}}{\partial p_i \partial p_j}=\dfrac{\partial}{\partial p_i}\left(-\ln p_j-1-\lambda \right)=-\delta_{ij}\dfrac{1}{p_j} 
$$
이다.  



#### 1.6.3 연속확률분포에서의 entropy 최대화

아래와 같은 constrains 가 주어져 있다고 하자.
$$
\begin{align}
\int p(x)\,dx &=1\,,\\
\int xp(x) \,dx&= \mu\,,\\
\int (x-\mu)^2 p(x)\,dx &= \sigma^2\;.

\end{align}
$$
이 Lagrange multiplier $\lambda_1,\,\lambda_2,\,\lambda_3$ 를 이용하여 다음 $\widetilde{H}$ 를 이용하자.
$$
\widetilde{H}[p] = -\int p(x) \,\ln p(x)\,dx -\lambda_1 \left(\int p(x)\,dx-1\right)-\lambda_2 \left(\int x\,p(x)\,dx -\mu\right)-\lambda_3 \left(\int(x-\mu)^2p(x)\,dx-\sigma^2\right)
$$

$$
0=-\int \left[ \ln p + 1+\lambda_1+\lambda_2 x+\lambda_3 (x-\mu)^2 \right]dx
$$

이므로 $p=\exp (-1-\lambda_1 -\lambda_2 x -\lambda_3 (x-\mu)^2)$ 이다. problem 1.34 를 통해 풀면,
$$
p(x)=\dfrac{1}{\sigma \sqrt{2\pi}} \exp \left[-\dfrac{(x-\mu)^2}{2\sigma^2}\right]
$$
인 가우스 분포가 나온다. 즉 주어진 평균과 표준편차에 대해 entropy를 maximize 하는 분포는 가우스분포이다. 

또한 이 가우스분포에 대한 differential entropy $H[x]$ 는
$$
H[x]=\dfrac{1}{2} \left[1+\ln (2\pi \sigma^2)\right]
$$
이다. 



<b>Note : </b> 이산확률변수에 대한 엔트로피는 항상 non-negative 이다. 그러나 가우스 분포에 대한 differential entropy 에서 $\sigma^2<\dfrac{1}{2\pi e}$ 이면 $H[x]<0$ 이다.



#### 1.6.4 Conditional Entropy for Continuous Variables

일단 우리가 joint distribution $p(\mathbf{x},\,\mathbf{y})$ 를 알고 있다고 가정하자. 
$$
p(\mathbf{y}|\mathbf{x})=\dfrac{p(\mathbf{x,\,\mathbf{y}})}{p(\mathbf{x})}
$$
를 이용하여 $H[\mathbf{x},\,\mathbf{y}]$ 를 전개하면,
$$
\begin{align}
H[\mathbf{x},\,\mathbf{y}]&=-\iint p(\mathbf{x},\,\mathbf{y})\ln p(\mathbf{x},\,\mathbf{y})\,d\mathbf{x}\,d\mathbf{y}\\
&=-\iint p(\mathbf{x},\,\mathbf{y})\left[\ln p(\mathbf{y}|\mathbf{x}) + \ln p(\mathbf{x})\right]d\mathbf{x}\, d\mathbf{y}\\
&=-\iint p(\mathbf{x},\,\mathbf{y})\ln p(\mathbf{y|\mathbf{x}})d\mathbf{y}d\mathbf{x} -\iint p(\mathbf{x},\,\mathbf{y})\ln p(\mathbf{x}) d\mathbf{y}d\mathbf{x}\\
&=H[\mathbf{y}|\mathbf{x}]+H[\mathbf{x}]
\end{align}
$$
라 할 수 있다. 이 때 
$$
H[\mathbf{y}|\mathbf{x}]\equiv -\iint p(\mathbf{x},\,\mathbf{y})\ln p(\mathbf{y}|\mathbf{x})\,d\mathbf{y}d\mathbf{x}
$$
를 **conditional entropy** of $\mathbf{y}$ given $\mathbf{x}$ 라 한다. 