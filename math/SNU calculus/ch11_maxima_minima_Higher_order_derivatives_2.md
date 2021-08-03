XI. 최대최소값 문제와 고계미분 #2
===

## 연습문제 : 제 11 장 3 절

#### 정리 3.0.3  다변수 함수의 테일러 전개

$n$-공간의 열린 집합 $U$ 에서 정으;된 $k$-번 미분가능한 함수 $f$ 가 주어졌다고 하자. 이 때 $U$ 의 한 점 $P$ 와 벡터 $\mathbf{v}$ 에 대하여 tjsqns $[P,\, P+\mathbf{v}] : = \{P+t\mathbf{v}: 0\le t \le 1\}$ 이 $U$에 포함된다고 하자. 그러면
$$
f(P+\mathbf{v})=f(P)+D_{\mathbf{v}}f(P)+ \dfrac{1}{2!}{D_{\mathbf{v}}}^2 f{P}+ \cdots \dfrac{1}{(k-1)!}{D_{\mathbf{v}}}^{k-1}f(P)+ \dfrac{1}{k!} {D_{\mathbf{v}}}^k f(P+t^\ast \mathbf{v})
$$
를 만족시키는 $t^\ast$ 가 $0$ 과 $1$ 사이에 존재한다.

---

*(proof)* 함수 $g(t):=f(P+t\mathbf{v})$ 에 대하여
$$
g^{(i)}(t) = {D_{\mathbf{v}}}^i f(P+t\mathbf{v})
$$
임을 귀납법으로 보이자. $i=0$ 일 때는 자명하며, $i$ 에서 성립한다고 가정하면,
$$
g^{(i+1)}(t) = \dfrac{d}{dt} g^{(i)}(t) = \dfrac{d}{dt} \left( {D_{\mathbf{v}}}^i f(P+t\mathbf{v}) \right) = {D_{\mathbf{v}}}^{i+1}(P+t\mathbf{v})
$$
이다. 이제, $g(t)$ 의 일변수 테일러전개를 이용하고자 한다,
$$
g(t) = g(0)+g'(0)t+\cdots + \dfrac{g^{(k-1)}(0) }{(k-1)!}t^{k-1}+ \dfrac{g^{(k)}(t^{\ast})}{k!} t^k
$$
를 만족시키는 $t^\ast \in (0,\,t)$ 의 존재를 안다. 여기서 $t=1$ 로 두면 증명 끝. $\square$


<br>
#### 정리 3.2.2 테일러 전개의 유일성

$n$ 공간의 한 점 $P$ 근방에서 정의된 $k$ 번 미분가능한 함수 $f$ 와 $g$ 에 대하여, $\mathbf{x}$ 에 대한 함수 $f(P+\mathbf{x})$ 와 $g(P+\mathbf{x})$ 의 차가 $o(|\mathbf{x}|^k)$ 이면
$$
T_k f(P,\,\mathbf{x})=T_k g(P,\,\mathbf{x})
$$
이다.

---
*(proof)* 

$$
f(P+\mathbf{x})=T_k f(P,\,\mathbf{x})+o\left( |\mathbf{x}|^k 
\right),\qquad g(P+\mathbf{x})=T_k g(P,\,\mathbf{x})+o\left( |\mathbf{x}|^k \right)
$$
에서 두 식의 차는,
$$
f(P+\mathbf{x})-g(P+\mathbf{x})=T_k f(P,\,\mathbf{x})-T_k g(P,\,\mathbf{x})+o \left(|\mathbf{x}|^k\right)=o(|\mathbf{x}|^k)
$$
이므로,
$$
T_k f(P,\,\mathbf{x})-T_k g(P,\,\mathbf{x})=o\left( |\mathbf{x}|^k\right)
$$
이다. 위 식의 좌변은 차수가 $k$ 이하인 다항함수 이며 우변은 $k$ 차보다 큰 다항식이므로 항등식에 의해 $0$ 이다.$\square$
<br>
<b>1. </b> 원점에서 다음 함수의 2차 근사 다항식을 구하라.

---
문제에 주어진 함수를 $f(x,\,y)$ 라 하자. 
(1) $\sin (xy)$
$$
\begin{aligned}
\partial_x \sin (xy) &= y\cos (xy) \\
\partial_y \cos (xy) &= x \cos (xy) \\
(\partial_x)^2 \sin (xy) &= -y^2 \sin (xy) \\
\partial_x \partial_y \sin (xy)  &= \cos (xy) -xy \sin (xy) \\
(\partial_y)^2 \sin (xy) &= -x^2 \sin (xy) \\
\sin (xy) & \approx xy
\end{aligned}
$$


