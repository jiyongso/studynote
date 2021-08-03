X. 다변수함수 #2
===



## 연습문제 제 10 장 4 절



#### 정리 4.0.2 

$n$-공간의 열린 집합 $U$ 에서 정의된 함수 $f:U \to \mathbb{R}$ 가 점 $P\in U$ 에서 미분가능하면

(1) $f$ 는 점 $P$ 에서 연속이다.

(2) $f$ 는 점 $P$ 에서 모든 방향의 방향미분계수를 가지고
$$
D_\mathbf{v} f(P)=\nabla f(P)\cdot \mathbf{v} \qquad (\mathbf{v}\in \mathbb{R}^n)
$$
​	이다.

(3) 식 (10.4)를 만족시키는 벡터 $\mathbf{a}$ 는 $\nabla f(P)$ 이다.

---

*(proof)* (1) 식 (10.5) $f(P+\mathbf{v})-f(P)=\mathbf{a}\cdot \mathbf{v}+o(\mathbf{v})$ 이므로,
$$
\lim_{\mathbf{v}\to \mathbf{0}} f(P +\mathbf{v})-f(P)=\lim_{\mathbf{v}\to \mathbf{0}} \mathbf{a}\cdot \mathbf{v} + o(\mathbf{v}) = 0
$$
이다. 따라서 $f$ 는 $P$ 에서 연속이다.

(2) 
$$
D_{\mathbf{v}} f(P)=\lim_{t\to 0} \dfrac{f(P+t\mathbf{v})-f(P) }{t}=\lim_{t\to 0} \dfrac{t\mathbf{a}\cdot \mathbf{v} }{t}=\mathbf{a}\cdot \mathbf{v}
$$
이므로 모든 방향의 방향미분이 존재한다. $\mathbf{a}=(a_1,\ldots,\,a_n)$ 이라 하면,
$$
D_k f(P)=\mathbf{a}\cdot \mathbf{e}_k=a_k
$$
이므로,
$$
\nabla f(P)=\mathbf{a}
$$
이며, 따라서,
$$
D_\mathbf{v}f(P)=\nabla f(P)\cdot \mathbf{v}
$$
이다.

(3) (2)에서 보였다. $\square$



<b>1. </b> 좌표평면에서 온도분포함수가 함수
$$
f(x,\,y)=x^2y+xy^2 \quad({}^\circ \text{C})
$$
으로 주어졌을 때, 점 $(2,\,3)$ 에 위치한 길동이는

(1) 어느 방향으로 움직여야 빨리 시원해질까? 이때의 온도 순간변화율은 얼마인가?

(2) 가장 빨리 뜨거워지는 방향은 어느방향인가? 또 이 방향의 온도순간변화율은 얼마인가?

----

$$
\begin{align}
\nabla f(x,\,y) &= (2xy+y^2,\, x^2+2xy)\\
\nabla f(2,\,3) &=(21,\, 16)
\end{align}
$$

이다. 가장 빨리 시원해지는 방향의 방향벡터는 $-\dfrac{(21,\, 16)}{\sqrt{21^2+16^2}}$ 이며 이때의 온도의 순간변화율은 $\nabla f(2,\,3)$ 과의 내적이므로 $-\sqrt{21^2+16^2}\approx -26.40$ 이며 가장 빨리 뜨거워지는 방향의 방향벡터는 $\dfrac{(21,\, 16)}{\sqrt{21^2+16^2}}$ 이며 온도의 순간변화율은 $\approx 26.40$ 이다.



<b>2. </b> 좌표평면에서 정의된 미분가능함수 $f(x,\,y)$ 가 원점에서, $(1,\,2)$-방향 미분계수가 $1$ 이고 $(2,\,3)$ 방향 미분계수가 $2$ 라고 하자. 원점에서의 이 함수의 $(3,\,5)$ 방향 미분계수는 얼마인가? 또 기울기 벡터 $\nabla f(O)$ 를 구하라.

---

$$
\begin{align}
D_{(1,\,2)}f(O)&=\nabla f(O) \cdot (1,\,2)=1 \\
D_{(2,\,3)}f(O) &= \nabla f(O) \cdot (2,\,3)=2\\
D_{(3,\,5)}f(O) &= \nabla f(O) \cdot (3,\,5) = \nabla f(O) \cdot {\big(} (1,\,2)+(2,\,3){\big)}=3
\end{align}
$$

