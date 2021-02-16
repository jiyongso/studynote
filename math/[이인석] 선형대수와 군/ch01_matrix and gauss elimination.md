제 1 장 행렬과 가우스 소거법
===



## 1.1 Matrix



#### Notations

- 행렬 $A$ 의 $i$ 번째 행(row)를 $[A]_i$ 라 쓰겠다.
- 행렬 $A$ 의 $j$ 번째 열(column)을 $[A]^j$ 라 쓰겠다.
- $n\times n$ 항등행렬을 $I_n$ 으로 쓰겠다.
- $\mathbb{F}$ 는 field, $\R$ 은 실수의 집합, $\C$ 는 복소수의 집합, $\N$ 은 자연수의 집합($0$ 을 포함한다), $\Z$ 는 정수의 집합, $\Z_{+}$ 는 양의 정수의 집합, $\Z_{-}$ 는 음의 정수의 집합, $\Q$ 는 유리수의 집합을 의미한다.
- $\mathfrak {M}_{m,\,n}(\mathbb{F})$ 는 field $\mathbb{F}$ 위에서 정의된 $m \times n$ 행렬의 집합을 의미한다.





<b>연습문제 1.1.6</b>. $A,\,B$ 가 nilpotent matrix 이고 $AB=BA$ 이면 $(A+B)$ 도 nilpotent 임을 보여라.

---

(1) $r,\,s$ 는 각각 $A^r=0,\, B^s=0$ 이 되도록 하는 가장 작은 양의 정수라 하자. $r<s$ 라 가정해도 no loss of generality.

(2) $(A+B)^{r+s} = \sum_{k=0}^{r+s} A^kB^{r+s-k} = \sum_{k=0}^{r-1} A^kB^{r+s-k}$ 인데 $r+s-k >s$ 이므로 $(A+B)^{r+s}=0$. 



<b>연습문제 1.1.7.</b> $A=(a_{ij})$ 가 square matrix 라 하자. Upper-triangular matrix, strictly upper-triangular matrix는 알것이고, $A$ 가 upper triangular matrix 이며 $a_{ii}=1$ for all $i$ 이면 $A$ 를 unipotent triangular matrix라 한다.

(가) $A,\,B \in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 가 upper triangular 이면 $AB$ 도 upper triangular 임을 보이시오. $AB$ 의 대각성분을 묘사하라.

(나) $A,\,B\in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 가 strictly upper-triangular matrix 이면 $AB$ 도 그러함을 보이시오. $A,\,B$ 가 unipotent upper-triangular 이면 $AB$ 도 그러함을 보이시오.

(다) $A\in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 가 strictly upper triangular 이면 $A^n=0$ 임을 보이시오.

---

(가) Let $C=(c_{ij})=AB$. Then, $\displaystyle c_{ij}=\sum_{k=1}^n a_{ik}b_{kj}$. $a_{ik}=0$ if $i>k$ and $b_{kj}=0$ if $k>j$. $i>j$ 라 가정하자. $a_{ik}b_{jk}\ne 0$ 이려면 $k\ge i$ 이고 $k\le j$ 이어야 하는데 이는 $i>j$ 조건에 위배. 따라서 $c_{ij}=0$ if $i>j$. 따라서 $AB$ 는 uppertriangular.

$c_{ii}=\displaystyle \sum_{k=1}^n a_{ik}b_{ki}$ 이며 non-zero term은 $k=i$ 일 때 밖에 없다. 따라서 $c_{ii}=a_{ii}b_{ii}$. 

(나) (가)에 의해 자명하다.

(다) $\displaystyle (A^2)_{ij}=\sum_{k=1}^n a_{ik}a_{kj}$. Non-zero term은 $i<k<j$  이므로 $(A^2)_{ij}=0$ if $i+1\ge j$ . $(A^m)_{ij}=0$ If $i+{m-1}\ge j$ 임을 증명하자. $m=1$ 일 때는 strictly upper triangular matrix의 정의이므로 참이다. $m$ 일 때 참이라 가정하자.

