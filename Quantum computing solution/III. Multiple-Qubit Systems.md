III. Multiple-Qubit Systems
===





## 1. Quantum State Spaces



#### Direct sum of vector space

$V,\,W$가 각각 $\mathcal{B}_V = \{ |\alpha_1\rangle,\,|\alpha_2\rangle,\ldots,\,|\alpha_n\rangle\}$ , $\mathcal{B}_W = \{ |\beta_1\rangle,\,|\beta_2\rangle,\ldots,\,|\beta_m\rangle\}$  을 basis로 갖는 벡터공간일 때, $\mathcal{B} = \mathcal{B}_V \cup \mathcal{B}_W$ 를 basis로 갖는 벡터 공간을 $V \oplus  W$  **direct sum** of $V$ and $W$ 라 한다. 

$\dim (V\oplus W) = \dim (V) + \dim (W)$ 이다. 

$|x\rangle \in V \oplus W$  이면 어떤 $|v \rangle \in V,\, |w\rangle \in W$ 에 대해 $| x\rangle = |v\rangle \oplus |w \rangle$ 이다.

---

(1) $V,\,W$ 가 각각 inner product space 일 때 $(\langle v_2 | \oplus \langle w_2 |)(| v_1 \rangle \oplus |w_1 \rangle) = \langle v_2 | v_1 \rangle + \langle w_2 | w_1 \rangle$ 로 정의된다.



#### Tensor products of vectors

$V,\,W$ 가 vector space 이고 $|v\rangle,\,|v_1\rangle ,\,|v_2 \rangle \in V$ , $|w\rangle,\,|w_1\rangle,\,w_2\rangle \in W$  일 때 다음을 만족하는 binary operation $\otimes : V \times W \to \mathbb{F}$ 를 **tensor product** of vectors 라 한다.

(a) $(|v_1 \rangle + |v_2 \rangle)\otimes |w\rangle = |v_1 \rangle \otimes |w\rangle + |v_2 \rangle \otimes |w\rangle$.

(b) $|v \rangle \otimes (|w_1 \rangle + |w_2 \rangle) = |v\rangle \otimes |w_1 \rangle +  |v\rangle \otimes |w_2 \rangle $.

(c) $(a|v \rangle ) \otimes |w\rangle = |v \rangle \otimes (a |w\rangle) = a(|v\rangle \otimes |w\rangle)$. 



#### Tensor products of vector spaces

$V,\,W$가 각각 $\mathcal{B}_V = \{ |\alpha_1\rangle,\,|\alpha_2\rangle,\ldots,\,|\alpha_n\rangle\}$ , $\mathcal{B}_W = \{ |\beta_1\rangle,\,|\beta_2\rangle,\ldots,\,|\beta_m\rangle\}$  을 basis로 갖는 벡터공간일 때, $\mathcal{B} = \mathcal{B}_V \otimes \mathcal{B}_W =\{ |\alpha_i \rangle \otimes |\beta_j\rangle : |\alpha_i \rangle \in \mathcal{B}_V,\,|\beta_j \rangle \in \mathcal{B}_W\}$ 를 basis로 삼는 vector space를 **tensor product ** of vector space $V$ and $W$ 라 하며 $V \otimes W$ 라 쓴다.

---

(1) $k = \min (n,\,m)$ 일 때 $|v \rangle \in V \otimes W$ 는 $|v\rangle = |v_1 \rangle \otimes |w_1 \rangle + |v_2 \rangle \otimes |w_2 \rangle + \cdots + |v_k \rangle \otimes |w_k \rangle$  for some $|v_i \rangle \in V$ and $|w_i \rangle \in W$ 로 나타 낼 수 있으나, 이 표현은 unique 하지 않다.

(2) $V \otimes W$의 모든 elements 는 $\sum\limits_{i=1}^n \sum\limits_{j=1}^m a_{ij} (|\alpha_i\rangle \otimes |\beta_j \rangle )$ 로 표현 될 수 있으나 대부분의 $V\otimes W$의 원소들은 $|v \rangle \otimes |w \rangle$ for some $|v \rangle \in V$ and $|w\rangle \in W$ 의 간단한 형태로는 나타낼 수 없다. 이렇게 간단하게 나타 낼 수 없는 vector를 *entangled* 라 한다.

(3) $V,\,W$ 가 inner product space 일 때 $(\langle v_2 | \otimes \langle w_2 |)(|v_1 \rangle \otimes |w_1 \rangle ) =\langle v_2 | v_1 \rangle \langle w_2 | w_1 \rangle$ 이다. 

(4) $\dim (V \otimes W) = (\dim (V) ) (\dim (W))$.  



