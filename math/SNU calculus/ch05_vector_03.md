



V. 벡터 #3
===

## 제 5 장 탐구문제



<b>1. </b> 공간의 점 $P_0,\,P_1,\ldots,\,P_k$ 에 대하여 벡터

$$
\overrightarrow{P_0P_1},\ldots,\,\overrightarrow{P_0P_k}
$$
가 일차독립이면, 점 $P_0,\,P_1,\ldots,\,P_k$ 는 일반위치 (general position) 에 있다고 한다. 공간속의 점 $P_0,\ldots,\,P_k$ 가 일반위치에 있기 위한 필요충분조건은 벡터,
$$
\overrightarrow{P_0P_1},\,\overrightarrow{P_1P_2},\ldots,\,\overrightarrow{P_{k-1}P_k}
$$
가 일차독립인 것을 보여라.

---

(1) $\mathbf{a}_i = \overrightarrow{P_0P_k}$ 라 하고, $\mathbf{b}_i = \overrightarrow{P_{i-1}P_i}$ 이라 하자. $\mathbf{b}_1=\mathbf{a}_1,\,\mathbf{b_i}= \mathbf{a}_i-\mathbf{a}_{i-1}$ for $i=2,\ldots,\,k$ 임을 알 수 있다. 

(2) $\mathbf{a}_1,\ldots,\,\mathbf{a}_k$ 가 일차독립임을 가정하자. 
$$
\begin{align}
c_1 \mathbf{b}_1 + \cdots + c_k \mathbf{c}_k=0 &\implies c_1(\mathbf{a}_1)+c_2(\mathbf{a}_2-\mathbf{a}_1)+ \cdots + c_k (\mathbf{a}_k -\mathbf{a_{k-1}})=0 \\
&\implies (c_1-c_2)\mathbf{a}_1+(c_2-c_3)\mathbf{a}_2 + \cdots +(c_{k-1}-c_k)\mathbf{a}_{k-1}+c_k \mathbf{a}_k=0 \\
&\implies c_k =0,\, c_k=c_{k-1}=\cdots =c_2=c_1\\
&\implies c_1=c_2=\cdots =c_k=0

\end{align}
$$
따라서 $\mathbf{b}_1,\ldots,\,\mathbf{b}_k$ 는 일차독립이다.

(3) $\mathbf{b}_1,\ldots,\,\mathbf{b}_k$ 가 일차독립임을 가정하자. $\mathbf{a}_1=\mathbf{b}_1$ 이며, $\mathbf{a}_j = \mathbf{b}_1+\cdots +\mathbf{b}_j$ 이므로, 
$$
\begin{align}
d_1\mathbf{a}_1 + \cdots +d_k \mathbf{a}_k = 0 &\implies d_1\mathbf{b}_1+ d_2(\mathbf{b}_1+\mathbf{b}_2)+ \cdots + d_k(\mathbf{b}_1+\cdots +\mathbf{b_k})=0\\
&\implies  (d_1+\cdots +d_k)\mathbf{b_1}+ (d_2 + \cdots +d_k)\mathbf{b}_2 +\cdots + d_k\mathbf{b}_k =0 \\
&\implies d_k=0,\, d_k+d_{k-1}=0 ,\ldots, \, d_1+ \cdots + d_k = 0\\
&\implies d_1=d_2=\cdots =d_k=0

\end{align}
$$
따라서 $\mathbf{a}_1,\ldots,\,\mathbf{a}_k$ 도 일차독립이다.





<b>2. </b> 평면에서 일반위치에 있는 석점 $P_1,\,P_2,\,P_3$ 와 $m_1+m_2+m_3=1$ 인 실수 $m_1,\,m_2,\,m_3$ 에 대하여,
$$
Q:=m_1P_1+m_2P_2+m_3P_3
$$
로 두자. 이 때 점 $Q$ 를 지나고 직선 $P_2P_3$ 와 나란한 직선이 직선 $P_1P_2$ 와 만나는 점은
$$
m_1P_1 +(m_2+m_3)P_2
$$
임을 보이라.

---