$(A^{m+1})_{ij}=\sum_{k=1}^n (A^m)_{ik}a_{kj}$ 이며 nonzero term은 $i+m-1<k<j$ 이므로 $j\le i+m$ 이면 $(A^m)_{ij}=0$ 이다. 



<b>연습문제 1.1.8.</b> $A,\,B \in \mathfrak{M}_{m,\,n}(\mathbb{F})$, $C\in \mathfrak{M}_{n,\,r}(\mathbb{F})$ 일 때 다음을 보여라.

(가) $(A+B)^t=A^t+B^t$.

(나) $(cA)^t = cA^t$.

(다) $(A^t)^t=A$.

(라) $(AC)^t =C^tA^t$.

---

(가) $[(A+B)^t]_{ij}=(A+B)_{ji}=A_{ji}+B_{ji}=(A^t)_{ij}+(B^t)_{ij}$ .

(나) $[(cA)^t]_{ij}=(cA)_{ji}=cA_{ji}=c[A^t]_{ij}$. 

(다) $[(A^t)^t]_{ij}=(A^t)_{ji}=A^{ij}$. 

(라) $[(AC)^t]_{ij}=(AC)_{ji}=\displaystyle \sum_{k=1}^n A_{jk}C_{ki}=\sum_{k=1}^n (C^t)_{ik}(A^t)_{kj}=(C^tA^t)_{ij}$ .



<b>연습문제 1.1.11.</b> $(n\times n)$-행렬 $A,\,B$ 와 $c\in \mathbb{F}$ 에 대해 다음이 성립함을 보열.

(가) $\operatorname{tr} (A+B)=\operatorname{tr} (A)+ \operatorname{tr} (B)$.

(나) $\operatorname{tr}(cA)=c\cdot \operatorname{tr}(A)$.

(다) $\operatorname{tr}(A^t)=\operatorname{tr}(A)$.

(라) $\operatorname{tr}(AB)=\operatorname{tr}(BA)$. 

---

(가) $\operatorname{tr}(A+B)=\displaystyle \sum_{i=1}^n (A+B)_{ii}=\sum_{i=1}^n (A_{ii}+B_{ii}) = \operatorname{tr}(A)+\operatorname{tr}(B)$. 

(나) $\operatorname{tr}(cA)=\displaystyle \sum_{i=1}^n (cA)_{ii}=c\sum_{i=1}A_{ii}=c\cdot\operatorname{tr}(A)$. 

(다) $\operatorname{tr}(A^t)=\displaystyle \sum_{i=1}^n (A^t)_{ii}=\sum_{i=1}^n A_{ii}=\operatorname{tr}(A)$.

(라) $\displaystyle \operatorname{tr}(AB)= \sum_{i=1}^n (AB)_{ii}= \sum_{i=1}^n \sum_{k=1}^n A_{ik}B_{ki}=\sum_{k=1}^n \left(\sum_{i=1}^n B_{ki}A_{ik}\right)=\sum_{k=1}^n(BA)_{kk}=\operatorname{tr}(BA)$.



<b>연습문제 1.1.12</b> $AB-BA=I$ 인 $(n\times n)$-행렬 $A,\,B$ 는 존재하는가?

---

$\operatorname{tr}(AB-BA)=0$ 임은 연습문제 1.1.11로부터 쉽게 알 수 있다. 그런데 $\operatorname{I}=n\ne 0$ 이므로 $AB-BA=I$ 인 $(n\times n)$-행렬 $A,\,B$ 는 존재하지 않는다.



<b>연습문제 1.1.13. </b> $A=\begin{bmatrix} a & b \\ c & d \end{bmatrix}$ 일 때 $A^2-(a+d)A+(ad-bc)I=0$ 임을 증명하여라.

---

