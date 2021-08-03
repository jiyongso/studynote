XI. 최대최소값 문제와 고계미분 #1
===



## 연습문제 : 제 11 장 1 절



<b>1. </b> $x>0$ 일 때 다음 미분을 구하라.
$$
\dfrac{d}{dx} \int_{x^2}^{x^3} \dfrac{1}{y} e^{xy^2} \, dy
$$

---

$$
F(x,\, t) = \int_{a}^t \dfrac{1}{s}e^{xs^2}\, ds
$$

라 하면
$$
\int_{x^2}^{x^3}\dfrac{1}{y} e^{xy^2}\, dy = F(x,\, x^3)-F(x,\,x^2)
$$
이며,
$$
\begin{aligned}
\dfrac{d}{dx} \int_{x^2}^{x^3} \dfrac{1}{y} e^{xy^2} \, dy  &= D_1F(x,\, x^3)+3x^2D_2F(x,\,x^3)-D_1F(x,\,x^2)-2xD_2F(x,\,x^2)\\
&=\int_{a}^{x^3} se^{xs^2}ds+3x^2 \dfrac{1}{x^3}e^{x^7}-\int_a^{x^2} se^{xs^2}\, ds-2x \dfrac{1}{x^2}e^{x^5} \\
&=\left[\dfrac{1}{2x}e^{xs^2}\right]_{x^2}^{x^3}+\dfrac{3}{x}e^{x^7}-\dfrac{2}{x}e^{x^5} \\
&=\dfrac{1}{2x}e^{x^7}-\dfrac{1}{2x}e^{x^5} + \dfrac{3}{x}e^{x^7}-\dfrac{2}{x}e^{x^5}\\
&=\dfrac{7}{2x}e^{x^7}-\dfrac{5}{2x}e^{x^5}
\end{aligned}
$$
이다.



<b>2. </b> 일급함수 $a(x),\, b(x),\, g(x,\,y)$ 에 대하여
$$
\dfrac{d}{dx} \int_{a(x)}^{b(x)} g(x,\,y)\, dy = g(x,\,b(x))b'(x)-g(x,\,a(x))a'(x)+\int_{a(x)}^{b(x)}D_1g(x,\,y)\, dy
$$
임을 보이라.

---

