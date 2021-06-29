VII. 정사각행렬과 행렬식 #2
===



## 제 7 장 탐구문제



<b>1. </b> 임의의 $n$ 차 정사각행렬 $A,\,B$ 에 대하여 $B$ 가 가역이면
$$
e^{B^{-1}AB}=B^{-1}e^AB
$$
를 보이라.

---

우리는 제 3절 정리 3.4.2 에서 임의의 정사각 행렬 $A$ 에 대해 $e^{A}$ 를 정의할 수 있음을 알았다. 또한,
$$
(B^{-1}AB)^n = B^{-1}A^nB
$$
임은 쉽게 보일 수 있다. 따라서,
$$
e^{B^{-1}AB}=\sum_{k=0}^\infty \dfrac{(B^{-1}AB)^k}{k!}=B^{-1}\left(\sum_{k=0}^\infty \dfrac{A^k}{k!}\right)B=B^{-1}e^AB
$$
이다.



#### 이후 문제를 풀기 위한 Summary

우리는 제 6장 탐구문제 11번에서 선형변환이 단사일 필요충분조건이 전사임을 보였다. (이것은 유한차원벡터공간에서 항상 성립한다) 즉 선형사상이 단사이면 전단사이다. 또한 제 6장 탐구문제 12번에서 선형변환에 대한 역사상이 존재하면 역사상도 선형사상임을 보였다. 즉, 선형사상 $L:\mathbb{R}^n \to \mathbb{R}^m$ 이 단사이면 전단사이고 역사상도 선형사상이다. 

또한 선형사상$L : \mathbb{R}^n \to \mathbb{R}^m$ 이 단사일 필요충분 조건은 $L(X)=0$ 의 해가 $O$ 일 때 뿐임을 보았다.( 연습문제 6장 2절 4번). 

이를 정리하자. 



<b>S1.</b>  선형사상 $L: \mathbb{R}^n \to \mathbb{R}^m$ 에 대해 세 명제는 동치이다.

1. $L$ 은 단사이다.
2. $L$ 은 전사이다.
3. $L(X)=O$ 의 해는 자명해 뿐이다. 



<b>S2. </b> 선형사상 $L:\mathbb{R}^n \to \mathbb{R}^m$ 이 단사이면 역사상이 존재하며 이 역사상도 선형사상이다. 

(탐구문제, 연습문제에서 풀었으므로 증명은 필요 없을 것이다.)



<b>S3. </b>또한 제 5장 6절의 따름정리 6.4.2 를 다시 쓰면,

(1) $n$ 공간에서 $n+1$ 개 이상의 벡터들은 일차종속이다.

(2) $n$-공간에서 $k$ 개의 벡터가 일차독립이면 $k\le n$ 이다.

(3) $k$ 개의 벡터가 $n$ 공간을 생성하면 $k\ge n$ 이다.

(4) $k$ 개의 벡터가 $n$ 공간의 기저이면 $k=n$ 이다.



<b>2. </b> 만약 $n \ne m$ 이면, $n$ 차원 공간 $\mathbb{R}^n$ 과 $m$ 차원 공간 $\mathbb{R}^m$ 에는 전단사인 선형사상이 존재하지 않음을 보이라.

---

$n<m$ 이면 이 선형사상은 전사일 수 없다. $\mathbb{R}^n$ 의 basis 를 $\mathbf{a}_1,\ldots,\, \mathbf{a}_n$ 이라 하고 임의의 선형사상 $L:\mathbb{R}^n \to \mathbb{R}^m $ 에 대해 $\mathbf{b}_i = L(\mathbf{a}_i)$ 라 하자. 그렇다면 $L$ 에 의한 치역은 $L(\mathbf{a}_1),\ldots,\ldots,\,L(\mathbf{a}_n)$ 의 선형결합으로 생성되며 <b>S3.</b>(3) 에 따라 $R^m$ 을 생성 할 수 없다. 

$n>m$ 이면 이 선형사상은 단사 일 수 없다. $L(\mathbf{a}_1),\ldots,\,L(\mathbf{a}_n)$ 가 일차독립이려면 <b>S3.</b>(1) 의해 $n\le m$ 이어야 하는데 조건에 위배된다. 따라서 $L(\mathbf{a}_1),\ldots,\,L(\mathbf{a}_n)$ 은 일차종속이며, 따라서 $c_1L(\mathbf{a}_1)+\cdots c_n L(\mathbf{a}_n)=0$ 을 만족하는 nontrivial $(c_1,\ldots,\,c_n)$ 이 존재한다. 그런데,
$$
0=c_1L(\mathbf{a}_1)+\cdots c_n L(\mathbf{a}_n)=L(c_1\mathbf{a}_1+\cdots c_n\mathbf{a}_n)
$$
이므로 $L(X)=0$ 을 만족하는 $X\ne O$ 이 존재하므로 <b>S1.</b> 에 따라 $L$ 은 단사가 아니다. 

따라서 $n\ne m$ 이면 $\mathbb{R}^n$ 과 $\mathbb{R}^m$ 사이에는 전단사인 선형사상이 존재하지 않는다.



