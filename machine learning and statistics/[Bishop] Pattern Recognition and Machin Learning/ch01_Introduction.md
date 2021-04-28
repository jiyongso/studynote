I. Introduction
===



- Training set : $\{\mathbf{x}_1,\ldots,\,\mathbf{x}_N\}$ 
- Target vector : $\mathbf{t}$
- 결국 우리는 $\mathbf{y}(\mathbf{x})$ 를 표현하는 함수를 구하는 것이다. 
- Supervised learning : input vectors 와 각각의 vector에 대한 target vector가 training set으로 주어지는 경우 이를 *supervised learning* 이라 한다. targent vector가 주어지지 않을 경우 *unsuperviesd learning* 이라 한다. 
- Supervised learning 에서 $\mathbf{y}(\mathbf{x})$ 가 유한개의 불연속적인 category 값만 가질 수 있을경우 이를 *classfication* 문제라 한다. 연속적인 값만 가질 수 있을 경우 이를 *regression* 이라 한다.
- Unsupervised learning 에서 데이터 사이에 유사한 것 끼리 group화 하는 것을 *clustering* 이라 하며, input space에서의 데이터의 분포를찾는것을 *density estimation* 이라 한다.
- 어떤 상황에서 최상의 결과(보상)를 갖는 행동을 trial and error를 통해 찾는 문제를 *reinforced learining* 이라 한다. 



## 1.1 Example : Polynomial Curve Fitting



#### 구조

- $N$ Input variable $\{x_1,\ldots,\,x_N\}$ and target variable $\{t_1,\ldots,\,t_N\}$.

- vector로 표현하여 $\mathbf{x}\equiv (x_1,\ldots,\,x_N)^T$, $\mathbf{t}\equiv (t_1,\ldots,\,t_N)^T$. 

- Polynomial
  $$
  y(x,\,\mathbf{w})=\sum_{j=0}^M w_j x^j\;. \tag{1.1}
  $$
  with $\mathbf{w}=(w_0,\ldots,\,w_M)^T$. 

- Typical error function
  $$
  E(\mathbf{w})=\dfrac{1}{2}\sum_{n=1}^N \left\{y(x_n,\,\mathbf{w})-t_n\right\}^2\;.\tag{1.2}
  $$
  여기서 $1/2$ 는 편의를 위해 붙인 factor. (이유는 나중에). 목적은 $E(\mathbf{w})$ 를 최소로 하는 $\mathbf{w}$ 를 찾는 것이다.이 때의 $\mathbf{w}$ 를 $\mathbf{w}^\ast$ 라 하자. 

- Root-mean-square error
  $$
  E_{RMS}=\sqrt{\dfrac{2E(\mathbf{w^\ast})}{N}}\;.\tag{1.3}
  $$
  



#### Regularization

Text 의 exmaple에서 보았듯이, polynomial curve fitting 에서 parameters의 갯수가 클 경우 항상 *over fitting* 문제가 발생한다. Bayesian approach 를 택할 경우 이러한 over-fitting을 피할 수 있으나 (왜 피할 수 있는지는 다음에..) polynomial curve fitting에서는 regularization 방법으로 over-fitting 문제를 회피한다. [회피라는 말이 가장 적당한 듯 하다.]



Regularization에서는 error function을 악간 고쳐서 사용하며 대표적인 형태는 다음과 같다.
$$
\widetilde{E}(\mathbf{w})=\dfrac{1}{2} \sum_{n=1}^N \left\{ y(x_n,\, \mathbf{w})-t_n\right\}^2+\dfrac{\lambda}{2}\| \mathbf{w}\|^2 \tag{1.4}
$$
여기서 $\|\mathbf{w}\|^2=\mathbf{w}^T \mathbf{w}$ 이다. $\lambda$ 는 일반적인 의미의 error function에  대해 추가되는 term $\|\mathbf{w}\|^2$ 의 가중치를 의미한다.  많은 경우 $w_0$ 를 제외하고 사용한다. 즉 $\|\mathbf{w}\|^2-w_0^2$ 를 사용한다. ($w_0$ 는 target variable의 origin의 위치의 선택문제이므로.) 통계학 문헌에서는 이러한 방법을 *shrinkage method* 라 부른다. 