앞의 1과 같은 방법으로,
$$
F(x,\,t):=\int_c^t g(x,\,y)\, dy
$$
라 하면,
$$
\begin{aligned}
\int_{a(x)}^{b(x)}g(x,\,y)\, dy &= F(x,\,b(x))-F(x,\, a(x)) \\
D_1F(x,\,t)&=\int_c^t \frac{\partial g}{\partial x}(x,\,y)\, dy = \int_c^t D_1 g(x,\,y)\,dy \\
D_2F(x,\,y)&= g(x,\,y)
\end{aligned}
$$
이므로,
$$
\begin{aligned}
\dfrac{d}{dx} \int_{a(x)}^{b(x)}g(x,\,y)dy &= \dfrac{d}{dx} \left[F(x,\,b(x))-F(x,\,a(x)\right] \\
&= D_1F(x,\,b(x)) +D_2F(x,\, b(x))b'(x)-D_1F(x,\,a(x))-D_2F(x,\,a(x))a'(x) \\
&=g(x,\,b(x))b'(x)-g(x,\,a(x))a;(x)+\int_{a(x)}^{b(x)} D_1 g(x,\,y)\, dy
\end{aligned}
$$
이다.



<b>3. </b> $k<1$ 일 때 함수
$$
f(k):=\int_0^{\pi/2} \dfrac{dx}{\sqrt{1-k\cos^2x}}
$$
는 $k$ 에 대한 증가함수 임을 보이라. 또 $k=0$ 일 때의 순간변화율은 얼마인가?

---

$$
\begin{aligned}
\dfrac{df(k)}{dk} &=\int_0^{\pi/2}\dfrac{\partial}{\partial k}\left( \dfrac{1}{\sqrt{1-k\cos^2 x}}\, \right)dx  = \int_0^{\pi/2} \dfrac{\cos^2 x}{2(1-k\cos^2x)^{3/2}}\, dx
\end{aligned}
$$

이며 $1-k\cos^2 x>0$ , $\cos^2 x>0$ 이므로 $f'(k)>0$  이다. 따라서 $f(k)$ 는  $k$ 에 대한 증가함수이다.

$k=0$ 일 때의 순간변화율은
$$
\dfrac{df}{dk}(0)= \int_0^{\pi/2}\dfrac{1}{2}\cos^2x\, dx= \dfrac{\pi}{8}
$$


<b>4. </b> 좌표평면에서 호의 길이로 매개화된 이급 곡선
$$
C(s),\qquad s_0\le s \le s_1
$$
에 대하여 단위 접벡터를
$$
\mathbf{t}(s) : =C'(s)
$$
로 두면 이 곡선의 각 점에서 곡률은
$$
\kappa (x) := |\mathbf{t}'(s)|
$$
로 주어진다. 이때 곡선  $C(s)$ 를 단위법벡터
$$
\mathbf{n}(s) := -\dfrac{\mathbf{t}'(s)}{\kappa(s)}
$$
방향으로 $u$ 만큼 이동한 곡선의 식은
$$
C_u(s):=C(s)+u\mathbf{n}(s),\qquad s_0\le s\le s_1
$$
이다. 곡선 $ C_u$ 의 길이를
$$
L(u):=\int_{s_0}^{s_1}\left|C'_u(s)\right|\, ds
$$
라 하자.

(1) $\mathbf{n}'(s)=\kappa (s) \mathbf{t}(s)$ 임을 보이라.

(2) $|u|\ll 1$ 이면 $ L(u)$ 의 순간변화율은 처음 주어진 곡선의 전곡률 임을, 즉
$$
L'(u)=\int_{s_0}^{s_1}\kappa (s)\, ds
$$
를 보이라.

(3)  만약 처음에 주어진 곡선 $ C$ 가 타원이면  $L'(0)$ 의 값은 얼마인가?

---

(1)  $|\mathbf{t}(s)|=1,\,|\mathbf{n}(s) |=1$​ 이다. 이로부터,
$$
\begin{aligned}
\dfrac{d}{ds}\left|\mathbf{t}(s)\right|^2 &=0 \implies \mathbf{t}(s) \cdot \mathbf{t}'(s)=0 \\
\dfrac{d}{ds}\left|\mathbf{n}(s)\right|^2 &=0 \implies \mathbf{n}(s) \cdot \mathbf{n}'(s)=0 
\end{aligned}
$$
좌표평면이므로 2차원이고, $\mathbf{n}(s) \propto \mathbf{t}'(s)$ 이므로, $\mathbf{n}'(s) \propto \mathbf{t}(s)$ 이다. 따라서 어떤 스칼라 함수 $ f(s)$ 에 대해
$$
\mathbf{n}'(s) =f(s)\mathbf{t}(s) \tag{1}
$$
 이다. 또한, $\mathbf{n}(s) \cdot \mathbf{t}(s)=0$ 이므로, 
$$
\begin{aligned}
\mathbf{n}'(s)\cdot \mathbf{t}(s) &=\left(\mathbf{n}(s) \cdot \mathbf{t}(s)\right)'-\mathbf{n}(s)\cdot \mathbf{t'(s)} =0-(-\kappa(s))=\kappa(s)
\end{aligned}
$$
이며, (1) 로 부터,
$$
\mathbf{n'}(s)\cdot \mathbf{t}(s) = f(s) |\mathbf{t}(s)|^2=f(s)
$$
이므로 $ f(s)=\kappa (s)$ 이다. 즉,
$$
\mathbf{n}'(s) = \kappa (s) \mathbf{t}(s)
$$
이다.

(2) 
$$
|C'_u(s)| = |C'(s)+u\mathbf{n'(s)}|=|\mathbf{t}(s)+u\kappa(s)\mathbf{t}(s)|=|\mathbf{t}(s)|\cdot |1+u\kappa(s)|=|1+u\kappa(s)|
$$
이다 .$|u|\ll 1$​ 이면  $1+u\kappa(s)>0$​ 이므로,
$$
\begin{aligned}
L(u) &= \int_{s_0}^{s_1} (1+u\kappa(s))ds\\
L'(u) &=\int_{s_0}^{s_1} \dfrac{\partial }{\partial u}(1+u\kappa(s))ds =\int_{s_0}^{s_1} \kappa(s)\, ds
\end{aligned}
$$
이다.

(3) 타원의 전곡률은  $2\pi$ 이다. (계산이 복잡해서...생략..)


## 연습문제 : 제 11 장 2 절

#### 편미분의 교환법칙

$n$-공간의 열린 집합 $A$ 에서 정의된 이급함수 $f$ 는 $P\in A$ 에 대하여 다음을 만족한다.
$$
D_i D_j f(P)=D_j D_i f(P) \qquad (1\le i,\,j \le n)
$$

---

이변수 함수 $f(x,\,y)$ 에 대해서만 보이면 된다. 우선 $A$ 에 포함되는 충분히 작은 직사각형 $[a,\,b]\times [c,\,d]$ 에 대하여
$$
\begin{aligned}
\int_c^y D_1 D_2 f(x,\,t)\, dt &=\dfrac{\partial }{\partial x} \int_{c}^y D_2 f(x,\,t)\, dt \\
&= \dfrac{\partial }{\partial x}\left(f(x,\,y)-f(x,\,c)\right)\\
&= D_1f(x,\,y)-D_1 f(x,\,c)
\end{aligned}
$$
이다. 이제 좌변을 $y$ 에 대해 미분 가능하며, 따라서 오른쪽도 $y$ 에 대해 미분가능하다. 따라서,
$$
D_1D_2 f(x,\,y) = D_2D_1 f(x,\,y)
$$
이다. $\square$



<br></br>
<b>1.</b> 다음 함수에서 $D_1D_2 f= D_2 D_1 f$ 가 성립하는가를 조사하라.

---
(1) $2x^2y^3 -x^3y^5$
$$
\begin{aligned}
D_1 D_2 f(x,\,y) &= D_1(6x^2y^2-5x^3y^4)=12xy^2-15x^2y^4 \\
D_2 D_1 f(x,\,y) &= D_2 (4xy^3-3x^2y^5) = 12xy^2-15x^2y^5
\end{aligned}
$$
따라서 $D_1D_2f=D_2D_1f$ 가 성립한다.


(2) $\cos^7 x - \sin ^2 y$
$$
\begin{aligned}
D_1D_2f(x,\,y) &= D_1(-2\cos y \sin y )=0 \\
D_2D_1 f(x,\,y) &=D_2 (-7 \sin x \cos^6 x)=0
\end{aligned}
$$
따라서 $D_1D_2f=D_2D_1f$ 가 성립한다.

(3) $\arctan(x y)$
$$
\begin{aligned}
D_1D_2 f(x,\,y) &= D_1 \dfrac{x}{1+x^2y^2} = \dfrac{1+x^2y^2-x(2xy^2)}{(1+x^2y^2)^2} = \dfrac{1-x^2y^2}{(1+x^2y^2)^2} \\
D_2D_1 f(x,\,y) &=D_2 \dfrac{y}{1+x^2y^2}=\dfrac{1-x^2y^2}{(1+x^2y^2)^2}
\end{aligned}
$$
따라서 $D_1D_2f=D_2D_1f$ 가 성립한다.


(4) $\ln \dfrac{x-1}{y+1}$
$$
\begin{aligned}
D_1D_2f(x,\,y) = D_2D_1f(x,\,y)=0
\end{aligned}
$$

<br></br>
<b>2.</b> 함수 $f(x,\,y)=xy^2+ye^{-x}\sin (x-y)$ 의 모든 이계편도함수를 구하라.

---

$$
\begin{aligned}
D_1 f(x,\,y) &=y^2-ye^{-x}\sin (x-y)+ye^{-x}\cos (x-y) \\
D_2 f(x,\,y) &=2xy+e^{-x}\sin (x-y)-ye^{-x}\cos(x-y) \\
{D_1}^2 f(x,\,y) &=ye^{-x}\sin (x-y) -ye^{-x} \cos (x-y)-ye^{-x}\cos (x-y) +ye^{-x} \sin (x-y) \\
&=2ye^{-x} (\sin (x-y) -\cos(x-y)) \\
D_2D_1 f(x,\,y) &= 2y-e^{-x}\sin (x-y) +ye^{-x}\cos (x-y) +e^{-x}\cos (x-y)+ye^{-x} \sin (x-y) \\
&= 2y+(y-1)e^{-x}\sin (x-y) + (y+1)e^{-x} \cos (x-y) \\
D_1D_2 f(x,\,y) &= 2y-e^{-x}\sin (x-y)+e^{-x}\cos (x-y)+ye^{-x}\cos (x-y)+ye^{-x} \sin (x-y) \\
&=2y+(y-1)e^{-x}\sin (x-y) + (y+1)e^{-x} \cos (x-y) \\
{D_2}^2 f(x,\,y) &=2x -e^{-x} \cos (x-y) -e^{-x}\cos (x-y) -ye^{-x} \sin (x-y) \\
&=2x-2e^{-x} \cos (x-y) -ye^{-x}\sin (x-y)
\end{aligned} 
$$


<br></br>

<b>3. </b> $z=\sin (x+ct)+\cos (2x+2ct)$ 일때
$$
\dfrac{\partial^2z}{\partial t^2}=c^2 \dfrac{\partial^2z}{\partial x^2}
$$
임을 보이라.

---

$$
\begin{aligned}
\dfrac{\partial z}{\partial t} &= c\cos (x+ct)-2c\sin (2x+2ct) \\
\dfrac{\partial z}{\partial x} &= \cos (x+ct)-2 \sin (2x+2ct) \\
\dfrac{\partial^2 z}{\partial t^2} &= -c^2\sin (x+ct) - 4c^2 \cos (2x+2ct) \\
\dfrac{\partial^2 z}{\partial x^2} &= -\sin (x+ct)-4 \cos (2x+2ct)
\end{aligned}
$$
이므로 주어진 식이 성립한다.

<br></br>
<b>4. </b> 이급함수 $f(x,\,y) $ 는 정의역의 각 점에서 임의의 벡터 $\mathbf{v}$ 에 대하여 $\mathbf{v}$ 방향 이계미분계수와 $(-\mathbf{v})$ 방향 이계미분계수가 같은가?

---
Let $\mathbf{v}=(a,\,b)$ Then,

$$
{D_{(a,\,b)}}^2f(x,\,y)=a^2{D_1}^2f(x,\,y)+2abD_2D_2f(x,\,y)+b^2{D_2}^2f(x,\,y) ={D_{(-a,\,-b)}}^2f(x,\,y)
$$


<b>5. </b> 원점 근방에서 정의된 삼급함수 $f(x,\,y)$ 가 원점에서 $\mathbf{v}$-방향 이계미분계수가 $1$ 이라고 하자. 이 때 $2\mathbf{v}$-방향 이계미분계수는 얼마인가? 또 $f(x,\,y)$ 가 원점에서 $\mathbf{v}$-방향 삼계미분계수가 $1$ 이면 $2\mathbf{v}$-방향 삼계미분계수는 얼마인가?

---
$$
\begin{aligned}
D_{2\mathbf{v}} f &= 2\mathbf{v} \cdot \nabla f=2D_{\mathbf{v}}f\\
{D_{2\mathbf{v}}}^2 & f= 2\mathbf{v} \cdot \nabla (2\mathbf{v} \cdot \nabla f) =4{D_{\mathbf{v}}}^2f \\
{D_{2\mathbf{v}}}^3 &f = 8 {D_{\mathbf{v}}}^3f
\end{aligned}
$$


<b>6. </b> 곡선 $(x_1(t),\ldots,\, x_n(t))$ 와 함수 $f(x_1,\ldots,\,x_n)$ 에 대하여,
$$
\dfrac{d^2}{dt^2} f(x_1,\ldots,\,x_n) = \sum_{i,\,j=1}^n \dfrac{\partial^2 f}{\partial x_i \partial x_j} \dfrac{dx_i}{dt} \dfrac{dx_j}{dt}+ \sum_{k=1}^n \dfrac{\partial f}{\partial x_k} \dfrac{d ^2 x_k}{dt^2}
$$
임을 보이라.

---

$$
\begin{aligned}
\dfrac{d}{dt} f(x_1,\ldots,\,x_n) &= \sum_{i=1}^n  \dfrac{\partial f}{\partial x_i}\dfrac{dx_i}{dt} \\
\dfrac{d^2}{dt^2} f(x_1,\ldots,\,x_n) &= \sum_{i=1}^n\dfrac{d}{dt}\left(\dfrac{\partial f}{\partial x_j}\right) \cdot \dfrac{d x_i}{dt} + \sum_{k=1}^n \dfrac{\partial f}{\partial x_k} \cdot \dfrac{d}{dt}  \left(\dfrac{dx_i}{dt}\right) \\
&= \sum_{i,\,j=1}^n   \dfrac{\partial^2 f}{\partial x_i \partial x_j} \dfrac{dx_i}{dt}\dfrac{dx_j}{dt} + \sum_{k=1}^n \dfrac{\partial f}{\partial x_k} \dfrac{d^2x_k}{dt^2}
\end{aligned}
$$


<b>7. </b> $n$-공간에서 미분작용소
$$
\nabla^2 := {D_1}^2 + \cdots + {D_n}^2
$$
를 라플라스 작용소라고 부른다. 좌표평면에서 극좌표계로 라플라스 작용소를 표현하면,
$$
\partial_x^2 +\partial_y^2 = {\partial_r}^2 + \dfrac{1}{r}{\partial_r} + \dfrac{1}{r^2}{\partial_{\theta}}^2
$$
임을 보이라.

---

$$
(x,\,y) = (r \cos \theta,\, r \sin \theta),\qquad r=\sqrt{x^2+y^2},\qquad \theta = \arctan(y/x)\\
$$
이므로,
$$
\begin{aligned}
\partial_x &= \dfrac{\partial r}{\partial x}\partial r + \dfrac{\partial \theta}{\partial x} \partial_{\theta}=\cos \theta \partial_r -\dfrac{\sin \theta}{r} \partial_{\theta} \\
\partial_y &= \dfrac{\partial r}{\partial y}\partial_r + \dfrac{\partial \theta}{\partial y}\partial_{\theta} = \sin \theta \partial_r + \dfrac{\cos\theta}{r} \partial_{\theta}\\
{\partial_x}^2 &= \left(\cos \theta \partial_r -\dfrac{\sin \theta}{r} \partial_{\theta}\right)\left(\cos \theta \partial_r -\dfrac{\sin \theta}{r} \partial_{\theta} \right)  \\
&= \cos^2 \theta {\partial_r}^2+\dfrac{\sin \theta \cos \theta}{r^2} \partial_{\theta}+ \dfrac{\sin^2 \theta }{r} \partial_r + \dfrac{\sin \theta \cos \theta}{r^2}\partial_{\theta}+\dfrac{\sin^2 \theta}{r^2} {\partial_{\theta}}^2\\
{\partial_y}^2 &= \left(\sin \theta \partial_r + \dfrac{\cos\theta}{r} \partial_{\theta}\right) \left(\sin \theta \partial_r + \dfrac{\cos\theta}{r} \partial_{\theta}\right) \\
&=\sin^2 \theta {\partial_r}^2 -\dfrac{\sin \theta \cos \theta}{r^2}\partial_{\theta}+\dfrac{\cos^2 \theta}{r}\partial_r -\dfrac{\sin \theta \cos \theta}{r^2} \partial_{\theta}+ \dfrac{\cos^2\theta}{r^2}  {\partial_\theta}^2 \\
{\partial_x}^2+{\partial_y}^2 &= (\cos^2 \theta +\sin^2 \theta) {\partial_r}^2+ \dfrac{\cos^2\theta +\sin^2\theta}{r}\partial_r + \dfrac{\sin^2\theta+\cos^2\theta}{r^2}{\partial_{\theta}}^2 \\
&= {\partial_r}^2 + \dfrac{1}{r}\partial_r + \dfrac{1}{r^2} {\partial_{\theta}}^2
\end{aligned}
$$


<b>8. </b> 라플라스 방정식 $\nabla^2 f$ 를 만족시키는 함수를 **조화함수**라고 한다. 다음 함수들이 조화함수임을 보이라.

---

(1) $f(x,\,y) = \ln (x^2+y^2)$ 
$$
\nabla^2 \ln (r^2) = 2 \nabla^2 \ln r = 2\left( {\partial_r}^2+\dfrac{1}{r}\partial_r\right)\ln r = 2\left(\dfrac{1}{r^2}-\dfrac{1}{r^2}\right)=0
$$

(2) $f(x,\,y)=e^x \sin y$
$$
\begin{aligned}
\partial_x f &= e^x \sin y \\
\partial_y f &= e^x \cos y \\
{\partial_x}^2 f &= e^x \sin y \\
{\partial_y}^2 f &= -e^x \sin y
\end{aligned}
$$


(3) $f(x,\,y,\,z) = x^2+y^2-2z^2$
$$
\begin{aligned}
{\partial_x}^2 f&=2\\
{\partial_y}^2 f &=2 \\
{\partial_z}^2 f &= -4
\end{aligned}
$$


(4) $f(x,\,y,\,z)=1/\sqrt{x^2+y^2+z^2}$ 
$$
\begin{aligned}
\partial_x f &= \dfrac{-x}{(x^2+y^2+z^2)^{3/2}} \\
{\partial_x}^2f & = \dfrac{-1}{(x^2+y^2+z^2)^{3/2}}+\dfrac{3x^2}{(x^2+y^2+z^2)^{5/2}} = \dfrac{-2x^2+y^2+z^2}{(x^2+y^2+z^2)^{5/2}}\\
{\partial_y}^2f & =  \dfrac{x^2-2y^2+z^2}{(x^2+y^2+z^2)^{5/2}}\\
{\partial_z}^2f & =  \dfrac{x^2+y^2-2z^2}{(x^2+y^2+z^2)^{5/2}}\\
\end{aligned}
$$


<b>9. </b> $ \left(\dfrac{\partial}{\partial x} + x \dfrac{\partial}{\partial y}\right)^2$ 과 $\left(\dfrac{\partial}{\partial x}\right)^2 + 2x \dfrac{\partial^2}{\partial x \partial y}+   x^2\left(\dfrac{\partial}{\partial y}\right)^2$ 는 같지 않음을 보이라.

---
$$
\begin{aligned}
\left(\dfrac{\partial}{\partial x} + x \dfrac{\partial}{\partial y}\right)^2 &=\left(\dfrac{\partial}{\partial x} + x \dfrac{\partial}{\partial y}\right)\left(\dfrac{\partial}{\partial x} + x \dfrac{\partial}{\partial y}\right) \\
&= \left(\dfrac{\partial}{\partial x}\right)^2+ \dfrac{\partial }{\partial y}+x\dfrac{\partial^2}{\partial x \partial y}+ x \dfrac{\partial^2 }{\partial y \partial x} + x^2 \left(\dfrac{\partial}{\partial y}\right)^2
\end{aligned}
$$


<b>10. </b> 함수 $f(x,\,y) = \ln (1+xy)$ 에서 ${D_{\mathbf{v}}}^2 f,\, {D_{\mathbf{v}}}^3f $ 를 구하라. 그리고 점 $(1,\,1)$ 에서 $\mathbf{v}=(1,\,2)$ 방향으로 볼록인지 또는 오목인지 조사하라.

---

$$
\begin{aligned}
D_1 f &= \dfrac{y}{1+xy}\\
D_2 f &= \dfrac{x}{1+xy}\\
{D_1}^2 f &= -\dfrac{y^2}{(1+xy)^2} \\
{D_2}^2 f&= -\dfrac{x^2}{(1+xy)^2} \\
D_1D_2 f &= \dfrac{1+xy-xy}{(1+xy)^2}=\dfrac{1}{(1+xy)^2}=D_2D_1 f \\
{D_1}^3f &= \dfrac{2y^3}{(1+xy)^3} \\
{D_2}^3 f &=\dfrac{2x^3}{(1+xy)^3} \\
{D_1}^2D_2f &= -\dfrac{2y}{(1+xy)^3} = D_1D_2D_1 f = {D_2}{D_1}^2 f\\
{D_1}{D_2}^2 f &=  -\dfrac{2x}{(1+xy)^3} = {D_2}^2D_1 f = D_2D_1D_2f 
\end{aligned}
$$

이다. $\mathbf{v}=(a,\,b)$ 라 하면,
$$
{D_{(a,\,b)}}^2 f=a^2{D_1}^2 f + 2abD_1D_2 f + b^2D_2f=-\dfrac{1}{4}<0
$$
이므로 $(1,\,1)$ 에서 $\mathbf{v}=(1,\,2)$ 방향으로 오목이다. 그리고 ${D_{(a,\,b)}}^3 f$ 는,
$$
\begin{aligned}
D_{(a,\,b)}^3 f &= a^3 {D_1}^3f + 3a^2b {D_1}^2D_2 f+ 3ab D_1 {D_2}^2 f+b^3{D_2}^3 \\
&= \dfrac{2a^3y^3}{(1+xy)^3} -\dfrac{6a^2by}{(1+xy)^3}-\dfrac{6ab^2x}{(1+xy)^3}+\dfrac{2b^3x^3}{(1+xy)^3}
\end{aligned}
$$

이다.

<b>11. </b>  좌표평면에서 정의된 연속함수
$$
f(x,\,y) = \left\{\begin{array}{ll} \dfrac{xy(x^2-y^2)}{x^2+y^2} ,\qquad & (x,\,y) \ne (0,\,0) \\ 0, & (x,\,y )=(0,\,0)  \end{array} \right.
$$
를 생각하자. 이때 임의의 벡터 $\mathbf{v}$ 에 대하여 $D_{\mathbf{v}} f(0,\,0)=0$ 임을 보이라. 또 원점에서 $\dfrac{\partial^2 f}{\partial x \partial y}$ 와 $\dfrac{\partial^2 f}{\partial y \partial x}$ 가 존재하지만,
$$
\dfrac{\partial^2 f}{\partial x \partial y} (0,\,0) \ne \dfrac{\partial^2 f}{\partial y \partial x} (0,\,0)
$$
임을 보이라. 이때 왜 오일러의 편미분 교환법칙 (2.0.2) 가 성립하지 않는 지를 설명하라.

----
$\mathbf{v}=(a,\,b)$ 라 하면, 
$$
\begin{aligned}
D_{(a,\,b)} f(0,\,0) = \lim_{t\to 0}\dfrac{f(at,\,bt)-f(0,\,0)}{t} = \lim_{t \to 0} \dfrac{ab(a^2-b^2)t^4}{(a^2+b^2)t^3}= \lim_{t \to 0} \dfrac{ab(a^2-b^2)}{a^2+b^2}t = 0 
\end{aligned}
$$
이므로 임의의 벡터 $\mathbf{v}$ 에 대하여 $D_{\mathbf{v}}f(0,\,0)=0$ 이다. 우선
$$
\begin{aligned}
D_1 f(x,\,y) &= \dfrac{(3x^2y-y^3)(x^2+y^2)-2x^2y(x^2-y^2)}{(x^2+y^2)^2}  = \dfrac{y(x^4+4x^2y^2-y^4)}{(x^2+y^2)^2}\\
D_2f(x,\,y) &=  \dfrac{(x^3-3xy^2)(x^2+y^2)-2xy^2(x^2-y^2)}{(x^2+y^2)^2} = \dfrac{x(x^4-4x^2y^2-y^4)}{(x^2+y^2)^2} \\
\end{aligned}
$$
임을 안다. 
$$
\dfrac{\partial^2f}{\partial x \partial y}(0,\,0) = \lim_{t \to 0} \dfrac{D_2f(t, 0) - D_2f(0,\,0)}{t}  \\
\dfrac{\partial^2f}{\partial y \partial x}(0,\,0) = \lim_{s \to 0} \dfrac{D_1f(0,  s) - D_1f(0,\,0)}{s}
$$
이며, 

$x^2+y^2=R^2$ 일 때, $|x|\le R,\, |y|<R,\, |xy|\le R^2/2$ 이므로, 
$$
\left|D_2f(x,\,y)\right| \le \dfrac{|x|}{R^4}{\big(}|x^4|+ 4|x^2y^2|+|y^4|  {\big)} \le 3R
$$
이므로 
$$
\lim_{(x,\,y) \to (0,\,0)} D_2(x,\,y)=0
$$
이며, 자연스럽게 $D_2f(0,\,0)$ 을 $0$ 으로 정의한다. 같은 방법으로 
$$
\lim_{(x,\,y) \to (0,\,0)} D_1(x,\,y)=0
$$
임을 알 수 있다. 
또한 $D_2 f(t,\,0)=t$ 이며, $D_1 f(0,\,s)= -s$ 이다. 따라서,
$$
\dfrac{\partial^2 f}{\partial x \partial y}(0,\,0)=1,\qquad \dfrac{\partial^2 f}{\partial y\partial x}(0,\,0)=-1
$$
이다.

오일러의 편미분 교환법칙이 성립하지 않는것은 아마 이급함수가 아니기 때문일 것이다. $f$ 가 일급함수임을 보였으므로 이제 $D_2D_1 f$ 가 연속이 되지 않음을 보자. 

$$
\begin{aligned}
D_2D_1 f (x,\,y) &= \dfrac{(x^4+12x^2y^2-5y^4)(x^2+y^2)^2 - 4y(x^2+y^2)(x^4y+4x^2y^3-y^5)}{(x^2+y^2)^4} \\
&=\dfrac{1}{(x^2+y^2)^3} \left[ x^6+x^4y^2+12x^4y^2+12x^2y^4-5x^2y^4-5y^6 \right. \\
&\qquad - 4x^4y^2-16x^2y^4+4y^6\left.\right] \\
&= \dfrac{(x^6+9x^4y^2 -9x^2y^4-y^6)}{(x^2+y^2)^3}
\end{aligned}
$$
이며
$$
\begin{aligned}
\lim_{t \to 0}D_2D_1 f(t,\,0) &= 1\\
\lim_{s \to 0}D_2 D_1 f(0,\,s) &= -1
\end{aligned}
$$
이므로 $D_2D_1 f$ 는 연속이 아니다. 따라서 $f$ 는 이급함수가 아니다.

<b>12. </b> $n$-공간의 한 열린집합 $U$ 에서 정의된 무한급함수 전체의 집합을 $C^\infty(U)$ 라고 두자. 그러면 임의의 두 벡터 $\mathbf{v},\,\mathbf{w}$ 에 대하여 방향미분작용소
$$
D_{\mathbf{v}},\, D_{\mathbf{w}}: C^{\infty} (U)\to C^{\infty}(U)
$$
들은 서로 교환가능함, 즉
$$
D_{\mathbf{v}}\circ D_{\mathbf{w}}=D_{\mathbf{w}}\circ D_{\mathbf{v}}
$$
임을 보이라.

---

$\mathbf{v}=(v_1,\ldots,\,v_n),\, \mathbf{w}=(w_1,\ldots,\,w_n)$ 이라 하자. 

$$
\begin{aligned}
(D_{\mathbf{v}}\circ D_{\mathbf{w})}f &= D_{\mathbf{v}} \left(\sum_{i=1}^n w_i \partial_i f \right) \\
&= \sum_{j=1}^n v_j \partial_j \left(\sum_{i=1}^n w_i \partial_i f\right) \\
&= \sum_{i,\,j=1}^n w_i v_j\partial_j \partial_i f \\
&= \sum_{i,\,j=1}^n w_i v_j \partial_i \partial_j f\\
&= \sum_{i=1}^n w_i \partial_i \left(\sum_{j=1}^n v_j \partial_j f\right) \\
&= (D_{\mathbf{w}}\circ D_{\mathbf{v}})f
\end{aligned}
$$


<b>13. </b> 함수 $f(x_1,\ldots,\, x_n)$ 이 $k$ 급 함수이면, 임의의 벡터 $\mathbf{v} = \sum_{i=1}^n v_i \mathbf{e}_i$ 에 대하여
$$
{D_{\mathbf{v}}}^k f = \sum_{i_1,\ldots,\,i_k=1}^n v_{i_1}\cdots v_{i_k}D_{i_1}\cdots D_{i_k}f
$$
임을 보이라.

---
Induction 을 통해 증명하자. $k=1$ 일 때는 자명하다. 이제 $k$ 에 대해 위 식이 성립함을 가정하자. $k+1$ 에 대해 
$$
\begin{aligned}
{D_{\mathbf{v}}}^{k+1} f &= D_{\mathbf{v}}\left(D_{\mathbf{v}}^k\right)f\\
&= D_{\mathbf{v}}\left(\sum_{i_1,\ldots,\,i_k=1}^n v_{i_1}\cdots v_{i_k} D_{i_1}\cdots D_{i_k} f\right) \\
&= \sum_{i_{k+1}=1}^n v_{i_{k+1}} D_{i_{k+1}}\left(\sum_{i_1,\ldots,\,i_k=1}^n v_{i_1}\cdots v_{i_k} D_{i_1}\cdots D_{i_k} f\right)\\
&= \sum_{i_1,\ldots,\,i_{k+1}=1}^n \left( v_{i_1}\cdots v_{i_{k+1}} D_{i_1}\cdots D_{i_{k+1}} f\right)
\end{aligned}
$$
이므로 성립한다. 



<br></br>
a
b
c
d
e
f

<br></br>

b