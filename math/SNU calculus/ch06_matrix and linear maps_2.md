VI. 행렬과 선형사상 #2
==



## 제 6장 탐구문제



<b>1. </b> 다항식 $p(x),\,q(x),\,r(x)$ 에 대하여 $p(x)=q(x)r(x)$ 이면, 임의의 정사각행렬 $A$ 에 대하여 $p(A)=q(A)r(A)$ 가 성립함을 보이라.

---

우리는 임의의 정사각 행렬 $A$ 와 실수 $a,\,b$ , 자연수 $n,\,m$ 에 대해 $\left(aA^n \right)\left(bA^m\right)=abA^{n+m}$ 임을 안다. 

$\displaystyle p(x)=\sum_{k=0}^{n_p}p_kx^k,\, q(x) =\sum_{k=0}^{n_q}q_k x^k,\, r(x)=\sum_{k=0}^{n_r} r_k x^k$ 라 하자. $p(x)=q(x)r(x)$ 이므로,
$$
p_k = \sum_{i=0}^k q_ir_{k-i}
$$
이제,
$$
q(A)r(A)=\left(\sum_{i=0}^{n_q}q_i A^i\right) \left(\sum_{j=0}^{n_r} r_j A^{j}\right) = \sum_{i=0}^{n_p}\sum_{j=0}^{n_r} q_ir_j A^{i+j} = \sum_{k=0}^{n_p}\sum_{l=0}^k q_{l}r_{k-l}A^k=\sum_{k=0}^{n_p} p_kA^k =p(A)
$$


<b>2.  </b> $m \times n$ 행렬 $A$ 와 $n \times l$ 행렬 $B$ 에 대하여, $B$ 의 각 열벡터를 차례로 $B_1,\ldots,\,B_l$ 이라고 두자. 이 때 $AB$ 의 각 열벡터는 $AB_1,\ldots,\,AB_l$ 임을 보이라. 또 $A$ 의 각 행벡터를 $A_{(1)},\ldots,\,A_{(m)}$ 으로 두면, $AB$ 의 각 행벡터는 $A_{(1)}B ,\ldots,\,A_{(m)}B$ 임을 보이라. 

---

$\widehat{e}_i$ 는 $n \times 1$ 열백터로 $i$ 번째 성분만 $1$ 이고 나머지는 $0$ 인 벡터라고 하자. $\widehat{f}_j$ 는 $1\times n$ 행백터로 $j$ 번째 성분만 $1$ 이고 나머지는 $0$ 인 벡터라고 하자. 그렇다면, 
$$
B_i = B\widehat{e}_i ,\qquad A_{(j)}=\widehat{f}_j A
$$
이다. 
$$
(AB)_{i}=(AB)\widehat{e}_i=A(B\widehat{e}_i)=AB_i,\qquad (AB)_{(j)}=\widehat{f}_j (AB)=(\widehat{f}_j A)B=A_{(j)}B
$$


<b>3. </b> $m\times n$ 행렬 $A$ 와 $n \times l$ 행렬 $B$ 에 대하여, $AB$ 의 각 행벡터는 $B$ 의 행벡터들의 일차결합임을 보이라. 또 $AB$ 의 각 열벡터는 $A$ 의 열벡터들의 일차결합임을 보이라.

---

$$
\begin{align}
(AB)_{(i)}&=A_{(i)}B= (a_{i1}\,a_{i2}\cdots \, a_{in})\begin{pmatrix} B_{(1)}\\
B_{(2)}\\
\vdots \\B_{(n)}\end{pmatrix}=a_{i1}B_{(1)}+ \cdots + a_{in}B_{(n)} \\

(AB)_{j} &= AB_i = \begin{pmatrix}A_1\, A_2 \, \cdots A_n\end{pmatrix} \begin{pmatrix}b_{j1}\\ b_{j2} \\ \vdots  \\b_{jn}\end{pmatrix} =b_{j1}A_1 + \cdots+b_{jn}A_n

\end{align}
$$



<b>4. </b> $m \times n$ 행렬 $A$ 의 열벡터 $A_1,\ldots,\,A_n$ 이 일차종속이면 $A\mathbf{v}=0$ 이 되는 영이 아닌 $n$ 벡터 $\mathbf{v}$ 가 존재함을 보이라. 또 이 명제의 역이 성립함을 보이라.

---

$A_1,\ldots,\,A_n$ 이 일차종속이면 $v_1A_1+\cdots +v_nA_n=0$ 을 만족시키는 nontrivial $v_1,\ldots,\,v_n$ 이 존재한다. 즉 $v_1,\ldots,\,v_n$ 중 최소한 하나는 $0$ 이 아니다. $\mathbf{v}=(v_1,\ldots,\,v_n)$ 이라 하면  $\displaystyle A\mathbf{v}=\sum_{i=1}^n A_i v_i=0$ 이 된다. 

