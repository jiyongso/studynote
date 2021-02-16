IV. Measurement of Multiple Qubit States
===



## 1. Dirac's braket notation for linear transformation



#### Operator on $n$-qubit system

$|i\rangle\langle j|$ is an operator on $n$-qubit system which maps $|j\rangle$ to $|i\rangle$ and others to 0. 

Linear combination of operators are also operators. Therefore $\hat{O} = \sum\limits_i \sum\limits_j a_{ij}|i\rangle\langle j|$ is also an operator.

Matrix elements of $\hat{O}$ in the standard basis $\hat{O}_{ij} = \langle i | \hat{O} |j\rangle = \sum\limits_{p} \sum\limits_{q} a_{pq} \langle i|p \rangle \langle q | j\rangle = a_{ij}$ 

For $|\psi \rangle = \sum_k b_k |k\rangle$, $\hat{O}|\psi\rangle = \sum_i \sum_j a_{ij}|i\rangle\langle j | (\sum_k b_k |k\rangle) = \sum_i \sum_j \sum_k a_{ij}b_k |i\rangle\langle j|k\rangle = \sum_i \sum_j a_ij b_j |i\rangle$. 



## 2. Projection Operators for Measurements

#### Projection operator

$V$ 가 vector space 이고 $S$ 는  proper subspace of $V$ 라 하자. 이 때 $V$의 다른 proper subspace  $S^{\perp}$가 존재하여 임의의  $|w\rangle \in S^{\perp}$ 는 모든 $|v\rangle \in S$ 에 대해 perpendicular 하다. 그리고 $S \cap S^{\perp} = \{0\}$ 이며 $V = S \oplus S^{\perp}$ 이다.

$|v\rangle \in V$ 는 어떤  $|s\rangle \in S$ and $|s' \rangle \in S^{\perp}$에 대해  $|v\rangle = |s \rangle  + |s' \rangle$ 이며 이 표현은 unique 하다. 이로부터 $\hat{P}:V \to V$ s.t $\hat{P}|v\rangle = |s\rangle$ 인 operator $\hat{P}$를 생각 할 수 있다. 이런 operator를 **projection operator** 라 한다.

$V = S_1 \oplus S_2 \oplus \cdots \oplus S_k$ 이고 $\{S_i : i=1,\ldots,\,k\}$ 가 orthogonal subspaces 이면 projection operator $\hat{P_i} : V \to V$ with $\hat{P_i}(V) = S_i$ 를 생각 할 수 있다. 



$S$ 가 vector space $V$의 subspace 이고 $\{|\alpha_1 \rangle, \ldots,\,|\alpha_s\rangle\}$ 이 basis of $S$ 일 때 projection operator of $V$ on $S$, $\hat{P}_S$ 는 다음과 같다. $\hat{P}_S = {\textstyle \sum\limits_{i=1}^s}|\alpha_i \rangle \langle\alpha_i|$.



#### Adjoint operator or Conjugate transpose

$V,\,W$가 inner product vector space 이고 $\hat{O}:V \to W$가 operator 라 하자. $\hat{O}$에 대한 **adjoint operator** (or **conjugate transpose**) 는 다음을 만족하는 operator from $W$ to $V$를 의미하며 $\hat{O}{}^{\dagger}$ 로 쓴다.

(1) For any $|w\rangle\in W$ and $\hat{O}|v \rangle \in W$, $\langle v| \hat{O}{}^\dagger |w \rangle = \langle w | \hat{O} |v\rangle $   



$V$, $W$ 의 basis $\{|\alpha_i\rangle\}$, $\{|\beta_i\rangle\}$ 을 생각하자. 이 basis에서의 $\hat{O}$의 matrix element $\hat{O}_{ij} = {\hat{O}_{ji}}^*$ 임을 알 수 있다. 



#### Projection operator case

$\hat{P} : V \to V$ 가 projection operator 이면 ${\hat{P}}{}^2=\hat{P}$ 이다. 또한 $\hat{P}{}^{\dagger}= \hat{P}$ 이다.



## 3. Hermitian Operator Formalism for Measurement



Vector space $V,\,W$ 에 대해 $V \to W$ 로의 모든 operator의 집합을 $\mathcal{L}(V,\,W)$ 라 하자. $\mathcal{L}(V,\,V)$ 는 $\mathcal{L}(V)$ 로 쓰자.

#### Eigenvalue, Eigenvector, Eigenspace

$\hat{O} \in \mathcal{L}(V)$ 일 때 $\hat{O}|v\rangle = \lambda |v\rangle$ for some nonzero vector $|v\rangle$ 이면 $|v\rangle$을 **eigenvector** of $\hat{O}$ 라 하고 $\lambda$를 **eigenvalue** of $\hat{O}$라 한다. 만약 $|v\rangle$과  $|w\rangle$이 같은 eigenvalue $\lambda$를 갖는 eigenvectors of $\hat{O}$ 일 때 $|v\rangle $와 $|w\rangle$ 로 span 되는 subspace of $V$를 **$\lambda$-eigenspace** of $\hat{O}$ 라 한다.    