#### State space of an $n$-Qubit system

$V_i$ 가 single qubit에 상응하는 vector space 이고 그 basis를 $\{|0\rangle_i,\, |1\rangle_i\}$ 라 하자. Standard basis for the vector space $V_{n-1}\otimes V_{n-2}\otimes \cdots \otimes V_0$ for $n$ qubit system은 $2^n$ 개이며 다음과 같다
$$
|0\rangle_{n-1}\otimes \cdots \otimes |0\rangle_1 \otimes |0\rangle_0\;, \\
|0\rangle_{n-1}\otimes \cdots \otimes |0\rangle_1 \otimes |1\rangle_1\;, \\
\vdots\\
|1\rangle_{n-1}\otimes \cdots \otimes |1\rangle_1 \otimes |1\rangle_0\;.
$$
이것들을 이제 $|0\rangle|1\rangle \cdots |1\rangle$ 혹은 $|01\cdots1\rangle$ 식으로 첨자를 없애고 쓰기로 하자.

$n$ qubit system을 2진수로 표현 할 수 있다. 예를 들어 $|0000 \rangle = |0\rangle$, $|0110\rangle = |6\rangle$ 과 같이 쓸 수 있다. 이를 **binary representation** 이라 하며 $n$-qubit system 은 $|0\rangle,\ldots,\,|2^n-1\rangle$ 로 쓸 수 있다.



#### Bell basis

Standard basis 이외에 basis를 정하여 사용 할 수 있다. 예를 들면 2 qubit system 에서 아래와 같은 **Bell basis** $\{|\Phi^+,\,\Phi^-,\,\Psi^+,\,\Psi^- \}$ 가 많이 사용된다.
$$
\begin{align*}
\Phi^+ &= \dfrac{1}{\sqrt{2}} (|00\rangle + |11\rangle)\;,\\
\Phi^- &= \dfrac{1}{\sqrt{2}} (|00 \rangle - |11\rangle)\,,\\
\Psi^{+} &= \dfrac{1}{\sqrt{2}} (|01\rangle + |10\rangle)\,,\\
\Psi^{-} &= \dfrac{1}{\sqrt{2}} (|01\rangle - |10\rangle)\,.
\end{align*}
$$


#### Complex projective space

양자역학에서 $a|0\rangle + b|1\rangle$와 $ e^{i\phi}(a|0\rangle + b|1\rangle )$  가 서로 equivalent state이므로 $n$-dim. complex vector space 는 $n-1$ dim. **complex projective space**와 equivalent 하다. 따라서 $n$ qubit system 은 $2^n-1$ dim. complex projective space 이다.

$|v\rangle = e^{i\phi}|u \rangle$ for some $\phi \in \mathbb{R}$ 일 때 $e^{i\phi}$ 를 *global phase* 라 하며 $|v\rangle \sim |u\rangle$ 이라 쓴다.



## 2. Entangled State



#### Definition : Entangled state

$n$-qubit state $|\phi \rangle$ 가 single qubit states의 tensor product로 표현 될 수 없을 때 이를 **entangled state** 라 한다. 



<b>Example </b> Bell state $|\Phi^+\rangle = \dfrac{1}{\sqrt{2}} (|00\rangle + |11\rangle)$ 이 entangled state 임을 보이자. $|\Phi^+\rangle$ 이 entangled state 라면 $|\Phi^+\rangle = (a_1|0\rangle + b_1 |1\rangle) \otimes (a_2 |0\rangle + b_2 |1 \rangle) = a_1a_2 |00\rangle + a_1b_2|01\rangle +a_2b_1 |10\rangle + a_2b_2\rangle$ 이어야 한다. 따라서 $a_1 a_2 = a_2b_2 = 1/\sqrt2$ 이며 $a_1b_2 = a_2b_1=0$ 이어야 하나 불가능하다는 것을 쉽게 보일 수 있다.

모든 Bell states for $2$-qubit state는 entangled state 이다.



#### Entanglement for specific tensor product decomposition

Entanglement는 항상 state space에서의 어떤 특정한 tensor product decomposition에 대해서 이야기되어야 한다. 어떤 decomposition에선 entanglement 일지라도 다른 decomposition에서는 아닐 수 있다. 