<b>3. </b> $n$ 차 정사각행렬 $A$ 가 역행렬을 가지지 않으면, $AB=O$ 이 되는, 영 아닌 $n$ 차 정사각행렬 $B$ 가 존재함을 보이라.

---

$A$ 가 역행렬을 가지지 않으면 $AY=O$ 를 만족하는 nontrivial $Y \in \mathbb{R}^n$ 가 존재함을 보이자.  $A$ 에 의해 표현되는 선형사상 $L_A:\mathbb{R}^n\to \mathbb{R}^n$ 을 생각하자. $X = (x_1,\ldots,\,x_n)^t\in \mathbb{R}^n$ 이고 $A=(a_{ij})$ 라 하면, $L_A(X)=AX$ 로 정의된다. 이제 $L_A$ 가 단사이면 (따라서 전단사이면) $L_A$ 의 역사상이 존재하며 이는 선형사상이다. 

이제 $A$ 가 역행렬을 가진다는 것과 $L_A$ 가 역사상을 가진다는 것이 동치임을 보이자. 

$A$ 가 역행렬 $A^{-1}$을 가진다고 하자. $L_A(X)=A(X)$ 이며 $(L_{A^{-1}}\circ L_{A})(X)=L_{A^{-1}}(AX)=A^{-1}AX=X$ 이며, 같은 방법으로 $(L_A \circ L_{A^{-1}})(X)=X$ 임을 보일 수 있다. 즉 $A^{-1}$ 에 의해 정해지는 $L_{A^{-1}}$ 은 $L_A$ 의 역사상이므로 행렬 $A$ 의 역행렬이 존재하면 $L_A$ 는 역사상을 가진다.

이제 $L_A$ 가 역사상을 가짐을 가정하자. 즉 $L_B \circ L_A = L_A \circ L_B = I_n$ 이므로 $BA=AB=I$ 인 $B$ 가 존재하는데 이는 정의상 $A$ 의 역행렬이다. 

그리고,  <b>S1.</b> 에 따라 $A$ 가 역행렬을 가진다는 것과 $AX=O$ 을 만족하는 $X$ 는 자명해 뿐이라는 것이 동치이다. 즉 $A$ 가 역행렬을 갖지 않으면 $AX=O$ 를 만족하는 비자명해가 존재한다. 이제 $B$ 의 각 열벽터를 $AX=O$ 을 만족하는 $\mathbb{R}^n$ 벡터들로 구성하면 $AB=0$ 이다.



<b>4. </b> 직교행렬의 행렬식의 값은 $1$ 또는 $-1$ 임을 보이라.

---

직교행렬은 $A^tA=I$ 를 만족하는 정사각행렬 $A$ 를 말한다. 우리가 $\det A^t=\det A$ 임을 보이면 $\det(I)=1=(\det A^t)(\det A)$ 이므로 $\det A= \pm 1$ 이다. 이제 $\det A^t = \det A$ 임을 보이자.
$$
\det A=\sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) A_{1\sigma(1)}\cdots A_{n\sigma(n)}
$$
이다. $\sigma$ 는 전단사함수이므로 항상 $\sigma^{-1}$ 이 존재하며 $\sigma^{-1}\in S_n$ 이다. 또한 모든 치환은 호환의 곱임을 알고 있다. (정리 4.1.2)  $\sigma = \tau_1\cdots \tau_n$ 이라 하면, $\tau_n \cdots \tau_1=\sigma^{-1}$ 이다. 따라서 $\operatorname{sgn}(\sigma)=\operatorname{sgn}(\sigma^{-1})$ 이다. 그리고, 임의의 $\sigma$ 에 대해 ($\sigma$ 가 전단함수임을 생각하면)
$$
A_{1\sigma(1)}\cdots A_{n\sigma(n)}=A_{\sigma^{-1}(1)1}\cdots A_{\sigma^{-1}(n)n}
$$
이다. 
$$
\begin{align}
\det A^{t}&=\sum_{\sigma \in S_n}\operatorname{sgn}(\sigma) A_{\sigma(1)1}\cdots A_{\sigma(n)n} \\
&=\sum_{\sigma^{-1}\in S_n} \operatorname{sgn}(\sigma^{-1}) A_{1\sigma^{-1}(1)} \cdots A_{n\sigma^{-1}(n)}\\
&=\sum_{\phi\in S_n} \operatorname{sgn}(\phi) A_{1\phi(1)}\cdots A_{n \phi(n)}=\det A

\end{align}
$$



<b>5. </b> 어떤 집합 $X$ 에서 정의된 함수 $y_1(x),\ldots,\,y_n(x)$ 에 대하여 항등식
$$
c_1y_1 + \cdots + c_n y_n(x)=0
$$
이 성립하는 경우가 자명한 상수인 경우 ($c_1=\cdots =c_n=0$)뿐이면, 힘수 $y_1,\ldots,\,y_n$ 을 일차독립이라고 부른다. 또 $y_1,\ldots,\,y_n$ 이 일차독립이 아니면, 일차종속이라고 부른다. 이제 실수체에서 정의된 함수
$$
1,\,x,\,x^2,\ldots,\,x^n
$$
는 일차독립임을 보이라. 또,
$$
1,\,\cos x,\, \cos 2x,\ldots,\, \cos nx,\,\sin x,\,\sin 2x,\ldots,\, \sin nx
$$
도 일차독립임을 보이라.

