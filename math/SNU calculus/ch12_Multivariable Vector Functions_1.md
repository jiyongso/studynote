Chapter 12. Multivariable Vector Functions #1
===



## 연습문제 : 제 12 장 1 절



<b>1. </b> 구면좌표 변환의 부피 변화율이 야코비 행렬식과 일치함을 보이라.

---

정의역의 한 cube 

$$
\rho_0 \le \rho \le \rho_0 + \Delta\rho,\qquad \varphi_0 \le \varphi\le \varphi_0+\Delta \varphi,\qquad \theta_0 \le \theta \le \theta_0 +\Delta \theta
$$

가 구면좌표변환에 의하여 부피의 변화가 어떻게 변하는지 보면 된다. 일단 고정된 $\rho$ 에서의 면적의 변화를 보면 $\varphi$ 방향으로는 $\rho \Delta \varphi $ 이며 $\theta$ 방향으로는 $\rho\sin \varphi \Delta \theta$ 이므로 면벅의 변화는 $\rho^2 \sin \varphi \Delta \varphi \Delta \theta$ 이다. 

부피의 변화 $\Delta V$ 는

$$
\begin{aligned}
\Delta V &\approx \dfrac{1}{3} \left((\rho_0 +\Delta\rho)^3-(\rho_0)^3\right) \sin \varphi \Delta \varphi \Delta \theta \approx \rho^2\sin \varphi \Delta \varphi \Delta \theta = \det \dfrac{\partial(x,\,y,\,z)}{\partial (\rho,\, \varphi,\,\theta)}
\end{aligned}
$$ {d}


<b>2. </b> 사상 
$$
\begin{aligned}
F(x,\, y)&=(x^2-y^2,\, 2xy) \\
G(x,\,y) &=(x^3-xy^2,\, x^2y-y^3)
\end{aligned}
$$
의 야코비 행렬과 행렬식을 구하라.

---

$$
\begin{aligned}
F'(x,\,y) &= \begin{pmatrix} 2x & 2y \\ 2y & 2x\end{pmatrix} \\
\det F'(x,\,y)&= 4x^2-4y^2\\
G'(x,\,y) &= \begin{pmatrix} 3x^2-y^2 & -2xy \\ 2xy & x^2-3y^2 \end{pmatrix} \\
\det G'(x,\,y) &= 3x^4-10x^2y^2+3y^4+4x^2y^2=3(x^2-y^2)^2


\end{aligned}
$$



나머지는 지루함..



## 제 2 절 : 역함수 정리와 음함수 정리



#### 미분가능한 역함수와 역함수의 미분

$F: X \subset \mathbb{R}^n \to Y\subset \mathbb{R}^n$ 에 대한 역함수 $G:Y \to X$ 가 존재한며 $G$ 가 미분가능하면 $G'(Y)=\left(F'(X)\right)^{-1}$ 이다. 

---

$$
G(F(X))=X \implies G'(Y)F'(X)=I \implies G'(Y)=\left(F'(X)\right)^{-1}
$$





#### 역함수 정리

$n$ 공간의 한 열린 집합에서 정의된 일급사상 $F:U\subset \mathbb{R}^n\to \mathbb{R}^n$ 을 생각하자. $X_0 \in U$ 에 대해 $F'(X_0)$ 가 가역행렬이면 $F$ 는 $X_0$ 의 어떤 근방에서 국소적으로 일급가역이다. 이 때 $F$ 의 국소 역사상을 $G$ 라 하고 $Y_0=F(X_0)$ 라 하면
$$
G'(Y_0)=(F'(X_0))^{-1}
$$
이다. 

---

증명은 해석학 참고



#### 음함수 정리

일급함수 $f(x_1,\ldots,\,x_n,\,y)$ 의 등위면 $f^{-1}(c)$ 의 한 점 $P_0:=(X_0,\,y_0)=(x_1^0,\ldots,\,x_n^0,\,y_0)$ 에서
$$
\dfrac{\partial f}{\partial y}(P_0) \ne 0
$$
이면 $f^{-1}(c)$ 는 점 $P_0$ 근방에서 어떤 일급함수 
$$
y=g(x_1,\ldots,\,x_n)
$$
의 그래프이다. 이 때
$$
\dfrac{\partial g}{\partial x_j}(X_0)=-\dfrac{\partial f}{\partial x_j}(P_0){\huge /}\dfrac{\partial f}{\partial y}(P_0)
$$
이다. 

