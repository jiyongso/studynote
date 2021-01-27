제 3 장. Basis and dimension
===



## 3.1. Linear Combination



<b>연습문제 3.1.7.</b> $S,\,T \subseteq V$ 이면 $\langle S \cup T\rangle = \langle S \rangle + \langle T \rangle$ 임을 보여라.

---

$$
\begin{align*}
v \in \langle S \cup T\rangle &\iff v=\sum_i a_i s_i + \sum_j b_j t_j \qquad &;\text{for some }s_i \in S,\,t_i \in T,\,a_i,\,b_j\in \mathbb{F} \\
&\iff v \in \langle S\rangle + \langle T \rangle\;.&; \sum_{i}a_is_i \in \langle S\rangle,\, \sum_{j}b_j t_j \in \langle T \rangle\quad\quad\,

\end{align*}
$$

<b>연습문제 3.1.8.</b> $\langle (2,\,5)^t,\, (1,\,3)^t \rangle = \mathbb{F}^2$ 임을 보여라.

---

$\langle (2,\, 5)^t,\,(1,3)^t\rangle \subset \mathbb{F}^2$ 임은 자명하다. $(x,\,y)\in \mathbb{F}^2$ 에 대해 $a=3x-y,\, b=-5x+2y\in \mathbb{F}$ 를 선택하면 $a(2,\,5)^t+b(1,\,3)^t=(x,\,y)$ 이므로 $\mathbb{F}^2\subset \langle (2,\,5)^t,\, (1,\,3)^t\rangle$ 이다. 따라서 $\langle (2,\,5)^t,\, (1,\,3)^t \rangle = \mathbb{F}^2$ .



## 3.2 일차독립과 일차종속



<b>연습문제 3.2.2.</b> 유한집합 $S=\{v_1,\ldots,\,v_n\}$ 이 일차독립이면, $S$ 의 모든 부분칩합 $\{v_{i_1},\ldots,\,v_{i_k}\}$ 도 일차독립임을 보여라.

---

$V_0=\{v_{i_1},\ldots,\,v_{i_k}\}$ 가 일차독립이 아니라고 하면 $\sum_k a_k v_{i_k}=0$ 를 만족하는 non-zero $a_k$ 가 존재한다. 그렇다면 
$$
\sum_{k}a_k v_{i_k}+\sum_{v' \in S-V_0} 0 \cdot v'=0 = \sum_{j=1}^n c_kv_k
$$
를 만족하는 nonzero $c_k$ 가 존재한다는 뜻이므로 $S$ 가 일차독립이라는 가정에 모순된다.



<b>연습문제 3.2.3</b> (가) $\{ (2,\,5)^t,\, (1,\,3)^t\}\subset \mathbb{F}^2$ 는 일차독립인가?

(나) $\{ 2t+5, t+3\}=\mathbb{F}[t]$ 는 일차독립인가?

(다) 만약 $\{v,\,w\}\subset V$ 가 일차독립이면 $\{2v+5w,\, v+3w\}$ 도 일차독립인가? 또, $\langle v,\,w\rangle = \langle 2v+5w,\, v+3w\rangle$ 인가?

---

(가) $a(2,\,5)^t + b(1,\,3)^t = (2a+b,\, 5a+3b)^t=0 \implies a=b=0$. 따라서 일차독립이다.

(나) $a(2t+5)+b(t+3)=(2a+b)t+5a+3b=0 \implies a=b=0$. 따라서 일차독립.

(다) $a(2v+5w)+b(v+3w)=(2a+b)v+(5a+3b)w=0 \implies 2a+b=0 \text{ and } 5a+3b=0 \implies a=b=0$. 따라서 일차독립. 
$$
x\in \langle v,\,w \rangle \implies x=av+bw =(3a-b)(2v+5w)+(-5a+2b)(v+3w) \in \langle2v+5w,\,v+3w\rangle .
$$
따라서 $\langle v,\,w\rangle \subseteq \langle 2v+5w,\, v+3w\rangle$. 또한,
$$
x\in \langle 2v+5w,\, v+3w\rangle \implies x=c(2v+5w)+d(v+3w)=(2c+d)v+(5c+3d)w \in \langle v,\,w \rangle.
$$
이므로  $\langle 2v+5w,\, v+3w\rangle \subseteq \langle v,\,w\rangle $ 이므로 $\langle v,\,w \rangle= \langle 2v+5w,\, v+3w\rangle$. 



<b>연습문제 3.2.4</b> (가) $0\in S$ 이면, $S$ 는 일차종속임을 보여라.

(나) $\{v\}$ 가 일차독립일 필요충분조건은 $v\ne 0$ 임을 보여라.

(다) $0\ne v,\,w \in V$ 이고 $v\ne w$ 일 때, $\{v,\,w\}$ 가 일차종속이기 위한 필요충분조건은 $v=aw$ 인 $a\in \mathbb{F}$ 가 존재하는 것임을 보여라.

(라) $u,\,v,\,w\in \mathbb{R}^3$ 일 때, $\{u,\,v,\,w\}$ 가 일차종속일 필요충분조건은 $u,\,v,\,w$ 가 $0$ 을 지나는 하나의 평면 위에 있는 것임을 보여라.

---

(가) For any nonzero $a\in \mathbb{F}$, $a\cdot 0 + \sum_{s\in S,\, s \ne 0} 0 \cdot s=0$.

(나) $v\ne 0$ 에 대해 $av=0 \implies a=0$. 따라서 $\{v\}$ 는 일차독립이다. $\{v\}$ 가 일차독립이려면 $av=0$ 을 만족하는 scalar $a=0$ 이어야 한다. 만약 어떤 nonzero $c\in \mathbb{F}$ 에 대해 $cv=0$ 이면 $v=0$ 이다. 따라서 $\{v\}$ 가 일차독립이면 $v\ne 0$ 이다.

(다) $\{v,\,w\}$ 가 일차종속이면 $cv+dw=0$ 을 만족하는 non-zero $c,\,d\in \mathbb{F}$ 가 존재해야 한다. $a\ne 0,\, b\ne 0$ 이면 $v=-\dfrac{d}{c} w$ 이다. $c=0,\,d\ne 0$ 이면 $w=0$ 이므로 $\{v,\,w\}$ 는 일차종속이다. 그런데 이 경우 $v=aw$ 를 만족하는 $a\in \mathbb{F}$ 가 존재하지 않는데?  마찬가지로 $c\ne 0,\, d=0$ 일 경우 $v=0$ 이므로 일차종속이며, $v=0 w$ 이므로 $v=aw$ 를 만족하는 $a\in \mathbb{F}$ 가 존재한다. 

거꾸로 $v=aw$ 인 $a\in \mathbb{F}$ 가 존재한다면 i) $a=0$ 이면 $v=0$ 이므로 $\{v,\,w\}$ 는 일차종속, ii) $a\ne 0$ 이면 $v-aw=0$ 이므로 $\{v,\,w\}$ 는 일차종속.