---

$$
c_0+c_1x+\cdots +c_nx^n=0
$$

이라 하자. 여기서 $0$ 은 실수 $0$ 이 아니라 $0$ 함수, 즉 모든 $x\in \mathbb{R}$ 에 대해 $f(x)=0$ 인 함수 $f$ 를 의미한다. 이것은 상수함수이므로 무한번 미분 가능하며 그 도함수는 모든 실수구간에서 $0$ 이다, $k$ 번 미분하고 $x=0$ 을 넣으면 $c_k=0$ 을 얻는다. 따라서 일차독립이다.

또한,
$$
g(x)=a_0+a_1\cos x + \cdots + a_n \cos nx + b_1\sin x + \cdots +b_n \sin nx=0
$$
이라 하자. 임의의 자연수 $m\ne n$ 에 대해,
$$
\begin{align}
\int_0^{2\pi} \cos mx  \cos nx
\,dx &=\dfrac{1}{2} \int_0^{2\pi}  \left[\cos (m+n)x + \cos(m-n)x\right]\,dx=0\\
\int_0^{2\pi} \sin mn \sin nx \, dx &= \dfrac{1}{2} \int_0^{2\pi} \left[ \cos (m-n)x - \cos (m+n)x\right]\, dx.=0
\\
\int_0^{2\pi} \sin mx \cos nx\,dx & = \dfrac{1}{2}\int_0^{2\pi} \left( \sin (m+n)x + \sin (m-n)x   \right)\,dx = 0\;,\\
\end{align}
$$
  이며 $m \ne 0$ 에 대해 
$$
\begin{align}
\int_0^{2\pi} \cos^2 mx \, dx & = \dfrac{1}{2} \int_0^{2\pi} (\cos 2mx +1)\,dx = \pi \\
\int_0^{2\pi} \sin^2 mx\, dx &=\dfrac{1}{2} \int_0^{2\pi} (1-\cos 2mx)\, dx = \pi

\end{align}
$$
임을 이용한다. 이제 $g(x)=0$ 이므로 임의의  $m\in \mathbb{N}$ 에 대해  $\displaystyle \int_0^{2\pi}g(x)\sin mx \, dx = \int_0^{2\pi} g(x) \cos mx\, dx=0$ 이다. 이를 이용하면
$$
0=\int_0^{2\pi}g(x) \sin mx\, dx = \pi b_m \implies b_m =0  \quad{\forall}m=1,\ldots,\,n\\
0 = \int_0^{2\pi} g(x) \cos mx\, dx = \pi a_m \implies a_m =0 \quad{\forall}m=1,\ldots,\,n6. 
$$
따라서  $g(x)=a_0=0$ 이므로 $ a_0=0$ 이다. 즉 일차독립이다.



<b>6. </b> 두 함수  $y_1,\,y_2 :\mathbb{R} \to \mathbb{R}$ 이 일차종속이면,
$$
W(y_1,\,y_2) :=\det \begin{pmatrix} y_1 & y_2 \\ y'_1 & y'_2 \end{pmatrix}
$$
가 항등적으로 $0$ 임을 보이라. 또 함수 $y_1,\, y_2,\,y_3$ 가 일차종속이면, 이들의 **Wronskian** 
$$
W(y_1,\,y_2,\,y_3):=\det \begin{pmatrix} y_1 & y_2 & y_3 \\  y_1' & y_2' & y_3' \\  y_1'' & y_2'' & y_3'' \end{pmatrix}
$$
가 항등적으로 $0$ 임을 보이라.

---

$y_1,\ldots,\,y_n$ 이 일차종속이면 $c_1y_1+\cdots + c_n y_n=0$ 을 만족하는 nontrivial $c_1,\ldots,\, c_n$ 이 존재한다. 이를 $k$ 번 미분해도 이 $(c_1,\ldots,\,c_n)$ 에 대해
$$
c_1 y_1^{(k)}+ \cdots+ c_n y_n^{(k)}=0
$$
이다. 정사각 행렬 $A_{ij}=y_j^{(i-1)}$  과 $C=\begin{pmatrix}c_1 & \cdots & c_n \end{pmatrix}^t$ 를 생각하면, $AX=0$ 의 nontrivial solution $C$ 가 존재하는 것이며 따라서  $\det A=0$ 이다. 





<b>7. </b> 행렬함수 
$$
A(X)=(a_{ij}(x))
$$
의 미분은 각 항의 미분으로 이루어진 행렬
$$
A'(x) =\left(a'_{ij}(x)\right)
$$
를 뜻한다. 이제
$$
\begin{align}
\dfrac{d}{dx} \det \begin{pmatrix} a_{11}(x) & a_{12}(x) & a_{13}(x) \\ a_{21}(x) & a_{22}(x) & a_{23}(x) \\ a_{31}(x) & a_{32}(x) & a_{33}(x) \end{pmatrix} &=  \det \begin{pmatrix} a_{11}'(x) & a'_{12}(x) & a'_{13}(x) \\ a_{21}(x) & a_{22}(x) & a_{23}(x) \\ a_{31}(x) & a_{32}(x) & a_{33}(x) \end{pmatrix} +  \det \begin{pmatrix} a_{11}(x) & a_{12}(x) & a_{13}(x) \\ a'_{21}(x) & a'_{22}(x) & a'_{23}(x) \\ a_{31}(x) & a_{32}(x) & a_{33}(x) \end{pmatrix}\\
&= \det \begin{pmatrix} a_{11}(x) & a_{12}(x) & a_{13}(x) \\ a_{21}(x) & a_{22}(x) & a_{23}(x) \\ a'_{31}(x) & a'_{32}(x) & a'_{33}(x) \end{pmatrix}