역으로  $A\mathbf{v}=0$ 이 되는 영이 아닌 $n$ 벡터 $\mathbf{v}$ 가 존재한다면 $\mathbf{v}=(v_1,\ldots,\,v_n)$ 일 때 $\displaystyle A\mathbf{v}=\sum_{i=1}^n v_iA_i=0$ 이므로 $A_1,\ldots,\,A_n$ 은 일차종속이다.



<b>5. </b> 자연수 $m_1,\,m_2,\,n_1,\,n_2,\,l_1,\,l_2$ 에 대하여 $m=m_1+m_2,\, n=n_1+n_2,\,l=l_1+l_2$ 라고 두자. 이제 $m \times n$ 행력 $A$ 와 $n \times l$ 행렬 $B$ 를 $m_i\times n_j$ 행렬 $A_{ij}$ 와 $n_j\times l_k$ 행렬 $B_{jk}$ 로 분해하여,
$$
A=\begin{pmatrix}A_{11} & A_{12}\\ A_{21} & A_{22}\end{pmatrix},\qquad B=\begin{pmatrix} B_{11} & B_{12} \\ B_{21} & B_{22}\end{pmatrix}
$$
로 두면
$$
AB=\begin{pmatrix} A_{11}B_{11} + A_{12}B_{21} &  A_{11}B_{12} + A_{12} B_{22} \\ A_{21}B_{11}+A_{22}B_{21} & A_{21}B_{12} + A_{22}B_{22}\end{pmatrix}
$$
임을 보이라.

---

$1\le i\le n_1,\, 1\le j\le l_1$ 에서의 $(AB)_{ij}$ 를 보자. 
$$
(AB)_{ij}=\sum_{k=1}^{n_1+n_2}A_{ik}B_{kj}=\sum_{k=1}^{n_1}A_{ik}B_{kj} +\sum_{k=n_1+1}^{n_1+n_2} A_{ik}B_{kj}=\sum_{k=1}^{n_1}(A_{11})_{ik}(B_{11})_{kj}+\sum_{k=1}^{n_2}(A_{12})_{ik}(B_{21})_{kj}
$$
이므로 $1\le i\le n_1,\, 1\le j\le l_1$ 에서의 $AB=A_{11}B_{11}+A_{12}B_{21}$ 이다. 

이렇게 계속 확인해가면 답을 보일 수 있다.



<b>6. </b> $n$ 차 정사각행렬 $A$ 가 임의의 정사각행렬 $B$ 에 대하여 $AB=BA$ 이면 $A$ 는 항등행렬의 상수배임을 보이라.

---

$n$차 정사각행렬 $E_{ij}$ 를 $(i,\,j)$ 항만 $1$ 이고 나머지 항은 $0$ 인 행렬로 정의하자.  $AE_{ij}=C$ 라 하면 $C$ 는 $j$ 번째 열이 $A$ 의 $i$ 번째 열과 같으며 나머지 열은 $0$ 인 행렬이다. $E_{ij}A=D$ 라 하면 $D$ 의 $i$ 번째 행이 $A$ 의 $j$ 번째 행과 같고 나머지 행은 $0$ 인 행렬이다. 

$AE_{11}=E_{11}A$ 이므로 $A_{11}$ 을 제외한 나머지 $A_{j1}$ 과  $A_{1i}$ 도 $0$ 이다. 이것을 $AE_{ii}=E_{ii}A$ $i=1,\,2,\ldots,\,n$ 까지 계속 해 나가면 행렬 $A$ 는 대각성분을 제외한 성분이 $0$ 임을 알 수 있다. 

$AE_{12}=E_{12}A$ 이므로 $A_{11}=A_{22}$ 이다. 이것을 $AE_{1j}=E_{1j}A$ 에서 반복하면 $A_{11}=A_{22}=\cdots =A_{nn}$ 임을 알 수 있다. 따라서 $A$ 는 항등행렬의 상수배이다. 



<b>7. </b> 대각선이 $(a_1,\ldots,\,a_n)$ 인 정사각행렬과 반대각선이 $(b_1,\ldots,\,b_n)$ 인 정사각행렬을 각각 $D_{a_1,\ldots,\,a_n}$ 과 $E_{b_1,\ldots,\,b_n}$ 으로 나타내기로 하자. 이 대 다음을 보이라.
$$
\begin{align}
D_{a_1,\ldots,\,a_n} E_{b_1,\ldots,\,b_n} &= E_{a_1b_1,\ldots,\,a_nb_n}\\
E_{b_1,\ldots,\,b_n}E_{c_1,\ldots,\,c_n}&= D_{b_1c_n,\, b_2c_{n-1},\ldots,\,b_nc_1}
\end{align}
$$

---

