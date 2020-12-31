Appendix A. & B 
===

## Appendix A. Scalars, Vectors, Tensors, and Coordinate Transformations






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



