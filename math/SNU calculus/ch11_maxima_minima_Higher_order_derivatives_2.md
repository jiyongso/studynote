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
e^x \tan y &= \left( 1+x+\dfrac{x^2}{2} +o\left( |x|^3 \right)\right)\left(y+o\left(|y|^3\right)\right) \approx y+xy
\end{aligned}
$$

(11) $(1+x)^y$

$$
\begin{aligned}
\partial_x f &= y(1+x)^{y-1}\\
\partial_y f &=  (1+x)^y\ln (1+x) \\
{\partial_x}^2 f &= y(y-1)(1+x)^{y-2}  \\
{\partial_y}\partial_x f &= (1+x)^{y-1} +(1+x)^{y-1}\ln (1+x)\\
{\partial_y}^2 f  &= {\big(} \ln (1+x) {\big)}^2 \ln (1+x)^y \\
(1+x)^y &\approx 1+xy
\end{aligned}
$$

(12) $\sin e^{xy}$
$$
\begin{aligned}
\partial_x f &= ye^{xy} \cos e^{xy} \\
\partial_y f &= xe^{xy} \cos e^{xy} \\
{\partial_x}^2 f &= y^2e^{xy\cos e^{xy}}-y^2e^{2xy}\sin e^{xy} \\
{\partial_x }{\partial_y} f &= e^{xy}\cos e^{xy} +xye^{xy}-xye^{2xy} \sin e^{xy} \\
{\partial_y}^2 f &= x^2e^{xy}\cos e^{xy}-x^2e^{2xy} \sin e^{xy} \\
\sin e^{xy} &\approx \sin 1 + (\cos 1 ) xy 
\end{aligned}
$$

<br>

<b>2. </b> 원점에서 함수 $f(x,\,y)=\cos x \sin y$ 의 3차 근사 다항식을 구하라.

---
$$
\begin{aligned}
\cos x \sin y &= \left(1-\dfrac{x^2}{2} + o\left(|x|^4 \right) \right) \left(y-\dfrac{y^3}{6} + o\left(|x|^5\right)\right) \\
&\approx y-\dfrac{x^2y}{2} -\dfrac{y^3}{6}
\end{aligned}
$$


<b> 3. </b>> 다음을 보이라.
$$
\ln (1+x+2y) = x+2y-\dfrac{1}{2}\left(x^2+4xy+4y^2\right) +o (x^2+y^2)
$$

---
Let $f(x,\,y)=\ln (1+x+2y)$. 그렇다면,  

$$
\begin{aligned}
\partial_x f &= \dfrac{1}{1+x+2y} \\
\partial_y f &= \dfrac{2}{1+x+2y} \\
{\partial_x}^2 f &= -\dfrac{1}{(1+x+2y)^2}  \\
\partial_y \partial_x f &= - \dfrac{2}{(1+x+2y)^2} \\
{\partial_y}^2 f &= -\dfrac{4}{(1+x+2y)^2} 
\end{aligned}
$$
이므로,
$$
\ln(1+x+2y) = x+2y -\dfrac{1}{2} (x^2+4xy+4y^2)+o\left(|x^2+y^2|\right)
$$



<b>4. </b>  점 $(x,\,y)$ 가 원점에 가까이 갈 때, $\sin (xy)/x$ 의 극한값은 존재하는가? 존재하면 그 값을 구하라. (분모가 영이 아닌 영역에서만 조사한다.) 또 다음 함수들에 대하여는 어떠한가?

---

$|\sin xy|<|xy|$ 이므로 $\left| \dfrac{\sin xy}{x}\right| < |y|$ 이다. 따라서 원점으로의 극한은 $0$ 이다. 

(1) $\dfrac{e^{xy}-1}{x}$

$$
e^{xy}=1+xy+\dfrac{(xy)^2}{2}+\cdots + \dfrac{(xy)^k}{k!}+\cdots
$$
이므로,
$$
\dfrac{e^{xy}-1}{x} = y+\dfrac{xy^2}{2} + \cdots + \dfrac{x^{k-1}y^k}{k!}+\cdots
$$
이다. 따라서 원점으로의 극한은 $0$ 이다. 

(2) $\dfrac{\ln (1+x^2+y^2)}{x^2+y^2}$​