$$
A^2-(a+d)A+(ad-bc)I =\begin{bmatrix} a^2+bc & ab+bd \\ ac+cd & ad+d^2\end{bmatrix} - \begin{bmatrix} a^2 +ad & ab+bd \\ ac+cd & ad+d^2\end{bmatrix}+\begin{bmatrix} ad-bc & 0 \\ 0 & ad-bc\end{bmatrix}=\begin{bmatrix}0 & 0 \\ 0 & 0 \end{bmatrix}
$$



<b>연습문제 1.1.16.</b> 가역행렬 $A,\,B \in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 와 scalar $0 \ne c \in \mathbb{F}$ 에 대해 다음이 성립함을 보이시오.

(가)  $I$ 는 가역이고 $I^{-1}=I$.

(나) $cA$ 도 가역이고 $(cA)^{-1}=\dfrac{1}{c}A^{-1}$.

(다) $AB$ 도 가역이고 $(AB)^{-1}=B^{-1}A^{-1}$. 

(라) $A^{-1}$ 도 가역이고 $(A^{-1})^{-1}=A$. 

(마) $A^{t}$ 도 가역이고 $(A^t)^{-1}=(A^{-1})^t$. 

---

먼저 $A,\,B,\,C\in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 에 대해 $AB=CA=I$ 이면 $B=C$ 임을 보이자.  $B=(CA)B=C(AB)=C$. 즉 정방행렬에 대한 역행렬은 왼쪽이나 오른쪽이나 하나만 보이면 된다. 

(가) $II=I$. 

(나) $(cA)(\dfrac{1}{c}A^{-1})=I$. 

(다) $(AB)(B^{-1}A^{-1})=(B^{-1}A^{-1})AB=I$.

(라) $(A^{-1})A=A(A^{-1})=I$.

(마) $[A^t(A^{-1})^t]_{ij}=\sum_{k}(A^t)_{ik}((A^{-1})^t)_{kj}=\sum_k A_{ki}(A^{-1})_{jk}=(A^{-1}A)_{ji}=\delta_{ij}$.  



<b>연습문제 1.1.17.</b> $A,\,B\in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 일 때,

(가) $A$ 가 invertible symmetric matrix 이면 $A^{-1}$ 도 symmetric 인가?

(나) $A,\,B$ 가 symmetric 이면 $AB$ 도 symmmetric 인가? 만약 $AB=BA$ 이면?

(다) $A,\,B$ 가 invertible 이면 $(A+B)$ 도 invertible 인가?

---

(가) $(AA^{-1})^t=(A^{-1})^tA^t=I$ 이다. $A^t=A$ 이므로 $(A^{-1})^t=A^{-1}$. 따라서 $A^{-1}$ 도 symmetric.

(나) $(AB)_{ij}=\sum_k A_{ik}B_{kj}=\sum_{k} A_{ki}B_{jk}=(BA)_{ji}$ 이므로 $A,\,B$ 가 symmetric 이고 $AB=BA$ 이면 $AB$ 가 symmetric 이다. $A=\begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix},\, B=\begin{bmatrix} 1 & 0 \\ 0 & 2\end{bmatrix}$ 라 하면 $A,\,B$ 는 symmetric 이다. 그러나 $AB=\begin{bmatrix} 0 & 2 \\ 1 & 2\end{bmatrix}$ 로 symmetric 하지 않다. 

(다) No!. see $A=\begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix}$ and $B=\begin{bmatrix} -1 & 0 \\ 0 & 1\end{bmatrix}$ . $A^{-1}=A$ and $B^{-1}=B$. But $A+B=0$ is not invertible.



<b> 연습문제 1.1.18.</b> $\mathbf{O}(n)=\{A\in \mathfrak{M}_{n,\,n}(\mathbb{R}) : A\text{ is invertible and }A^{-1}=A^t\}$ 로 정의할 때, 다음을 보여라.

(가) $I_n \in \mathbf{O}(n)$.

