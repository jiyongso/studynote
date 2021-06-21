VII. 정사각행렬과 행렬식 #1
===



## 연습문제 : 제 7장 1절



<b>1. </b> $n$ 차 정사각행렬 $A,\,B$ 에 대하여 $AB=O$ 이면 $BA=O$ 인가?

---

No. For example, $A=\begin{pmatrix} 0 & 0 & 1 \\ 0 & 0 & 1 \\ 0 & 0 & 0\end{pmatrix}, B=\begin{pmatrix} 0 & 0 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 0\end{pmatrix}$ 이면 $AB=\begin{pmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0\end{pmatrix},  BA=\begin{pmatrix} 0 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0\end{pmatrix}$ 



<b>2. </b> 행렬 $A=\begin{pmatrix} 1 & 2 & 0 \\ 2 & 3 & 0 \end{pmatrix} ,\, B=\left(\begin{array}{rr} -3 & 2 \\ 2 & -1 \\ 0 & 0\end{array}\right)$ 에 대하여 $AB=I$ 를 보이라. 이 때 $BA=I$ 인가?

---

$BA=\begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0\end{pmatrix}$. 



<b>3. </b> $n$ 차 가역행렬 $A$ 에 대하여
$$
\left(A^{-1}\right)^{-1}=A,\qquad \left( A^{-1} \right)^k = \left( A^k \right)^{-1}, \qquad (k=1,\,2,\,3,\ldots)
$$
임을 보이라. 또 전치행렬 $A^t$ 도 가역임을 보이고, 이때,
$$
\left( A^{t}\right)^{-1}=\left(A^{-1}\right)^t
$$
임을 밝히라. 또 $B$ 가 $n$ 차 가역행렬이면
$$
\left(AB\right)^{-1}=B^{-1}A^{-1}
$$
임을 보이라.

---

(1) $A^{-1}A=I$ 이므로 $\left( A^{-1} \right)^{-1}=A$ 이다. 

(2) $\underbrace{A^{-1}\cdots A^{-1}}_{k-\text{times}} \underbrace{A \cdots A}_{k-\text{times}} =\underbrace{A^{-1}\cdots A^{-1}}_{(k-1)-\text{times}} \underbrace{A \cdots A}_{(k-1)-\text{times}}=\cdots= A^{-1}A=I$  

(3) $B$ 를 $A^{-1}$ 이라 하면, $AB=BA=I$ 이므로, $ I^t=I=(AB)^t=B^tA^t$, $I^t=I=(BA)^t=A^tB^t$ 이다. 따라서 $\left(A^{t}\right)^{-1}=\left(A^{-1}\right)^t$ 이다. 

(3) $AB(B^{-1}A^{-1})=(B^{-1}A^{-1})AB=I$ 이므로 $(AB)^{-1}=B^{-1}A^{-1} $ 이다.



<b>4. </b> 행렬 $\begin{pmatrix} 0 & 0 & 1\\ 0 & 2 & 0 \\ 3 & 0 & 0 \end{pmatrix}$ 의 역행렬을 보여라. 

----

주어진 행렬을 $A$ 라 하고 역행렬을 $B=\begin{pmatrix} a & b & c\\ d&e&f \\g & h & i\end{pmatrix}$ 라 하면, $AB=\begin{pmatrix} g & h & i \\2d & 2e & 2f \\ 3a & 3b & 3c\end{pmatrix} = I$ 이므로, $a=0,\,b=0,\,c=1/3,\, d=0, \, e=1/2,\, f=0,\, g=1,\, h=0,\, i=0$ 이다. 즉
$$
\begin{pmatrix}0 & 0 & \frac{1}{3} \\ 0 & \frac{1}{2} & 0 \\ 0 & 0 & 1\end{pmatrix}
$$
이다.



## 연습문제 : 제 7장 2절 



없음





## 연습문제 : 제 7장 3절



<b>2. </b> 좌표평면 위의 두 벡터 $\mathbf{x},\, \mathbf{y}$ 가 이루는 평행사변형
$$
\{s\mathbf{x}+t\mathbf{y}:0 \le s,\,t \le 1\}
$$
의 넓이는 $|\det(\mathbf{x},\,\mathbf{y})|$ 임을 보이라.

----

연습문제 5장 3절 5번에 의해 면적 $S=\sqrt{|\mathbf{x}|^2|\mathbf{y}|^2-(\mathbf{x}\cdot \mathbf{y})^2}$ 이다. $\mathbf{x}=(x_1,\,\mathbf{x}_2),\, \mathbf{y}=(y_1,\,y_2)$ 라 하면,
$$
S=\sqrt{(x_1^2+x_2^2)(y_1^2+y_2^2)-(x_1y_1+x_2y_2)^2} =\sqrt{(x_1y_2-x_2y_1)^2}=|x_1y_2-x_2y_1|=|\det(\mathbf{x},\, \mathbf{y})|
$$
이다. 



<b>3. </b> 좌표평면에서 네 점 $(0,\,0),\, (1,\,0),\, (3,\,1),\, (2,\,3)$ 을 꼭지점으로 가지는 볼록사각형의 넓이는
$$
\left|\det \begin{pmatrix} 1 & 0 \\ 3 & 1 \end{pmatrix} + \det \begin{pmatrix}  3&1\\ 2 & 3 \end{pmatrix} \right| = \dfrac{1}{2}(1+7)=4
$$
임을 보이라. 일반적으로 평면의 점 $A_1,\,A_2,\,\ldots,\,A_n,\,A_1$ 을 차례로 연결한 평면다각형의 넓이는
$$
\dfrac{1}{2}\left|\det(A_1,\,A_2) + \cdots + \det (A_{n-1},\,A_n)+\det(A_n,\,A_1)\right|
$$
임을 보이라.

---



-- 이거 지금까지 배운걸로 풀 수 있는거 맞아? 각 삼각형의 determinant의 부호가 같다는걸 보여야 하는데..



<b>4. </b> 좌표평면의 벡터 $\mathbf{x},\,\mathbf{y}$ 가 이루는 평행사변형의 넓이를 $\operatorname{area}(\mathbf{x},\,\mathbf{y})$ 라고 두었을 때, 2차 정사각행렬 $A$ 에 대하여
$$
\operatorname{area}(L_A(\mathbf{x}),\,L_A(\mathbf{y}))=|\det A|\operatorname{area}(\mathbf{x},\,\mathbf{y})
$$
임을 보이라.

---

$L_A(x_1,\,x_2)=(ax_1+bx_2,\, cx_1+dx_2),\, \mathbf{x}=(x_1,\, x_2),\, \mathbf{y}=(y_1,\, y_2)$ 라 하자. $B,\,C$ 가 $n\times n$ 행렬일 때 $\det(BC)=\det(B)\det(C)$ 임을 알고 있으며, $\operatorname{area}(\mathbf{x},\,\mathbf{y})=|\det (\mathbf{x},\,\mathbf{y})|$ 임을 알고 있다. 
$$
\begin{align}
\operatorname{area}(L_A(\mathbf{x}),\,L_A(\mathbf{y}))=\left|\det \begin{pmatrix} ax_1+bx_2  & cx_1+dx_2 \\ ay_1+by_2 & cy_1+dy_2\end{pmatrix} \right|=\left| \det \left[\begin{pmatrix}x_1 & x_2 \\ y_1 & y_2 \end{pmatrix}\begin{pmatrix}a & b \\ c & d \end{pmatrix} \right]\right|=|\det A| \operatorname{area}(\mathbf{x},\,\mathbf{y})

\end{align}
$$


<b>5. </b> 좌표평면에서 원판 $x^2+y^2\le 1$ 이 선형변환 $\begin{pmatrix} 2 & 0 \\ 0 & 3\end{pmatrix}$ 에 의하여 변화된 상의 넓이를 구하라. 또 넓이가 $A$ 인 영역은 이 선형변환에 의하여 넓이가 얼마인 영역이 되는가?

---

이 선형변환을 $L$ 이라 하면 $L(x,\,y)=(2x, 3y)$ 이다. $x'=2x,\,y'=3y$ 이므로 $\dfrac{x^2}{2^2}+\dfrac{y^2}{3^2}\le 1$ 인 영역이 된다. 이는 타원의 면적으로 $2\times 3 \times \pi = 6\pi$ 이다. 

-- 아직 일반화된 면적의 변화까지는 안배운것 같은데...



<b>6. </b> $n$ 차 정사각행렬 $A$ 와 실수 $c$ 에 대하여 $\det (cA)$ 는 $\det (A)$ 의 몇배인가?

---

$A$ 의 $i$ 번째 열을 $A_i$ 라 하면 $\det (cA) = \det (cA_1,\,cA_2,\ldots,\,cA_n)$ 이다. 정리 3.0.3을 이용하면,
$$
\det (cA_1,cA_2,\ldots,\,cA_n)=c\det(A_1,\,cA_2,\ldots,\,cA_n)=c^2\det (A_1,\,A_2,\ldots,\,cA_n)=\cdots = c^n\det(A_1,\ldots,A_n)=c^n\det A
$$


<b>7. </b> 다음을 보이라..

---

생략.



## 제 4절 부록



<b>4.1.3 기본연습문제</b>

3. 호환들 중에서 인접한 항을 바꾸는 것, 즉 $(i\;\; i+1)$ 을 인접호환 이라고 부르자. 이때 임의의 호환은 홀수개의 인접호환으로 나타남을 보이라.
4. 모든 치환은 인접호환의 곱으로 나타남을 증명하라

---

*(proof 3 )* $(i \;\;j)$ 을 생각하자. $(i\;\;j)=(j\;\;i)$ 이므로 $i<j$ 라 두어도 상관 없다. $j-i=n$ 으로 놓고 $n$ 에 대한 induction을 사용한다. $n=1$ 일 때는 인접호환이므로 성립한다. $n$ 일 때 성립함을 가정하자. $(i\;\; i+n+1)=(i\;\;i+1)(i+1\;\;i+n)(i\;\;i+1) $ 이다. $(i\;\;i+1)$ 은 인접호환이고 $(i+1\;\;i+n)$ 은 가정에 의해 홀수개의 인접호환으로 나타낼 수 있으므로 $(i \;\;i+n+1)$ 은 홀수개의 인접호환으로 나타 낼 수 있다.

*(proof 4)* 정리 4.1.2 에 의해 모든 치환은 호환의 곱으로 나타나며 3. 에 의해 모든 호환은 홀수개의 인접호환의 곱으로 나타나므로 모든 치환은 인접호환의 곱으로 나타난다.



<b>4.1.5  기본연습문제</b> 호환 $(i\;\;j)$ 의 전도의 수는 $2|i-j|-1$ 임을 보여라.

---

$(i,\,j)=(j,\, i)$ 이므로  $i<j$ 라 가정하자. $\sigma(i)$ 가 $\sigma(i+1),\cdots,\ \sigma(j)$ 보다 크므로 일단 $j-i$ 개. $\sigma(i+1)$ 부터 $\sigma(j-1)$ 까지 $\sigma(j)$ 보다 크므로 $j-i-1$ 개. 따라서 $2(j-i)-1$ 개이다. $j<i$ 이면 $2(i-j)-1$ 이므로  $2|i-j|-1$ 개이다.



<b> 정리 4.1.6</b>  임읭 치환 $\sigma$ 와 호환 $\tau$ 에 대하여
$$
N(\sigma \tau)\equiv N(\sigma)+1 \;\operatorname{mod}\;2
$$
이다.

---

*(proof)* 우선 $\tau$ 가 인접호환 $(k,\, k+1)$ 인 경우를 보자. $N(\sigma\tau)$ 와 $N(\sigma)$ 의 차이는 $\tau$ 에 의해서 $\sigma(\tau (k))=\sigma(k+1),\, \sigma(\tau (k+1))=\sigma (k)$ 로 변하는 것이다. 즉
$$
\sigma \tau =\begin{pmatrix} 1 & 2 & 3 & \cdots & k & k+1 & \cdots & n\\ \sigma(1) & \sigma(2) & \sigma(3) &\cdots &\sigma(k+1) & \sigma(k) & \cdots & \sigma(n)\end{pmatrix}
$$

- $i<k$ 일 때는 $\sigma(i)$ 이후애 $\sigma(i)$ 보다 작은 항들의 갯수는 변화가 없다.

- $i>k+1$ 일 때에도 $\sigma(i)$ 이후에 $\sigma(i)$ 보다 작은 항들의 갯수는 변화가 없다.

- $\sigma(k)$ 이후에 $\sigma(k)$ 보다 작은 것의 갯수를 $M_k$ $\sigma(k+1)$ 이후에 $\sigma(k+1)$ 보다 작은 것의 갯수를 $M_{k+1}$ 이라 하자. $\sigma(k)<\sigma(k+1)$ 이라면 $\sigma\tau(k)$ 이후에 $\sigma\tau(k)$ 보다 작은 것의 갯수는 변함없이 $M_k$ 이며 $\sigma\tau(k+1)$ 이후에 $\sigma\tau(k)$ 보다 적은것이 하나 늘었으므로  $M_k+1$ 이다. $\sigma(k+1)<\sigma(k)$ 라면 $\sigma\tau(k)$ 이후에 $\sigma\tau (k)$ 보다 적은것이 하나 줄고, $\sigma\tau(k+1)$ 이후에 $\sigma(\tau)(k+1)$ 이후에 는 변화가 없으므로,
  $$
  N(\sigma \tau)=N(\sigma) \pm 1
  $$
  이다.

즉 임의의 인접호환마다 전도의 수는 하나씩 줄거나 늘어난다.

임의의 호환은 홀수개의 인접호환의 곱이므로 전도의 수는 홀수만큼 늘거나 준다. 따라서
$$
N(\sigma \tau)\equiv N(\sigma) +1\qquad \operatorname{mod}\;2
$$
이다. $\square$



<b>정리 4.1.8  </b> 자연수 $k,\,k'$ 과 호환 $\tau_1,\ldots,\,\tau_k,\,\tau'_1,\ldots,\,\tau'_{k'}$ 에 대하여
$$
\tau_1 \cdots \tau_k = \tau'_1\cdots \tau'_{k'}
$$
이면
$$
k \equiv k \quad \operatorname{mod}\; 2
$$
이다.

---

*(proof)* 우리는 
$$
\tau'_{k'}\cdots \tau'_{1}\tau_1 \cdots \tau_k = \operatorname{id}
$$
임을 안다. $N(\operatorname{id})=0$ 이므로 
$$
0=N(\operatorname{id})=N(\tau_{k'}\cdots \tau'_1\tau_1\cdots \tau_k) \equiv N(\tau'_{k'}\cdots \tau
'_1 \tau_1 \cdots \tau_{k-1})+1\quad \operatorname{mod}\;2 \equiv\cdots \equiv k+k' \quad \operatorname{mod}\; 2
$$
이다. 즉
$$
k \equiv k' \quad \operatorname{mod}\;2
$$
이다. 



<b>정리 3.0.3 의 증명</b>

$n\times n$ 정사각행렬 $A$ 의 행렬식 $\det A$ 는 $A$ 의 각 열 $A_1,\ldots,\,A_n$ 의 함수로 $\det(A_1,\ldots,\,A_n)$ 으로 표현 할 수 있다. 이 때 행렬식 
$$
\det : \mathbb{R}^n \times \cdots \times \mathbb{R}^n \to \mathbb{R}
$$
은 

(1) 각 열에 대한 선형사상이다. 즉 임의의 실수 $t,\,t'$ 에 대해
$$
\det(A_1,\dots,\,A_{i-1}, tA_i + t'A'_i ,\, A_{i+1},\ldots,\, A_n)=t\det(A_1,\ldots,\,A_{i-1},\,A_i, A_{i+1},\ldots, \,A_n)+ t'\det(A_1,\ldots,\,A_{i-1},\,A'_i, A_{i+1},\ldots, \,A_n)
$$
이다.

