Exerciese in Chapter 1.
==



<b>1.1 </b> 식 (1.2) 의 sum-of-square error function 을 생각하자ㅣ $y(x,\,\mathbf{w})$ 는 식 (1.1) 의 다항식으로 주어졌다. Error function을 minimize 하는 coefficient $\mathbf{w} =\{w_i\}$ 는 다음 방정식의 해로부터 얻어질 수 있음을 보여라.
$$
\sum_{j=0}^M A_{ij}w_j = T_i\quad \text{where } A_{ij}=\sum_{n=1}^N (x_n)^{i+j},\quad T_i = \sum_{n=1}^N (x_n)^i t_n\;.
$$

---

$$
\begin{align}
y(x,\,\mathbf{w})&= \sum_{j=0}^M w_j x^j\\
E &=\dfrac{1}{2} \sum_{n=1}^N \left\{  y(x_n,\, \mathbf{w})-t_n\right\}^2\;. \\
&= \dfrac{1}{2}\sum_{n=1}^N \left[\sum_{j=0}^M w_j x_n^j-t_n\right]^2

\end{align}
$$

이므로,
$$
\begin{align}
&\dfrac{\partial E}{\partial w_i}=\sum_{n=1}^N x_n^i \left( \sum_{j=0}^M w_j x_n^j -t_n\right)=0  \\
\implies & \sum_{j=0} ^M (x_n) ^{i+j}w_j=\sum_{n=0}^N x_{n}^i t_n
\end{align}
$$


<b>1.2 </b> 





<b>1.3 </b> 3개의 색칠한 상자 $r$ (red), $b$ (blue), $g$ (green) 이 있다고 하자. 각 상자에 포함된 과일들의 갯수는 다음과 같다.

|      | 사과 | 오렌지 | 라임 |
| ---- | ---- | ------ | ---- |
| $r$  | 3    | 4      | 3    |
| $b$  | 1    | 1      | 0    |
| $g$  | 3    | 3      | 5    |

각 상자를 선택할 확률이 $p(r)=0.2,\, p(b)=0.2,\, p(g)=0.6$ 이라 하자. 과일 하나가 box로부터 제거되었을 대 사과가 선택될 확률은 얼마인가? 만약 선택된 과일이 오렌지였을 때, 이것이 green box로부터 나왔을 확률은 얼마인가?

---

(1)

$$
\begin{align}
p(apple)&= p(r)\times p(apple\mid r)+p(b) \times p(apple\mid b) + p(g) \times p(apple\mid g) \\
&=0.2\times \dfrac{3}{10}+0.2 \times \dfrac{1}{2} + 0.6 \times \dfrac{3}{11}=0.3236
\end{align}
$$

(2)
$$
\begin{align}
p(orange) &= 0.2 \times \dfrac{4}{10}+0.2 \times \dfrac{1}{2} + 0.6 \times \dfrac{3}{11}= 0.3436\,,\\
p(g,\, orange)&=0.6 \times \dfrac{3}{11}=0.1636\,,\\
p(g\mid orange) &= \dfrac{p(g,\, orange)}{p(orange)}=0.4762\,.
\end{align}
$$


<b>1.4 </b> 확률밀도 $p_x(x)$ 가 연속 변수 $x$ 에 대해 정의되어 있으며 이 변수를 식 (1.27) 에 따라 $x=g(y)$ 를 이용하여 변화시켰다. $x$ 에서의 maximum density를 갖는 $\hat{x}$ 와 $y$ 에서의 $\hat{y}$ 를 생각하자. 식 (1.27) 을 미분하여 $\hat{x}$ 와 $\hat{y}$ 는 $\hat{x}=g(\hat{y})$ 의 간단한 관계가 성립하지 않음을 보여라. 또한 linear transformatin 인 경우는 $\hat{x}=g(\hat{y})$ 가 성립함을 보여라.

---