$\left(D_{a_1,\ldots,\,a_n}\right)_{ij}=a_i\delta_{ij}$ 이며 $(E_{b_1,\ldots,\,b_n})_{ij}=b_i \delta_{i,n-j+1}$ 이다. 역시 $\delta_{ij}$ 는 크로네커델타함수 이다.
$$
\begin{align}
\left(D_{a_1,\ldots,\,a_n}E_{b_1,\ldots,\,b_n}\right)_{ij}&=\sum_{k=1}^n \left(D_{a_1,\ldots,\,a_n}\right)_{ik}\left(E_{b_1,\ldots,\,b_n}\right)_{kj} \\
&=\sum_{k=1}^n a_i \delta_{ik}b_k\delta_{k,\, n-j+1}=a_ib_i\delta_{i,\,n-j+1} \\
& = \left(E_{a_1b_1,\ldots,\,a_nb_n}\right)_{ij}\\
\left(E_{b_1,\ldots,\,b_n}E_{c_1,\ldots,\,c_n}\right)_{ij} & = \sum_{i=1} \left(E_{b_1,\ldots,\,b_n}\right)_{ik}\left(E_{c_1,\ldots,\,c_n}\right)_{kj} \\
&=\sum_{k=1} b_i\delta_{i,\, n-k+1}c_k\delta_{k,\,n-j+1}\\
&=b_i c_{n-j+1}\delta_{ij}=(E_{b_1c_{n},\, b_2c_{n-1}\ldots,\,b_nc_1})

\end{align}
$$


<b>8. </b> $m\times n$ 행렬 $A$ 와 $B$ 에 대하여
$$
|\operatorname{tr} (A^tB)| \le |A|\cdot |B|
$$
임을 보이라.

---

$$
\begin{align}
|A|\cdot |B| &= \sqrt{\sum_{j=1}^n\sum_{i=1}^m (A_{ij})^2}  \sqrt{\sum_{j=1}^n\sum_{i=1}^m (B_{ij})^2} \le\left|\sum_{j=1}^n \sum_{i=1}^m A_{ij}B_{ij}\right|= \left|\sum_{j=1}^n \sum_{i=1}^m (A^t)_{ji}B_{ij}\right|=\left|\operatorname{tr}(A^tB)\right|

\end{align}
$$

중간의 부등호는 코시-슈바르츠 부등식.



<b>9. </b> 단사인 선형사상에 대하여 일차독립인 벡터들의 상은 여전히 일차독립임을 보이라.

---

벡터공간 $V,\,U$ 에 대해  $T:U \to V$ 가 단사인 선형사상이며, $\mathbf{u}_1,\ldots,\mathbf{u}_n$ 이 $U$의 일차독립인 벡터라 하자. 
$$
\begin{align}
c_1T(\mathbf{u_1})+ c_2T(\mathbf{u}_2)+\cdots + c_n T(\mathbf{u}_n)=0 \implies T(c_1\mathbf{u}_1 + \cdots +c_n \mathbf{u}_n)=0

\end{align}
$$
이며  $T$ 가 단사인 선형사상이므로  $c_1\mathbf{u}_1 + \cdots +c_n \mathbf{u}_n=0$ 이다. $\mathbf{u}_1,\ldots,\,\mathbf{u}_n$ 이 일차독립인 벡터이므로  $c_1=\cdots =c_n=0$. 따라서 $T(\mathbf{u}_1),\ldots,\,T(\mathbf{u}_n)$ 은 $V$ 에서의 일차독립이다.



<b>10. </b> 단사인 선형사상에 의한 직선의 상은 직선임을 보이라.

---

$n$-공간에서 직선은 $x_i = a_it+b_i$ for $i=1,\ldots,n$ 로 표현된다. 선형사상에 의해  $x'_i = \sum_{j=1}^n T_{ij}x_j$ 일 때,
$$
x_i'=\sum_{j=1}^n T_{ij} x_j = \sum_{j=1}^n (a_jt+b_j)=\left(\sum_{j=1}^n T_{ij}a_j\right) t+\left(\sum_{j=1}^n T_{ij}b_j\right)
$$
이므로 직선이다.



<b>11. </b> 선형변환  $L:\mathbb{R}^n \to \mathbb{R}^n$ 이 단사일 필요충분조건은  $L$ 이 전사임을 보이라.

---

우리는 연습문제 제 6장 2절 4번에서 선형사상이 단사일 필요충분조건은 $L(X)=O$ 의 해가 $O$ 뿐이라는 것을 보였다. 또한 9번에서 단사인 선형사상에 대하여 일차독립인 벡터들의 상은 여전히 일차독립임을 보였다. 

$L$ 이 단사임을 가정하자. $\mathbb{R}^n$ 의 임의의 기저 $\mathbf{u}_1,\ldots,\,\mathbf{u}_n$ 에 대해 $L(\mathbf{u}_1),\ldots,\,L(\mathbf{u}_n)$ 이 일차독립이므로 (문제 9) $\{L(\mathbf{u}_i):i=1,\ldots,\,n\}$ 은 $\mathbb{R}^n$ 의 기저이다. $\mathbb{R}^n$ 의 임의의 벡터는 $c_1L(\mathbf{u}_1)+\cdots + c_n L(\mathbf{u}_n)$ 으로 표현할 수 있으며 이는  $L(c_1 \mathbf{u}_1+\cdots c_n \mathbf{u}_n)$ 이므로 $L$ 은 전사이다.