> The particular case of a quadratic regularizer is called *ridge regression*. In the context of neural networks, this approach is know asn *weight decay*
>

- Text 에서 보았듯이 $\ln \lambda = -18$ (즉 $\lambda=1.525\times 10^{-8})$ 일 때 over-fitting 이 사라진다, 





## 1.2. Probability Theory



- Uncertainty의 근원 : 측정에서의 noise + finite size of data set



<b>Joint Probability</b>

Random varialble $X,\,Y$ 에 대해 $X$ 는 $x_1,\ldots,\,x_M$ 값을 가질 수 있으며, $Y$ 는 $y_1,\ldots,\,y_L$ 값을 가질 수 있다고 하자. 모두 $N$ 번의 시행에서 $X=x_i,\, Y=y_j$ 가 나온 횟수가 $n_{ij}$ 이었다. $N$ 번의 시행에서 $X=x_i$ 인 횟수는 $c_i$, $Y=y_j$ 인 횟수는 $r_j$ 라 하자. 
$$
p(X=x_i,\, Y=y_j)=\dfrac{n_{ij}}{N},\quad p(X=x_i)=\dfrac{c_i}{N},\quad p(Y=y_j)=\dfrac{r_j}{N}\;.
$$
이 때,
$$
p(X=x_i)=\sum_{j=1}^L p(X=x_i,\, Y=y_j)
$$
이며 (자명하다) 이를 **sum rule** 이라 한다. 



<b>Conditional probability</b>

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

\end{align*} \tag{1.5}
$$



<b>Bayes' theorem</b>
$$
p(Y\mid X)=\dfrac{p(X\mid Y) \, p(Y)}{p(X)}\;.\tag{1.6}
$$

With sum rule,
$$
P(X)=\sum_{Y}p(X \mid Y)\, p(Y)\,. \tag{1.7}
$$



<b>Independence of variable</b>

확률변수 $X,\,Y$ 에 때해 $p(X,\,Y)=p(X)\, p(Y)$ 일 때 $X$ 와 $Y$ 는 *independent* 하다고 한다.



#### 1.2.1 Probability densities



연속적인 변수, 이산적인 변수 모두에 대한 확률 분포함수를 probability density function 이라 하기도 하고, 이산적인 변수에 대해서 probability mass function 이라고 구분하여 부르기도 한다.



#### 1.2.2 Expectations and covariances



확률변수 $X$ 에 대한 확률분포가 $p(x)$ 일 때 $x$ 에 대한 함수 $f(x)$ 의 평균값을 **expectation** of $f(x)$ 라 하며 다음과 같이 쓴다.
$$
\begin{align}
\mathbb{E}[f]&=\sum_x p(x) f(x) &&\text{for descrete distribution,}\\
&=\int  p(x) f(x)\, dx& &\text{for continuous distribution.}

\end{align}
$$


다변수 확률분포에서 특정 변수에 대한 평균은 다음과 같이 쓴다. $\mathbb{E}_x [f(x,\,y)]$ 는 
$$
\mathbb{E}_x [f(x,\,y)]=\sum_x p (x,\,y) f(x,\,y) =\int p(x,\,y) f(x,\,y)\, dx
$$
<b>Conditional expectation value</b>
$$
\mathbb{E}_x [f \mid y\,]= \sum_x p(x\mid y) f(x)
$$


<b>Variance </b>

Variance of $f(x)$ is defined by
$$
\begin{align}
\operatorname{var}[f]&\equiv \mathbb{E}\left[(f(x)-\mathbb{E}[f(x)])^2\right] \\
&=\mathbb{E}[f(x)^2]-(\mathbb{E}[f(x)])^2\;.
\end{align}
$$


<b>covariance</b>
$$
\begin{align}
\operatorname{cov}[x,\,y]&\equiv \mathbb{E}_{x,\,y} \left[(x-\mathbb{E}[x]) (y-\mathbb{E}[y])\right] \\
&=\mathbb{E}_{x,\,y}[xy] -\mathbb{E}[x] \mathbb{E}[y]\;.