이다. $\nabla f(O)=(a,\,b)$ 라 하면 $a+2b=1,\, 2a+3b=2$ 이므로 $a=1,\,b=0$ 이다. 즉 $\nabla f(O)=(1,\,0)$ 이다.





<b>3. </b> 동차 다항함수
$$
a_0 x^n + a_1 x^{n-1}y + \cdots + a_{n-1}xy^{n-1}+a_n y^n
$$
는 일급함수인가? 또 이것은 미분가능함수인가? 모든 다항함수는 일급함수인가? 두 다항식의 몫으로 주어지는 유리함수는 (정의역에서) 일급함수인가?

---

위의 동차 다항함수를 $f(x,\,y)$ 라 하면,
$$
\nabla f(x,\,y)=(a_0 nx^{n-1}+a_1(n-1)x^{n-2}y + \cdots + a_{n-1}y^{n-1},\, a_1x^{n-1}+2a_2x^{n-2}y+\cdots + a_{n-1}(n-1)xy^{n-2}+ a_n n y^{n-1})
$$
이며 각각의 components 도 동차 다항함수이므로 연속이다. 따라서 동차 다항함수는 일급함수이다.

임의의 다항함수의 편미분 역시 다항함수이므로 연속이고, 따라서 일급함수이다. 

임의의 다항식 $p(x,\,y),\, q(x,\,y)$ 의 몫 $\dfrac{p(x,\, y)}{q(x,\, y)}$ 을 $q(x,\, y)\ne 0$ 인 정의역에서 생각하자. 
$$
\nabla\left(\dfrac{p(x,\,y)}{q(x,\,y)}\right)=\left( \dfrac{q(x,\, y)D_1 p(x,\,y)-p(x,\, y)D_1q(x,\,y)}{q(x,\,y)^2}, \dfrac{q(x,\, y)D_2 p(x,\,y)-p(x,\, y)D_2q(x,\,y)}{q(x,\,y)^2}  \right)
$$
이므로 $q(x,\,y)\ne 0$ 인 영역에서 각 편미분이 연속이다. 따라서 일급함수이다.



<b>4. </b> 직사각형 $(a,\,b)\times (c,\,d)\subset \mathbb{R}^2$ 에서 정의된 미분가능함수 $f(x,\,y),\, g(x,\,y)$ 가 항등적으로
$$
\dfrac{\partial f}{\partial x}= \dfrac{\partial g}{\partial x}
$$
이면 
$$
f(x,\,y)= g(x,\,y)+h(y)
$$
를 만족시키는 미분가능함수 $h:(c,\,d)\to \mathbb{R}$ 이 존재함을 설명하라.

---

$k : (a,\,b)\times (c,\,d)\to \mathbb{R}^2$ 를 $k(x,\,y)=f(x,\,y)-g(x,\,y)$ 로 정의하면,
$$
\dfrac{\partial k}{\partial x}=\dfrac{\partial f}{\partial x}-\dfrac{\partial g}{\partial x}=0
$$
이다. 이는 평균값 정리를 이용하면 임의의 $x_1<x_2\in (a,\,b)$ 와 정해진 $y\in (c,\,d)$ 에 대해  
$$
\dfrac{\partial k}{\partial x}(x_0,\,y)=k(x_2,\,y)-k(x_1,\,y)
$$
를 만족하는 $x_0\in (x_1,\,x_2)$ 가 존재함을 의미한다. 그런데 어떤 $x_0\in (a,\,b)$ , $y\in (c\,d)$ 에 대해서도 $\dfrac{\partial k}{\partial x}=0$ 이므로 $k(x_2,\, y)-k(x_1,\,y)=0$ 이다. 따라서 아무 $x_0\in (a,\,b)$ 에 대해서도 $k(x,\,y)=k(x_0,\,y)$ 이다. 이제 $h(y)=k(x_0,\,y)$ 라 놓을 수 있다.



<b>5. </b> 좌표평면의 원점 근방에서 정의된 함수 $f(x,\,y)$ 에 대하여 $D_1 f(O)=1,\, D_2 f(O)=-2$ 라 하자. 이 대 함수값의 변화가 거의 없는 방향은 어느 방향인가?

---

$\mathbf{v}=(v_1,\,v_2)$ 라 하면,
$$
D_{\mathbf{v}}f(O) = (1,\,-2)\cdot (v_1,\,v_2)=v_1-2v_2
$$
이며 $\mathbf{v}=(2,\,1)$ 혹은 $\mathbf{v}=(-2,\,-1)$ 일 때 $D_\mathbf{v} f(O)=0$ 이다. 따라서 $\pm(2,\,1)$ 방향이 함수값의 변화가 거의 없는 방향이다.





