VI. 행렬과 선형사상 #1
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



#### 정리 3.3.3

$m\times n$ 행렬의 수열 $A(k),\,k=1,\,2,\,3,\ldots$ 이 행렬 $B$ 에 수렴할 필요충분조건은
$$
\lim_{k \to \infty} |A(k)-B|=0
$$
이다.

---

*(proof)* $M=m\times n$ 라 하자. 만약 $A(k)$ 가 $B$ 에 수렴한다고 가정한다면 $A(k)$ 의 각 항이 해당하는 $B$ 각 항에 수렴하는 것이므로, 주어진 $\epsilon>0$에 대해 $n\ge N_{ij}\implies \left| (A(k))_{ij}-B_{ij} \right|\le \dfrac{\epsilon}{M}$ 를 만족하는 $N_{ij}$ 가 존재한다.  $N:=\max\{N_{ij}: 1\le i,\,j \le n\}$ 이라 하면 
$$
n\ge N \implies  \left| (A(k))_{ij}-B_{ij} \right|\le \dfrac{\epsilon}{M} \quad \forall i,\,j=1,\ldots,\,n
$$
이다. 그렇다면, $n\ge N$ 일 때
$$
|A(k)-B|= \sqrt{\sum_{i,\,j} \left(A(k)_{ij}-B_{ij}\right)^2}\le \sqrt{\sum_{i,\,j} \dfrac{\epsilon^2}{M^2}}=\dfrac{\epsilon}{\sqrt{M}}\le \epsilon
$$
이므로 $\displaystyle \lim_{k \to \infty} |A(k)-B|=0$ 이다.

이제 $\displaystyle \lim_{k \to \infty} |A(k)-B|=0$ 임을 가정하자. 임의의 행렬 $C$ 에 대해 $|C|\le \max\{C_{ij}\}$ 이므로 $|A(k)_{ij}-B_{ij}|\le |A(k)-B|$ 이며 따라서,
$$
\lim_{k \to \infty}|A(k)_{ij}-B_{ij}|=0
$$
이다. 따라서 행렬 $A(k)$ 는 $B$ 로 수렴한다.



#### 행렬 급수의 수렴

$m\times n$ 행렬의 급수 $\displaystyle \sum_{k=0}^\infty A(k)$ 가 행렬 $B$ 에 수렴한다는 것은 유한합으로 이루어진 행렬의 수열 $\displaystyle \sum_{k=0}^n A(k),\quad n=0,\,1,\,2,\ldots$ 가 $B$ 에 수렴한다는 뜻이다. 이 때 $\displaystyle \sum_{k=0}^\infty A(k)=B$ 로 쓰기로 한다.



#### 정리 3.4.2

임의의 정사각행렬 $A$ 에 대하여 급수
$$
I+A+\dfrac{1}{2!}A^2+ \dfrac{1}{3!}A^3 + \cdots + \dfrac{1}{k!}A^k + \cdots
$$
는 항상 수렴한다. 이 때 극한값을 $\exp A$ 또는 $e^A$ 로 쓴다.

---

*(proof)* (1) $a=\max\{|A_{ij}|: 1\le i,\,j \le n\}$ 라 하면 $|A| \le na$ 이다. 또한 정리 3.3.2 에 의해 $|A^k_{ij}|\le |A^k|\le |A|^k \le n^k a^k$ 이다. 

(2) 따라서 $B=I+A+\dfrac{1}{2!}A^2+\cdots $ 라 했을 때 $|B_{ij}|\le 1+na+\dfrac{n^2a^2}{2!}+\dfrac{n^3a^3}{3!}+\cdots = e^{na} $ 이다. 







## 연습문제 : 제 6장 3절



<b>1. </b> 차수가 같은 두 직교행렬의 곱은 직교행렬임을 보여라.

---

$A,\,B\in \mathbb{R}^{n \times n}$ 이 직교행렬이라 하자. $(AB)^t(AB)=B^tA^tA^B=B^tB=I$ 



<b>2. </b> 영이 아닌 벡터 $X\in \mathbb{R}^n$ 에 대하여 $n \times n$ 행렬
$$
A:=I_n-\dfrac{2}{|X|^2}XX^t
$$
는 직교행렬임을 보이라.

---