(2) $\sin x \cos y$
$$
\begin{aligned}
\partial_x \sin x \cos y &= \cos x \cos y\\
\partial_y \sin x \cos y &= - \sin x \sin y\\
{\partial_x}^2 \sin x \cos y &= - \sin x \cos y\\
\partial_x \partial_y \sin x \cos y &= - \cos x \sin y \\
{\partial_y}^2 \sin x \cos y &= - \sin x \cos y \\
\sin x \cos y &\approx  x
\end{aligned}
$$

(3) $\sin (x^2+y^2)$
$$
\begin{aligned}
\partial_x f &= 2x\cos (x^2+y^2)\\
\partial_y f &= 2y \cos (x^2+y^2)\\
{\partial_x}^2 f &= 2\cos (x^2+y^2)-4x^2 \sin (x^2+y^2) \\
{\partial_x}{\partial_y} f &= -2xy \sin (x^2+y^2) \\
{\partial_y}^2 f &= 2 \cos (x^2+y^2)-4y^2 \sin (x^2+y^2) \\
\sin (x^2+y^2) &\approx x^2+y^2
\end{aligned}
$$


(4) $ \sin (e^y+x^2-2)$
$$
\begin{aligned}
\partial_x f &= 2x \cos (e^y+x^2-2)\\
\partial_y f &= e^y\cos (e^y+x^2-2)\\
{\partial_x}^2 f &= 2\cos (e^y+x^2-2)-4x^2 \sin (e^y+x^2-2) \\
{\partial_x}{\partial_y} f &= -2xe^y \sin(e^y+x^2-2) \\
{\partial_y}^2 f &= e^y\cos (e^y+x^2-2)-e^{2y} \sin (e^y+x^2-2) \\
\sin (e^y+x^2-2) &\approx -\sin (1) + (\cos 1) y + \cos (1)x^2+\dfrac{1}{2}\cos (1) y^2 
\end{aligned}
$$


(5) $\ln (1+xy)$
$$
\begin{aligned}
\partial_x f &= \dfrac{y}{1+xy} \\
\partial_y f &= \dfrac{x}{1+xy} \\
{\partial_x}^2 f &= -\dfrac{y^2}{(1+xy)^2} \\
\partial_x \partial_y f &= \dfrac{1}{1+xy}-\dfrac{xy}{(1+xy)^2} \\
{\partial_y}^2 f &= -\dfrac{x^2}{(1+xy)^2} \\
f(x,\,y) &\approx xy
\end{aligned}
$$

(6) $x+xy+2y^2+x^2$
$$
\begin{aligned}
\partial_x f &= 1+y+2x \\
\partial_y f &= x+4y \\
{\partial_x}^2 f &= 2\\
\partial_x \partial_y f &= 1\\
{\partial_y}^2 f &= 4 \\
x+xy+2y^2+x^2 &\approx x+x^2+xy+2y^2
\end{aligned}
$$

(7) $e^{x+y}$
$$
\begin{aligned}
\partial_x f &= e^{x+y} \\
\partial_y f &= e^{x+y} \\
{\partial_x}^2 f&= \partial_y \partial_x f={\partial_y}^2 f =e^{x+y} \\
e^{x+y} &\approx 1+ x+y + \dfrac{x^2}{2}+xy+\dfrac{y^2}{2}
\end{aligned}
$$

(8) $e^x-e^y$
$$
\begin{aligned}
\partial_x f &= e^x = {\partial_x}^2 f\\
\partial_y f &= -e^y = {\partial_y}^2 f\\
\partial_x \partial_y f &= 0\\
e^x-e^y &\approx x-y+\dfrac{1}{2}x^2-\dfrac{1}{2}y^2
\end{aligned}
$$

(9) $ \dfrac{1}{1-x^2-y^2}$
$\dfrac{1}{1-x}=1+x+x^2+\cdots$ 이므로,
$$
\dfrac{1}{1-x^2-y^2}\approx 1+x^2+y^2
$$
이다. 

(10) $e^x \tan y$
$$
\begin{aligned}
e^x \tan y &= \left( 1+x+\dfrac{x^2}{2} +o\left( |x|^3 \right)\right)\left(y+o\left(|y|^3\right)\right)
\end{aligned}
$$

(11) $(1+x)^y$

$$
\begin{aligned}
\partial_x f &= y(1+x)^{y-1}\\
\partial_y f &= \ln (1+x) (1+x)^y
\end{aligned}
$$

(12) $\sin e^{xy}$
$$
\begin{aligned}

\end{aligned}
$$