## 연습문제 제 10 장 5 절



<b>1. </b> 좌표평면의 표준직교좌표계 $(x,\,y)$ 와 극좌표계 $(r,\,\theta)$ 에 대하여
$$
\begin{align}
\partial_x &= (\cos \theta)\partial_r - \dfrac{\sin \theta}{r}\partial_\theta\\
\partial_y &= (\sin \theta)\partial_r + \dfrac{\cos \theta}{r}\partial_\theta

\end{align}
$$
임을 보이라. 또 이로부터
$$
|\nabla f|^2 = \left(\dfrac{\partial f}{\partial r}\right)^2+\dfrac{1}{r^2}\left(\dfrac{\partial f}{\partial \theta}\right)^2
$$
을 유도하라.

---

$r=\sqrt{x^2+y^2},\, \theta = \arctan\left(\dfrac{y}{x}\right)$ 로부터, 
$$
\begin{align}
\partial_x r &= \dfrac{x}{r}=\cos \theta \\
\partial_y r &= \dfrac{y}{r} = \sin \theta\\
\partial_x \theta &= -\dfrac{y}{x^2} \dfrac{1}{1+y^2/x^2}= -\dfrac{y}{x^2+y^2}=\dfrac{\sin \theta}{r} \\
\partial_y \theta &= \dfrac{1}{x} \dfrac{1}{1+y^2/x^2} = \dfrac{x}{x^2+y^2}=\dfrac{\cos\theta}{r}

\end{align}
$$
이므로,
$$
\begin{align}
\partial_x f(r,\,\theta) &= (\partial _xr) (\partial_r f)+ (\partial_x \theta)(\partial_\theta f) = {\big (}(\cos \theta)\partial _r -\dfrac{\sin\theta}{r}\partial_\theta {\big )}f(r,\,\theta) \\
\partial_y f(r,\theta) &= (\partial_y r)(\partial_r f)+(\partial_y \theta)(\partial_\theta f)={\big (} (\sin \theta)\partial r + \dfrac{\cos \theta}{r}\partial_\theta {\big )}f(r,\,\theta)
\end{align}
$$
이다.  따라서,
$$
\begin{align}
|\nabla f|^2  &= (\cos \theta)^2 \left(\partial_r f\right)^2+ \dfrac{\sin^2\theta}{r^2}\left(\partial_\theta f\right)^2-2 \dfrac{\cos\theta \sin \theta}{r} (\partial _r f)(\partial_\theta f) \\ &\qquad+  (\sin \theta)^2 \left(\partial_r f\right)^2+ \dfrac{\cos^2\theta}{r^2}\left(\partial_\theta f\right)^2+2 \dfrac{\cos\theta \sin \theta}{r} (\partial _r f)(\partial_\theta f)\\
&=(\partial_r f)^2+ \dfrac{1}{r^2}(\partial_\theta f)^2

\end{align}
$$


<b>2. </b> (**오일러 공식**) 주어진 자연수 $k$ 에 대하여 함수 $f(x_1,\ldots,\,x_n)$ 이	
$$
f(tx_1,\ldots,\,tx_n)=t^k f(x_1,\ldots,\,x_n) ,\qquad \forall t,\, x_i \in \mathbb{R}
$$
을 만족시킬 때,
$$
x_1D_1 f(x_1,\ldots,\,x_n)+ \cdots + x_nD_n f(x_1,\ldots,\,x_n)=kf(x_1,\ldots,,x_n)
$$
임을 보이라.

---

$$
f(t\mathbf{x})=t^k f(\mathbf{x})
$$

이므로,
$$
\dfrac{d}{dt}f(t\mathbf{x})=\mathbf{x} \cdot \nabla f(t\mathbf{x})\implies kt^{k-1}f(\mathbf{x})=\sum_{i=1}^n x_i D_i f(t\mathbf{x}) = \mathbf{x} \cdot \nabla f(t\mathbf{x})
$$
이다. $t=1$ 을 대입하면 주어진 식을 얻는다.



<b>3. </b> 미분가능함수 $f(\mathbf{x})$ 가 임의의 실수 $t$ 와 임의의 $\mathbf{x}\in\mathbb{R}^n$ 에 대하여 $f(t\mathbf{x})=tf(\mathbf{x})$  이면
$$
f(\mathbf{x})=\mathbf{a}\cdot \mathbf{x}
$$
를 만족시키는 벡터 $\mathbf{a}$ 가 존재함을 보이라.