#### Hermitian

$\hat{O} \in \mathcal{L}(V)$ 에 대해 $\hat{O}{}^{\dagger}=\hat{O}$ 이면 $\hat{O}$를 **hermitian** operator 라 한다. 

---

(1) Hermitian operator의 eigenvalue는 real 이다. Let $|v\rangle \in V$ and $\hat{O}|v\rangle = \lambda |v\rangle$ . Then $\langle v |O|v\rangle = \lambda = $$\langle v| \hat{O}{}^{\dagger} |v\rangle =$$ (\langle v |\hat{O}|v\rangle) ^* =\lambda^*$ 

(2) 서로 다른 eigenvalue를 갖는 eigenvector는 orthogonal 하다. Suppose $|v_1\rangle$ and $|v_2\rangle$ are eigenvectors of $V$ of operator $\hat{O} \in \mathcal{L}(V)$ and has distinct eigenvalue $\lambda_1,\,\lambda_2$ respectively. 

$\langle v_2 | \hat{O}|v_1 \rangle = \lambda_1 \langle v_2|v_1 \rangle$  and $\langle v_2|\hat{O}|v_1 \rangle^* = \langle v_1 |\hat{O}{}^{\dagger}|v_2\rangle = \langle v_1 |\hat{O}|v_2\rangle = \lambda_2\langle v_1 |v_2 \rangle$.  

따라서  $0=\lambda_1\langle v_2|v_1\rangle - (\lambda_2\langle v_1|v_2\rangle)^*=(\lambda_1-\lambda_2)\langle v_2 |v_1\rangle$. $\lambda_1 \ne \lambda_2$ 이므로 $\langle v_2|v_1\rangle = 0$. 

이로부터 서로 다른 eigenvalue를 가지는 eigenspace는 서로 orthogonal 함을 알 수 있다.

(3)  $V$의 모든 vector는 $\hat{O}$ 의 eigenvectors의 linear combination으로 표현 할 수 있다. 즉 $\lambda_1,\ldots,\,\lambda_k$ 가 가능한 모든 eigenvalue 이고 이에 상응하는 eigenspace를 $S_1,\ldots,\,S_k$ 라 할 때 $V=S_1 \oplus \cdots \oplus S_k$ 이다. 이에 대한 증명은 exercise 4.16 을 통해서.







## Exercises

<b>4.2 </b> 다음 operator를 braket notation을 사용하여 표현하시오

(a) Hadamard operator $H =\left[\begin{array}{cc} \frac{1}{\sqrt{2}} &  \frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}} \end{array}\right]$.

(b) $X = \left[\begin{array}{cc} 0 & 1 \\ 1 & 0\end{array}\right]$.

(c) $Y=\left[\begin{array}{cc} 0 & 1 \\ -1 & 0\end{array}\right]$.

(d) $Z=\left[\begin{array}{cc} 1 & 0 \\ 0 & -1\end{array}\right]$.

(e) 생략

(f) $X\otimes X$.

(g) $X \otimes Z$.

(h) $H \otimes H$.

(i) The projection operator $P_1: V \to S_1$ and $P_2 :V \to S_2$ , where $S_1 = \text{span} ( \{ |\texttt{+}\rangle|\texttt{+}\rangle, |\texttt{-}\rangle|\texttt{-}\rangle \})$ ,  $S_1 = \text{span} ( \{|\texttt{+}\rangle|\texttt{-}\rangle, |\texttt{-}\rangle|\texttt{+}\rangle \})$

---

(a) $H = \dfrac{1}{\sqrt{2}}|0\rangle \langle 0| +\dfrac{1}{\sqrt{2}}|0\rangle \langle 1| +\dfrac{1}{\sqrt{2}}|1\rangle \langle 0|-\dfrac{1}{\sqrt{2}}|1\rangle \langle 1|$ .

(b) $X= |0\rangle\langle 1| + |1\rangle \langle 0|$ .

(c) $Y= |0\rangle\langle 1| - |1\rangle \langle 0|$ .

(d) $Z= |0\rangle\langle 0| - |1\rangle \langle 1|$ .

(f) $X \otimes X = (|0\rangle\langle 1| + |1\rangle \langle 0|) \otimes (|0\rangle\langle 1| + |1\rangle \langle 0|) = |00\rangle\langle 11| + |01\rangle\langle10| + |10\rangle\langle 01| + |11\rangle\langle11|$. 