(라) $u,\,v\in \R^3$ 가 일차독립이면 벡터의 외적에 의해 $u,\,v$ 모두와 수직인 벡터 $n$ 이 존재하며 $w$ 가 $u,\,v$ 의 linear combination 이면 $w$ 도 $n$ 에 수직이며 따라서 $u,\,v,\,w$ 는 이 $n$ vector에 의해 결정되며 $0$ 을 포함하는 평면상에 존재한다. 만약 세 벡터중 일차종속인 두 벡터가 없다면 세 벡터는 $0$ 벡터 이거나 $0$  벡터가 아니라면 다른 nonzero vector의 스칼라곱이므로 한 벡터의 스칼라곱으로 표현 될 수 있다. 한 벡터를 포함하는 원점을 지나는 평면은 무한하게 존재한다.

$u,\,v,\,w$ 가 $0$ 을 지나는 하나의 평면 위에 있다면 이 평면은 이중 linearly independent한 두 벡터가 존재하며 다른 하나는 두 벡터의 선형결합이라는 뜻이므로 $\{u,\,v,\,w\}$ 는 일차종속이다.



<b>연습문제 3.2.6.</b> $S=\{v_i\}_{i\in I}\subseteq V$ 일 때 다음을 보여라.

(가) $S$ 가 일차독립이면 $[\,v_i \ne v_j \text{ for all }i \ne j\,]$ .

(나) $S$ 가 일차독립이면, $S$의 모든 subset도 일차독립.

(다) $S\subseteq V$ 가 일차종속이면, $S$ 의 모든 subset도 일차종속인가?

(라) $S \subseteq T \subseteq V$ 이고 $S$ 가 일차종속이면 $T$ 도 일차종속인가?

---

(가) 어떤 $i\ne j$ 에서 $v_i=v_j$ 이면 $v_i+(-1)v_j=0$ 이므로 일차종속이다. 

(나) $S$ 가 일차종속이며 $S$ 의 어떤 subset 에서 일차종속이 말이 안되지.

(다) $V=\R^2$ 이고 $S=\{(0,\,1),\, (1,\,0),\,(1,\,1)\}$ 은 일차종속이나 $S_0=\{(0,\,1),\, (1,\,0)\}\subset S$ 는 일차독립이다. 따라서 No.

(라) 당연하지.



<b>연습문제 3.2.8.</b> (가) $\{1,\,t,\,t^2,\,t^3,\ldots\}\subset \mathbb{F}[t]$ 는 일차독립임을 보여라.