---

문제 2로 의 풀이에서 
$$
f(\mathbf{x}) = \mathbf{x} \cdot \nabla f(t\mathbf{x})
$$
를 얻는다. $t=0$ 을 대입하고 $\nabla{f}(O)=\mathbf{a}$ 라 놓으면 
$$
f(\mathbf{x})=\mathbf{a} \cdot \mathbf{x}
$$
이다. 

<b>4. </b> 미분가능함수 $f$ 에 대하여 $z=f\left(\dfrac{x-y}{y}\right)$ 로 둘 때,
$$
x\dfrac{\partial z}{\partial x}+ y \dfrac{\partial z}{\partial y}=0
$$
임을 보이라. 

---

$$
x\dfrac{\partial z}{\partial x}+y\dfrac{\partial z}{\partial y}= \dfrac{x}{y} f'\left(\dfrac{x-y}{y}\right)+ y \left(-\dfrac{x}{y^2}\right)f'\left(\dfrac{x-y}{y}\right)=0
$$



<b>5. </b> 함수
$$
f(x,\,y):=\int_{xy}^{x^2+y^2} e^{-(t-1)^2}\, dt
$$
의 편미분계수 $\dfrac{\partial f}{\partial x}(1,\,0)$ 과 $\dfrac{\partial f}{\partial y}(0,\,1)$ 을 구하라.

---

$$
F(s):=\int_{0}^{s} e^{-(t-1)^2}\, dt
$$

라 정의하면,
$$
f(x,\,y) = F(x^2+y^2)-F(xy) \\
F'(s) = e^{-(s-1)^2}
$$
이다. 따라서,
$$
\begin{align}
\dfrac{\partial f}{\partial x}(1,\,0) &= 2x e^{-(x^2+y^2-1)^2} - ye^{-(xy-1)^2}{\big |}_{(1,\,0)}=2\\
\dfrac{\partial f}{\partial y}(0,\,1) &= 2ye^{-(x^2+y^2-1)^2}-x e^{-(xy-1)^2}{\big |}_{(0,\,1)}=2

\end{align}
$$


<b>6. </b> 연속함수 $g(t)$ 와 일급함수 $a(x,\,y),\, b(x,\,y)$ 에 대하여, 함수
$$
f(x,\,y)=\int_{a(x,\,y)}^{b(x,\,y)} g(t)\, dt
$$
의 편도함수 $D_1 f(x,\,y),\, D_2 f(x,\,y)$ 를 구하라.

---

