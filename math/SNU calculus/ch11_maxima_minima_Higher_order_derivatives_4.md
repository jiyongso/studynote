XI. 최대최소값 문제와 고계미분 #4
===



## 제 6 절 : 라그랑즈 승수법



#### 정리 6.0.1 (라그랑즈 승수법)

$n$ 공간의 열린 집합 $U$ 에서 정의된 일급함수 $f,\,g$ 에 대하여 함수 $f$ 를 초곡면
$$
S:=\{X\in U: g(X)=c\}
$$
에 재한하였을 때, 점 $P\in S$ 가 극점이라고 하자. 그러면 $\nabla f(P)$ 와 $\nabla g(P)$ 는 일차종속이다. 즉
$$
\lambda_1 \nabla f(P)+\lambda_2 \nabla g(P)=\mathbf{0}
$$
이고 동시에 영이 아닌 실수 $\lambda_1,\,\lambda_2$ 가 존재한다. 특히, $\nabla g(P)\ne \mathbf{0}$ 이면, 식
$$
\nabla f(P)=\lambda \nabla g(P)
$$
를 만족시키는 실수 $\lambda$ 가 존재한다.

---

*(proof)* (1) $\nabla g(P)=\mathbf{0}$  이면 $\nabla f(P)$ 와 $\nabla g(P)$ 는 일차종속이므로 $\nabla g(P)\ne \mathbf{0}$ 일 때만 생각한다.

(2) $P\in S$ 에서 $\nabla f(P)$ 는 초곡면 $S$ 에 대해 수직임을 보이자. 점 $P$ 를 통과하는 $S$ 에서의 임의의 곡선 $X(t)$ 는 $X(0)=P$ 가 되도록 표현 할 수 있다. 이제 $X'(0)$ 는 $P$ 에서의 $S$ 의 접평면에 포함되는 벡터이다. 

(3) 문제의 가정에 의해 $f$ 가 $P$ 에서 극값을 가진다. $h(t) := f(X(t))$ 라 하면, $h'(0)=0$ 이므로, 
$$
h'(0)=X'(0)\cdot \nabla f(X(0)) = 0
$$
이다. 따라서 $\nabla f(P)$ 는 $X'(0)$ 에 수직이며, 따라서 $P$ 에서 $S$ 에 수직이다. 

(4) 또한 $\nabla g(P)$ 도 등위면에 수직이므로 $\nabla f(P)$ 와 $\nabla g(P)$ 는 평행하다. 따라서 원하는 결론을 얻는다. $\square$



#### 라그랑주 승수법의 응용 : 산술평균과 기하평균

$$
g(x_1,\ldots,\,g_n):=x_1+\cdots +x_n=1 ,\qquad x_1\ge 0,\ldots,\, x_n\ge 0
$$

을 만족시키는 점 $(x_1,\ldots,\,x_n)$ 으로 이루어진 영역에서 함수
$$
f(x_1,\ldots,\,x_n)=x_1\cdots x_n
$$
의 최대값을 구해보자.

---

우선 $0\le x_1,\ldots,\,x_n \le 1$ 임을 안다. 이 영역을 $K$ 라 하자. 주어진 영역은 유계인 닫힌집합이고 $f$ 는 연속함수이므로 $f$ 는 최대값을 가진다.  $P=(p_1,\ldots,\,p_n)\in K$ 에서 극값을 갖는다고 하자. 라그랑즈 승수법에 의해
$$
\begin{aligned}
\nabla f(P)&=(p_2\cdots p_n,\, p_1p_3 \cdots p_n,\cdots,\, p_1\cdots p_{n-1})\\
\nabla g(P) &= (1,\ldots,\, 1)
\end{aligned}
$$
로부터 $\nabla f(P)=\lambda\nabla g(P)$ 이므로, $p_1=\cdots =p_n=\frac{1}{n}$ 을 얻는다.  $Q_i $ 를 $x_i=1$, $x_1=\cdots =x _{i-1}=x_{i+1}=\cdots =x_n=0$ 인 point 라 했을 때 $f(Q_i)=0$ 이며 $f(P)>1$ 이므로 $f$ 는 $P$ 에서 최대값을 가지며 이 때의 최대값은 $\dfrac{1}{n^n}$ 이다.



이 식으로부터 모두 $0$ 이 아닌 임의의 양의 실수 $a_1,\ldots,\, a_n$ 에 대해 $S=\displaystyle\sum_{i=1}^n a_n$ 이라 하면 $0\le \dfrac{a_i}{S} \le 1$ 이므로,
$$
\dfrac{a_1}{S}  \cdots  \dfrac{a_n}{S} = \dfrac{a_1\cdots a_n }{S^n}\le \left(\dfrac{1}{n^n}\right) \implies a_1 \cdots a_n \le \left(\dfrac{S}{n}\right)^n  \implies (a_1\cdots a_n)^{1/n} \le \dfrac{a_1+\cdots +a_n}{n}
$$
을 얻으며 등호는 $a_1=\cdots =a_n$ 일 때만 성립한다.



#### 라그랑즈 승수법의 응용 : 산술평균과 이차평균

$$
g(x_1,\ldots,\,x_n):={x_1}^2+ \cdots + {x_n}^2 = 1,\qquad x_1\ge 0,\ldots,\,x_n \ge 0
$$

일 때 
$$
f(x_1,\ldots,\,x_n)=x_1+\cdots +x_n
$$
의 최대값을 구해보자.

---

역시 $0\le x_1 ,\ldots,\,x_n \le 1$ 이므로 유계인 닫힌 집합에서 정의되었으므로 연속함수 $f$ 는 최대값과 최소값을 가진다. 
$$
\begin{aligned}
\nabla f(x_1,\ldots,\,x_n) &= (1,\ldots,\,1) \\
\nabla g(x_1,\ldots,\, x_n) &= 2(x_1,\ldots,\,x_n)
\end{aligned}
$$
이므로 극값은 $x_1=\cdots =x_n= \dfrac{1}{\sqrt{n}}$ 뿐이며, 이 점을 $P$ 라 하면 $f(P)=\sqrt{n}$ 이다. $Q_i = \mathbf{e}_i$ 라 정의하면, $f(Q_i)=1 \le f(P)$ 이므로 $f(P)$ 는 $P$ 의 최대값이다. 