\end{align}
$$
임을 보이라.

---

$$

$$







<b>8. </b> $n$ 차 정사각행렬 전체의 집합을  $\mathcal{M}_n$ 이라고 두자 만약 함수 $f:\mathcal{M}_n\to \mathbb{R}$  이

(i) 임의의 $ A,\,B\in \mathcal{M}_n$ 에 대하여 $f(AB)=f(A)f(B)$ 이고,

(ii) 대각원이 차례로 $\lambda_1,\,1,\ldots,\, 1$ 로 주어진 임의의 대각행렬 $D_{\lambda}$ 에 대하여 $ f(D_\lambda)=\lambda$ 이면,

$f=\det $ 임을 보이라.

---

*임의의 정사각행렬은 대각화 가능한 두 행렬의 곱으로 나타냄을 보이면 된다고?????*





<b>9. </b> 좌표평면에서 행렬식 값이 $0$ 이 되지 않는 자기선형사상에 대하여, 타원의 상은 여전히 타원인가? 또 포물선이나 쌍곡선의 상은 여전히 타원인가?

---







<b>10. </b> (**수반행렬 (adjoint matrix)**) $n$ 차 정사각행렬 $A$ 의 $i$ 번째 행과 $j$ 번 째 쳘을 제거한 $n-1$ 차 정사각행렬을 $A_{ij}$ 라고 하였을 때, 임의의 $i$ 에 대하여
$$
\det A=\sum_{j=1}^n (-1)^{i+j} a_{ij}\det A_{ij}
$$
임을 보이라. 또 임의의 $j$ 에 대하여
$$
\det A = \sum_{i=1}^n (-1)^{i+j} a_{ij}\det A_{ij}
$$
임을 보이라. 또 $i \ne j$ 이면
$$
\sum_{k=1}^n (-1)^{j+k} a_{ik}\det A_{jk}=0=\sum_{k=1}^n (-1)^{j+k} a_{ki}\det A_{kj}
$$
임을 보이라. 이제 $(i,\,j)$ 항이 $(-1)^{i+j}\det A_{ji}$ 로 주어진 $n$ 차 정사각행렬 $\operatorname{adj} A$ 를 $A$ 의 수반행렬이라 하면,
$$
A(\operatorname{adj}A)=(\det A)I=(\operatorname{adj}A)A
$$
임을 보이라. 특히 $A$ 가 가역행렬이면,
$$
A^{-1}=\dfrac{1}{\det A} \operatorname{adj}A
$$
임을 보이라.

---

(1) 우리는 문제 4 에서 $\det A^t = \det A$ 임을 보였다. 이것은 행렬의 열에관한 정리 3.0.3과 따름정리 3.0.4가 행에 대해서도 그대로 성립함을 말한다. 여기서는 주로 행에 대한 연산을 말할 것이다. 

(2) $n$ 공간에서 $i$ 번 째 행은 $\displaystyle \sum_{j=1}^n a_{ij}\mathbf{e}_j$ 로 쓸 수 있다. 그리고 $i$ 번째 행이 $\mathbf{e}_j$ 일 때의 행렬식을 $\overline{A}_j$ 라 하자. 그렇다면
$$
\overline{A}_j = \begin{pmatrix} a_{11} &\cdots & a_{1(j-1)} & a_{1j} & a_{1(j+1)} & \cdots &a_{1n} \\ \vdots & & & & & &\vdots\\ 
a_{(i-1)1} & \cdots & a_{(i-1)(j-1)} &a_{(i-1)j} & a_{(i-1)(j+1)} & \cdots & a_{(i-1)n} \\
0 & \cdots & 0 &1 & 0 &\cdots & 0 \\
a_{(i+1)1} & \cdots & a_{(i+1)(j-1)} &a_{(i+1)j} & a_{(i+1)(j+1)} & \cdots & a_{(i+1)n} \\
\vdots & & & & & &\vdots\\ 
 a_{n1} &\cdots & a_{n(j-1)} & a_{nj} & a_{n(j+1)} & \cdots &a_{nn} 
