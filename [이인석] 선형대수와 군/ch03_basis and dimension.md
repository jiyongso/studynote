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

(라) 일단 원점을 지나는 평면은 모두 $ax+by+cz=0$ 꼴임을 알고 있다고 가정하고 진행한다. 

우선 $\{u,\,v,\,w\}$ 가 일차종속이면 $u,\,v,\,w$ 가 $0$ 을 지나는 하나의 평면 위에 존재함을 보인다.  $\{u,\,v,\,w\}$ 중 zero vector가 존재한다면 일차 종속이다(가). 셋 다 $0$ 이면 자명하다. 셋중 둘이 $0$ 벡터라 하자. $u=v=0$ 이며 $w\ne 0$ 이면 $aw_1+bw_2+cw_3=0$ 에서 $w_3\ne 0$ 이면 $c=-(aw_1+bw_2)/w_3$ 로 잡고 평면의 방정식 $ax+by+cz=0$ 을 세우면 $u,\,v,\,w$ 는 모두 이 평면상에 있다. $w_3=0$ 이면 nonzero component of $w$ 에 대해 같은 방법으로 풀면 된다.

$u=0$, $v\ne 0,\,w \ne 0$ 이면 $\alpha v+ \beta w=0$ 인 $\alpha,\, \beta\in \mathbb{F}$, $\alpha \ne 0,\, \beta \ne 0$ 이 존재한다. 
$$
\alpha v+\beta w= (\alpha v_1+\beta w_1,\, \alpha v_2+\beta w_2,\, \alpha v_3 + \beta w_3)=(0,\,0,\,0)
$$

이므로 $\beta\\\\