이제 임의의 $a_1,\ldots,\,a_n$ where $a_i \ge 0$ 에 대하여
$$
S:=({a_1}^2+\cdots +{a_n}^2)^{1/2}
$$
라 하면, $\left(\dfrac{a_1}{S}\right)^2 + \cdots +\left(\dfrac{a_n}{S}\right)^2 = 1$ 이며 $0 \le \dfrac{a_i}{S}\le 1$ 이므로,
$$
\dfrac{a_1}{S}+\cdots + \dfrac{a_n}{S}\le \sqrt{n}
$$
을 얻는다. 따라서, 절대부등식
$$
\dfrac{a_1+\cdots +a_n}{n} \le \left(\dfrac{{a_1}^2+\cdots + {a_n}^2}{n}\right)^{1/2}
$$
가 성립한다. 이 때 등호는 $a_1=\cdots =a_n$ 일 때 뿐이다. 





## 연습문제 : 제 11 장 6 절



<b>1. </b> 원판 $x^2+y^2\le 1$ 에서 정의된 함수 $f(x,\,y)=x^2+y^2-x-y+1$ 의 최대값과 최소값을 구하라.

---


$$
f(x,\,y)=\left(x-\dfrac{1}{2}\right)^2+\left( y-\dfrac{1}{2} \right)^2+\dfrac{1}{2} \ge \dfrac{1}{2}
$$
이므로 최소값은 $1/2$ 이다. 이제 경계 $g(x,\,y) =x^2+y^2=1$ 에서의 극값을 구해보자. 
$$
\begin{aligned}
\nabla f(x,\,y) &=  (2x-1,\, 2y-1)\\
\nabla g(x,\,y) &= (2x,\, 2y)
\end{aligned}
$$
이므로 라그랑즈 승수법을 사용하면 $x=y= \pm 1/\sqrt{2}$ 에 존재한다. 극값이 $2+\sqrt{2},\, 2-\sqrt{2}\approx 0.59$ 이므로 최대값은 $2+\sqrt{2}$ 최소값은 $1/2$ 이다. 



<b>2. </b> 반지름의 길이가 1 인 구면에 내접하는 원기둥 중에서 표면적을 최대로 하는 것의 표면적을 구하라. 원기둥은 바닥과 뚜껑이 없는 것으로 한다.

---

원기둥의 반경을 $r$, 높이를 $2h$ 라 하면 $r^2+h^2=1$ 이어야 하며 표면적은 $2\pi r (2h)=4\pi r h$ 이다. 또한 $0 \le r,\, h \le 1$ 을 만족해야 한다. $f(r,\,h)=4\pi rh$, $g(r,\,h)=r^2+h^2=1$ 에 대해 라그랑즈 승수법을 적용하면,
$$
\begin{aligned}
\nabla f (r,\,h)&= 4\pi (h,\, r)\\
\nabla g(r,\, h)&= (2r,\, 2h)
\end{aligned}
$$
이므로 $r=h=\frac{1}{\sqrt 2}$ 를 얻는다. 이 때 표면적 $f$ 의 극값은 $2\pi$ 이며 $(r,\,h)=(0,\,1)$ 이나 $(r,\,h)=(1,\,0)$ 에서 표면적이 $0$ 이므로 표면적의 최대값이 $2\pi$ 이다. 



<b>3. </b> 생략



<b>4. </b> (**케플러의 문제**) 대각선의 길이가 일정한 직원기둥중에서 부피가 최대인것을 구하라. 또 주어진 공(sphere) 속에 들어있는 직육면체 중에서 그 부피가 최대인 것을 구하라.

---

(1) 반지름 $r$, 높이 $h$ 인 직원기둥의 부피는 $V(r,\,h)=\pi r^2 h$  이며 대각선의 길이를 일정하게 놓으므로 대각선의 길이의 제곱함수  $g(r,\,h)= 4r^2+h^2=c$ 를 생각하자. 
$$
\begin{aligned}
\nabla V(r,\,h) &= \pi (2rh,\, r^2)\\
\nabla g(r,\,h) &= (8r,\, 2h)
\end{aligned}
$$
이 때의 극값은 $h=2r$ 일 때 이며 이 때의 부피는 $2\pi r^3$ 이다. 이 값이 최대값인 것은 $h$ 가 대각선의 길이와 같을 때 $r=0$ 이며 부피가 $0$ 이 되는 것으로 부터 알 수 있다.



(2) 반지름 $R$ 인 공의 직육면체의 각 변의 길이를 $2a,\,2b,\,2c$ 라 하면 직육면체의 부피 $V(a,\,b,\,c)=8abc$ 이며 공에 내접하므로 $g(a,\,b,\,c)=a^2+b^2+c^2=R^2$ 의 제한조건을 갖는다. 
$$
\begin{aligned}
\nabla V(a,\,b,\,c)&=(8bc,\, 8ac,\, 8ab)\\
\nabla g(a,\,b,\,c) &= (2a,\,2b,\,2c)
\end{aligned}
$$
이므로 $a=b=c=\dfrac{R}{\sqrt{3}}$ 에서 극값을 가진다. 이 때의 부피는 $\dfrac{8\sqrt{3}}{9}R^3$  이다. 이 값이 최대값인 것은 $a=R,\,b=c=0$ 일 때의 부피가 $0$ 인 것을 생각하면 된다. 



<b>5. </b> CBS 부등식을 라그랑즈 승수법을 이용하여 증명하라.

---