(g) $X \otimes Z = (|0\rangle\langle 1| + |1\rangle \langle 0|) \otimes  (|0\rangle\langle 0| - |1\rangle \langle 1|) = |00\rangle\langle10| - |01\rangle\langle11|+ |10\rangle\langle00| - |11\rangle\langle01|$.

(h) 

$$
\begin{align*}
H \otimes H &= \dfrac{1}{2} \left( |00\rangle\langle 00| +|00\rangle\langle01|+ |01\rangle\langle 00|  - |01\rangle \langle 01| + |00\rangle\langle10| + |00\rangle\langle 11| + |01\rangle\langle10| - |01\rangle\langle 11|  \right. \\
&+ \left. |10\rangle\langle 00| + |10\rangle\langle 01| + |11\rangle\langle 00| - |11\rangle\langle01| - |10\rangle\langle 10| - |10\rangle\langle 11|-|11\rangle\langle10| + |11\rangle\langle 11|    \right)\;.
\end{align*}
$$

(i) $P_1 = |\texttt{++}\rangle\langle \texttt{++}| + |\texttt{--}\rangle\langle \texttt{--}|$, $P_2 = |\texttt{+-}\rangle\langle \texttt{+-}| + |\texttt{-+}\rangle\langle \texttt{-+}|$ . 



<b>4.3 </b> Projection operator는 its own adjoint 임을 보이시오

---

(1) $\hat{P}{}^2=\hat{P}$ iff $\hat{P}$ is a projection operator. 

(2) $\hat{P} = |\psi\rangle \langle \psi|$ . Then $\hat{P}{}^{\dagger} = (|\psi\rangle)^* (\langle \psi |)^* = |\psi\rangle \langle \psi| = \hat{P}$



<b>4.4 </b> Hadamard basis에서의 projection operator를 구하고 $|\psi\rangle = a |0 \rangle + b|1 \rangle$ 에 대한 기대값을 구하시오.

---

(1) Hadamard basis : $|+\rangle = \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle)$ and $|-\rangle = \frac{1}{\sqrt{2}}(|0\rangle -|1\rangle)$ 

(2) $\hat{P}_+ = |+\rangle\langle+|$,  $\hat{P}_{-} = |-\rangle\langle-|$.  $|0\rangle = \frac{1}{\sqrt{2} }(|+\rangle + |-\rangle)$ , $|1\rangle = \frac{1}{\sqrt{2}} (|+\rangle - |-\rangle)$ . Therefore $|\psi\rangle = \dfrac{a+b}{\sqrt{2}}|+\rangle + \dfrac{a-b}{\sqrt{2}} |-\rangle$ . $\langle \psi |\hat{P}_{+}| \psi \rangle = \dfrac{|a+b|^2}{2}$, $\langle \psi |\hat{P}_{-}|\psi\rangle = \dfrac{|a-b|^2}{2}$



<b>4.7 </b> Projection operator formalism을 사용하시오.

(a) Hadamard basis 에서의 임의의 2-qubit states에서 첫번째 qubit을 측정할 때, 가능한 모든 상황에 대한 확률을 구하시요

(b) $|\Psi^+\rangle = \dfrac{1}{\sqrt{2}} ( |00\rangle + |11\rangle)$  에 대한 (a)의 결과를 구하시오

(c) (b)의 가능한 결과를 이용하여 standard basis에서 second qubit을 측정했을 때의 가능한 결과를 구하시오

(d) (b)의 가능한 결과를 이용하여 Hadamard basis에서 second qubit을 측정했을 때의 가능한 결과를 구하시오

---

(a) In Hadamard basis, $|\texttt{++}\rangle = \dfrac{1}{2}(|00\rangle + |01\rangle +|10\rangle + |11\rangle )$ , $|\texttt{+-}\rangle = \dfrac{1}{2}(|00\rangle - |01\rangle +|10\rangle - |11\rangle )$ ,  $|\texttt{-+}\rangle = \dfrac{1}{2}(|00\rangle + |01\rangle -|10\rangle - |11\rangle )$,  $|\texttt{--}\rangle = \dfrac{1}{2}(|00\rangle - |01\rangle -|10\rangle + |11\rangle )$.

Let arbitrary 2-qubit states $|\psi\rangle = a_1 |\texttt{++}\rangle + a_2 |\texttt{+-}\rangle + a_3 |\texttt{-+}\rangle + a_4 |\texttt{--}\rangle$. 

$P(|\psi\rangle \to |0\rangle_1) = |{}_1\langle 0|\psi\rangle|^2 = |a_1(1/2+1/2) + a_2(1/2-1/2) + a_3(1/2+1/2 )+ a_4(1/2-1/2))|^2 = |a_1+a_3|^2 $

