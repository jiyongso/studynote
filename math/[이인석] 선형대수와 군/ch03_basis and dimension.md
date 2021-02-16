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



<b>연습문제 3.3.13.</b> $A\in \mathfrak{M}_{m,\,n}(\mathbb{F})$ 일 때, 다음을 증명하라.

(가) $\left\{[A]^1,\ldots,\,[A]^n \right\}$ 이 일차독립이기 위한 필요충분조건은 $(\ast)\, AX=0$ 이 trivial solution 만을 갖는 것이다.

(나) $\left\langle [A]^1,\ldots,\,[A]^n\right\rangle =\mathbb{F}^n$ 이기 위한 필요충분조건은 임의의 $B\in \mathbb{F}^m$ 에 대하여 $(**)\, AX=B$ 가 solution을 갖는 것이다.

(다) $\left\{[A]_1,\ldots,\,[A]^n\right\}$ 이 $\mathbb{F}^m$ 의 기저일 필요충분조건은 임의의 $B\in \mathbb{F}^m$ 에 대하여 $(**)\, AX=B$ 가 unique solution을 갖는 것이다.

---

(가) $\left\{[A]^1,\ldots,\,[A]^n \right\}$ 이 일차독립임을 가정하면 $x_1[A]^1 + \cdots + x_n [A]^n=0 \implies x_1 = \cdots =x_n=0$ 일 때 분이다. $X=(x_1,\ldots,\,x_n)^t$ 라 하면 $x_1[A]^1+\cdots + x_n[A]^n=AX$ 이므로 $\left\{[A]^1,\ldots,\,[A]^n \right\}$ 이 일차독립이면 $AX=0$ 의 해는 $0$ 뿐이다. 

$AX=0$의 해가  trivial solution 뿐이면 $x_1[A]^1 + \cdots + x_n [A]^n=0 \implies x_1 = \cdots =x_n=0$ 이므로 $\left\{[A]^1,\ldots,\,[A]^n \right\}$ 이 일차독립이다.

(나) $AX=x_1[A]^1+\cdots + x_n[A]^n$ 이다. $\left\langle [A]^1,\ldots,\,[A]^n\right\rangle =\mathbb{F}^n$ 이려면 임의의 $B\in \mathbb{F}^m$ 에 대해 $AX=B$ 의 해가 존재하면 된다. 반대로 $AX=B$ 의 해 $X$ 가 존재한다면 $AX=x_1[A]^1+\cdots + x_n[A]^n=B$ 이므로 $\left\langle [A]^1,\ldots,\,[A]^n\right\rangle =\mathbb{F}^n$ 이다.

(다) $\left\{[A]_1,\ldots,\,[A]^n\right\}$ 이 $\mathbb{F}^m$ 의 기저라면 관찰 3.3.2에 의해 $AX=B$ 가 unique solution을 갖는다. $AX=B$ 가 unique solution을 가지면 역시 관찰 3.3.2에 의해 $\left\{[A]_1,\ldots,\,[A]^n\right\}$ 이 $\mathbb{F}^m$ 의 기저이다.



<b>연습문제 3.3.14. </b> (가) $\mathbb{F}[t]$ 는 infinite basis $\{1,\,t,\,t^2,\,t^3,\ldots\}$ 를 갖는 것을 보여라.

(나) $\mathbb{F}[t]$ 는 finite basis를 가질 수 있는가?

---

(가), (나). $\{1,\,t,\,t^2,\,t^3,\ldots\}$ 는 lineary independent 함을 연습문제 3.2.8에서 보였다. 또한 일차독립인 집합의 부분집합도 일차독립임을 연습문제 3.2.6에서 보였다. 만약 $\mathbb{F}[t]$ 가 finite basis를 가진다면 가장 큰 degree $n$ 을 가지며 이는 $t^{n+1}$ 을 표현하지 못한다. 따라서 $\mathbb{F}^n$ 은 infinite basis $\{1,\,t,\,t^2,\,t^3,\ldots\}$를 가진다.



<b>질문 3.3.15</b> (가) $\mathbb{R}^3$ 공간은 4개(또는 2개) 의 vector로 이루어진 basis도 가질 수 있는가?

