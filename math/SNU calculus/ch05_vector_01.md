V. 벡터 #1
===



## 연습문제 : 제 5장 1 절



<b>1. </b> 다음을 보이라.

(1) 평행이동은 전단사 함수이다.

(2) 평행이동에서는 한 점이 어디로 가는가를 알면, 임의의 점이 어디로 가는가를 알 수 있다.

(3) 임의의 두 점 $A,\,B$ 에 대하여 $A$ 를 $B$ 로 옮기는 평행이동이 존재하고, 오직 하나 뿐이다.

(4) 만약 $T:\mathbb{R}^n \to\mathbb{R}^n$ 이 평행이동이면,
$$
X \mapsto \operatorname{dist}(X,\,T(X)) \qquad (X\in \mathbb{R}^n)
$$
는 상수함수이다.

---

(1) 평행이동 함수 $T_{\mathbf{v}}:\mathbb{R}^n \to \mathbb{R}^n$ 가 어떤 $\mathbf{v}\in \mathbb{R}^n$ 에 대해 $T_{\mathbf{v}}(X):X + \mathbf{v}$ 로 정의된다고 하자. $X_1+\mathbf{v}=X_2+\mathbf{v}\implies X_1=X_2$ 이므로 $T_{\mathbf{v}}$ 는 단사이다. 임의의 $Y\in \mathbb{R}^n$ 에 대해 $X=Y-\mathbf{v}$ 이면 $T_\mathbf{v}(X)=Y$ 이므로 $T_{\mathbf{v}}$ 는 전사이다. 따라서 전단사이다.

(2) 우리는 어떤 평행이동 $T_{\mathbf{v}}$ 에 대해 $T_{\mathbf{v}}(A)=B$ 임을 안다고 하자. $A+\mathbf{v}=B$ 이므로 $\mathbf{v}=B-A$ 로 정해진다. 따라서 임의의 $X\in \mathbb{R}^n$ 에 대해
$$
T_{\mathbf{v}}(X)=X+(B-A)
$$
이다.