$P(|\psi\rangle \to |1\rangle_1) = |{}_1\langle 0|\psi\rangle|^2 = |a_1(1/2+1/2) + a_2(1/2-1/2) - a_3(1/2+1/2 )+ a_4(-1/2+1/2))|^2 = |a_1-a_3|^2 $  

(b) $P(|\Psi^{+} \rangle  \to |0\rangle_1)  = |{}_1\langle 0|\Psi^+\rangle|^2 = 1/2$, Similarly   $P(|\Psi^{+} \rangle \to |1\rangle_1)  =1/2$ .

(c) 





<b>4.8 </b> $(\hat{A}|x\rangle)^{\dagger} = \langle x|\hat{A}{}^{\dagger}$ 임을 보이시오.

---

$((\hat{A}|x\rangle)^{\dagger})_{i}= (\sum_j A_{ij} x_j)^{\dagger} = \sum_j \overline{x_j} \overline{A_{ji}} = (\langle x|\hat{A}{}^{\dagger})_i$



<b>4.9 </b>Design a measurement on a 3-qubit system that distinguishes between states in which all bit values are equal and those in which they are not, and gives no other information. Write all operators in bra/ket notation.

---

$\hat{M}=|000\rangle \langle 000|+|111\rangle \langle111|$ 



<b>4.10 </b> Design a measurement on a 3-qubit system that distinguishes between states in which the number of 1 bits is even, and those in which the number of 1 bits is odd, and gives no other information. Write all operators in bra/ket notation.

---

$\hat{M}=|000  \rangle \langle 000|+|011\rangle \langle  011|+|110\rangle \langle 110|$



<b>4.11 </b> Design a measurement on a 3-qubit system that distinguishes between states with different numbers of 1 bits, and gives no other information. Write all operators in bra/ket notation.

---

$\hat{M} =|001 \rangle \langle 001|+|010 \rangle \langle 010|+|100 \rangle \langle 100|+2(|011 \rangle \langle011|+|101 \rangle \langle 101|+|110 \rangle \langle 110|)+3|111 \rangle \langle 111|$ 



<b>4.12 </b>$\hat{O} $ 가 subspace decomposition $V=S_1 \oplus S_2 \oplus S_3 \oplus S_4$ with projection operators $\hat{P}_1,\,\hat{P}_2,\,\hat{P}_3,\,\hat{P}_4$ 를 만드는 operator라 하자. 이 때 subspace decomposition $V=S_5 \oplus S_6$ with $S_5 = S_1 \oplus S_2$ and $S_6 = S_3 \oplus S_4$ 에 대하 measurement operator는 무엇인가?

---

 $\hat{O}{}'  = P_1 +P_2 - (P_3+P_4) $











<b>4.16 </b> $O \in \mathcal{L}(V)$ 가 hermitian 이며 $U\in \mathcal{L}(V)$ 는 unitary라 하자. $U^{\dagger}U = UU^{\dagger}= I$ 일 때 $U$를 unitary 라 한다. 이 때 다음을 보이시오. ($V$는 finite dimensional vector space on $\mathbb{C}$ 임을 가정하자)

(a) $U$의 columns 는 서로 orthonormal 하다

(b) $U^{\dagger}OU$ 도 hermitian 이다

(c) $T\in \mathcal{L}(V)$ 이면 최소한 하나의 eigenvalue와 eigenvectors of $T$가 존재한다.

(d) 임의의 $A \in \mathcal{L}(V)$ 에 대해 어떤 unitary operator가 존재하여 $UAU^{-1}$ 를 upper triangle로 만든다.

(e) $O$의 eigenvalues $\lambda_1,\ldots,\lambda_k$ 에 상응하는 eigenspace $S_1,\ldots,S_k$ 에 대해 $V=S_1\oplus \cdots \oplus S_k$ 이다.

---

(a) $U = \left[\begin{array}{ccc} {}& {}&{}\\ u_1 &u_2& \cdots \\{}& {}&{}\end{array}\right]$ 라 하자. $u_i$ 는 $i$-th column of $U$ 이다. $(U^{\dagger}U)_{ij} = (u_i,\,u_j)= \delta_{ij}$.

(b) $A,\,B \in \mathcal{L}(V)$ 일 때 $(AB)^{\dagger}=B^{\dagger}A^{\dagger}$ 이므로 $(U^{\dagger}OU)^{\dagger} = U^{\dagger}O^{\dagger}U = U^{\dagger}OU$.

(c) $Tv\ne \lambda v$ for any $\lambda \in \mathbb{C}$ and $v \in V$. Then $(T-\lambda I)v \ne 0 \implies \det (T-\lambda I) \ne 0$ for any $\lambda \in \mathbb{C} $ . $\det (T-\lambda I)$ is a polynomial on complex field, and therefore must be zero for some $\lambda$.

(d) 

(e) 