(나) $A,\,B \in \mathbf{O}(n)$ 이면, $AB\in \mathbf{O}(n)$.

(다) $A\in \mathbf{O}(n)$ 이면, $A^{-1}\in \mathbf{O}(n)$.

(라) $A\in \mathbf{O}(n)$ 이면 $A^{t} \in\mathbf{O}(n)$. 

---

(가) $I_n = {I_n}^{-1}=(I_n)^t$ .

(나) $(AB)^{-1}=B^{-1}A^{-1}=B^tA^t=(AB)^t$. 

(다) $(A^{-1})^{-1}=(A^t)^{-1}=(A^{-1})^t$. (연습문제 1.1.16 (마) 참고)

(라) $A^t=A^{-1}\in \mathbf{O}(n)$ (다 참고)



<b>연습문제 1.1.19</b> $A,\,U \in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 이고 $U$ 가 가역이면
$$
\operatorname{tr} (U^{-1}AU)=\operatorname{tr}(A)
$$
임을 보여라.

---

연습문제 1.1.11에서 $\operatorname{tr}(AB)=\operatorname{tr}(BA)$ 임을 보였다. 
$$
\operatorname{tr}(U^{-1}AU)=\operatorname{tr}(U(U^{-1}A))=\operatorname{tr}((UU^{-1})A)=\operatorname{tr}(A)\;.
$$


<b>연습문제 1.1.20 </b> (가) $A,\,U \in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 이고 $U$ 가 가역일 때 $m \ge 0$ 이면,
$$
(U^{-1}AU)^m = U^{-1}A^mU 
$$
임을 보여라.

(나) $A,\,U \in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 이고 $U$ 가 가역일 때, $A$ 가 nilpotent 이면 $U^{-1}AU$ 도 nilpotent 임을 보여라.

(다) 행렬 $A,\,U,\,D$ 가
$$
A=\begin{bmatrix} 2 & 1 \\ 3 & 4\end{bmatrix},\quad U=\begin{bmatrix}1 & 1 \\ -1 & 3\end{bmatrix},\quad D=\begin{bmatrix} 1 & 0 \\ 0 & 5 \end{bmatrix}
$$
일 때 $U^{-1}AU=D$ 인 것을 확인하고 $A^{100}$ 을 구하라. 또 $B^3=A$ 인 $B$ 를 (하나만) 구하라.

---

(가) 수학적 귀납법을 사용한다. $A^0=I_n$ 이므로 $m=0$ 일 때 성립. $m$ 일 때 성립함을 가정하고,
$$
(U^{-1}AU)^{m+1}=(U^{-1}AU)^m (U^{-1}AU)=U^{-1}A^mU U^{-1}AU = U^{-1}A^{m+1}U
$$
이므로 $m\ge 0$ 일 때 성립한다.

(나) $A^r=0\implies (U^{-1}AU)^r=U^{-1}A^rU=0$. 

(다) $U^{-1}=\dfrac{1}{4}\begin{bmatrix} 3 & -1 \\ 1 & 1 \end{bmatrix}$ 이므로 
$$
U^{-1}AU=\dfrac{1}{4} \begin{bmatrix} 3 & -1 \\ 1 &1\end{bmatrix} \cdot\begin{bmatrix} 2 & 1 \\ 3 & 4 \end{bmatrix} \cdot \begin{bmatrix} 1 & 1 \\ -1 & 3 \end{bmatrix}=\dfrac{1}{4} \begin{bmatrix} 3 & -1 \\5 & 5 \end{bmatrix} \cdot\begin{bmatrix} 1 & 1 \\ -1 & 3 \end{bmatrix} = \dfrac{1}{4}\begin{bmatrix} 4 & 0 \\ 0 & 20\end{bmatrix}=D
$$
이다. $(U^{-1})AU)^{100}=U^{-1}A^{100}U=D^{100}$ 이며 $D^m = \begin{bmatrix} 1 & 0 \\ 0 & 5^m\end{bmatrix}$ 이므로,
$$
\begin{align*}
A^{100}=UD^{100}U^{-1}&= \dfrac{1}{4}\begin{bmatrix} 1 & 1 \\ -1 & 3 \end{bmatrix}\cdot \begin{bmatrix} 1 & 0 \\ 0 & 5^{100}\end{bmatrix}\cdot \begin{bmatrix} 3 & -1 \\ 1 & 1 \end{bmatrix}=\dfrac{1}{4} \begin{bmatrix}1 & 5^{100} \\-1 & 3\times 5^{100} \end{bmatrix}\cdot\begin{bmatrix} 3 & -1 \\ 1 & 1 \end{bmatrix} \\
&= \dfrac{1}{4} \begin{bmatrix} 3+5^{100} & -1+5^{100} \\ -3+3\times 5^{100} & 1+3\times 5^{100}\end{bmatrix}

