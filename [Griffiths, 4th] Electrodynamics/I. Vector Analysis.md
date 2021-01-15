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
\partial_y=\cos \phi \partial'_y - \sin \phi \partial'_z \,,\quad \partial_z = \sin\phi {\partial'_y}+\cos \phi \partial'_z\,.
$$
또한,
$$
\hat{\mathbf{y}}'=\cos \phi \hat{\mathbf{y}}+\sin \phi \hat{\mathbf{z}}\,,\quad \hat{\mathbf{z}}'=-\sin \phi \hat{\mathbf{y}}+\cos \phi \hat{\mathbf{z}}\\
\hat{\mathbf{y}}=\cos \phi \hat{\mathbf{y}}'-\sin \phi \hat{\mathbf{z}}'\,,\quad \hat{\mathbf{z}}=\sin \phi \hat{\mathbf{y}}'+\cos \phi \hat{\mathbf{z}}'
$$


따라서,
$$
\begin{align*}
\nabla f &= \hat{\mathbf{y}}\partial_y f+\hat{\mathbf{z}}\partial_z f\\
&= (\hat{\mathbf{y}}' \cos \phi - \hat{\mathbf{z}}'\sin \phi)(\cos \phi \partial'_y f - \sin \phi \partial'_z f) + (\sin \phi\hat{\mathbf{y}}'  + \cos \phi\hat{\mathbf{z}}')(\sin \phi \partial'_y f +\cos \phi \partial'_z f)\\
&=\hat{\mathbf{y}}'(\partial'_y f)+\hat{\mathbf{z}}'\partial_z' f = \nabla'f
\end{align*}
$$



<b>Problem 1.16</b> vector function
$$
\mathbf{v} = \dfrac{\hat{\mathbf{r}}}{r^2}
$$
을 스케치하고 그 divergence를 계산하시오.

----

$$
\sum_i\partial_i v_i = \sum_i\partial_i \left( \dfrac{x_i}{r^3} \right)= \sum_i\dfrac{1}{r^3}-\dfrac{3x_i^2}{r^5}=0\;.
$$









<b>Problem 1.17</b> In two dimension, show that the divergence transforms as a scalar under rotation

---

Use same notation in problem 1.14. Let $\boldsymbol{v}(y,\,z)=(v_1(y,\,z),\, v_2(y,\,z))$ 
$$
\begin{align*}
\nabla \cdot \boldsymbol{v} &=\partial_1 v_1+\partial_2 v_2 \\
&= (\cos \phi \part_1' v_1- \sin \phi \part_2'v_1)+(\sin \phi \partial_1' v_2 +\cos \phi \part_2' v_2) \\
&=\partial_1' (\cos \phi v_1 + \sin \phi v_2) + \part_2'(-\sin \phi v_1 + \cos \phi v_2 ) \\
&=\part_1' v_1' +\part_2' v_2' \\
&=\nabla' \cdot \boldsymbol{v}'


\end{align*}
$$



<b>Problem 1.21</b> Text의 pruduct rule (i), (iv), (v)를 증명하시오.
$$
\begin{align*}
\nabla(fg) &=f\,\nabla g + g\, \nabla f\tag{i}\,,\\
\nabla \cdot (\mathbf{A} \times \mathbf{B}) &=\mathbf{B} \cdot (\nabla \times \mathbf{A})-\mathbf{A} \cdot (\nabla \times \mathbf{B})\,, \tag{iv}\\
\nabla \times (f\mathbf{A})&=f(\nabla \times \mathbf{A})-\mathbf{A} \times (\nabla f)\,. \tag{v}
\end{align*}
$$

---

$$
\begin{align*}
\nabla (fg) &= \sum_{i}\hat{\mathbf{e}}_i \partial_i (fg)=\sum_i \hat{\mathbf{e}}_i(g\cdot\partial_i f +f \cdot\partial_i f) =f\, \nabla g + g\, \nabla f\\