우리는 임의의 $n\times n$ 행렬 $P,\,Q$ 와 $c\in \mathbb{R}$ 에 대해 다음이 성립함을 안다.
$$
\begin{align}
(P+cQ)^t&=P^t+cQ^t
\end{align}
$$
따라서,
$$
A^t = (I_n)^t-\dfrac{2}{|X|^2}(XX^t)^t = I_n -\dfrac{2}{|X|^2}XX^t=A
$$
이며, $X^tX=|X|^2$ 임을 이용한다. 
$$
\begin{align}
A^tA &= A^2=\left(I_n - \dfrac{2}{|X|^2}XX^t\right)^2\\
&= I_n - \dfrac{4}{|X|^2}XX^t+ \dfrac{4}{|X|^2}XX^tXX^t \\
&=I_n - \dfrac{4}{|X|^2}XX^t+\dfrac{4}{|X|^2}|X|^2XX^t\\
&=I_n
\end{align}
$$


<b>3. </b> 좌표평면의 점들을 원점 주위로 크기 $\alpha$ 만큼 회전시키는 변환을 한 다음, 다시 각의 크기 $\beta$ 만큼 회전시키는 변환은, 각의 크기 $\alpha+\beta$ 만큼 회전시키는 변환과 같음을 이용하여,
$$
\begin{align}
\cos (\alpha+\beta)&=\cos \alpha \, \cos \beta -\sin \alpha\sin \beta\\
\cos (\alpha+\beta)& =\sin \alpha \cos \beta + \cos \alpha \sin \beta

\end{align}
$$
를 유도하라.

---

$\mathbb{R}^2$ 에서 $\theta$ 만큼 회전 시키는 변화를 나타내는 행렬 $R_\theta = \begin{pmatrix} \cos \theta & -\sin \theta \\ \sin \theta & \cos \theta \end{pmatrix}$ 이다. 따라서,
$$
\begin{pmatrix} \cos (\alpha+\beta)& - \sin (\alpha+\beta) \\\sin (\alpha+\beta) & \cos (\alpha+\beta)  \end{pmatrix} = \begin{pmatrix} \cos \beta& -\sin \beta \\ \sin \beta & \cos \beta \end{pmatrix} \begin{pmatrix} \cos \alpha & -\sin \alpha \\ \sin \alpha & \cos \alpha \end{pmatrix}= \begin{pmatrix} \cos \alpha\cos \beta - \sin \alpha \sin \beta & -\sin \alpha \cos \beta - \cos \alpha \sin \alpha \\ \sin \alpha \cos \beta + \cos \alpha \sin \alpha  & \cos \alpha\cos \beta - \sin \alpha \sin \beta \end{pmatrix}
$$




<b>4. </b> 삼차원 공간에서 회전변환 $R_1,\,R_2,\,R_3$ 가 다음 관계를 가짐을 보여라.
$$
R_1 \left(-\dfrac{\pi}{2}\right)\circ R_3 (\theta) \circ R_1\left(\dfrac{\pi}{2}\right)=R_2(\theta)
$$

---

$$
\begin{align}
R_1 \left(-\dfrac{\pi}{2}\right)\circ R_3 (\theta) \circ R_1\left(\dfrac{\pi}{2}\right)& = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & -1 & 0\end{pmatrix} \begin{pmatrix} \cos \theta & - \sin \theta & 0 \\\sin \theta & \cos \theta& 0 \\ 0 & 0 & 1\end{pmatrix} \begin{pmatrix} 1 & 0 & 0 \\ 0 & 0 & -1 \\ 0 & 1 & 0\end{pmatrix} \\
&= \begin{pmatrix} \cos \theta & -\sin \theta & 0 \\ 0 & 0 & 1 \\ - \sin \theta & - \cos \theta & 0\end{pmatrix}\begin{pmatrix} 1 & 0 & 0 \\ 0 & 0 & -1 \\ 0 & 1 & 0\end{pmatrix} \\
&=\begin{pmatrix} \cos \theta & 0 & \sin \theta \\ 0 & 1 & 0 \\ - \sin \theta & 0 & \cos \theta\end{pmatrix}\\
&=R_2(\theta)


\end{align}
$$



<b>5. </b> 좌표평면에서 곡선
$$
ax^2+2bxy+cy^2+d=0
$$
을 회전이동하여 얻은 곡선이 
$$
a'x^2+2b'xy+c'y^2+d'=0
$$
이라고 하자. 이 때
$$
ac-b^2=a'c'-b'^2
$$
임을 보이라.

---