\end{align*}
$$
$F=\begin{bmatrix}1 & 0 \\ 0 &\sqrt[3]{5}\end{bmatrix}$ 라 하면 $F^3=D$ 이다. $(UFU^{-1})^3=UF^3U^{-1}=UDU^{-1}=A$ 이므로 $B=UFU^{-1}$ 이다.



<b>연습문제 1.1.21</b> $A_i \in \mathfrak{M}_{n_i,\,n_i}(\mathbb{F})$ 일 때 (단, $i=1,\ldots,\,k$), $n_1+\cdots+n_k=n$ 이라고 놓자. 다음
$$
A=\operatorname{diag} (A_1,\ldots,)=\begin{bmatrix} A_1 & & & & &\\ & A_2 & & & 0 & \\ & & \cdot & & & \\ & & & \cdot & & \\ & 0 & & & \cdot & \\ & & & & & A_k  \end{bmatrix} \in \mathfrak{M}_{n,\,n}(\mathbb{F})
$$
형태의 행렬을 ($A_i$ 를 $i$-th diagonal block 으로 갖는) **block diagonam matrix** 라고 부른다. $A_i,\,B_i \in \mathfrak{M}_{n_i,\,n_i}(\mathbb{F})$ 일 때, 다음을 보여라.

(가) $\operatorname{diag} (A_1,\ldots,\,A_k)\cdot \operatorname{diag}(B_1,\ldots,\,B_k)=\operatorname{diag}(A_1B_1,\ldots,\,A_kB_k)$ .

(나) $A_i$ 가 가역이면 $(\operatorname{diag}(A_1,\ldots,\,A_k))^{-1}=\operatorname{diag}(A_1^{-1},\ldots,\,A_k^{-1})$ . 

----

(가) Let $K=\operatorname{diag} (A_1,\ldots,\,A_k)\cdot \operatorname{diag}(B_1,\ldots,\,B_k)$, $s_i = \sum_{j=1}^{i-1} n_j$.  그렇다면 $A_i$ 는 행렬 $K$ 의 $s_i+1$ 행/열 부터 $s_{i+1}$ 행/열 까지를 차지한다. $A=(a_{ij}),\, B=(b_{ij})$ 라 하자.  $a_{ij}=0$ if $i,\, j \le s_i$ or $i,\,j >s_{i+1}$ 이므로 $(AB)_{lm}=\sum_{k=1}^n a_{lk}b_{km}$ 에 있어 $l$ 이 어떤 $i$ 에 대해 $s_i +1 \le l \le s_{i+1}$ 이라면 $k$도 $s_i+1\le l\le s_{i+1}$ 의 범위에서만  $a_{lk}$ 가 nonzero 이다. 마찬가지로 $m$도 $s_i +1 \le l \le s_{i+1}$ 범위에서만 nonzero 이므로 $(AB)_{lm}$ 은 $l$ 과 $m$ 이 모드 특정한 $i$ 에 대해 $s_i+1 \le l,\,m \le s_{i+1}$ 일 때만 nonzero 이며,
$$
(AB)_{lm}=\sum_{k={s_i+1}}^{s_{i+1}} a_{lk}b_{km}=A_iB_i
$$
이다. 또한 이로부터 $(AB)$ 역시 block diagonal matrix 이며 $K=\operatorname{diag}(A_1B_1,\ldots,\,A_kB_k)$ 임을 알 수 있다.

