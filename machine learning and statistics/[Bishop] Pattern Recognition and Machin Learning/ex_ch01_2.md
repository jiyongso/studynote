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



<b>1.24 </b> Classifiction problem 을 생각하자. 여기서 loss 는 $C_k$ 로 부터 온 input pector 가 class $\mathcal{C}_j$ 로 분류되었을 때 $L_{kj}$ 값을 갖도록 정해졌으며,  rejecti option