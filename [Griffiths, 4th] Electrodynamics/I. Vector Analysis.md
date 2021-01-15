I. Vector Analysis
===



Griffiths의 분리벡터를 표기하기가 힘드므로 여기서는 $\boldsymbol{\xi}=\mathbf{r}-\mathbf{r}'$ 으로 쓰기로 하자.

## 1. Vector Algebra





## 2. Differential Calculus

<b> Problem 1.13</b> $\boldsymbol{\xi}=\mathbf{r}-\mathbf{r}'$ 이며 $\xi =|\boldsymbol{\xi}|$ 일 때 다음을 보이시오.

(a) $\nabla (\xi^2)=2\boldsymbol{\xi}$, 

(b) $\nabla(1/\xi)=-\hat{\boldsymbol{\xi}}/\xi^2$, 

(c) $\nabla (\xi^n)$ 에 대한 일반식은?

---

(a) $\nabla (\xi^2) = \sum_i\hat{\boldsymbol{e}}_i\partial_i (\sum_j(x_j-x'_j)^2)=\sum_{i,\,j}2(x_j-x'_j)\delta_{ij}\hat{\boldsymbol{e}}_i=2\boldsymbol{\xi}$.

(b) $\nabla (1/\xi) = \sum_i \hat{\boldsymbol{e}_i}\partial_i \left(\dfrac{1}{\sqrt{\sum_j(x_j-x'_j)^2}}\right)=\sum_i \hat{\boldsymbol{e}}_i \dfrac{-(x_j-x'_j)}{\xi^{3/2}}\delta_{ij}=-\widehat{\boldsymbol{\xi}}/\xi^2$.

(c) $\nabla (\xi^n)=\sum_i \hat{\boldsymbol{e}}_i \partial_i \left(\sum_j (x_j-x'_j)^2\right)^{n/2} = \sum_i \hat{\boldsymbol{e}}_i  n\delta_{ij}\left(\sum_j\left(x_j-x'_j\right) \right)\xi^{n-2}=n\xi^{n-1}\hat{\boldsymbol{\xi}}$.



<b>Problem 1.14</b> $f=f(y,\,z)$ 일 때 shows that the gradient $\nabla f = \partial_y f \hat{\mathbf{y}}+\partial_z f \hat{\mathbf{z}}$ transforms as a vector under rotation 임을 보이시오.

---

Consider rotation along $x$ axis by $y'=\cos \phi y + \sin \phi z$ and $z'=-\sin \phi y+ \cos \phi z$. Then,
$$
\partial_y=\cos \phi \partial'_y + \sin \phi \partial'_z \,,\quad \partial_z = -\sin\phi {\partial'_y}+\cos \phi \partial'_z\,.
$$
 따라서,
$$
\begin{align*}
\nabla f &= \hat{\mathbf{y}}\partial_y f+\hat{\mathbf{z}}\partial_z f\\
&= (\hat{\mathbf{y}}' \cos \phi + \hat{\mathbf{z}}'\sin \phi)(\cos \phi \partial'_y f+ \sin \phi \partial'_z f) + (-\sin \phi\hat{\mathbf{y}}'  + \cos \phi\hat{\mathbf{z}}')(-\sin \phi \partial'_y f +\cos \phi \partial'_z f)\\
&=\hat{\mathbf{y}}'(\partial'_y f)+\hat{\mathbf{z}}'\partial_z' f = \nabla'f
\end{align*}
$$


<b>Problem 1.17</b> In two dimension, show that the divergence transforms as a scalar under rotation

---

Use same notation in problem 1.14. Let $\boldsymbol{v}(y,\,z)=(v_1(y,\,z),\, v_2(y,\,z))$ 
$$
\begin{align*}
\nabla \cdot \boldsymbol{v} &=\partial_1 v_1+\partial_2 v_2 \\
&= (\cos \phi \part_1' v_1+ \sin \phi \part_2'v_1)+(-\sin \phi \partial_1' v_2 +\cos \phi \part_2' v_2) \\
&=\partial_1' (\cos \phi v_1 - \sin \phi v_2) + \part_2'(\sin \phi v_1 + \cos \phi v_2 ) \\
&=


\end{align*}
$$
