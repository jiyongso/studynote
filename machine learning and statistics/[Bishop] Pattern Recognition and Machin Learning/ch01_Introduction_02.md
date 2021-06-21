I. Introduction #2
===

## 1.5 Decision Theory

#### 1.5.0 Introduction

$X$-선 사진 촬영을 통해 암인지 아닌지 판별하는 의사라고 하자. 이는 Classification 문제이며 암인 경우 $C_1$, 암이 아닌 경우를 $C_2$ 라 하자. $X$ 선 사진을 vector $\mathbf{x}$ 이고 그 결과를 $\mathbf{t}$ 라 하자.

Bayes' theorem 에 따라
$$
p(C_k|\mathbf{x})=\dfrac{p(\mathbf{x}|C_k)\, p(C_k)}{p(\mathbf{x})} \tag{1.77}
$$
가 성립한다. 여기서 

- $p(C_k)$ 는 prior probability for $C_k$  로서 암일 확률 $p(C_1)$ 과 암이 아닐 확률 $p(C_2)$ 의 2가지이다.
- $p(\mathbf{x}|C_k)$ 는 학습에 의해 얻는 likelihood function 이다.



#### 1.5.1 Minimizing the Misclassification Rate

- 우리의 목표가 misclassification을 최소화 하는 것이라고 하자. 이 때 우리는 input space를 어떤 규칙에 따라 몇개의 영역으로 분할할 필요가 있다. 각각의 영역 $R_k$ 를 **decision regions** 라 하며 한  $R_k$ 의 모든 points는 하나의 class $\mathcal{C}_k$ 로 assign 될 것이다.  각각의 $\{R_k\}$ 는 서로 disjoint 하다.  Decision regions 사이의 경계를 **decision boundary** 혹은 **decision surface** 라 한다. 서로 분리된 영역이 하나의  decision region이 될 수 도 있다. 

- Inputs 를 그 결과가 되는 $\mathcal{C}_1,\,\mathcal{C}_2$ 에 따라 $R_1,\,R_2$ 의 decision region으로 나누자. 그렇다면 위의 암 판정에서 에러가 발생할 확률 $p(\text{mistake})$ 는 다음과 같다.
  $$
  \begin{align}
  p(\text{mistake})=p(\mathbf{x}\in R_1,\, \mathcal{C}_2)+p(\mathbf{x}\in R_2,\,\mathcal{C}_1)&=\int_{R_1} p(\mathbf{x},\,\mathcal{C}_2)\,d\mathbf{x} +\int_{R_2}p(\mathbf{x},\,\mathcal{C}_1)\,d\mathbf{x} \\
  
  &=\int_{R_1}p(\mathcal{C}_2|\mathbf{x})\,p(\mathbf{x})\,d\mathbf{x} + \int_{R_2}p(\mathcal{C}_1|\mathbf{x})\,p(\mathbf{x})\,d\mathbf{x}
  \end{align} \tag{1.78}
  $$

- 우리는 각각의  $\mathbf{x}$ 를 $\mathcal{C}_1$ 과 $\mathcal{C}_2$ 가운데 아무데나 assign 할 수 있다. $p(\text{mistake})$ 를 최소하 하기 위해서는 각각의  $\mathbf{x}$ 에 대해 $\min\{p(\mathbf{x},\,\mathcal{C}_1),\,p( \mathbf{x},\,\mathcal{C}_2)\}$ 를 적분해야 할 것이다. 

- 만약 $K$ 개의 classes 로 분류하는 일반적인 문제의 경우는 에러가 발생학 확률을 최소화 하는 것보다 맞을 확률을 최대화 하는 것이 계산이  좀 더 쉽다. 이 확률을 $p(\text{correct})$ 라 하면,

$$
p(\text{correct})=\sum_{k=1}^K p(\mathbf{x}\in R_k,\,C_k)=\sum_{k=1}^K \int_{R_k} p(\mathbf{x},\, C_k)\, d\mathbf{x} \tag{1.79}
$$

이다. 



#### 1.5.2 Minimizing the Expected Loss

- 위의 결과는 암 환자를 건강하다고 판정했을 때와, 건강한 환자를 암환자로 판정했을 때의 상대적인 비중이 등가이지만, 실제에서는 암 환자를 건강하다고 판정하는 것이 더 큰 문제이다. 

- Minimization process 에서는 이것을 방지하기 위해 **loss function** 혹은 **cost function** 이라 불리는 함수를 도입한다. 여기서는 어떤 오류가 있었을 때의 cost를 차등적으로 둔다. 만약 Maximize 를 통해 수행하고자 할 때 이러한 역할을 하는 함수는 **utility function** 이라 불린다.

- 실제 $C_k$ class로 분류되어야 할 input $\mathbf{x}$ 가 $C_j$ class로 분류되었을 때의 차등적인 cost를 나타내는 행렬 $L_{kj}$ 로 쓴다. 예를 들어, 암인 경우의 $C_1$, 암이 아닌 경우 $C_2$ 로 했을 때 $L_{kj}$ 를 
  $$
  \begin{bmatrix}
  0 & 1000 \\ 1 & 0
  \end{bmatrix}
  $$
  으로 표현 할 수 있다. 이것을 **loss matrix** 라 한다. $L_{12}$ 는 암인 환자를 암이 아닌 환자로 예측했을 때의 cost 이다. 