$g(t)$ 가 연속함수이므로
$$
G(t) = \int_{t_0} ^t g(t')\, dt'
$$
을 정의 할 수 있다. 이 때 $G'(t) = g(t)$ 이다. 따라서,
$$
f(x,\,y)=G(b(x,\,y))-G(a(x,\,y))
$$
이고,
$$
\begin{align}
D_1f(x,\,y)&=D_1b(x,\,y)g(b(x,\,y))-D_1a(x,\,y)g(a(x,\,y)) \\
D_2f(x,\,y)&=D_2 b(x,\,y) g(b(x,\,y))-D_2 a(x,\,y)g(a(x,\,y))
\end{align}
$$
이다. 



<b>7. </b> 변수 $x$ 에 대한 함수 $y$ 가 방정식
$$
f(x,\,y)=0
$$
을 만족시킬 때,
$$
D_1 f(x,\,y)+D_2 f(x,\,y)\dfrac{dy}{dx}=0
$$
임을 보이라. (이 문제에서 함수 $y$ 와 $f$ 가 모두 미분가능하다고 가정한다.)

---

$X(x)=(x,\, y(x))$, $f(X(x))=0$ 이므로,
$$
0=\dfrac{d}{dx} f(X(x))=\nabla f(X(x))\cdot \left( 1,\, \dfrac{dy}{dx}\right)=D_1 f(x,\,y)+ D_2 f(x,\,y)\dfrac{dy}{dx}
$$


<b>8.</b> $x^2+y^2=1$ 이고 $y \ne 0$ 일 때, $\dfrac{dy}{dx}=-\dfrac{x}{y}$ 임을 보여라.

---

$f(x,\,y)=1-x^2-y^2$ 으로 놓고 7 번의 결과를 이용하면,
$$
-x -y \dfrac{dy}{dx}=0 \implies \dfrac{dy}{dx}=-\dfrac{x}{y}
$$
이다. 



<b>9. </b> $x^3+x^2y+xy^2+y^3=1$ 일 때 $\dfrac{dy}{dx}(1)$ 을 구하라.

---

$f(x,\, y ) = x^3+x^2y+xy^2+y^3-1$ 일 때 $f(x,\,y)=0$ 을 만족한다. $x=1$ 이면 $y^3+y^2+y=0$ 이므로 $y=0$ 이다. 역시 문제 7의 결과를 이용하면,
$$
(3x^3+2xy+y^2)+(x^2+2xy+3y^2)\dfrac{dy}{dx}=0 \implies \dfrac{dy}{dx}(1)=-\dfrac{3}{1}=-3
$$
이다.



<b>10. </b> 독도 근방의 바다에서 (경도, 위도)- 좌표를 $(x,\,y)$ 라 하자. 어느날 이 근방의 해수 온도가 $f(x,\,y)\, ({}^\circ \text{C})$ 라고 하자. 이때 바다 지점 $(x_0,\, y_0)$ 에서 동쪽으로 움직일 경우 순간 온도 변화율이 $+1\, (^\circ \text{C/rad})$ 이고, 북쪽으로 움직일 경우 순간 온두 변화율이 $-1\, (^\circ \text{C/rad})$ 라고 하자. 만약 독도 근방을
$$
x(t)=x_0 +2(t-t_0),\qquad y(t)=y_0 +3\sin (t-t_0)
$$
과 같이 배회하는 선박이 지점 $(x_0,\,y_0)$ 를 지날 때 순간 온도 변화율은 얼마인가?

---

$\dfrac{df}{dx}(x_0,\,y_0)=+1$, $\dfrac{df}{dy}(x_0,\, y_0)=-1$ 이며 $X(t)=(x(t),\, y(t))$ 라 할 때,
$$
f'(X(t))=\nabla f(X(t_0))\cdot X'(t_0)=(1,\,-1)\cdot(2,\, 3)=-1
$$


<b>11. </b> 다음 함수에서 $x,\,y$ 에 대한 편도함수를 구하라.

---

(1) $f(u,\,v)=(u-v)e^u,\qquad u=xy,\qquad v=x^2-y^2$
$$
\begin{align}
\dfrac{\partial f}{\partial x} &= \dfrac{\partial f}{\partial u}\dfrac{\partial u}{\partial x}+ \dfrac{\partial f}{\partial v}\dfrac{\partial v}{\partial x}=(u-v+1)e^u y-e^u (2x)=(xy^2-x^2y+y^3+y-2x)e^{xy}\\
\dfrac{\partial f}{\partial y} &=\dfrac{\partial f}{\partial u}\dfrac{\partial u}{\partial y}+ \dfrac{\partial f}{\partial v}\dfrac{\partial v}{\partial y} =(u-v+1)e^ux+e^u (2y)=(x^2y-x^3+xy^2+x+2y)e^{xy}
\end{align}
$$
(2) $f(u,\,v) = u \ln v + v \ln u,\qquad u=\dfrac{y}{2}+\dfrac{2}{y},\qquad v=xe^y$
$$
\begin{align}
\dfrac{\partial f}{\partial x} &= \left( \ln v+\dfrac{v}{u} \right) \cdot 0 + \left(\dfrac{u}{v} + \ln u\right) e^y = \left[\dfrac{1}{xe^y}\left(\dfrac{y}{2}+\dfrac{2}{y}\right) + \ln \left(\dfrac{y}{2}+\dfrac{2}{y}\right)\right] e^y \\
\dfrac{\partial f}{\partial y} &= \left( \ln v+\dfrac{v}{u} \right) \left(\dfrac{1}{2}-\dfrac{2}{y^2}\right) + \left(\dfrac{u}{v} + \ln u\right) xe^y


\end{align}
$$
(3), (4) 번은 풀귀 귀찮아서..



<b>12. </b> $w=f(x-y,\, y-x)$ 일 때, $\dfrac{dw}{dx}+\dfrac{dw}{dy}=0$ 임을 보이라.

---

$u=x-y,\, v=y-x,\, w=f(u,\,v)$ 라 하면,
$$
\begin{align}
\dfrac{dw}{dx} &= \dfrac{dw}{du}\dfrac{du}{dx} + \dfrac{dw}{dv}\dfrac{dw}{dx}=D_1f(u,\,v) -D_2 f(u,\,v)\\
\dfrac{dw}{dy} &= \dfrac{dw}{du}\dfrac{du}{dy} + \dfrac{dw}{dv}\dfrac{dw}{dy}=-D_1(y,\,v)+D_2 f(u,\,v)

\end{align}
$$
이므로 $\dfrac{dw}{dx}+\dfrac{dw}{dy}=0$ 이다.



<b>13. </b> $w=x^3 f\left(\dfrac{y}{x},\, \dfrac{z}{x}\right)$ 일 때, $x\dfrac{\partial w}{\partial x}+ y \dfrac{\partial w}{\partial y}+z\dfrac{\partial w}{\partial z}=3w$ 임을 보이라.

---

$$
\begin{align}
\dfrac{\partial w}{\partial x} &=3x^2 f\left(\dfrac{y}{x},\, \dfrac{z}{x}\right)-xy D_1 f\left(\dfrac{y}{x},\, \dfrac{z}{x}\right)-xz D_2f\left(\dfrac{y}{x},\, \dfrac{z}{x}\right)\\
\dfrac{\partial w}{\partial y} &=x^2 D_1f\left(\dfrac{y}{x},\, \dfrac{z}{x}\right) \\
\dfrac{\partial w}{\partial z} &= x^2 D_2 f\left(\dfrac{y}{x},\, \dfrac{z}{x}\right)\\
 x\dfrac{\partial w}{\partial x}+ y \dfrac{\partial w}{\partial y}+z\dfrac{\partial w}{\partial z} &=
3x^3f\left(\dfrac{y}{x},\, \dfrac{z}{x}\right)-x^2yD_1f\left(\dfrac{y}{x},\, \dfrac{z}{x}\right) -x^2zD_2f\left(\dfrac{y}{x},\, \dfrac{z}{x}\right) \\
&\qquad +x^2y D_1f\left(\dfrac{y}{x},\, \dfrac{z}{x}\right) +x^2 z D_2f\left(\dfrac{y}{x},\, \dfrac{z}{x}\right) \\
&=3w
\end{align}
$$



<b>14. </b> $g(x,\,y)=f(x+y,\, x-y)$ 이고 $x+y=u,\, x-y=v$ 라 하자. 이때 다음이 성립함을 보이라.
$$
\dfrac{\partial g}{\partial x}\cdot \dfrac{\partial g}{\partial y}=\left(\dfrac{\partial f}{\partial u}\right)^2 - \left(\dfrac{\partial f}{\partial v}\right)^2
$$

---

$$
\begin{align}
\dfrac{\partial g}{\partial x}&=\dfrac{\partial f}{\partial u}\cdot 1+ \dfrac{\partial f}{\partial v}\cdot 1 \\
\dfrac{\partial g}{\partial y}&=\dfrac{\partial f}{\partial u}\cdot 1 + \dfrac{\partial f}{\partial v}\cdot (-1)


\end{align}
$$

이므로, 성립한다.



<b>15.  </b> 상수 $\theta$ 에 대하여 $x=u\cos \theta -v \sin \theta,\, y=u \sin \theta+v \cos \theta$ 라 하자. $f(x,\,y)=g(u,\,v)$ 일 때,
$$
\left(\dfrac{\partial g}{\partial u}\right)^2 + \left(\dfrac{\partial g}{\partial v}\right)^2 = \left(\dfrac{\partial f}{\partial x}\right)^2 +\left(\dfrac{\partial f}{\partial y}\right)^2 
$$
임을 보이라.

---

$$
\begin{align}
\dfrac{\partial g}{\partial u} &= \dfrac{\partial f}{\partial x}\dfrac{\partial x}{\partial u} + \dfrac{\partial f}{\partial y}\dfrac{\partial y}{\partial u}=\cos \theta\dfrac{\partial f}{\partial x} +\sin \theta \dfrac{\partial f}{\partial y}\\
\dfrac{\partial g}{\partial v} &= \dfrac{\partial f}{\partial x}\dfrac{\partial x}{\partial v} + \dfrac{\partial f}{\partial y}\dfrac{\partial y}{\partial v} =-\sin \theta \dfrac{\partial f}{\partial x}+ \cos \theta \dfrac{\partial f}{\partial y}

\end{align}
$$

이므로 주어진 식이 성립한다.



<b>16. </b> 미분가능한 일변수 함수 $g(r)$ 의 도함수가 영이 되지 않는다고 하자. 이때 함수
$$
f(X):=g(|X|) \qquad (X\in \mathbb{R}^3-O)
$$
의 기울기 벡터 $\nabla f(X)$ 는 $X$ 와 나란함을 보이라.

---

$$
\nabla f(X)=g'(|X|) (\nabla |X|) = \dfrac{g'(|X|)}{|X|}X
$$





