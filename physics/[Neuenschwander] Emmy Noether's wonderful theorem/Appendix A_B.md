Appendix A. & B 
===

## Appendix A. Scalars, Vectors, Tensors, and Coordinate Transformations



<b>Note : </b> 여기서는 speed of light $c=1$ 인 unit을 사용한다.




#### 뉴턴-갈릴레오 상대성과 특수상대성 이론의 invariants 

- 뉴턴-갈릴레오 상대성에서는 모든 관성좌표계에서, length, time intervals 가 invariants 이며 $c$ 는 invariant가 아니다.
- Special relativity 에서는 $c$ 가 모든 관성좌표계에서 invariant 이며 length, time intervals가 invariants 가 아님.



#### Covariants relation

$\mathbf{F}=m\mathbf{a}$ 를 생각하자. $F_i = ma_i$ 이며 $(x,\,y,\,z)\to (x',\,y',\,z')$ 으로 좌표변환을 하더라도 $F'_i = ma'_i$ 꼴은 변하지 않는다. 이런 관계를 **covariant** 라 한다. 



#### Scalar

$K=\dfrac{1}{2} mv^2$ 는 잘 알다시피 좌표변환에 대해 그 값이 변하지 않는다. 이런 물리량을 **scalar** 라 한다.



#### Contravariant Vectors, Tensors

coordinates 를$\{x^\mu\}$ 로 하자. 즉 index를 superscript로 쓴다. (아직까지는 왜냐고 묻지 말자) 3차원 Cartesian coordinate system 에서는 $\{x^\mu\}=(x^1,\,x^2,\,x^3)$ , Spherical coordinate 에선 $\{x^\mu\}=(x^1,\,x^2,\,x^3)=(\rho,\,\theta,\,\varphi)$ 이다. 

$\{x^\mu\}\to \{{x'^\mu} \}$ coordinate transform을 생각하자. $x'^\mu$ 은 $x^\mu$ 의 함수이므로,
$$
{x^\mu}' ={x^\mu}'(x^\nu)\tag{A.1}
$$
라 쓸 수 있다. Chain rule에 의해
$$
d{x'^\mu}=\dfrac{\partial {x'^\mu}}{\partial x^\nu}dx^\nu \tag{A.2}
$$
이다. 

이렇게 coordinate transformation에 대해 (A.2)와 같이 변환되는 물리량을 **contravariant vector** 라 한다. 즉 $\{A^\mu\}$ 가
$$
{A'^\mu} = \dfrac{\partial {x'^\mu}}{\partial x^\nu} A^\nu \tag{A.3}
$$
의 변환을 따르면 $\{A^\mu\}$ 는 vector 이다. scalar를 rank-0 tensor, vector를 rank-1 tensor라 한다.



어떤 물리량 $\{T^{\alpha \beta}\}$ 가 좌표변환에 대해 다음과 같은 변환을 따를 때 이를 rank-2 tensor 라 한다.
$$
T'^{\mu \nu} =\dfrac{\partial x'^{\mu}}{\partial x^\alpha} \dfrac{\partial x'^\nu}{\partial x^\beta} T^{\alpha \beta}
$$

#### Symmetric metric tensor $g_{\mu\nu}$

Infinitesimally nearby two points $x^\mu$ and $x^\mu + dx^\mu$ 사이의 거리가 다음과 같이 주어지도록 하는 symmetric metric tensor $g_{\mu \nu}$ 를 생각하자.
$$
(ds)^2=g_{\mu \nu}dx^\mu dx^\nu \;.\tag{A.4}
$$
3차원 유클리드 공간에서의 Cartesian coordinate system 에서는 $g_{\mu \nu}=\delta_{\mu \nu}$ 이다. 3차원 유클리드 공간에서의 spherical coordi. system 에서는 
$$
(ds)^2=dr^2 + r^2 d\theta^2 + r^2\sin^2 \theta d\varphi^2
$$
이므로 $g_{rr}=1,\, g_{\theta\theta}=r^2,\, g_{\varphi \varphi}=r^2\sin^2\theta$ 이며 나머지는 $0$ 이다.

특수상대론의 민코프스키 공간에서 $(x^0,\,x^1,\,x^2,\,x^3)=(t,\,x,\,y,\,z)$ 라 놓으면 그 길이는 proper time $d\tau$ 가 되며,
$$
(d\tau)^2=g_{\mu\nu}dx^\mu dx^\nu= dt^2-x^2-y^2-z^2 \tag{A.5}
$$
이므로 $g_{00}=1,\,g_{11}=g_{22}=g_{33}=-1$ 이고 나머지는 $0$ 이다.



#### Covariant vectors

(A.5) 에서  보았듯이 metric tensor의 - 성분으로 인해 우리가 지금까지 알던 두 벡터의 inner product로 표현할 수  없으며 새로운 정의를 도입해야 한다. 이를 위해 다음과 같은 벡터를 정의하는데 이렇게 정의된 벡터를 **covariant vector** 라 한다. (index가 밑에 있다.)
$$
A_\mu =g_{\mu \nu}A^\nu \;.\tag{A.6}
$$
민코프스키 공간에서는 다음과 같다.
$$
A_0 = A^0,\quad A_k = -A^k \quad \text{for}\;k=1,\,2,\,3\;. \tag{A.7}
$$
$g_{\mu \nu}$ 의 역행렬을 $g^{\nu \mu}$ 로 정의한다. 따라서,
$$
A^\mu = g^{\nu \mu}A_\mu\tag{A.8}
$$
이다. 



Covariant vector의 예로서는 대표적으로 gradient of scalar function이 있다. Scalar function $\lambda$ 에 대해
$$
\dfrac{\partial \lambda}{\partial x^\mu} \equiv \partial_\mu \lambda \tag{A.9}
$$
로 정의하자. 이것의 transformation은 chain rule에 의해
$$
\partial'_{\mu}\lambda = \dfrac{\partial \lambda}{\partial x'^\mu}=\dfrac{\partial x^\nu}{\partial x'^\mu} \dfrac{\partial \lambda}{\partial x^\nu}=\dfrac{\partial x^\nu}{\partial x'^\nu} \partial_\nu \lambda \tag{A.10}
$$
이므로 (A.2) 와 다르며 이것이 covariant vector와 contravariant vector를 구분하는 이유이다. 즉 covariant vector $\{A_\mu\}$ 는 좌표변환에 대해
$$
A'_\mu = \dfrac{\partial x^\nu}{\partial x'^\mu} A_\nu \tag{A.11}
$$
과 같이 변환된다.