$x^2+y^2=R^2$ 라 하면, 
$$
\ln (1+R^2) = R^2 - \dfrac{1}{2}R^4 + \cdots + (-1)^{k+1}\dfrac{R^{2k}}{k}+\cdots
$$
이다. 따라서,
$$
\dfrac{\ln (1+R^2)}{R^2} = 1-\dfrac{1}{2}R^2 + \cdots + (-1)^{k+1}\dfrac{R^{2k-2}}{k}+\cdots
$$
이므로 원점으로의 극한 ($R\to 0$ 극한)에서 극한값은 $1$ 이다. 

(3) $\dfrac{\cos xy -1}{x}$
$$
\cos xy = 1-\dfrac{x^2y^2}+ o(|(xy)^2|)
$$
이므로 원점 으로의 극한은 $0$ 이다.

(4) $\dfrac{\sin xy - xy}{xy}$
$$
\sin xy - xy = \dfrac{(xy)^3}{6} + o(|x^3y^3|)
$$
이므로 원점 으로의 극한은 $0$ 이다. 


<b>5. </b> 함수 $x^3-2xy^4+(x-1)^2y^10$ 의 테일러급수에서 제 7차항은 무엇인가?

---

테일러급수의 유일성에 의헤 다항식은 테일러 급수와 같다. 따라서 7차항은 $0$ 이다.



<b>6. </b> 함수 $f(x,\,y,\,z)$ 가 $x,\,y,\,z$ 의 다항식이면, $f$ 는 자기 자신의 테일러 급수와 같음을 보이라.

---
$x_0,\,y_0,\,z_0$ 에서의 테일러 전개를 생각하자. 다항식 $f$ 를
$$
f=\sum_{i,\,j,\,k} a_{i,\,j,\,k}(x-x_0)^i (y-y_0)^j (z-z_0)^k
$$
로 표현 할 수 있으며,

$$
a_{i,\,j,\,k} = \dfrac{1}{i!j!k!} {D_1}^i{D_2}^j{D_3}^k f (x_0,\,y_0\,z_0)
$$
이다. 



<b>7. </b> 함수 $x^2y+xy^2+1$ 을 $(x-1)$ 과 $(y-1)$ 의 멱급수로 표현하라.

---

$f(x,\,y)=x^2y+xy^2+1$ 이라 놓고 6. 의 결과를 이용한다.
$$
\begin{aligned}
D_1 f &= 2xy+y^2 \\
D_2 f &= x^2+2xy \\
{D_1}^2 f &= 2y \\
{D_2D_1}f &= 2x+2y\\
{D_2}^2 f &= 2x \\
{D_1}^2 D_2 f = 2 \\
{D_1} {D_2}^2 f = 2
\end{aligned}
$$
이며 나머지 테일러 계수는 $0$ 이므로, 
$$
\begin{aligned}
x^2+xy^2+1 =& 3+3(x-1)+3(y-1) +(x-1)^2 + 4(x-1)(y-1) + (y-1)^2 \\
&+ 2(x-1)^2 (y-1)+2(x-1)(y-1)^2
\end{aligned}
$$
이다.



<b>8. </b> 이급함수 $f(x,\,y)$ 가 임의의 $(x,\,y)$ 와 실수 $t$ 에 대하여
$$
f(tx,\,ty) = t^2 f(x,\,y)
$$
이면
$$
f(x,\,y) = \dfrac{1}{2} (xD_1 + yD_2)^2 f(0,\,0)
$$
임을 보이라.

---

$\mathbf{v}=(x,\,y)$ 로 놓고, 도움정리 2.1.1 을 사용하면 
$$
\left.\dfrac{d^2}{dt^2}\right|_{t=0}f(t\mathbf{v}) = {D_{\mathbf{v}}}^2 f(0,\,0) \implies 2f(x,\,y)= (xD_1 +yD_2)^2f(0,\,0)
$$
이다. 



<b>9. </b> 기준점에서의 값을 $1$ 로 두었을 때 다음의 일차 근사값을 구하고, 또 오차를 생각하라.

---

(1) $(1.02)^{1.01}$

Let $f(x,\,y)=(1+x)^{1+y}$. Then,

$$
\begin{aligned}
D_1 f &= (1+y)(1+x)^y \\
D_2 f &= \ln (1+x) (1+x)^{1+y}\\
\end{aligned}
$$
이므로, $D_1f(0,\,0)=1,\, $D_2 f(0,\,0)=0$ 이다. 따라서,
$$
(1+x)^{1+y} \approx 1+x 
$$
이므로,

$$
(1.02)^{1.01} = f(0.02,\, 0.01)\approx 1.02 
$$