$Q$ 를 지나고 직선 $P_2P_3$ 나란한 직선이 직선 $P_1P_2$ 와 만나는 점 $S$ 의 위치는 어떤 실수 $0\le r \le 1$ 에 대하여 $rP_1+(1-r)P_2$ 라 할 수 있다. $QS$ 와 $P_2P_3$ 는 평행하므로, 어떤 실수 $t$ 에 대해 $tQS=P_2P_3$ 이다. 즉,
$$
t\left(rP_1+(1-r)P_2 - m_1P_1-m_2P_2-m_3P_3\right)= P_3-P_2
$$
이다. 여기서 $P_1,\,P_2,\,P_3$ 가 일반위치에 존재하므로,
$$
(tr-tm_1)P_1 +(t-tr-tm_2+1)P_2 -(tm_3+1)P_3=0
$$
그렇다면 $tr-tm_1=0,\, t-tr-tm_2+1=0,\, tm3+1=0$ 이다. $t(r-m_1)=0$ 에서 $t=0$ 이면 두번째 조건에서 $1=0$ 이 되므로 모순. 따라서 $t\ne 0$ and $r=m_1$ 이다. 즉,
$$
S=m_1P_1+(1-m_1)P_2=m_1P_1+(m_2+m_3)P_2
$$
이다. 



<b>3. </b> 공간의 점 $P_0,\,P_1,\ldots,\,P_k$ 가 일반위치에 있지 않으면,
$$
t_0+\cdots + t_k = 1=t'_0+\cdots+t_k'\\
(t_0,\ldots,\,t_k) \ne (t'_0,\ldots,\, t'_k)\\
t_0P_0 + \cdots + t_k P_k = t'_0P_0 + \cdots + t_k'P_k
$$
을 만족시키는 실수 $t_0,\ldots,\,t_k,\,t'_0,\ldots,\,t'_k$ 가 존재함을 보이라.

---

Let $\mathbf{a}_i = \overrightarrow{P_iP_0}$ for $i=1,\ldots,\,n$. 문제 1에 의해 $\mathbf{a}_1,\ldots,\,\mathbf{a}_k$ 는 일차종속이므로, 어떤 nonzero $c_1,\ldots,\,c_k$ 에 대해
$$
c_1\mathbf{a}_1+\cdots +c_k\mathbf{a}_k=0
$$
이며,
$$
c_1(P_1-P_0)+c_2(P_2-P_0)+ \cdots c_k (P_k-P_0)=0 \implies -(c_1+\cdots +c_k)P_0 +c_1P_1 + \cdots +c_k P_k=0
$$
을 만족시키는 nonzero $c_1,\ldots,\,c_k$ 가 존재함을 의미한다. 이제 $c_0=-(c_1+\cdots+c_k )$ 라 하면,
$$
c_0P_0+\cdots +c_kP_k=0
$$
을 만족하는 $c_0,\ldots,\,c_k$ 중 최소한 하나는 $0$ 이 아님을 의미한다. $c_0 \ne 0$ 이면 어떤 $c_1,\ldots,\,c_k$ 중 nonzero 인 것이 존재한다. 따라서,
$$
P_0 = \dfrac{1}{(c_1+\cdots + c_k)}\left(c_1P_1+\cdots c_k P_k\right)
$$
이므로 $t_0=1,\,t_2=\cdots = t_k=0$ 과 $t'_0=0,\,t'_k = c_k/(c_1+\cdots +c_k)$ 이면 주어진 조건을 만족한다.

$c_0=0$ 이면 $c_1+\cdots + c_k=0$ 이며 최소한 하나의 $c_1,\ldots,\,c_k$ 는 nonzero 이다. $c_1P_1+\cdots + c_kP_k=0$ 이므로,
$$
P_1 + c_1P_1+\cdots +c_kP_k = P_1
$$
이며 주어진 조건을 만족한다. 



<b>4. </b> 벡터 $\mathbf{v}_1,\ldots,\,\mathbf{v}_k$ 에 의하여 생긴 **(선형)부분공간** 이란
$$
\langle\langle \mathbf{v}_1,\ldots,\,\mathbf{v}_k\rangle\rangle :=\{t_1\mathbf{v}_1+\cdots + t_k\mathbf{v}_k\mid t_1,\ldots,\,t_k\in \mathbb{R}\}
$$
을 뜻한다. 이 때 $\langle\langle \mathbf{v}_1,\ldots,\,\mathbf{v}_k\rangle\rangle$ 의 차원은 $k$ 를 넘지 않음을 보여라.

---

trivial