## Appendix B. Special Relativity



#### 상대성 이론의 기본 가정 : 광속도 $c$ 불변

모든 관성좌표계에서 $c$는 불변이다.



#### Proper time $\tau$

관성좌표계에서 두 event가 한 장소에서 이루어 졌을 때의 time interval을 **proper time** 이라 하고 관례적으로 $d\tau$ 라 쓴다.  관성좌표계 $\Sigma$에서 이 events가 $(t,\,0,\,0,\,0)$ 와  $(t+dt,\,0,\,0,\,0)$ 에서 이루어 졌고 다른 관성좌표계 $\Sigma'$ 에서 $(t',\,x',\,y',\,z')$ 와 $(t'+dt',\,x'+dx',\, y+dy',\, z+dz')$ 에서 이루여 졌을 때,
$$
d\tau^2=dt^2=dt'^2-dx'^2-dy'^2-dz'^2 \tag{A.12}
$$
이며 이 $d\tau$ 가 관성좌표계 변환에 대해 불변량이다.



#### 4-vectors

- space time 4 vectors : $(x^0,\,x^1,\,x^2,\,x^3)=(t,\,x,\,y,\,z)$
- spacetime displacement 4 vectors $(dx^0,\, dx^1,\,dx^2,\,dx^3)=(dt,\,dx,\,dy,\,dz)$



#### Momentum 4-vectors

주어진 관성계에서 다음과 같이 정의된 $\{p^\mu\}$ 를 **momentum four-vetor** 라 한다.
$$
p^\mu = m \dfrac{dx^\mu}{d\tau}=m \left(\dfrac{dx^\mu}{dt}\dfrac{dt}{d\tau}\right)=mu^\mu \tag{A.13}
$$
여기서 
$$
u^\mu = \gamma v^\mu\quad \text{where }\gamma \equiv\dfrac{dt}{d\tau}=\dfrac{1}{\sqrt{1-v^2}} \tag{A.14}
$$
($c=1$ 인 unit을 사용함을 유념하라.)



여기서 spatial component of momentum 4-vectors는 
$$
\boldsymbol{p}=\gamma m\boldsymbol{v} \quad \text{where } \boldsymbol{v}=\dfrac{d\boldsymbol{r}}{dt}\tag{A.15} 
$$
이다. 그렇다면 $p^0=\gamma m$ 은? $p^0$ 를 $v^2$ 에 대해 멱급수 전개하면 다음과 같다.
$$
p^0 = m+\dfrac{1}{2}mv^2+O(v^4)\tag{A.16}
$$
$m$ 은 관성계와 무관한 상수이며 두번째 식은 운동에너지이다. 즉 momentum 4-vectors 는
$$
\{p^\mu\} = (E,\,\boldsymbol{p}) = \gamma m (1,\, \boldsymbol{v})\tag{A.17}
$$
이다. 