(2) 두 열을 바꾸면 부호가 바뀐다. 즉 $i<j$ 에 대하여,
$$
\det(A_1,\ldots,\,A_i,\,\ldots,\,A_j,\ldots,\,A_n)=-\det(A_1,\ldots,\,A_j,\ldots,\,A_i,\ldots,\,A_n)
$$
이다. 

역으로 함수 $f:\mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}$ 이 위의 성질 (1) 과 (2) 를 만족시키면, 임의의 정사각행렬 $A$ 에 대하여
$$
f(A)=f(I)\det A
$$
이다.

---

*(proof)* 행렬식의 정의는 
$$
\det A=\sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) A_{1\sigma(1)}\cdots A_{n\sigma(n)}
$$
이다. 



함수  $f$ 가 성질 (1), (2)를 가진다면 따름정리 3.0.4 를 만족함을 보이자.

$i<j$ 에 대해 $ A_i=A_j$ 라 하자. 
$$
\det (\ldots,\,A_i,\ldots,\,A_j=A_i ,\ldots)=\det(\ldots, A_i -A_j,\ldots, A_j,\ldots)=\det(\dots,\,0,\ldots, A_j,\ldots)=0
$$
  이므로 서로 다른 열이 같은 벡터의 정사각행렬은 $0$ 이다.  $i\ne j$ 에 대해, 