$L$ 이 단사가 아님을 가정하자. 어떤 $\mathbf{u}\ne 0$ 에 대해  $L(\mathbf{u})=O$ 이다.  우리는 앞서 $n$ 공간에서의 표준단위벡터 $\mathbf{e}_1,\ldots,\,\mathbf{e}_n$ 을 배웠다. $\mathbf{u}\ne O$ 이므로 $\mathbf{u}$ 의 $0$ 이 아닌 첫번째 성분이 있을 것이다. 그 성분이 $k$ 번째 성분이라면 표준단위벡터의 집합에서 에서 $\mathbf{e}_k$ 를 빼고 $\mathbf{u}$ 를 넣어도 이것이  $\mathbb{R}^n$ 의 기저임을 알 수 있다. 그렇다면  $L(\mathbf{e}_1),\ldots,\, L(\mathbf{e}_{k-1}),\,L(\mathbf{u}),\, L(\mathbf{e}_{k+1}),\ldots,\, L(\mathbf{e}_n)$ 중에서 최소한 하나 이상은 $0$ 벡터 이며 이것들의 선형결합으로 표현되는 벡터공간의 차원은 $n$ 보다 작다. 따라서 $L$ 은 전사가 아니다.



<b>12. </b> 선형사상 $L:\mathbb{R}^n \to \mathbb{R}^n$ 이 역사상을 가지면, 그 역사상 역시 선형임을 보이라.

---

선형사상 $L$ 역사상을 가지면 $L$ 은 전단사이다. $L(\mathbf{u}_1)=\mathbf{v}_1,\, L(\mathbf{u}_2)=\mathbf{v}_2,\, c\in \mathbb{R}$ 라 하자. $L^{-1}(\mathbf{v}_1)=\mathbf{u}_1$ 이며 $L^{-1}(\mathbf{v}_2)=\mathbf{u}_2$ 이다. $L$ 이 선형사상이므로 $L(\mathbf{u}_1+\mathbf{u_2})=\mathbf{v}_1+\mathbf{v}_2,\, L(c\mathbf{u}_1)=cL(\mathbf{u_1})=c\mathbf{v}_1$ 이며 $L$ 이 전단사이므로 
$$
\begin{align}
L^{-1}(\mathbf{v}_1+\mathbf{v}_2)&=\mathbf{u}_1+\mathbf{u}_2=L^{-1}(\mathbf{v}_1)+L^{-1}(\mathbf{v}_2)\\
L^{-1}(c\mathbf{v}_1) & =c\mathbf{u_1}=cL^{-1}(\mathbf{v}_1)
\end{align}
$$

이다. 따라서 $L^{-1}$ 도 선형사상이다. 



<b>13. </b> 선형사상 $L:\mathbb{R}^n \to \mathbb{R}^m$ 에 대응되는 $m \times n$ 행렬을  $A$ 라고 하자. 또 $A$ 의 전치 행렬 $A^t$ 에 대응되는 선형사상을  $L^t:\mathbb{R}^m \to \mathbb{R}^n$ 으로 두자. 이때
$$
\mathbf{w} \cdot L\mathbf{v}=L^t\mathbf{w}\cdot \mathbf{v} \qquad (\mathbf{v}\in \mathbb{R}^n,\, \mathbf{w}\in \mathbb{R}^m)
$$
을 보이라.

---

$$
\mathbf{w}\cdot L\mathbf{v}=\sum_{i=1}^m w_i (A\mathbf{v})_{i}=\sum_{i=1}^m w_i \left(\sum_{j=1}^n A_{ij}v_j\right)=\sum_{j=1}^n \left(\sum_{i=1}^m A_{ij}w_i\right)v_j=\sum_{j=1}^n \left(\sum_{i=1}^m (A^t)_{ji}w_i\right)v_j = \sum_{j=1}^n (A^t \mathbf{w})_j v_j = L^t\mathbf{w}\cdot \mathbf{v}
$$



<b>Note</b> $n$ 벡터 $\mathbf{u},\,\mathbf{v}$ 를 $n\times 1$ 열벡터로 표현한것을 $U,\,V$ 라 하면 벡터의 내적 $ \mathbf{u}\cdot \mathbf{v}$ 는 $ U^tV$ 와 같다. 선형사상을 $L$  의 행렬표현을  $A$ 라 하고 $\mathbf{w},\,\mathbf{v}$ 의 행렬표현을  $w,\,v$ 라 하면 
$$
\mathbf{w}\cdot L\mathbf{v}=w^t Av =(A^tw)^t v = (L^t\mathbf{w})\cdot \mathbf{v}
$$
로 더 쉽게 표현 할 수 있다. 



<b>14. </b> $m$-행 벡터  $\langle \mathbf{w}|$ 와 $m\times n$  행렬  $A$ 에 대하여, 사상
$$
\langle \mathbf{w}|\mapsto \langle\mathbf{w}|A
$$
는 선형사상임을 보이라. 또 주어진 $n$-열벡터 $|\mathbf{v}\rangle$ 에 대하여 사상
$$
\langle \mathbf{w}|\mapsto \langle \mathbf{w}|A|\mathbf{v}\rangle
$$
도 선형사상임을 보이라.

---