$n$ 벡터 $\mathbf{a}=(a_1,\cdots,\,a_n),\,\mathbf{b}=(b_1,\cdots\, b_n)$ 에 대해 $|\mathbf{a}\cdot \mathbf{b}|\le |\mathbf{a}||\mathbf{b}|$  를 보이자. 둘 중 하나가 영벡터이면 자명하므로, 둘 다 영벡터가 아님을 가정하자.  $\mathbf{x}=(x_1,\ldots,\,x_n) = \dfrac{\mathbf{a}}{|\mathbf{a}|},\, \mathbf{y}=(y_1,\ldots,\,y_n)=\dfrac{\mathbf{b}}{|\mathbf{b}|}$ 라 하면 $|\mathbf{x}|^2=|\mathbf{y}|^2=1$ 이다. 이제,
$$
\begin{aligned}
f(x_1,\ldots,\,x_n,\,y_1,\ldots,\,y_n) &= \mathbf{x} \cdot \mathbf{y} = x_1y_1 + \cdots +x_ny_n\\
g(x_1,\ldots,\,x_n,\,y_1,\ldots,\,y_n) &=|\mathbf{x}||\mathbf{y}| =1
\end{aligned}
$$
로 놓고 $f(x_1,\ldots,\,x_n,\,y_1,\ldots,\,y_n)$ 의 극값을 구해보자. 우리는 $-1\le x_i,\,y_i \le 1$ 임을 안다.  라그랑즈 승수법으로부터,
$$
\begin{aligned}
\nabla f(x_1,\ldots,\,x_n,\,y_1,\ldots,\,y_n) &= (y_1,\ldots,\,y_n,\,x_1,\ldots,\,x_n) \\
\nabla g(x_1,\ldots,\,x_n,\,y_n,\ldots,\,y_n) &= \left( \dfrac{|\mathbf{y}|}{|\mathbf{x}|}x_1,\ldots,\,\dfrac{|\mathbf{y}|}{|\mathbf{x}|} x_n,\, \dfrac{|\mathbf{x}|}{|\mathbf{y}|} y_1,\ldots,\,\dfrac{|\mathbf{x}|}{|\mathbf{y}|}y_n  \right) \\
&=(x_1,\ldots,\,x_n,\,y_1,\ldots,\,y_n)
\end{aligned}
$$
을 이용하면 $y_i = \lambda x_i ,\, x_j = \lambda y_j$ for $1\le i,\, j \le n$  임을 안다. $\lambda = \pm 1$ 이며 따라서 극값은 $\mathbf{x}=\pm \mathbf{y}$  에서 발생한다. 또한 $\mathbf{x}=\mathbf{y}$ 이면 $f=1$, $\mathbf{x}=-\mathbf{y}$ 이면 $f=-1$ 이다. 유계인 닫힌 영역에서의 연속함수이므로 최대값과 최소값이 존재하며, $\mathbf{x}=\mathbf{e}_1,\,\mathbf{y}=\mathbf{e}_2$  에 대해 $f=0$  이므로 $f$ 의 최대값은 $1$, 최소값은 $-1$ 이며 $|\mathbf{x}\cdot \mathbf{y}|\le 1$ 이므로 
$$
|\mathbf{a}\cdot \mathbf{b}|\le |\mathbf{a}| |\mathbf{b}|
$$
를 얻는다.



<b>6. </b> $0<p<q$ 이고 $a_1\ge 0,\ldots,\, a_n \ge 0$ 이면, 부등식
$$
\begin{align}
\left( {a_1}^q + \cdots + {a_n}^q\right)^{1/q} &\le \left({a_1}^p+ \cdots + {a_n}^p\right)^{1/p} \tag{1}\\
\left( \dfrac{ {a_1}^p + \cdots + {a_n}^p}{n}\right)^{1/p} &\le \left( \dfrac{ {a_1}^q + \cdots + {a_n}^q}{n}\right)^{1/q} \tag{2}

\end{align}
$$
이 성립함을 보이라.

---

$n=1$ 일 때는 자명하므로 $n\ge 2$ 일 경우만 생각한다. 

(2) $g(a_1,\ldots,\,a_n)={a_1}^p+\cdots + {a_n}^p=c^p$ 라 하고 이를 만족하는 영역에서 $f(a_1,\ldots,\,a_n)={a_1}^q+\cdots +{a_n}^q$ 의 극값을 구한다.
$$
\begin{aligned}
\nabla f(a_1,\ldots,\,a_n) &= q \left( a_1^{q-1},\ldots,\,a_n^{q-1} \right) \\
\nabla g(a_1,\ldots,\,a_n) &=p\left( a_1^{p-1},\ldots,\, a_n^{p-1} \right)
\end{aligned}
$$
이며 $\nabla f = \lambda \nabla g$ 이므로 극값은, $a_1=\cdots =a_n =\left( \dfrac{\lambda p}{q} \right)^{1/(q-p)}$ 	에 존재한다. 이 때 
$$
c^p = a_1^p + \cdots + a_n^p = n \left(\dfrac{\lambda p}{q}\right)^{p/(q-p)} \implies a_1=\cdots =a_n = \dfrac{c}{n^{1/p}}
$$
이며 이 때의  벡터를 $\mathbf{a}$ 라 할 때 $f(\mathbf{a})$ 값은
$$
f(\mathbf{a})=f\left(\dfrac{c}{n^{1/p}},\ldots,\, \dfrac{c}{n^{1/p}} \right)= n \dfrac{c^q}{n^{q/p}}=c^qn^{1-q/p}
$$
경계값을 보자. $n$ 개의 성분 중 $k$ 개의 성분이 $c/(k^p)$ 이고 나머지는 $0$ 이라면 이때의 벡터를 $\mathbf{d}_k$ 라 하면  $g(\mathbf{d}_k)=c^p$ , $f(\mathbf{d}_k)=c^q k^{1-q/p}$ 이다. 이 때 $k\le n$ 이므로
$$
\dfrac{f(\mathbf{a})}{f(\mathbf{d}_k)}=\dfrac{c^q n^{1-q/p}}{c^qk^{1-q/p}} < 1
$$
이다. 따라서 $f(\mathbf{a})$ 는 $f$ 의 최소값이며,
$$
\begin{aligned} 
&{a_1}^q+\cdots + {a_n}^q \ge n c^q n^{-q/p}  \\
\implies & \left(\dfrac{{a_1}^q+\cdots +{a_n}^q}{n}\right) \ge\left( \dfrac{\left({a_1}^p+\cdots {a_n}^p\right)^{1/p}}{n^{1/p}}\right)^q \\
\implies & \left(\dfrac{{a_1}^q+\cdots +{a_n}^q}{n}\right)^{1/q} \ge \left(\dfrac{{a_1}^p+\cdots +{a_n}^p}{n}\right)^{1/p}

\end{aligned}
$$
이다. 



(1) 번은 좀 더 생각해보고...





<b>7. </b> 포물면 $z=x^2+y^2$ 과 점 $(1,\,1,\,0)$ 사이의 최단거리를 구하라.

---

$$
\begin{aligned}
d(x,\,y,\,z) &=(x-1)^2+(y-1)^2+z^2 \\
g(x,\,y,\,z) &=x^2+y^2-z=0\\
\nabla d(x,\,y,\,z) &=2(x-1,\, y-1,\,z)\\
\nabla g(x,\,y,\,z) &= (2x,\, 2y,\, -1)
\end{aligned}
$$

$\nabla d = \lambda \nabla g$ 일 때 $x-1=\lambda x,\, y-1=\lambda y,\, z=-\lambda$ 이면 $\lambda = -1, (x,\,y,\,z )=(1/2,\, 1/2,\,1/2)$ 인 경우 극값을 가진다. 이 때의 거리는 $\sqrt{3}/2$이며 이 값이 최소값이다. 



<b>8. </b> 곡면 $z=xy$ 의 점 중에서 점 $(0,\,0,\,5)$ 에 가장 가까운 점을 모두 구하라.

---