---

$n=1$ 인 경우만 다룬다. $n\ge 2$ 의 증명은 유사하다. $F(x,\,y)=(x,\,f(x,\,y))$  의 야코비 행렬
$$
F'(x,\,y)&=\begin{bmatrix} 1 & 0 \\ \partial_x f (x,\,y) & \partial_y f(x,\,y)\end{bmatrix}
$$
에 대해 $\det F'(x,\,y)=\partial_y f(x,\,y)\ne 0$ 이므로 $F$ 는 역함수정리에 의해 점 $(x_0,\,y_0)$ 근방에서 역함수 $G=G(g_1,\,g_2)$ 를 가지며
$$
x=g(x,\, f(x,\,y))\qquad y=g_2(x,\, f(x,\,y))
$$
$f(x,\,y)=c$ 이면 $y=g_2 (x,\,c)=g(x)$ 이다. 

$f(X,\,g(X))=c$ 이므로 연쇄법칙을 이용하면
$$
\partial_j f(X,\, g(X))+\partial_y f(X,\, g(X))\partial_j g(X)=0 \implies \partial_j g(X_0)=-\dfrac{\partial_j f(P_0)}{\partial_y f(P_0)}
$$
이다.







## 연습문제 : 제 12 장 2 절



<b>1. </b> 사상
$$
(u,\,v):=F(x,\,y)=(x^3-3xy^2,\, 3x^2y-y^3),\qquad (x,\,y)\ne (0,\,0)
$$

은 국소적으로 가역사상임을 보이라. 이 때 점 $(x,\,y)=(1,\,0)$ 에서 역사상 $G(u,\,v)$ 의 미분을 구하라.

---

$$
F'(x,\,y)= \begin{bmatrix} 3x^2-3y^2 & -6xy \\ 6xy & 3x^2-3y^2\end{bmatrix},\qquad \det F'=9(x^2+y^2)^2
$$

이므로 $(x,\,y)\ne (0,\,0) \iff \det F'\ne 0$ 이다. 따라서 $(x,\,y)\ne (0,\,0)$ 일 때 $F$ 는 국소적으로 가역사상이다. 
$$
F'(1,\,0)=\begin{bmatrix} 3 & 0 \\ 0 & 3\end{bmatrix}\implies G'(1,\,0)=F'^{-1}=\begin{bmatrix} 1/3 & 0 \\ 0 & 1/3\end{bmatrix}
$$


<b>2. </b> 다음 함수들이 주어진 점에서 국소적으로 일급가역인가를 조사하라.

---

(1) $F(x,\,y)=(x+y,\, y^{1/4}),\qquad (x_0,\,y_0)=(1,\,2)$
$$
F'(x,\,y)= \begin{bmatrix} 1 & 1 \\ 0 & \frac{1}{4} y^{-3/4}\end{bmatrix},\qquad F'(x_0,\,y_0) =\begin{bmatrix} 1 & 1 \\ 0 & \frac{1}{4\cdot 2^{3/4} }\end{bmatrix} \implies \det F''(x_0,\,y_0) \ne 0
$$
따라서 국소적으로 일급가역이다.



(2) $F(x,\,y )= \dfrac{(x,\,y)}{(x^2+y^2)},\qquad (x_0,\,y_0)\ne (0,\,0)$
$$
\begin{aligned}
F'(x,\,y)&=\dfrac{1}{x^2+y^2} \begin{bmatrix} -x^2+y^2 & -2y^2 \\ -2x^2 & x^2-y^2 \end{bmatrix}  \\
\det F'(x,\,y) &= -(x^2+y^2)
\end{aligned}
$$
이므로 주어진 조건에서 일급가역이다.



