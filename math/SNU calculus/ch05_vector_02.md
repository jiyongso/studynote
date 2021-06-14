V. 벡터 #2
===



## 연습문제 : 제 5장 4절



<b>1. </b> 좌표평면의 두 직선 $y=mx+b$ 와 $y=m'x+b'$ 이 서로 수직일 필요충분조건은 $mm'=-1$ 임을 보여라.

---

$x+\dfrac{b}{m}=\dfrac{y}{m}$ , $x+\dfrac{b'}{m'}=\dfrac{y}{m'}$ 으로 부터 두 직선의 방향은 $(1,\, 1/m),\, (1,\, 1/m')$ 이다. 

두 직선이 수직 $\iff$ 두 방향벡터의 내적이 $0$ $\iff$ $1+\dfrac{1}{mm'}=0 \iff mm'=-1$. 



<b>2 </b> 생략



<b>3. </b> 삼차원 공간에서 원점에 광원이 위치하고 스크린이 평면
$$
ax+by+cz=d \qquad (a^2+b^2+c^2 \ne 0,\, d\ne 0)
$$
으로 주어졌을 때 점 $P=(p,\, q,\,r)$ 의 상의 위치를 구하여라.

---

원점과  $(p,\,q,\,r)$ 을 지나는 직선은 $(pt,\,qt,\,rt)$ 로 쓸 수 있으며 이것의 상의 위치는 $t=\dfrac{d}{ap+bq+cr}$ 로 정해진다. 즉
$$
\left(\dfrac{pd}{ap+bq+cr},\, \dfrac{qd}{ap+bq+cr},\, \dfrac{rd}{ap+bq+cr}\right)
$$
이며 $ap+bq+cr=0$ 이면 해가 존지하지 않는다.



<b>4. </b> 평면상에서 두 직선 $l,\,l'$ 과 이 직선 밖의 한 점 $O$ 를 생각하자. 이제 $l$ 상의 한 점 $P$ 와 $O$ 를 잇는 직선이 $l'$ 과 만나는 점을 $P'$ 이라고 두자. 



이 때 $P'$ 이 존재하는 $P\in l$ 의 집합을 $l_\ast$ 라고 하였을 때, $l_\ast$ 의 임의의 네 점 $P_1,\,P_2,\,P_3,\,P_4$ 에 대하여,
$$
\dfrac{\overline{P_1P_2}\cdot \overline{P_3P_4}}{\overline{P_1P_4}\cdot \overline{P_2P_3}}=\dfrac{\overline{P'_1P'_2}\cdot \overline{P'_3P'_4}}{\overline{P'_1P'_4}\cdot \overline{P'_2P'_3}}
$$

---

$O$ 를 원점으로 이동하고 회전시켜 $l'$ 이 $x$ 축과 평행하도록 하자. 도형을 축소시켜 $l'$ 이 $y=1$ 선상에 있도록 하고 이 때 $l$ 의 직선의 방정식을 $y=ax+b$ 라 하자. $P'_1,\,P'_2,\,P'_3,\,P'_4$ 의 좌표를 각각 $(x'_1,\,1),\, (x'_2,\,1),\, (x'_3,\,1),\, (x'_4,\,1)$이라 하자. 

원점과 $(x'_1,\,1)$ 을 지나는 직선의 방정식은 $y=\dfrac{1}{x'_1}x$ 이다. 이것과 $l$ 과의 교점 $P_1$ 의 좌표는 $\dfrac{b}{1-ax_1'}\left(x_1',\,1\right)$ 이다. 즉,
$$
P_i = \left(\dfrac{b}{1-ax'_i}x'_i,\,\dfrac{b}{1-ax'_i}\right)
$$
이다. 
$$
\dfrac{\overline{P'_1P'_2}\cdot \overline{P'_3P'_4}}{\overline{P'_1P'_4}\cdot \overline{P'_2P'_3}}=\dfrac{|x_1'-x_2'|\cdot|x_3'-x_4'|}{|x_1'-x_4'|\cdot |x_2'-x_3'|}
$$
이며,
$$
\dfrac{\overline{P_1P_2}\cdot \overline{P_3P_4}}{\overline{P_1P_4}\cdot \overline{P_2P_3}} = \dfrac{|x_1'-x_2'|\cdot|x_3'-x_4'|}{|x_1'-x_4'|\cdot |x_2'-x_3'|}=\dfrac{\overline{P'_1P'_2}\cdot \overline{P'_3P'_4}}{\overline{P'_1P'_4}\cdot \overline{P'_2P'_3}}
$$
임을 알 수 있다.



<b>5. </b> (a) 공간속의 한 점 $A$ 에서 평면 $\mathbf{n}\cdot (X-P)=0$ 에 내린 수선의 발을 구하라.

(b) (**반사변환**(reflection)) 평면 $\mathbf{n}\cdot X =0$ 에 대한 점 $A$ 의 대칭점 $A'$ 을 구하라. 또 평면 $\mathbf{n}\cdot (X-P)$ 에 대한 점 $A$ 의 대칭점 $A''$ 을 구하라.

---

(a) $A=(a_1,\ldots,\,a_k)$ 를 지나며 방향벡터가 $\mathbf{n}=(n_1,\ldots,\,n_k)$ 인 직선은 $x_i = n_i t+a_i$ for $i=1,\ldots,\,k$ 로 나타 낼 수 있다. 직선과 평면의 교점이 수선의 발이므로 교점을 구하자. 수선의 발의 위치를 $Q$ 라 하면,
$$
\mathbf{n}\cdot (\mathbf{n}t+A-P)=0 \implies t=\dfrac{\mathbf{n}\cdot (P-A)}{|\mathbf{n}|^2} \implies Q=\left(\dfrac{\mathbf{n}\cdot (P-A)}{|\mathbf{n}|^2}\right)\mathbf{n} +A
$$
이다.

(b) $A''+A=2Q$ 이므로 $A'' =2Q-A$ 이다. 즉, 
$$
A''=2\left(\dfrac{\mathbf{n}\cdot (P-A)}{|\mathbf{n}|^2}\right)\mathbf{n} +A
$$
$A'$ 은 $A''$ 에서 $P=0$ 일 때 이다.
$$
A'=-2\left(\dfrac{\mathbf{n}\cdot A}{|\mathbf{n}|^2}\right)\mathbf{n} +A
$$


<b>6. </b> 좌표공간에서 평면 $x+y+2z=1$ 에 대하여 점 $P=(1,\,1,\,1)$ 의 대칭점을 구하라.

---

$$
x+y+2z=1 \implies (x-1)+y+2z=0 \implies (1,\,1,\,2)\left[(x,\,y,\,z)-(1,\,0,\,0)\right]=0
$$

이므로 문제 5를 이용하여 $P$ 의 대칭점 $P'$ 을 구하면,
$$
P'=2 \left( \dfrac{-3}{6}\right)(1,\,1,\,2)+(1,\,1,\,1)=(-1+1,\,-1+1,\, -2+1)=(0,\,0,\,-1)
$$


<b>7. </b> 삼차원 좌표공간에서 두 평면
$$
2x+4y+z=5,\qquad x-3y+2z=0
$$
이 이루는 교각의 코사인 값을 구하라.

---

두 평면의 방햑벡터를 $\mathbf{n}_1=(2,\,4,\,1),\, \mathbf{n}_2=(1,\,-3,\,2)$ 라 하면,
$$
\cos(\mathbf{n}_1,\,\mathbf{n}_2)= \dfrac{\mathbf{n}_1 \cdot \mathbf{n}_2}{|\mathbf{n}_1||\mathbf{n}_2|}=-\dfrac{8}{7\sqrt{6}}
$$




<b>8. </b> (**입체사영**) 구면 $x^2+y^2+z^2=1$ 의 점 $(0,\,0,\,1)$ 과 $xy$-평면의 점 $(x,\,y,\,0)$ 을 지나는 직선이 구면과 만나는 새로운 점의 좌표를 구하라. 또 이를 이용하여 정수방정식 $a^2+b^2+c^2=d^2$ 의 풀이를 구하라. $p,\,q$ 가 정수이면 정수점 $(2pq,\,2p^2,\,q^2)$ 과 원점까지의 거리가 정수 $2p^2+q^2$ 임을 살펴보라. 또 원점까지의 거리가 정수인 정수점 $(a,\,b,\,c)$ 를 모두 구하라.

---

(1) $(0,\,0,\,1)$ 과 $(x,\,y,\,0)$ 을 지나는 직선은 $(xt,\, yt,\, -t+1)$ 로 표현 할 수 있다. 이 직선과 구면이 만나는 새로운 점의 좌표는,
$$
x^2t^2+y^2t^2+t^2-2t+1=1 \implies t=\dfrac{2}{x^2+y^2+1}\text{ or }t=0
$$
이다. $t=0$ 일 때는 $(0,\,0,\,1)$ 인 사소한 해 이다. 

(2) 정수방정식 $a^2+b^2+c^2=d^2$ 을 생각하자. $d=0 \iff a= b=c=0 $ 의 사소한 해를 제외하고 생각하기로 하자. $d\ne 0$ 이므로,
$$
\left(\dfrac{a}{d}\right)^2+\left(\dfrac{b}{d}\right)^2+\left(\dfrac{c}{d}\right)^2=1
$$
를 얻는다. (1) 로 부터 $x,\,y\in \mathbb{Q}$ 일 때 $(x,\,y,\,0)$ 과 $(0,\,0,\,1)$ 을 지나는 직선이  $x^2+y^2+z^2=1$ 과 만나는 점의 좌표는 유리수임을 알 수 있다. 역으로 $x,\,y,\,z\in \mathbb{Q}$ 이고 $x^2+y^2+z^2=1$ 이면 $(0,\,0,\,1)$ 과 $(x,\,y,\,z)$ 를 동시에 지나는 직선 $(xt,\,yt,\,zt+1)$ 이 $xy$-평면과 만나는 점의 좌표는 $(-x/z,\, -y/z,\,0)$ 이므로 좌표값이 유리수이다. 즉 $x^2+y^2+z^2=1$ 을 만족하는 $x,\,y,\,z$ 가 유리수 인 것은 $(0,\,0,\,1) $ 과 $(x,\,y,\,z)$ 를 잇는 직선이 $xy$--평면과 만나는 점의 $x,\,y$ 좌표가 모두 유리수인것의 필요충분조건이다.

따라서 임의의 유리수 $q_1\,q_2$ 에 대하여 
$$
\left(\dfrac{2q_1}{q_1^2+q_2^2+1},\, \dfrac{2q_2}{q_1^2+q_2^2+1},\, \dfrac{q_1^2+q_2^2-1}{q_1^2+q_2^2+1}\right)
$$
가 $x^2+y^2+z^2=1$ 상의 유리수이므로 $a^2+b^2+c^z=d^2$ 을 만족하는 정수방정식은 임의의 유리수 $q_1,\,q_2$ 에 대하여 $q_1^2+q_2^2+1,\,2q_1,\,2q_2$ 의 최소공배수의 임의의 배수를 $M$ 이라 할 때 $a=2Mq_1,\, b=2Mq_2,\,c=M(q_1^2+q_2^2-1),\, d=M(q_1^2+q_2^2+1)$ 이 정수방정식의 해이다. 또한 사소한 해 즉 임의의 정수 $d$ 에 대해 $a=d,\,b=c=0$, $b=d,\,a=c$, $c=d,\, a=b=0$ 또 해이다.

(3) $p,\,q$ 가 정수일 때 $(2pq,\,2p^2,\,q^2)$ 과 원점 까지의 거리는 $\sqrt{4p^2q^2+4p^4+q^4}=(2p^2+q^2)$ 

(4) 원점까지의 거리가 정수인 정수점은 (2) 에서 구하였다.



<b>10. </b> 삼차원 공간의 원점에서 $(1,\,2,\,3)$ 방향으로 발사된 빛이 평면 $x+y+z=1$ 에 위치한 거울에 반사되었을 때, 반사된 빛이 $xy$-평면과 만나는 점을 구하라.

---

삼차원공간의 원점에서 $(1,\,2,\,3)$ 방향으로 발사된 빛은 직선의 방정식 $(t,\,2t,\,3t)$ 로 기술되며 평면 $x+y+z=1$ 에 위치한 거울 만나는 점은
$$
t+2t+3t=1\implies t=\dfrac{1}{6} 
$$
로부터 $(1/6,\,1/3,\,1/2)$ 이다. 

원점에서 출발하여 거울에 반사된 빛이 원점에서 반사점까지의 거리만큼 반사되어 갔을 때의 위치를 $P=(x,\,y,\,z)$ 라 하면  원점과 $P$ 의 중점이 $(1/6,\,1/3,/,1/2)$ 를 지나며 평면의 방향벡터와 같은 $(1,\,1,\,1)$ 을 방향벡터로 갖는 직선 위에 있어야 한다. 즉,
$$
\dfrac{O+P}{2}=\left(\dfrac{x}{2},\, \dfrac{y}{2},\, \dfrac{z}{2}\right) = \left(t+\dfrac{1}{6},\, t+\dfrac{1}{3},\, t+\dfrac{1}{2}\right)
$$
 를 만족하는 $t\in \mathbb{R}$ 이 존재해야 한다. 또한 $\vec{OP}\cdot (1,\,1,\,1)=0$ 이어야 하므로, $(x+y+z)=0$  이어야 한다. 즉 $t=-\dfrac{1}{3}$ 이므로,
$$
P=\left(-\dfrac{1}{3},\, 0,\, \dfrac{1}{3}\right)
$$
이다. 즉 반사된 빛의 경로는, $\left(3s-\dfrac{1}{3},\, 2s,\, s+\dfrac{1}{3}\right)$ 을 따른다. $xy$-평면과 만나는 점은 $s=-\dfrac{1}{3}$ 일 때 이므로 
$$
\left(-\dfrac{4}{3},\, -\dfrac{3}{2},\,0 \right)
$$
이다.



<b>11. </b> 공간의 세 점 $P_0,\,P_1,\,P_2$ 가 동일 직선상에 있으면, 방정식
$$
\begin{align}
&t_0+t_1+t_2=0\,,\\
&(t_0,\,t_1,\,t_2)\ne (0,\,0,\,0)\,,\\
&t_0P_0+t_1P_1+t_2P_2=0\;.
\end{align}
$$
을 만족시키는 실수 $t_0,\,t_1,\,t_2$ 가 존재함을 보이라. 또 이 명제의 역이 성립함을 보이라.

---

세 점이 동일직선상에 있으면 $\vec{P_1P_0}$ 와 $\vec{P_2P_0}$ 가 평행해야 한다. 즉 $a(P_0-P_1)+b(P-0-P_2)=0 \implies (a+b)P_0-aP_1-bP_2=0$ 을 만족하는 실수 $0$ 이 아닌 실수 $a,\,b$ 가 존재히야 한다. $a+b=t_0,\, -a=t_1,\,-b=t_2$ 라 놓으면 $t_0+t_1+t_2=0$ 이므로 방정식 3개중 첫번째와 세번째를 만족하는 실수 $t_0,\,t_1,\,t_2$ 가 존재해야함과 동치이다. 또한 $a,\,b \ne 0 \iff (t_0,\,t_1,\,t_2)\ne (0,\,0,\,0)$ 이므로 두번째 방정식도 만족해야 한다.



<b>12. </b> 공간의 부분집합 $A$ 에 속하는 임의의 두 점 $P,\,Q$ 에 대하여 선분
$$
PQ:=\{(1-t)P+tQ \mid 0\le t\le 1 \}
$$
가 여전히 $A$ 에 속하면 $A$ 를 **볼록집합** (convex set) 이라고 부른다. 이제 공간 속의 임의의 점 $P_0,\,P_1,\ldots,\,P_k$ 에 대하여 집합
$$
K:=\{t_0P_0 + t_1P_1 + \cdots + t_k P_k : t_0,\ldots,\,t_k \ge 0,\, t_0+t_1+\cdot +t_k =1\}
$$
가 볼록집합임을 보이라. 또 $K$ 는 $P_0,\ldots,\,P_k$ 를 포함하는 최소의 볼록집합임을 보이라.

---

(1) $X,\,Y\in K$ 라 하면 $X=x_0P_0 + \cdots x_k P_k,\, Y=y_0P_0 + \cdots + y_k P_k$ 이며 $x_0,\ldots,\,x_k,\,y_0,\ldots,\,y_k \ge 0$ 이고 $x_0+\cdots + x_k = y_0 + \cdots + y_k=1$ 을 만족시키는 $x_0,\ldots,\,x_k,\,y_0,\ldots,\,y_k$ 가 존재한다.  $0\le t \le 1$ 에 대해
$$
\begin{align}
(1-t)X+tY &= \sum_{m=1}^k (1-t)x_mP_m+ty_mP_m = \sum_{m=1}^k (x_m-tx_m+ty_m))P_m

\end{align}
$$
이다. $t<1,\, x_m,\, y_m\ge 0$ 이므로 $(1-t)x_m-ty_m\ge 0$  이며, $\displaystyle \sum_{m=1}^k (x_m-tx_m +ty_m)=1-t+t=1$ 이므로,
$$
(1-t)X+tY\in K
$$
이다. 따라서 $K$ 는 볼록집합이다.

(2) $K_i:=\{t_0P_1 + \cdots + t_i P_i : t_0,\ldots,\,t_i \ge 0,\, t_0+\cdots + t_i=1 \}$ 에 대해 이것이 $P_0,\ldots,\,P_i$ 를 포함하는 최소한의 볼록집합임을 induction을 사용하여 증명하자.  $K_0 =\{P_0\}$  이며 $K_1=\{(1-t)P_0+tP_1: 0 \le t\le 1\}$ 임을 보이자. 볼록집합의 정의에 의해 $K_1$ 이 $P_0,\,P_1$ 을 포함하는 최소한의 볼록집합임은 자명하다. 

이제 $K_N$ 이 $P_0,\ldots,\,P_N$ 을 포함하는 최소한의 볼록집합임을 가정하면 $K_{N+1}$ 이 $P_0,\ldots,\,P_N,\, P_{N+1}$ 을 포함하는 최소한의 볼록집합임을 보이자. $Q_N\in K_N$ 이라 할 때 $0\le s \le 1$ 을 만족하는 $s$ 에 대해 $(1-s)Q_N + sP_{N+1} \in P_{N+1}$ 이어야 한다. $Q_N = x_0P_1 + \cdot + x_NP_N$ for some $x_0,\ldots,\,x_N \ge 0,\, x_0+\cdots + x_N=1$ 이므로
$$
(1-s)Q_N+sP_{N+1}=(1-s)x_0 P_1 + \cdots +(1-s)x_NP_1 + sP_{N+1}
$$
이다. $\displaystyle \sum_{j=1}^N (1-s)x_j + s=(1-s)\sum_{j=1}^N x_j + s=1$ 이므로 $(1-s)Q_N + sP_{N+1}\in P_{N+1}$ 이다. 따라서 $P_1,\ldots,\,P_{N+1}$ 을 포함하는 볼록집합은 $K_{N+1}$ 부분집합이다. 또한 $K_{N+1}$ 의 정의에 의해 $K_{N+1}$ 은 $P_1,\ldots,\,P_{N+1}$ 을 포함하는 볼록집합에 포함된다. 따라서 $K_N$ 이 $P_1,\ldots,\,P_N$ 을 포함하는 최소한의 볼록집합이면 $K_{N+1}$ 은 $P_1,\ldots,\,P_{N+1}$ 을 포함하는 최소한의 볼록집합이다. 따라서 증명 끝.



<b>13. </b> 볼록집합과 볼록집합의 교집합은 볼록집합임을 보이라.

---

$A,\,B$ 가 볼록집합이며 $P,\,Q\in A \cap B$ 라 하자. 임의의 $0\le t \le 1$ 에 대해 $tP+(1-t)Q \in A \cap B$ 임은 trivial 하므로 $A \cap B$ 는 볼록집합이다.



<b>14. </b> $n$ 공간 속의 공 
$$
\begin{align}
B^{n}(C,\,r) &:= \{X\in \mathbb{R}^n : |X-C|<r\}\\  
\overline{B}^n (C,\,r)&:= \{X \in \mathbb{R}^n : |X-C|\le r\}
\end{align}
$$
은 모두 볼록집합임을 보이라.

---

$X,\,Y \in B^n(C,\,r)$ 이라면 $|X-C|<r,\, |Y-C|<r$ 이다. 임의의 $0\le t \le 1$ 에 대해
$$
|tX+(1-t)Y-C|=|t(X-C)+(1-t)(Y-C)| \le t|X-C|+(1-t)|Y-C|< tr+(1-t)r=r
$$
이므로 $tX+(1-t)Y\in B^n(C,\,R)$ 이다. 따라서 $B^n(C,\,r)$ 은 볼록집합이다. 

$X,\,Y \in \overline{B}^n(C,\,r)$ 이라면 $|X-C|\le r,\, |Y-C|\le r$ 이다. 임의의 $0\le t \le 1$ 에 대해
$$
|tX+(1-t)Y-C|=|t(X-C)+(1-t)(Y-C)| \le t|X-C|+(1-t)|Y-C| \le tr+(1-t)r=r
$$
이므로 $tX+(1-t)Y\in \overline{B}^n(C,\,R)$ 이다. 따라서 $\overline{B}^n(C,\,r)$ 은 볼록집합이다. 



<b>15. </b> $n$-공간의 단위벡터 $\mathbf{n}$ 에 대하여 초평면 $\mathbf{n}\cdot X+c=0$ 과 점 $P_1,\ldots,P_k$ 사이의 거리의 제곱합은 $\displaystyle \sum_{i=1}^k (\mathbf{n}\cdot P_i +c)^2$ 으로 주어진다. 이 값이 최소로 되는 초평면을, 주어진 점 $P_1,\ldots,\,P_k$ 에서 가장 가까운 초평면이라고 부를 때, 주어진 점에서 가장 가까운 초평면은 그 점들의 중심을 지남을 보이라.

---

$c=-\mathbf{n}\cdot X$ 이므로, $
$$
\sum_{i=1}^k (\mathbf{n}\cdot P_i + c)^2=\sum_{i=1}^k (\mathbf{n} \cdot (P_i-X))^2 
$$

$$
\begin{align}
\sum_{i=1}^k \left(\mathbf{n} \cdot P_i + c\right)^2 &=\sum_{i=1}^k (\mathbf{n}\cdot P_i)^2 + 2c\left(\sum_{i=1}^k \mathbf{n}\cdot P_i\right) + kc^2 \\
&=k\left[c^2 + \dfrac{2}{k}\left(\sum_{i=1}^k \mathbf{n}\cdot P_i\right)c+\dfrac{1}{k^2}\left(\sum_{i=1}^k \mathbf{n}\cdot P_i\right) ^2\right]+\sum_{i=1}^k (\mathbf{n}\cdot P_i)^2-\dfrac{1}{k}\left(\sum_{i=1}^k \mathbf{n}\cdot P_i\right) ^2 \\
&=k\left[c+\dfrac{1}{k} \left(\sum_{i=1}^k \mathbf{n}\cdot P_i\right)\right]^2+\sum_{i=1}^k (\mathbf{n}\cdot P_i)^2-\dfrac{1}{k}\left(\sum_{i=1}^k \mathbf{n}\cdot P_i\right) ^2

\end{align}
$$

여기서 뒤의 두 term 은 상수 term 이므로 $\displaystyle c=-\dfrac{1}{k} \left(\sum_{i=1}^k \mathbf{n}\cdot P_i\right)$ 일 때 최소값을 가진다. 이 때,
$$
0=\mathbf{n}\cdot X +c = \mathbf{n}\cdot \left(X-\dfrac{1}{k}
\sum_{i=1}^k P_i\right)
$$
이므로 이 초평면은 $\displaystyle \dfrac{1}{k}\sum_{i=1}^k P_i$ 를 지나는데 이 점이 중심이다.



<b>16. </b> 어떤 보물섬의 지도에는 $n$ 개의 마을이 그려져 있고, 보물을 찾아 갈 수 있는 지시가 다음과 같이 쓰여 있다.

> 마을 $A_1$ 에서 출발하여 마을 $A_2$ 쪽으로 $\frac{1}{2}$ 만큼 간 다음, 마을 $A_3$ 쪽으로 $\frac{1}{3}$ 만큼 가고, 계속해서 마을 $A_4$ 쪽으로 $\frac{1}{4}$ 만큼 가고, ... , 마을 $A_n$ 쪽으로 $\frac{1}{n}$ 만큼 간 곳에 보물이 묻여 힜다.

그러나 지도에는 마을의 이름이 모두 지워져 있었다. 이 때 부물이 묻힌 곳을 알 수 있겠는가.

---

처음 시작점의 위치를 $P_1$, $k$ 번째 마을을 향하여 주어진 만큼 향하였을때의 위치를 $P_k$ 라 하자. 그렇다면, $P_1=A_1$ 이며 $k\ge 2$ 에 대해 
$$
P_k = P_{k-1}+\dfrac{1}k(A_k-P_{k-1})= \dfrac{k-1}{k}P_{k-1} + \dfrac{1}{k}A_k
$$
이므로,
$$
kP_k = (k-1)P_{k-1}+A_k
$$
이다. 양 변에 $\displaystyle \sum_{k=1}^n$ 을 씌워 계산하면,
$$
P_1 + 2P_2 + \cdots + nP_n = P_1 + \cdots (n-1)P_{n-1} + A_1 + \cdot + A_n
$$
이므로, $nP_n =A_1+\cdots +A_n$ 이다. 즉, 
$$
P_n = \dfrac{1}{n} \sum_{k=1}^n A_n
$$
이므로 $P_n$ 은 $n$ 개의 마을들의 중심이다.



<b>17. </b> 사각형의 각 변의 중점을 차례로 이어 얻은 사각형은 평행사변형임을 보이라.

---

사각형의 각 꼭지점을 $A,\,B,\,C,\,D$ 라 하면 각 변의 중점은 $X_1=(A+B)/2,\,X_2=(B+C)/2,\,X_3=(C+D)/2,\,X_4=(D+A)/2$ 이다. 이 때 $X_1-X_2=\dfrac{A-C}{2}=X_4-X_3$ 이므로 $X_1-X_2$ 가 이루는 변과 $X_4-X_3$ 가 이루는 변이 평행하며, $X_4-X_1=\dfrac{D-B}{2}=X_3-X_2$ 이므로 $X_4-X_1$ 과 $X_3-X_2$ 가 이루는 변이 평행하다. 따라서 이 사각형은 평행사변형이다.



<b>18. </b> trivial



<b>19. </b> trivial



<b>20. </b> 공간속의 점 $P_1,\ldots,\,P_k$ 에 대하여
$$
|P_1-Q|^2 + \cdots +|P_k-Q|^2
$$
 의 값을 최소로 하는 점 $Q$ 는 $P_1,\ldots,\,P_k$ 의 중심임을 보여라.

---

$$
\begin{align}
\sum_{i=1}^k|P_i-Q|^2&= \sum_{i=1}^k |P_i|^2-2\sum_{i=1}^k P_i \cdot Q + k|Q|^2 \\
&=k\left(|Q|^2-2\left(\dfrac{1}{k}\sum_{i=1}^k P_i\right) \cdot Q + \left( \dfrac{1}{k}\sum_{i} P_i  \right)^2 \right) +\sum_{k=1}^k |P_i|^2-\dfrac{1}{k}\left(\sum_{i=1}^k P_i\right)^2 \\
&= k \left(Q- \dfrac{1}{k} \sum_{i=1}^k P_i\right)^2+\sum_{k=1}^k |P_i|^2-\dfrac{1}{k}\left(\sum_{i=1}^k P_i\right)^2 

\end{align}
$$

이다. 마지막 두 terms 는 $\{P_i\}$ 에만 의존하는 상수 term 이므로 이 값을 최소하 하는 점 $Q$ 는
$$
Q=\dfrac{1}{k}\sum_{i=1}^k P_i
$$
이다. 즉 $P_1,\ldots,\,P_k$ 의 중심이다. 



<b>21. </b> 두 평면 $x+y+z=1$ 과 $x-y-z=5$ 의 교선의 식을 구하라.

---

두 식을 더하면 $2x=6\implies x=3$ 이다. 따라서 $y+z=-2$ 이다. 따라서 교선의 식은,
$$
x=3,\quad y=t,\quad z=-t-2
$$
이다.



<b>22. </b> 공간에서 점과 실수의 쌍 $(P,\,m)$ 을 질점이라고 부르기로 하자. 질점들의 집합
$$
A:=\{(P_1,\,m_1),\,(P_2,\,m_2),\ldots,\, (P_n,\,m_n)\}
$$
에 대하여 $m:=m_1+\cdots +m_n$ 을 $A$ 의 질량이라고 한다. 그리고 질량이 $0$ 이 아닌 질점들의 집합 $A$ 에 대하여 $A$ 의 질량중심을
$$
\operatorname{CM}(A):= \left(\dfrac{m_1}{m}P_1 + \dfrac{m_2}{m}P_2 + \cdots + \dfrac{m_n}m P_n\right)
$$
으로 정의한다. 서로 공통부분이 없는 두 질점들의 유한집합 $A,\,B$ 에 대하여,
$$
\operatorname{CM}(A \cup B)=\operatorname{CM}(\{\operatorname{CM}(A),\, \operatorname{CM}(B)\})
$$
임을 보이라. (편의상 $A,\,B$ 의 각 질량이 모두 양수라 가정한다.

---

$A:=\{(P_1^A,\,m_1^A) \ldots,\,(P_N^A,\,m_N^A)\}$, $B:=\{(P_1^B,\,m_1^B) \ldots,\,(P_M^B,\,m_M^B)\}$ 라 하자.  $m_A=m_1^A+ \cdots +m_N^A$, $m_B=m_1^B+\cdots + m_M^B$ 라 하자. 
$$
\begin{align}
\operatorname{CM}(\{\operatorname{CM}(A),\, \operatorname{CM}(B)\}) &= \dfrac{m_A}{m_A+m_B} \operatorname{CM}(A) + \dfrac{m_B}{m_A+m_B} \operatorname{CM}(B) \\
&=\dfrac{m_A}{m_A+m_B}\left(\dfrac{1}{m_A}\sum_{i=1}^N m_i^AP_i^A\right) + \dfrac{m_B}{m_A+m_B}\left(\dfrac{1}{m_B}\sum_{j=1}^M m_j^BP_j^B\right) \\
&=\dfrac{1}{m_A+m_B} \left(\sum_{i=1}^N m_i^AP_i^A+ \sum_{j=1}^M m_j^B P_j^B\right) = \operatorname{CM}(A \cup B)
\end{align}
$$


## 연습문제 : 제 5장 5 절



<b>1.</b> trivial



<b>2. </b> trivial



<b>3. </b> 세 벡터 $\mathbf{u},\,\mathbf{v},\,\mathbf{w}$ 가 일차독립일 때, 벡터
$$
\begin{align}
\mathbf{a}&= a_1 \mathbf{u}+a_2 \mathbf{v}+a_3\mathbf{w}\\
\mathbf{b} &= b_1 \mathbf{u}+b_2 \mathbf{v}+b_3\mathbf{w}\\
\mathbf{c} &= c_1 \mathbf{u}+c_2 \mathbf{v}+c_3\mathbf{w}\\
\end{align}
$$
가 일차독립일 필요충분조건은 벡터 $(a_1,\,a_2,\,a_3),\, (b_1,\,b_2,\,b_3),\, (c_1,\,c_2,\,c_3)$ 가 일차독립임을 보여라.

---

(1) $\mathbf{a},\,\mathbf{b},\,\mathbf{c}$ 가 일차독립이면 $d_1\mathbf{a}+d_2\mathbf{b}+d_3\mathbf{c}=0$ 을 만족시키는 $d_1,\,d_2,\,d_3$ 는 모두 $0$ 이다. 즉,
$$
(d_1a_1+d_2b_1+d_3c_1)\mathbf{u}+(d_1a_2+d_2b_2+d_3 c_2)\mathbf{v}+(d_1a_3+d_2b_3+d_3c_3)\mathbf{w}=0
$$
이면 $d_1=d_2=d_3=0$ 이다.  $\mathbf{u},\,\mathbf{v},\, \mathbf{w}$ 가 일차독립이므로, 
$$
d_1a_1+d_2b_1+d_3c_1=0\\
d_1a_2+d_2b_2+d_3 c_2=0\\
d_1a_3+d_2b_3+d_3c_3=0
$$
이어야 한다. 따라서 $d_1(a_1,\,a_2,\,a_3)+d_2(b_1,\,b_2,\,b_3)+d_3(c_1,\,c_2,\,c_3)=0$ 를 만족하는 $d_1,\,d_2,\,d_3$ 는 모두 $0$ 일 때이다. 따라서 벡터 $(a_1,\,a_2,\,a_3),\, (b_1,\,b_2,\,b_3),\, (c_1,\,c_2,\,c_3)$ 는 일차독립이다. 

(2) 벡터 $(a_1,\,a_2,\,a_3),\, (b_1,\,b_2,\,b_3),\, (c_1,\,c_2,\,c_3)$ 가 일차독립임을 가정하자. 그렇다면 $d_1(a_1,\,a_2,\,a_3)+d_2(b_1,\,b_2,\,b_3)+d_3(c_1,\,c_2,\,c_3)=0$ 를 만족하는 $d_1,\,d_2,\,d_3$ 는 모두 $0$ 일 때이다. 이는 $d_1 \mathbf{a}+d_2\mathbf{b}+d_3\mathbf{c}=0$ 을 만족하는 $d_1,\,d_2,\,d_3$ 는 모두 $0$ 이란 뜻이며, 따라서 $\mathbf{a},\,\mathbf{b},\,\mathbf{c}$ 는 모두 일차독립이다.



<b>4. </b> 벡터 $\mathbf{a}_1,\ldots,\,\mathbf{a}_k$ 가 일차독립이면, 모든 $i\in \{1,\ldots,\,k\}$ 에 대하여 $\mathbf{a}_i \ne 0$ 임을 보여라. 

---

$\mathbf{a}_1=0$ 이면 $\sum c_i \mathbf{a}_i=0$ 에 대해 $c_1\ne 0,\, c_2=\cdots c_k=0$ 이어도 성립하므로 $\mathbf{a}_1,\ldots,\,\mathbf{a}_k$ 는 일차독립이 아니다.



<b>5. </b> 자연수 $k$ 가 자연수 $l$ 보다 작을 때, $n$-벡터 $\mathbf{a}_1,\ldots,\mathbf{a}_l$ 이 일차독립이면 $\mathbf{a}_1,\ldots,\mathbf{a}_k$ 도 일차독립임을 보여라.

---

$\mathbf{a_1},\ldots,\,\mathbf{a}_k$ 가 일차독립이 아니면 $c_1 \mathbf{a}_1 + \cdots + c_k \mathbf{a}_k=0$ 을 만족하는 nontrivial $c_1,\ldots,\,c_k$ 가 존재한다. 그렇다면 $c_j=0$ for $j=k+1,\ldots,\,l$ 이라 놓으면 $c_1 \mathbf{a}_1 + \cdots +c_k\mathbf{a}_k + \cdots +c_l \mathbf{a}_l=0$ 을 만족하는 nontrivial $c_1,\ldots,\,c_l$ 이 존재하므로 $\mathbf{a}_1,\ldots,\,\mathbf{a}_l$ 은 일차독립이 아니다.



<b>6. </b> 벡터 $\mathbf{a}$ 가 벡터 $\mathbf{b}_1,\ldots,\,\mathbf{b}_k$ 의 일차결합이고, 벡터 $\mathbf{b}_i\,(i=1,\ldots,\,k)$ 가 각각 벡터 $\mathbf{c}_1,\ldots,\,\mathbf{c}_l$ 의 일차결합이면, 벡터 $\mathbf{a}$ 는 $\mathbf{c}_1,\ldots,\,\mathbf{c}_l$ 의 일차결합이 됨을 설명하라.

---

Let $\displaystyle \mathbf{a}=\sum_{i=1}^k \beta_i \mathbf{b}_i$ and $\displaystyle \mathbf{b}_i=\sum_{j=1}^l \gamma_{ji}\mathbf{c}_j$ 라 하자. 그렇다면 $\displaystyle \mathbf{a}=\sum_{i=1}^k \beta_i \left(\sum_{j=1}^l \gamma_{ji}\mathbf{c}_j\right)=\sum_{j=1}^l \left(\sum_{i=1}^k \beta_i \gamma_{ji}\right) \mathbf{c}_j$ 이므로 증명 끝.





## 연습문제 : 제 5장 6절



<b>1. </b> $n$ 공간의 단위벡터 $\mathbf{v}_1,\ldots,\,\mathbf{v}_n$ 이 서로 수직이면, 이들을 정규직교기져라고 부른다. 이제 임의의 $n$-벡터 $\mathbf{a}$ 와 정규직교기저 $\mathbf{v}_1,\ldots,\,\mathbf{v}_n$ 에 대하여,
$$
\mathbf{a}=(\mathbf{a}\cdot \mathbf{v}_1)\mathbf{v}_1 + \cdots +(\mathbf{a}\cdot \mathbf{v}_n)\mathbf{v}_n
$$
임을 보이라.

---

$\displaystyle \mathbf{a}=\sum_{k=1}^n a_k \mathbf{v}_k$ 이며 이 때 $a_k$ 는 유일하게 결정된다. $\displaystyle \mathbf{a}\cdot \mathbf{v}_i =\sum_{k=1}^n a_k (\mathbf{v}_k \cdot \mathbf{v}_i)=a_i$ 이다. 따라서 $\displaystyle \mathbf{a}=\sum_{k=1}(\mathbf{a}\cdot \mathbf{v}_k)\mathbf{v}_k$  이다.



<b>2. </b> 정육면체 격자의 각 정육면체의 중점들로 이루어진 집합을
$$
\operatorname{FC}:=\left\{\left(\dfrac{1}{2},\, \dfrac{1}{2},\, 0\right), \, \left(\dfrac{1}{2},\,0,\, \dfrac{1}{2}\right),\,\left(0,\,\dfrac{1}{2},\, \dfrac{1}{2}\right)\right\}+\mathbb{Z}^3
$$
라고 하자. 이제 **FCC 격자** 
$$
\mathbb{Z}^3 \cup \text{FC}
$$
에서,
$$
\mathbf{i}=(1,\,0,\,0) ,\quad \left(\dfrac{1}{2},\, \dfrac{1}{2},\,0\right),\quad \left(0,\,\dfrac{1}{2},\, \dfrac{1}{2}\right)
$$
가 기저임을 보여라.

---

$\mathbf{v}_1=\mathbf{i}=(1,\,0,\,0) ,\, \mathbf{v}_2= \left(\dfrac{1}{2},\, \dfrac{1}{2},\,0\right),\,\mathbf{v}_3=\left(0,\,\dfrac{1}{2},\, \dfrac{1}{2}\right)$ 라 하자. 
$$
c_1 \mathbf{v}_1+c_2\mathbf{v}_2+c_3\mathbf{v}_3=0 \implies \left(c_1+\dfrac{c_2}{2},\, \dfrac{c_2+c_3}{2},\, \dfrac{c_3}{2}\right) =0 \implies c_1=c_2=c_3=0
$$
이므로 $\mathbf{v}_1,\,\mathbf{v}_2,\,\mathbf{v}_3$ 는 일차독립이다.
$$
\begin{align}
\text{FC} =&\left\{\left(\dfrac{1}{2}+n_1,\, \dfrac{1}{2}+n_2,\, n_3 \right):n_1,\,n_2,\,n_3\in \mathbb{Z} \right\} \bigcup \left\{\left(\dfrac{1}{2}+n_1,\,n_2,\, \dfrac{1}{2}+n_3\right) : n_1,\,n_2,\,n_3\in \mathbb{Z} \right\} \\
&\bigcup \left\{\left(n_1,\,\dfrac{1}{2}+n_2,\, \dfrac{1}{2}+n_3\right):n_1,\,n_2,\,n_3\in \mathbb{Z} \right\}
\end{align}
$$
이다. 
$$
\begin{align}
\left(\dfrac{1}{2}+n_1,\, \dfrac{1}{2}+n_2,\, n_3 \right) & = (n_1-n_2+n_3)\mathbf{v}_1+(1+2n_2-2n_3)\mathbf{v}_2+2n_3 \mathbf{v}_3\\
\left(\dfrac{1}{2}+n_1,\,n_2,\, \dfrac{1}{2}+n_3\right) &= (1+n_1-n_2+n_3)\mathbf{v}_1+(-1+2n_2-2n_3)\mathbf{v}_2+(1+2n_3)\mathbf{v}_3 \\
\left(n_1,\,\dfrac{1}{2}+n_2,\, \dfrac{1}{2}+n_3\right) &=(n_1-n_2+n_3)\mathbf{v}_1+(2n_2-2n_3)\mathbf{v}_2+(1+2n_3)\mathbf{v}_3
\end{align}
$$
이므로 모든 $\text{FC}$ 의 벡터들을 표현 할 수 있다. 따라서 기저이다.