$m$ 행 벡터  $\langle \mathbf{w}|$ 는 이에 상응하는 열벡터 $|\mathbf{w}\rangle$ 의 행렬표현을 $\mathbf{w}$ 라 하면  $\mathbf{w}^t$ 이다. 따라서 $(\mathbf{w}_1^t+\mathbf{w}_2^t)A=\mathbf{w}^t_1A+\mathbf{w}^t_2A$ 이며 임의의 $c\in \mathbb{R}$ 에 대해 $ (c\mathbf{w}_1^t)A=c(\mathbf{w}_1^tA)$ 이므로 선형사상이다. 또한,
$$
\begin{align}
(\mathbf{w}_1^t+\mathbf{w}_2^t)A\mathbf{v}&=\mathbf{w}_1^tA\mathbf{v}+\mathbf{w}_2^tA\mathbf{v}\\
(c\mathbf{w}_1^t)A\mathbf{v}&=c(\mathbf{w_1}^tA\mathbf{v})
\end{align}
$$
이므로 선형사상이다.



<b>15. </b> 열벡터들이 일차독립인 $m\times n$  행렬 $A$ 와 $Y\in \mathbb{R}^m$ 에 대하여 $m>n$ 이면 방정식  
$$
AX=Y \qquad (X\in \mathbb{R}^n)
$$
는 일반적으로 해를 가지지 않음을 설명하라. 이때
$$
A^tAX=A^tY \qquad (X\in \mathbb{R}^n)
$$
은 항상 해를 가짐을 설명하라.

---

행렬 $A$ 의 $i$-번째 열벡터를 $A_i$ 라 하고 $X=(x_1,\ldots,\,x_2)$ 라 하자. 그렇다며 $AX=x_1A_1+\cdots +x_nA_n=Y$ 이어야 한다. $n<m$ 이며 $ A_i \in \mathbb{R}^m$   이므로  $AX=Y$ 인 $X$  가 존재한다는 것은 $Y$ 를 $A_1,\ldots,\,A_n$ 의 일차결합으로 표현할수 있다는 뜻이다. 그런데 $Y\in \mathbb{R}^m$ 이며  $A_i$ 의 갯수는 $n$ 개이므로 $Y$ 가 속한 $\mathbb{R}^m$ 을 모두 표현 할 수 없다. 따라서 일반적으로 해를 가지지 않는다.

$A^tAX=A^tY\implies A^t(AX-Y)=0$ 이다. $Y\in \mathbb{R}^m$ 이며 $A_1,\ldots,\, A_n$ 의 선형결합으로 표현되지 않을 경우 $AX=Y$ 인 $X$ 가 존재하지 않는다. 이제 $ A_1,\ldots,\,A_n$ 을 포함하는 $\mathbb{R}_n$ 의 basis를 항상 잡을 수 있다. 나머지 basis를  $B_1,\ldots,\,B_{m-n}$ 이라 하자. 우리는 $B_1,\ldots,\,B_{m-n}$ 을 모든 $ A_1,\ldots,\,A_n$ 과 수직한 벡터로 구성 할 수 있다. (제 5장 탐구문제  6번) 이제 $Y$ 가 $A_1,\ldots,\,A_n,\,B_1,\ldots,\,B_{m-n}$ 의 일차결합으로 다음과 같이 표현된다면
$$
Y=a_1A_1+\cdots +a_nA_n+b_1B_1+\cdots +b_{m-n}B_{m-n}
$$
$X=(a_1,\ldots,\,a_n)^t$ 라 놓자. 그렇다면 $AX-Y=b_1B_1+\cdots +b_m-nB_{m-n}$ 이 된다. 그렇다면,
$$
A^t(AX-Y)=\begin{pmatrix} A_1^t \\A_2^t \\ \vdots \\ A_n^t\end{pmatrix}(b_1B_1+\cdots +b_{m-n}B_{m-n})=\begin{pmatrix} \displaystyle \sum_{j=1}^{m-n} b_j \left(A_1^t \cdot B_j\right) \\ \displaystyle \sum_{j=1}^{m-n} b_j \left(A_2^t \cdot B_j\right) \\ \vdots \\ \displaystyle \sum_{j=1}^{m-n} b_j \left(A_n^t \cdot B_j\right) 
\end{pmatrix} = O
$$
이다.



<b>16. </b> 두 벡터 공간 사이에 정의된 선형사상 $L:X \to Y$ 와 주어진 $ y\in Y$ 에 대하여 방정식 $L(x)=y$ 를 만족시키는  해 $x_0\in X$ 가 존재한다고 하자. 이 때 주어잔 방정식의 해집합은
$$
x_0+\ker L:=\{x_0 +x : x\in X,\,L(x)=0\}
$$
임을 보이라.

---

$L(x)=y$ 의 해집합을 $A$ 라 하자. 임의의 $x\in \ker L$ 에 대해 $L(x_0+x)=L(x_0)+L(x)=L(x_0)=y$ 이므로 로  $x_0+\ker L\subset A$ 이다. 