\nabla \cdot (\mathbf{A} \times \mathbf{B})&= \sum_i \varepsilon_{ijk} \partial_i (A_jB_k) =\sum_i  \varepsilon_{ijk} \left(A_j \partial_iB_k + B_k \partial_i A_j\right) \\
&= \sum_i \varepsilon_{ijk} B_k\partial_i A_j + \sum_{i}\varepsilon_{ijk}(A_j \partial_i B_k)\\
&=\mathbf{B} \cdot (\nabla \times \mathbf{A})-\mathbf{A} \cdot (\nabla \times \mathbf{B})\,. \\
\nabla \times (f\mathbf{A}) &= \sum_i \varepsilon_{ijk}\hat{\mathbf{e}}_i \partial_j (fA_k) = \sum_i \varepsilon_{ijk}\hat{\mathbf{e}_i} (A_k\partial_j f+f\partial_jA_k) \\
&=\sum_i \varepsilon_{ijk} \hat{\mathbf{e}_i }A_k \partial _j f + \sum_{i}\varepsilon_{ijk} \hat{\mathbf{e}_i} f\partial_j A_k \\
&=-\mathbf{A} \times(\nabla f)+f(\nabla \times \mathbf{A})
\end{align*}
$$



<b>Problem 1.22</b> 

(a) $\mathbf{A},\, \mathbf{B}$ 가 두 vector functions 일 때 $(\mathbf{A} \cdot \nabla ) \mathbf{B}$ 가 의미하는 것은 무엇인가?

(b) $\hat{\mathbf{r}}$ 이 unit vector defined in Eq. 1.21 일 때 $(\hat{\mathbf{r}}\cdot \nabla) \hat{\mathbf{r}}$ 가 의미하는 것은 무엇인가?

---

(a) $\left[(\mathbf{A}\cdot \nabla )\mathbf{B}\right]_i= \left(\sum_j A_j \partial_j\right) B_i$  

(b) $\left[(\hat{\mathbf{r}}\cdot \nabla) \hat{\mathbf{r}}\right]_i = \left(\sum_j \dfrac{x_j}{r} \partial_j\dfrac{x_i}{r}\right)=\sum_j \dfrac{x_j}{r} \left(\dfrac{\delta_{ij}}{r}-\dfrac{x_i x_j}{r^3} \right)$



<b>Problem 1.23 </b> product rule (ii)와 (vi)를 증명하시오.
$$
\begin{align*}
\nabla(\mathbf{A}\cdot \mathbf{B}) &=\mathbf{A} \times (\nabla \times \mathbf{B})+\mathbf{B} \times (\nabla \times \mathbf{A}) + (\mathbf{A}\cdot \nabla)\mathbf{B}+ (\mathbf{B}\cdot \nabla)\mathbf{A} \tag{ii} \\
\nabla \times (\mathbf{A}\times \mathbf{B})&=(\mathbf{B}\cdot \nabla)\mathbf{A} -(\mathbf{A}\cdot \nabla)\mathbf{B} + \mathbf{A}(\nabla \cdot \mathbf{B})-\mathbf{B}(\nabla \cdot \mathbf{A}) \tag{vi}
\end{align*}
$$

---

$$
\begin{align*}
\mathbf{A} \times (\nabla \times \mathbf{B}) &+\mathbf{B} \times (\nabla \times \mathbf{A}) + (\mathbf{A}\cdot \nabla)\mathbf{B}+ (\mathbf{B}\cdot \nabla)\mathbf{A} \\
&=\varepsilon_{ijk} A_j\varepsilon_{klm}\partial_l B_m
 + \varepsilon_{ijk}B_j\varepsilon_{klm} \part_lA_m + A_j\partial_j B_i + B_j \part_j A_i \\
 &=(\delta_{il}\delta_{jm}-\delta_{im}\delta_{jl})A_j (\partial_l B_m) +(\delta_{il}\delta_{jm}-\delta_{im}\delta_{jl}) (\partial_lA_m)B_j + A_j \partial_jB_i + B_j\partial_j A_i \\
 &=A_j \partial_i B_j-A_j\partial_jB_i + B_j\partial_iA_j-B_j\part_jA_i +A_j \part_jB_i + B_j \part_j A_i \\
 &=A_j \part_i B_j +B_j\part_i A_j = \nabla (\mathbf{A}\cdot \mathbf{B})

\end{align*}
$$

$$
\begin{align*}
\left[\nabla \times (\mathbf{A}\times \mathbf{B})\right]_i &= \varepsilon_{ijk} \part_j \left(\varepsilon_{klm} A_l B_m\right) = (\delta_{il}\delta_{jm}-\delta_{im}\delta_{jl}) \part_j(A_lB_m) \\
&=\partial_j(A_iB_j) - \partial_j(A_jB_i)=B_j\partial_jA_i+A_i\partial_jB_j - B_i\partial_jA_j-A_j\partial_jB_i \\
&=\left[ (\mathbf{B}\cdot\nabla)\mathbf{A} +\mathbf{A}(\nabla \cdot \mathbf{B})-\mathbf{B}(\nabla \cdot \mathbf{A}) -(\mathbf{A}\cdot \nabla) \mathbf{B}   \right]_i