(1) 식 (1.27) 은 다음과 같다.
$$
p_y(y)=p_x(x)\left|\dfrac{dx}{dy}\right|=p_x(g(y))|g'(y)| \tag{1}
$$
따라서,
$$
\dfrac{dp_y}{dy}= \left(\dfrac{dp_x}{dx}\right)_{g({y})} g'(y) |g'(y)| + p_x(g(y)) \dfrac{d }{dy}(|g'(y)|) \tag{2}
$$
(2) Linear transformation $x=ay+b$ 인 경우 $g'(y)=a=\text{const.}$ 이므로 식 (2) 를 보면 자명하다.



<b>1.5 </b> 식 (1.38) 의 정의를 이용하여 $\operatorname{var}[f]$ 가 식 (1.39) 를 만족함을 보이시오.

---

식 (1.38), (1.39) 는 다음과 같다.
$$
\begin{align}
\operatorname{var}[f]&=\mathbb{E}[(f(x)-\mathbb{E}[f(x)])^2] & (1.38)\\
\operatorname{var}[f]&=\mathbb{E}[f(x)^2]-\mathbb{E}[f(x)]^2 &(1.39)
\end{align}
$$
$\mathbb{E}[f(x)]$ 는 scalar value 이므로 $\mu$ 로 놓자.
$$
\begin{align}
\operatorname{var}[f] &= \mathbb{E}[(f(x)-\mu)^2] \\
&=\mathbb{E}[f(x)^2-2\mu f(x)+\mu^2]\\
&=\mathbb{E}[f(x)^2]-2\mu \mathbb{E}[f(x)]+\mu^2\\
&= \mathbb{E}[f(x)^2]-\mu^2 = \mathbb{E}[f(x)^2]-\mathbb{E}[f(x)]^2\;/.
\end{align} 
$$


<b>1.6 </b> $x,\,y$ 가 서로 독립적인 변수라면 covariance가 $0$ 임을 보이시오.

---
두 변수 $x,\,y$ 에 대한 covariance $\operatorname{cov}[x,\,y]$ 는 다음과 같이 정의된다.
$$
\operatorname{cov}[x,\,y]=\mathbb{E}_{x,\,y}[xy]-\mathbb{E}[x]\mathbb{E}[y]
$$

두 변수가 독립이면 $p(x,\,y)=p_x(x) p_y(y)$ 이므로,
$$
\begin{align}
\mathbb{E}_{x,\,y}[xy]&=\sum_{x} \sum_y (xy)p(x,\,y)=\left(\sum_x x\, p_x(x)\right)\left(\sum_y y\, p_y(y)\right) = \mathbb{E}[x]\mathbb{E}[y]
\end{align}
$$
이다.



<b>1.8 </b> change of variables 를 이용하여 식 (1.46) 에 의해 정의된 $\mathcal{N}(x\mid \mu,\,\sigma^2)$ 가 식 (1.49) 를 만족함을 보이시오. 또한 normalization condition
$$
\int_{-\infty}^\infty \mathcal{N}(x\mid \mu,\,\sigma^2)\,dx=1
$$
의 양변을 $\sigma^2$ 에 대해 미분하여 가우시안이 식 (1.50) 을 만족함을 보이시오. 마지막으로 식 (1.51) 이 성립함을 보이시오.

---

$$
\begin{align}
\mathcal{N} (x\mid \mu,\,\sigma^2) &=\dfrac{1}{\sigma \sqrt{2\pi}}\exp \left[-\dfrac{(x-\mu)^2}{2\sigma^2}\right] & (1.46) \\
\mathbb{E}[x] &= \int_{-\infty}^\infty \mathcal{N}(x\mid \mu,\, \sigma^2)x\,dx=\mu & (1.49)\\
\mathbb{E}[x^2] &= \int_{-\infty}^\infty \mathcal{N}(x\mid \mu,\,\sigma^2)\,x^2\,dx =\mu^2+\sigma^2 & (1.50)\\
\operatorname{var}[x]&= \mathbb{E}[x^2]-\mathbb{E}[x]^2=\sigma^2 & (1.51)
\end{align}
$$

(1) 식 1.46 에서 $t=x-\mu$ 로 변환하여 적분하면 된다.

(2) 주어진 식의 양 변을 $\sigma^2$ 에 대해 미분하면, 
$$
\begin{align}
0&=\dfrac{d}{d\sigma^2}\int_{-\infty}^\infty \dfrac{1}{\sqrt{2\pi \sigma^2}} \exp \left[-\dfrac{(x-\mu)^2}{2\sigma^2}\right] dx\\
&=\int_{-\infty}^\infty \dfrac{\partial }{\partial \sigma^2} \left(\dfrac{1}{\sqrt{2\pi \sigma^2}} \exp \left[-\dfrac{(x-\mu)^2}{2\sigma^2}\right]\right) dx \\
&=-\dfrac{1}{2\sigma^2}\int_{-\infty}^\infty \dfrac{1}{\sqrt{2\pi \sigma^2}}  \exp \left[-\dfrac{(x-\mu)^2}{2\sigma^2}\right] dx + \int_{-\infty}^\infty  \left( \dfrac{(x-\mu)^2}{2\sigma^4}\right)  \dfrac{1}{\sqrt{2\pi \sigma^2}}  \exp \left[-\dfrac{(x-\mu)^2}{2\sigma^2}\right] dx \\
&= -\dfrac{1}{2\sigma^2} + \dfrac{1}{2\sigma^4} \left(\mathbb{E}[x^2]-\mu^2\right)
\end{align}
$$
따라서, $\mathbb{E}[x^2] = \sigma^2+\mu^2$ .

(3) $\mu=\mathbb{E}[x]$ 이므로 $\sigma^2 = \mathbb{E}[x^2]-\mathbb{E}[x]^2$. 



<b>1.12</b> (1.49) 와 (1.50)의 결과를 이용하여 다음을 보이시오.
$$
\mathbb{E}[x_nx_m]=\mu^2+I_{nm}\sigma^2\;.
$$
여기서 $x_n,\,x_m$ 은 평균 $\mu$, 분산 $\sigma^2$ 의 가우시안 분포로부터 샘플링 된 데이터포인트이며 $I_{nm}=\delta_{nm}$  이다. 이로부터 식 (1.57)과 (1.58) 을 증명하라.

---

식 (1.58) 을 제외하면 trivial 하다.
$$
\begin{align}
\sigma_{ML}^2 &= \dfrac{1}{N}\sum_{n=1}^N (x_n-\mu_{ML})^2 =\dfrac{1}{N}\sum_{n=1}^N \left(x_n-\dfrac{1}{N}\sum_{m=1}^N x_m\right)^2 \\
&=\dfrac{1}{N} \sum_{n=1}^N \left[ \dfrac{N-1}{N}x_n - \dfrac{1}{N} \sum_{m\ne n}^N x_{m} \right]^2 \\
&=\dfrac{(N-1)^2}{N^3}\sum_{n=1}^N {x_n}^2 -2\dfrac{N-1}{N^3} \sum_{n=1}^N x_n \left(\sum_{m\ne n}^N x_m\right) +\dfrac{1}{N^3} \sum_{n=1}^N\left(\sum_{m\ne n} x_m\right)^2 \\
&=\dfrac{(N-1)^2}{N^3} \sum_{n=1}^N {x_n}^2 -\dfrac{2(N-1)}{N^3} \sum_{n\ne m=1}^N x_nx_m + \dfrac{N-1}{N^3} \sum_{n=1}^N {x_n}^2 + \dfrac{(N-2)}{N^3} \sum_{n\ne m=1}^N x_m x_n \\
&=\dfrac{N-1}{N^2} \sum_{n=1}^N {x_n}^2-\dfrac{1}{N^2} \sum_{n\ne m=1}^N x_n x_m
\end{align}
$$

따라서, 
$$
\begin{align}
\mathbb{E}\left[\sigma_{ML}^2\right] &= \dfrac{N-1}{N^2}\mathbb{E}\left[\sum_{n=1}^N{x_n}^2\right]-\dfrac{1}{N^2} \mathbb{E} \left[\sum_{n\ne m = 1}^N  x_nx_m\right] \\
&=\dfrac{N-1}{N^2}\cdot N\left( \mu^2+\sigma^2 \right) - \dfrac{1}{N^2} N(N-1) \mu^2 \\
&= \dfrac{N-1}{N} \sigma^2

\end{align}
$$



<b>1.13</b> 

Let $\displaystyle \widetilde{\sigma\,}_{ML}^2 = \dfrac{1}{N} \sum_{n=1}^N \left(x_n-\mu\right)^2$. 
$$
\begin{align}
\mathbb{E}[\widetilde{\sigma\,}_{ML}^2] &= \dfrac{1}{N} \sum_{n=1}^N \mathbb{E}[(x_n-\mu)^2] =\dfrac{1}{N} \sum_{n=1}^N\left(\mathbb{E}[x^2]-2\mu \mathbb{E}[x]+\mu^2  \right)\\
&=\dfrac{1}{N}(N(\mu^2+\sigma^2)-N\mu^2)=\sigma^2\;/.

\end{align}
$$


<b>1.14 </b> 

(1) Let $w_{ij}^S = \dfrac{1}{2}(w_{ij}+w_{ji})$ and $w_{ij}^A = \dfrac{1}{2}(w_{ij}-w_{ji})$ . Then,
$$
\begin{align}
w_{ji}^S &= w_{ij}^S \quad\; &\text{symmetric}, \\
w_{ji}^A &= -w_{ij}^S \quad & \text{assymetric}\,,\\
w_{ij}^S+w_{ij}^A&= w_{ij}
\end{align}
$$
(2) 
$$
\begin{align}
\sum_{i=1}^\mathcal{D}\sum_{j=1}^\mathcal{D} w_{ij} x_i x_j &= \sum_{i=1}^\mathcal{D} \sum_{j=1}^\mathcal{D} w_{ji}x_j x_i \\
\text{Therefore,}\\
\sum_{i}\sum_j w_{ij}x_i x_j  &= \dfrac{1}{2} \sum_{i}\sum_j (w_{ij}x_ix_j + w_{ji}x_ix_j)=\sum_{i}\sum_j \dfrac{1}{2}(w_{ij}+w_{ji})x_ix_j\\&=\sum_i \sum_j w_{ij}^S x_ix_j \;.
\end{align}
$$
(3) $w_{ij}$ 의 elements의 갯수는 $D^2$. 여기서 diagonal 성분을 제외한 $D^2-D$ 개의 elements 의 절반이  independent 하므로  $D+ (D^2-D)/2=\dfrac{D(D+1)}{2}$ 개의 독립적인 parameter가 존재한다.



<b>1.15  </b> 이 문제와 다음 문제에서는 다항식의 독립변수가 다항식의 오더 $M$ 과 input space의 dimensionality $D$ 에 따라 어떠게 증가하는지를 본다. 우리는 $D$ 차원에서의 다항식에 대한 $M$-th order term 을 다음과 같이 쓰자.
$$
\sum_{i_1=1}^D \sum_{i_2=1}^{D} \cdots \sum_{i_M=1}^{D} {w}_{i_1 i_2 \cdots i_M} x_{i_1}x_{i_2}\cdots x_{i_M}
$$
The coefficient $w_{i_1 \cdots i_M}$ 은 $D^M$ 개가 가능하나 실제 독립적인 갯수는 $x_{i_1},\, \ldots,\, x_{i_M}$ 사이의 interchange symmetry를 고려하면 훨씬 적다. 이를 고려하du $M$-th order term을 다시 쓰면,
$$
\sum_{i_1=1}^D \sum_{i_2=1}^{i_1}\cdots \sum_{i_M=1}^{i_{M-1}}\widetilde{w}_{i_1 i_2 \cdots i_M} x_{i_1}\cdots x_{i_M}
$$
으로 쓸 수 있다. 여기서 $w_{i_1\cdots i_M}$ 과 $\widetilde{w}_{i_1 \cdots i_M}$ 의 관계를 명확하게 할 필요는 없다. 이 결과를 이용하여 the number of independent parameters $n(D,\,M)$, which appears at order $M$, 은 다음의 재귀관계를 만족함을 보이라.
$$
n(D,\,M)=\sum_{i=1}^D n(i,\,M-1) \tag{1.135}
$$
다음으로 induction을 이용하여 다음 관계가 성립함을 보이라.
$$
\sum_{i=1}^D \dfrac{(i+M-2)!}{(i-1)!(M-1)!}= \dfrac{(D+M-1)!}{(D-1)!M!} \tag{1.136}
$$
마지막으로 앞의 두 결과를 이용하고, 역시 induction을 사용하여,
$$
n(D,\,M)=\dfrac{(D+M-1)!}{(D-1)!M!} \tag{1.137}
$$
임을 보이라.

---

(1) $(1.135)$ 를 보인다. $x_1,\ldots,\,x_D$ 까지의 변수가 이루는 $M$ 차식에서의 독립적인 계수의 갯수가 갖는 관계이다. 독립적인 변수의 갯수는
$$
n(D,\,M)=\sum_{i_1=1}^D \sum_{i_2=1}^{i_1}\cdots \sum_{i_M=1}^{i_{M-1}}1 = \sum_{i_1=1}^D \left( \sum_{i_2=1}^{i_1}\cdots \sum_{i_M=1}^{i_{M-1}}1 \right)=\sum_{i=1}^D n(i,\,M-1)
$$


(2) $(1.136)$ 을 보이자. 임의의 정수 $M$ 에 대해 $D=1$ 일 때 
$$
\begin{align}
\sum_{i=1}^1 \dfrac{(i+M-2)!}{(i-1)!(M-1)!} &=\dfrac{(1+M-2)!}{(1-1)! (M-1)!}=1\,\\
\dfrac{(D+M-1)!}{(D-1)!M!} &= 1
\end{align}
$$
이므로 성립한다. 

$D$ 에 대해 성립함을 가정한다.
$$
\begin{align}
\sum_{i=1}^{D+1}\dfrac{(i+M-2)!}{(i-1)!(M-1)!} &= \sum_{i=1}^D \dfrac{(i+M-2)!}{(i-1)!(M-1)!} + \dfrac{(D+M-1)!}{D!(M-1)!} \\
&= \dfrac{(D+M-1)!}{(D-1)!M!}  + \dfrac{(D+M-1)!}{D!(M-1)!} \\
&= \dfrac{(D+M)!}{D!M!}=\dfrac{((D+1)+M-1 )!}{((D+1)-1)! M!}

\end{align}
$$
따라서 $(1.136)$ 이 성립한다.



(3)  임의의 $D \ge 1$ 에 대해 $M=2$ 일 때, 즉 2차식에 대해 독립적인 계수의 갯수는 $D+\dfrac{D(D-1)}{2}=\dfrac{D(D+1)}{2}$ 임이 자명하다. 식 (1.137) 에서 $n(D,\,2)=\dfrac{D(D+1)}{2}$ 이다. 이제 $M-1$ 차항의 계수가 식 (1.137)에서 주어짐을 가정하자.  $M$ 차항의 독립적인 변수의 개수는 식 (1.135)에 의해
$$
\begin{align}
n(D,\,M)&=\sum_{i=1}^D n(i,\,M-1) = \sum_{i=1}^D \dfrac{(i+M-2)!}{(i-1)! (M-1)!}=\dfrac{(D+M-1)!}{(D-1)!M!}

\end{align}
$$
이므로 성립한다.



<b>1.16</b> 문제 1.15 에서 우리는 $D$-차 다항식의 $M$-th order term의 독립적인 parameter의 갯수에 대해 식 (1.135)를 얻었다. 이제 우리는 $1$-st order 부터 $M$-th order 까지의 모든 독립적인 parameters의 갯수 $N(D,\,M)$ 을 얻고자 한다. 즉,
$$
N(D,\,M)=\sum_{m=0}^M n(D,\,m) \tag{1.138}
$$
을 얻고자 한다. 식 (1.137) 에서의 결과를 이용하고, induction을 사용하여
$$
N(D,\,M)=\dfrac{(D+M)!}{D!M!} \tag{1.139}
$$
를 구하라.마지막으로 Stirling's approximation
$$
n! \approx n^n e^{-n}
$$
for large $n$ 을 이용하여 $D\gg M$ 일 경우 $N(D,\,M)$ 은 $D^M$ 처럼 증가하며, $M \gg D$ 의 경우 $N(D,\,M)$ 은 $M^D$ 처럼 증가함을 보이라.

Cubic polynomial($M=3$) in $D$ dimensions 에서 (i)$D=10$ 일 때와 (ii) $D=100$ 일 때의 total number of independent parameters 를 구하라.

---

(1) 식 (1.138) 을 임의의 $M$ 에 대해 induction을 통해 구하자. $D=1$ 일 때 $N(D=1,\,M)=M+1$ 이며, $\displaystyle \sum_{m=0}^M n(1,\,m)=\sum_{m=0}^m1=m+1$ 이므로 성립한다.  $M$ 에 대해 성립함을 가정하면,
$$
\begin{align}
N(D,\,M+1) &=\sum_{m=0}^{M+1}n(D,\,m)=\sum_{m=0}^M n(D,\,m)+n(D,\,M+1)\\
&= \dfrac{(D+M)!}{D!M!}+ \dfrac{(D+M)!}{(D-1)!(M+1)!}=\dfrac{(D+M)!}{D!(M+1)!} (M+1+D)\\
&=\dfrac{(D+(M+1))!}{D!(M+1)!}

\end{align}
$$
 (2) $D \gg M$ 의 경우,
$$
N(D,\,M) \approx \dfrac{(D+M)^{D+M}e^{-(D+M)}}{D^D M! e^{-D}} \approx \dfrac{(D+M)^{D+M}}{D^DM!}e^{-M}\approx \dfrac{(D+M)^D (D+M)^M}{D^DM!}e^{-M}
$$
여기서 $D\gg M \implies D+M \approx D$ 이므로 
$$
D\gg M \implies N(D,\, M) \approx \dfrac{D^M}{M!}e^{-M}
$$
$M\gg D$ 의 경우는 식 (1.139) 의 대칭성에 의해 $M\\gg D \implies N(D,\,M)\approx \dfrac{M^D}{D!}e^{-D}$ 



<b>1.17 </b> 감마 함수는 다음과 같이 정의된다.
$$
\Gamma(x)\equiv \int_0^\infty u^{x-1}e^{-u}du\,.\tag{1.141}
$$
부분적분을 이용하여 $\Gamma(x+1)=x\Gamma(x)$ 임을 보이라. 또한 $\Gamma(1)=1$ 이며, 따라서 $x$ 가 정수일 경우 $\Gamma(x+1)=x!$ 임을 보이라.

---

$$
\begin{align}
\Gamma(x+1) &=\int_0^\infty u^{x}e^{-u}du =-\left[u^xe^{-u}\right]_{u=0}^{u \to \infty} + \int_0^\infty xu^{x-1}e^{-u}\, du = x\Gamma(x)

\end{align}
$$

$$
\Gamma(1) = \int_0^\infty e^{-u}\, du = \left[-e^{-u}\right]_0^\infty=1
$$



<b>1.18</b> 식 (1.126) 을 이용하여 $D$ 차원에서의 unit radius를 갖는 구의 표면적 $S_D$ 와 부피 $V_D$ 를 구할 수 있다. 이를 위해 Cartesian to polar coordinates 로의 변환에 의해 얻어지는 다음 결과
$$
\prod_{i=1}^D \int_{-\infty}^\infty e^{-{x_i}^2} dx_i = S_D \int_0^\infty e^{-r^2} r^{D-1}\, dr \tag{1.142}
$$
를 이용한다. 식 (1.141) 과 식 (1.126)의 결과를 이용하여 양쪽의 결과를 계산하여
$$
S_D = \dfrac{2\pi^{D/2}}{\Gamma(D/2)} \tag{1.143}
$$
다음으로 $0$ 에서 $1$ 까지 $r$ 에 대해 적분하여 
$$
 V_D =\dfrac{S_D}{D}
$$
임을 구하라. 마지막으로 $\Gamma (1)=1$ 과 $\Gamma\left(\dfrac{3}{2}\right)=\dfrac{\sqrt{\pi}}{2}$ 를 이용하여 식 (1.142) 와 식 (1.143) 이 $D=2$ 와 $D=3$ 에서의 우리가 아는 표현과 일치함을 보여라.

---

From (1.126), $\displaystyle \int_0^\infty e^{-x^2}\, dx= \sqrt{\pi}$ 이므로, $(\pi )^{D/2}=S_D \displaystyle \int_0^\infty e^{-r^2}r^{D-1} \, dr$ 이다. 이 때,
$$
\int_0^\infty e^{-r^2}r^{D-1}\, dr = (r^2=u \text{ substitution})=\dfrac{1}{2}\int_{0}^\infty e^{-u} u^{D/2-1}  du =\dfrac{1}{2}\Gamma(D/2)
$$
이므로,
$$
S_D = \dfrac{2 \pi^{D/2}}{\Gamma(D/2)}
$$
이다.  

식 (1.142)로 부터, 
$$
V_D=S_D\int_0^1 r^{D-1}dr=\dfrac{S_D}{D}
$$
$D=2$ 일 때 $S_2=2\pi $, $V_2=\pi$ 임을 안다. $D=3$ 일 때 $S_3=4\pi,\, V_D =\dfrac{3}{4}\pi$ 임을 안다. 위의 식을 만족한다.



<b>19. </b> $D$-차원에서 반경 $a$ 인 구와 한 변의 길이가 $2a$ 인 concentric hypercube 를 생각하자. 이 때 구는 hybercube 의 안에 포함되며 각 면에 그 면의 중심에서 접한다. 문제 1.18 의 결과를 이용하여 hybercube의 부피에 대한 구의 부피비가 다음과 같음을 보이라.
$$
\dfrac{\text{volume of sphere}}{\text{volume of cube}}= \dfrac{\pi^{D/2}}{D2^{D-1}\Gamma(D/2)} \tag{1.145}
$$
Stirling's formula 의 아래와 같은 형식은 $x \gg1$ 에서 유효하다.
$$
\Gamma (x+1)\approx (2\pi)^{1/2} e^x x^{x+1/2} \tag{1.146}
$$
이를 이용하여 $D\to \infty$ 극한에서 (1.145)의 비율이 $0$ 이 됨을 보이라.

또한  [hypercube의 한 꼭지점에서 중심까지의 거리] $ \div$ [중심에서 한 면까지의 거리]  는 $D\to \infty$ 극한에서 $\infty$ 임을 보여라. 이 결과로부터 고차원의  hypbercube 는 그 부피의 대부분이 많은 코너에 몰려있으며, 아주 큰 'spikes' 가 됨을 알 수 있다.

---

hybercube의 volume = $(2a)^D$ 이며, volume of sphere 는 문제 1.18로부터 (unit volume $\times a^D$ 하여, ) $2a^D\pi^{D/2}/\Gamma(D/2)$ 임을 안다. 따라서,
$$
\dfrac{\text{volume of sphere}}{\text{volume of cube}}= \dfrac{2\pi^{D/2 }a^D}{\Gamma(D/2) (2a)^D}=\dfrac{\pi^{D/2}}{2^{D-1}\Gamma(D/2)}
$$
Stirling's formula 를 이용하면, 또한 $D \gg 1$ 일 때 $D-1 \approx D,\, D/2-1 \approx D/2$ 임을 이용하면
$$
\dfrac{\text{volume of sphere}}{\text{volume of cube}} \approx \dfrac{\pi^{D/2}}{2^{D-1} (2\pi)^{1/2} e^{D/2-1} (D/2-1)^{(D-1)/2}} \approx \dfrac{1}{2\sqrt{2\pi}} \left(\dfrac{2\pi}{eD}\right)^{D/2}
$$
이다. 우리는 $\displaystyle \lim_{x \to \infty} \left(\dfrac{a}{x}\right)^{x/2}=0$ for any $a>0$ 임을 안다. 따라서 위 식으 $D\to \infty$ 극한은 $0$ 이다.

하이퍼큐브의 한 꼭지점 $\displaystyle \sum_{i=1}^D a\mathbf{e}_i$ 에서 중심까지의 거리는 $\sqrt{D}a$ 이며 하이퍼 큐브의 한 변에서 중심까지의 거리는 $a$ 이다. 따라서 그 $D\to \infty$ 극한은 $\infty$ 이다. 



<b>20. </b> 이 연습문제에서는 고차원 공간에서의 가우시안 분포에 대해 알아본다. $D$ 차원에서의 가우시안 분포는 다음과 같이 주어진다.
$$
p(\mathbf{x}) = \dfrac{1}{(2\pi \sigma^2)^{D/2}} \exp \left(-\dfrac{\|\mathbf{x}\|^2}{2\sigma^2}\right) \tag{1.147}
$$
우리는 극좌표계에서의 radius에 대한 확률밀도함수를 구하고자 한다.  Radius가 $r$ 이고 두께가 $\epsilon \ll 1$ 인 영역에서의 확률밀도함수의 적분은 $p(r)\epsilon$ 이며 $p(r)$ 은 다음과 같이 주어짐을 보여라.
$$
p(r)  = \dfrac{S_Dr^{D-1}}{(2\pi \sigma^2)^{D/2}} \exp \left(-\dfrac{r^2}{2\sigma^2}\right)
$$
여기서 $S_D$ 는 $D$-차원에서의 단의 구의 표면적이다. 함수 $p(r)$ 은 하나의 stationalry point를 가지며, 그 위치는 $D$ 가 클 때 $\widehat{\,r\,}\approx \sqrt{D}\sigma$ 임을 보여라. $\epsilon \ll \widehat{\,r\,}$ 이고 $D$ 가 클 때,
$$
p(\widehat{\,r\,}+\epsilon)=p(\widehat{\,r\,})\exp\left(-\dfrac{3\epsilon^2}{2\sigma^2}\right)
$$
임을 보여라. 이는 $\widehat{\,r\,}$ 이 radial probability density의 극값이며 $p(r)$ 은 $\widehat{\,r\,}$ 에서 멀어질 때 lengthscale $\sigma$ 로 지수함수적으로 감소함을 보여준다. 우리는 이미 큰 $D$ dptj $\sigma \ll \widehat{\,r\,}$ 임을 보았으며, 또한 대부분의 확률질량의 대부분은 큰 반경의 얇은 shell에 집중되어 있음을 알 수 있다. 마지막으로 확률밀도 $p(\mathbf{x})$ 는 반경 $\widehat{\,r\,}$ 에서보다 원점에서 factor $\exp (D/2)$ 맡큼 큼을 보여라. 우리는 이에 고차원 가우시안 분포에서의 대부분의 확률질량은 높은 확률밀도를 갖는 영역과는 다른 영역에 집중되어 있음을 알 수 있다. 고차원에서의 분포의 이러한 특성은 우리가 나중에 모델 파라메터에 관한 베이지안 추론을 다룰 때 중요한 결과들을 준다.

---

식 (1.142) 에서 의 결과를 이용한다. 
$$
\begin{align}
\int_{-\infty}^\infty\cdots\int_{-\infty}^\infty p(\mathbf{x}) \, dx_1\cdots dx_D &=\prod_{i=1}^D \int_{-\infty}^\infty \dfrac{1}{(2\pi \sigma^2)^{1/2}} \exp \left(-\dfrac{x_i^2}{2\sigma^2}\right)\, dx_i \\
&= \dfrac{1}{(2\pi \sigma^2)^{D/2}} \prod _{i=1}^D \int_{-\infty}^\infty \exp \left(-\dfrac{x_i^2} {2\sigma^2}\right)\, dx_i \\
&= \dfrac{S_D}{(2\pi\sigma^2)^{D/2}} \int_0^\infty \exp \left(-\dfrac{r^2}{2\sigma^2}\right) r^{D-1}\, dr


\end{align}
$$
이므로 radial probability density $p(r)$ 은 
$$
p(r) = \dfrac{S_D r^{D-1}}{(2\pi \sigma^2)^{D/2}} \exp \left(-\dfrac{r^2}{2\sigma^2}\right)
$$
이다. 
$$
\dfrac{d p(r)}{dr} = \dfrac{S_D}{(2\pi \sigma^2)^{D/2}} \exp \left(-\dfrac{r^2}{2\sigma^2}\right) \left( (D-1)r^{D-2}-\dfrac{r^D}{\sigma^2}\right)
$$
이므로 $\dfrac{dp(r)}{dr}=0 \implies \widehat{\,r\,}^2 = (D-1)\sigma^2 $ 이다.  $D \gg 1$ 일 때 $\widehat{\,r\,}\approx \sqrt{D}\sigma$ 이다. 

$\epsilon \ll \widehat{\,r\,}$ 이고 $D\gg 1$ 일 때, $D \approx \dfrac{\widehat{\,r\,}^2}{\sigma^2}$ 이고 $D-1 \approx D$ 이므로,
$$
\begin{align}

\end{align}
$$