(나) (가) 로 부터 자명하다.



<b>연습문제  1.1.23</b> $A,\,B \in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 일 때 $AB=0$ 이면 $BA=0$ 인가?

---

Let $A=\begin{bmatrix} 1 & 1 \\ 1 & 1\end{bmatrix}$ and $B=\begin{bmatrix} 0 & -1 \\ 0 & 1\end{bmatrix}$. $AB=0$ and $BA=\begin{bmatrix} -1 & -1 \\ 1 & 1\end{bmatrix}$.



## 2. Gaussian Elimination



<b>연습문제 1.2.1</b> 연립방정식 ($**$) $AX=B$ 에 elementary row operation 을 유한 번 시행하여 연립방정식 $A'X=B'=(b'_1,\ldots,\,b'_m)^t$ 를 얻었다고 하자. 행렬 $A'$ 이 다음과 같을 때 연립방정식 ($**$) $AX=B$ 의 해집합을 구하여라.

(가) $A'=I$.

(나) $A'=\begin{bmatrix} 1 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix}$. 

(다) $A' = \begin{bmatrix} 1 & 2 & 0 \\ 0 & 0 & 1 \end{bmatrix}$.

(라) $A'=\begin{bmatrix} 1 & 0 & 2 \\ 0 & 1 & 3\\ 0 & 0 & 0 \end{bmatrix}$

(마) $A'=\begin{bmatrix} 1 & 1 & 0 & 2 & 0 & 0 & -2 \\ 0 & 0 & 1 & 3 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & 1 & 4 \\ 0 & 0 & 0 & 0 & 0 & 0& 0\end{bmatrix}$.

---

$AX=B$ 에 elementary row opertation 을 유한 번 시행하여 $A'X=B'$ 을 얻었을 때 연립방정식의 해잡합은 변하지 않는다. 따라서,

(가) $X=B'$ 

(나) $X=(x_1,\,x_2,\,x_3)^t$ 라 하면,  $x_1=b_1',\, x_3=b_2'$ 이며 $x_2$ 는 임의의 $\mathbb{F}$ 이다.

(다) $X=(x_1,\,x_2,\,x_3)^t$ 라 하면, $x_1+2x_2=b'_1$ 을 만족하는 모든 $x_1,\,x_2$ 이며 $x_3=b'_2$ 이다.

(라) $X=(x_1,\,x_2,\,x_3)^t$ 라 하면 $x_1+2x_3=b_1'$, $x_2+3x_3=b'_2$ 를 만족하는 $x_1,\,x_2,\,x_3$ 의 값에 의해 결정된다. 만약 $b_3'\ne 0$ 이면 만족하는 해의 집합은 공집합이다. 

(마)$X=(x_1,\ldots,\,x_7)^t$ 라 하면 $x_1+x_2+2x_4-2x_7=b_1'$, $x_3+3x_4=b'_2$, $x_6+4x_7=b'_3$ 를 만족하는 모든 $x_1,\ldots,\,x_7$ 에 의해 결정되며 $b'_4\ne 0$ 이면 만족하는 해의 집합은 공집합이다.



<b>연습문제 1.2.4</b> (가) $(4 \times 7)$-행렬 $A$ 가
$$
A=\begin{bmatrix} 4 & 4 & 9 & 35 & 0 & 1 & -4 \\ -1 & -1 & -2 & -8 & 0 & 1 & 6 \\ -3 & -3 & -7 & -27 & 0 & -1 & 2 \\ 1 & 1 & 2 & 8 & 0 & 1 & 2  \end{bmatrix}
$$
일 때, $A$ 를 row-reduced echelon form으로 바꾸어 보라.