$$
\det (\ldots ,A_i+tA_j,\ldots, A_j,\ldots)=\det(\ldots,A_i,\ldots,\,A_j,\ldots )+ t\det(\ldots,\,A_j,\ldots,\,A_j,\ldots)=\det(\ldots,\,A_i,\ldots,\,A_j,\ldots)=\det A
$$
이므로 정사각행렬에 어떤 열의 벡터를 상후배하여 다른 열에 더하더라도 행열식의 값은 변화가 없다. 

이제 열벡터  $A_j = \displaystyle \sum_{i=1}^n a_{ij}\mathbf{e}_i$ 라 쓰자. 그렇다면,
$$
\begin{align}
f(A)&= f\left(\sum_{i_1=1}^n a_{i_11}\mathbf{e}_{i_1}, \, \sum_{i_2=1}^n a_{i_22}\mathbf{e}_{i_2},\ldots,\, \sum_{i_n=1}^n a_{i_nn}\mathbf{e}_{i_n}\right) \\
&= \sum_{i_1=1}^n a_{i_11}f\left(\mathbf{e}_{i_1}, \, \sum_{i_2=1}^n a_{i_22}\mathbf{e}_{i_2},\ldots,\, \sum_{i_n=1}^n a_{i_nn}\mathbf{e}_{i_n}\right) \\
&= \sum_{i_1=1}^n \cdots \sum_{i_n=1}^n a_{i_11} \cdots a_{i_n n} f\left(\mathbf{e}_{i_1},\ldots, \mathbf{e}_{i_n}\right)\\
&=\sum_{\sigma \in S_n} a_{\sigma(1)1}\cdots a_{\sigma(n)n } f(\mathbf{e}_{\sigma(1)},\ldots,\, \mathbf{e}_{\sigma(n)})\\
&=\sum_{\sigma\in S_n}\operatorname{sgn}(\sigma)a_{\sigma(1)1}\cdots a_{\sigma(n)n} f(\mathbf{e}_1,\ldots,\,\mathbf{e}_{\sigma(n)})\\
&= f(I)\det A^t\\
&=f(I)\det A
\end{align}
$$