$$
\begin{aligned}
d(x,\,y,\,z) &=x^2+y^2+(z-5)^2\\
g(x,\,y,\,z) &= xy-z = 0\\
\nabla d(x,\,y,\,z) &= (2x,\, 2y,\, 2z-10)\\
\nabla g(x,\,y,\,z) &= (y,\, x,\, -1)
\end{aligned}
$$

$\nabla d = \lambda \nabla g$ 이면 $x=\dfrac{\lambda}{2}y,\, y=\dfrac{\lambda}{2} x,\, z=-\dfrac{\lambda}{2} +5$ 이며 이를 만족시키는 $(x,\,y,\,z)=(0,\,0,\,0),\, (2,\,2,\,4)$ 이므로 최단거리는 $3$ 이다. 



<b>9. </b> 점 $(1,\,2,\,0)$ 에서 원뿔 $z^2=x^2+y^2$ 까지의 거리를 구하라.

---

$$
\begin{aligned}
d(x,\,y,\,z) &= (x-1)^2+(y-2)^2+z^2\\
g(x,\,y,\,z) &=x^2+y^2-z^2=0\\
\nabla d(x,\,y,\,z) &= (2x-2,\, 2y-4,\, 2z) \\
\nabla g(x,\,y,\,z) &= (2x,\,2y,\,-2z) 
\end{aligned}
$$

 $\nabla d=\lambda \nabla g$ 이면 $x-1=\lambda x,\, y-2=\lambda y,\, z=-\lambda z$ 이므로, $z =0$ 일 때 $(0,\,0,\, 0)$, $\lambda  =-1$ 일 때 $(1/2,\, 1,\, \pm \sqrt{5}/2)$ 이며 거리는 각각 $\sqrt{5},\, \dfrac{\sqrt{10}}{2}$ 이므로 최단거리는  $\dfrac{\sqrt{10}}{2}$ 이다. 



... 아 지겨우니 생략...





<b>14. </b> $n$ 차 대칭행렬 $Q=(q_{ij})$ 와 $X=\begin{pmatrix} x_1 \\ \vdots \\ x_n\end{pmatrix}$ 에 대하여, 이차형식은
$$
q(X)= X \cdot QX = \sum_{i,\,j=1}^n q_{ij}x_i x_j = \sum_{i=1}^n q_{ii}x_i^2 + 2\sum_{i<j} q_{ij}x_i x_j
$$
로 주어진다. 이때 $q$ 의 기울기 벡터는 $\nabla q(X)=2QX$ 임을 보이라. 또 $q$ 를 단위 구면 $S: x_1^2+\cdots + x_n^2=1$ 에서 제한하였을 때, 최대점에서는 $QX=\lambda X$ 를 만족시키는 실수 $\lambda$ 가 존재함을 보이라. 

---

$$
\part_i q(X) = 2q_{ii}x_i + 2\sum_{j \ne i} q_{ij}x_j=2\sum_{j=1}^n q_{ij}x_j = 2(QX)_{i}
$$

이므로 $\nabla q(X)=2QX$ 이다. $g(X)=|X|^2-1=0$ 일 때,
$$
\begin{aligned}
\nabla q(X) &= 2QX \\
\nabla g(X) &= 2(x_1,\ldots,\,x_n) =2X
\end{aligned}
$$
이므로 $QX=\lambda X$ 인 극점 $X$ 가 존재하므로 최대점에서는  $QX=\lambda X$ 를 만족시키는 실수 $\lambda$ 가 존재한다. 



<b>15.</b> 영 이상의 실수 $x,\,y,\,z$ 가  $x+y+z=1$ 을 만족 시킬 때 $xy+yz+zx-2xyz$ 의 최대값과 최소값을 구하라.

---

$$
\begin{aligned}
f(x,\,y,\,z)  &= xy+yz+zx-2xyz\\
g(x,\,y,\, z) &= x+y+z-1 \\
\nabla f(x,\,y,\,z )&= (y+z-2yz,\, x+z-2xz,\, x+y-2xy) \\
\nabla g(x,\,y,\,z) &= (1,\,1,\,1)
\end{aligned}
$$

이므로 $(x-y)(1-2z)=(y-z)(1-2x)=(z-x)(1-2y)=0$ 에서 극값이 존재한다. 

1) $x=y=z=\dfrac{1}{3}$ 이면  $f\left(\dfrac{1}{3},\, \dfrac{1}{3},\, \dfrac{1}{3}\right)= \dfrac{7}{27}$
2) $x=y=\dfrac{1}{2},\, z=0$, 혹은 $x=0,\, y=z=\dfrac{1}{2}$, 또는 $y=0,\, x=z=\dfrac{1}{2}$ 인 경우, $f(x,\,y,\,z)=\dfrac{1}{4}$
3) 경계값에서, $x=1,\,y=z=0$ 혹은 $y=1,\, x=z=1$ 혹은 $z=1,\, x=y=0$ 인 경우 $f(x,\,y,\,z)=0$

따라서 최대값은 $7/27$, 최소값은 $0$ 이다. 



<b>16. </b> 조건 
$$
g(x,\,y,\,z) :=x+y-2 \ge 0,\qquad h(x,\,y,\,z):= z^2-1\ge 0
$$
아래에서 함수 

$$
f(x,\,y,\,z) = x^4+2y^2+4z^4-2z^2
$$
 의 최소값을 구하여라.

---

$f_1 (x,\,y,\,z)=x^4+2y^2,\, f_2=4z^4-2z^2$ 이라 하면 $f=f_1+f_2$ 이며 $g$ 와 $f_1$ 은 $x,\,y$ 의 함수 $h$ 와 $f_2$ 는 $z$ 의 함수이므로 $f_1,\,f_2$ 각각의 최소값을 구하면 그 합이 $f$ 의 최소값이다.
$$
\begin{aligned}
\nabla f_1&= (4x^3,\, 4y)\\
\nabla g &= (1,\,1) \\
f_2' &= 16z^3-4z\\
h' &= 2z

\end{aligned}
$$
$\nabla f_1 = \lambda g$ 라 하면, $x^3=y$ 일 때 극값을 가진다. $x+y-2 = x^3+x-2\ge 0 \implies x\ge 1$ 이며 $f_1(x,\,x^3)=x^4+2x^6$ 이므로 $f_1$ 의 극값은 $3$ 보다 크다. 경계값인 $x+y=2$ 일 때 
$$
f_1(x,\, 2-x)= x^4+2(2-x)^2=x^4+2x^2-8x+8
$$
이며 극값은 $x=1$  일 때 $3$ 이며 최소값이다. 따라서 $f_1$ 의 최소값은 $3$ 이다.



