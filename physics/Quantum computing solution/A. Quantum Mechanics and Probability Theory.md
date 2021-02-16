A. Quantum Mechanics and Probability Theory
===



## 1. Tensor Products in Probability Theory



#### Definition : Simplex

$\mathbb{R}^n$에서의 vector의 집합 $\sigma_{n-1}=\{\mathbf{x} \in \mathbb{R}^n : x_i \ge 0 \text{ and } x_1+x_2 + \cdots +x_n =1\}$ 을 $n$ dimensional **simplex** (정확히는 *standard simplex* 혹은 *probability simplex*) 라 한다.



#### Definition : Probability distribution

$A$가 $n$ 개의 원소를 가진 집합일 때 $\mu : A \to [0,\,1]$ s.t. $\sum\limits_{a\in A} \mu (a) = 1$ 을 **probability distribution** on $A$ 라 한다. $\mathcal{P}^A$ 를 $A$ 에서의 모든 가능한 probability distribution을 나타내는 space라 하면 $\mathcal{P}^A = \sigma_{n-1}$ 이다.



$\mathbb{R}^A$ 는 $A \to \mathbb{R}$ functions의 집합을 의미한다. $\mathcal{P}^A \subset \mathbb{R}^A$ 이다.



#### Theorem 1.1

$A,\,B$가 유한집합일 때 $\mathcal{P}^{A\times B} \ne \mathcal{P}^A \times \mathcal{P}^B$ 이다.

---

*Proof is trivial*



#### Definition : Tensor products of the $\mathbb{R}^A$ kinds. 

$f \in \mathbb{R}^A$ 이고 $g \in \mathbb{R}^B$ 일 때 $f\otimes g : A\times B \to \mathbb{R}$ 을 $f\otimes g ((a,\,b)) = f(a)g(b)$ 로 정의한다.



#### Lemma 1.2

위의 tensor product의 정의는 axiom of tensor product를 만족한다.

---

*(Proof)* (1) Let $f_1,\,f_2,\,f \in \mathbb{R}^A$ and $g_1,\,g_2,\,g \in \mathbb{R}^B$. 이제 3개의 axioms를 보이자.

(2) $(f_1+f_2)\otimes g (a,\,b) = (f_1(a)+f_2(a))g(b) = f_1(a)g(b) + f_2(a)g(b) = (f_1 \otimes g) (a,\,b) + (f_2 \otimes g)(a,\,b)$.

(3) $f\otimes (g_1 + g_2)(a,\,b) = f(a) (g_1(b)+ g_2 (b)) = (f\otimes g_1) (a,\,b) + (f\otimes g_2) (a,\,b)$. 

(4)  for $c \in \mathbb{C}$, $(cf)\otimes g(a,\,b) = c\cdot f(a)g(b) = f\otimes (cg) (a,\,b) = c(f\otimes g (a,\,b))$. $\;\;\square$ 



#### Theorem 1.3

(a) $\mathbb{R}^A$ is a vector space.

(b) $\mathbb{R}^{A\times B} = \mathbb{R}^A \otimes \mathbb{R}^B$ where $\mathbb{R}^A \otimes \mathbb{R}^B$ is defined as $\{f\otimes g  : f \in \mathbb{R}^A,\,g\in\mathbb{R}^B\}$.

---

*(Proof)* (a) is trivial

(b) $\mathbb{R}^A \otimes \mathbb{R}^B \subset \mathbb{R}^{A \times B}$ 임은 자명하다. $h \in \mathbb{R}^{A \times B}$ 라 하자. Define $f_b^A : A \to \mathbb{R}$ and $g_a^B : B\to \mathbb{R}$ as $f_b^A(a) = h(a,\,b)$ and $g_a^B(b) = h(a,\,b)$. 

또한 probability distribution $\delta_a^A : A\to \mathbb{R},\, \delta_b^B : B \to \mathbb{R}$ as $\delta_a^A (a') = \delta_{a,\,a'}$  and $\delta_b^B (b') = \delta_{b,\,b'}$ 으로 정의한다. $\delta(x)$ 는 Kronecker delta 이다.

이제 $h(a,\,b) = \sum\limits_{a'\in A} \delta_{a'}^A (a) \otimes g_{a'}^B (b) = \sum\limits_{b'\in B}f_{b'}^A \otimes \delta_{b'}^B$ 임은 쉽게 보일 수 있다. 즉 $h \in \mathbb{R}^{A\times B} \implies  h \in \mathbb{R}^A \otimes \mathbb{R}^B$ 이므로 $\mathbb{R}^{A \times B} \subset \mathbb{R}^A \otimes \mathbb{R}^B$ 이다.  따라서 $\mathbb{R}^{A\times B} = \mathbb{R}^A \otimes \mathbb{R}^B$ . $\;\;\square$



#### Theorem 1.4

$\mathcal{P}^{A \times B} = \mathcal{P}^A \otimes \mathcal{P}^B$.