어떤 $z\not\in \ker L$ 이면  $x_0 + z \not \in x_0 +\ker L$ 임을 보이자 . 역으로 $x_0 +z \in x_0 + \ker L$ 이면 어떤  $x\in \ker L$ 에 대해 $x_0 +z = x_0 +x \implies z=x$ 이어야 하므로 모순. 따라서 $x_0 +z \not\in x_0 +\ker L$ 이다.  그렇다면  $L(x_0 +z)=L(x_0)+L(z)=L(z)\ne O$ 이므로 $(x_0+\ker C)^C \subset A^C$ 이다. 따라서 $A=x_0 + \ker L$ 임을 보였다.



<b>17. </b> $\mathbb{R}^n$ 의 선형부분공간 $\mathcal{V}$  와 $n$ 차 정사각행렬 $A$  에 대하여
$$
A\mathcal{V}:=\{ A\mathbf{v}: \mathbf{v}\in \mathcal{V}\}
$$
가 $\mathcal{V}$ 가 포함되면 $A$ 가  $\mathcal{V}$ 를 보존한다고 말한다. 이제 $A$ 가 $\mathcal{V}$ 를 보존하면, $A^t$ 는
$$
\mathcal{V}^\perp :\{\mathbf{w} \in \mathbb{R}^n: \mathbf{w}\cdot \mathbf{v}= 0,\, \forall\mathbf{v}\in \mathcal{V}\}
$$
를 보존함을 보이라.

---

$\mathbf{w}=(w_1,\ldots,\,\,w_n) \in \mathcal{V}^\perp$ 라 하자. $\mathbf{v}=(v_1,\ldots,\,v_n)\in \mathcal{V}$ 이면  $A\mathcal{v}=\mathbf{v}'\in \mathcal{V}$ 이다.  
$$
(A^t\mathbf{w})\cdot \mathbf{v}= (A^t\mathbf{w})^t\mathbf{v} = (\mathbf{w}^tA)\mathbf{v} = \mathbf{w}^t(A\mathbf{v}) = \mathbf{w}^t \mathbf{v'}=0
$$


<b>18. </b> 정사각행렬 $ A$ 가 $A^tA=I$ 이면 $ AA^t=I$ 임을 보이라.

---

$A$가  $n \times n$ 행렬이라 하자. 
$$
(A^tA)_{ij}=\sum_{k=1}^n (A^t)_{ik}A_{kj}=\delta_{ij}
$$
임을 안다. 
$$
(AA^t)_{ij}=\sum_{l=1}^n A_{il}(A^t)_{lj}=\sum_{l=1}^n (A^t)_{li}A_{jl}=\sum_{i=1}^n A_{jl}(A^t)_{li}=\delta_{ji} 
$$
이므로 $(AA^t)=I$ 이다.



<b>19. </b> 삼차원 좌표공간 $\mathbb{R}^3$ 에서 점 $P$ 를 지나고, 단위벡터 $\mathbf{v}$ 에 수직인 평면으로의 정사영을 $E$ 라고 두면
$$
E(X)=X+((P-X)\cdot \mathbf{v})\mathbf{v},\qquad X\in \mathbb{R}^3
$$
임을 보이라. 또 $E^2=E$ 임을 보이라.

---

점 $P$ 를 지나고 단위벡터 $\mathbf{v}$ 에 수직인 평면은 $\mathbf{v}\cdot (X-P)=0$ 이다. $X_0\in \mathbb{R}^3$  를 지나고 기울기 $\mathbf{v}$ 인 직선의 방정식은  $t\in \mathbb{R}$ 에 대해 
$$
X=\mathbf{v}t+X_0
$$
이다. 이 때 직선과 평면의 교점은, ($|\mathbf{v}|=1$ 이므로, )
$$
\mathbf{v} \cdot (\mathbf{v}t+X_0-P)=0 \implies |\mathbf{v}|^2t=\mathbf{v}\cdot (P-X_0) \implies t=(P-X_0)\cdot \mathbf{v}
$$
에 의해 결정된다. 즉 이 교점을 $X_1$ 라 하고  $t_0=(P-X_0)\cdot \mathbf{v}$ 라 하면, 
$$
X_1=\mathbf{v}t_0 +X_0
$$
이다. 이 때 $X_0-X_1=-\mathbf{v}t_0$ 이며, 평면상의 임의의 점 $X_2$ 에 대해 $\mathbf{v}\cdot (X_2-X_1)=\mathbf{v}(X_2-P)-\mathbf{v}(X_1-P)=0$ 이므로  $X_1-X_0$ 와 $X_2-X_1$ 은 항상 수직하다. 따라서 피타고라스의 정리에 의해 평면과 $X_0$ 사이의 최단거리는 $|X_1X_0|$ 이므로  $X_0$ 가 $X_1$ 의 정사영이다. 

$X_1\to X,\, X_0\to E(X)$ 라 하면,
$$
E(X)=X+\left((P-X)\cdot \mathbf{v}\right)\mathbf{v}
$$
이다.

또한 $E^2=E$ 임을 보이자. $|\mathbf{v}|^2=\mathbf{v}\cdot \mathbf{v}=1$ 을 이용하면, 
$$
\begin{align}
E(E(X))&=X+((P-X)\cdot \mathbf{v})\mathbf{v} +((P-[X+\left((P-X)\cdot \mathbf{v}\right)\mathbf{v}])\cdot \mathbf{v})\mathbf{v} \\
&=X+((P-X)\cdot \mathbf{v})\mathbf{v} +((P-V)\cdot \mathbf{v}) \mathbf{v}-((P-X)\cdot \mathbf{v})(\mathbf{v}\cdot \mathbf{v})\mathbf{v} \\ 
&= X+((P-X)\cdot \mathbf{v})\mathbf{v}\\
&=E(X)

\end{align}
$$
이다.





<b>20. </b> 좌표공간 $\mathbb{R}^3$ 에서 서로 다른 두 평면 $\pi_1,\,\pi_2$ 로의 정사영을 각각 $E_1,\,E_2$ 라고 할 때, $E_1E_2=E_2E_1$ 이 될 필요충분조건은 $\pi_1$ 과  $\pi_2$ 가 서로 수직으로 만나는 것임을 보이라. 

---

$\pi_1,\,\pi_2$ 의 방향벡터의 단위벡터를 각각 $\mathbf{v}_1,\,\mathbf{v}_2$ 라고 하고 각각의 평면이 지나는 한 점을 $P_1,\,P_2$ 라 하자. 두 평면이 서로 다른 평면상에 있으므로 $P_1$  을 $\pi_2$  위에 있지 않고, $P_2$  는 $\pi_1$  위에 있지 않도록 잡을 수 있다.  
$$
\begin{align}
E_1(E_2(X)) &=E_1(X+((P_2-X)\cdot \mathbf{v}_2)\mathbf{v}_2)\\
&= X+((P_2-X)\cdot \mathbf{v}_2)\mathbf{v}_2 +((P_1-X-((P_2-X)\cdot \mathbf{v}_2)\mathbf{v}_2)\cdot \mathbf{v}_1)\mathbf{v}_1\\
&=X+((P_2-X)\cdot \mathbf{v}_2)\mathbf{v}_2 +((P_1-X)\cdot \mathbf{v}_1)\mathbf{v}_1 -((P_2-X)\cdot \mathbf{v}_2)(\mathbf{v}_2\cdot \mathbf{v}_1)\mathbf{v}_1\\
E_2(E_1(X))&=X+((P_1-X)\cdot \mathbf{v_1})\mathbf{v}_1 + ((P_2-X)\cdot \mathbf{v}_2)\mathbf{v}_2 -((P_1-X)\cdot \mathbf{v}_1)(\mathbf{v}_1 \cdot \mathbf{v}_2)\mathbf{v}_2
\end{align}
$$
이다. 
$$
E_1E_2=E_2E_2\implies (\mathbf{v}_1\cdot \mathbf{v}_2)\left[(P_2-X)\cdot \mathbf{v}_2)\mathbf{v}_1-((P_1-X)\cdot \mathbf{v}_1)\mathbf{v}_2 \right]=0
$$
이다. 따라서 $\mathbf{v}_1\cdot \mathbf{v}_2=0$ 이거나 $((P_2-X)\cdot \mathbf{v}_2)\mathbf{v}_1=((P_1-X)\cdot \mathbf{v}_1) \mathbf{v}_2$ 일 때이다.