$f_2 (z) = 4z^4-2z^2=4\left( z^2- \dfrac{1}{4}\right)^2-\dfrac{1}{4}$ 이며 $z^2\ge 1$ 일 때의 최소값은 $z^2=1$ 일 때이므로 최소값은 $2$ 이다. 따라서 $f$ 의 최소값은 $5$ 이다.



<b>17. </b> 좌표평면의 원점에서의 곡선 $x^6+y^6=1$ 의 한 점에 이르는 거리의 최대값과 최소값을 구하라.

---

 $d(x,\,y)=x^2+y^2$ , $g(x,\,y)=x^6+y^6-1=0$ 이라 하면,
$$
\begin{aligned}
\nabla d &= (2x,\, 2y)\\
\nabla g &= (6x^5,\, 6y^5)
\end{aligned}
$$
이므로  $\nabla d = \lambda \nabla g$ 로 부터 $x(3\lambda x^3-1)=0,\, y(3\lambda y^3-1)=0$ 를 얻는다. 우선 $x=0,\, y=1$  혹은 $x=1,\, y=0$ 일 때   거리는 $1$ 다. $x=y= \dfrac{1}{3\lambda}$ 로 놓으면,  $x=y=\dfrac{1}{\sqrt[6]{2}}$ 일 때 거리는 $2^{1/3}>1$  이므로 최소값은 $1$ 최대값은 $2^{1/3}$ 이다. 



## 제 11장 탐구문제 



<b>1. </b> $n$-공간에서 주어진 벡터 $\mathbf{v}$ 와 무한급 미분가능함수 $f,\,g$ 에 대하여,
$$
{D_{\mathbf{v}}}^k (fg)=\sum_{a+b=k} \begin{pmatrix} k \\ a\end{pmatrix} \left({D_{\mathbf{v}}}^a f \right) \left({D_{\mathbf{v}}}^b g \right)\, \qquad k=0,\,1,\,2,\ldots
$$
임을 보이라.

----