\end{pmatrix}
$$
이다.  따름정리 3.0.4 (1) 의 행에 대한 응용에 의해,
$$
\det A = \sum_{j=1}^n a_{ij}\det(\overline{A_j}) \tag{10.1}
$$
이다. $i$ 번째 행을 첫째 행으로 그리고 1번부터 $i-1$ 번째 행까지는 행번호가 하나씩 늘어나는 행렬(즉 $i$ 번째 행이 맨 첫번째 행으로 바뀌고 1행부터 $i-1$ 행까지는 아래로 하나씩 밀리는 행렬)을 $A'_j$ 이라 하면,
$$
A'_j =  \begin{pmatrix}0 & \cdots & 0 &1 & 0 &\cdots & 0 \\
a_{11} &\cdots & a_{1(j-1)} & a_{1j} & a_{1(j+1)} & \cdots &a_{1n} \\ \vdots & & & & & &\vdots\\ 
a_{(i-1)1} & \cdots & a_{(i-1)(j-1)} &a_{(i-1)j} & a_{(i-1)(j+1)} & \cdots & a_{(i-1)n} \\

a_{(i+1)1} & \cdots & a_{(i+1)(j-1)} &a_{(i+1)j} & a_{(i+1)(j+1)} & \cdots & a_{(i+1)n} \\
\vdots & & & & & &\vdots\\ 
 a_{n1} &\cdots & a_{n(j-1)} & a_{nj} & a_{n(j+1)} & \cdots &a_{nn} 
 \end{pmatrix}
$$
 이고, 행끼리 $(i-1)$ 번의 치환을 한 것이므로, 따름정리 3.0.4 (2) 의 행에 대한 응용에 의해
$$
\det A'_j=(-1)^{i-1} \det \overline{A}_j
$$
이다. 이제 행렬의 첫행은 $\mathbf{e}_j$ 이다. 이제 $j$ 번째 열을 첫번째로 옮기고 $1$ 번 열부터 $j-1$ 번 열까지 뒤로 한칸씩 민 행렬을 $A''_j$ 라 하면
$$
A''_j =  \begin{pmatrix}1 &  0& \cdots &0 & 0 &\cdots & 0 \\
a_{1j} & a_{11} &\cdots & a_{1(j-1)} &  a_{1(j+1)} & \cdots &a_{1n} \\ \vdots & & & & & &\vdots\\ 
a_{(i-1)j} & a_{(i-1)1} & \cdots & a_{(i-1)(j-1)} &a_{(i-1)(j+1)} & \cdots & a_{(i-1)n} \\

a_{(i+1)j} & a_{(i+1)1} & \cdots & a_{(i+1)(j-1)} & a_{(i+1)(j+1)} & \cdots & a_{(i+1)n} \\
\vdots & & & & & &\vdots\\ 
a_{nj} & a_{n1} &\cdots & a_{n(j-1)} & a_{n(j+1)} & \cdots &a_{nn} 
 \end{pmatrix}