두번째 경우부터 보자. 임의의  $X$ 에 대해 성립해야 하므로, $\mathbf{v}_1=c\mathbf{v}_2$ for some $c\in \mathbb{R}$ 이어야 한다. $\mathbf{v}_1$ 과 $\mathbf{v}_2$  는 단위벡터이므로 $c=\pm 1$ 이며, 따라서,
$$
(P_2-X)\cdot \mathbf{v}_2 = \pm (P_1-X)\cdot \mathbf{v}_1\implies (P_2-X)\cdot \mathbf{v}_1=(P_1-X)\cdot \mathbf{v_1} \implies (P_1-P_2)\cdot \mathbf{v}_1 =0
$$
이다. 이것을 만족하는 $P_2$ 는 평면 $\pi_1$ 상에 있는데 우리는 이미 $P_2$ 가 $\pi_1$ 위에 있지 않다고 가정했으므로 위 식은 성립할 수 없다. 따라서,
$$
E_1E_2=E_2E_1 \iff \mathbf{v}_1\cdot \mathbf{v}_2=0
$$


<b>21. </b> 좌표공간에서 원점을 지나는 한 평면으로의 정사영을 $E$ 라고 두자. 이때 임의의 벡터 $\mathbf{v}$ 에 대하여,
$$
\langle \mathbf{v}|E\mathbf{v}\rangle = |E\mathbf{v}|^2
$$
임을 보이라.

---

