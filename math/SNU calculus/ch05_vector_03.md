



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
이 존재한다. 이는 
$$
c_1(P_1-P_0)+c_2(P_2-P_0)+ \cdots c_k (P_k-P_0)=0 \implies -(c_1+\cdots c_k)P_0 +c_1P_1 + \cdots +c_k P_k=0
$$
이며 $