(나) 실변소 함수 $f,\,g,\,h \in C^\infty(\R)$ 을 다음과 같이 정의하면
$$
f(x)=1,\quad g(x) = \exp (x),\quad h(x)=\exp (2x)\, , \quad x\in \R
$$
$\{f,\,g,\,h\}$ 는 일차독립임을 보여라.

---

 (가) $0= \sum_{k=0}^\infty c_k t^k$ 라 하자. $t=0$ 을 놓으면 $c_0=0$ 이다. 양 변을 $t$ 에 대해 미분하고 $t=0$ 을 대입하면 $c_1=0$. 이를 계속 반복하면 $c_k=0$ for all $k=0,\,1,\,\ldots$ 임을 알 수 있다.

(나) $af(x)+bg(x)+ch(x)=0$ 이라 놓자. $x=0$ 에 대해 $a+b+c=0$. $x=\ln 2$ 를 넣으면 $a+2b+4c=0$. $x=\ln 4$ 를 넣으면 $a+4b+16c=0$ 이다. 이를 풀면 $a=b=0$ 이므로 $\{f,\,g,\,h\}$ 는 일차독립.



## 3.3. Vector Space의 Basis



<b>Note : </b> $S\subset V$ 일 때 $\langle S\rangle$ 은 $S$ 의 원소중 <u>유한개의 선형결합으로</u> 이루어진 모든 벡터의 집합이다. 



<b>연습문제 3.3.9.</b> $\mathcal{B}=\{v_1,\ldots,\,v_n\}$ 이 $V$ 의 basis 라 하자. $v,\,w\in V$, $a\in\mathbb{F}$ 일 때, 다음을 보여라.

(가) $[v+w]_{\mathcal{B}}=[v]_{\mathcal{B}}+[w]_{\mathcal{B}}$. 

(나) $[av]_{\mathcal{B}}=a[v]_{\mathcal{B}}$.

---

(가) $v=\sum_i a_i v_i,\, w=\sum_i b_i v_i$ 일 때 $v+w=\sum_i (a_i +b_i)v_i$ 이므로 
$$
[v+w]_{\mathcal{B}}=(a_1+b_1,\ldots,\, a_n+b_n)^t =(a_1,\ldots,\,a_n)^t+(b_1,\ldots,\,b_n)^t=[v]_{\mathcal{B}}+[w]_{\mathcal{B}}\,.
$$

(나) $av=\sum_{i}aa_i v_i$ 이므로,
$$
[av]_\mathcal{B}=(aa_1,\ldots,\,aa_n)^t = a(a_1,\ldots,\,a_n)^t=a[v]_{\mathcal{B}}\;.
$$


<b>명제 3.3.12. </b> $\{v_1,\ldots,\,v_n\}$ 이 $V$ 의 기저이고 $w_j = \sum_{i}a_{ij}v_i\quad (j=1,\ldots,\,n)$ 이라 하자.  만약 $A=(a_{ij})\in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 가 가역이면 $\{w_1,\ldots,\,w_n\}$ 도 $V$ 의 basis 이다.

---

*(proof)* (1) 우선 $\{w_j\}$ 가 일차독립임을 보이자. 
$$
0=\sum_j c_j w_j = \sum_j c_j(\sum_i a_{ij}v_j)=\sum_i (\sum_{j}a_{ij}c_j)v_i
$$
이므로 $\sum_j a_{ij}c_j=0$ 이다. $c=(c_1,\ldots,\,c_n)^t$ 라 하면 $Ac=0$ 이며 $A$ 가 가역이므로 $A^{-1}Ac=c=A^{-1}0=0$ 이므로 $c=0$ 이다. 즉 $\{w_j\}$ 는 일차독립이다.

(2) $\langle \{w_j\} \rangle =V$ 임을 보인다. $B=(b_{ij})=A^{-1}$ 이며 $\displaystyle w_j=\sum_i a_{ij}v_i$ 일 때 $\displaystyle v_j=\sum_i b_{ij}w_i$ 임을 보이자.  $AB=BA=I$ 이므로 $\displaystyle \sum_k b_{ik}a_{kj}=\sum_k a_{ik}b_{kj}=\delta_{ij}$ 이다. 
$$
\sum_{j}b_{ji}w_j = \sum_j b_{ji}\sum_k a_{kj}v_k=\sum_k v_k \left( \sum_j a_{kj}b_{ji} \right)=\sum_k\delta_{ki}v_k =v_i
$$
$\{v_i\}$ 가 $V$ 의 basis 이므로 임의의 $v\in V$ 는 $v=\sum_j c_jv_j$ 로 표현 할 수 있다. 그렇다면,
$$
v=\sum_i c_i v_i = \sum_i c_i \left( \sum_j  b_{ji}w_j\right )=\sum_j \left(\sum_i b_{ji}c_i\right)w_j
$$
이므로 $\langle\{w_j\}\rangle =V$ 이다. $\quad\square$



