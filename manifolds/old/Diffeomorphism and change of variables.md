Diffeomorphisms and Change of Variables
---

<u>(2019.05.09) </u>



#### Definition : Diffeomorphism

$A,\,B$ 가 $\mathbb{R}^n$의 open set 이고 $g: A \rightarrow B$ 가 bijection 이며 $g,\,g^{-1}$ 이 $C^r$ class 함수 일 때 $g$를 **diffeomorphism** (of class $C^r$) 이라 한다.



#### Lemma 1. 

Let $A$ be open in $\mathbb{R}^n$ and $g : A \rightarrow \mathbb{R}^n$ be a $C^1$ class function. 만약 $E\subset A$가 measure 0 이면 $g(E)$ 도 measure zero 이다.

---

*Proof*   $S \subset \mathbb{R}^n$ 이 measure 0 이면 전체 volume이 $\varepsilon$ 보다 작고 개개의 width가 $\delta$ 보다 작은 closed cubes 로 cover 됨은 쉽게 보일 수 있다. 

$C\subset A$ 가 $\mathbf{a}$를 중심으로 하는 width $w$ 의 cube라 하자.  $g \in C^1$ 이므로 ${}^\exist M>0$ s. t. $|Dg(\mathbf{x}) |\le M$ for all $\mathbf{x} \in C$ 이다. $|\mathbf{x} - \mathbf{a}| < w/2$ 고 $\mathbf{x}$와 $\mathbf{a}$를 잇는 line segments가 $C$ 안에 존재하므로 mean value theorem을 쓰면 $g_j (\mathbf{x}) - g_j(\mathbf{a}) = Dg_j (\mathbf{c_j}) \cdot (\mathbf{x} -\mathbf{a})$ 를 만족하는 $\mathbf{c_j} \in C$ 이다. 따라서
$$
|g_j (\mathbf{x}) -g_j (\mathbf{a})| \le n |Dg_j (\mathbf{c}_j)| |\mathbf{x}-\mathbf{a}| \le nM\left(\dfrac{w}{2}\right)\;.
$$
for all $j \in \{1,\,2,\,\ldots,\,n\}$ and $\mathbf{x} \in C$ 이며 따라서 모든  $\mathbf{x}\in C$ 에 대해 다음이 성립한다. 
$$
|g(\mathbf{x})-g(\mathbf{a}) |\le n M (w/2)\;.
$$
($|\mathbf{a}| = \sup\{ |a_1|,\,|a_2|,\ldots,\,|a_n|\} $ 이며 $|\mathbf{A}| = \sup \{ |A_{ij}| \}$ 임에 유의하라.)

이제 $g(E)$가 measure 0임을 보이자. $\{C_i\}$ 가 $C_i \subset \text{Int}(C_{i+1})$ 를 만족하며  $\bigcup_{i}\{C_i\} = A$ 를 만족하는 compact subset의 sequence라 하자(우리는 이런 sequence가 항상 존재함을 안다.). $E_k = C_k \cap E$라 하자. $C_k$가 compact set 이므로 $C_k$의 $\delta$-neighborhood가 $\text{int} (C_{k+1})$ 에 포함되도록 하는 $\delta > 0$을 선택 할 수 있다. $g \in C^1$ 이므로 $|Dg(\mathbf{x})| \le M$ for $\mathbf{x} \in C_{k+1}$ 이 되는 $M$을 선택 할 수 있다. 