<b>3. </b> $f(x,\,y):=(x-2)^2y-xe^y$ 일 때
$$
f(a,\,b)=0,\qquad D_2 f(a,\,b)=0
$$
인 점 $(a,\,b)$ 를 구하라.

---

$$
\nabla f = (2(x-2)y-e^y,\, (x-2)^2-xe^y)
$$

를 풀면 $a=\dfrac{e+4\pm \sqrt{e^2+8e}}{2},\, b=1$  이다. 



<b>4. </b> 다음 함수 $f$ 에 대하여 식 $f(x,\,y)=0$ 으로 주어진 등위선은 점 $(x_0,\,y_0)$ 근방에서 함수 $y=g(x)$ 의 그래프로 나타남을 설명하고, 이때 미분계수 $g'(x_0)$ 를 구하라.

---

(1) $f(x,\,y)=x^2-xy+y^2-3,\quad (x_0,\,y_0)=(1,\,2)$

$F(x,\,y)=(x,\,f(x,\,y))$ 라 놓을 때, 
$$
F'(x,\,y)=\begin{bmatrix} 1 & 0 \\ 2x-y & -x+2y \end{bmatrix},\qquad \det F'(1,\,2)=\det \begin{bmatrix} 1 & 0 \\ 0 & 3 \end{bmatrix}=3
$$
이므로 음함수 정리에 의해 $(1,\,2)$ 근처에서 $y=g(x)$ 의 그래프로 나타난다. 
$$
g'(1)=-\dfrac{0}{3}=0
$$


(2) $f(x,\,y)=x \cos (xy),\qquad (x_0,\,y_0)=(1,\,\pi/2)$ 

$\partial_y f (x_0,\,y_0)=-1\ne 0$ 이므로 $(x_0,\,y_0)$ 근방에서 $y=g(x)$ 의 그래프로 나타난다.  $\partial_x f(x_0,\,y_0)=-\frac{\pi}{2}$ 이므로,
$$
g'(1) = \dfrac{\pi}{2}
$$
이다.



(3) $f(x,\,y) = 2e^{x+y}-x+y,\qquad (x_0,\,y_0)=(1,\,-1)$ 

$\partial_y f(x_0,\,y_0)= 3\ne 0$, $\partial_x f(x_0,\,y_0)=1$ 이므로 $g(1)= -\frac{1}{3}$ 이다.



(4) $ f(x,\,y)=x+y+x\sin y,\qquad (x_0,\,y_0)=(0,\,0)$

$\partial_y f(0,\,0)= 1 \ne 0,\, \partial_x f(0,\,0)= 1$ 이므로 $g(1)=-1$ 이다.



<b>5. </b> 다음 함수 $f$ 에 대하여 식 $f(x,\,y,\,z)=0$ 으로 주어진 등위면은 주어진 점 $(x_0,\,y_0,\,z_0)$ 근방에서 함수$z=g(x,\,y)$ 의 그래프로 나타남을 설명하고, 이때 미분계수 $D_1 g(x_0,\,y_0)$ 와 $D_2 g(x_0,\,y_0)$ 를 구하라.

---

(1) $f(x,\,y,\,z)=x+y+z + \cos xyz,\qquad (x_0,\,y_0,\,z_0)=(0,\,0,\,-1)$

$\partial_z f(x_0,\,y_0,\,z_0)= 1 \ne 0$ 이므로 $(x_0,\,y_0,\,z_0)$ 근처에서 $z=g(x,\,y)$ 의 그래프로 나타난다. $\partial_x f(x_0,\,y_0,\,z_0)= 1$, $\partial_y f (x_0,\,y_0,\,z_0)=1$ 이므로 $D_1 g(0,\,0)=-1,\, D_2 g(0,\,0)=-1$ 이다.



(2)-(4) 도 같은 방법으로 풀 수 있다.



<b>6. </b> 식 
$$
xe^y-y+1=0
$$
으로 주어진 집합은 점 $(e^{-2},\, 2)$ 근방에서 함수의 그래프로 나타나는가?

---