<b>5. </b> 삼차원 좌표공간에서 식
$$
x+y+z=0,\quad x-y-z=0
$$
을 만족시키는 점들의 집합은 벡터공간임을 보이고, 그 벡터공간의 기저를 구하라.

---

$X=\{(x,\,y,\,z) \in \mathbb{R}^3: x+y+z=0,\, x-y-z=0\}$ 는 문제에 주어진 집합이다. $(x,\,y,\,z),\,(x',\,y',\,z')\in X$ 라 하고 임의의 $a,\,b\in \mathbb{R}$ 에 대해,
$$
a(x,\,y,\,z)+b(x',\,y',\,z') =(ax+bx',\, ay+by',\,az+bz')\in X
$$
임을 보이면 된다. 
$$
(ax+bx')+(ay+by')+(az+bz')=a(x+y+z)+b(x'+y'+z')=0\\
(ax+bx')-(ay+by')-(az+bz')=a(x-y-z)+b(x'-y'-z')=0
$$
이므로 $a(x,\,y,\,z)+b(x',\,y',\,z')\in X$ 이다. 따라서 $X$ 는 벡터공간이다.

$x+y+z=0$ 과 $x-y-z=0$ 을 만족하는 $(x,\,y,\,z)$ 는 임의의 $t\in \mathbb{R}$ 에 대해 $(0,\,t,\,-t)$ 이어야 한다. 따라서 기저는 $(0,\,1,\,-1)$ 일 수 있다.



<b>6. </b> (**Gram-Schmidt 방법**) 일차독립인 벡터 $\mathbf{v}_1,\ldots,\,\mathbf{v}_k$ 에 대하여,
$$
\mathbf{w}_i :=\mathbf{v}_i - \dfrac{\mathbf{v}_i\cdot \mathbf{w}_1}{\mathbf{w}_1 \cdot \mathbf{w}_1} \mathbf{w}_1 - \cdots - \dfrac{\mathbf{v}_i \cdot \mathbf{w}_{i-1}}{\mathbf{w}_{i-1}\cdot \mathbf{w}_{i-1}} \mathbf{w}_{i-1}\quad (i=1,\ldots,\,k)
$$
로 정의하자. 이 때 $\mathbf{w}_i\ne 0$ 임을 보이라. 또,
$$
\mathbf{u}_i = \dfrac{\mathbf{w}_i}{|\mathbf{w}_i|} \quad (i=1,\ldots,\,k)
$$
로 두면, 임의의 $i\in \{1,\ldots,\,k\}$ 에 대하여
$$
\langle\langle \mathbf{u}_1,\ldots,\,\mathbf{u}_i\rangle\rangle = \langle\langle \mathbf{v}_1,\ldots,\,\mathbf{v}_i\rangle \rangle \\
\mathbf{u}_i \perp \langle\langle \mathbf{u}_1,\ldots,\,\mathbf{u}_{i-1}\rangle \rangle ,\,\quad \mathbf{u}_i \cdot \mathbf{v}_{i} >0,\quad |\mathbf{u}_i|=1
$$
임을 보이라. 따라서 $\mathbf{u}_1,\ldots,\,\mathbf{u}_k$ 는 서로 수직인 단위벡터가 된다.

----

(1) $\mathbf{w}_1=\mathbf{v}_1$ 이므로 $\mathbf{w}_1\ne 0$ 이다. $\mathbf{w}_i$ 는 linear combination of $\mathbf{v}_i ,\,\mathbf{w}_1,\ldots,\,\mathbf{w}_{i-1}$ 이며, 
$$
\mathbf{w}_i = \mathbf{v}_i - \left(\text{linear combination of }\mathbf{v}_1,\cdots,\,\mathbf{v}_{i-1}\right)
$$
이다. $\mathbf{v}_1,\ldots,\,\mathbf{v}_k$ 는 일차독립이므로 $\mathbf{w}_i\ne 0$ 이다. 

(2) $\mathbf{u}_j$ 는 linear combination of $\mathbf{v}_1,\ldots,\,\mathbf{v}_j$ 이므로 $\langle\langle \mathbf{u}_1,\ldots,\,\mathbf{u}_i\rangle\rangle \subset \langle\langle \mathbf{v}_1,\ldots,\,\mathbf{v}_i\rangle\rangle$ 이다. 

$\mathbf{u}_1,\ldots,\,\mathbf{u}_k$ 가 일차독립임을 보이기 위해 다음을 보이자.

> $n$ 공간의 영벡터가 아닌 벡터들  $\mathbf{a}_1,\ldots,\,\mathbf{a}_n$ 에서 $i\ne j \implies \mathbf{a}_i \cdot \mathbf{a}_j= 0$ 이면 $\mathbf{a}_1,\ldots,\,\mathbf{a}_n$ 은 일차독립이다.

이를 보이기 위해 $c_1\mathbf{a}_1+\cdots c_n\mathbf{a}_n=0$ 이라 하자. 이 벡터에 임의의 벡터 $\mathbf{a}_j$ 와의 내적을 구하면, $c_j |\mathbf{a}_j|^2=0$ 이므로 $c_j=0$ 이다. 따라서 $\mathbf{a}_1,\ldots,\,\mathbf{a}_n$ 은 일차독립이다.

이제 $\mathbf{w}_1,\ldots,\,\mathbf{w}_k$ 에 대하여 $1\le i,\,j\le k,\, i \ne j \implies. \mathbf{w}_i\cdot\mathbf{w}_j=0$ 임을 보이자.
$$
\mathbf{w}_2 = \mathbf{v}_2 -\dfrac{\mathbf{v}_2\cdot \mathbf{w}_1}{\mathbf{w}_1 \cdot \mathbf{w}_1}\mathbf{w}_1 \implies \mathbf{w}_1 \cdot \mathbf{w}_2 = \mathbf{w}_1\cdot \mathbf{v}_1 -\mathbf{w}_1 \cdot \mathbf{w}_1=0
$$
이다. 임의의 $n$ 에 대해 $0\le i\ne j\le n$ 에서 $\mathbf{w}_i \cdot \mathbf{w}_j =0$ 임을 가정하자.
$$
\mathbf{w}_{n+1}=\mathbf{v}_{n+1} -\sum_{j=1}^{n} \dfrac{\mathbf{v}_{n+1}\cdot \mathbf{w}_j}{\mathbf{w}_j \cdot \mathbf{w}_j}\mathbf{w}_j \implies \mathbf{w}_{n+1}\cdot \mathbf{w}_i = \mathbf{v}_{n+1} \cdot \mathbf{w}_i-\sum_{j=1}^{n} \dfrac{\mathbf{v}_{n+1}\cdot \mathbf{w}_j}{\mathbf{w}_j \cdot \mathbf{w}_j}(\mathbf{w}_j \cdot \mathbf{w}_i) = \mathbf{v}_{n+1}\cdot \mathbf{w}_i-\mathbf{v}_{n+1}\cdot \mathbf{w}_i=0
$$
이다. 즉 induction에 의해 $\mathbf{w}_1,\ldots,\,\mathbf{w}_k$ 는 일차독립임을 보였다. 따라서 $\mathbf{u}_1,\ldots,\,\mathbf{u}_k$ 는 일차독립이다. 따라서 $\mathbf{u}_1,\ldots,\,\mathbf{u}_i$ 는 일차독립이다. (일차독립인 집합의 부분집합은 일차독립이다.)

이제 $\langle\langle \mathbf{u}_1,\ldots,\,\mathbf{u}_i\rangle\rangle \supset \langle\langle \mathbf{v}_1,\ldots,\,\mathbf{v}_i\rangle\rangle$ 임을 보이자. 우리는 $\mathbf{u}_1,\ldots,\,\mathbf{u}_i$ 가 일차독립이며, $\langle\langle \mathbf{u}_1,\ldots,\,\mathbf{u}_i\rangle\rangle \subset \langle\langle \mathbf{v}_1,\ldots,\,\mathbf{v}_i\rangle\rangle$  임을 안다. 만약 $\langle\langle \mathbf{u}_1,\ldots,\,\mathbf{u}_i\rangle\rangle \ne \langle\langle \mathbf{v}_1,\ldots,\,\mathbf{v}_i\rangle\rangle$ 이면 어떤 $\mathbf{v}\in \langle\langle \mathbf{v}_1,\ldots,\,\mathbf{v}_i\rangle\rangle$ 에 대해 $v \not\in \langle\langle \mathbf{u}_1,\ldots,\,\mathbf{u}_i\rangle\rangle $  이어야 한다. 















<b>7. </b> 두 연속함수 $f,\,g:[0,\,1]\to \mathbb{R}$ 에 대하여
$$
\langle f,\,g \rangle:=\int_0^1 f(t)g(t)\,dt,\qquad \|f\|:=\sqrt{\langle f,\,f\rangle}
$$
로 정의하자. 이 때,
$$
\langle f,\,g\rangle \le \|f\|\cdot\|g\|
$$
임을 보이라. 여기서 등호가 성립할 때는 언제인가? 또,
$$
\left(\int_0^1 f(t)\,dt\right)^2 \le \int_0^1 f(t)^2 \,dt
$$
임을 보이라.

---

우선,
$$
\|f\|^2=\langle f,\,f\rangle =\int_0^1 f(t)^2 \, dt \ge 0
$$
이며 $\|f\|=0 \iff f(t)=0,\, \forall t\in [0,\,1] $ 임을 알 수 있다. 임의의 $\lambda \in \mathbb{R}$ 에 대해 $\|f+\lambda g\|\ge 0$ 이므로,
$$
\int_0^1 (f(t)+\lambda g(t))^2\,dt =\|f\|^2+2\lambda \langle f,\,g\rangle+\lambda^2\|g\|^2 \ge 0
$$
 이다 따라서, 
$$
\langle f,\,g\rangle^2 -\|f\|^2\cdot \|g\|^2 \le 0 \implies \langle f,\,g\rangle\le |\langle f,\,g\rangle |\le \|f\|\cdot \|g\|
$$
이다. 만약 $g(t)=c f(t)$ for some $c >0 $ 이면 $\langle f,\,g\rangle = c\|f\|^2 =\|f\|\cdot \|cf\|$ 이다. 

$g(t)=1$ 이라 하면 연속함수이므로,
$$
\begin{align}
\langle f,\,1\rangle &= \int_0^1 f(t)\, dt\,\\
\|f\| &= \sqrt{\int_0^1 f(t)^2\, dt}\\
\|1\| &=\sqrt{\int_0^1 1\, dt}=1

\end{align}
$$
이며,
$$
\left|\int_0^1 f(t)\, dt \right|= \left|\langle f,\,1\rangle\right| \le \|f\|\cdot \|1\|=\sqrt{\int_0^1 f(t)^2\, dt}
$$
이므로, 양 변을 제곱하면,
$$
\left(\int_0^1 f(t)\,dt\right)^2 \le \int_0^1 f(t)^2 \,dt
$$
를 얻는다. 



<b>8. </b> 다음 네 행렬은 일차독립인가?
$$
\begin{pmatrix} 0 & 1 \\ 1 & 1\end{pmatrix}, \quad \begin{pmatrix} 1 & 0 \\ 1 & 1\end{pmatrix},\quad \begin{pmatrix} 1 & 1 \\ 0 & 1\end{pmatrix},\quad \begin{pmatrix} 1 & 1 \\ 1 & 0\end{pmatrix}
$$

---

$$
\begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}=a\begin{pmatrix} 0 & 1 \\ 1 & 1\end{pmatrix}+ b\begin{pmatrix} 1 & 0 \\ 1 & 1\end{pmatrix}+c\begin{pmatrix} 1 & 1 \\ 0 & 1\end{pmatrix}+d\begin{pmatrix} 1 & 1 \\ 1 & 0\end{pmatrix} = \begin{pmatrix} b+c+d & a+c+d \\ a+b+d & a+b+c\end{pmatrix}
$$

이다, 즉,
$$
a+b+c=0\\
a+b+d=0\\
a+c+d=0\\
b+c+d=0
$$
을 만족하는 $a,\,b,\,c,\,d$ 를 찾자. 네 식을 더하면 $3(a+b+c+d)=0$ 이므로 $a+b+c+d=0$ 이다. 따라서 $a=b=c=d=0$ 이다. 따라서 일차독립이다.



<b>9. </b> 미분방정식
$$
f''(x)-f(x)=0
$$
을 만족히키는 함수 $f:\mathbb{R} \to \mathbb{R}$ 전체의 집합을 $V$ 라고 두자. 이 때

(1) $V$ 는 벡터공간임을 설명하라.

(2) $V$ 의 한 원소 $f$ 가 서로 다른 실수 $a,\,b$ 에 대하여 $f(a)=f(b)=0$ 이면
$$
\int_a^b f(x)^2 \, dx = -\int_a^b f'(x)^2\, dx
$$
임을 보이라.

(3) 함수 $e^x$ 와 $e^{-x}$ 는 $V$ 의 기저임을 보이라.

(4) $V$ 의 차원을 구하라.

---

(1) $f,\,g\in V,\, c\in \mathbb{R}$ 에 대해 $(f(x)+cg(x))''-(f(x)+cg(x))=(f''-f(x))+c(g''(x)-g(x))=0$ 이므로 $f+cg\in V$ 이다. 따라서 벡터공간이다.

(2) $f(x)=f''(x)$ 이므로,
$$
\int_a^b f(x)^2\,dx = \int_a^b f(x)f''(x)\,dx = \left[f(x)f'(x)\right]_{x=a}^{x=b}-\int_a^b f'(x)f'(x)\,dx=-\int_a^b f'(x)^2\,dx
$$
(3) $e^x,\, e^{-x}\in V$ 임은 쉽게 알 수 있다. 또한 $c_1e^x+c_2e^{-x}=0\implies c_1=c_2=0$ 이므로 $e^x,\,e^{-x}$ 는 일차독립이다. 주어진 미분방정식을 만족시키는 함수는 $e^x$ 와 $e^{-x}$ 의 선형 결합 함수 뿐이므로 (이게 미적분학 범위인가....) $\{e^x,\,e^{-x}\}$ 는 $V$ 의 기저이다.

(4) (3) 에 따라 2 차원이다.



<b>10. </b> 등장사상 $T:\mathbb{R}^n \to \mathbb{R}^n$ 에 대하여,
$$
X\mapsto \operatorname{dist}(X,\,T(X)),\qquad(X\in \mathbb{R}^n)
$$
가 상수함수이면 $T$ 는 평행이동임을 보여라.

---

$f:\mathbb{R}^n\to \mathbb{R}$ 을 $f(X)=\operatorname{dist}(X,\,T(X))=\|X-T(X)\|$ 로 정의한다. $T$ 가 평행이동이면 $f$ 가 상수함수임은 자명하다. 



<b>11. </b> 실수 $c_1,\,c_2,\,c_3,\,c_4$ 에 대하여 미지수 $x,\,y,\,z$ 에 관한 방정식
$$
\begin{align}
x + y + z &= c_1 \tag{1}\\
x + 2y + 3z &= c_2 \tag{2}\\
x + 4y + 9z &= c_3 \tag{3}\\
x + 8y + 27 z &= c_4 \tag{4}



\end{align}
$$
는 일반적으로 해를 가지지 않음을 설명하라.

---

$\mathbb{R}^3$ 에서 생각하자. $X=(x,\,y,\,z),\, A=(1,\,1,\,1),\,B=(1,\,2,\,3),\,C=(1,\,4,\,9),\,D=(1,\,8,\,27)$ 이라 하면 위 식은,
$$
X\cdot A=c_1,\quad X\cdot B=c_2,\quad X\cdot C=c_3,\quad X\cdot D=c_4
$$
가 된다. $\mathbb{R}^3$ 의 기저벡터는 3개이며, 
$$
\begin{align}
aA+bB+cC=0 &\implies (a+b+c,\, a+2b+4c,\, a+3b+9c)=(0,\,0,\,0)\\
&\implies a+b+c=0,\, b+3c=0,\, b+5c=0\\
&\implies a=b=c=0

\end{align}
$$
이므로 $A,\,B,\,C$ 는 $\mathbb{R}^3$ 의 기저이다. $D=6A-11B+6C$ 이므로, 
$$
c_4=X\cdot D=X\cdot (6A-11B+6C)=6c_1-11c_2+6c_3
$$
이어야 한다. 만약 $6c_1-11c_2+6c_3-c_4\ne 0$ 이면  방정식들은 해를 갖지 않는다.





<b>12. </b> 차수가 $n$ 이하인 다항식 전체로 이루 어진 공간의 차원은 $n+1$ 임을 설명하라.

---

일단 차수가 $n$ 이하인 다항식 전체로 이루어진 공간은 $1,\,x,\,x^2,\ldots,\,x^n$ 의 선형결합으로 이루어진다.
$$
c_0+c_1x+c_2x^2+ \cdots + c_nx^n=0
$$
이라 하면 $c_0= c_1=\cdots =c_n=0$ 이므로 기저는 $1,\,x,\,x^2,\ldots,\,x^n$ 이다. 따라서 $n+1$ 차원 공간이다. 