---

*(Proof)* (1) Let $\mu \in \mathcal{P}^A$ and $\nu\in \mathcal{P}^B$. $\sum\limits_{(a,\,b) \in A \times B} (\mu \otimes \nu )(a,\,b) = \sum\limits_a \sum\limits_b \mu(a)\nu(b) = 1$.  따라서 $\mathcal{P}^A \otimes \mathcal{P}^B \subset \mathcal{P}^{A \times B}$.

(2) Suppose $\lambda_i \in \mathcal{P}^{A}$  for $i=1,\,2,\ldots$ . Then we can show that $\theta =\sum c_i \lambda_i \in \mathcal{P}^A$ if $\sum c_i=1$. Same for $\mathcal{P}^B$ and $\mathcal{P}^{A \times B}$. 

(3) Suppose $\eta \in \mathcal{P}^{A \times B}$ and it will be shown that $\eta \in \mathcal{P}^A \otimes \mathcal{P}^B$. Define $h_a^B : B \to \mathbb{R}$ as $h_a^B (b) = \dfrac{\eta (a,\,b)}{\sum\limits_{b' \in B} \eta (a,\,b')}$ (4) Let $c_a =\sum\limits_{b \in B} \eta (a,\,b)$ and $c_b =\sum\limits_{a \in A}\eta (a,\,b)$. Then $1 = \sum\limits_{a\in A}c_a = \sum\limits_{b \in B} c_b$. 

(5) $\eta(a,\,b) = \sum\limits_{a'\in A} c_{a'} h_{a'}^B (b) \delta_{a'}^A (a) = \sum\limits_{a'\in A} c_{a'} \left(\delta_{a'}^A \otimes h_{a'}^B\right) (a,\,b) \in \mathcal{P}^A \otimes \mathcal{P}^B $ , with $\sum\limits_{a' \in A} c_{a'} =1$. $\;\;\square$



#### Definition : Independent (or uncorrelated) joint distribution, Marginal distribution

$\mu \in \mathcal{P}^{A \times B}$ is said to be **independent** (or **uncorrelated**)  If $\exist \mu_A \in \mathcal{P}^A$ and $\mu_B \in \mathcal{P}^B$ s.t. $\mu = \mu_A \otimes \mu_B$ .  **Marginal distribution** $\mu_A \in \mathcal{P}^A$ is defined as $\mu_A (a) = \sum\limits_{b\in B} \mu (a,\,b)$. 

---

(1) 많은 경우 $\mu \in \mathcal{P}^{A \times B}$ is not independent.



#### Lemma 1.5

$\mu \in \mathcal{P}^{A\times B}$ is independent $\iff$ $\mu$ is a tensor product of its marginal. 

---

*(Proof)* (1) $\Longleftarrow $ is trivial

(2) Suppose $\mu \in \mathcal{P}^{A \times B}$ is independent. 즉 $\mu (a,\,b) = (\mu_A \otimes \mu_B )(a,\,b) = \mu_A(a) \mu_B(b)$. $\sum\limits_{a \in A} \mu (a,\,b) = \sum \limits_{a \in A} \mu_A(a) \mu_B(b) \implies \sum\limits_{a\in A} \mu (a,\,b) = \mu_B(b)$. 즉 $\mu_B$ is marginal. 같은 방법으로 $\mu_A$ 가 magninal 임을 보일 수 있다. $\;\;\square$



#### Definition : Pure distribution, Mixed distribution

