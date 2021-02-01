Rank Theorem
===



#### Notation

- $\mathfrak{M}_{m,\,n}(\mathbb{F})$ : Field $\mathbb{F}$ 에서 정의된 $m\times n$ 행렬의 집합.
- $\mathcal{L}(V,\,W)$ : Vector space $V,\,W$ 가 있을 때 $V \to W$ 선형사상의 집합.
- $A\in \mathfrak{M}_{m,\,n}(\mathbb{F})$ 일 때 $A$ 의 $i$-th column 을 $[A]^i$ 로, $j$-th row 를 $[A]_j$ 로 표현한다. 
- $S=\{v_1,\ldots,\,v_n\}\subseteq V$ 일 때 $\langle S\rangle$ 은 $S$ 의 원소중 유한개의 원소들의 모든 선형결합의 집합이다.
- Vector space $V$ 에 대해 $U \subseteq V$ 이고 $U$ 가 vector space 이면 $U$ 를 $V$ 의 subspace 라 하고 $U \le V$ 라 쓴다.
- $A\in \mathfrak{M}_{m,\,n}(\mathbb{F})$ 일 때 $\left\langle \left\{[A]^1,\ldots,\,[A]^n \right\}\right\rangle$ 을 $A$ 의 column space 라 하며 $\mathbb{F}^m$ 의 부분공간이다. 또한 $\left\langle \left\{  [A]_1,\ldots,\,[A]_m\right\}\right\rangle$ 을 $A$ 의 row space 라 하며 $\mathbb{F}^n$ 의 부분공간이다. $\dim(\left\langle \left\{[A]^1,\ldots,\,[A]^n \right\}\right\rangle)$ 를 $A$ 의 column rank 라 하며 $\dim (\left\langle \left\{  [A]_1,\ldots,\,[A]_m\right\}\right\rangle) $ 을 $A$ 의 row rank 라 한다.



#### 1. Lemma

$A\in \mathfrak{M}_{m,\,n}(\mathbb{F})$ 에 대해 $L_A \in \mathcal{L}(\mathbb{F}^n,\, \mathbb{F}^m)$ 을 $L_A(X) = AX$ 로 정의하면 $A$ 의 column space는 $\operatorname{im}L_A$ 와 같다.  따라서, $\dim (\operatorname{im} L_A)=[\text{column rank of }L_A]$ 이다.  

---

$X=(x_1,\ldots,\,x_n)^t\in \mathbb{F}^n$ 에 대해 $AX=\sum_{i=1}^n x_i [A]^i$. 



####2. Rank Theorem 

$A \in \mathfrak{M}_{m,\,n}(\mathbb{F})$ 이면 $A$ 의 row rank 와 column rank 는 같다. 

---

Dimension theorem 으로 부터 $\dim (\mathbb{F}^n)=n=\dim(\ker (L_A))+\dim \operatorname{im L_A}=\dim(\ker (L_A))+[\text{column rank of }L_A] $ 이다. 

 