$$
이고, 행끼리 $j-1$ 번의 치환을 한 것이므로,
$$
\det A''_j = (-1)^{j-1} \det A'_j =(-1)^{i+j-2}\det \overline{A}_j=(-1)^{i+j}\det \overline{A}_j \tag{10.2}
$$
이다. 이제 $B$ 가 $n \times n$ 행렬이고 $B$ 의 첫 행이 $\mathbf{e}_1$ 인 행렬 일 때 $\det B$ 는 1행과 1열을 제거한 나머지 $(n-1)\times (n-1)$ 행렬 $B_0$ 의 행렬식과 같음을 보이자. 
$$
\operatorname{sgn}(\sigma) B_{1\sigma(1)}=\operatorname{sgn}(\sigma)\delta_{1,\sigma(1)}
$$
이며 $S_n$ 중 $\sigma(1)=1$ 인 것의 집합은 $\{2,\ldots,\,n\}$ 의 치환의 집합(을 $S'$ 이라 할 때) 과 전단사 대응이 존재하며 이 둘 의 $\operatorname{sgn}$ 함수값은 변하지 않음도 쉽게 알 수 있다. 즉   
$$
\det B = \sum_{\sigma\in S_n} \operatorname{sgn}(\sigma)B_{1\sigma(1)}\cdots B_{n\sigma(n)} =\sum_{\sigma'\in S'}\operatorname{sgn}(\sigma')B_{2\sigma'(2)} \cdots B_{n \sigma'(n)}=\det (B_0)
$$
이다. 그렇다면 $A''_j$ 의 1행과 1열을 제거한것은 문제에서 정의된 $A_{ij} 와 같으므로
$$
\det (A''_j)=\det A_{ij}
$$
이며, 식 (10.1), (10.2) 로 부터,
$$
\det A=\sum_{j=1}^n a_{ij}\det \overline{A}_j = \sum_{j=1}^n  (-1)^{i+j} a_{ij} \det A_{ij}
$$
임을 보였다. 



(3) (2) 번 과정을 열에 대해 수행하면 
$$
\det A = \sum_{i=1}^n (-1)^{i+j} a_{ij}\det A_{ij}
$$
를 얻을 수 있다.

(4) $i \ne j$ 라 하자.  $\displaystyle \sum_{k=1}^{n}(-1)^{j+k}a_{ik}\det A_{jk}$ 는 행렬 $A$ 의 $j$ 번째 행을 $i$ 번째 행으로 바꾼 행렬의 행렬식인데 이 행렬에 동일한 행이 존재하므로 이 행렬의 행렬식은 $0$ 이다. 또한 $\displaystyle \sum_{k=1}^n (-1)^{j+k} a_{ki}\det A_{kj}$ 는 행렬의 $j$ 번째 열을 $i$ 번째 열로 바꾼 행렬의 행렬식으로 그 값은 $0$ 이다. 따라서,
$$
\sum_{k=1}^n (-1)^{j+k} a_{ik}\det A_{jk}=0=\sum_{k=1}^n (-1)^{j+k} a_{ki}\det A_{kj}
$$
이다. 

(5) (4) 의 결과를 이용하면,
$$
\begin{align}
\left[A (\operatorname{adj}A)\right]_{ij} &= \sum_{k=1}^na_{ik}(\operatorname{adj}(A))_{kj}=\sum_{k=1}^n a_{ik}(-1)^{k+j}\det A_{jk}=\delta_{ij}\det A \\
\left[\operatorname{adj}(A) A\right]_{ij} &= \sum_{k=1}^n (\operatorname{adj}(A))_{ik}a_{kj}= \sum_{k=1}^n (-1)^{i+k}\det A_{ki} a_{ij}=\delta_{ij}\det A
\end{align}
$$
이므로 $A(\operatorname{adj}A)=(\det A) I=(\operatorname{adj}A)A$ 이다.

(6) $I=A \left(\dfrac{1}{\det A} \operatorname{adj} A\right) =  \left(\dfrac{1}{\det A} \operatorname{adj} A\right)A$ 이므로 $A$ 가 가역이면 $A^{-1}=\dfrac{1}{\det A} \operatorname{adj} A$ 이다.



<b>11. , 12.</b> 번은 생략.



<b>13. </b> (**크래머** 의 공식) $n$ 차 가역행렬 $A$ 와 $\mathbf{x}=\begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix}$ , $\mathbf{c}=\begin{pmatrix}c \\ \vdots \\ c_n \end{pmatrix}$ 에 대하여 방정식
$$
A\mathbf{x}=\mathbf{c}
$$
의 해는 
$$
x_j =\dfrac{\det (\mathbf{a}_1,\ldots, \mathbf{a}_{j-1},\, \mathbf{c},\,\mathbf{a}_{j+1},\ldots, \mathbf{a}_n)}{\det A} \qquad (j=1,\,2,\ldots,\,n)
$$
임을 보이라. 여기서 $\mathbf{a}_j$ 는 $A$ 의 $j$ 번째 열을 나타낸다.

---

$A$ 가 가역행렬이라는것과 문제 10의 결과를 이용하면,
$$
\mathbf{x}=A^{-1}\mathbf{c}=\dfrac{1}{\det A} (\operatorname{adj} A)\mathbf{c}
$$
이다. 행렬 $A$ 에서 $j$ 번째 열을 $\mathbf{c}$ 로 바꾼 것을 $A(j)$ 라 하면,
$$
\det A(j) =\sum_{k=1}^n (-1)^{j+k}A(j)_{kj} \det A(j)_{kj}=\sum_{k=1}^n (-1)^{j+k}c_k \det A_{kj}
$$
이다. 그렇다면, 
$$
\begin{align}
x_{j} = \dfrac{1}{\det A} \sum_{k=1}^n (-1)^{j+k}\det A_{kj}c_{k}=\dfrac{\det A(j)}{\det A}
\end{align}
$$




<b>14. </b> 정사각행렬 $A$ 의 각 항이 모두 정수이고 $\det A=1$ 이면 $A^{-1}$ 의 각 항도 모두 정수임을 보이라.

---

$\displaystyle \det A= \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma)a_{1\sigma(1)}\cdots a_{n \sigma(n)}$ 로 부터 우리는 각 항이 모두 정수인 정사각행렬 $A$ 에 대해 $\det A$ 도 정수임을 알 수 있다. $\det A=1$ 이면 가역행렬이고 $A^{-1}$ 의 $j$ 번째 열을 $X$ 라 하면 $AX=\mathbf{e}_j$ 임을 알 수 있다. 크라머의 공식으로 부터
$$
X_j = \sum_{k=1}^n (-1)^{j+k}\det A_{kj}\delta_{jk}=\det A_{jj}
$$
인데 $A_{jj}$ 역시 정수로 이루어진 행렬이므로 $\det A_{jj}$ 가 정수이고 따라서 $X$ 는 정수행렬이며,  $A^{-1}$ 역시 정수행렬이다.





<b>15. </b> $n$ 차 정사각행렬 $A$ 의 처음 $n-1$ 개의 행과 열로 이루어진 $n-1$ 차 행렬을 $B$ 라 두고
$$
A=\begin{pmatrix} B & C \\ C^t & d\end{pmatrix}
$$
로 두자. 이때 $B$ 가 가역이면
$$
\det A= (d-C^tB^{-1}C)\det B
$$
을 보이라. 또 $B$ 가 가역이 아니더라도
$$
\det A = d \cdot \det B - C^t(\operatorname{adj}B)C
$$
임을 보이라.

---