$\mu \in \mathcal{P}^A $ is said to be **pure** if $\mu (a) = \delta (a-a')$ for some $a' \in A$. If $\mu$ is not pure, it is said to be **mixed**.



#### Definition : collapse, update

새로운 정보가 입수된 후 확률분포가 바뀌는 것을 **updating** 이라 하며, 양자 측정에서는 이를 **collapse**라 한다.



#### Probability distribution as operator

Consider set of linear operators $\mathcal{M}^A =\{ M: \mathbb{R}^A \to \mathbb{R}^A\}$ . For $f \in \mathbb{R}^A$, $M_f : \mathbb{R}^A \to \mathbb{R}^A$, defined as $M_f (g) = fg$, is an element of $\mathcal{M}^A$ .  $\mu \in \mathcal{P}^A$ 이면 $M_\mu \in \mathcal{M}^A$. 





## 2. Quantum Mechanics as a Generalization of Probability Theory







## Exercises

<b>1. </b> Independent joint distribution 은 its marginals의 tensor product 임을 보이시오.

---

see lemma 1.5



<b>2. </b> 일반적인 distribution은 its marginals의 tensor product로 표현할 수 없음을 보이시오. 같은 marginals를 갖는 세 distinct distribution을 보이시오.

---

(1) Let $A=\{a_1,\,a_2\}$ and $B=\{b_1,\,b_2,\,b_3\}$ . $\mu \in \mathcal{P}^{A \times B}$ is defined as $\mu (a_1,\,b_1)= 0$, $\mu (a_1,\,b_2)= 1/12$, $\mu(a_1,\,b_3) = 1/12$, $\mu(a_2,\,b_1)=1/4$, $\mu(a_2,\,b_2) = 1/3$, and $\mu(a_3,\,b_3) = 1/4$.

(2) $\mu_A (a_1) = 1/6$, $\mu_A (a_2) = 5/6$ , $\mu_B(b_1) = 1/4$, $\mu_B(b_2)= 5/12$, $\mu_B(b_3) = 1/3$.

(3) $\mu_A \otimes \mu_B (a_1,\,b_1) = 1/24$, $\mu_A \otimes \mu_B (a_1,\,b_2) = 5/72$, $\mu_A\otimes \mu_B (a_1,\,b_3) = 1/18$, $\mu_A \otimes \mu_B (a_2,\,b_1) = 5/24$, $\mu_A \otimes \mu_B (a_2,\,b_2 ) = 25/72$ , $\mu_A \otimes \mu_B (a_2,\,b_3) = 5/18$.   $\mu \ne \mu_A \otimes \mu_B$. 

(4)  

```
 A\B      0     1     2     3      Tot
 ------------------------------------- 
  0      1/8    0     0     0      1/8
  1       0    2/8   1/8    0      3/8
  2       0    1/8   2/8    0      3/8
  3       0     0     0    1/8     1/8
 ------------------------------------- 
 Tot     1/8   3/8   3/8   1/8      1  
```

(5)

```
 A\B      0     1     2     3      Tot
 ------------------------------------- 
  0       0     0     0    1/8     1/8
  1       0    1/8   2/8    0      3/8
  2       0    2/8   1/8    0      3/8
  3      1/8    0     0     0      1/8
 ------------------------------------- 
 Tot     1/8   3/8   3/8   1/8      1  
```

(6)

```
 A\B      0     1     2     3      Tot
 ------------------------------------- 
  0     1/16    0     0   1/16     1/8
  1       0    1/8   2/8    0      3/8
  2       0    2/8   1/8    0      3/8
  3     1/16    0     0   1/16     1/8
 ------------------------------------- 
 Tot     1/8   3/8   3/8   1/8      1  
```



<b>3. </b> 다음을 증명하시오

(a) Tensor product of pure distribution is pure.

(b) 모든 distribution은 pure distribution의 linear combination이다. 또한 유한집합 $A$에 대한 distribution은 convex 이다.

(c) Joint system $A \times B$ 에서의 pure distribution은 uncorrelated 되어 있다.

(d) 다른 distribution의 linear combination으로 표현 될 수 없는 distribution을 **extremal** 이라 한다. Extremal distribution 는 pure distribution 임을 보이시오.

---

(a) Let $\delta = \delta_{a'}^A\otimes \delta_{b'}^B$ . Then $\delta(a,\,b) = 1$ only if $(a,\,b) = (a',\,b')$. 따라서 $\delta$ 는 pure distribution

(b)  Let $\mu \in \mathcal{P}^A$ . Then $\mu =\sum\limits_{a \in A} \mu(a)\delta_a^A$ , linear combination of pure distribution. Let $\mu_1,\,\mu_2 \in \mathcal{P}^A$. Then $\mu = \theta \mu_1 + (1-\theta)\mu_2 \in \mathcal{P}^A$ for $0\le \theta \le 1$. 다라서 $\mathcal{P}^A $ for finite set $A$ is convex

(c) Define $\delta_{(a',\,b')}^{A\times B} : A \times B \to \mathbb{R}$ as $\delta_{(a',\,b')}^{A \times B} (a,\,b)=1$ only if $(a,\,b) = (a',\,b')$ and $0$ otherwise. Then $\delta_{(a',\,b')}^{A\times B}$ is pure distribution on $A \times B$ and $\delta_{(a',\,b')}^{A \times B} = \delta_{a'}^A \otimes \delta_{b'}^B$, which means uncorrelated distribution.

(d) (b) 로 부터 pure distribution이 아닌 distribution은 linear combination of more than two pure distributions 이므로 extremal distribution 이면 pure distribution 이다. 그리고 pure distribution은 다른 pure distribution의 linear combination으로 표현 될 수 없으므로 extremal 이다.



<b>4. </b> operator $M_\mu$ 에 대한 probability distribution $\mu$가 projector 이면 $\mu$ 는 pure distribution 임을 보이시오.

---

(1) Suppose $\mu\in \mathcal{P}^A$ is projector. Then for any $f \in \mathbb{R}^A $,  $\mu(a)\mu (a)f (a)= \mu(a) f (a) $ for all $a \in A$.  따라서 $\mu (a) = 1$ or $0$ 이며 $\mu \in \mathcal{P}^A$ 이므로 $\mu$는 pure distribution.



<b>5. </b> 