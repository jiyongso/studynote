VI. 행렬과 선형사상
===



## 연습문제 : 제 6장 1절



<b>1.</b>  생략



<b>2. </b> $m\times n$ 행렬 $A_0,\,A_1,\ldots,\,A_k$ 가 임의의 실수 $x$ 에 대하여
$$
A_0 +A_1x + \cdots + A_k x^k=O
$$
이면 $A_0 = A_1=\cdots =A_k =O$ 임을 보이라.

---

$(A_i)_{1,\,1}=a_i$ 라 하면 $a_0+a_1x+\cdots +a_kx^k=0$ 이어야 한다. 임의의 실수 $x$ 에 대해 성립하려면 $a_0=a_1=\cdots =a_k=0$ 이어야 하며 이는 $A_0,\ldots,\,A_k$ 의 각 성분에 대해서도 그러하다. 따라서 $A_0=\cdots =A_k=O$ 이어야 한다.



<b>3. </b> 생략



<b>4. </b> $m \times n$ 행렬 전체의 집합은 $\mathbb{R}^{mn}$ 과 일대일 대응 관계가 있음을 보이라.

---

정확히 말하면 실수에서 정의된 $m\times n$ 행렬 전체의 집합 $\mathbb{R}^{m \times n}$ 과 $\mathbb{R}^{mn}$ 이 일대일 대응 관계가 있음을 보여야 한다. $f:\mathbb{R}^{m \times n}\to \mathbb{R}^{mn}$ 을 다음과 같이 정의하자. $A\in \mathbb{R}^{m \times n}$ 에 대해 
$$
f(A)=(A_{11},\ldots, A_{1n},\,A_{21},\ldots,\, A_{2n},\cdots , A_{m1},\ldots,\,A_{mn})
$$
라 하자. 이는 잘 정의된 함수이다. 임의의 $B\in \mathbb{R}^{mn}$ 에 대해 $f(A)=B$ 인 $A$ 가 존재하므로 $f$ 는 전사이며 $f(A)=f(A')\implies A=A'$ 이므로 $f$ 는 단사이다.



<b>5. </b> (**야코비 항등식**) $n$ 차 정사각행렬 $A,\,B$ 에 대하여
$$
[A,\,B]:=AB-BA
$$
로 정의하자. 이때 $n$ 차 정사각행렬 $C$ 에 대하여,
$$
[[A,\,B],\,C]+[[B,\,C],\,A]+[[C,\,A],\,B]=O
$$
임을 보이라.
$$
\begin{align}
[[A,\,B],\,C]+[[B,\,C],\,A]+[[C,\,A],\,B] &=[AB-BA,\,C]+[BC-CB,\,A]+[CA-AC,\,B]\\
&=(AB-BA)C-C(AB-BA)+(BC-CB)A-A(BC-CB)\\
&\qquad\qquad +(CA-AC)B-B(CA-AC)\\
&=ABC-BAC-CAB+CBA+BCA-CBA-ABC+ACB\\
&\qquad \qquad +CAB-ACB-BCA+BAC\\
&=0

\end{align}
$$


<b>6. </b> 행렬
$$
\sigma_0 =\begin{pmatrix} 1 & 0 \\ 0 &-1\end{pmatrix},\quad \sigma_+=\begin{pmatrix} 0 & 1\\0 & 0\end{pmatrix},\quad \sigma_{-} = \begin{pmatrix}0 & 0 \\ 1 & 0\end{pmatrix}
$$
에 대하여 
$$
[\sigma_+,\,\sigma_-]=\sigma_0,\quad [\sigma_0,\,\sigma_+]=2\sigma_+,\quad [\sigma_0,\,\sigma_-]=-2\sigma_-
$$
임을 보이라.

---

$$
\begin{align}
[\sigma_+,\,\sigma_-]&=\sigma_+\sigma_--\sigma_-\sigma_+=\begin{pmatrix} 1 & 0\\ 0 & 0\end{pmatrix}
- \begin{pmatrix} 0 & 0\\ 0 & -1\end{pmatrix} = \begin{pmatrix} 1 & 0\\ 0 & 1\end{pmatrix}=\sigma_0\\
[\sigma_0,\, \sigma_+] &=\sigma_0 \sigma_+-\sigma_+\sigma_0=\begin{pmatrix} 0 & 1\\ 0 & 0\end{pmatrix} - \begin{pmatrix} 0 & -1\\ 0 & 0\end{pmatrix} = \begin{pmatrix} 0 & 2\\ 0 & 0\end{pmatrix} =2 \sigma_{+ }\\
[\sigma_0,\,\sigma_-] &=\sigma_0 \sigma_- - \sigma_-\sigma_0 =\begin{pmatrix} 0 & 0\\ -1 & 0\end{pmatrix}- \begin{pmatrix} 0 & 0\\ 1 & 0\end{pmatrix}=\begin{pmatrix} 0 & 0\\ -2 & 0\end{pmatrix}=-2\sigma_-


\end{align}
$$



<b>7. </b> $n$ 차 정사각행렬중 $(i,\,j)$ 항만 $1$ 이고 나머지 항은 $0$ 이 되는 행렬을 $E_{ij}$ 라고 두자. 그러면,
$$
E_{ij}E_{kl}=\delta_{kj}E_{il} \quad (i,\,j,\,k,\,l) \in \{1,\ldots,\,n\}
$$
임을 보이라. 여기서,
$$
\delta_{jk}=\left\{\begin{array}{ll}1 \qquad & (j=k) \\ 0 &(j \ne k)\end{array}\right.
$$
이다.

---

$E_{ij}$ 의 $(p,\,q)$ 항을 $[E_{ij}]_{pq}$ 라 하면 $[E_{ij}]_{pq}=\delta_{ip}\delta_{jq}$ 이다. 
$$
[E_{ij}E_{kj}]_{pr}=\sum_{q=1}^n [E_{ij}]_{pq} [E_{kl}]_{qr}=\sum_{q=1}^n \delta_{ip}\delta_{jq}\delta_{kq}\delta_{lr}= \delta_{ip}\delta_{jk}\delta_{lr}=\delta_{jk}[E_{il}]_{pr}
$$
이므로 $E_{ij}E_{kj}=\delta_{jk}E_{il}$ 이다.



<b>8. </b> 정사각행렬중에 대각선 이외의 항이 모두 $0$ 인 행렬을 대각행렬이라고 부른다. 이 때 임의의 $n$ 차 대각행렬 $A,\,B$ 에 대하여 $AB=BA$ 임을 보이라.

---

$A$ 가 대각행렬이면 $A_{ij}=a_j\delta_{ij}$ 이다. $B_{ij}=b_j \delta_{ij}$ 라 하면,
$$
\begin{align}
(AB)_{jk}&=\sum_{i=1}^n A_{ji}B_{ik}=\sum_{i=1}^n a_j\delta_{ij}b_i\delta_{ik}=a_jb_j\delta_{jk}\\
(BA)_{jk}&= \sum_{i=1}^n B_{ji}A_{ik}=\sum_{i=1}^m b_{j}\delta_{ij}a_k\delta_{ik}=a_jb_j \delta_{jk}
\end{align}
$$
따라서 $AB=BA$ 이다. 



<b>9. </b>(**복소수** 와 행렬)  행렬 $I=\begin{pmatrix} 1 & 0 \\ 0 & 1\end{pmatrix},\, J=\begin{pmatrix}0 & -1 \\ 1 & 0\end{pmatrix}$ 에 대하여,
$$
J^2=-I
$$
임을 보이라. 또 임의의 실수 $a,\,b,\,c$ d에 대하여
$$
(aI+bJ)(cI+dJ)=(ac-bd)I+(bc+ad)J
$$
임을 보이라.

---

$$
J^2=\begin{pmatrix}0 & -1 \\ 1 & 0\end{pmatrix}\begin{pmatrix}0 & -1 \\ 1 & 0\end{pmatrix}=\begin{pmatrix}-1 & 0 \\ 0 & -1\end{pmatrix}=-I
$$

이다. 이와 함께, $I^2=I,\, IJ=JI=J$ 를 이용하면,
$$
\begin{align}
(aI+bJ)(cI+dJ)&= acI+adJ+bcJ+bdJ^2=(ac-bd)I+(bc+ad)J

\end{align}
$$
이다. 





## 연습문제 : 제 6장 2절



<b>1. </b> 삼차원 공간에서 $xy$ 평면으로의 정사영에 대응되는 행렬을 구하라. 또 $yz$-평면, $zx$-평면으로의 정사영에 대응되는 행렬을 각각 구하라.

---

삼차원 공간에서 $xy$ 평면으로의 정사영을 함수로 하면 $p_{xy}(x,\,y,\,z)=(x,\,y,\,0)$ 이다. 이를 행렬로 표현한 것을 $P_{xy}$ 라 하면.. 그리고 $yz,\,zx$ 평면에 대해서도 같이 생각하면,
$$
P_{xy}=\begin{pmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0\end{pmatrix},\quad P_{yz}=\begin{pmatrix}0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{pmatrix},\quad P_{zx}=\begin{pmatrix}1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 1\end{pmatrix}
$$
이다.



<b>2. </b> $m \times n$ 행렬 $A,\,B$ 와 실수 $c$ 에 대하여,
$$
L_{A+B}=L_A+L_B,\quad L_{cA}=cL_A
$$
임을 보이라.

---

$$
\begin{align}
L_{A+B}(\mathbf{x})&=(A+B)\mathbf{x}=A\mathbf{x}+B\mathbf{x}=L_A(\mathbf{x})+L_B(\mathbf{x})\\
L_{cA}(\mathbf{x})&=(cA)\mathbf{x}=c(A\mathbf{x})=cL_A(\mathbf{x})

\end{align}
$$

<b>3. </b> $m\times n$ 행렬 $A$ 와 $n \times l$ 행렬 $B$ 에 대하여 두 선형사상 $L_B : \mathbb{R}^l \to \mathbb{R}^n$ 과 $L_A: \mathbb{R}^n \to \mathbb{R}^m$ 의 합성
$$
L_A \circ L_B : \mathbb{R}^l \to \mathbb{R}^m
$$
은 $L_{AB}: \mathbb{R}^l \to \mathbb{R}^m$ 과 일치함을 보이라. 즉 행렬의 곱은 선형사상의 합성에 해당된다.

---

$$
L_A\circ L_B (\mathbf{x})=L_A (B\mathbf{x})=A(B\mathbf{x})=(AB)\mathbf{x}=L_{AB}(\mathbf{x})
$$



<b>4. </b> 선형사상 $L:\mathbb{R}^n \to \mathbb{R}^m$ 이 일대일 함수일 필요충분조건은 방정식 $L(X)=O$ 의 해가 자명한 것일 뿐임을 보이라.

---

일대일 함수는 단사함수를 의미한다. 

(1) $L(X)=O$ 의 해가 자명한 것, 즉 $X=O$ 뿐임을 가정한다. 그렇다면 $A,\,B\in \mathbb{R}^n$ 에 대해 
$$
L(A)=L(B)\implies L(A)-L(B)=O \implies L(A-B)=O \implies A=B
$$
이다. 이므로 $L$ 은 일대일 함수이다.

(2) $L$ 이 일대일 함수임을 가정하자. 우리는 $L'$ 이 선형사상이면 $L'(O)=O$ 임을 알고 있다. $L$ 이 일대일 함수이면 $L(X)=O$ 를 만족하는 $X$ 가 하나 뿐 이므로 자명한 $O$ 뿐이다.



<b>5. </b> 공간의 점들의 질량중심은 선형사상에 의하여 보존됨을 보여라. 즉, 점 $P_1,\ldots,\,P_k$ 의 질량이 각각 $m_1,\ldots,\,m_k$ 로 주어지고, 이들의 질량중심이 $\overline{P}$ 일 때 선형사상에 의한 이들의 상 $L(P_1),\ldots,\,L(P_k)$ 의 질량중심은 $L(\overline{P})$ 임을 보이라. (단, $L(P_i)$ 의 질량은 $m_i$ 이다.)

---

$M=m_1+\cdots +m_k$ 라면 $\displaystyle \overline{P}=\sum_{i=1}^k \dfrac{m_i}{M}P_i$ 이다.
$$
L\left(\overline{P}\right)=L\left(\sum_{i=1}^k \dfrac{m_i}{M}P_i\right)=\sum_{i=1}^k \dfrac{m_i}{M}L(P_i)
$$


<b>6. </b> 공간 속의 점들의 질량중심은 평행이동에 대하여 보존됨을 보이라.

---

평행이동을 $f:X \mapsto X+\mathbf{v}$ 라 하자. 문제 5와 같은 notation을 사용한다. 
$$
f\left(\sum_{i=1}^k \dfrac{m_i}{M}P_i\right) = \sum_{i=1}^k \dfrac{m_i}{M}P_i +\mathbf{v}=\sum_{i=1}^k \dfrac{m_i}{M}P_i +\sum_{i=1}^m \dfrac{m_i}{M}\mathbf{v} = \sum_{i=1}^k \dfrac{m_i}{M}(P_i+\mathbf{v})=\sum_{i=1}^k \dfrac{m_i}{M}f(P_i)
$$


<b>7. </b> 차수가 $n$ 이하인 다항식 전체의 집합을 $P_n$ 이라 두고,
$$
p(x)=a_0+a_1x+\cdots + a_nx^n
$$
을 벡터 $(a_0,\ldots,\,a_n)$ 과 같이 보았을 때, 미분사상
$$
D:P_n \to P_n , \quad p(x)\mapsto p'(x)
$$
에 대응하는 행렬을 구하라. 또 사상
$$
S:P_n \to P_{n+1},\qquad p(x)\mapsto xp(x)
$$
에 대응되는 행렬을 구하라.

----

$$
\begin{align}
D(a_0,\ldots,\,a_n)&=(a_1,\, 2a_2,\cdots,\,na_n,\,0)\\
S(a_0,\ldots,\,a_n)&= (0,\,a_0,\,a_1,\ldots,\,a_n)
\end{align}
$$

이므로
$$
D=\begin{pmatrix} 0 & 1 & 0 & 0 & \cdots & 0 & 0\\0 & 0 & 2 & 0 & \cdots & 0 & 0 \\
0 & 0 & 0 & 3 & \cdots & 0 & 0 \\ & & & \vdots  &\\0& 0 & 0 & 0 & \cdots & 0 & n \\ 0 & 0 & 0& 0 & \cdots & 0 & 0\end{pmatrix} \,\qquad S=\begin{pmatrix} 0 & 0 & 0 & \cdots & 0& 0\\ 1 & 0 & 0 &\cdots & 0 & 0 \\
0 & 1 & 0 & \cdots & 0 & 0 \\ 0 & 0 & 1 & \cdots & 0 & 0 \\
&&&\vdots \\
0&0&0&\cdots&1 & 0\\
0 & 0 & 0 & \cdots & 0 & 1\end{pmatrix}
$$
이다. 



<b>8. </b> $m \times n$ 행렬 $A,\,B$ 가 임의의 $n \times l$ 행렬 $X$ 에 대하여 $AX=BX$ 이면 $A=B$ 임을 보이라.

---

연습문제 6.1.7 에 정의된 $E_{ij}\in \mathbb{R}^{n\times l}$ 을 생각하자. $E_{ij}$ 는 $(i,\,j)$ 항만 $1$ 이고 나머지는 $0$ 인 행렬이다. $X=E_{ij}$ 이면 
$$
(AX)_{pq}=(AE_{ij})_{pq}=\sum_{r=1}^n A_{pr}(E_{ij})_{rq}=\sum_{r=1}^nA_{pr}\delta_{ir}\delta_{jq}=A_{pi}\delta_{jq}
$$
이므로 $AE_{ij}$ 의 $j$-th column 은 $A$ 의 $i$-th column 이며 나머지는 $0$ 이다. $AE_{ij}=BE_{ij}$ 이므로 $A$ 의 $i$-th column 과 $B$ 의 $i$-th column이 같다는 것을 확인 할 수 있으며 $i$ 를 $1$ 부터 $n$ 까지 변화시키면 $A$ 와 $B$ 의 모든 column 이 같음을 확인 할 수 있다. 따라서 $A=B$ 이다.



<b>9. </b> 삼차원의 공간에서 벡터 $(1,\,2,\,3)$ 에 대한 정사영을 나타내는 행력을 구하라.

----

$X=(x,\,y,\,z)$ 의 $\mathbf{a}=(1,\,2,\,3)$ 에 대한 정사영 $P$ 는 정리 3.1.1 에 의해,
$$
P(X)=\dfrac{X \cdot \mathbf{a}}{\mathbf{a}\cdot \mathbf{a}}\mathbf{a}=\dfrac{x+2y+3z}{14}(1,\,2,\,3)
$$
이므로 이를 행렬 $P$ 로 나타내면,
$$
P =\dfrac{1}{14}\begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 3 & 6 & 9\end{pmatrix}
$$
이다.



<b>10. </b> 행렬 $\begin{pmatrix} 1 & 1 & 1\\ 1 & 1 & 1 \\ 1 & 1 & 1\end{pmatrix}$ 로 표현되는 선형변환의 기하학적 의미를 설명하라.

---

$$
(x,\,y,\,z) \mapsto (x+y+z,\, x+y+z,\, x+y+z)
$$

이다. 



## 부록 : 등장변환과 행렬의 극한



#### 등장변환

변환 $T:\mathbb{R}^n \to \mathbb{R}^n$ 이
$$
|T(X)-T(Y)|=|X-Y| \qquad (X,\,Y \in \mathbb{R}^n)
$$
를 만족시키면 $T$ 를 등장변환이라고 한다.



#### 정리 3.1.2

변환 $T:\mathbb{R}^n \to \mathbb{R}^n$ 이 원점을 보존하는 등장변환이면, 임의의 $X,\,Y\in \mathbb{R}^n$ 에 대하여 (여기서 $T(X)$ 를 $TX$ 로 쓰기로 하자.)

(1) $|TX|=|X|$

(2) $TX\cdot TY=X \cdot Y$

(3) $T(aX+bY)=aTX+bTY \qquad (a,\,b\in \mathbb{R})$ 

가 성립한다. 특히 원점을 보존하는 등장변환은 선형변환이다. 

---

*(proof)*

(1) 등장변환이면 $|TX-TY|=|X-Y|$  이며 $T$ 가 원점을 보존하는 선형변환이므로 $Y=0$ 에 대해 $T(Y)=0$ 이다. 따라서 $|TX|=|X|$

(2) $|TX-TY|=|X-Y|\implies |TX-TY|^2=|X-Y|^2 \implies TX\cdot TY=X\cdot Y$ 

(3) 임의의 $Z\in \mathbb{R}^n$ 에 대해 
$$
\begin{align}
|TZ-aTX-bTY|^2&=|TZ|^2+a^2|TX|^2+b^2|TY|^2-2a(TZ\cdot TX)-2b(TZ \cdot TY)+2ab(TX\cdot TY)\\
&= |Z|^2+a^2|X|^2+|Y|^2-2a(Z\cdot X)-2b(Z\cdot Y)+2ab(X \cdot Y)\\
&=|Z-aX-bY|^2


\end{align}
$$
을 얻는다. $Z=aX+bY$ 라 하면 $|T(aX+bY)-aTX-bTY|^2=0$ 이므로 $T(aX+bY)=aTY+bTY$ 이다.



#### 정리 3.1.3 

$n$ 차 정사각행렬 $A$ 로 부터 얻은 $n$-공간의 선형변환 $L_A$ 가 등장변환일 필요충분조건은
$$
A^tA=I
$$
이다.

---

*(proof)* (1) $L_A$ 가 등장변환이라 가정하자. 임의의 $X,\,Y\in \mathbb{R}^n$ 에 대해 정리 3.1.2 (2) 를 사용한다면,
$$
X \cdot Y = AX \cdot AY =(AX)^t AY=X^tA^tAY
$$
이다. 

(2) $A^tA=I$ 임을 가정한다. 임의의 $X\in \mathbb{R}^n$ 에 대해,
$$
|X|^2=X\cdot X = X^tX= X^tA^tAX=(AX)^tAX=(AX)\cdot (AX)=|AX|^2
$$
이다. 따라서 $|X|=|AX|$ 이므로, 임의의 $X,\,Y\in \mathbb{R}^n$ 에 대해,
$$
ㅣL_A(X)-L_A(Y)|=|AX-AY|=|A(X-Y)|=|X-Y|
$$
이므로 $L_A$ 는 등장변환이다.



#### 직교행렬 (Orthogonal matrix)과 직교변환

정사각행렬 $A$ 가 $A^tA=I$ 를 만족할 때 $A$ 를 직교행렬이라고 부른다. 직교행렬에 의한 변환을 직교변환이라고 한다. 



#### 직교행렬과 정규직교기저

$n \times n$ 행렬 $A$ 가 직교행렬이면 $A$ 의 각 열벡터는 $n$ 공간의 정규직교기저를 이룬다.

---

*(proof)* $A$ 행렬의 $i$-th column 을 $A_i$ 라 하고 $A=(A_1,\ldots,\,A_n)$ 이라 쓸 수 있다. 이 때, $(A^tA)_{ij}=A_i \cdot A_j = \delta_{ij}$ 이므로 $A$ 의 각 열벡터는 정규직교공간의 기저이다.



#### 따름정리 3.1.4

$n$ 공간의 등장변환은 직교변환과 평행이동의 합성으로 이루어진다.

---

*(proof)* $T:\mathbb{R}^n \to \mathbb{R}^n$ 이 등장변환이면
$$
L(X):=T(X)-T(O)
$$
은 원점을 보존한다. 임의의 $X,\,Y\in \mathbb{R}^n$ 에 대해,
$$
|L(X)-L(Y)|=|T(X)-T(O)-T(Y)+T(O)|=|T(X)-T(Y)|=|X-Y|
$$
이므로 등장변환이다. $L$ 은 원점을 보존하는 등장변환이며 따라서 정리 3.1.2에 의해 선형변환므로 정리 3.1.3에 의해 직교변환이다. 
$$
T(X)=L(X)+T(O)
$$
이므로 등장변환은 직교변환과 평행이동의 함성이다. 



#### 행렬의 극한

$m\times n$ 행렬 $A=(a_{ij})$ 의 크기, 혹은 절대값을 $|A|$ 라 쓰고 다음과 같이 정의하자.
$$
|A|:=\sqrt{\sum_{i=1}^m \sum_{j=1}^n {a_{ij}}^2}
$$


#### 정리 3.3.2

$m \times n$ 행렬 $A$ 와 $n \times l$ 행렬 $B$ 에 대하여,
$$
|AB|\le |A|\cdot |B|
$$
가 성립한다. 특히 $A$ 가 정사각행렬이면,
$$
\left|A^k \right|\le |A|^k \qquad (k=1,\,2,\,3,\ldots)
$$
가 성립한다.

---

*(proof)* 
$$
|AB|^2 = \sum_{i=1}^m \sum_{j=1}^l \left(\sum_{k=1}^n a_{ik}b_{kj}\right)^2 \le \sum_{i=1}^m \sum_{j=1}^l \left(\sum_{k=1}^n a_{ik}^2\right)\left(\sum_{k=1}^n b_{kj}^2\right)=\left(\sum_{i=1}^m\sum_{k=1}^{n}a_{ik}^2
\right)\left(\sum_{j=1}^l\sum_{k=1}^{n}b_{kj}^2 \right)=|A|^2|B|^2
$$