우리는 역시 covariant partner of $p^\mu$ 를 정의하면,
$$
p_\mu = g_{\mu\nu}p^\nu \tag{A.18}
$$
그렇다면,
$$
\{p_\mu\}=(E,\, -\boldsymbol{p}) \tag{A.19}
$$
이며,
$$
p_\mu p^\mu = E^2-p^2 = m^2 \tag{A.20}
$$
이므로 invariant mass 를 얻는다.



#### Lorentz transformation

관성좌표계 $\Sigma$ 에 대해 $v_r \hat{\boldsymbol{x}}$ 로 움직이는 다른 관성좌표계 $\Sigma'$ 을 생각하자. $\gamma_r = 1/\sqrt{1-v_r^2}$ 라 할 때, $\Sigma$ 에서의 $(t,\,x,\,y,\,z)$ 와 $\Sigma'$ 에서의 $(t',\,x',\,y',\,z')$ 사이에는 다음과 같은 관계가 성립한다.
$$
\begin{bmatrix}t' \\ x' \\ y' \\z'\end{bmatrix} = \begin{bmatrix} \gamma_r & -v_r & 0 & 0 \\ -\gamma_r v_r & \gamma_r & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1\end{bmatrix} \cdot \begin{bmatrix}t \\ x\\ y \\ z \end{bmatrix} \tag{A.21}
$$
이 때 **rapidity** $\varepsilon \equiv \tanh^{-1} v_r$ (정확히는 $\varepsilon \equiv \tanh^{-1} (v_r/c)$ ) 를 정의하면 아래와 같이 rotation과 비슷한 form을 가진다.
$$
\begin{bmatrix}t' \\ x' \\ y' \\z'\end{bmatrix} = \begin{bmatrix} \cosh \varepsilon & -\sinh \varepsilon & 0 & 0 \\ -\sinh \varepsilon & \cosh \varepsilon & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1\end{bmatrix} \cdot \begin{bmatrix}t \\ x\\ y \\ z \end{bmatrix} \tag{A.22}
$$
위 식을 $\varepsilon$ 에 대해 1st order 까지 나타내면,
$$
\begin{bmatrix}t' \\ x' \\ y' \\z'\end{bmatrix} = \begin{bmatrix} 1 & - \varepsilon & 0 & 0 \\ -\varepsilon & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1\end{bmatrix} \cdot \begin{bmatrix}t \\ x\\ y \\ z \end{bmatrix} \tag{A.23}
$$
이다. 즉
$$
x'^\mu \approx x^\mu+\varepsilon {\omega^\mu}_\nu x^\nu\,,\quad \text{where } {\omega^\mu}_\nu=\begin{bmatrix} 0 & - 1 & 0 & 0 \\ -1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0\end{bmatrix} \tag{A.24}
$$
으로 나타 낼 수 있다. 



Lorentz transformation matrix coefficiants $\partial x'^\mu/\partial x^\nu$ 를 ${\Lambda^\mu }_\nu$ 로 쓰기로 하자. 그렇다면,
$$
x'^\mu = {\Lambda^\mu}_\nu x^\nu \tag{A.25}
$$
이며 infinitesimal transformation은
$$
{\Lambda^\mu}_\nu \approx {\delta^\mu}_\nu + \varepsilon {\omega^\mu}_\nu \tag{A.26}
$$
이다. 



#### Lorentz group and Poincaré group

모든 Lorentz transformation의 집합은 group 이다. 이를 Lorentz group 이라 하나. 여기에 spacetime translation 까지 포함하면 역시 group을 이루며 이를 Poincaré group 이라 한다.



From the invariance of the spacetime interval 로 부터,
$$
g'_{\mu\nu} dx'^\mu dx'^\nu = g_{\rho \sigma}dx^\rho dx^\sigma \tag{A.27}
$$
임을 안다. 또한 $dx'^\mu ={\Lambda^\mu}_\rho dx^\rho$ 이므로, 
$$
\begin{align*}
g_{\rho\sigma}dx^\rho dx^\sigma = g'_{\mu\nu} dx'^\mu dx'^\nu = g'_{\mu\nu} {\Lambda^\mu}_\rho {\Lambda^\nu}_\sigma dx^\rho dx^\sigma 
\end{align*}
$$
이다. 따라서,
$$
g'_{\mu \nu} {\Lambda^\mu}_\rho {\Lambda^\nu}_\sigma = g_{\rho \sigma}
$$
이것을 행렬로 쓰면,
$$
\Lambda^T g'\Lambda = g\tag{A.28}
$$
이 된다. 



우리는 $\det(g')=\det(g)=-1$ 임을 알고 있다. 도한 $\det(\Lambda^T)=\det(\Lambda)$ 임도 알고 있다. 따라서,
$$
\det (\Lambda)= \pm 1\tag{A.29}
$$
이다. 