<b>17. </b> 미분가능한 함수 $f(X)$ 의 기울기 벡터가 $X$ 와 나란하면
$$
\nabla f(X)=g(X)X
$$
인 함수 $g(X)$ 가 존재한다. 이 때 $f(X)$ 는 원점을 중심으로 하는 임의의 구면에서 상수임을 보이라.

---

반지름 $R$ 인 구면상의 임의의 일급 곡선 $X(t)$ 를 생각하자. $|X(t)|^2=R^2$ 이므로,
$$
X'(t) \cdot X(t) = 0
$$
이다. 이제 
$$
h(t) = f(X(t))
$$
라 하면,
$$
h'(t) = \nabla f(X(t))\cdot X'(t) = g(X(t))X(t) \cdot X'(t) = 0
$$
이므로 $h(t)=\text{const.}$ 이다. 



## 연습문제 제 10 장 6 절



<b>1. </b> 타원 
$$
\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}=1
$$
의 점 $(x_0,\,y_0)$ 에서의 접선의 방정식은
$$
\dfrac{x_0x}{a^2}+\dfrac{y_0y}{b^2}=1
$$
임을 보이라.

----

$f(x,\,y)=\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}-1$ 에서 $\nabla f(x_0,\,y_0)=\left(\dfrac{2x_0}{a^2}, \dfrac{2y_0}{b^2}\right)$ 이므로 접선 기울기는 $-\dfrac{2x_0/a^2}{2y_0/b^2}=-\dfrac{b^2x_0}{a^2y_0}$ 이다. 접선이 $(x_0,\,y_0)$ 를 지나므로,
$$
y-y_0 = -\dfrac{b^2x_0}{a^2y_0}(x-x_0) \implies \dfrac{x_0x}{a^2}+\dfrac{y_0y}{b^2}=\dfrac{x_0^2}{a^2}+\dfrac{y_0^2}{b^2}=1
$$