(3) (2) 에 의해 $A$ 를 $B$ 로 옮기는 평행이동이 존재함을 안다. 다른 평행이돈 $T_{\mathbf{v'}}=X+\mathbf{v'}$ 이 존재하여 $A$ 를 $B$ 로 보낸다면 $A+\mathbf{v}'=B$ 이므로 $\mathbf{v}=\mathbf{v}'$ 이 된다. 따라서 $T_{\mathbf{v}}=T_{\mathbf{v}'}$ 이므로 오직 하나 뿐이다.

(4) 임의의 $\mathbf{v}\in\mathbb{R}^n$ 에 대해 $T(X)=X+\mathbf{v}$ 이면 $\operatorname{dist}(X,\, T(X))=\operatorname{dist}(X,\, X+\mathbf{v})=\operatorname{dist}(0,\, \mathbf{v})$ 이므로 $X$ 와 무관한 상수함수이다.



<b>2. </b> $n$-공간에서 점 $P$ 에 대한 점대칭 변환 (central symmetry)
$$
s_P : X \to s_P(X)
$$
는 식 $\dfrac{1}{2} (X+s_P(X))=P$ 가 만족되도록 주어진다. 즉,
$$
s_P(X)=2P-X
$$
이다. 이 때 두 점 $P_1,\,P_2$ 에 대한 점대칭변환의 합성 $s_{P_1}\circ s_{P_2}$ 는 어떠한 변환인가?

---

$$
(s_{P_1}\circ s_{P_2})(X) = s_{P_1}(2P_2-X)=2P_1-(2P_2-X)=2P_1-2P_2+X
$$

이므로 $X$ 에 대해 $2P_1-2P_2$ 만큼의 평행이동이다.



<b>3. </b> $n$-공간에서 점 $P$ 를 중심으로 하고, 닮음비가 $c\in \mathbb{R}$ 인 닮음변환 $S_{P,\,c}:\mathbb{R}^n \to \mathbb{R}^n$ 은
$$
S_{P,\,c}(X)=P+c(X-P)
$$
로 정의된다. 이제 점 $Q$ 를 중심으로 하고 닮음비가 $c$ 인 닮음변환 $S_{Q,\,c}$ 는 닮은 변환 $S_{P,\,c}$ 를 실행한 다음 $(1-c)(Q-P)$ 만큼 평행이동하는 사상과 같음을 보이라.

---

평행이동 $T(X)=X+(1-c)(Q-P)$ 를 생각하면,
$$
\begin{align}
(T\circ S_{P,\,c})(X)&=T(P+c(X-P))\\
&=(1-c)(Q-P)+P+cX-cP\\
&=(1-c)Q-(1-c)P+P+cX-cP\\
&=Q+c(X-Q)\\
&=S_{Q,\,c}

\end{align}
$$




## 연습문제 : 제 5장 2절



<b>1. </b> 다음 벡터와 나란한 방향의 단위벡터를 모두 구하라.

---

(1) $\mathbf{a}=(-1,\,-2,\,-3)$  : $\dfrac{1}{14}(1,\,2,\,3)$ , $-\dfrac{1}{14}(1,\,2,\,3)$

(2) $\mathbf{b}=(4,\,-5,\,6)$ : $\dfrac{1}{77}(4,\,-5,\,6)$, $-\dfrac{1}{77}(4,\,-5,\,6)$ 

(3) $\mathbf{c}=(1999,\, 1999,\, 1999)$ : $\dfrac{1}{\sqrt{3}}(1,\,1,\,1)$, $-\dfrac{1}{\sqrt{3}}(1,\,1,\,1)$

(4) $\mathbf{d}=(3,\,4,\,0)$ : $\dfrac{1}{5}(3,\,4,\,0)$, $-\dfrac{1}{5}(3,\,4,\,0)$



<b>2. </b> 모든 벡터는 단위벡터의 상수배로 나타낼 수 있음을 보이라.

----

임의의  non-zero 벡터 $\mathbf{v}$ 에 대해 $\mathbf{v}=|\mathbf{v}| \cdot \left(\dfrac{\mathbf{v}}{|\mathbf{v}|}\right)$ . Zero vector $\mathbf{0}$ 은 임의의 단위벡터 $\mathbf{e}$ 에 대해 $\mathbf{0}=0\cdot\mathbf{e}$ 이다. 



<b>3. </b> (**동등관계**) 어떤 집합 $X$ 에 대하여 (**제**)**곱집합** 
$$
X\times X=\{(x,\,y): x\in X,\, y\in X\}
$$
의 부분집합 $R$ 이 주어졌다고 하고 $(x,\,y)\in R$ 일 때 $x\equiv y$ 로 쓰기로 하자. 이 때 $R$ 이 다음 세 조건을 만족시키면 $R$ 을 동등관계라고 부른다.

​	(**반사율**) $x \equiv x$ 

​	(**대칭률**) $x\equiv y \implies y \equiv x$

​	(**추이율**) $x\equiv y,\, y \equiv z \implies x \equiv z$

이제 주어진 실수 $c$ 에 대하여 두 실수 $a,\,b$ 의 차가 $c$ 의 정수배가 될 때
$$
a \equiv b \,\operatorname{mod}\,c
$$
로 쓰기로 한다. 이 관계가 동등관계임을 보이라.

---

(반사율) $x-x=0 = 0 \cdot c$

(대칭률) $\exists c\in \mathbb{Z} \text{ s.t. } x-y=k \cdot c \implies y-x = (-k)\cdot c$ and $(-k)\in \mathbb{Z}$ 

(**추이율**) $x-y=nc,\, y-z=mc \implies x-z=(x-y)+(y-z)=(n+m)c$ 



<b>4. </b> 생략



<b>5. </b> 실수 $d$ 에 대하여
$$
d^o :=\{x\in \mathbb{R} : x \equiv d \;\operatorname{mod} \, 360\}
$$
으로 정의하자. 이 때 임의의 실수 $a,\,b$ 에 대하여
$$
a^o=b^o \qquad \text{또는} \qquad a^o \cap b^o = \varnothing
$$
임을 보이라.

---

$x,\,y \in d^o$ 이면 어떤 정수 $m,\,n$ 이 존재하여 $x-d=m\cdot 360,\, y-d=n\cdot 360$ 이며 $y \equiv x \;\operatorname{mod}\;360$ 이다. 따라서 $d^o=x^o=y^o$ 이다.  따라서 $x\in a^o \cap b^o$ 이면 즉 $a^o \cap b^o \ne \varnothing$ 이면 $x^o = a^o = b^o$ 이다. 



<b>6. </b> $n$-공간의 임의의 한 점 $P$ 에 대하여, $n$-벡터 전체의 집합은 $P$ 를 시점으로 하는 유향선분 전체의 집합과 일대일 대응관계가 있음을 설명하라.

---

평행이동!



<b>7. </b> $n$-공간의 임의의 벡터 $\mathbf{a}$ 와 실수 $t$ 에 대하여,
$$
0 \mathbf{a}=\mathbf{0},\qquad t\mathbf{0}=\mathbf{0}
$$
임을 보이라. 또 $t\mathbf{a}=\mathbf{0}$ 이면 $t=0$ 또는 $\mathbf{a}=\mathbf{0}$ 임을 보이라.

----

trivial



#### 3.1.10 기본연습문제

<b>1. </b> 임의의 실수 $a_1,\,a_2,\ldots,\,a_n$ 에 대하여 부등식
$$
(a_1+a_2+\cdots + a_n)^2 \le n({a_1}^2+{a_2}^2+\cdots +{a_n}^2 )
$$
이 성립함을 보이라. 또 등호가 성립하는 경우는 언제인가? 그리고 평균의 제곱 제곱의 평균보다 이하임을 보이라.

----

$\mathbb{R}^n$ 에서 $\mathbf{a}=(a_1,\,a_2,\ldots,\,a_n)$ 과 $\mathbf{b}=(1,\,1,\ldots,\,1)$ 을 생각한다. CBS 부등식 $|\mathbf{a}|^2|\mathbf{b}|^2\ge |\mathbf{a}\cdot \mathbf{b}|^2$ 을 생각하면,
$$
\begin{align}
|\mathbf{a}|^2&= ({a_1}^2+{a_2}^2 + \cdots +{a_n}^2)\,,\\
|\mathbf{b}|^2&=n\,,\\
|\mathbf{a}\cdot \mathbf{b}|&=|a_1+a_2+\cdots +a_n|
\end{align}
$$
이므로 성립한다. 등호가 성립하는 경우는 둘이 나란할 할 때 이므로 $a_1=a_2=\cdots =a_n$ 일 때 이며,
$$
\begin{align}
[\text{평균의 제곱}] &=\dfrac{1}{n^2} (a_1+a_2+\cdots +a_n)^2\,,\\
[\text{제곱의 평균}] &=\dfrac{1}{n} ({a_1}^2+{a_2}^2+\cdots +{a_n}^2)\;.

\end{align}
$$
이므로 주어진 식에 의해 [평균의 제곱]$\le$ [제곱의 평균] 이다.



<b>2. </b> 실수 $a_1,\ldots,\,a_n$ 이 $a_1+\cdots +a_n=1$ 을 만족시킬 때 ${a_1}^2+\cdots +{a_n}^2$ 의 최소값을 구하라.

---

1. 의 결과를 이용하면, $({a_1}^2+\cdots +{a_n}^2)\ge \dfrac{1}{n}$ 이다.



<b>3. </b> (**라그랑즈 항등식**) 다음 항등식을 증명하라.
$$
\left(\sum_{k=1}^n {a_k}^2\right)\left(\sum_{k=1}^n {b_k}^2\right) = \left(\sum_{k=1}^n a_kb_k\right)^2 + \dfrac{1}{2}\sum_{i,\,j=1}^n (a_ib_j-a_jb_i)^2
$$

---

$\mathbf{a}=(a_1,\ldots,\,a_n),\,  \mathbf{b}=(b_1,\ldots,\,b_n)\in \mathbb{R}^n$ 이라 하자. 
$$
\begin{align}
\sum_{i,\,j=1}^n (a_ib_j-a_jb_i)^2 &=\sum_{i=1}^n \sum_{j=1}^n \left({a_i}^2{b_j}^2 + {a_j}^2{b_i}^2-2a_ia_jb_ib_j\right) \\
&=\left(\sum_{i=1}^n {a_i}^2 \right)\left(\sum_{j=1}^n {b_j}^2 \right)+\left(\sum_{i=1}^n {b_i}^2 \right)\left(\sum_{j=1}^n {a_j}^2 \right)-2\left(\sum_{i=1}^n a_ib_i\right) \left(\sum_{j=1} a_j b_j\right)\\
&=2|\mathbf{a}|^2|\mathbf{b}|^2-2(\mathbf{a}\cdot\mathbf{b})^2
\end{align}
$$
이므로,
$$
\left(\sum_{k=1}^n a_kb_k\right)^2 + \dfrac{1}{2}\sum_{i,\,j=1}^n (a_ib_j-a_jb_i)^2=(\mathbf{a}\cdot \mathbf{b})^2+|\mathbf{a}|^2|\mathbf{b}|^2-(\mathbf{a}\cdot \mathbf{b})^2=|\mathbf{a}|^2|\mathbf{b}|^2=\left(\sum_{k=1}^n {a_k}^2\right)\left(\sum_{k=1}^n {b_k}^2\right)
$$
이다.



## 연습문제 : 제 5장 3절



<b>4. </b> $\mathbf{v}_1,\,\mathbf{v}_2,\ldots,\,\mathbf{v}_k$ 가 서로 수직인 단위벡터들이면, 임의의 실수 $a_1,\,a_2,\ldots,\,a_k$ 에 대하여
$$
\left|a_1\mathbf{v}_1 + a_2\mathbf{v}_2 + \cdots + a_k\mathbf{v}_k\right|^2 ={a_1}^2+{a_2}^2+\cdots + {a_k}^2
$$
임을 보이라.

---

$\delta_{ij}$ 를 다음과 같이 정의한다.
$$
\delta_{ij}=\left\{\begin{array}{ll}1 \qquad &\text{if }i=j \\ 0 &\text{if } i \ne j\end{array}\right.
$$
이 때 임의의 $\mathbf{v}_i,\,\mathbf{v}_j$ 에 대해 $\mathbf{v}_i \cdot \mathbf{v}_j = \delta_{ij}$ 임을 알 수 있다. 
$$
\left|a_1\mathbf{v}_1 + a_2\mathbf{v}_2 + \cdots + a_k\mathbf{v}_k\right|^2  = \sum_{i=1}^k \sum_{j=1}^k a_i a_j (\mathbf{v}_i\cdot \mathbf{v}_j)=\sum_{i=1}^k\sum_{j=1}^k a_ia_j \delta_{ij}=\sum_{i=1}^k {a_i}^2
$$


<b>5. </b> $n$-공간에서 벡터 $\mathbf{a}_1,\ldots,\,\mathbf{a}_k$ 가 이루는 나란히꼴은
$$
\{t_1\mathbf{a}_1+\cdots + t_k \mathbf{a}_k : 0\le t_1,\ldots,\,t_k\le 1\}
$$
로 정의한다. 이 때 두 벡터 $\mathbf{a},\,\mathbf{b}$ 가 이루는 나란히꼴의 넓이는
$$
\sqrt{|\mathbf{a}|^2|\mathbf{b}|^2-(\mathbf{a}\cdot \mathbf{b})^2}=|\mathbf{a}||\mathbf{b}| \sin \theta
$$
임을 보이라. (여기에서 $\mathbf{a}$ 와 $\mathbf{b}$ 사이의 각을 $\theta$ 라 두었다.)

----

두 변의 길이가 각각 $a,\,b$ 이며 사잇각이 $\theta$ 인 사다리꼴의 넓이가 $ab\sin \theta$ 임을 안다. 따라서,
$$
[\text{Area}]=|\mathbf{a}||\mathbf{b}|\sin\theta =|\mathbf{a}||\mathbf{b}|\sqrt{1-\cos^2\theta}=\sqrt{|\mathbf{a}||\mathbf{b}|-(\mathbf{a}\cdot \mathbf{b})^2}
$$
이다. 



<b>6. </b> (**정사영과 피타고라스정리**) 삼차원 좌표공간에서 두 벡터 $A,\,B$ 가 이루는 나란히꼴 $P$ 를 $yz$-평면에 정사영한 것의 넒이를 $a_1$, $zx$-평면에 정사영한 것의 넒이를 $a_2$, $xy$-평면에 정사영한 것의 넓이를 $a_3$ 라고 두자. 이 때 $P$ 의 넓이 $a$ 는 
$$
a^2={a_1}^2+{a_2}^2+{a_3}^2
$$
을 만족시킴을 보이라. 또 $P$ 와 $yz$-평면의 사이의 각을 $\theta_1$, $zx$-평면 사이의 각을 $\theta_2$, $xy$-평면 사이의 각을 $\theta_3$ 이라 두면
$$
a_i = a \cos \theta_i,\qquad (i=1,\,2,\,3)
$$
임을 보여라.

---

(1) $A=(A_1,\,A_2,\,A_3), \, B=(B_1,\,B_2,\,B_3)$  라 하면 
$$
\begin{align}
a_1 &= \sqrt{({A_2}^2+{A_3}^2)({B_2}^2+{B_3}^2)-(A_2B_2+A_3B_3)^2}=|A_2B_3-A_3B_2|\,,\\
a_2 &= \sqrt{({A_1}^2+{A_3}^2)({B_1}^2+{B_3}^2)-(A_1B_1+A_3B_3)^2}=|A_1B_3-A_3B_1|\,,\\
a_3 &= \sqrt{({A_1}^2+{A_2}^2)({B_1}^2+{B_2}^2)-(A_1B_1+A_2B_2)^2}=|A_1B_2-A_2B_1|\,,\\
a&= \sqrt{({A_1}^2+{A_2}^2+{A_3}^2)({B_1}^2+{B_2}^2+{B_3}^2)-(A_1B_1+A_2B_2+A_3B_3)^2}\,,\\
&=\sqrt{(A_1B_2-A_2B_1)^2+(A_1B_3-A_3B_1)^2+(A_2B_3+A_3B_2)^2} \\
&= \sqrt{{a_1}^2+{a_2}^2+{a_3}^2 }&


\end{align}
$$


(2) 뒤에 나오는 벡터의 외적을 이용한다. $A,\,B$  두 벡터에 의해 정해지는 평면과 수직인 벡터 $N=A\times B$ 이며, $yz,\, zx,\,xy$-평면에 수직인 벡터는 차례대로 $\mathbf{e}_1,\,\mathbf{e}_2,\,\mathbf{e}_3$ 이다. 두 평면이 이루는 $\theta_i$ 는 $0\le \theta_i <\dfrac{\pi}{2}$ 사이로 정해지므로 $\cos \theta_i>0$ 이며, 
$$
\cos \theta_i =\dfrac{|N\cdot \mathbf{e}_i|}{|N||\mathbf{e}_i|}=\dfrac{a_i}{a}
$$
이다. 



<b>7. </b> 삼차원 좌표공간에서 한 나란히꼴 $P$ 를 $yz$-평면, $zx$-평면, $xy$-평면에 정사영한 것의 넓이가 각각 $1,\,2,\,3$ 이었다고 하자. 이때 $P$ 의 넓이는 얼마인가?

---

문제 6. 으로부터, $P$ 의 넓이는 $\sqrt{1+4+9}=\sqrt{14}$ 임을 안다.



<b>8. </b> 모든 벡터와 수직인 벡터는 영벡터임을 안다.

---

$n$ 차원 공간에서 표준 단위벡터 $\mathbf{e}_1,\ldots,\, \mathbf{e}_n$ 과 모든 벡터에 수직인 벡터 $X=(x_1,\ldots,\,x_n)$ 을 생각하자. $i=1,\,2,\,\ldots,\,n$ 에 대해 $\mathbf{e}_i \cdot X=x_i=0$  이어야 한다. 따라서 모든 벡터와 수직인 벡터는 영벡터이다.



<b>9. </b> 내적이 주어진 공간, 즉 내적공간에서는 벡터 $\mathbf{v}$ 는 함수의 역할을 한다. 
$$
\mathbf{v}^\ast : \mathbf{w}\to \mathbf{v}\cdot \mathbf{w}
$$
이제 두 함수 $\mathbf{v}^\ast_1$ 와 $\mathbf{v}^\ast_2$ 가 같은 함수이면 $\mathbf{v}_1^\ast = \mathbf{v}_2^\ast$ 임을 보이라.

---

임의의 $\mathbf{w}$ 에 대해 $\mathbf{v}^\ast_1 (\mathbf{w})= \mathbf{v}_2^\ast (\mathbf{w})$ 이어야 한다. 따라서,
$$
\mathbf{v}_1\cdot \mathbf{w}=\mathbf{v}_2\cdot \mathbf{w} \implies (\mathbf{v}_1-\mathbf{v}_2)\cdot \mathbf{w}=0
$$
이므로 문제 8에 의해 $\mathbf{v}_1-\mathbf{v}_2=0$ 이어야 한다. 즉 $\mathbf{v}_1=\mathbf{v}_2$ 이다.



<b>10. </b> 두 벡터 $\mathbf{a},\,\mathbf{b}$ 가 수직일 필요충분조건은,
$$
|\mathbf{a}+\mathbf{b}|=|\mathbf{a}-\mathbf{b}|
$$
임을 보이라.

---

(1) 두 벡터 $\mathbf{a}$ 와 $\mathbf{b}$ 가 수직이면 $\mathbf{a} \cdot \mathbf{b}=0$ 이다. 주어진 식으로부터,
$$
|\mathbf{a}+\mathbf{b}|^2-|\mathbf{a}-\mathbf{b}|^2 = 4\mathbf{a}\cdot \mathbf{b}=0
$$
이므로 $|\mathbf{a}+\mathbf{b}|=|\mathbf{a}-\mathbf{b}|$ 이다.

(2) $|\mathbf{a}+\mathbf{b}|=|\mathbf{a}-\mathbf{b}|$ 임을 가정하자.
$$
|\mathbf{a}+\mathbf{b}|=|\mathbf{a}-\mathbf{b}| \implies |\mathbf{a}+\mathbf{b}|^2=|\mathbf{a}-\mathbf{b}|^2\implies \mathbf{a}\cdot \mathbf{b}=0
$$
이므로 $\mathbf{a}$ 와 $\mathbf{b}$ 는 수직이다. 



<b>11. </b> 임의의 두 벡터 $\mathbf{a},\,\mathbf{b}$ 에 대하여
$$
\large| \normalsize|\mathbf{a}|-|\mathbf{b}|\large|\normalsize\ge |\mathbf{a}-\mathbf{b}|
$$
임을 보여라.

---

두 벡터의 사잇각을 $\theta$ 라 하면,
$$
(\large|\normalsize |\mathbf{a}|-|\mathbf{b}|\large|\normalsize)^2-|\mathbf{a}-\mathbf{b}|^2=2|\mathbf{a}||\mathbf{b}|+2\mathbf{a}\cdot \mathbf{b}=2|\mathbf{a}||\mathbf{b}|(1-\cos \theta) \ge 0
$$
이다. 



<b>12. </b>  벡터 $\mathbf{a}=(a_1,\ldots,\,a_n)\ne 0$ 이 표준단위벡터 $\mathbf{e}_1,\ldots,\,\mathbf{e}_n$ 과 이루는 각을 각각 $\theta_i$ 이라고 할 때 다음을 보이라.

(1) $\cos \theta_1=a_1/|\mathbf{a}|,\ldots,\, \cos \theta_n|=a_i/|\mathbf{a}|$ 

(2) $\cos^2\theta_1 + \cdots + \cos^2\theta_n=1$

(3) $(\cos \theta_1,\ldots,\,\cos \theta_n)$ 은 $\mathbf{a}$ 와 같은 방향의 단위벡터이다.

---

(1) $\cos \theta_i = \dfrac{\mathbf{a} \cdot \mathbf{e}_i}{|\mathbf{a}| |\mathbf{e}_i|}=\dfrac{a_i}{|\mathbf{a}|}$ 

(2) $|\mathbf{a}|^2 =a_1^2+\cdots +a_n^2 = |\mathbf{a}|^2(\cos^2 \theta_1 + \cdots + \cos^2 \theta_n)$ 이므로 $\cos^2\theta_1 + \cdots +\cos^2 \theta_n =1$. 

(3) $\mathbf{a}=(a_1,\ldots,\,a_n)=|\mathbf{a}| (\cos \theta_1,\ldots,\,\cos \theta_n)$ 이므로 두 벡터는 같은 방향. (2) 로부터 단위벡터.



<b>13. </b> 좌표공간 $\mathbb{R}^3$ 에서 단위벡터 $\mathbf{v}$ 가 $x$-축과 이루는 각을 $\theta_x$, $y$-축과 이루는 각을 $\theta_y$ 라 하였을 때, $\mathbf{v}$ 가 $xy$-평면과이루는 각 $\alpha$ 는 얼마인가? 또 $\theta_x=\theta_y =60^{\circ}$ 이면 $\alpha$ 는 얼마인가?

---

문제 12 로 부터 $\mathbf{v}=(\cos \theta_x,\, \cos \theta_y,\, \cos \theta_z)$ 이며 $\cos \theta_z =\sqrt{1-\cos^2 \theta_x -\cos^2 \theta_y}$ 임을 안다. $xy$-평면과 이루는 각은 $\mathbf{v}$ 와 $(\cos \theta_x,\,\cos \theta_y,\,0)$ 과 이루는 각이므로,
$$
\cos \alpha= \dfrac{\cos^2 \theta_x + \cos^2 \theta_y}{\sqrt{\cos^2 \theta_x+\cos^2 \theta_y}}=\sqrt{\cos^2 \theta_x + \cos^2 \theta_y}
$$
이 성립한다. 따라서,
$$
\alpha = \arccos \sqrt{\cos^2 \theta_x +\cos^2 \theta_y}
$$
이다. 

$\theta_x =\theta_y=60^\circ$ 라면 $\alpha = \arccos \sqrt{1/2}=45^\circ$ 이다. 



<b>14. </b> 양수 $a,\,b$ 에 대하여
$$
A=(b,\, ab^2),\qquad A'=(-b,\,ab^2)
$$
으로 두고, 또 $t \ne b$ 인 양수 $t$ 에 대하여
$$
P=P(t) = (t,\,at^2)
$$
으로 두면, 이들은 포물선 $y=ax^2$ 위의 점들이 됨을 알 수 있다. 이때 벡터 $\vec{PA}$ 와 $\vec{PA'}$ 이 이루는 각의 크기를 $\theta(t)$ 라고 두면,
$$
\lim_{t \searrow b} \cos \theta(t)=\dfrac{1}{\sqrt{1+4a^2b^2}}\,,\qquad \lim_{t \nearrow b}\cos \theta(t)=-\dfrac{1}{\sqrt{1+4a^2b^2}}
$$
임을 보여라.

---

$$
\vec{PA}=(b-t,\, ab^2-at^2),\qquad \vec{PA'}=(-t-b,\, ab^2-at^2)
$$

이며,
$$
\begin{align}
\cos \theta(t) &= \dfrac{-b^2+t^2+a^2t^4+a^2b^4-2a^2t^2b^2}{\sqrt{(b-t)^2+a^2(b^2-t ^2)^2}\sqrt{(b+t)^2+a^2(b^2-t^2)^2}}\\
&=\dfrac{a^2t^4-(2a^2b^2-1)t^2+b^2(a^2b^2-1)}{|b^2-t^2|\sqrt{1+a^2(b+t)^2}\sqrt{1+a^2(b-t)^2}} \\
&= \dfrac{(t^2-b^2)}{|t^2-b^2|}\dfrac{(a^2t^2-a^2b^2+1)}{\sqrt{1+a^2(b+t^2)}\sqrt{1+a^2(b-t^2)}} \\
\end{align}
$$
이다. 따라서,
$$
\lim_{t \searrow b}\cos \theta(t)=\dfrac{1}{\sqrt{1+4a^2b^2}},\qquad \lim_{t \nearrow b}\cos \theta(t)=-\dfrac{1}{\sqrt{1+4a^2b^2}}
$$


<b>15. </b> (**코사인법칙**) 변의 길이가 각각 $a,\,b,\,c$ 인 삼각형에서 "$a$-변" 과 "$b$-변" 사이의 각을 $\theta$ 라 하면
$$
c^2=a^2+b^2-2ab\cos \theta
$$
임을 보이라.

---

삼각형의 세 꼭지점을 $A,\,B,\,C$ 라 하고 $\mathbf{a}=\vec{BC},\, \mathbf{b}=\vec{CA},\, \mathbf{c}=\vec{AB}$ 라 하자. 또한 $a=|\mathbf{a}|,\, b=|\mathbf{b}|,\, c=|\mathbf{c}|$ 라 하자. 그렇다면 $\cos \theta$ 는 $\mathbf{a}$ 와 $\mathbf{b}$ 의 사잇각이다. $\mathbf{a}+\mathbf{b}=\mathbf{c}$ 이므로,
$$
c^2=|\mathbf{c}|^2=|\mathbf{a}+\mathbf{b}|^2=a^2+b^2+2\mathbf{a}\cdot \mathbf{b}=a^2+b^2+2ab\cos \theta
$$
이다.



<b>16. </b> $x^2+2y^2+3z^2=1$ 일 때 $x+y+z$ 의 최대값과 최소값을 구하라.

---

$\mathbb{R}^3$ 에서의 세 백터 $\mathbf{x}=(x,\, \sqrt{2}y,\,\sqrt{3}z)$ 와 $\mathbf{a}=(1,\,1/\sqrt{2},\,1\sqrt{3})$ 을 생각한다. $|\mathbf{x} \cdot \mathbf{a}|^2\le |\mathbf{x}|^2|\mathbf{a}|^2$ 를 이용하면,
$$
|\mathbf{x}\cdot \mathbf{a}|^2=|x+y+z|가 ^2\le |x^2+2y^2+3z^3|\cdot\dfrac{11}{6}=\dfrac{11}{6}
$$
 따라서 최대값은 $\sqrt{11/6}$ 최소값은 $-\sqrt{11/6}$ 이다. 



<b>17. </b> 다음은 중심의 위치가 $P_0,\,P_1,\,P_2$ 이고 질량이 같은 세개의 당구공이 당구대위에 놓여 있는것을 위에서 본 그림이다.

(그림 생략)

이 때 당구공 $P_0$ 를 때려, 이것이 당구공 $P_1$ 을 맞춘 다음 당구공 $P_2$ 와 속력 $v_2$ 로 정면 충돌하기 위해서는 처음에 당구공 $P_0$ 를 어느 방향으로 얼마만큼의 속력으로 때려야 하는가. 

---

당구공의 질량이 모두 같으므로 $1$ 로 놓아도 된다.  운동량 보존에 의해 $\mathbf{v}_0=\mathbf{v}_1+\mathbf{v}_2$ 이다. 탄성충돌을 가정한다면 $|\mathbf{v}_0|^2=|\mathbf{v}_1|^2+|\mathbf{v}_2|^2$ 이다.  $P_1P_2$ 와 $P_2P_3$ 의 사잇각을 $\theta$ 라 하면 $v_0=v_2/\cos \theta$ 이어야 한다. 



#### 4.1.2 기본연습문제

<b>1. </b> $n$ 공간의 한 점 $Q$ 와 초평면 $\mathbf{a}\cdot (X-P)=0$ 사이의 거리는
$$
\dfrac{|\mathbf{a}\cdot (Q-P)|}{|\mathbf{a}|}
$$
 임을 보이라.

---

$Q$ 와 초평면 $\mathbf{a}\cdot(X-P)$ 사이의 거리는 $(Q-P)$ 의 $\mathbf{a}$ 방향으로의 정사영의 크기이다.  이 정사영을 $k\mathbf{a}$ 라 하면 $(k\mathbf{a} -(Q-P) ) \cdot \mathbf{a}=0$ 이므로,
$$
k|\mathbf{a}|^2=\mathbf{a}\cdot (Q-{P})\implies |k\mathbf{a}|= \dfrac{|\mathbf{a}\cdot (Q-P)|}{|\mathbf{a}|}
$$


이다.



<b>2. </b> 원점과 평면 $ax+by+cz=d$ 사이의 거리를 구하라. 

---

$a(x-x_0)+b(y-y0)+c(z-z_0)=0$ and $ax_0+by_0+cz_0=d$ 라 하면 이 식이 평면의 방정식이다. 이를 1.에 대입하면,
$$
[\text{distance}]=\dfrac{|ax_0+by_0+cz_0|}{\sqrt{a^2+b^2+c^z}}= \dfrac{|d|}{\sqrt{a^2+b^2+c^z}}
$$