(나) Function space $C^0(\R)$ 은 basis를 갖는가? $C^0(\R)$ 은 finite basis를 가질 수 있는가?

---

(가) $t,\,u,\,v,\,w\in \R^3$ 가 basis of $\R^3$ 면 연습문제 3.3.13 (가) 에 의해 $t,\,u,\,v,\,w$ 를 열로 갖는 행렬 $A$ 에 대해 $AX=0$ 이 trivial solution 만을 가져야 한다. 명제 $A\in \mathfrak{M}_{3,\,4}(\mathbb{F})$ 이므로 명제 1.2.6 에 의해 항상 nontrivial solution을 가진다. 따라서 $t,\,u,\,v,\,w$ 는 일차독립이 아니므로 $\R^3$ 공간은 4개의 vector로 이루어진 basis를 가질 수 없다.

$u,\,v \in \R^3$ 가 basis of $\R^3$ 라면 $u,\,v$ 를 열로 갖는 행렬 $A\in \mathfrak{M}_{3,\,2}(\mathbb{F})$ 과 임의의 $B\in \R^3$에 대해 $AX=B$ 가 solution을 가져야 한다. 그런데 $A$ 에 대한 row induced echelon form은 최소한 하나의 $0$ row를 가지므로 이것이 불가능. 즉 두개의 vector 로는 $\R^3$ 를 span하지 못한다. 따라서 $\R^3$ 에 두개의 vector로 이루어진 basis는 존재 할 수 없다. 

(나) $\R[t] \subset C^0 (\R)$ 이므로 $C^0$ 가 basis를 갖는다면 무한개의 basis를 가질 수 밖에 없다. 



## 3.4. Basis 의 존재



<b>연습문제 3.4.1.</b> $S\subset V$ 가 일차독립이고 $v\not\in S$ 일 때, 다음 조건

(가) $S\cup \{v\}$ 는 일차독립.

(나) $v\not\in \langle S\rangle$. 

이 동치임을 증명하라.

---

(1) $S=\{v_1,\,v_2,\ldots\}$ 라 하자. 

(2) $S\cup \{v\}$ 가 일차독립임을 가정한다. $v\in \langle S\rangle$ 이면 $v=\sum_i a_i v_i$ 이므로 $(\sum_i a_iv_i)-v=0$ 이며 이는 $S \cup \{v\}$ 가 일차독립이라는 것에 모순. 따라서 $v\not\in \langle S \rangle$.

(3) $v\notin \langle S\rangle$ 이면 $\sum a_i v_i +av=0$ 을 만족하는 $\{a_i\},\,a$ 는 $0=a=a_1=a_2=\cdots$ 뿐이다. 따라서 $S \cup \{v\}$ 는 일차독립이다.



## 3.5. Vector Space 의 Dimension



#### 보조정리 3.5.3.

Vector space $V$ 가 finite basis $\mathcal{B}=\{v_1,\ldots,\,v_m\}$ 을 갖는다고 하자. 이 때 만약 $\mathcal{C}=\{w_1,\ldots,\,w_n\}\subset V$ 이고 $m<n$ 이면 $\mathcal{C}$ 는 일차종속이다.

---

*(proof)* $\mathcal{B}$ 가 basis of $V$ 이므로 $w_j= \sum_{i=1}^m a_{ij}v_i$ 인 $A=(a_{ij})\in \mathfrak{M}_{m,\,n}(\mathbb{F})$ 가 유일하게 존재한다. 
$$
0=\sum_{j=1}^n c_jw_j = \sum_{j=1}^n c_j \left(\sum_{i=1}^m a_{ij}v_i\right)=\sum_{i=1}^m \left(\sum_{j=1}^n a_{ij}c_j\right)v_i
$$
이므로 $\sum_{j=1}^n a_{ij}c_j=0$ for all $i=1,\ldots,m$. 그런데 $m<n$ 이면 항상 nonzero vector $c=(c_1,\ldots,\,c_n)^t$ 가 존재하므로 (명제 1.2.6) $\{w_j\}$ 는 일차종속이다. $\quad\square$