<b>2. </b> 쌍곡선 
$$
\dfrac{x^2}{a^2}-\dfrac{y^2}{b^2}=1
$$
의 점 $(x_0,\, y_0)$ 에서의 접선의 방정식은
$$
\dfrac{x_0x}{a^2}-\dfrac{y_0y}{b^2}=1
$$
임을 보이라.

----

$f(x,\,y)=\dfrac{x^2}{a^2}-\dfrac{y^2}{b^2}-1$ 에서 $\nabla f(x_0,\,y_0)=\left(\dfrac{2x_0}{a^2}, -\dfrac{2y_0}{b^2}\right)$ 이므로 접선 기울기는 $-\dfrac{2x_0/a^2}{2y_0/b^2}=-\dfrac{-b^2x_0}{a^2y_0}$ 이다. 접선이 $(x_0,\,y_0)$ 를 지나므로,
$$
y-y_0 = \dfrac{b^2x_0}{a^2y_0}(x-x_0) \implies \dfrac{x_0x}{a^2}-\dfrac{y_0y}{b^2}=\dfrac{x_0^2}{a^2}-\dfrac{y_0^2}{b^2}=1
$$


<b>3. </b> 다음 식으로 주어진 곡면의 점 $P$ 에서 접평면의 방정식을 구하라.

---

(1) $8x^2+y^2+8z^2=16,\qquad P=(1,\,2,\,1/\sqrt{2})$

$f(x,\,y,\,z)=8x^2+y^2+8z^2$ 이라 하면,
$$
\nabla f(P)=(16x,\, 2y,\, 16z)(P)=(16, 4, 8\sqrt{2})
$$
이므로 접평면의 방정식은
$$
16(x-1)+4(y-2)+8\sqrt{2} \left( z-\dfrac{1}{\sqrt{2}} \right)=16x+4y +8\sqrt{2} z-32=0
$$


(2) $x^2+y^2-z^2=4,\qquad P=(2,\,1,\,1)$

$f(x,\,y,\,z)=x^2+y^2-z^2$ 이라 하면,
$$
\nabla f(P)=(2x,\, 2y,\, -2z)(P)=(4,\,2,\, -2)
$$
이므로 접평면의 방정식은
$$
4(x-2)+2(y-1)-2(z-1)=4x+2y-2z-8=0
$$


(3) $ x^2+\dfrac{1}{4}y^2 - \frac{1}{9}z^2=1,\qquad P=(1,\,2,\,3)$

