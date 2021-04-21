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
&=\dfrac{(N-1)^2}{N^3} \sum_{n=1}^N {x_n}^2 -\dfrac{4(N-1)}{N^3} \sum_{n\ne m=1}^N x_nx_m + \dfrac{N-1}{N^3} \sum_{n=1}^N {x_n}^2 + \dfrac{2(N-2)}{N^3} \sum_{n\ne m=1}^N x_m x_n \\
&=\dfrac{N-1}{N^2} \sum_{n=1}^N {x_n}^2-\dfrac{2}{N^2} \sum_{n\ne m=1}^N x_n x_m
\\
\\

&= \dfrac{1}{N}\sum_{n=1}^N (x_n-\mu_{ML})^2 =\dfrac{1}{N} \sum_{n=1}^N (x_n-\mu +\mu-\mu_{ML})^2 \\
&= \dfrac{1}{N}\left[\sum_{n=1}^N (x_n-\mu)^2+2(x_n-\mu)(\mu-\mu_{ML})+ (\mu-\mu_{ML})^2  \right]

\end{align}
$$

$$
\begin{align}
\mathbb{E}\left[ \sigma^2_{ML} \right] &= \dfrac{1}{N} \sum_{m,\,n=1}^N \mathbb{E}[x_mx_n]-2\mu \dfrac{1}{N}\sum_{n=1}^N \mathbb{E}[x_n]-\mu^2 \\
&=\dfrac{1}{N} (N^2\mu^2+N\sigma^2)-\mu^2\\
&=(N-1)\mu^2+N\sigma^2

\end{align}
$$
