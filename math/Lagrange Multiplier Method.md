Lagrange Multiplier Method
===



#### Theorem 1. 

$f,\,g: U \subset \mathbb{R}^n \to \mathbb{R}$ 이 모두 $C^1$ class function이고 $S=\{ \mathbf{x}\in U : g(\mathbf{x})=0\}$ 이라 하자. $f$ 는 $S$에서만 의미가 있다고 가정하자. $\mathbf{x}_0 \in S$ 이고 $\nabla g(\mathbf{x}_0)\ne 0$ 일 때  $f|_S$ 가 $\mathbf{x}_0$에서 local maximum(or minimum)을 가지면 다음을 만족하는  $\lambda \in \mathbb{R}$이 존재한다. 
$$
\nabla f(\mathbf{x}_0) = \lambda (\nabla g(\mathbf{x}_0))
$$

---

*(Proof)* (1)  $\mathbf{c}(t)$를 $S$에서 정의된 임의의 path이며 $\mathbf{c}(0)=\mathbf{x}_0$ 라 하자. $\mathbf{c}'(t)$는 $S$에서의 vector 이므로
$$
\begin{align*}
\dfrac{d}{dt}g(\mathbf{c}(t)) &= \dfrac{d}{dt}0 = 0\\
\left. \dfrac{d}{dt}g(\mathbf{c}(t))\right|_{t=0} &= \nabla g(\mathbf{x}_0)\cdot \mathbf{c}'(0)\;.

\end{align*}
$$
이다. 따라서 $\nabla g(\mathbf{x}_0)$와 $\mathbf{c}'(0)$ 는 perpendicular 하다.

(2) $f_S$는 $\mathbf{x}_0$에서 local maximum/minimum 을 가지므로 
$$
\left.\dfrac{d}{dt} f_S(\mathbf{c}(t))\right|_{t=0}=0=\nabla f(\mathbf{x}_0)\cdot \mathbf{c}'(0)\;.
$$
(3) From (1) and (2), $\nabla g(\mathbf{x}_0)$ 와 $\nabla f(\mathbf{x}_0)$는 parallel 하며 $\nabla g(\mathbf{x}_0)\ne 0$ 이므로 $\nabla f(\mathbf{x}_0)=\lambda (\nabla g(\mathbf{x}_0))$ 를 만족하는 $\lambda\in \mathbb{R}$ 이 존재한다. $\qquad \square$



#### Corollary 2.

$f:U\subset \mathbb{R}^n \to \mathbb{R}$이 surface $S$에 제한되어 있으며 $\mathbf{x}_0\in S$ 에서 local maximum/minimum 을 가지면 $\nabla f(\mathbf{x}_0)$는 surface $S$에 $\mathbf{x}_0$에서 perpendicular 하다.

---

*(Proof)* Theorem 1의 증명 과정에서 우리는 $\mathbf{c}(t)$ 에 대해 $S$에서 정의되었다는 것 이상의 조건을 걸지 않았다. 즉 $S$에서 정의된 임의의 path에 대해 성립하므로 $\nabla f(\mathbf{x}_0)$는 $S$에 perpendicular at $\mathbf{x}_0$ 이다. $\qquad\square$



#### Note

From $\nabla f(\mathbf{x}_0)= \lambda (\nabla g(\mathbf{x}_0))$, 
$$
\dfrac{\partial f}{\partial x_i}(\mathbf{x}_0)= \lambda \dfrac{\partial g}{\partial x_i} (\mathbf{x}_0) \qquad \text{for } i=1,\ldots,\,n\;.
$$


#### Several Constraints

$f$가 다수의 constraint에 의해 정의되는 surface $S$에서 의미가 있다고 하자. 이 때 constraints가 $g_j (\mathbf{x})=0$ for $j=1,\ldots,\,m$ 으로 주어진다고 하자. $f$가 $\mathbf{x}_0$ on $S$에서 local maximum/minimum을 가진다면 다음을 만족하는 $\lambda_1,\ldots,\,\lambda_m \in\mathbb{R}$이 존재한다. 
$$
\nabla f(\mathbf{x}_0)= \lambda_1 (\nabla g_1 (\mathbf{x}_0))+ \cdots + \lambda_m (\nabla g_m (\mathbf{x}_0))\;.
$$