<b>Example</b> $4$-qubit state $|\psi \rangle = \dfrac{1}{2} (|00\rangle + |01\rangle +|22\rangle + |33 \rangle )  = \dfrac{1}{2} (|0000\rangle + |0101\rangle + |1010\rangle + |1111\rangle)$ 을 생각하자. 이것이 single qubit states의 tensor product로 표현될 수 없음은 쉽게 보일 수 있다. 그러나 다음과 같이 표현 할 수 있다. $|\psi \rangle = \dfrac{1}{\sqrt{2}} (|0\rangle_1 |0\rangle_3 + |1\rangle_1 |1\rangle_3) \otimes \dfrac{1}{\sqrt{2}}  (|0\rangle_2 |0\rangle_4 + |1\rangle_2 |1\rangle_4) $ . 즉 $|\psi\rangle$ 은 tensor product of two $2$-qubits state 로 표현 될 수 있다. 





## 3. Basics of Multi-Qubit Measurements



#### Measurement in Quantum Mechanics 

Let $V$ be the $N=2^n$ dimensional vector space for $n$-qubit system. 특정 측정 방법에 따라 $V$는 orthogonal subspaces의 direct sum으로 decomposition 된다. 즉 $V=S_1 \oplus \cdots \oplus S_k$ for some $k \le N$.  

$|\psi\rangle \in V$ 는 linear combination of vectors in decomposes subspace 로 표현 될 수 있다. 즉 $|\psi\rangle = \sum\limits_{i=1}^k a_i |\psi_i \rangle$ where $|\psi_i \rangle \in S_i$. $|\psi\rangle$ 을 측정했을 때 $|\psi_i\rangle$ 이 얻어질 확률은 $|a_i|^2$ 이다. 더 정확히는 $|a_i|^2 /(\sum_i |a_i|^2)$ 이다. 








## Exercises

<b>3.2 </b> Entangled states의 linear combination이 entangled state가 되지 않을 수 있음을 예를 들어 보이시오.

---

Let $|\Phi^+\rangle = \dfrac{1}{\sqrt{2}} (|00\rangle + |11\rangle)$ and $|\Phi^- \rangle = \dfrac{1}{\sqrt{2}}(|00 \rangle - |11\rangle)$.  Then $\dfrac{1}{\sqrt{2}}(|\Phi^+\rangle + |\Phi^-\rangle) = |00\rangle$. 



<b>3.3</b> $|W_n\rangle = \dfrac{1}{\sqrt{n}} ( |0\ldots 001\rangle +|0\ldots 010\rangle + |0\ldots 100\rangle + \cdots + |1\ldots 000\rangle)$ 이라 하자. Show that $|W_n\rangle$ is entangled, with respect to the decomposition into the $n$ qubits, for every $n>1$ .

---

(1) Suppose $|W_n\rangle $ is not entangled. Then $|W_n \rangle = {\Large \otimes}_{i=1}^n(a_i|0\rangle_i + b_i |1\rangle_i)$ .

(2) 그렇다면 $a_1a_2\cdots b_{n-1}b_{n}= 0$ , $a_1 a_2 \cdots a_{n-1}b_n = 1$ 이므로 $b_{n-1}=0$ 이어야 한다. 그러나 $a_1 \cdots a_{n-2}b_{n-1}a_n=1$ 이므로 모순. 따라서 $|W_n\rangle$ 은 tensor product of components 로 표현 될 수 없으므로 entangled state 이다.   	



<b>3.4</b> $|GHZ_n \rangle = \dfrac{1}{\sqrt{2}} ( |00\ldots 0\rangle + |11\ldots 1\rangle)$ 이 with respect to the decomposition into the $n$ qubits 에 대해 entangled 임을 보이시오.

---

(1) Suppose $|GHZ_n\rangle $ is not entangled. Then $|GHZ_n \rangle = {\Large \otimes}_{i=1}^n(a_i|0\rangle_i + b_i |1\rangle_i)$ .

(2) $a_1 \cdots a_n = b_1 \cdots b_n=1$ but $a_1b_2 \cdots b_n=0$. contradiction !. 따라서 $|GHZ_n \rangle$ is entangled.



<b>3.5</b> $|\phi\rangle =\dfrac{1}{\sqrt{2}}(|0\rangle |+\rangle + |1\rangle |-\rangle)$ is entangled?

---

(1) $|+\rangle = \dfrac{1}{\sqrt{2}}(|0\rangle + |1\rangle),\, |-\rangle =\dfrac{1}{\sqrt{2}}(|0\rangle - |1\rangle)$ are Hadamard basis. Therefore, $|\phi \rangle = \dfrac{1}{2} (|00\rangle + |01\rangle + |10\rangle - |11\rangle)$ . 

(2) Suppose it is not entangled. Then $|\phi\rangle = (a_1|0\rangle + a_2 |1|\rangle)\otimes (b_1|0\rangle + b_2|1\rangle)$ , and $a_1b_1 = a_1b_2=a_2b_1=1/2$, and $a_2b_2 = -1/2$. Contradiction!



<b>3.7</b> 다음 states를 Bell basis를 사용하여 쓰시오.