\end{align}
$$
$X,\,Y$ 가 독립변수이면 $\operatorname{cov}[x,\,y]=0$. 이다.



두 random variable vectors $\mathbf{x},\, \mathbf{y}$ 에 대한 covariance는
$$
\begin{align*}
\operatorname{cov}[\mathbf{x},\, \mathbf{y}]&= \mathbb{E}_{\mathbf{x},\, \mathbf{y}}\left[\left( \mathbf{x}-\mathbb{E}[\mathbf{x}]\right)\left( \mathbf{y}^T-\mathbb{E}[\mathbf{y}^T]\right)\right] \\
&=\mathbb{E}_{\mathbf{x},\,\mathbf{y}}[\mathbf{x}\mathbf{y}^T]-\mathbb{E}[\mathbf{x}]\,\mathbb{E}[\mathbf{y}^T]\,.

\end{align*}
$$
이다. $\operatorname{cov}[\mathbf{x}]\equiv \operatorname{cov}[\mathbf{x},\,\mathbf{x}]
$ 로 정의한다. 





#### 1.2.3 Bayesian Probabilities

- 지금까지 우리는 확률을 random, repeatable events의 빈도(frequencies)라는 관점에서 봤다. 이것을 확률에 대한 고전적인 (classical) 혹은 빈도주의자(frequentist) 해석이라 한다. 이제 우리는 확률이 uncertainty를 정량화하는 *Bayesian* 확률에 대한 관점을 학습할 것이다.

- Polynomial curve fitting example 을 생각하자.  측정된 값 $\mathcal{D}=\{t_1,\ldots,\,t_n\}$ 과 parameter $\mathbf{w}$ 에 대해 Bayes theorem은 다음과 같다.
  $$
  p(\mathbf{w}\mid \mathcal{D})=\dfrac{p(\mathcal{D}\mid\mathbf{w})p(\mathbf{w})}{p(\mathcal{D})}
  $$

- 여기서 $p(\mathcal{D}|\mathbf{w})$ 를 **likelihood function**  하고  $p(\mathbf{w})$ 를 **prior distribution** 이라 한다. $p(\mathcal{D})$ 는 normalization constant 이다. 
- frequentist 든 Bayesian 이든 $p(\mathcal{D}|\mathbf{w})$ 가 중심적인 역할을 하지만 이에 대한 두 입장의 견해는 매우 다르다. 빈도주의 입장에서는 $\mathbf{w}$ 는 고정된 parameters 이며 그 값과 에러는 dataset $\mathcal{D}$ 의 분포를 고려하여 얻어진다. 그러나 Bayesian 입장에서는 유일한 data set $\mathcal{D}$ 가 존재하며 the uncertainty in the parameters is expressed through a probability distribution over $\mathbf{w}$. 



#### 1.2.4 The Gaussian Distribution (Normal Distribution)

평균 (mean) $\mu$ 와 분산 $\sigma^2$ 에 대한 Gaussian distribution $\mathcal{N}(x\mid \mu,\,\sigma^2)$ 는 다음과 같다.
$$
\mathcal{N} (x\mid \mu,\,\sigma^2) = \dfrac{1}{\sigma \sqrt{2\pi }} \exp \left[-\dfrac{(x-\mu)^2}{2\sigma^2}\right]
$$
Gaussian distribution $\mathcal{N}(x\mid \mu,\,\sigma^2)$ 는 다음과 같은 성질을 갖는다.
$$
\begin{aligned}
\mathbb{E}[x] &=\int_{-\infty}^\infty x\, \mathcal{N}(x\mid \mu,\,\sigma^2)\,dx=\mu\;,\\
\mathbb{E}[x^2] &= \int_{-\infty}^\infty x^2 \mathcal{N}(x\mid \mu,\,\sigma^2)\,dx=\mu^2+\sigma^2\;,\\
\operatorname{var}[f] &=\mathbb{E}[x^2]-\left(\mathbb{E}[x]\right)^2=\sigma^2 \;.

\end{aligned}
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