우리는 문제 19를 풀 때 문제에는 3차원 좌표공간임을 가정했지만 3차원임을 이용하지 않았다. 즉 문제 19의 결론은 임의의 $n$ 차원 좌표공간에 적용 할 수 있다. 원점을 지나는 한 평면의 방정식은 단위방향벡터 $\mathbf{n}$ 에 대하여 $\mathbf{n}\cdot X=0$ 으로 나타 낼 수 있다. 이에 대한 정사영은 (문제 19를 이용하면),
$$
E(X)=X-(X\cdot\mathbf{n})\mathbf{n}
$$
이다. 임의의 $\mathbf{v}\in \mathbb{R}^n$ 에 대해 $\langle {\mathbf{v}-E\mathbf{v}}|E\mathbf{v}\rangle$ 을 계산해보자. $E(\mathbf{v})=\mathbf{v}-(\mathbf{v}\cdot \mathbf{n})\mathbf{n}$ 이므로,
$$
\langle {\mathbf{v}-E\mathbf{v}}|E\mathbf{v}\rangle =\langle (\mathbf{v}\cdot \mathbf{n})\mathbf{n}|\mathbf{v}-(\mathbf{v}\cdot \mathbf{n})\mathbf{n}\rangle = (\mathbf{v}\cdot \mathbf{n})^2-(\mathbf{v}\cdot \mathbf{n})^2(\mathbf{n}\cdot\mathbf{n})=0
$$
이다. 그런데,
$$
0=\langle {\mathbf{v}-E\mathbf{v}}|E\mathbf{v}\rangle =\langle\mathbf{v}|E\mathbf{v}\rangle -\langle E\mathbf{v}|E\mathbf{v}\rangle = \langle \mathbf{v}|E\mathbf{v}\rangle -|E\mathbf{v}|^2
$$
이다. 따라서 $\langle \mathbf{v}|E\mathbf{v}\rangle =|E\mathbf{v}|^2$ 이다. 



<b>22. </b> 삼차원 좌표공간에서 단위벡터 $\mathbf{v}=(v_1,\,v_2,\,v_3)$ 가 만드는 축의 주위로 $\theta$ 만큼 회전이동하는 변환의 행렬 $R_{\mathbf{v}}(\theta)$ 는
$$
\begin{pmatrix}
v_1^2 (1-\cos \theta) +\cos \theta & v_1v_2(1-\cos \theta)-v_3\sin \theta  & v_1v_3 (1-\cos \theta)+ v_2\sin \theta \\
v_1v_2(1-\cos\theta)+v_3 \sin \theta & v_2^2 (1-\cos \theta) + \cos \theta & v_2v_3 (1-\cos \theta) - v_1 \sin \theta \\
v_1v_3 (1-\cos \theta) - v_2 \sin \theta & v_2v_3 (1-\cos \theta)+v_1\sin \theta & v_3^2(1-\cos \theta) + \cos \theta


\end{pmatrix}
$$
임을 보이라. 또,
$$
\cos \theta = \dfrac{1}{2} \left(\operatorname{tr} R_{\mathbf{v}}(\theta)-1\right)
$$
임을 보이라.

---



지겨운데..



<b>23. </b> 정사각행렬 $A$ 에 대하여 $|A|<1$ 이면 급수
$$
I+A+A^2+A^3+\cdots
$$
가 수렴하고 이 때
$$
(I-A)(I+A+A^2+A^3+\cdots )=I
$$
임을 보이라.

---

$A$ 를 $n \times n$ 행렬이라 하자. 우리는 $|A_{ij}|<1 \;\forall 1\le i,\,j \le n$ 이며 $|A^k|\le |A|^k$ 임을 안다. (정리 3.3.2) 즉 $|A_{ij}|=r<1$ 이면 $|A^k|\le r^k$ 이므로 모든 $A^k$ 의 성분은 $r^k$ 보다 작다. 따라서, $\displaystyle \lim_{k=\infty}A^k=0$ 이며, $B_k=I+A+A^2+\cdots +A^k $ 라 하면, 
$$
|(B_k)_{ij}|<1+r+r^2+\cdots +r^{k}<\dfrac{1}{1-r}
$$
이므로 $(B_k)_{ij}$ 는 절대수렴한다. $I+A+A^2+\cdots = B$ 이므로 양변에 $A$ 를 곱하면 $B-I=AB$ 임을 안다. 따라서,
$$
(I-A)(I+A+A^2+\cdots)=B-AB=I
$$
이다.



<b>24. </b> 수렴반경이 $r>0$ 인 멱급수 $\displaystyle f(x)=\sum_{k=0}^\infty b_k x^k$ 를 생각하자. 이 때 $A$ 가 $|A|<r$ 인 정사각행렬이면 급수
$$
f(A):=\sum_{k=0}^\infty b_k A^k
$$
가 수렴함을 보이라.

---

우리는 $|A^k|<|A|^k<r^k$ 임을 알며 $|(A^k)_{ij}|<|A^k|<r^k$ 임을 안다. 따라서,
$$
|f(A)_{ij}| = \left|\sum_{k=0}^\infty b_k (A^k)_{ij}\right|\le \sum_{k=0}^\infty \left|b_k (A^k)_{ij}\right| \le \sum_{k=0}^{\infty} b_k r^k
$$
이므로 절대수렴한다. 