(나) 그럴듯한 행렬을 세 개만 임의로 택해 행 간소 사다리꼴로 바꾸어 보라.

---

(가) $[A]_1=[A]_1+[A]_3$, $A=\begin{bmatrix} 1 & 1 & 2 & 8 & 0 & 0 & -2 \\-1 & -1 & -2 & -8 & 0 & 1 & 6 \\ -3 & -3 & -7 & -27 & 0 & -1 & 2 \\ 1 & 1 & 2 & 8 & 0 & 1 & 2  \end{bmatrix}$ .

$[A]_2 = [A]_2+[A]_1$, $A=\begin{bmatrix} 1 & 1 & 2 & 8 & 0 & 0 & -2 \\0 & 0 & 0 & 0 & 0 & 1 & 4 \\ -3 & -3 & -7 & -27 & 0 & -1 & 2 \\ 1 & 1 & 2 & 8 & 0 & 1 & 2  \end{bmatrix}$

$[A]_3=[A_3]+3\times [A_1]$, $A=\begin{bmatrix} 1 & 1 & 2 & 8 & 0 & 0 & -2 \\0 & 0 & 0 & 0 & 0 & 1 & 4 \\ 0 & 0 & -1 & -3 & 0 & -1 & -4 \\ 1 & 1 & 2 & 8 & 0 & 1 & 2  \end{bmatrix}$ 

$[A]_3=-1 \times [A]_3$ , $A=\begin{bmatrix} 1 & 1 & 2 & 8 & 0 & 0 & -2 \\0 & 0 & 0 & 0 & 0 & 1 & 4 \\ 0 & 0 & 1 & 3 & 0 & 1 & 4 \\ 1 & 1 & 2 & 8 & 0 & 1 & 2  \end{bmatrix}$ 

$[A]_4=[A]_4+(-1)\times [A]_1$, $A=\begin{bmatrix} 1 & 1 & 2 & 8 & 0 & 0 & -2 \\0 & 0 & 0 & 0 & 0 & 1 & 4 \\ 0 & 0 & 1 & 3 & 0 & 1 & 4 \\ 0 & 0 & 0 & 0 & 0 & 1 & 4  \end{bmatrix}$

$[A]_2 \longleftrightarrow [A]_3$, $A=\begin{bmatrix} 1 & 1 & 2 & 8 & 0 & 0 & -2  \\ 0 & 0 & 1 & 3 & 0 & 1 & 4 \\0 & 0 & 0 & 0 & 0 & 1 & 4\\ 0 & 0 & 0 & 0 & 0 & 1 & 4  \end{bmatrix}$

$[A]_1=[A]_1-2\times [A]_2$, $A=\begin{bmatrix} 1 & 1 & 0 & 2 & 0 & -2 & -10  \\ 0 & 0 & 1 & 3 & 0 & 1 & 4 \\0 & 0 & 0 & 0 & 0 & 1 & 4\\ 0 & 0 & 0 & 0 & 0 & 1 & 4  \end{bmatrix}$

$[A]_4=[A]_4-[A]_3$, $A=\begin{bmatrix} 1 & 1 & 0 & 2 & 0 & -2 & -10  \\ 0 & 0 & 1 & 3 & 0 & 1 & 4 \\0 & 0 & 0 & 0 & 0 & 1 & 4\\ 0 & 0 & 0 & 0 & 0 & 0 & 0  \end{bmatrix}$

$[A]_1=[A]_1+2\times[A]_3$, $A=\begin{bmatrix} 1 & 1 & 0 & 2 & 0 & 0 & -2  \\ 0 & 0 & 1 & 3 & 0 & 1 & 4 \\0 & 0 & 0 & 0 & 0 & 1 & 4\\ 0 & 0 & 0 & 0 & 0 & 0 & 0  \end{bmatrix}$

