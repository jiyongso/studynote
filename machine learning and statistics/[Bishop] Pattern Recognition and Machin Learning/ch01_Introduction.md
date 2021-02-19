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





## 2. Probability Theory



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
\begin{align*}
\mathbb{E}[f]&=\sum_x p(x) f(x) &&\text{for descrete distribbution,}\\
&=\int  p(x) f(x)\, dx& &\text{for continuous distribution.}

\end{align*}
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
\begin{align*}
\operatorname{var}[f]&\equiv \mathbb{E}\left[(f(x)-\mathbb{E}[f(x)])^2\right] \\
&=\mathbb{E}[f(x)^2]-(\mathbb{E}[f(x)])^2\;.
\end{align*}
$$


<b>covariance</b>
$$
\begin{align*}
\operatorname{cov}[x,\,y]&\equiv \mathbb{E}_{x,\,y} \left[(x-\mathbb{E}[x]) (y-\mathbb{E}[y])\right] \\
&=\mathbb{E}_{x,\,y}[xy] -\mathbb{E}[x] \mathbb{E}[y]\;.

\end{align*}
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

- 

- 여기서 $p(\mathcal{D}|\mathbf{w})$ 를 **likelihood function**  하고  $p(\mathbf{w})$ 를 **prior distribution** 이라 한다. $p(\mathcal{D})$ 는 normalization constant 이다. 
- frequentist 든 Bayesian 이든 $p(\mathcal{D}|\mathbf{w})$ 가 중심적인 역할을 하지만 이에 대한 두 입장의 견해는 매우 다르다. 빈도주의 입장에서는 $\mathbf{w}$ 는 고정된 parameters 이며 그 값과 에러는 dataset $\mathcal{D}$ 의 분포를 고려하여 얻어진다. 그러나 Bayesian 입장에서는 유일한 datatset $\mathcal{D}$ 가 존재하며 the uncertainty in the parameters is expressed through a probability distribution over $\mathbf{w}$. 