$f(x,\,y)=xe^y-y+1$ 일 때 $\partial_y f(e^{-2},\, 2)= 0$ 이므로 함수의 그래프로 나타나지 않는다.  거꾸로 $x=h(y)$ 로 나타낼 수 있는지 보기 위해 $\partial_x f(e^{-2},\,2)= e^2\ne 0$ 이므로 $x=h(y)$ 의 그래프로 나타 낼 수 있다.



<b>7. </b> 좌표평면에서 정의된 함수 $z=f(x,\,y)$ 가 식
$$
x^3+y^3+z^3+3xyz=6
$$
을 만족시킨다고 하자. 이 때 점 $(1,\,1)$ 에서 $f$ 의 기울기 벡터 $\nabla f(1,\,1)$ 을 구하라.

---

$g(x,\,y,\,z)=x^3+y^3+z^3+3xyz$ 라 하자. $g(1,\,1,\,z)=6$ 을 만족하는 $z$ 는 $z=1$ 뿐임을 쉽게 알 수 있다. 

$\partial_z g(1,\,1,\,1)=6\ne 0$ 이다. $g_x (1,\,1,\,1)= g_y (1,\,1,\,1)=1$ 이므로 $\nabla f(1,\,1)=(-1,\,-1)$ 이다.



<b>8. </b> 방정식
$$
x^5+2x^3+x+c=0
$$
에 대하여 다음에 답하라.

(1) 임의의 실수 $c$ 에 대하여 위 방정식은 오직 하나의 실근을 가짐을 보이라.

(2) 이 방정식의 근을 $g(c)$ 로 두었을 때 $g'(0), \, g''(0)$ 의 값을 구하라.

---

(1) $f(x) = x^5+2x^3+x+c=0$ 이라 했을 때 $f'(x)=5x^4+6x^2+1>0$ 이므로 $f$ 는 단조증가 함수이다. $\displaystyle \lim_{x\to -\infty}f(x) = -\infty\, \lim_{x \to \infty} f(x)=\infty$ 이므로 $f(x)=0$ 의 실근은 오직 하나 뿐이다.

(2) $h(x,\,y)=x^5+2x^3+x+y$ 라 했을 때 $h(x,\,y)=0$ 을 만족하는 $x,\,y$ 에 대해  $\partial_x h(x,\,y)>0$ 이므로 $x=g(y)$ 인 $g$ 가 존재한다. 이 때 $g(c)$ 는 $h(x,\, c)=0$ 의 근이며 $c=0$ 일 때의 근은 $x=0$ 이다. $g'(0)=-\partial_y h(0,\,0)/\partial_x h(0,\,0)=-1$ 이다. 

$g'(y) = -\dfrac{1}{5x^4+6x^2+1}$ 이므로,
$$
g''(y)=\dfrac{20x^3+12x}{(5x^4+6x^2+1)^2}\cdot \dfrac{dg}{dy} \implies g''(0)=0
$$


<b>9. </b> 방정식 
$$
x^3+ax-10=0
$$
은 $a>0$ 일 때 오직 하나의 실근을 가진다. 이 실근을 $g(a)$ 로 둘 때, $g'(1)$ 과 $g''(1)$ 을 구하라.

---

$f(x,\,y)=x^3+xy-10$ 이라 하자. $\nabla f (x,\,y)=(3x^2+y,\, x)$ 이며 $y>0$ 일 때 $x=g(y)$ 인 그래프가 존재한다. $y=1$ 일 때 가능한 $f(x,\,1)=0$ 의 해 는 $x=2$ 뿐이다. 음함수의 정리를 이용하면
$$
\begin{aligned}
g'(1) &= -\partial_y f(2,\,1)/\partial_x f (2,\,1)=-\dfrac{2}{13} \\
g'(y) &= -\dfrac{x}{3x^2+y} =-\dfrac{g(y)}{3g(y)^2+y}\\
g''(y) &= -\dfrac{g'(y)}{3g(y)^2+y}+ \dfrac{6g(y)^2g'(y) + g(y)}{(3g(y)^2+y)^2} \\
g''(1) &= -\dfrac{20}{169}
\end{aligned}
$$
 