<b>정리 4.2.2</b> $n$ 벡터 $\mathbf{a}_1,\ldots,\,\mathbf{a}_n$ 이 일차독립일 필요충분조건은
$$
\det (\mathbf{a}_1,\ldots,\,\mathbf{a}_n) \ne 0
$$
이다. 

---

*(proof)* $n$ 벡터 $\mathbf{a}_1,\ldots, \mathbf{a}_n$ 이 일차독립이면 표준단위벡터  $\mathbf{e}_1,\ldots,\,\mathbf{e}_n$ 이 모두  $\mathbf{a}_1,\ldots,\,\mathbf{a}_n$ 의 일차결합으로 표시된다. 따라서,
$$
\mathbf{e}_j=\sum_{i=1}^n \mathbf{a}_ib_{ij}
$$
로 쓸 수 있다. 이제 $ A=(\mathbf{a}_1,\ldots,\,\mathbf{a}_n),\, B=(b_{ij})$ 로 두면 $I=AB$ 이며, 따라서,
$$
1=\det (I)=\det(AB)=(\det A)(\det B)
$$
가 되므로 $\det A\ne 0$ 이다. 

만약  $\mathbf{a}_1,\ldots,\,\mathbf{a}_n$ 이 일차종속이면 이중 어느 하나는 나머지 하나의 일차결합이므로 $\det A=0$ 이다. 





## 연습문제  : 제 7 장 4절



<b>1. </b> $n$  치환 중에서 짝치환인 것의 갯수와 홀치환인 것의 갯수를 구하라.

----

 모든 원소가  $1$ 인 $n \times n$ 행렬  $A$ 를 생각하면  $\det A=0$ 임은 자명하다. 그런데 $A$ 의 행렬식은 정의에 의해
$$
\det A=\sum_{\sigma\in S_n}\operatorname{sgn}(\sigma) =[\text{짝치환의 갯수}]-[\text{홀치환의 갯수}]=0
$$
이므로 홀치환의 갯수 와 짝치환의 갯수는 같으며 둘의 합이 $n!$ 이므로 각각 $\dfrac{n!}{2}$  이다.



<b>2. </b> 치환  
$$
\sigma(k)=16-k\qquad (k\in \{1,\,2,\ldots,\,15\})
$$
는 홀치환임을 보이라.

---

$$
\sigma(k)=\begin{pmatrix} 1 & 2 & \cdots & 14 & 15 \\ 15 & 14 &\cdots & 2 & 1\end{pmatrix} =(1\;\;15)(2\;\; 14)\cdots (7\;\;8)
$$

이므로 7개의 호환이 모인 홀치환이다.



<b>3. </b>