\end{align*}
$$



<b>Problem 1.24</b> Three quotient rules를 증명하라.

---

$$
\begin{align*}
\nabla \left(\dfrac{f}{g}\right)&= \sum_i \hat{\mathbf{e}}_i \partial_i \left(\dfrac{f}{g}\right)=\sum_i \hat{\mathbf{e}}_i \dfrac{g\,\partial_i f -f\, \partial_i g}{g^2} = \dfrac{g\nabla f - f \nabla g}{g^2}\,,\\
\nabla\cdot \left(\dfrac{\mathbf{A}}{g}\right) &=\sum_i \partial_i \left(\dfrac{A_i}{g}\right) = \sum_i \dfrac{g\partial_i A_i -A_i \partial_i g}{g^2} = \dfrac{g(\nabla \cdot \mathbf{A})-\mathbf{A}\cdot (\nabla g)}{g^2}\,,\\
\left[\nabla \times \left(\dfrac{\mathbf{A}}{g}\right)\right]_i &= \varepsilon_{ijk}\partial_j \left(\dfrac{A_k}{g}\right) = \varepsilon_{ijk}\dfrac{g\,\part_j A_k-A_k \part_jg}{g^2} = \dfrac{g(\nabla\times \mathbf{A}) +\mathbf{A} \times (\nabla g)}{g^2}\;.
\end{align*}
$$





<b>Problem 1.27 </b> Divergence of a curl은 항상 $0$ 임을 보이시오.

---

Let $\mathbf{A}$ be any vector function.
$$
\begin{align*}
\nabla \cdot (\nabla \times \mathbf{A})&=\sum_i \part_i (\varepsilon_{ijk} \part_j A_k)=\sum_i \varepsilon_{ijk} (\part_i \part_j A_k) \\
&=(\part_1\part_2 A_3-\part_2\part_1A_3)+(\part_2\part_3 A_1-\part_3\part_2A_1)+(\part_3\part_1A_2-\part_1\part_3A_2)=0

\end{align*}
$$


<b>Problem 1.28</b> Curl of a gradient 는 항상 $0$ 임을 보이시오.

---

Let $f$ be any scalar function. Then,
$$
\left[\nabla \times (\nabla f)\right]_1= \varepsilon_{1jk} \part_j \part_k f= \part_2\part_3 f-\part_3\part_2f=0
$$


## 3. Integral calculus

<b>Problem 1.36</b> 다음을 보이시오.
$$
\int_S f(\nabla \times \mathbf{A})\cdot d\mathbf{a}=\int_S \left[\mathbf{A} \times (\nabla f)\right] \cdot d\mathbf{a}  + \oint_\mathcal{P} f\mathbf{A}\cdot d\mathbf{l}\,, \\
\int_\mathcal{V} \mathbf{B}\cdot (\nabla \times \mathbf{A}) \, d\tau =\int_{\mathcal{V}} \mathbf{A} \cdot (\nabla \times \mathbf{B})\, d\tau + \oint_\mathcal{S} (\mathbf{A} \times \mathbf{B}) \cdot d\mathbf{a}\,.
$$

---

From $\nabla \times (f\mathbf{A})=f(\nabla  \times \mathbf{A})-\mathbf{A}\times (\nabla f)$, 
$$
\oint_{\mathcal{P}} f\mathbf{A}\cdot d\mathbf{l}=\int_S \left[\nabla \times (f\mathbf{A})\right] \cdot d\mathbf{a}= \int_{\mathcal{S}} f(\nabla \times \mathbf{A})\, \cdot d\mathbf{a} -\int_{\mathcal{S}} \left[\mathbf{A}\times (\nabla f)\right] \cdot d\mathbf{a}\,.
$$
From $\nabla  \cdot (\mathbf{A}\times \mathbf{B}) = \mathbf{B} \cdot (\nabla \times \mathbf{A})-\mathbf{A}\cdot (\nabla \times \mathbf{B})$,
$$
\oint_{\mathcal{S}} (\mathbf{A}\times \mathbf{B})\cdot d\mathbf{a}= \int_\mathcal{V}\left[\nabla \cdot (\mathbf{A} \times \mathbf{B})\right] \ d\tau =\int_{\mathcal{V}} \mathbf{B}\cdot (\nabla \times \mathbf{A}) \,d\tau -\int_{\mathcal{V}} \mathbf{A}\cdot (\nabla \times \mathbf{B})\, d\tau\,.
$$