$E_k \subset E$ 이므로 $E_k$는 measure 0 이고 따라서, $E_k$ 를 그 폭이 $\delta$보다 작고 총 부피가 $\varepsilon' = \varepsilon/(nM)^n$보다 작은 cube로 cover 할 수 있음을 알고 있다.  $D_1,\,D_2,\ldots$를 $E_k$와 intersect 하는 이 cubes라 하자. $D_i$의 width는 $\delta$보다 작고 $D_i \subset \text{Int}(C_{k+1})$ 이므로 $|Dg(\mathbf{x})| \le M$ for $\mathbf{x} \in D_i$ 이다. 따라서 $g(D_i)$ 는 width가 $nM \cdot (\text{width} \, D_i)$ 인 cube $D'_i$에 포함된다. $D'_i$의 부피는 다음과 같다.
$$
v(D'_i) = (nM)^n (\text{width }D_i)^n = (nM)^n v(D_i)\;.
$$
Cubes $\{D'_i \}$ 가 $g(E_k)$를 cover 하므로 total volume of $g(E)$ 는 $\varepsilon = \varepsilon' (nM)^n$ 보다 작다고 할 수 있다. $\square$. 



#### Theorem 2.

$\mathbb{R}^n$ 에서의 open set $A,\,B$ 에 대해 $g:A \rightarrow B$가 diffeomorphism of class $C^r$ 이라 하자. $D$가 compact subset of $A$ 이고 $E=g(D)$ 일 때 다음이 성립한다.

1. $g(\text{Int}(D)) = \text{Int}(E)$ and $g(\text{Bd}(D)) = \text{Bd}(E)$.
2. $D$가 rectifiable 이면 $E$도 rectifiable이다.

---

*Proof*  $g^{-1}$이 연속이므로 $g(\text{Int}(D))$ 는 open subset of $E$, i.e., $g(\text{Int}(D)) \subset \text{Int}(E)$. 마찬가지로 $g(\text{Ext}(D)\cap A)$는 open in $B$ and disjoint with $E = g(D)$, i.e., $g(\text{Ext}(D) \cap A) \subset \text{Ext}(D)$. $g$가 bijection 이므로 $ \text{Bd}(E) \subset  g(\text{Bd}(D))$  이다. 

더 자세히 말하면, Let $\mathbf{y} \in \text{Bd}(E)$ 라 하자. $E=g(D)$, $g$ is continuous and $D$ is compact 이므로 $E$는 compact. 따라서 $E$ is closed 이므로 $\mathbf{y} \in E$. Let $\mathbf{x} \in A$ s. t. $\mathbf{y} = g(\mathbf{x})$ . $\mathbf{x} \in \text{Int}(D)$ 이면 $\mathbf{y} \in \text{Int}(E)$ 이고 $\mathbf{x} \in \text{Ext}(D)$ 이면 $\mathbf{y} \in \text{Ext}(E)$  이어야 하므로 모순. 따라서 $\mathbf{x} \in \text{Bd}(D)$ 이며 $\text{Bd}(E) \subset g(\text{Bd}(D))$ 이다. 

위와 같은 이유료 $g$가 연속이므로 $g^{-1}(\text{Int}(E)) \subset \text{Int}(D)$ 이고 $\text{Bd}(D) \subset g^{-1}(\text{Bd}(E))$ 이다.  

$\text{Int}(E) = g\circ g^{-1} (\text{Int}(E)) \subset g(\text{Int}(D)) \subset \text{Int}(E)$  이므로 $g (\text{Int}(D)) = \text{Int}(E)$ 이다. (1. 증명) 

$g(\text{Bd}(D)) \subset g \circ g^{-1}(\text{Bd}(E)) \subset \text{Bd}(E) \subset g(\text{Bd}(D))$ 이므로 $\text{Bd}(E) = g(\text{Bd}(D))$ 이다. (2. 증명)

$D$가 rectifiable 이면 $E$도 rectifiable 임은 Lemma 1.에 의해 자명하다. $\square$.



#### Definition : Primitive Diffeomorphism

Diffeomorphism $h:A \subset \mathbb{R}^n \rightarrow B \subset{\mathbb{R}^n}$ 가 $h(\mathbf{x}) = (h_1 (\mathbf{x}),\ldots,\, h_n (\mathbf{x}))$  로 주어졌고 하자. 어떤 $i$ 에서 $h_i (\mathbf{x})= x_i$ 일 때 $h$는 $i$-th coordinate를 보존한다고 한다. $h$가 어떤 $i$-th coordinate를 보존한다면 $h$를 **primitive diffeomorphism** 이라 한다.



#### Theorem 3.

 $g:A \rightarrow B$가 diffeomorphism of open sets in $\mathbb{R}^n$ 이라 하자. $\mathbf{a} \in A$ 이면 어떤 neighborhood of $\mathbf{a}$, $U_{\mathbf{a}}$ 가 존재하여 $g|_{U_{\mathbf{a}}}$ 가 composite of primitive diffeomorphism $h_k \circ h_{k-1} \circ \cdots \circ h_1$  과 같다.

---

*Proof*  <u>(Step 1)</u> Linear algebra로 부터 다음 두 사실을 알고 있다.

1. Non-singular linear transformation $T:\mathbb{R}^n \rightarrow \mathbb{R}^n$ , $T(\mathbf{x}) = C \cdot \mathbf{x}$ 일 경우 행렬 $C$는 elementary row operation matrix의 product 이므로 $C$는 primitive diffeomorphism 의 composite 이다. 

2. $t :\mathbb{R}^n \rightarrow \mathbb{R}^n$ 이 translation $t(\mathbf{x}) = \mathbf{x} + \mathbf{c}$ 일 경우 $t_1(\mathbf{x}) = (x_1 + c_1, x_2,\ldots,\,x_n)$, $t_2 = (x_1, x_2+c_2,\ldots,\, x_n + c_n)$ 으로 정의하면 $t_1,\,t_2$ 는 primitive diffeomorphism 이며 $t = t_1 \circ t_2$. 

<u>(Step 2)</u> $\mathbf{a}=0$, $g(0)=0$, $Dg(0)=I_n$ 인 경우 $g$ 가 locally composite of two primitive diffeomorphism 임을 보이자. $g(\mathbf{x})=\sum_{i=1}^n g_i (\mathbf{x})\hat{e}_i$ 이며 $h (\mathbf{x})=\sum_{i=1}^{n-1}g_i(\mathbf{x}) \hat{e}_i+ x_n \hat{e}_n$ 이라 하자. $h(0)=0$ 이며 $Dh(0) = I_n$ 임을 알 수 있다.  Inverse function theorem에 의해 $h$는 $0$ 의 neighborhood $V_0,\,V_1$ 사이의 diffeomorphism임을 알 수 있다.

이제 $k(\mathbf{y}) = (y_1,\,\ldots,\,y_{n-1},\, g_n (h^{-1}(\mathbf{y})))$ 라 정의하자. $k(0)=0$ 이며 
$$
D k(\mathbf{y}) = \left[ \begin{array}{c} I_{n-1} \;\;\;\;\; 0 \\ D(g_n \circ h^{-1})(\mathbf{y}) &  \end{array} \right]
$$
이다. Chain rule에 의해 $D(g_n \circ h^{-1})(\mathbf{y}) = Dg_n(0) \cdot Dh^{-1}(0) = [0,\ldots,\,0,\,1]\cdot I_n = [0,\ldots,\,0,\,1]$ . 따라서 $Dk(0) = I_n$ 이며 $k$는 $0$ 의 neighborhood $W_1,\,W_2$ 사이의 diffeomorphism이다.  $k(W_1)=W_2$ , $W_0 = h^{-1} (W_1)$ 이라 하면 $k,\,h$ 는 primitive diffeomorphism  이며 $k \circ h = g|_{W_0}$ 임을 알 수 있다.
$$
W_0  \xrightarrow[]{\;\Large{h}\;}  W_1 \xrightarrow[]{\;\Large{k}\;} W_2
$$

<u>(Step 3)</u> 이제 일반적인 경우에 대해 생각해보자. 주어진 $g:A \rightarrow B$ 에 대해 $\mathbf{a}\in A$ 이고 $C=Dg(\mathbf{a})$ 라 하자. Diffeomorphism $t_1,\,t_2, T :\mathbb{R}^n \rightarrow \mathbb{R}^n$을 다음과 같이 정의한다.
$$
\begin{align*}
t_1 (\mathbf{x}) &= \mathbf{x}+ \mathbf{a} \;,\\
t_2 (\mathbf{x}) &= \mathbf{x} - g(\mathbf{a}) \;, \\
T(\mathbf{x})&= C^{-1}\cdot \mathbf{x}\;.
\end{align*}
$$
$\tilde{g}  = T \circ t_2 \circ g \circ t_1$이라 하면 $\tilde{g}$ 는 open sets $t_1^{-1} (A),\, T(t_2(B))$ 사이의 diffeomorphism 이다. 여기서 $\tilde{g}(0)=0$, $D\tilde{g}(0)=I_n$  임은 쉽게 보일 수 있다. Step 2에서 보았듯이  $0$의 어떤 neighborhood $W_0 \subset t_1^{-1}(A)$ 에 대해 $g|_{W_0}$ 는 two primitive diffeomorphism의 composite 이다. $W_2 = \tilde{g}(W_0)$, $A_0 = t_1 (W_0)$, $B_0 = t_2^{-1} T^{-1}(W_2)$ 라 하면, 
$$
A_0 \xrightarrow[]{\;\Large{t_1^{-1}}\;}W_0  \xrightarrow[]{\;\Large{\tilde{g}}\;}  W_2 \xrightarrow[]{\;\Large{T^{-1}}\;} T^{-1}(W_2) \xrightarrow[]{\;\Large{t_2^{-1}}\;} B_0\;.
$$
각각의 $t_1^{-1},\,t_2^{-1},\,T^{-1}$ 이 primitive transformation 이거나 primitive transformation으로 factorize 될 수 있으므로 증명 끝. $\square$



#### Definition

An open $A \subset \mathbb{R}^n$ 에 대해 $C^r$ class injective function $g:A \rightarrow \mathbb{R}^n$ 이 $\det Dg \ne 0$ for all $\mathbf{x}\in A$ 이면 $g$ 를 **change of variables** in $\mathbb{R}^n$ 이라 한다.



#### Theorem 4. (Change of Variables Theorem)

$g : A \rightarrow B$는 $\mathbb{R}^n$ 에서의 open sets에서의 diffeomorphism 이고 $f: B \rightarrow \mathbf{R}$ 은 연속함수라 하자. 이 때  $f$가 integrable over $B$  iff $(f \circ g) |\det Dg\,|$ is integrable 이며 이 경우
$$
\int_B f = \int_A (f \circ g) |\det Dg\,| 
$$
이다.

----

*(Proof)*  우선 $f$ is integrable $\implies$ $(f \circ g) |\det Dg\,|$ is integrable을 보인다(Lemma 6). 이후 $(f \circ g)|\det Dg\,|$ is integrable $\implies$ $f$ is integrable 을 보인다(Lemma 7).

  

#### Lemma 5.

 $g:A \subset \mathbb{R}^n \rightarrow B$, $h : B \subset \mathbb{R}^n \rightarrow \mathbb{R}^n$이 differentiable 일 때 $\det(D(h \circ g)) (\mathbf{x})= \det(Dh(g(\mathbf{x}))) \cdot \det(Dg)(\mathbf{x})$ 이다. 따라서  $|\det(D(h \circ g)) |= |\det(Dh)\circ g\,| \cdot |\det(Dg)\,|$ 이다. 

----

*Proof is trivial*



#### Lemma 6. 

$g:A \rightarrow B$가 open sets $A,\,B$ in $\mathbb{R}^n$에 대한 diffeomorphism 이라 하자. $B$에서 integrable한  연속 함수 $f:B \rightarrow \mathbb{R}$ 에 대해 $(f \circ g)| \det Dg|$ 는 integrable 하며,
$$
\int_B f = \int_A (f \circ g)|\det Dg|
$$
이다.

---

*Proof*   <u>(Step 1)</u>  임의의 $\mathbf{x} \in A$에 대해 위의 Lemma가 성립하는  $\mathbf{x}$의 neighborhood $U \subset A$가 존재함을 가정하자.   즉 일단 locally 성립하면 globally 성립함을 보인다. 그리고 난 후 이러한 $U$가 항상 존재함을 induction을 통해 보이기로 하자.

<u>(Step 2)</u>  Collection of open sets $\{ U_{\alpha}\}$ s. t. $\bigcup_{\alpha} U_{\alpha} = A$ 이고, $V_{\alpha} = g(U_{\alpha})$ 이면 $B = \bigcup_{\alpha} V_{\alpha}$ 이다. $B$에 대한 partition of unity $\{ \phi_i\}$ having compact support, that is dominated by $\{ V_{\alpha} \}$ 를 생각하자. 우리는 $\{ \phi_i \circ g\}$ 가 partition of unity on $A$ having comact support 임을 보일것이다. 

1. $\phi_i (g(\mathbf{x})) \ge 0$ for all $\mathbf{x} \in A$ 이다. 

2. $T_i= \text{Supp } (\phi_i)$ 라 하자. $g(T_i)$ 는 compact 이며 $\phi_i \circ g (\mathbf{x}) = 0$ if $\mathbf{x} \not\in g^{-1}(T_i)$ 이다. 따라서 $S_i = \text{Supp } (\phi_i \circ g) \subset g^{-1}(T_i)$ 이며 $S_i$는 compact set  이다.
3. $\mathbf{x} \in A$, $\mathbf{y} = g(\mathbf{x}) $ 라 하자. $\mathbf{y}$ 는 finitly many $T_i$ 와 intersect 하는 neighborhood $N_\mathbf{y}$ 를 가지며 $g^{-1}(N_{\mathbf{y}})$ 는 $\mathbf{x}$의 neighborhood로 이 $T_i$에 상응하는 $S_i$와만 intersect 한다. 
4. $\sum \phi_i (g(\mathbf{x})) = \sum \phi_i (\mathbf{y}) = 1$. 

따라서 $\{ \phi_i \circ g\}$는 partition of unity on $A$ 이다. 

이제 $f:B \rightarrow \mathbb{R}$ 이 연속함수이고 $f$가 $B$에서 integrable 이라 하자. 우리는 $\int_B f = \sum_{i=1}^{\infty} \left[ \int_B \phi_i f\right]$ 임을 알고 있다.  Given $i$에 대해 $T_i \subset V_{\alpha}$ 가 되도록 $\alpha$를 선택하자. $\phi_i f$는 $B$에서 연속이므로 
$$
\int_B \phi_i f = \int_{T_i} \phi_i f = \int_{V_{\alpha}} \phi_i f\;,
$$

이다. $g: U_{\alpha}\rightarrow V_{\alpha}$ 를 생각하면 다음이 성립한다.
$$
\int_{V_{\alpha}} \phi_i f  = \int_{U_{\alpha}} (\phi_i \circ g)(f \circ g)|\det Dg|\ \;.
$$
우변의 적분은 $S_i$ 밖에서 $0$ 이므로 다음이 성립한다.
$$
\begin{equation}
\int_B \phi_i f = \int_A (\phi_i \circ g)(f \circ g)|\det Dg\,|\;,\; \text{and} \\
\int_B f = \sum_{i=1}^{\infty} \left[ \int_B \phi_i f\right] = \sum_{i=1}^{\infty} \left[ \int_A (\phi_i \circ g)(f \circ g)|\det Dg\,| \,\right]\;.
\end{equation}
$$
$\phi_i \circ g$가 $A$의 partition of unity 이고 $|f|$가 integrable 이므로 $(f\circ g)|\det Dg|$ 도 integrable 하다. 따라서 
$$
\int_B f = \int_A (f \circ g)|\det Dg\,|
$$
이다. 

<u>*(Step 3)*</u> 임의의 $\mathbf{x} \in A$에 대해 위의 Lemma가 성립하는  $\mathbf{x}$의 neighborhood $U \subset A$가 존재함을 induction을 통해 보인다. 일단 $n=1$ 일 때 즉 $\mathbb{R}^1$에서 보이자. $A,\,B$ 가 open in $\mathbb{R}$ 이라 하자. $x \in A$에 대해 $I$는 $x \in \text{int}(I)$ 인 closed interval 이며 $J = g(I)$ 라 하자. $g$가 diffeomorphism 이므로 $g(x) \in \text{Int}(J)$ 이다. 

이제 $\text{int}(J)$에서 정의된 연속함수 $f$에 대해 $\int_{\text {Int}(J)} f = \int_{\text{Int}(I)} (f \circ g)|g'|$ 임을 보이면 되는데 $I,\,J$가 closed interval 이므로 자명하다.

<u>*(Step 4)*</u> 이제 $n-1$일때 성립함을 가정하고 $n$에서 성립함을 보이자. Lemma 4를 생각하면 우리는 primitive diffeomorphism에서 성립함을 보이면 된다. $h:U \rightarrow V$를 $\mathbb{R}^n$의  open set $U,\, V$에서 정의된 primitive diffeomorphism 이라 하자. 편의를 위해 $h$를 마지막 components를 보존하는 primitive diffeomorphism 이라고 가정한다. 

$\mathbf{p} \in U,\,\mathbf{q} = h(\mathbf{p})$ 이며 $Q$는 $\mathbf{q}$를 내부에 포함하는 $V$의 subset 이라 하고 $S = h^{-1}(Q)$라 하자. $h$는 $\text{Int}(S)$ 와 $\text{Int}(Q)$ 사이의 diffeomorphism이다. 이제 $h$와 임의의 연속함수 $f:\text{Int}(Q) \rightarrow \mathbb{R}$ whose support is compact subset of $\text{Int}(Q)$ 에 대해 lemma가 성립함을 보이자. 

$(f \circ h) | \det Dh \,|$ 가 compact subset of $\text{Int} (S)$ 이므로 $(f \circ h) |\det Dh\,|$ 는 integrable over $\text{Int}(S) $ 이다. 이제 우리는 다음을 보여야 한다.
$$
\int_{\text{Int}(Q)} f = \int_{\text{Int}(S)} (f \circ h) | \det Dh\,|\;.
$$
이제 $f$를 확장시킨 $f_e :\mathbb{R}^n \rightarrow \mathbb{R}$ ,  $F:\mathbb{R}^n \rightarrow \mathbb{R}$ 을 다음과 같이 정의하면 $f_e$와 $F$는 $\mathbb{R}^n$에서 연속이다.
$$
\begin{align*}
f_e(\mathbf{x}) & = \left\{ \begin{array}{ll} f(\mathbf{x}) & \text{if }\mathbf{x}\in \text{Int}(Q)\;, \\
0 & \text{otherwise.} \end{array} \right. \\
\\
F(\mathbf{x}) &= \left\{ \begin{array}{ll} (f_e \circ h) |\det Dh\,| & \text{if }\mathbf{x} \in \text{Int}(Q)\;, \\ 0 & \text{oterwise}\;. \end{array} \right.
\end{align*}
$$

$Q$는 closed rectangle in $\mathbb{R}^n$ 이므로 $\mathbb{R}^{n-1}$ 에서의 closed rectengle $D$와 closed interval $I$ 에 대해 $Q=D\times I$로 쓸 수 있다. $S$가 compact 이므로 $\mathbb{R}^{n-1}\times 0$으로의 projection $S_0$ 도 compact 하며 어떤 $\mathbb{R}^{n-1}$의 rectangle $E$ 에 대해 $S_0 \subset E \times 0$ 이다. $h$가 last coordinate를 preserve 하는 primitive diffeomorphism 이므로 $S \subset E \times I$ 이다. 

$F(\mathbf{x})=0$ when $\mathbf{x} \not\in S$ 이므로 $\int_Q f = \int_{E \times I}F$ 이다. Fubini's theorem 에 의해 다음과 같다.
$$
\int_{t \in I} \int_{\mathbf{y} \in D} f(\mathbf{y},\,t) = \int_{t \in I} \int_{\mathbf{x} \in E} F(\mathbf{x},\,t) \;.
$$
이제 $\text{Int}(D \times I)$ 와 $\text{Int}(E \times I)$ 에 대해 위의 등식이성립함을 보이면 된다.

앞의 $\mathbb{R}^n$에서의 open $U,\,V$와 $\mathbb{R}^{n-1}\times t$ 와의 각각의 intersections는 $\mathbb{R}^{n-1}$ 에서의 open $U_t,\,V_t$에 대해 $U_t \times t,\,V_t\times t$ 로 쓸 수 있다. 비슷하게 $S$ 와 $\mathbb{R}^{n-1} \times t$ 와의 intersection도 $S_t \times t$ for some compact set $S_t$ in $\mathbb{R}^{n-1}$로 쓸 수 있다. $F$가 $S$ 밖에서 $0$ 이므로 $\int_{\mathbf{y}\in D} f (\mathbf{y},\,t) = \int_{\mathbf{x}\in S_t} F(\mathbf{x},\,t)$ 이며 이는 아래와 같다.
$$
\int_{\mathbf{y} \in V_t} f(\mathbf{y},\,t)  = \int_{\mathbf{x} \in U_t} F(\mathbf{x},\,t)\;.
$$


앞서 가정한 diffeomorphism $h:U \rightarrow V$는 $h(\mathbf{x},\,t) = (k(\mathbf{x},\,t),\,t)$ for some $k:U \rightarrow \mathbb{R}^{n-1}$ of $C^ 1$ class function 이다. $\det Dh = \det \partial k/\partial \mathbf{x}$ 이며 non zero for $\mathbf{x} \in U$ 이므로 map $\sigma : \mathbf{x} \rightarrow k(\mathbf{x},\,t)$ for  fixed $t$ 는 $U_t$와 $V_t$ 사이의 diffeomorphism이다. 

Induction의 가정을 fixed $t$ 에 대해 적용하면
$$
\int_{\mathbf{y} \in V_t} f(\mathbf{y},\,t) = \int_{\mathbf{x} \in U_t} f(k(\mathbf{x},\,t),\,t) | \det \partial k/\partial \mathbf{x}\,| 
$$
이다. $\;\;\square$ 