- $p(\text{mistake})$ 를 생각하면 $L_{kj}$ 의 대각성분은 $0$ 이어야 할 것이다. 그렇다면 loss function은 다음과 같다.
  $$
  \begin{align}
  \mathbb{E}[L]&=\sum_k \sum_j \int_{R_j} L_{kj} p(\mathbf{x},\,C_k)\,d\mathbf{x} \tag{1.80} \\
  &=\sum_k \sum_j \int_{R_j}L_{kj}\, p(C_k|\mathbf{x})\, p(\mathbf{x})\, d\mathbf{x} \tag{1.81}
  \end{align}
  $$
  이 때 우리의 목표는 $\mathbb{E}[L]$ 을 최소로 하는 decision region $\{R_j\}$ 를 찾는 것이다. 



#### 1.5.3 The Rejection Option

- 어떤 특정한 영역에서 모든 $p(C_k|\mathbf{x}) \ll 1$ 인, 혹은 (이와 동등한 표현이다) 가장 큰  $p(C_k|\mathbf{x})$  값이 서로 comparable 할 경우 문제가 된다. 이 경우 결정을 피할 수 있는데 이를 **reject option** 이라 한다. 
- 이것을 구현하는 방법 중의 하나는 확률에 대한 threshold $\theta$ 를 부여하여  $\max\{p(C_k|\mathbf{x}): k=1\ldots,\}\le\theta$ 일 때 reject option을 발동시키는 것이다.  $\theta=1$ 이면 모든 경우에서 reject option 이 발동된다. .  $\theta<1/K$ 이면 어떤 경우에서도 reject option은 발동되지 않는다. 



#### 1.5.4 Inference and Decision

- 지금까지는 classification problem 을 두단계로 나누었다. *Inference* 단계에서는 훈련 데이터를 이용하여 $p(C_k|\mathbf{x})$ model 을 학습하였고, *decision* 단계에서는 이 posterior probabilities 를 이용하여 optimal class assignment를 수행하였다. 
- Inference와 decision을 한 단계에 모두 수행하는 함수를 **discriminant function** 이라 한다.
- 실제로 다음에 소개할 3가지 접근법이 모두  dicision problem을 푸는데 실제적으로 사용된다. 



##### 3 approaches for decision problems (in decreasing order of complexity)

<b>(a) 1-st Approach : Generative model</b> 

- 우선 각각의 class $C_k$ 에 대해 class-conditional density $p(\mathbf{x}|C_k)$ 를 구한다. 또한 별도로 prior class probabilities $p(C_k)$ 를 추정한다. 이를 바탕으로 아래와 같은 Bayes' theorem 을 사용하여 posterior class probabilities $p(C_k|\mathbf{x})$ 를 계산한다. 

$$
p(C_k|\mathbf{x} )=\dfrac{p(\mathbf{x}|C_k)\,p(C_k)}{p(\mathbf{x})} \tag{1.82}
$$

- 보통은 위 식의 분모  $p(\mathbf{x})$ 는 
$$
p(\mathbf{x})=\sum_k p(\mathbf{x}|C_k)\,p(C_k)=\sum_k p(\mathbf{x},\,C_k)\tag{1.83}
$$
 	를 이용하여 계산 할 수 있다. 
- 이제 posterior probability $p(C_k|\mathbf{x})$ 를 구했다면 새로운 input $\mathbf{x}$ 에 대해 decision theory를 사용하여 classification 을 수행한다. 
- 이렇게 명시적으로든 묵시적으로든 input과 output의 분포를 modeling 하는 것을 **generative models** 라 한다. 이 이름이 붙은 이유는 이 분포를 sampling 하여 input space에서의 synthetic data 생성 할 수 있기 때문이다.
- $p(\mathbf{x}|C_k),\, p(C_k) \longrightarrow p(C_k|\mathbf{x}),\, p(\mathbf{x})\longrightarrow [\text{decision}]$ 



<b>(b) 2-nd Approach : Discriminative model</b>

- 우선 posterior probabilities $p(C_k|\mathbf{x})$ 을 구한다.(inference problem) 이후 decision theory 를 이용하여 새로운 $\mathbf{x}$ 를 classification 할 수 있도록 한다. 이렇게 직접적으로 posterior probabilities 를 모델링 하는 접근법을 **discriminative models** 라 한다.
- $p(C_k|\mathbf{x})\longrightarrow [\text{decision}]$ 



<b>(c) 3-rd Approach : Discriminant function</b>

- 각각의 input $\mathbf{x}$를 직접적으로 classification 하는 discriminant function $f$ 를 구한다. 2 class problem의 경우 $ f(\mathbf{x})$ 는 $0$ for $\mathcal{C}_1$ or $1$ for $\mathcal{C}_2$ 이다.  이 경우 확률은 아무런 역할을 하지 않는다. 



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