<b>연습문제 3.5.4. </b> $V=\mathbb{F}^m$ 일 때 보조정리 3.5.3과 명제 1.2.6은 동치임을 보여라.

---

[명제 1.2.6] $A\in\mathfrak{M}_{m,\,n}(\mathbb{F})$ 이고 $m<n$ 이면 $AX=0$ 은 항상 nontrivial solution을 갖는다.

(1) $A$ 의 열벡터를 $[A]^1,\ldots,\,[A]^n$ 이라 하자.  

(2) 보조정리 3.5.3을 가정하자. $\mathbb{F}^m$ 은 standard basis $\{\mathbf{e}_1,\ldots,\,\mathbf{e}_m\}$ 을 가지며 따라서 $\{[A]^1,\ldots,\,[A]^n\}$ 을 일차종속이므로 $\sum_{i=1}^n x_j [A]^j=0$ 에 대해 nonzero $x_j$ 가 존재한다. 이는 $AX=0$ 이 nontrivial solution을 갖는다는 말고 같은 뜻이다. 

(3) 명제 1.2.6을 가정하자. $[A]^i=w_i$ 로 하여 행렬 $A\in \mathfrak{M}_{m,\,n}(\mathbb{F})$ 를 만들자. $AX=0$ 이 non-trivial solution 을 가지므로 $X=(x_1,\ldots,\,x_n)^t$ 라 하면 $\sum_{i=1}^n x_i [A]^i=0$ 을 만족하는 nonzero $x_i$ 가 최소한 하나 이상 존재한다. 따라서 $\{w_i\}$ 는 일차종속이다. 



<b>연습문제 3.5.6.</b> $\C$- vector space $\C^n$ 은 동시에 $\R$-vector space 로도 볼 수 있다.(연습문제 2.3.5) 이 때 $\dim_\R \C^n$ 을 구하라. (물론 $\dim_{\C}\C^n=n$)

---

$\R^n$ 의 standard basis $\mathcal{B}_{Re}=\{\mathbf{e}_1,\ldots,\,\mathbf{e}_n\}$ 과 여기에 $i$ 를 곱한 $\mathcal{B}_{Im}=\{i\mathbf{e}_1,\ldots,\,i\mathbf{e}_n\}$ 을 생각하자. $\mathcal{B}=\mathcal{B}_{Re}\cup \mathcal{B}_{Im}$ 이 선형독립이며 $\R$-vector space $\C^n$ 을 span함을 알 수 있으므로 $\dim_{\R}\C^n=2n$ 이다.



<b>연습문제 3.5.7.</b> $V,\,W$ 가 FDVS(finite dimensional vector space) 일 때,
$$
\dim (V \times W)=\dim V +\dim W
$$
임을 보여라.

---

(1)  $m=\dim V$ and $n =\dim W$ 이라 하자. $\mathcal{B}_{V0}=\{v_1,\ldots,\,v_m\}$ and $\mathcal{B}_{W0}=\{w_1,\ldots,\,w_n\}$ 을 각각 $V,\,W$ 의 basis라 하자. $\mathcal{B}_V=\{(v_i,\,0): v_i \in \mathcal{B}_{V0}\}$ , $\mathcal{B}_W=\{(0,\,w_j): w_j \in \mathcal{B}_{W0}\}$ 라 하고 $\mathcal{B}=\mathcal{B}_V \cup \mathcal{B}_W$ 라 하자. $(0,\,0)=0_{V \times W}$ 임은 자명하다. 

(2) $v\in V,\, w\in W$ 일 때 $v=\sum_{i}a_i v_i,\, w=\sum_{j}b_j w_j$ 이며 $(v,\,w)=\sum_{i}a_i (v_i,\,0)+\sum_{j}b_j (0,\,w_j)$ 이다. 따라서 $\langle \mathcal{B}\rangle = V \times W$ 이다. 

(3) $\sum_{i=1}^m a_i (v_i,\,0) + \sum_{j=1}^n b_j (0,\,w_j)= (\sum_{i} a_iv_i,\,\sum_j b_j w_j) =(0,\,0)$ 이라면 $a_i=0$ for $i=1,\ldots,\,m$ and $b_j =0$ for $j=1,\,\ldots,\,n$ 이다. 따라서 $\mathcal{B}$ 는 선형독립이며 basis of $V\times W$ 이다. 이로부터,
$$
\dim(V\times W)=m+n = \dim V + \dim W.
$$