$x\to \cos \theta x-\sin \theta y,\, y \to \sin \theta x + \cos \theta y$ 라 하면,
$$
\begin{align}
a'x^2+2b'xy+c'y^2+d'&=a(\cos \theta x-\sin \theta y)^2 +2b (\cos \theta x-\sin \theta y)(\sin \theta x+\cos \theta y)\\
&\qquad + c(\sin \theta x+\cos \theta y)^2+d\\
&=(a \cos^2 \theta +2b \cos \theta \sin \theta +c\sin^2 \theta)x^2 +(-2a\cos \theta \sin \theta+2b \cos^2\theta-2b \sin^2 \theta+2c\sin \theta \cos \theta)xy\\
&\qquad + (a\sin^2 \theta -2b \sin \theta \cos \theta+c\cos ^2 \theta)y^2+d'


\end{align}
$$
이다. 따라서,
$$
\begin{align}
a'c'-b'^2&=(a \cos ^2 \theta +2b \cos \theta \sin \theta + c\sin ^2 \theta)(a\sin^2 \theta -2b \sin \theta \cos \theta+c\cos ^2 \theta)\\
&\qquad -(-a\cos \theta \sin \theta+b \cos^2\theta-b \sin^2 \theta+c\sin \theta \cos \theta)^2\\
&=(\cos^2\theta\sin^2\theta-\cos^2\theta\sin^2\theta)a^2+(-4\cos^2\theta \sin^2 \theta-(\cos^2\theta-\sin^2\theta)^2)b^2\\
&\qquad+(\cos^2\theta\sin^2\theta-\cos^2\theta\sin^2\theta)c^2+(-2\cos^3\theta \sin \theta+2\cos\theta\sin^2\theta+2\cos\theta\sin\theta(\cos^2\theta-\sin^2\theta)) ab\\
&\qquad +(2\cos^3\theta \sin\theta-2\cos\theta \sin^3\theta-2\sin\theta\cos\theta(\cos^2\theta-\sin^2\theta))bc\\
&\qquad +(\cos^4\theta+\sin^4\theta+2\sin^2\theta\cos^2\theta)ac\\
&=0\cdot a^2+(-2\sin^22\theta-2\cos^2 2\theta)b^2 + 0\cdot c^2-0\cdot ab+0\cdot bc + (\cos^2\theta+\sin^2\theta)^2ac\\
&=ac-b^2

\end{align}
$$


<b>6. </b> 좌표평면에서 두 직선 $ax+by+c_1=0,\, ax+by+c_2=0$ 에 대한 반사변환을 각각 $T_1,\,T_2$ 라고 두자. (단 $a^2+b^2=1$ 이라고 가정한다) 이 때 합성변환 $T_1 \circ T_2$ 는 어떤 변환인가.

---

$ax+by+c_2=0$ 의 한 점 $X$에서 $ax+by+c_1=0$ 으로 수선을 내렸을때의 교점을 $Y$ 라 한다면 $\overrightarrow{XY}$ 방향으로 두 직선의 거리의 두배만큼 평행이동 하는 변환이다.



<b>7. </b> 포물선 $y=x^2$ 과 $y=2x^2$ 은 닮음 변환임을 보이라. 

---

$x \to 2x$, $y \to 2y$ 변환을 생각하라.



<b>8. </b> 좌표평면에서 곡선
$$
x^2+4xy+3y^2=1
$$
은 타원, 쌍곡선, 포물선 중 어느 것인지를 판정하라.

---

$$
x^2+4xy+3y^2=1 \implies (x+2y)^2-y^2=1
$$

이므로 쌍곡선이다.



<b>9. </b> 좌표평면의 점 $(x,\,y)$ 를 $x$ 축에 대하여 대칭이동 시키고, 원점을 중심으로 하여 반시계방향으로 $60^\circ$ 회전시킨 다음, 다시 $x$ 축에 대하여 대칭이동시키는 선형사상을 $T$ 라고 두자. 이 사상을 2001회 시행하였을 때, 점 $(1,\,1)$ 의 상을 구하라.

---

$$
T=\begin{pmatrix} 1 & 0 \\ 0 & -1\end{pmatrix} \begin{pmatrix} 1/2 & -\sqrt{3}/2 \\ \sqrt{3}/2 &1/2 \end{pmatrix}\begin{pmatrix} 1 & 0 \\ 0 & -1\end{pmatrix}=\begin{pmatrix} 1/2 & \sqrt{3}/2 \\ -\sqrt{3}/2 &1/2 \end{pmatrix}
$$