## 4. Curvilinear coordinates

<b>Problem 1.37</b> $r,\,\theta,\,\phi$ 를 $x,\,y,\,z$ 로 표시하시오.

---

$$
\begin{align*}
r&=\sqrt{x^2+y^2+z^2}\,,\\
\theta &= \arctan(\sqrt{x^2+y^2}/z)\,,\\
\phi &= \arctan(x/y)\,.

\end{align*}
$$



<b>Problem 1.38 </b> Unit vectors $\hat{\mathbf{r}},\,\hat{\boldsymbol{\theta}},\,\hat{\boldsymbol{\phi}}$ 를 $\hat{\mathbf{x}},\,\hat{\mathbf{y}},\,\hat{\mathbf{z}}$ 로 표시하시오.

---

Let 
$$
\begin{align*}
\hat{\mathbf{r}} &= a_{11}\hat{\mathbf{x}}+a_{12}\hat{\mathbf{y}}+a_{13}\hat{\mathbf{z}}\,,\\
\hat{\boldsymbol{\theta}}&=a_{21}\hat{\mathbf{x}}+a_{22}\hat{\mathbf{y}}+a_{23}\hat{\mathbf{z}}\,,\\
\hat{\boldsymbol{\phi}}&=a_{31}\hat{\mathbf{x}}+a_{32}\hat{\mathbf{y}}+a_{33}\hat{\mathbf{z}}\,,\\
\end{align*}
$$
From Fig. 1.36 in the text, we know that 
$$
a_{11}=\hat{\mathbf{r}}\cdot \hat{\mathbf{x}} = \sin \theta \cos\phi,\quad a_{12}=\hat{\mathbf{r}}\cdot \hat{\mathbf{y}}= \sin \theta \sin \phi,\quad a_{13}=\hat{\mathbf{r}}\cdot \hat{\mathbf{z}}=\cos \theta\,,\\
a_{21}=\hat{\boldsymbol{\theta}}\cdot \hat{\mathbf{x}}=\cos \theta \cos \phi,\quad a_{22}=\hat{\boldsymbol{\theta}}\cdot\hat{\mathbf{y}}=\sin \theta \sin \phi,\quad a_{23}=\hat{\boldsymbol{\theta}}\cdot \hat{\mathbf{z}}=-\sin\theta\,\\
a_{31}=\hat{\boldsymbol{\phi}}\cdot \hat{\mathbf{x}}= - \sin \phi,\quad a_{32}=\hat{\boldsymbol{\phi}}\cdot \hat{\mathbf{y}}=\cos \phi,\quad a_{33}=\hat{\boldsymbol{\phi}}\cdot \hat{\mathbb{z}}=0
$$



<b>Problem 1.39</b> (a) $\mathbf{v}_1=r^2\hat{\mathbf{r}}$ 에 대해 divergence theorem이 성리하는지 보이시오. 이 때 반경 $R$ 의 원점을 중심으로 하는 구를 부피로 삼으시오.

(b) $\mathbf{v}_2=1/r^2 \hat{\mathbf{r}}$ 에 대해 (a) 와 같이 하시오.

---

(a) 
$$
\begin{align*}
\int_\mathcal{V} \nabla \cdot \mathbf{v}_1 \, d\tau &= \int_0^R\int_0^\pi \int_0^{2\pi} \dfrac{1}{r^2}\dfrac{\part}{\partial r}\left(r^4\right) r^2 \sin\theta\, dr d\theta d\phi = 4\pi \int_0^R 4r^3\, dr=4\pi R^4\,,\\
\oint_{\mathcal{S}} \mathbf{v}_1 \cdot \hat{\mathbf{n}} da &=\oint_{\mathcal{S}} r^2  \hat{\mathbf{n}}\cdot \hat{\mathbf{r}} \, da =4\pi R^4\,.

\end{align*}
$$
 (b)
$$
\begin{align*}
\int_{\mathcal{V}} \nabla\cdot \mathbf{v}_2 \,d\tau &=\int_0^R \int_0^\pi \int_0^{2\pi} \dfrac{1}{r^2}\dfrac{\part}{\part r}\left(\dfrac{1}{r^2} r^2\right)r^2 \,dr d\theta d\phi=0\,,\\
\oint_{\mathcal{S}} \mathbf{v}_2 \cdot d\mathbf{a} &=\int
\end{align*}
$$