<b> 연습문제 3.5.13.</b> $V$ 가 f.d.v.s 이고 $S \subseteq V$ 일 때 $|S|<\dim V$ 이면, $\langle S\rangle \ne V$ 임을 보여라.

---

$|S| \le \dim V$ 이면 $S$ 에서의 선형독립인 벡터의 갯수는 $\dim V$ 보다 작으므로 $S$ 의 원소들로 $V$ 를 span 하지 못한다.



<b> 연습문제 3.5.14. </b>$A$ 가 $n \times n$ square matrix 일 때, 다음 조건

(가) $\left\{ [A]^1,\ldots,\,[A]^n\right\}$ 은 $\mathbb{F}^n$ 의 basis.

(나) $\left\langle [A]^1,\ldots,\,[A]^n\right\rangle=\mathbb{F}^n$.

(다) $\left\{ [A]^1,\ldots,\,[A]^n\right\}$ 은 일차독립.

(라)  임의의 $B\in \mathbb{F}^n$ 에 대하여 $(**)\; AX=B$ 는 unique solution을 갖는다.

(마) 임의의 $B\in \mathbb{F}^n$ 에 대하여 $(**)\; AX=B$ 는 solution을 갖는다.

(바) $(*)\; AX=0$ 은 trivial solution 만을 갖는다.

은 동치임을 보여라.

---

(1) (가), (나), (다) 따름정리 3.5.12에 의해 equivalent.

(2) (가)$\implies$(라) 는 관찰 3.3.2를 보라.

(3) (라)$\implies$(바) $0\in\mathbb{F}^n$ 이므로 $AX=0$ 은 unique solution을 갖는다. $X=0$ 이 solution 이므로 unique 하다. 따라서 $AX=0$ 은 trivial solution 만을 가진다.

(4) (바)$\implies$(다) $X=(x_1,\ldots,\,x_n)^t$ 라 하면 $\sum_{j=0}^n x_j [A]^j=0$ 을 만족시키는 해는 $x_1=\cdots =x_n=0$ 뿐이므로 (다) 증명.

여기까지 (마)를 제외한 (가), (나), (다), (라), (바) 가 동치임을 보였다. (라)$\implies$(마) 는 자명하다(unique solution이 있다는 이야기는 일단 solution이 있다는 이야기이까.) (마)$\implies$(나) 역시 자명하다. 따라서 여섯 명제는 equivalent 하다.



## 3.6 우리의 철학



## 3.7 Dimension의 보기



<b>연습문제 3.7.3.</b>  다음 벡터공간의 기저와 차원을 구하라.