$[A]_2=[A]_2-[A]_3$,  $A=\begin{bmatrix} 1 & 1 & 0 & 2 & 0 & 0 & -2  \\ 0 & 0 & 1 & 3 & 0 & 0 & 0 \\0 & 0 & 0 & 0 & 0 & 1 & 4\\ 0 & 0 & 0 & 0 & 0 & 0 & 0  \end{bmatrix}$

(나) 는 생략한다.



<b>정리 1.2.3 가능성 증명</b> (수학적 귀납법으로 증명)

모든 행렬은 유한번의 elementary row operation을 시행하여 row-induced echelon form으로 바꿀 수 있다.

---

(1) 행의 갯수 $n$ 에 대한 귀납법으로 증명한다. $n=1$ 일 때는 첫번째 nonzero element 가 $a$ 일 때 $1/a$ 를 곱하면 된다.

(2) $n$ 개보다 적거나 같은 수의 행을 가진 행렬에 대해 성립한다고 가정하고 $n+1$ 개의 행을 가진 행렬을 생각하자. 마지막 행을 제외한 행렬에 대한 row-induced echelon form $A_0$ 를 만드는 것은 귀납법의 가정에 의해 가능하다. 

(3) 마지막 행의 nonzero 열에 대해 만약 $A_0$ 에 해당 열에 대한 최초의 1이 있으면 이 열을 elementary row operation으로 $0$ 으로 만들 수 있다. 해당 열에 대한 최초의 1이 $A_0$에 없으면 해당 열의값의 곱셈의 역수를 $n+1$ 번째 행에 곱해 그 값을 1로 만든 후 그 행을 적당한 행과 교환하여 echelon form으로 만든다. 그 행부터 최후 행까지의 행렬에 대해서만 생각하면 행의 갯수가 $n$ 보다 작거나 같으므로 row-induced echelon form을 만들 수 있으며 전체 행렬에 대해 생각하면 row-induced echelon form이다.  $\square$





<b>연습문제 1.2.5.</b> (가) $0$ 은 언제나 $(*)\, AX=0$ 의 solution 임을 보여라.

(나) $X_1,\,X_2$ 가 $(*)$의 solution 이면 $X_1+X_2$ 도 ($*$) 의 solution 임을 보여라.

(다) $X_0$ 가 ($*$) 의 solution 이고 $c\in \mathbb{F}$ 이면 $cX_0$ 도 ($*$) 의 solution 임을 보여라.

---

(가) Let $A\in\mathfrak{M}_{m,\,n}(\mathbb{F})$ and $X=0\in \mathfrak{M}_{n,\,1}(\mathbb{F})$. Then $(AX)_j=\sum_{k=1}^{n} A_{jk}X_{k1}=0$ .

(나) $A(X_1+X_2)=AX_1+AX_2=0$. 

(다) $A(cX_0)=cAX_0=0$. 



## 1.3 Elementary Matrix



<b>연습문제 1.3.8</b> $A\in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 일 때 $(A,\,I_n)\in \mathfrak{M}_{n,\,2n}(\mathbb{F})$ 를 생각하자. 만약 행렬 $(A,\,I_n)$ 에 elemtary row operation을 수행하여 $(I_n,\,B)$ 를 얻을 수 있었다면, $B=A^{-1}$ 임을 보여라. (왜 이 연습문제가 section 1.2 에 등장하지 못했을까?)

---

Let $E_1\cdots E_m A=I_n$ where $E_i,\, i=1,\ldots,\,m$ is elementary matrices. Then, $E_1\cdots E_m I_n = E_1\cdots E_m= \ B$. Then, $BA=I_n$. 

$A=E^{-1}_m \cdots E^{-1}_1$ 이므로 $AB=E^{-1}_m \cdots E^{-1}_1 E_1 \cdots E_m=I$. 따라서, $B=A^{-1}$. 



n 





