Exerciese in Chapter 1. #1
===



<b>1.22</b> A loss matrix with elements $L_{kj}$ 가 주여졌을 때, 각각의 $\mathbf{x}$ 에 대해 식 (1.81)을 minimize 하는 class 를 선택하면 expected risk 가 minimize 된다. Loss matrix가 $L_{kj}=1-I_{kj}$ 로 주어졌을 때, 이 문제는 largest posterior probability 문제로 환원됨을 보이라. 이러한 형태의 loss matrix의 해석은 무엇인가?

---

From (1.81), and $L_{kj}=1-I_{kj}$ , 
$$
\sum_{k}L_{kj}p(\mathcal{C}_k|\mathbf{x})=\sum_{k\ne j}p(\mathcal{C}_k|\mathbf{x})=1-p(\mathcal{C}_j|\mathbf{x})
$$
이므로 이것을 minimize 하는 것은 $p(C_j|\mathbf{x})$ 를 maximize 하는 것이다. 



<b>1.23 </b> A general loss matrix 와 classes 에 대한 general prior probabilities 가 주어졌을 때 expected loss 를 최소화 하는 기준을 유도하라.

---

Class $\{\mathcal{C}_1,\ldots,\,\mathcal{C}_N\}$ 에 대해 loss matrix $L_{kj}$ 와 prior probability $p(\mathcal{C}_j)$ 가  주여졌다. 
$$
\mathbb{E}[L]=\sum_{k}\sum_{j}\int_{R_j} L_{kj} p(\mathbf{x},\,\mathcal{C}_k)\, d\mathbf{x}=\sum_{k}\sum_{j} L_{kj} p(\mathcal{C}_k) \int_{R_j} p(\mathbf{x}|C_k)\, d\mathbf{x} 
$$
이다. Effective loss matrix(이렇게 이름 붙일 수 있다면...) $\widehat{L}_{kj}=L_{kj}p(\mathcal{C}_k)$ 로 정의하여,
$$
\mathbb{E}[\widehat{L}]=\sum_{k}\sum_{j} \widehat{L}_{kj}\int_{R_j} p(\mathbf{x}|\mathcal{C}_k)\, d\mathbf{x}
$$
가 최소화 되도록 한다. 



<b>1.24 </b> Classifiction problem 을 생각하자. 여기서 loss 는 $C_k$ 로 부터 온 input vector 가 class $\mathcal{C}_j$ 로 분류되었을 때 $L_{kj}$ 값을 갖도록 정해졌으며,  reject option을 선택했을 때 발생하는 loss는 $\lambda$ 이다. Minimum expected loss를 주는 결정 원칙을 발견하라. 이것은 loss matrix가   $L_{kj}=1-I_{kj}$ 로 주어졌을 때 section 1.5.3 에서 논의된 reject criterion 으로 환원됨을 보이라. $\lambda$ 와 rejection threshold $\theta$ 와의 관계는 무엇인가?

---

$C_j$ 는 $C_j$ 에 속하지 않은 input vector를 $C_j$ 에 속했다고 오판했을 때 위험한 특정하고 unique 한 class 라 하자. Input vector $\mathbf{x}$ 가 class $C_k$ 에 속할 확률은 $p(C_k|\mathbf{x})$ 이며 class $C_j$ 로 잘못 분류되었을 때의 expected loss는  $\sum_{k} L_{kj} p(C_k|\mathbf{x})=\lambda$ 이다.

-- to be done--

<b>1.25 </b> Single target variable $t$ 에 대한 Squared loss function (1.87) 을 multiple target variables $\mathbf{t}$ 에 대해 일반화 하면 다음과 같다.
$$
\mathbb{E}\left[L(\mathbf{t},\,\mathbf{y}(\mathbf{x}))\right] = \iint \left\| \mathbf{y}(\mathbf{x})-\mathbf{t} \right\|^2 p(\mathbf{x},\,\mathbf{t})d\mathbf{x}d\mathbf{t} \tag{1.151}
$$
변분법을 사용하여 expected loss를 최소화하는 함수$\mathbf{y}(\mathbf{x})$ 는 $\mathbf{y}(\mathbf{x})=\mathbb{E}_\mathbf{t} [\mathbf{t}\,|\, \mathbf{x}]$ 로 주어짐을 보이라. 이 결과는 single target variable $t$ 의 경우 시 (1.89) 가 됨을 보이라.

---

변분법에 의해 $\mathbf{y}(\mathbf{x})$ 의 미분에 의한 의존성이 없는 경우 기대값을 최소화 하는 함수는 
$$
\dfrac{\partial \mathbb{E}}{\partial \mathbf{y}(\mathbf{x})}=\int 2(\mathbf{y}(\mathbf{x})-\mathbf{t})\,p(\mathbf{x},\,\mathbf{t})\, d\mathbf{t}=0
$$
으로 주어진다. 따라서,
$$
\begin{align}
&\mathbf{y}(\mathbf{x}) \int p(\mathbf{x},\,\mathbf{t})\, d\mathbf{t} = \int\mathbf{t}\, p(\mathbf{x},\,\mathbf{t})\, d\mathbf{t} \\
\implies & \mathbf{y}(\mathbf{x})=\dfrac{\displaystyle \int\mathbf{t}\, p(\mathbf{x},\,\mathbf{t})\, d\mathbf{t}}{\displaystyle \int p(\mathbf{x},\,\mathbf{t})\, d\mathbf{t} } = \int \mathbf{t} p(\mathbf{x},\,\mathbf{t}) \dfrac{1}{p(\mathbf{x})}\, d\mathbf{t} = \int\mathbf{t} p(\mathbf{t}\,|\,\mathbf{x})\, d\mathbf{t} =\mathbb{E}_\mathbf{t} [\mathbf{t}\,|\,\mathbf{x}]
\end{align}
$$
이다. 