<b>10.</b> 다음 주장에서 잘못된 곳을 가려라

> $x$ 에 관한 함수 $y$ 가 $y^3=x(x-1)(x-2)$ 로 주어졌을 때, 이 식을 $x$ 에 관해 미분하면, 
> $$
> 3y^2y'=(x-1)(x-2)+x(x-2)+x(x-1)
> $$
> 을 얻는다. 이 식의 양변에 $x=0$ 을 대입하면 $0=2$ 를 얻는다.

---

$y=\left(x(x-1)(x-2)\right)^{1/3}$ 이므로,
$$
y'=\dfrac{x(x-1)+x(x-2)+(x-1)(x-2)}{[x(x-1)(x-2)]^{2/3}}
$$
이며 $y'(0)$ 은 정의되지 않는다.



<b>11. </b> $(x,\,y)$ 에 대한 함수 $z$ 가 식 $x^3-2y^2+z^2=0$ 을 만족시킬 때, $\dfrac{\partial z}{\partial x}(1,\,1)$ 과 $\dfrac{\partial z}{\partial y}(1,\,1)$ 을 구하라.

---

$f(x,\,y,\,z)=x^3-2y^2+z^2$ 이라 할 때 $x=1,\,y=1$ 에 대해 가능한 $f(x,\,y,\,z)=0$ 의 $z$ 값은 $\pm 1$ 이다. 또한 이때 $\partial_z f(1,\,1,\, 1)=2\ne 0,\, \partial_z f(1,\,1,\,-1)=-2\ne 0$ 이 므로 각각의 경우에 대해 $z=g_1(x,\,y),\, g_2(x,\,y)$ 인 그래프가 존재한다. 
$$
\nabla f(x,\,y,\,z)=(3x^2,\, -4y,\, 2z)
$$
임을 이용한다. 

1) $(1,\,1,\,1)$  근처에서, $\partial_x g_1 (1,\,1)=-\dfrac{\partial_x f(1,\,1,\,1)}{\partial_z f(1,\,1,\,1)}=-\dfrac{3}{2},\, \partial_y g_1 (1,\,1)=-\dfrac{\partial_y f(1,\,1,\,1)}{\partial_z f(1,\,1,\,1)}=2$

2. $(1,\,1,\,-1)$ 근처에서 $\partial_x g_2 (1,\,1)=-\dfrac{\partial_x f(1,\,1,\,-1)}{\partial_z f(1,\,1,\,-1)}=-\dfrac{3}{2},\, \partial_y g_2 (1,\,1)=-\dfrac{\partial_y f(1,\,1,\,1)}{\partial_z f(1,\,1,\,1)}=-2$



<b>12. </b> $y^5+3x^2y^3-7x^6-8=0$ 일 때 $\dfrac{dy}{dx}(0)$ 을 구하라.

---

$f(x,\,y)=y^5+3x^2y^3-7x^6-8$ 이라 할 때, $x=0,\, y = 2^{3/5}$ 만이 $f(x,\,y)=0$ 을 만족한다. 
$$
\nabla f(x,\,y)=(6xy^3-42x^5,\, 5y^4+9x^2y^2)
$$
이며 $\partial_y f(0,\, 2^{3/5})=5\times 2^{12/5}>0$ 이므로 $(0,\, 2^{3/5})$ 근처에서  $y=g(x)$ 가 존재한다. 그렇다면,
$$
\dfrac{dy}{dx}(0)=-\dfrac{\partial_x f(0,\, 2^{3/5})}{\partial_y f(0,\,2^{3/5})}= 0
$$
이다. 



<b>13. </b> 만약 $n$ 차 정사각행렬 $A$ 가 항등행렬 $I$ 에 아주 가까우면, $e^X=A$ 가 되는 정사각행렬 $X$ 가 존재함을 설명하라. 이때 임의의 자연수 $k$ 에 대하여 $Y^k=A$ 가 되는 정사각행렬 $Y$ 가 존재함을 보이라.

---

]