수학적 귀납법을 통해 보인다. $k=0,\,1$ 일 때는 자명하다. $k$ 일 때 성립함을 가정하면, (아래에서는 $\mathbf{v}$ 를 $v$ 로 쓰겠다. )
$$
\begin{aligned} 
{D_v}^{k+1} (fg) &= D_v \left( {D_{v}}^{k} (fg) \right )\\
&= \sum_{a=0}^k \dfrac{k!}{a!(k-a)!} \left[\left({D_v}^{a+1} f \right) \left({D_v}^{k-a} g\right)  + \left({D_v}^{a} f \right) \left({D_v}^{k-a+1} g\right)  \right] \\
&= \sum_{a=0}^k \dfrac{k!}{(a+1)!(k-a)!}(a+1) \left({D_v}^{a+1} f \right) \left({D_v}^{k-a} g\right)  \\
&\qquad + \sum_{a=0}^k \dfrac{k!}{a!(k-a+1)!}(k-a+1)\left({D_v}^{a} f \right) \left({D_v}^{k-a+1} g\right)   \\
&= \sum_{a'=1}^{k+1}  \dfrac{k!a'}{a'!(k-a'+1)! } \left({D_{v}}^{a'} f \right) \left({D_v}^{k-a+1} g\right)  + \sum_{a=0}^{k} \dfrac{k!(k-a+1)}{a! (k-a+1)!} \left({D_v}^{a} f \right) \left({D_v}^{k-a+1} g\right)   \\
&= \sum_{a=0}^{k+1} \dfrac{(k+1)!}{a!(k-a+1)!}  \left({D_{v}}^{a} f \right) \left({D_v}^{k-a+1} g\right)  \\
&= \sum_{a+b=k+1} \begin{pmatrix}k+1 \\ a\end{pmatrix} \left({D_{v}}^{a} f \right) \left({D_v}^{b} g\right) 


\end{aligned}
$$


<b>2. </b> (**라플라스 작용소**) 구면좌표계에서
$$
\nabla^2 f = \dfrac{1}{\rho^2}  \dfrac{\partial}{\partial \rho} \left(\rho^2 \dfrac{\partial f}{\partial \rho}\right) + \dfrac{1}{\rho^2 \sin \varphi} \dfrac{\partial }{\partial \varphi} \left(\sin \varphi \dfrac{\partial f}{\partial \varphi}\right) + \dfrac{1}{\rho^2 \sin^2 \varphi} \dfrac{\partial^2 f}{\partial\theta^2}
$$
임을 보이라.

---

탐구문제 10장 10번을 이용한다. 
$$
\begin{aligned}
\partial_x &= \sin \varphi \cos \theta \,\partial_{\rho} + \dfrac{\cos \varphi \cos \theta }{\rho} \partial_{\varphi} - \dfrac{\sin \theta}{\rho \sin \varphi} \partial_\theta \\
\partial_y &= \sin \varphi \sin \theta \,\partial_{\rho} + \dfrac{\cos \varphi \sin \theta }{\rho} \partial_{\varphi} + \dfrac{\sin \theta}{\rho \cos \varphi} \partial_\theta \\
\partial_z &= \cos \varphi \, \partial_{\rho} -\dfrac{\sin \varphi}{\rho} \partial_{\varphi}

\end{aligned}
$$
이므로,
$$
\begin{aligned}
\partial_x^2 &= \sin \varphi \cos \theta \left( \sin \varphi \cos \theta \, \partial_{\rho}^2  - \dfrac{\cos \varphi \cos \theta}{\rho^2} \partial_{\varphi}  + \dfrac{\cos \varphi \cos \theta}{\rho} \partial_\varphi \partial_{\rho}  + \dfrac{\sin \theta}{\rho^2 \sin \varphi} \partial_\theta - \dfrac{\sin \theta}{\rho \sin \varphi  } \partial_{\rho}\partial_{\theta} \right) \\
&\quad+ \dfrac{\cos \varphi \cos \theta}{\rho} \left(\cos \varphi \cos \theta \,\partial_{\rho} + \sin \varphi \cos \theta \partial_{\rho}\partial_\varphi  - \dfrac{\sin \varphi \cos \theta}{\rho}\partial_{\varphi} + \dfrac{\cos \varphi \cos \theta}{\rho} \partial_\varphi^2  \right. \\
&\qquad + \left. \dfrac{\sin \theta \cos \varphi}{\rho \sin^2\varphi} \partial_{\theta} - \dfrac{\sin \theta}{\rho \sin \varphi} \partial_\theta \partial_\varphi \right)
 \\
 &\quad - \dfrac{\sin \theta}{\rho \sin \varphi } \left( - \sin \varphi \sin \theta \, \partial_{\rho} + \sin \varphi \cos \theta \partial_{\rho}\partial_{\theta}- \dfrac{\cos \varphi \sin \theta}{\rho}\, \partial_\varphi + \dfrac{\cos \varphi \cos \theta}{\rho} \partial_{\varphi}\partial_{\theta}  \right. \\
 &\qquad \left. - \dfrac{\cos \theta}{\rho \sin \varphi} \partial_{\theta} - \dfrac{\sin \theta}{\rho \sin \varphi} \partial_{\theta}^2\right) \\
 &= \sin ^2 \varphi \cos ^2 \theta \partial_{\rho}^2 + \dfrac{\cos \varphi ^2 \cos ^2\theta}{\rho^2} \partial_{\varphi}^2 + \dfrac{\sin^2 \theta}{\rho^2 \sin^2 \varphi} \partial_\theta^2 + \left(\dfrac{\cos^2 \varphi \cos^2 \theta}{\rho}+ \dfrac{\sin^2\theta}{\rho}\right)\partial_{\rho} \\
 &\quad + \left(-2\dfrac{\cos \varphi \sin \varphi \cos^2 \theta}{\rho^2} + \dfrac{\cos \varphi  \sin ^2 \theta}{\rho^2 \sin \varphi }\right) \partial_{\varphi } \\
 &\quad + \left( \dfrac{\cos \theta  \sin \theta}{\rho^2} + \dfrac{\cos^2 \varphi \sin \theta\cos \theta}{\rho^2 \sin^2\varphi} + \dfrac{\cos \theta \sin \theta}{\rho^2 \sin^2\varphi}\right) \partial_{\theta} \\
 &\quad + 2\dfrac{\cos \varphi \sin \varphi \cos^2\theta}{\rho}\partial_{\rho}\partial_{\varphi} - 2 \dfrac{\cos \theta \sin \theta}{\rho} \partial_\rho \partial_\theta -2 \dfrac{\cos \varphi \cos \theta \sin \theta}{\rho^2 \sin \varphi} \partial_\varphi \partial_\theta \\

\end{aligned}
$$

$$
\begin{aligned}
{\partial_y}^2 &= \sin \varphi \sin \theta \left(\sin \varphi \sin \theta \,\partial_{\rho}^2 - \dfrac{\cos \varphi \cos \theta}{\rho^2} \partial_{\varphi} + \dfrac{\cos \varphi \sin \theta}{\rho} \partial_\rho \partial _\varphi - \dfrac{\cos \theta }{\rho^2 \sin \varphi} \partial_\theta + \dfrac{\cos \theta}{\rho \sin \varphi} \partial_{\rho} \partial_{\theta}\right) \\
&\quad + \dfrac{\cos \varphi \sin \theta}{\rho} \left( \cos \varphi \sin \theta \, \partial_{\rho}  + \sin \varphi \sin \theta \, \partial_{\rho} \partial_\varphi- \dfrac{\sin \varphi \sin \theta}{\rho} \partial_{\varphi} + \dfrac{\cos \varphi \sin \theta}{\rho} {\partial_{\varphi}}^2 \right.  \\
&\qquad \left. - \dfrac{\cos \varphi \cos \theta}{\rho \sin^2\varphi }\partial_{\theta} + \dfrac{\cos \theta}{\rho \sin \varphi} \partial_\varphi \partial_\theta\right) \\
&\quad + \dfrac{\cos \theta}{\rho \sin \varphi} \left( \sin \varphi \cos \theta \,\partial_{\rho} + \sin \varphi \sin \theta \, \partial_\rho \partial_\theta + \dfrac{\cos \varphi \cos \theta}{\rho} \partial_{\varphi} + \dfrac{\cos \theta \sin \theta}{\rho} \partial_{\varphi}\partial_{\theta}  \right. \\
&\qquad \left. - \dfrac{\sin \theta}{\rho \sin \varphi} \partial_{\theta} + \dfrac{\cos \theta}{\rho \sin \varphi} {\partial_{\theta}}^2 \right) \\
&= \sin^2\varphi \sin^2 \theta \, {\partial_\rho}^2 + \dfrac{\cos^2\varphi \sin^2 \theta}{\rho}{\partial_{\varphi}}^2 + + \dfrac{\cos^2 \theta}{\rho^2 \sin^2\varphi} {\partial_{\theta}}^2 + \left(\dfrac{\cos^2 \varphi \sin^2\theta }{\rho} + \dfrac{\cos^2\theta}{\rho}\right) \partial_{\rho} \\
&\quad + \left(-2\dfrac{\sin \varphi \cos \varphi \sin^2 \theta}{\rho^2} + \dfrac{\cos \varphi \cos^2\theta}{\rho^2 \sin \varphi}\right) \partial_{\varphi} \\
&\quad + \left(-\dfrac{\cos \theta \sin \theta}{\rho^2} - \dfrac{\cos^2\varphi \sin \theta \cos \theta}{\rho^2 \sin^2\varphi} - \dfrac{\cos \theta \sin \theta}{\rho^2 \sin^2\varphi }\right)\partial_{\theta} \\
&\quad + 2 \dfrac{\cos \varphi \sin \varphi \sin^2 \theta}{\rho} \partial_{\rho}\partial_{\varphi} + 2 \dfrac{\cos \theta \sin \theta}{\rho}\partial_{\rho}\partial_\theta + 2\dfrac{\cos \varphi \cos \theta \sin \theta}{\rho^2 \sin \varphi } \partial_{\varphi}\partial_\theta
\end{aligned}
$$

$$
\begin {aligned}
{\partial_z}^2 &= \cos \varphi \left(\cos \varphi \, {\partial_\rho}^2 + \dfrac{\sin \varphi}{\rho^2} \partial_{\varphi}-\dfrac{\sin\varphi}{\rho} \partial_\rho \partial_\varphi \right) - \dfrac{\sin \varphi}{\rho}\left(-\sin \varphi \, \partial_\rho + \cos \varphi \, \partial_{\rho}\partial_\varphi -\dfrac{\cos \varphi}{\rho}\partial_{\varphi}-\dfrac{\sin \varphi}{\rho}{\partial_\varphi}^2\right) \\
&= \cos^2\varphi \, {\partial_{\rho}}^2 +\dfrac{\sin^2\varphi}{\rho^2}{\partial_{\varphi}}^2 + \dfrac{\sin^2\varphi}{\rho}\partial_\rho + 2\dfrac{\cos \varphi \sin \varphi}{\rho^2}\partial_{\varphi } -2\dfrac{\cos \varphi \sin \varphi }{\rho}\partial_\rho \partial_{\varphi }
\end{aligned}
$$

이므로,
$$
\begin{aligned}
\nabla^2  &= \left(\sin^2\varphi \cos^2 \theta + \sin^2 \varphi \sin ^2\theta +\cos^2\varphi \right){\partial_{\rho}}^2  + \left( \dfrac{\cos^2\varphi \cos^2\theta + \cos^2\varphi \sin^2\theta + \sin^2\varphi}{\rho^2}\right) {\partial_{\varphi}}^2 \\
&\quad + \left(\dfrac{\sin^2\theta +\cos^2\theta}{\rho^2\sin^2\varphi } \right) {\partial_{\theta}}^2 + \left(\dfrac{\cos^2\varphi \cos^2\theta + \cos^2\varphi \sin^2\theta + \sin^2\varphi+1}{\rho}\right) \partial_\rho \\
&\quad + \left(-2\dfrac{\cos \varphi \sin \varphi}{\rho^2} + \dfrac{\cos \varphi}{\rho^2 \sin \varphi } + 2\dfrac{\cos \varphi \sin \varphi}{\rho^2} \right)\partial_{\varphi} +  0\cdot \partial_{\theta} + 0 \cdot \partial_\rho \partial_\varphi  + 0 \cdot \partial_\rho \partial_\theta + 0 \cdot \partial_\varphi \partial_\theta\\
&= {\partial_\rho}^2+ \dfrac{1}{\rho^2}{\partial_\varphi}^2 + \dfrac{1}{\rho^2 \sin^2\varphi }{\partial_\theta}^2 + \dfrac{2}{\rho}\partial_\rho + \dfrac{\cos \varphi}{\rho^2 \sin\varphi}\partial_{\varphi }
\end{aligned}
$$
문제에 주어진 식을 전개하면,
$$
\begin{aligned}
\nabla^2 &= \dfrac{1}{\rho^2}\partial_\rho\left( \rho^2 \partial_\rho\right) + \dfrac{1}{\rho^2 \sin \varphi } \partial_\varphi \left(\sin \varphi \,  \partial_\varphi \right) + \dfrac{1}{\rho^2 \sin^2 \varphi} {\partial_\theta}^2 \\
&= {\partial_\rho}^2 + \dfrac{2}{\rho}\partial_\rho +  \dfrac{1}{\rho^2} {\partial_{\varphi}}^2+\dfrac{\cos \varphi }{\rho^2 \sin \varphi }\, \partial_{\varphi } + \dfrac{1}{\rho^2\sin^2\varphi }{\partial_\theta}^2
\end{aligned}
$$
로 두 식이 같다. 



<b>3. </b> 다음 연립 방정식이 해를 가지는 지 판정하라. 
$$
x^3+2xy-3ye^{\sin x} \cos x = -7,\qquad y^5+x^2-3e^{\sin x}=5
$$

---

함수를 다음과 같이 놓자.
$$
\begin{aligned}
f(x,\,y) &= x^3+2xy-3ye^{\sin x} \cos x +7=0\\
g(x,\,y) &= y^5+x^2-3e^{\sin x}-5=0 \\
\nabla f(x,\,y) &= (3x^2+2y-3y \cos^2 x e^{\sin x}+3ye^{\sin x}\sin x,\,  2x-3\cos x e^{\sin x }) \\
\nabla g(x,\,y) &= (2x-3\cos x e^{\sin x},\, 5y^4)
\end{aligned}
$$
우리는 $\partial_y f = \partial_x g$ 임을 안다. 어떤 함수 $h(x,\,y)$ 에 대해 $f=\partial_x h,\, g=\partial_y h$ 로 잡을 수 있을까? 
$$
h(x,\,y)= \dfrac{1}{4}x^4+\dfrac{1}{6}y^6+x^2y-3ye^{\sin x}+7x-5y
$$
라 하면 $\partial_x h=f,\, \partial_y h=g$ 가 성립하며 $h$ 는 무한급 함수이다. 또한 $1/e \le  e^{\sin x} \le e$ 를 생각하면, $r=\sqrt{x^2+y^2} \to \pm \infty$ 에서 $h\to \infty$ 이므로 $h$ 는 최소값이 존재하며 이 때 $\partial_x h =f = 0,\, \partial_y h = g = 0$ 이므로, 주어진 연립방정식의 해가 존재한다. 





<b>4. </b> ($\textbf{H\"older}$ 부등식 ) 양수 $p,\,q$ 가 $\dfrac{1}{p}+\dfrac{1}{q}=1$ 을 만족시킬 때, 벡터
$$
a=(a_1,\ldots,\,a_n),\quad b=(b_1,\ldots,\,b_n)
$$
 에 대하여 부등식
$$
|a\cdot b| \le (|a_1|^p + \cdots + |a_n|^p)^{1/p}(|b_1|^q  + \cdots + |b_n|^q)^{1/q}
$$
을 증명하라. 

---

양수 $p,\,q$ 가 $\dfrac{1}{p}+\dfrac{1}{q}=1$ 을 만족시키므로, $p>1,\, q>1$ 이다. 영벡터에 대해서는 자명하므로 영벡터가 아닌 벡터에 대해서만 생각하자.  $n$-벡터 $x=(x_1,\ldots,\,x_n),\,y=(y_1,\ldots,\,y_n)$ where $x_i\ge 0,\, y_i\ge 0$ 가 다음을 만족한다고 하자.
$$
x_1^p + \cdots + x_n^p=y_1^q+ \cdots +y_n^q=1
$$
함수 $f(x,\,y),\, g_1(x,\,y),\, g_2(x,\,y)$ 를 다음과 같이 정의하자. 
$$
\begin{aligned}
f(x,\,y) &= x\cdot y = \sum_{i=1}^n x_i y_i \\
g_1(x,\, y)&= x_1^p + \cdots + x_n^p-1 \\
g_2(x,\,y) &= y_1^q + \cdots + y_n^q-1
\end{aligned}
$$
라그랑즈 승수법에 의해 극값에서는 어떤 실수 $\lambda,\, \mu$ 에 대해  $\nabla f = \lambda \nabla g_1,\, \nabla f=\mu \nabla g_2$ 가 성립해야 한다. 
$$
\begin{aligned}
\nabla f &= (y_1,\ldots,\, y_n,\, x_1,\ldots,\,x_n) \\
\nabla g_1 &= p(x_1^{p-1},\ldots,\,x_n^{p-1},\,0,\ldots,\, 0) \\
\nabla g_2 &= q(0,\ldots,\, 0,\, y_1^{q-1},\ldots,\, y_n^{q-1})
\end{aligned}
$$
이므로 $x_i=\mu q y_i^{q-1},\, y_i = \lambda p x_i^{p-1}$ 이다. $1/p+1/q=1 \implies pq-p-q=0$ 임을 생각하면,
$$
\begin{aligned}
x_i &= \mu q \lambda^{q-1}p^{q-1}x_i^{(p-1)(q-1)}=\mu \lambda^{q-1}qp^{q-1} x_i \\
y_i &= \lambda p \mu^{p-1}q^{p-1} y_i ^{(p-1)(q-1)} = \lambda \mu ^{p-1}pq^{p-1}y_i
\end{aligned}
$$
그렇다면 
$$
\mu \lambda^{q-1} qp^{q-1}=\lambda \mu^{p-1}pq^{p-1}=1 \tag{1}
$$

이어야 한다. 이때의 극값은
$$
\begin{aligned}
f(x,\,y)=\sum_{i=1}^n x_i y_i&=\lambda p \sum_{i=1}^n x_i^p =\lambda p\\
& =\mu q\sum_{i=1}^n y_i^q = \mu q

\end{aligned}
$$
이므로 (1) 로부터 $\lambda p = \mu q=1$ 이므로 $f(x,\,y)=1$ 은 극값이다. $x=\mathbf{e}_1,\, y=\mathbf{e}_2$ 라 하면 $x \cdot y = 0$ 이며 $g_1,\,g_2$ 를 만족하므로  $f(x,\,y)$ 의 최대값은 $1$ 이다. 즉  $f(x,\,y)\le 1$ 이다. 이제 $x_i = \dfrac{|a_i|}{(\sum |a_i|^p)^{1/p}},\, y_i =\dfrac{|b_i|}{\sum (|b_i| ^q)^{1/q}}$ 라 하면
$$
|a \cdot b| = \left|\sum a_i b_i \right|\le \sum |a_i||b_i| \le \left(|a_1|^p+ \cdots + |a_n|^p\right)^{1/p} \left(|b_1|^q+ \cdots + |b_n|^q\right)^{1/q}
$$
이다. 



<b>5. </b> 함수 $L(x,\,y,\,z)$ 에 대하여 공간 $\mathcal{F}=\{ f\in \mathcal{C}^1[a,\,b] \mid f(a)=y_a,\, f(b)=y_b\}$  에서 정의된 범함수
$$
\mathcal{L}(f) :=\int_a^b L(u,\,f(u),\, f'(u))\, du
$$
의 Euler-Lagrange 방정식이
$$
D_2 L(u,\, f(u),\, f'(u))=\dfrac{d}{du} D_3 L(u,\, f(u),\, f'(u))
$$
임을 보이라.

---

임의의 일급 함수 
$$
h:[a,\,b] \to \mathbb{R},\qquad h(a)=h(b)=0
$$
에 대하여 
$$
g(t) := \int_a^b L{\big (}u,\, f(u)+th(u),\, f'(u)+th'(u) {\big )} \, du
$$
라 하면 $g(t)$ 는 $t=0$ 에서 최소이므로
$$
0=\left.\dfrac{d}{dt} \right|_{t=0} g(t) = \left.\dfrac{d}{dt}\right|_{t=0} \int_a^b L{\big (}u,\, f(u)+th(u),\, f'(u)+th'(u) {\big )}\, du
$$
가 된다. 따라서,
$$
\begin{aligned}
0 &= \int_a^ b \left.\dfrac{d}{dt}\right|_{t=0} L(u,\, f(u)+th(u),\, f'(u)+th'(u))\, du \\
&= \int_a^bD_2 L(u,\, f(u),\, f'(u))h(u) \, du + \int_a^b D_3L(u,\, f(u),\, f'(u)
)h' (u)\, du \\
&=\int_a^bD_2 L(u,\, f(u),\, f'(u))h(u) \, du + {\big [ }  D_3L(u,\, f(u),\, f'(u))h(u) {\big ]}_a^b  \\
&\qquad -\int_a^b \left(\dfrac{d}{du} D_3 L(u,\, f(u),\, f'(u))\right) h(u)\, du \\
&= \int_a^b \left(D_2 L(u,\, f(u),\, f'(u)) - \dfrac{d}{du}D_3L(u,\, f(u),\, f'(u)\right)h(u)\, du
\end{aligned}
$$
이다. 임의의 $h(u)$ 에 대해 성립해야 하므로 Euler-Lagrange equation 은
$$
D_2 L(u,\, f(u),\, f'(u)) - \dfrac{d}{du}D_3L(u,\, f(u),\, f'(u)=0
$$
이다. 



<b>6. </b> 최단강하선 문제에서 $f$ 가 직선이거나 원호이면 걸리는 시간은 얼마인가.

---

$(0,\,0) \to (a,\, b)$ where $a>0,\, b<0$ 까지의 경로가 $y=f(x)$ 를 따를 때 걸리는 시간 $T$ 는
$$
T=\int_0^a \dfrac{\sqrt{1+f'(x)^2}}{\sqrt{2gf(x)}}\, dx
$$
이다. $f$ 가 직선이면 $y=f(x)= \dfrac{b}{a}x$ 를 따르므로
$$
T_{line}= \int_0^a \dfrac{\sqrt{1+b^2/a^2}}{\sqrt{2gbx/a}}\, dx = \dfrac{\sqrt{a^2+b^2}}{\sqrt{2gab}}2\sqrt{a}=\dfrac{\sqrt{2}\sqrt{a^2+b^2}}{\sqrt{gb}}
$$
$f$ 가 원호이면, 원의 방정식 $(x-c)^2+(y-d)^2=c^2+d^2$ 에 대해 $a^2-2ca+b^2-2db=0$ 을 만족한다.  여기서 원호가 하나로 결정되지 않음에 유의하자. 
$$
\begin{aligned}
y&=d+\sqrt{(c^2+d^2)-(x-c)^2} \\
y'&= -\dfrac{(x-c)}{\sqrt{c^2+d^2-(x-c)^2)}}
\end{aligned}
$$

이므로 
$$
\begin{aligned}
T_{circ} &= \int_0^a \dfrac{\sqrt{1+ \dfrac{(x-c)^2}{c^2+d^2-(x-c)^2}}}{\sqrt{2g (d+ \sqrt{c^2+d^2-(x-c)^2})}}dx  \qquad R=\sqrt{c^2+d^2},\quad (x-c)=R\sin \theta\\
&= \dfrac{1}{\sqrt{2g}}\int_{\sin^{-1}(-c/R)}^{\sin^{-1}(a-c)/R}\dfrac{R}{\sqrt{d+R \cos \theta}}\, d\theta

\end{aligned}
$$



더 계산할 수 있나...