$f(x,\, y,\,z)= x^2+\frac{1}{4}y^2 - \frac{1}{9}z^2$ 라 하면,
$$
\nabla f(P)=\left( 2x,\, \dfrac{y}{2},\,-\dfrac{2z}{9} \right)(1,\,2,\,3)=(2, 1, -\dfrac{2}{3})
$$
이므로 접평면의 방정식은
$$
2(x-1)+(y-2)-\dfrac{2}{3}(z-3)=2x+y-\dfrac{2}{3}z-2=0
$$


(4) $\sin xy + \sin yz + \sin zx = 1,\qquad P=(1,\, \pi/2,\,0)$

$f(x,\,y,\,z)=\sin xy + \sin yz + \sin zx $ 라 하면,
$$
\nabla f(P)=(y\cos xy + z \cos zx,\, x \cos xy+ z \cos yz,\, y \cos yz+x \cos zx )(1,\, \pi/2 ,\, 0)=(0, 0, \pi/2+1)
$$
이므로 접평면의 방정식은
$$
\left(\dfrac{\pi}{2}+1\right)z=0 \implies z=0
$$
이다.



(5) $z-e^x \sin y=0,\qquad P=(\ln 3,\, 3\pi/2,\, -3)$

$f(x,\,y,\,z)=z-e^x\sin y$ 라 하면,
$$
\nabla f(P)=(-e^x \sin y,\, -e^x \cos y ,\, 1)(\ln 3,\, 3\pi/2,\, -3)=(3,\, 0,\, 1)
$$
이므로 접평면의 방정식은
$$
3(x-\ln 3)+ (z+3)=3x+z-3\ln 3 + 3=0
$$
이다.



(6) $2y-z^3-3xz=0,\qquad P=(1,\,7,\,2)$ 

$f(x,\,y,\,z)=2y-z^3-3xz$ 라 하면,
$$
\nabla f(P)=(-3z,\, 2,\, -3x-3z^2)(1,\,7,\,2)=(-6,\, 2,\, -15)
$$
이므로 접평면의 방정식은
$$
-6(x-1)+2(y-7)-15(z-2)=-6x+2y-15z+10=0
$$
이다. 



(7) $x^3-2y^2+z^2=0,\qquad P=(1,\,1,\,1)$

$f(x,\,y,\,z)=x^3-2y^2+z^2$ 으로 잡으면,
$$
\nabla f(P)=(3x^2,\, -4y,\, 2z)(1,\,1,\,2)=(3,\, -4,\,4)
$$
이므로 접평면의 방정식은
$$
3(x-1)-4(y-1)+4(z-1)=3x-4y+4z-3=0
$$
이다. 



<b>4.</b> 쌍곡면 
$$
\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}-\dfrac{z^2}{c^2}=1
$$
의 점 $(x_0,\,y_0,\, z_0)$ 에서의 접평면의 방정식을 구하라. 또 쌍곡면
$$
\dfrac{x^2}{a^2}-\dfrac{y^2}{b^2}-\dfrac{z^2}{c^z}=1
$$
의 접평면의 방정식은 어떻게 주어지는가?

----

$f(x,\,y,\,z)=\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}-\dfrac{z^2}{c^2}$ 라 하면,
$$
\nabla f(x_0,\,y_0,\,z_0)=\left(\dfrac{2x_0}{a^2},\, \dfrac{2y_0}{b^2},\, -\dfrac{2z_0}{c^2}\right)
$$
이므로 접평면의 방정식은,
$$
\begin{align}
&\dfrac{2x_0}{a^2}(x-x_0)+\dfrac{2y_0}{b^2}(y-y_0)-\dfrac{2z_0}{c^2}(z-z_0)=0\\
\implies & \dfrac{x_0}{a^2}x+\dfrac{y_0}{b^2}y-\dfrac{z_0}{c^2}z=\dfrac{x_0^2}{a^2} + \dfrac{y_0^2}{b^2}-\dfrac{z_0^2}{c^2}=1\\
\implies & \dfrac{x_0}{a^2}x+\dfrac{y_0}{b^2}y-\dfrac{z_0}{c^2}z=1

\end{align}
$$
로 주어진다. 

$g(x,\,y,\,z)=\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}-\dfrac{z^2}{c^2}$ 위의 점 $(x_0,\, y_0,\,z_0)$ 에서의 접평면의 방정식을 같은 방법으로 풀면,
$$
\dfrac{x_0}{a^2}x-\dfrac{y_0}{b^2}y-\dfrac{z_0}{c^2}z=1
$$
이다. 