이므로 $T$ 는 시계방향 $60^\circ$ 회전이다. 2001회 시행은 시계방향으로 $180^\circ$ 회전이므로 역시 반시계방향 $180^\circ$ 회전이다. 따라서 (1,1) 의 상은 (-1,-1) 이다.



<b>10. </b> (**오일러 항등식**) 임의의 실수 $t$ 에 대하여,
$$
\exp \begin{pmatrix} 0 &-t\\ t & 0\end{pmatrix} = \begin{pmatrix} \cos t & - \sin t \\ \sin t & \cos t\end{pmatrix}
$$
임을 보이라.

---

$A=\begin{pmatrix} 0 &-t\\ t & 0\end{pmatrix},\, J=\begin{pmatrix} 0 & -1 \\ 1 & 0\end{pmatrix}$ 라 하면, $J^2=-I_2$, $J^3=-J$, $J_4=I$ 이므로 
$$
\begin{align}
A^k = t^k J^k 

\end{align}
$$
이다. $\exp A =I+tJ+\dfrac{1}{2}t^2J^2+\cdots + \dfrac{t^k}{k!}J^k+\cdots$ 이므로,
$$
\left(\exp A \right)_{11}=  (\exp A)_{22}=\sum_{k=0}^\infty \dfrac{(-1)^{k}t^{2k}}{(2k)!}=\cos t,\,\\
\left(\exp A\right)_{21}=-\left(\exp A\right)_{12}=\sum_{k=0}^\infty \dfrac{(-1)^{k}t^{2k+1}}{(2k+1)!}=\sin t\,.
$$


<b>11. </b> 다음을 보이라.
$$
\exp \begin{pmatrix} 0 & t & 0 & 0 \\ 0 & 0 & t & 0 \\ 0 & 0 & 0 & t \\ 0 & 0 & 0 & 0\end{pmatrix} = \begin{pmatrix} 1 & t & \dfrac{t^2}{2} & \dfrac{t^3}{3!} \\ 0 & 1 & t & \dfrac{t^2}{2} \\ 0 & 0 & 1 & t \\ 0 & 0 & 0 & 1\end{pmatrix}
$$

---

$A=\begin{pmatrix} 0 & t & 0 & 0 \\ 0 & 0 & t & 0 \\ 0 & 0 & 0 & t \\ 0 & 0 & 0 & 0\end{pmatrix} $ 라 하면, $A^2= \begin{pmatrix} 0 & 0& t^2 & 0 \\ 0 & 0 & 0 & t^2 \\ 0 & 0 & 0 & t \\ 0 & 0 & 0 & 0\end{pmatrix} ,\, A^3 = \begin{pmatrix} 0 & 0 & 0 & t^3 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0\end{pmatrix} ,\, A^4=0$ 이므로 $k\ge 4$ 이면 $A^k=0$ 이다. 따라서,
$$
\exp A= I+A+\dfrac{1}{2}A^2+\dfrac{1}{3}A^3
$$
이므로 주어진 식을 만족함을 쉽게 보일 수 있다.



<b>12. </b> 행렬 $\sigma_0 :=\begin{pmatrix}  1 & 0 \\ 0 & -1\end{pmatrix}$ 에 대하여,
$$
e^{t\sigma_0} \begin{pmatrix} a& b \\ c & d\end{pmatrix}e^{-t\sigma_0}=\begin{pmatrix}  a & e^{2t}b \\ e^{-2t}c &d\end{pmatrix}
$$
임을 보이고, 이 식을 미분하여
$$
\left[\sigma_0,\, \begin{pmatrix} a & b \\ c & d \end{pmatrix}\right]=2\begin{pmatrix}   0 & b \\ -c & 0\end{pmatrix}
$$
임을 보이라.

---

