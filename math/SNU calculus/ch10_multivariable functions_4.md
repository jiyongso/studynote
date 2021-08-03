X. 다변수함수 #4
===





## 제 10 장 탐구문제



<b>1. </b> 좌표평면에서 정의된 함수
$$
h(x,\,y)=\left\{\begin{array}{ll} \dfrac{xy}{x^2+y^2}, \quad & (x,\, y)\ne (0,\,0)\\ 0 , & (x,\,y)=(0,\,0)  \end{array} \right.
$$
은 연속함수가 아님을 보이라. 또 $h(x,\,y)$ 는 모든 점에서 편도함수 $D_1 h(x,\,y),\, D_2 h(x,\,y)$ 가 존재함을 보이라. 함수 $h$ 는 미분가능한 함수인가?

---

$(x,\, y)=(t,\,t)$ 에 대해 $\displaystyle \lim_{t\to 0} h(x,\,y)=\lim_{t \to 0} \dfrac{t^2}{2t^2}=\dfrac{1}{2}$ 이며, $(x,\, y)=(t,\,t^2)$ 에 대해 $\lim_{t \to 0}\dfrac{t^3}{t^2+t^4}=0$ 이다. 따라서 $h(x,\,y)$ 는 연속이 아니다.

도함수는,
$$
\begin{aligned}
D_1 h(x,\, y) &= \dfrac{y(x^2+y^2)-xy(2x)}{(x^2+y^2)^2}=\dfrac{y^3-x^2y}{(x^2+y^2)^2}\\
D_1 h(x,\, y) &= \dfrac{x^3-xy^2}{(x^2+y^2)^2}
\end{aligned}
$$
이다. 함수 $h$ 는 $(x,\,y)=(0,\,0)$ 에서 연속이 아니므로 당연히 미분가능하지 않다. 

$D_1 h(x,\,y)$ 의 경우 $(x,\,y)=(t,\,t)$ 로 놓으면 $t\to 0 \implies h(x,\,y)\to 0$ 이지만  $(x,\,y)=(t,\,t^2)$ 로 놓으면  $t\to 0$ 에서  $h(x,\,y)\to -1$ 이므로 불연속이다. 



<b>2. </b> 좌표평면에서 정의된 함수
$$
f(x,\,y)=\left\{\begin{array}{ll} \dfrac{y^3}{x^2+y^2} , \qquad & (x,\,y) \ne (0,\,0) \\ 0, &(x,\,y)=(0,\,0)\end{array} \right.
$$
은 연속함수인가? 또 이 함수는 원점에서 모든 방향미분계수를 가지는가? 또 $f$ 는 미분가능한 함수인가?

----

$\epsilon>0$ 에 대해 $x^2+y^2=\epsilon^2$ 이라 하면 $|y|\le \epsilon$ 이므로 $\left|\dfrac{y}{x^2+y^2}\right|\le\epsilon$ 이다. 따라서 $\epsilon\to 0$ 이면 $f(x,\,y)\to 0$ 이므로 연속함수이다.
$$
\begin{aligned}
D_1 f(x,\,y) &= \dfrac{-2xy^3}{(x^2+y^2)^2}\\
D_2 f(x,\,y) &= \dfrac{3y^2(x^2+y^2)-2y^4}{(x^2+y^2)^2}=\dfrac{3x^2y^2+y^4}{(x^2+y^2)^2}

\end{aligned}
$$
이다. $D_1f$ 를 $(x,\,y)= (t,\,t)$ 에 따라 $t\to 0$ 극한을 취하면 $-\frac{1}{2}$ 이다. 그러나 $(x,\, y)=(0,\,t)$ 를 따라 극한을 취하면  $0$ 이므로  $D_1f$ 는 $(0,\,0)$  에서 연속이 아니다. 따라서 $f$ 원점에서 방향미분계수를 갖지 않는다. 따라서 $f$ 는 미분가능하지 않다.



<b>3. </b> 함수
$$
f(x) =\left\{\begin{array}{ll} \dfrac{xy}{x^2-y},\qquad &x^2\ne y \\ 0 , & x^2=y  \end{array} \right.
$$
은 원점에서 연속은 아니지만 모든 방향 미분계수가 존재함을 보이라.

---

$(x,\,y)=(t,\,t^2-t^3)$ 경로에서  $t\to 0$ 극한을 취하면 
$$
\lim_{t\to 0} \dfrac{t(t^2-t^3)}{t^3}=1
$$
이므로 연속이 아니다. 
$$
\begin{aligned}
D_1 f(x,\,y) &= \dfrac{y(x^2-y)-2x^2y}{(x^2-y)^2}=-\dfrac{x^2y+y^2}{(x^2-y)^2}\\
D_2 f(x,\,y) &= \dfrac{x(x^2-y)+xy}{(x^2-y)^2} = \dfrac{x^3}{(x^2-y)^2}

\end{aligned}
$$
이다. $(0,\,0)$ 에서의 $\mathbf{e}_1$ 방향 미분 계수는 
$$
\lim_{t\to 0} \dfrac{f(tx,0)-f(0,\,0)}{t}=0
$$
이며 $y\ne 0$​ 방향에서의 방향미분계수는
$$
\lim_{t \to 0}\dfrac{f(tx,\,ty)-f(0,\,0)}{t}=\lim_{t \to 0}\dfrac{t^2xy}{t^2(tx^2-y)}=-x
$$
이므로 원점에서의 방향미분계수는 $0$ 이다.



<b>4. </b> 함수
$$
f(x,\,y) = \left\{\begin{array}{ll} \dfrac{x^2y\sqrt{x^2+y^2}}{x^4+y^2}, \qquad & (x,\,y) \ne (0,\,0) \\ 0, & (x,\,y) = (0,\,0) \end{array} \right.
$$
는 원점에서 연속이고 모든 방향미분계수가 $0$ 이지만, 미분가능함수가 아님을 보이라.

---

산술평균, 기하평균으로부터,
$$
x^4+y^2 \ge 2\sqrt{x^4y^2}=2|x^2y|
$$
임을 안다. 따라서,
$$
|f(x,\,y)| \le \dfrac{\sqrt{x^2+y^2}}{2}
$$
이므로 원점에서 연속이다.

원점에서의 방향미분계수는
$$
\lim_{t \to 0}\dfrac{f(tx,\,ty)-f(0,\,0)}{t}= \lim_{t\to 0}\dfrac{t^4x^2y\sqrt{x^2+y^2}}{t^3(t^2x^2+y^2)}= \lim_{t \to 0}\dfrac{tx^2y \sqrt{x^2+y^2}}{t^2x^2+y^2}=0
$$
이다. 
$$
\begin{aligned}
D_1 f(x,\,y) &= \dfrac{(x^4+y^2)\left(2xy\sqrt{x^2+y^2}+\dfrac{2x^3y}{\sqrt{x^2+y^2}}\right)-4x^5y\sqrt{x^2+y^2}}{(x^4+y^2)^2} \\
&=\dfrac{2xy(x^4+y^2) \left(3x^2+y^2\right)-4x^5y(x^2+y^2)}{(x^4+y^2)^2\sqrt{x^2+y^2}} \\
&= \dfrac{2xy(3x^6+x^4y^2+3x^2y^2+y^4-4x^6-4x^4y^2)}{(x^4+y^2)^2\sqrt{x^2+y^2}}\\
&= \dfrac{2xy(-x^6-3x^4y^2+3x^2y^2+y^4)}{(x^4+y^2)^2\sqrt{x^2+y^2}}
\end{aligned}
$$
이므로 $(x,\,y)=(t,\,t^2)$​ 로 놓고 $t \to 0$​ 극한을 취하면,
$$
\lim_{t \to 0} D_1 f(t,\,t^2)= \lim_{t \to 0}\dfrac{4t^3(t^6-t^8)}{4t^9\sqrt{1+t^2}}=1
$$
이며 $(x,\,y)=(t,\,0)$ 으로 놓고  $t\to 0$ 극한을 취하면,
$$
\lim_{t \to 0}D_1f(t,\,0)=0
$$
이므로 방향도함수  $D_1 f$ 는 원점에서 연속이 아니다. 따라서 미분가능함수가 아니다.





<b>5. </b> 일단 생략



<b>6. </b> $n$-공간의 정규직교기저  $\mathbf{v}_1,\ldots,\,\mathbf{v}_n$ 과 미분가능 함수 $f(x_1,\ldots,\,x_n)$ 에 대하여
$$
\nabla f(P)=\sum_{i=1} D_{\mathbf{v}_i}f(P)\mathbf{v}_i
$$
임을 보이라.

---

$n$-공간에서의 임의의 벡터 $\mathbf{u},\,\mathbf{v}$와 실수 $c$ 에 대해 미분가능함 함수 f의 $\mathbf{u}+c\mathbf{v}$ 방향의 도함수는
$$
D_{\mathbf{u}+c\mathbf{v}}f(P) =  \mathbf{a}\cdot (\mathbf{u}+c\mathbf{v})=\mathbf{a}\cdot \mathbf{u}+c\mathbf{a}\cdot\mathbf{v} = D_{\mathbf{u}}f(P)+cD_\mathbf{v} f(P)
$$
이다. 여기서 $\mathbf{a} = \nabla f(P)$ 이다. 

$n$-공간에서의 임의의 정규직교기저 $\mathbf{v}_1,\ldots,\mathbf{v}_n$ 이 주어졌을 때 선형변환을 통해 이를 표준정규직교기저 $\mathbf{e}_1,\ldots,\,\mathbf{e}_n$ 으로 바꾸는 선형변환이 존재하며, 
$$
\mathbf{e}_j = \sum_{i=1}^n a_{ij}\mathbf{v}_i
$$
로 쓸 수 있다. 이 때 
$$
\mathbf{e}_j \cdot \mathbf{v}_k = \sum_{i=1}^n a_{ij}\mathbf{v}_i \cdot \mathbf{v}_k =a_{kj}
$$
이다. 이로부터
$$
\delta_{ik}=\mathbf{e}_i \cdot \mathbf{e}_k= \sum_{j, l}a_{ji}\mathbf{v}_j \cdot a_{lk}\mathbf{v}_l = \sum_{jl}a_{ji}a_{lk}\delta_{jl}=\sum_{j}a_{ji}a_{jk}
$$
임을 안다. 이제,
$$
\begin{aligned}
\nabla f(P) &= \sum_{j=1}^n D_j f(P)\mathbf{e}_j \\
&= \sum_{j=1}^n\sum_{i=1}^nD_{a_{ij}\mathbf{v}_i} f(P) \sum_{k=1}^n a_{kj}\mathbf{v}_k\\
&=\sum_{i=1} \sum_{j=1}\sum_{k=1} D_{\mathbf{v}_i} a_{ij}a_{kj}\mathbf{v}_k\\
&=\sum_{i=1}\sum_{k=1}D_{\mathbf{v}_i}f(P)\mathbf{v}_k \delta_{ik}\\
&=\sum_{i=1}D_{\mathbf{v}_i}f(P)\mathbf{v}_i
\end{aligned}
$$
이다.



<b>7. </b> 원기둥좌표계
$$
(x,\,y,\,z)=G(r,\,\theta,\,z)=(r\cos \theta,\, r \sin \theta ,\, z)
$$
에서
$$
\mathbf{e}_r = {\dfrac{\partial G}{\partial r}}\left/{\left|\dfrac{\partial G}{\partial r}\right|}\right., \qquad \mathbf{e}_\theta = {\dfrac{\partial G}{\partial \theta}}\left/{\left|\dfrac{\partial G}{\partial \theta}\right|}\right.,\qquad \mathbf{e}_z = {\dfrac{\partial G}{\partial z}}\left/{\left|\dfrac{\partial G}{\partial z}\right|}\right.
$$
라고 두자. 이때 임의의 일급함수 $f(x,\,y,\,z)$ 에 대하여
$$
\nabla f = \dfrac{\partial f}{\partial r}\mathbf{e}_r + \dfrac{1}{r} \dfrac{\partial f}{\partial \theta} e_{\theta}+\dfrac{\partial f}{\partial z}\mathbf{e}_z 
$$
임을 보이라.

---

$$
\begin{aligned}
\dfrac{\partial G}{\partial r} &= (\cos \theta,\, \sin \theta,\, 0) \\
\left|\dfrac{\partial G}{\partial r}\right| &=  1\\
\dfrac{\partial G}{\partial \theta} &= (-r\sin \theta,\, r\cos \theta,\, 0) \\
\left|\dfrac{\partial G}{\partial \theta}\right| & =r\\
\dfrac{\partial G}{\partial z} &= (0,\, 0,\, 1)\\
\left|\dfrac{\partial G}{\partial z}\right| & =1
\end{aligned}
$$
이다. 또한,
$$
\begin{aligned}
\mathbf{e}_r &= \left(\dfrac{x}{r},\, \dfrac{y}{r},\, 0\right) =(\cos \theta,\, \sin\theta,\,0)\\
\mathbf{e}_\theta &= \left(\dfrac{-y}{r},\, \dfrac{x}{r},\, 0\right)=(-\sin \theta,\,\cos \theta,\,0)\\
\mathbf{e}_z &= (0,\,0,\,1)
\end{aligned} 
$$
이다. 
$$
\begin{aligned}
\dfrac{\partial f}{\partial x} &= \dfrac{\partial r}{\partial x}\dfrac{\partial f}{\partial r} + \dfrac{\partial \theta}{\partial x}\dfrac{\partial f}{\partial \theta} + \dfrac{\partial z}{\partial x}\dfrac{\partial f}{\partial z} = \cos \theta \dfrac{\partial f}{\partial r}-\dfrac{\sin \theta}{r}\dfrac{\partial f}{\partial \theta} \\
\dfrac{\partial f}{\partial y} &= \dfrac{\partial r}{\partial y}\dfrac{\partial f}{\partial r} + \dfrac{\partial \theta}{\partial y}\dfrac{\partial f}{\partial \theta} + \dfrac{\partial z}{\partial y}\dfrac{\partial f}{\partial z}  = \sin \theta  \dfrac{\partial f}{\partial r}+ \dfrac{\cos \theta}{r} \dfrac{\partial f}{\partial \theta} \\
\end{aligned}
$$

이므로,
$$
\begin{aligned}
\nabla f&= (\cos \theta, \sin \theta, 0)\dfrac{\partial f}{\partial r} + \dfrac{1}{r}(-\sin \theta,\, \cos \theta, 0) \dfrac{\partial f}{\partial \theta}+ (0,\,0,\,1)\dfrac{\partial f}{\partial z} \\
&= \dfrac{\partial f}{\partial r} \mathbf{e}_r + \dfrac{1}{r} \dfrac{\partial f}{\partial \theta}\mathbf{e}_{\theta} + \dfrac{\partial f}{\partial z}\mathbf{e}_z
\end{aligned}
$$



<b>8</b> 구면좌표꼐
$$
(x,\,y,\,z)=G(\rho,\,\varphi,\, \theta)=(\rho \sin \varphi \cos \theta,\, \rho \sin \varphi \sin \theta,\, \rho \cos \varphi) 
$$
에서
$$
\mathbf{e}_{\rho} = {\dfrac{\partial G}{\partial \rho}}\left/{\left|\dfrac{\partial G}{\partial \rho}\right|}\right., \qquad \mathbf{e}_\varphi = {\dfrac{\partial G}{\partial \varphi}}\left/{\left|\dfrac{\partial G}{\partial \varphi}\right|}\right.,\qquad \mathbf{e}_{\theta} = {\dfrac{\partial G}{\partial \theta}}\left/{\left|\dfrac{\partial G}{\partial \theta}\right|}\right.
$$
라고 두자. 이때 임의의 일급함수 $f(x,\,y\,z)$ 에 대하여
$$
\nabla f = \dfrac{\partial f}{\partial \rho}\mathbf{e}_{\rho} + \dfrac{1}{\rho}\dfrac{\partial f}{\partial \varphi} \mathbf{e}_{\varphi} + \dfrac{1}{\rho \sin\varphi}\dfrac{\partial f}{\partial \theta} \mathbf{e}_\theta
$$

임을 보이라.

---

$$
\begin{aligned}
\dfrac{\partial G}{\partial \rho} &=(\sin \varphi \cos \theta,\, \sin \varphi \sin\theta, \cos \varphi) \\
\dfrac{\partial G}{\partial \varphi} &= (\rho \cos \varphi \cos \theta,\, \rho \cos \varphi \sin \theta,\, - \rho \sin \varphi) \\
\dfrac{\partial G}{\partial \theta} &= (-\rho \sin \varphi \sin \theta,\, \rho \sin \varphi \cos \theta,\, 0)\\
\left|\dfrac{\partial G}{\partial \rho}\right| &= 1\\
\left|\dfrac{\partial G}{\partial \varphi}\right| &= \rho  \\
\left|\dfrac{\partial G}{\partial \theta}  \right| &= \rho \sin \varphi 
\end{aligned}
$$
이며,

$$
\begin{aligned}
\mathbf{e}_{\rho} &= (\sin \varphi \cos \theta,\, \sin \varphi \sin \theta,\, \cos \varphi) \\
\mathbf{e}_{\varphi}  &= (\cos \varphi \cos \theta,\, \cos \varphi \sin \theta,\, - \sin \varphi) \\
\mathbf{e}_{\theta} &= ( -\sin \theta,\, \cos \theta,\, 0)
\end{aligned}
$$
이다. 또한, 
$$
\begin{aligned}
\dfrac{\partial f}{\partial x} &= \dfrac{\partial \rho}{\partial x}\dfrac{\partial f}{\partial \rho}+ \dfrac{\partial \varphi}{\partial x}\dfrac{\partial f}{\partial \varphi}+ \dfrac{\partial \theta}{\partial x}\dfrac{\partial f}{\partial \theta} = \sin \varphi \cos \theta  \dfrac{\partial f}{\partial \rho} + \dfrac{\cos \varphi \cos \theta}{\rho} \dfrac{\partial f}{\partial \varphi}-\dfrac{\sin \theta}{\rho\sin \varphi}\dfrac{\partial f}{\partial \theta} \\
\dfrac{\partial f}{\partial y} &= \dfrac{\partial \rho}{\partial y}\dfrac{\partial f}{\partial \rho}+ \dfrac{\partial \varphi}{\partial y}\dfrac{\partial f}{\partial \varphi}+ \dfrac{\partial \theta}{\partial y}\dfrac{\partial f}{\partial \theta} = \sin \varphi \sin \theta \dfrac{\partial f}{\partial \rho}  + \dfrac{\cos \varphi\sin \theta }{\rho} \dfrac{\partial f}{\partial \varphi} + \dfrac{\cos \theta}{\rho \sin \varphi} \dfrac{\partial f}{\partial \theta} \\
\dfrac{\partial f}{\partial z} &= \dfrac{\partial \rho}{\partial z}\dfrac{\partial f}{\partial \rho}+ \dfrac{\partial \varphi}{\partial z}\dfrac{\partial f}{\partial \varphi}+ \dfrac{\partial \theta}{\partial z}\dfrac{\partial f}{\partial \theta} = \cos \varphi \dfrac{\partial f}{\partial \rho} -\dfrac{\sin \phi}{\rho} \dfrac{\partial f}{\partial \varphi} 
\end{aligned}
$$

이다. 따라서,

$$
\begin{aligned}
\nabla f &= (\sin \varphi \cos \theta,\, \sin \varphi \sin \theta,\, \cos \varphi) \dfrac{\partial f}{\partial \rho} + \dfrac{1}{\rho}( \cos \varphi \cos \theta,\, \cos \varphi \sin \theta,\, -\sin \varphi) \dfrac{\partial f}{\partial \varphi} \\
&\qquad + \dfrac{1}{\rho\sin \varphi}(-\sin \theta,\, \cos \theta,\, 0)\dfrac{\partial f}{\partial \theta} \\
&= \dfrac{\partial f}{\partial \rho}\mathbf{e}_{\rho}+\dfrac{1}{\rho}\dfrac{\partial f}{\partial \varphi}\mathbf{e}_{\varphi} + \dfrac{1}{\rho \sin \varphi} \dfrac{\partial f}{\partial \theta }\mathbf{e}_{\theta} 
\end{aligned}
$$



<b>9. </b> 좌표공간의 한 닫힌 집합 $A$ 에서 정의된 연속함수 $f:A \to \mathbb{R}$ 가
$$
\lim_{P \to \infty} f(P)=\infty
$$
을 만족시키면, $f$ 는 최소값을 가짐을 보이라.

---
많이 쓰이는 정의이지만, $f(A)$ 를 다음과 같이 정의하자.
$$
f(A):=\{f(a): a\in A\}
$$

우선 $f(A)$ 가 아래로 유계임을 보이자. 만약 $f(A)$ 가 아래로 유계가 아니라면 어떤 $Q\in A$, $|Q|<\infty$ 에서 
$$
\lim_{P \to Q}f(P)=-\infty
$$
이어야 하는데 이는 연속함수라는 조건에 위배된다. 따라서 $f(A)$ 는 아래로 유계이다. 이제 $f(A)$ 는 최소값을 갖지 않는다고 가정하자. 실수의 완비성에 의해 $f(A)$ 의 최소값은 ($\mathbb{R}$ 에서) 존재하나 이 값이 $f(A)$ 에 포함되지 않는다는 뜻이다. 이 최소값을 $m$ 이라 하고 $g:A \to \mathbb{R}$ 을 다음과 같이 정의하자.

$$
g(X) = \dfrac{1}{f(X)-m}
$$

이 때 $f(A)-m\ne 0\;\forall X\in A$ 이므로 $g$ 양의 연속함수며, 따라서 아래로 유계이다. 즉 어떤 $m' > 0$ 에 대해
$$
g(A)<m'
$$
이다. 

그렇다면,
$$
\dfrac{1}{f(X)-m}<m' \implies f(X) > m+\dfrac{1}{m'}
$$
이므로 $f(A)$ 의 하한이 $m$ 이라는 것에 위배된다. 따라서 $f(A)$ 는 최소값을 가진다.



<b>10. </b> 좌표공간의 표준 좌표계 $(x,\,y,\,z)$ 에서 얻은 벡터장 $(\partial_x,\,\partial_y,\,\partial_z)$ 와 구면좌표계 $(\rho,\,\varphi,\,\theta)$ 에서 얻은 벡터장 $(\partial_{\rho},\,\partial_{\varphi},\,\partial_{\theta})$​ 에 대하여 다음을 보이라.
$$
\begin{aligned}
\partial_x &= \sin\varphi \cos \theta \partial_{\rho}+ \dfrac{\cos \varphi \cos \theta}{\rho} \partial_{\varphi} - \dfrac{\sin\theta}{\rho \sin \varphi} \partial_{\theta} \\
\partial_y &= \sin \varphi \sin \theta \partial_{\rho} + \dfrac{\cos \varphi \sin \theta}{\rho} \partial_{\varphi} + \dfrac{\cos \theta}{\rho \sin \varphi}\partial_{\theta}\\
\partial_z &= \cos \varphi \partial_{\varphi} -\dfrac{\partial \varphi}{\rho}\partial_{\varphi}
\end{aligned}
$$

---

$$
\begin{aligned}
\rho &= \sqrt{x^2+y^2+z^2} \\
\varphi &= \arctan \left( \dfrac{\sqrt{x^2+y^2}}{z} \right) \\
\theta &= \arctan \left(\dfrac{y}{x}\right)
\end{aligned}
$$

이며,

$$
\begin{aligned}
(x,\,y,\,z) =(\rho \sin \varphi\cos \theta,\, \rho \sin \varphi \sin \theta,\, \rho \cos \varphi)
\end{aligned}
$$

이므로,
$$
\begin{aligned}
\partial_x &= \dfrac{\partial \rho}{\partial x}\partial_{\rho}+ \dfrac{\partial \varphi}{\partial x}\partial_{\varphi}+ \dfrac{\partial \theta}{\partial x}\partial_\theta \\
&= \dfrac{x}{\rho}\partial_\rho + \dfrac{x/(z\sqrt{x^2+y^2})}{1+\dfrac{x^2+y^2}{z^2}} \partial_{\varphi} + \dfrac{-y/x^2}{1+\dfrac{y^2}{x^2}} \partial_{\theta} \\
&= \sin \varphi \cos \theta \partial_\rho + \dfrac{\rho^2\sin \varphi \cos \varphi \cos \theta}{\rho^3\sin \varphi} \partial_{\varphi} - \dfrac{\rho \sin \varphi \sin \theta}{\rho^2 \sin \varphi} \partial_{\theta} \\
&= \sin \varphi \cos \theta \partial_\rho + \dfrac{\cos \varphi \cos \theta}{\rho} \partial_{\varphi} - \dfrac{\sin \theta}{\rho}\partial_{\theta} \\
\partial_y &= \dfrac{\partial \rho}{\partial y}\partial_{\rho}+ \dfrac{\partial \varphi}{\partial y}\partial_{\varphi}+ \dfrac{\partial \theta}{\partial y}\partial_\theta \\
&= \sin \varphi \sin \theta \partial_{\rho} + \dfrac{\rho^2 \sin \varphi \cos \varphi \sin \theta}{\rho^3 \sin \varphi}\partial_{\varphi} + \dfrac{1/x}{1+y^2/x^2}\partial_{\theta} \\
&= \sin \varphi \sin \theta \partial_{\rho}  + \dfrac{\cos \varphi \sin \theta}{\rho} \partial_{\varphi} + \dfrac{\cos \theta}{\rho \sin \varphi} \partial _{\theta} \\
\partial_z &= \dfrac{\partial \rho}{\partial z}\partial_{\rho}+ \dfrac{\partial \varphi}{\partial z}\partial_{\varphi}+ \dfrac{\partial \theta}{\partial z}\partial_\theta \\
&= \cos \varphi \partial_{\rho} - \dfrac{\sin \varphi}{\rho} \partial_{\varphi}
\end{aligned}
$$