이다. 
$$
\begin{aligned}
{D_1}^2 f &= (1+y)y(1+x)^{1-y} \\
{D_2}D_1f &= D_1D_2 f=(1+x)^y + \ln (1+x) (1+y)(1+x)^y\\
{D_2}^2 f &= {\big(} \ln (1+x){\big )}^2 (1+x)^{1+y}
\end{aligned}
$$
이므로, $P=(0,\,0),\, \mathbf{v}=(0,02,\, 0.01)$​​ 에 대해 
$$
M_2 =\left\{\left|D_iD_j f(P+t\mathbf{v})\right|: 1\le i,\,j \le 2,\, 0 \le t \le 1\right\}
$$
를 구하자. $(1+0.02)^{0.01}<1.0002$​​ 이며 $0<\ln (1+0.02)<1$​​, $(1+0.01)(1+0.02)^{0.01} <(1+0.02)^{1.01}<1.0002$ 이므로 대략 $M_2 < 2$ 라고 볼 수 있다. 정확히는 $M_2<1.03$ 이다. 따라서,
$$
|R_1f(P,\,\mathbf{v})\le \dfrac{M_2}{2}|\mathbf{v}|^2 <0.00026
$$
이다. 

(2) $(0.99)^{0.99}$

귀찮으니...




<b>10. </b> 함수 $f$ 와 $g$ 가 무한급함수이면 정의역의 점 $P$ 와 벡터 $\mathbf{v}$ 및 자연수 $k$ 에 대하여
$$
T_k (fg)(P,\,\mathbf{v})=T_k f(P,\,\mathbf{v}) \cdot T_k g(P,\,\mathbf{v}) \qquad \operatorname{mod} \quad o\left(|\mathbf{v}|^k \right)
$$
임을 보이라.

---

우선 $T_k (fg)(P,\,\mathbf{v})$ 를 전개하면,
$$
\begin{aligned}
T_k (fg)(P,\,\mathbf{v}) &= \sum_{n=0}^k \dfrac{{D_{\mathbf{v}}}^k (fg)(P,\,\mathbf{v})}{n!}  \\
&= \sum_{n=0}^k \dfrac{1}{n!} \sum_{m=0}^n \dfrac{n!}{m!(n-m)!}{D_{\mathbf{v}}}^m f(P) \cdot {D_{\mathbf{v}}}^{n-m} g(P) \\
&=\sum_{n=0}^k \sum_{m=0}^n \dfrac{1}{m! (n-m)!} {D_{\mathbf{v}}}^m f(P) \cdot {D_{\mathbf{v}}}^{n-m} g(P)
\end{aligned}
$$

이다. 이제 $T_k f(P,\,\mathbf{v}) \cdot T_k g(P,\,\mathbf{v})$  를 전개하면, 

$$
\begin{aligned}
T_k f(P,\,\mathbf{v})\cdot T_k g(P,\,\mathbf{v}) &= \left(\sum_{p=0}^k \dfrac{{D_{\mathbf{v}}}^p f(P)}{p!}\right) \left(\sum_{q=0}^k \dfrac{{D_{\mathbf{v}}}^q g(P)}{q!}\right)  \\
&= \sum_{p=0}^k \sum_{q=0}^k \dfrac{1}{p!q!} {D_{\mathbf{v}}}^p f(P)\cdot {D_{\mathbf{v}}}^q g(P) \\
&= \sum_{n=0}^{2k} \sum_{m=0}^n \dfrac{1}{n! (n-m)!} {D_{\mathbf{v}}}^m f(P)\cdot {D_{\mathbf{v}}}^{n-m} g(P) \\
&= \sum_{n=0}^k \sum_{m=0}^n \dfrac{1}{n! (n-m)!} {D_{\mathbf{v}}}^m f(P)\cdot {D_{\mathbf{v}}}^{n-m} g(P) \\
&\quad + \sum_{n=k+1}^{2k}\sum_{m=0}^n \dfrac{1}{n! (n-m)!} {D_{\mathbf{v}}}^m f(P)\cdot {D_{\mathbf{v}}}^{n-m} g(P) \\
&= T_{k}(fg)(P)+  \sum_{n=k+1}^{2k}\sum_{m=0}^n \dfrac{1}{n! (n-m)!} {D_{\mathbf{v}}}^m f(P)\cdot {D_{\mathbf{v}}}^{n-m} g(P)
\end{aligned}
$$
-- to be done --