일단 
$$
\det A = d \cdot \det B - C^t(\operatorname{adj}B)C = \det B \left( d-C^t \dfrac{\operatorname{adj} B}{\det B} C \right)
$$
이며 $B$ 가 가역행렬이면 $B^{-1}=\dfrac{\operatorname{adj} B}{\det B}$ 이므로 $\det A = d \cdot \det B - C^t(\operatorname{adj}B)C$ 만 보이면 된다.
$$
\det A= \sum_{j=1}^n (-1)^{i+j}a_{ij}\det A_{ij}
$$
이며 $i=n$ 으로 놓으면 $a_{nn}=d$ 이고 $j\ne n$ 일 때 $a_{nj}=(C^t)_{j}$ 이므로
$$
\begin{align}
\det A &= \sum_{j=1}^n (-1)^{n+i}a_{nj}\det A_{nj}= (-1)^{2n}d \cdot\det B+\sum_{j=1}^{n-1} (-1)^{n+j}(C^t)_{j} \det(A_{nj})= d \cdot \det B +\sum_{j=1}^{n-1} (-1)^{n+j}(C^t)_{j} \det(A_{nj}) \tag{1}

\end{align}
$$
이다. $j<n$ 일 때, $\det(A_{nj})$ 는 행렬 $B$ 에서 $j$ 번째 열을 빼고 남은 $(n-1)\times (n-2)$ 행렬에 마지막 열로 $C$ 를 넣은 행렬의 행렬식이다.  



--- to be done--





<b>16. </b> 
$$
\det \begin{pmatrix} 1 & 2 & 1 \\ 2 & 5 & 3 \\ 8 & 2& 5\end{pmatrix} \equiv 0 \quad \operatorname{mod}\; 11
$$
임을 보이라.

---

첫번째 행에 100을 곱한것과 두번째 행에 10을 곱한것과 세번째 행을 더하여 세번째 행에 두더라도 행렬식 값은 바뀌지 않는다. 따라서,
$$
\det \begin{pmatrix} 1 & 2 & 1 \\ 2 & 5 & 3 \\ 8 & 2& 5\end{pmatrix} =\det \begin{pmatrix} 1 & 2 & 121 \\ 2 & 5 & 253 \\ 8 & 2& 825\end{pmatrix}
$$
이다. 행렬식의 각 term 에는 121, 253, 825 중 하나가 들어가는데 이는 모두 11로 나누어 떨어지는 수이다. 따라서 증명 끝.



<b>17. </b> 격자 $L$ 의 한 기저를 $\mathbf{v}_1,\ldots,\,\mathbf{v}_k$ 라 하고 또 다른 기저를 $\mathbf{w}_1,\ldots,\,\mathbf{w}_k$ 라고 하자. 이 때,
$$
\mathbf{w}_j = \sum_{i=1}^n a_{ij}\mathbf{v}_i
$$
로 두었을 때,
$$
|\det (a_{ij})|=1
$$
임을 보이라.

----

$\{\mathbf{v}_1,\ldots,\,\mathbf{v}_k\}\in L$ 이며 $\{\mathbf{w}_1,\ldots,\,\mathbf{w}_k\}\in L$ 이므로 $a_{ij}\in \mathbb{Z}$ 이어야 한다. $A=(a_{ij})$ 라 하면 $A$ 는 가역행렬 이어야 하며 같은 이유로 $A^{-1}$ 도 정수행렬이어야 한다. 따라서 $\det A$ 와 $\det A^{-1}$ 이 정수이다. 그런데 $(\det A ) (\det A^{-1})=1$ 이어야 하므로 가능한 값은 $\det A=\pm 1$ 뿐이다.



<b>18. </b> 



<b>19. </b> 모든 정사각행렬은 가역행렬로 이루어진 수열의 극한값임을 설명하여라.

---

가역행렬이 아닌 행렬에 대해서만 생각하면 된다. 예를 들어 생각해보자. $O$ 행렬의 경우는 $\displaystyle \lim_{k \to \infty}\dfrac{1}{k} I_n$ 이며 대각행렬의 경우는 비가역 행렬이면 대각성분에 $0$ 이 존재하므로 $0$ 을 $\dfrac{1}{k}$ 로 바꾸고 $\displaystyle \lim_{k \to \infty}$ 를 취하면 된다.

 $n \times n$ 행렬 $A$ 의 각 열을 $A_i$ 라 하자. $A$ 가 비가역 행렬이면 $\{A_1,\ldots,\, A_n\}$ 중에 일차종속인 것이 존재한다. 이제 여기서 일차독립인 수열은 남겨놓고, 이것으로부터 이것들과 일차독립인 벡터들을 모아 $n$ 공간의 basis 를 구성 할 수 있다. 이를 $B_1,\ldots,\,B_m$ 이라 하자. 즉 $\{A_1,\ldots,\,A_n\}$ 에는 일차독립인 벡터 $n-m$ 개가 있고, 이들과 일차종속인 열벡터 $m$ 개가 있다. 이 일차종속인 열벡터에 순서대로 $\dfrac{1}{k}B_1,\ldots,\dfrac{1}{k}B_k$ 를 더한 행렬 $D_k$ 를 생각한다. 즉 $A_p$ 가 일차종속인 $j$ 번째 열벡터이면 $D_k$ 의 $p$ 번째 열벡터는 $A_p+\dfrac{1}{k}B_j$ 이다. 