(가) $\mathfrak{t}_n (\mathbb{F})=\left\{ (a_{ij}\in \mathfrak{M}_{n,\,n}(\mathbb{F}) \mid a_{ij}=0 \text{ if }i > j\right\}$.

(나) $\mathfrak{n}_n (\mathbb{F})=\left\{(a_{ij})\in \mathfrak{M}_{n,\,n}(\mathbb{F}) \mid a_{ij}=0\text{ if } i \ge j  \right\} $.

(다) $\mathfrak{o}_n (\mathbb{F}) = \left\{(a_{ij})\in \mathfrak{M}_{n,\,n} (\mathbb{F})\mid a_{ij}=0 \text{ if }i \ne j  \right\}  $.

(라) $\mathfrak{sl}_n (\mathbb{F}) = \left\{  (a_{ij})\in \mathfrak{M}_{n,\,n}(\mathbb{F}) \mid \operatorname{tr} (A)=0 \right\}$.

(마) $\mathfrak{Snm}_n (\mathbb{F})=\left\{(a_{ij})\in \mathfrak{M}_{n,\,n}(\mathbb{F}) \mid A=A^t\right\}$.

(바) $\mathfrak{Ult}_n (\mathbb{F})=\left\{ (a_{ij})\in \mathfrak{M}_{n,\,n}(\mathbb{F})\mid A=-A^t \right\}$.

---

(가) $\{ \mathbf{e}_{ij}: 1 \le i \le j \le n\}$ , $\dim (\mathfrak{t}_n (\mathbb{F}) )=n(n+1)/2$. 

(나) $\{\mathbf{e}_{ij} : 1 \le i < j\le n\}$, $\dim (\mathfrak{n}_n (\mathbb{F}))=n(n-1)/2$. 

(다) $\{\mathbf{e}_{ii}: i = 1,\ldots,\,n\}$, $\dim (\mathfrak{o}_n (\mathbb{F}))=n$. 

(라) $\{\mathbf{e}_{ij} : 1 \le i \ne j \le n\} \cup \{\mathbf{e}_{ii}: i=1,\ldots,\,n-1\}$, $\dim (\mathfrak{sl}_n(\mathbb{F}))=n^2-1$. 

(마) $\{\mathbf{e}_{ij}+\mathbf{e}_{ji} : 1 \le i < j \le n\}\cup \{\mathbf{e}_{ii}: i=1,\ldots,\,n\}$ , $\dim(\mathfrak{Snm}_n(\mathbb{F}))=n(n-1)/2+n=n(n+1)/2$.

(바) $\{\mathbf{e}_{ij}-\mathbf{e}_{ji}: 1\le i < j \le n\}$, $\dim (\mathfrak{Ult}_n (\mathbb{F}))=n(n-1)/2$. 



<b>연습문제 3.7.4. </b> (**Lagrange interpolation formula**) $a_0,\,a_1,\ldots,\,a_n \in \mathbb{F}$ 가 서로 다른 scalar 이고 (단 $n\ge 0$), $b_0,\,b_1,\ldots,\,b_n\in \mathbb{F}$ 는 임의의 scalar 라고 할 때,
$$
g(a_i)=b_i,\qquad (i=0,\,1,\ldots,\,n)
$$
인 다항식 $g(t)\in \mathcal{P}_n (\mathbb{F})$ 가 유일하게 존재하고 또 쉽게 계산 할 수 있음을 다음 순서로 증명하라. 먼저, Lagrange polynomial $f_0(t),\, f_1(t),\ldots,\,f_n(t)$ 를 
$$
f_i (t) = \prod_{j\ne 1 \\ i \le j \le 0} \dfrac{t-a_j}{a_i-a_j},\qquad (i=0,\ldots,\,n)
$$
이라 정의하자.

(가) $f_i (a_j)=\delta_{ij}$ 임을 이용해 $\mathcal{B}=\{f_0(t),\ldots,\,f_n(t)\}$ 가 $\mathcal{P}_n(\mathbb{F})$ 의 일차독립인 subset 임을 보여라. 이제 따름정리 3.5.12 (와 보기 3.5.5 (나) 항)에 의해 $\mathcal{B}$ 는 $\mathcal{P}_n(\mathbb{F})$  의 basis 가 됨을 보여라.

(나) $g(t) = b_0 f_0(t) + b_1 f_1(t) + \cdots + b_n f_n (t)$ 이어야만 함을 보여라.

---

(가) $c_0f_0(t)+ c_1 f_1(t)+\cdots c_n f_n (t)=0$ 을 만족하는 $c_0,\,c_1,\ldots,\,c_n$ 을 구하자. $t$ 에 $a_i$ 를 넣어 보면 $c_i=0$ 임을 알 수 있다. 따라서 $\mathcal{B}$ 는 일차독립이며 $|\mathcal{B}|=n+1=\dim (\mathcal{P}_n (\mathbb{F}))$ 이므로 $\mathcal{B}$ 는 $\mathcal{P}_n (\mathbb{F})$ 의 basis 이다.

(나) 주어진 $g(t)$ 가 $g(a_i)=b_i$ 를 만족함은 쉽게 알 수 있다.  $g(t)\in \mathcal{P}_n(\mathbb{F})$ 이고 $\mathcal{B}$ 가 $\mathcal{P}_n(\mathbb{F})$ 의 basis 이므로 $g(t)$ 는 $\mathcal{B}$ 의 선형결합으로 유일하게 결정된다.



<b>연습문제 3.7.6.</b> 앞 연습문제 3.7.3에서 $U=\mathfrak{t}_n(\mathbb{F})$ , $W=\mathfrak{sl}_n (\mathbb{F})$ 로 놓을 때 $U+V$ 를 묘사하고 명제 3.7.5 를 확인하라.

----

(1) $U=\mathfrak{t}_n (\mathbb{F})$ 는 $n \times n$ upper triangular matrix 의 집합이며 $W=\mathfrak{sl}_n (\mathbb{F})$ 는 trace가 $0$ 인 $n \times n$ 행렬의 집합이다. 임의의 $A\in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 는 어떤 $A_U\in U$ 와 $A_W\in W$ 의 합으로 나타낼 수 있는데, $A$ 에서 upper triangule part를 $A_U$ 라 하면 $(A-A_U)_{ij}=0$ 이므로 $A-A_U\in W$ 이다. 따라서 $\dim (U+W)=n^2$ 이며 $U+V=\mathfrak{M}_{n,\,n}(\mathbb{F})$ 이다.

(2) $U\cap V$ 따라서 trace가 $0$ 인 upper triangular matrix의 집합이다. 따라서 $\dim (U \cap V)=n(n+1)/2-1$ 이다. 

(3) 연습문제 3.7.3에서 보았듯이 $\dim (U)=n(n+1)/2$ 이며 $\dim (W)=n^2-1$ 이다. 

(4) 명제 3.7.5 를 확인해보면 $\dim (U+W)+\dim (U \cap W)= n^2+n(n+1)/2-1$ 이고 $\dim(U)+\dim (W)=n^2+n(n+1)/2-1$ 이다.



<b>연습문제 3.7.7.</b> $V$ 가 f.d.v.s 이고 $U,\,W \le V$ 일 때 다음 조건들,

(가) $U \cap W=0$.

(나) $(U + W)$ 의 vector를 $(u+w)$ 꼴로 (단 $u\in U,\, w\in W$) 쓰는 방법은 유일.

(다) $0$ 을 $(u+w)$ 꼴로 (단 $u \in U,\, w\in W$) 쓰는 방법은 $0+0$ 뿐.

(라) $\mathcal{B},\,\mathcal{C}$ 가 각각 $U,\,W$ 의 기저이면, $\mathcal{B}\cap \mathcal{C} =\varnothing$ 이고 $\mathcal{B}\cup \mathcal{C}$ 는 $U+W$ 의 기저.

는 동치임을 보여라. 또, 이 때 $\dim (U+W)=\dim U + \dim W$ 임을 보여라.

---

(1) (가)$\implies$(나) $U \cap W=\{0\}$ 임을 가정한다. $v\in U +W$ 에 대해 $v=u_1+w_1=u_2+w_2$ where $u_1,\,u_2\in U$, $w_1,\,w_2\in W$ 라 하자. $u_1-u_2=w_1-w_2$ 이며 $u_1-u_2\in U$, $w_1-w_2\in W$ 이므로 $u_1-u_2,\, w_1-w_2 \in U \cap W=\{0\}$. 따라서 $u_1=u_2,\,w_1=w_2$  이므로 $u+w$ 꼴로 쓰는 방법은 유일하다.

(2) (나)$\implies$(다) 일단 $0\in U \cap W$ 이므로 $0=0+0$ 꼴로 쓸 수 있으며, (나) 에 의해 유일하므로 증명 끝.

(3) (다)$\implies$(라) $v\in \mathcal{B} \cap \mathcal{C}$, $v\ne 0$ 이면 $v\in U$ 이며 $v\in W$ 이므로 $v+(-v)=0$ 인 nonzero vector $v\in U,\, (-v)\in W$ 가 존재한다. 따라서 (다) 를 가정하면 $\mathcal{B} \cap \mathcal{C}=\varnothing$ 이다. 또한,

$$
|\mathcal{B}\cup \mathcal{C}|=|\mathcal{B}|+|\mathcal{C}|+|\mathcal{B} \cap \mathcal{C}|=|\mathcal{B}|+|\mathcal{C}|=\dim V + \dim W -\dim (V \cap W)= \dim (V +W)
$$

이다. $\mathcal{B} \cup \mathcal{C}$ 가 $V+W$ 를 span 하며 $|\mathcal{B}\cup \mathcal{C}|=\dim (V+W)$ 이므로 $\mathcal{B}\cup \mathcal{C}$ 는 $V+W$ 의 기저이다.

(4) (라)$\implies$(가) $\mathcal{B},\,\mathcal{C}$ 가 각각 $U,\,W$ 의 기저이므로 $|\mathcal{B}|=\dim U,\, |\mathcal{C}|=\dim U$ 이다. $\mathcal{B}\cup \mathcal{C}$ 가 $U+W$ 의 기저이므로 $|\mathcal{B}\cup\mathcal{C}|=\dim (U+V)$ 이다. 그런데 $\mathcal{B}\cap \mathcal{C}=\varnothing$ 이므로 $|\mathcal{B}\cup \mathcal{C}|=\dim U + \dim V$ 이며 $\dim (U \cap V)=0$ 이다. 따라서 $U \cap W=0$ 이다.



<b>연습문제 3.7.9.</b> $X_1,\ldots,\,X_r\in \mathbb{F}^n$ 일 때, ${X_i}^t$ 를 $i$ 번 째 행으로 갖는 $(r\times n)$-행렬 $A$ 를 생각하고, $A$ 로 부터 얻어지는 행 간소 사다리꼴을 $R$ 이라고 놓자. 

(가) $\left\langle [A]_1,\ldots,\,[A]_r\right\rangle$ =$\left\langle [R]_1,\ldots,\,[R]_r\right\rangle$ 임을 보여라.

(나) $R$ 의 [최초의 1]을 갖는 행들 (즉, nonzero-row 들) 은 일차독립임을 보여라.

(다) $\{X_1,\ldots,\,X_r\}$ 이 일차독립인지 (또는 $\mathbb{F}^n$ 의 기저인지는) $R$ 이 zero row를 갖는지 (또는 항등행렬인지) 여부만 확인해 보면 알 수 있음을 보여라.

---

(가) 행렬 $A$ 를 행 간소 사다리꼴로 바꾸는 것은 3종류의 elementary row operation을 계속 반복하는 것이다. 각각의 elementary row operation에 대해 모든 row에 대한 span이 바뀌지 않음을 보이며 된다. elementary row operations 는 다음과 같다.

(i) 두 행의 위치를 바꾼다. (ii) 한 행에 non-zero scalar를 곱한다 (iii) $i$ 번째 행에 $j$  번째 행의 $s$ 배를 더한다. 

(i), (ii)는 span 을 변경시키지 않음이 자명하다. $[A]_i \to [A]_i + s[A]_j$ 라 하자. 어떤 $v\in \mathbb{F}^n$ 이 $v=\cdots +a[A]_i +\cdots + b[A]_j+ \cdots$ 일 때 $v= \cdots + a([A]_i + s[A]_j) + \cdots + (b-sa)[A]_j + \cdots$ 이므로 (iii)-th row operation에 대해서도 span이 변화하지 않는다. $R$ 의 $A$ 에 유한번의 elementary row operation 을 수행한 것이므로 (가) 는 성립한다.

(나) 최초의 1을 갖는 행의 그 1의 열에 대해 다른 행의 그 열 값은 0 이다. 따라서 그 행에 $0$ 을 곱해야만 그 열을 0으로 만들수 있다. 따라서 $R$ 의 [최초의 1] 을 갖는 행들은 일차독립이다.

(다) (가) 에 의해 $\dim (\left\langle [A]_1,\ldots,\,[A]_r\right\rangle)= \dim (\left\langle [R]_1,\ldots,\,[R]_r\right\rangle)$ 이며 (나) 에 의해 이 값은 [최초의 1]을 갖는 $[R]_i$ 의 갯수 임을 알 수 있다. $[A]_i={X_i}^t$  이므로 $R$  이 zero row를 가지면 일차종속, 갖지 않으면 일차독립이다.



<b>연습문제 3.7.11.</b>  $V$ 가 f.d.v.s. 일 때 $V$ 의 기저 $\mathcal{B}$ 와 $\mathcal{C}$ 가 주어져 있다고 하자. 만약 $\{v_1,\ldots,\,v_r\}\subseteq \mathcal{B}$ 이면, $\{v_1,\ldots,\,v_r,\,w_1,\ldots,\,w_s\}$ 가 $V$ 의 기저가 되는 $\{w_1,\ldots,\,w_s\}\subseteq \mathcal{C}$ 가 존재함을 보여라. (물론 $r+s = \dim V$). (따라서 $V=\mathbb{F}^n$ 이고 $\mathcal{C}=\mathcal{E}$ ) 이면, $w_j$ 는 표준단위벡터가 된다.

---

(1) $n=\dim V$ 라 하자. $\mathcal{C}=\{w_1,\ldots,\,w_n\}$ 이라 할 때 $\{w_i\}$  가운데 $\{v_1,\ldots,\,v_r\}$ 의 선형결합으로 표현될 수 있는 것의 갯수 $m$ 이라 하면 $m=r$ 임을 보이자. 이 $m$ 개의 $\mathcal{C}$ 의 원소를 $\{w_{i_1},\ldots,\,w_{i_m}\}$ 이라 하면 이는 선형독립이며 $\langle w_{i_1},\ldots,w_{i_m}\rangle \le \langle v_1,\ldots,\,v_r\rangle$ 이므로 $m\le r$ 이다. 

(2) $\mathcal{C}$ 에서 $w_{i_1},\ldots,\,w_{i_m}$ 을 제외한 것을 $\mathcal{C}_0$ 라 하고 이것의 index를 재배치하여 $\{w_1,\ldots,\,w_{n-m}\}$ 으로 놓자. $\{v_1,\ldots,\,v_r,\,w_1\}$ 은 선형독립임이 자명하다. 만약 $w_2$ 를 포함시켰을때 선형독립이면 유지시키고 선형독립이 아니면 기각한다. $w_2,\ldots,\,w_{n-m}$ 까지 계속하여(그리고 $w_j$ 의 index를 다시 지정하여) $\{v_1,\ldots,\,v_r,\,w_1,\ldots,\,w_s\}$ 을 얻었다고 하자. 생성 방법에 따라 이것은 선형 독립이다. 이제 이것이 $V$ 의 기저가 됨을 보이면 된다.

(3) 거꾸로 이것이 $V$ 의 기저가 되지 않는가고 가정해보자. 즉 $r+s<\dim V$ 라 하자. $v_X\in V-\langle v_1,\ldots,\,v_r,\,w_1,\ldots,\,w_s\rangle$ with $v_X\ne0$ 이면 $v_X$ 는 $\mathcal{C}$ 의 span에 포함되지 않으며, 이는 $\mathcal{C}$ 가 base of $V$ 라는 것과 모순이다. 따라서 $r+s=\dim V$ 이며, 따라서 $\{v_1,\ldots,\,v_r,\,w_1,\ldots,\,w_s\}$ 는 $V$ 의 기저이다.



<b>연습문제 3.7.12.</b> (연습문제 3.7.9. 계속) $\{X_1,\ldots,\,X_r\}\subset \mathbb{F}^n$ 이 일차독립일 때 (물론 $r\le n$), $R$ 의 [최초의 1] 을 갖지 않는 column 들을 $[R]^{j_1},\ldots,\,[R]^{j_s}$ 라고 하면 $\{X_1,\ldots,\, X_r,\,\mathbf{e}_{j_1},\ldots,\,\mathbf{e}_{j_s}\}$ 는 $\mathbb{F}^n$ 의 기저가 됨을 보이시오.

---

$A$ 는 $n$ 개의 column이 존재한다.  $\{X_1,\ldots,\,X_r\}$ 이 일차독립이면 $r$ 개의 최초의 1을 갖는 row가 존재하며(연습문제 3.7.9의 (나)와 (다)) 최초의 1이 중복될수 없으므로 $r$ 개의 최초의 1을 갖는 column이 있다. 즉 $n-r$ 개의 column은 최초의 1을 갖지 않는다. 그리고 최초의 1을 갖는 칼럼은 표준기저벡터이므로 증명 끝.

 



<b>Note</b>  : 연습문제 3.7.13. ~ 3.7.15. 는 생략. 



 

 