---

(a) $|00\rangle = \dfrac{1}{\sqrt{2}}(|\Phi^+\rangle + |\Phi^-\rangle)$. 

(b) $|+\rangle|-\rangle = \dfrac{1}{2}(|00\rangle - |01\rangle + |10\rangle - |11\rangle) =\dfrac{1}{\sqrt{2}}(|\Phi^{-}\rangle -|\Psi^{-}\rangle )$.

(c) $\dfrac{1}{\sqrt{3}} (|00\rangle + |01 \rangle +|10\rangle) = \dfrac{1}{\sqrt{6}}(|\Phi^+\rangle + |\Phi^{-}\rangle + 2|\Psi^+\rangle)$.  



<b>3.9 </b> (a) 임의의 $n$-qubit quantum state는 $a_0|0\ldots 00\rangle + a_1 |0\ldots 01\rangle + \cdots + a_{2^n-1}|1\ldots 11\rangle$ 로 표현될 수 있음을 보이시오.

(b) (a)의 표현 형식이 unique 함을 보이시오.

---

(a) 임의의 $n$-qubit quantum state $|\psi\rangle = {\Large \otimes}_{i=1}^n (c_i |0\rangle  + d_i |1\rangle)$  를 생각하자. $a_i$에서 $i$의 2진법 표현에 따라 $c_i,\,d_i$ 를 곱하면 위의 주어진 벡터 표현이 된다.

(b) (a)의 표현법은 $\{c_i,\,d_i \} \to a_i$ 의 bijection 이다. 따라서 unique 하다. 



<b>3.10 </b> $\mathcal{B} = \{|\beta_1\rangle,\,|\beta_2\rangle,\ldots,\,|\beta_n\rangle \}$ 이 $n$-dim vector space $V$의 basis 이고 $|v\rangle =\sum_i a_i |\beta_i\rangle$, $|w\rangle = \sum_i c_i|\beta_i\rangle$ 일 때 다음을 보이시오.

(a) $\langle w|v\rangle = \sum_i a_i \overline{c_i}$ 

(b)$\big{|}|v\rangle\big{|}^2 = \langle v|v \rangle = \sum_i |a_i|^2$ 

---

Trivial



<b>3.11 </b> $|\psi\rangle$ 이 $n$-qubit state 일 때 $|\psi\rangle$ 과 한 standard basis $|j\rangle$ 사이의 거리는 $n$에만 dependent한  어떤 상수보다 큼을 보이시오. 즉 $\sum_j\big{|} |\psi\rangle - |j\rangle \big{|} \ge C$ where $C$ is a constant only depends on $n$.

---

(1) $n$-qubit state의 number of basis = $2^n$. Let $N=2^n$ and $\sum_j = \sum\limits_{j=1}^N = \sum\limits_{j=1}^{2^n}$. 

(2) $\sum_j \big{|}|\psi \rangle  - |j\rangle \big{|} = \dfrac{1}{2} \sum_j \left( \big{|}  |\psi \rangle - |j\rangle \big{|} + \big{|} |\psi\rangle - |j+1\rangle\big{|}\right)$ if we put $|N+1\rangle =|1\rangle|$.  From the triangle inequality  $|a-b|+|a-c| \ge |b-c|$, $\sum_j \big{|}|\psi \rangle  - |j\rangle \big{|} \ge \dfrac{1}{2} \sum_j \big{|}|j\rangle - |j+1\rangle\big{|} = \dfrac{1}{2}\sum_j \sqrt{2} = \dfrac{N}{\sqrt{2}}=2^{n-1/2}$ .



<b>3.12 </b> Standard basis 에 대해서 superposition 이지만 entangled 되지 않은 2-qubit state의 예를 드시오.

---

(1)  Consider $\left( \dfrac{1}{\sqrt{2}}(|0\rangle_1 + |1\rangle_1 ) \right) \otimes  \left( \dfrac{1}{\sqrt{2}}(|0\rangle_2 - |1\rangle_2 ) \right) = \dfrac{1}{2} ( |00\rangle -|01 \rangle +|10\rangle - |11\rangle)$.



<b>3.14 </b> Standard basis, Hadamard basis, 그리고 또하나의 basis $\mathcal{B}=\{ \frac{1}{\sqrt{2}}(|0\rangle+ \mathbf{i}|1\rangle), \frac{1}{\sqrt{2}}(|0\rangle - \mathbf{i}|1\rangle)  \}$ 를 생각하자. 

(a) 2-cubit system 의 $|00\rangle$ state에서 second qubit을 측정했을 때의 위의 세 basis에 대한 결과를 논하시오

(b) 