당연히 $D_k$ 의 열벡터들은 서로 일차독립이 되며 따라서 $D_k$ 는 가역행렬이고 $\displaystyle \lim_{k \to \infty}D_k = A$ 이다. 



<b>20. </b> $n$-벡터 $\mathbf{v}_1,\ldots,\,\mathbf{v}_n$ 에 대하여 
$$
\det (\mathbf{v}_1,\ldots,\,\mathbf{v}_n)>0
$$
 이면, 기저 $(\mathbf{v}_1,\ldots,\,\mathbf{v}_n)$ 은 **양으로 향하여** 있다고 부르고,
$$
\det (\mathbf{v}_1,\ldots,\,\mathbf{v}_n)<0
$$
이면 $(\mathbf{v}_1,\ldots,\,\mathbf{v}_n)$ 은 **음으로 향하여** 있다고 부른다. 이제 벡터 $\mathbf{v}_1,\ldots,\,\mathbf{v}_n$ 이 시각에 따라 연속적으로 변한다고 하자. 시각 $t=0$ 일 때 이들이 양으로 향하여 있고 시각 $t=1$ 일 때 음으로 향하여 있으면, 어느 시각에서 $\mathbf{v}_1,\ldots,\mathbf{v}_n$ 이 일차종속임을 보이라.

---

말인 즉슨 어느 시각에서 $\det (\mathbf{v}_1,\ldots,\,\mathbf{v}_n)=0$ 이 된다는 뜻이다. $\mathbf{v}_1(t)=(v_{11}(t),\ldots,\,v_{1n}(t))$  라 하자. 뒤에 배우겠지만 $\mathbf{v}_1(t)$ 가 $t$ 에 대해 연속적으로 변한다는 것은 각 $v_{11}(t),\ldots,\,v_{1n}(t)$ 가 모두 시간에 대해 연속적이란 말과 동치이다. (9.1 매개화된 곡선 을 보라.)  

이렇게 $\mathbf{v}_k(t) = (v_{k1}(t),\ldots,\, v_{kn}(t))$ 로 정의하고 행렬 $V(t)=(v_{ij}(t))$ 라 정의하자. 문제의 조건에 의해 $v_{ij}(t)$ 가 연속함수이며 $\det V(t)$ 는 이런 $v_{ij}(t)$ 의 유한개의 곱들의 합이므로 $\det V(t)$ 는 $t$ 에 대한 연속함수이다. (당연하겠지?)

이제 $\det V(t=0)>0$ 이며 $\det V(t=1)<0$ 이고 $\det V(t)$ 는 연속함수 이므로 평균값 정리에 의해 어떤 $t_0\in (0,\,1)$ 에서 $\det V(t_0)=0$ 이다. 즉 $ (\mathbf{v}_1(t_0),\ldots,\,\mathbf{v}_n(t_0))$ 은 일차종속이다. 



<b>21. </b> 표준단위벡터 $\mathbf{e}_1,\ldots,\,\mathbf{e}_n$ 에 대하여 $n$ 공간의 기저 $(\mathbf{e}_1,\ldots,\,\mathbf{e}_n)$ 양으로 향해 있음을 보이라.

---

trivial.



<b>22. </b> 임의의 $n$ 차 정사각행렬 $A,\,B$ 에 대하여, $B$ 가 가역이면,
$$
(B^{-1}AB)^k = B^{-1}A^kB \qquad (k=1,\,2,\,3,\ldots)
$$
임을 보이라. 임의의 다항식 $p(x)$ 에 대하여,
$$
p(B^{-1}AB)=B^{-1}p(A)B
$$
임을 보이라.

---

(1) 우선 induction으로 증명한다. $k=1$ 일 때 자명하다. $n$ 일 때 성립함을 가정한다.
$$
(B^{-1}AB)^{n+1}=(B^{-1}AB)^n B^{-1}AB=B^{-1}A^nBB^{-1}AB=B^{-1}A^{n+1}B
$$
이다. 

(2) $p(x)=a_0 + a_1x+\cdots +a_nx^n$ 이면,
$$
\begin{align}
p(B^{-1}AB)&=a_0 + a_1(B^{-1}AB)+ a_2(B^{-1}AB)^2 + \cdots + a_n (B^{-1}AB)^n \\
&=a_0 +a_1(B^{-1}AB)+a_2B^{-1}A^2B+\cdots + a_n B^{-1}A^nB\\
&=B^{-1}(a_0 +a_1A+a_2 A^2+\cdots + a_nA^n)B^{-1}\\
&=B^{-1}p(A)B^{-1}
\end{align}
$$


<b>23. </b> $n$ 차 정사각행렬 $A,\,B$ 에 대하여 $B$ 가 가역이면
$$
\operatorname{tr} (B^{-1}AB)=\operatorname{tr}A
$$
임을 보이라.

---

우선 $n$ 차 정사각행렬 $A,\,B$ 에 대해 $\operatorname{tr}(AB)=\operatorname{tr}(BA)$ 임을 안다. $B^{-1}A$ 도 $n$ 차 정사각행렬이므로, 
$$
\operatorname{tr}(B^{-1}AB)=\operatorname{tr}(ABB^{-1})=\operatorname{tr}(A)
$$
.