(1) $\sigma_0^2=I$ 이므로, 
$$
\begin{align}
\left(e^{t\sigma_0}\right)_{11}&=1+t+\dfrac{t^2}{2!}+\dfrac{t^3}{3!}+\cdots =e^{t}\\
\left(e^{t\sigma_0}\right)_{22}&=1-t+\dfrac{t^2}{2!}-\dfrac{t^3}{3!}+\cdots =e^{-t}\\
\left(e^{t\sigma_0}\right)_{21}&=\left(e^{t\sigma_0}\right)_{12}=0\\
\left(e^{-t\sigma_0}\right)_{11}&=1-t+\dfrac{t^2}{2!}-\dfrac{t^3}{3!}+\cdots =e^{-t}\\
\left(e^{-t\sigma_0}\right)_{22}&=1+t+\dfrac{t^2}{2!}+\dfrac{t^3}{3!}+\cdots =e^{t}\\
\left(e^{-t\sigma_0}\right)_{21}&=\left(e^{-t\sigma_0}\right)_{12}=0
\end{align}
$$
이다. 따라서
$$
e^{t\sigma_0} \begin{pmatrix} a& b \\ c & d\end{pmatrix}e^{-t\sigma_0}=\begin{pmatrix} e^t & 0 \\ 0 & e^{-t}\end{pmatrix} \begin{pmatrix}a & b \\ c & d\end{pmatrix}\begin{pmatrix} e^{-t} & 0 \\ 0 & e^{t}\end{pmatrix}  = \begin{pmatrix} a & e^{2t}b \\ e^{-2t}c & d\end{pmatrix}
$$
이다. 

(2) 행렬함수 $A(t)=(a_{ij}(t))$ 의 미분은 $A'(t)=(a_{ij}'(t))$ 로 정의된다. 그렇다면 $e^{At}$ 의 미분은?
$$
\left(e^{At}\right)_{ij}=\sum_{k=0}^\infty \dfrac{(A^k)_{ij}t^k}{k!} \implies \dfrac{d}{dt}\left(e^{At}\right)_{ij} =\sum_{k=0}^\infty\dfrac{(A^k)_{ij}t^{k-1}}{(k-1)!}=\sum_{l=0}^n A_{il} \left(\sum_{k=0}^\infty \dfrac{A^{k-1}_{lj} t^{k-1}}{(k-1)!} \right) = \sum_{l=0}^n A_{il} \left(e^{^{At}}\right)_{lj}=\left(Ae^{At}\right)_{ij}
$$
이다.  또한 행렬함수 $A(t),\,B(t)$ 가 행렬곱이 가능할 때 $A(t)B(t)$ 의 미분은,
$$
\dfrac{d}{dt}\left(A(t)B(t)\right)_{ij}= \dfrac{d}{dt}\sum_{l}A_{il}(t)B_{lj}(t) =\sum_l A'_{il}(t)B_{lj}(t)+A_{il}(t)B'_{lj}(t)= \left(A'(t)B(t)+A(t)B'(t)\right)_{ij}
$$
이다. 또한 
$$
\sigma_0 e^{t\sigma_0}=\sigma_0 \sum_{k} \dfrac{\sigma_0^k t^k}{k!}=\sum_{k}\dfrac{\sigma_0^k t^k}{k!}\sigma_0 = e^{t\sigma_0}\sigma_0
$$
이므로, 이를 이용하여 문제의 식의 좌 우변을 미분한 후 $t=0$ 을 취하면,
$$
\begin{align}
\dfrac{d}{dt} \left[e^{t\sigma_0} \begin{pmatrix} a& b \\ c & d\end{pmatrix}e^{-t\sigma_0}\right] &=\sigma_0 e^{t\sigma_0} \begin{pmatrix} a& b \\ c & d\end{pmatrix}e^{-t\sigma_0}-e^{t\sigma_0} \begin{pmatrix} a& b \\ c & d\end{pmatrix}\sigma_0e^{-t\sigma_0}\,,\\
\dfrac{d}{dt} \left[e^{t\sigma_0} \begin{pmatrix} a& b \\ c & d\end{pmatrix}e^{-t\sigma_0}\right]_{t=0} &=\sigma_0 \begin{pmatrix} a& b \\ c & d\end{pmatrix}-\begin{pmatrix} a& b \\ c & d\end{pmatrix}\sigma_0 =\left[\sigma_0,\,\begin{pmatrix} a& b \\ c & d\end{pmatrix}\right] \\
\dfrac{d}{dt}\begin{pmatrix} a & e^{2t}b \\ e^{-2t}c & d\end{pmatrix} &=\begin{pmatrix} 0 & 2e^{2t}b \\ -2e^{-2t}c & 0\end{pmatrix} \\
\dfrac{d}{dt}\begin{pmatrix} a & e^{2t}b \\ e^{-2t}c & d\end{pmatrix}_{t=0} &= 2\begin{pmatrix} 0 & b\\ -c & 0\end{pmatrix}
\end{align}
$$


