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

2, 3에서도 같은 방법으로 보일 수 있다.



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
\oint_{\mathcal{S}} \mathbf{v}_2 \cdot d\mathbf{a} &=\int \dfrac{1}{R^2}R^2\sin\theta\,d\theta d\phi = 4\pi
\end{align*}
$$


<b>Problem 1.40</b> 다음 함수의 divergence를 구하시오.
$$
\mathbf{v}=(r\cos\theta)\hat{\mathbf{r}}+(r\sin\theta)\hat{\boldsymbol{\theta}}+(r \sin\theta \cos \phi)\hat{\boldsymbol{\phi}}
$$
이 함수에 대해서 divergence theorem을 확인하시오. 이 때 volume을 그림 1.40의 inverted hemispherical bowl of radius $R$ 을 사용하시오.

---

Using (1.71)
$$
\begin{align*}
\nabla \cdot \mathbf{v} &= \dfrac{1}{r^2} \dfrac{\part}{\part r}(r^3 \cos\theta) + \dfrac{1}{r\sin\theta} \dfrac{\part}{\part \theta}(r \sin^2\theta) + \dfrac{1}{r\sin\theta} \dfrac{\part}{\part \phi}(r \sin \theta \cos \phi) \\
&=3\cos\theta+2\cos\theta-\sin\phi = 5 \cos\theta - \sin \phi
\end{align*}
$$
이다.
$$
\int_{\mathcal{V}} \left( \nabla \cdot \mathbf{v} \right) d\tau = \int_0^R \int_0^{\pi/2} \int_0^{2\pi} r^2(5\cos \theta -\sin \phi)\sin\theta \,dr d\theta d\phi =\dfrac{5R^3}{3}\int_0^{\pi/2} \cos\theta \sin\theta\,d\theta d\phi=\dfrac{5\pi}{3}R^3\
$$
이다. 
$$
\int_{\mathcal{S}} \mathbf{v}\cdot d\mathbf{a}= \int_{\text{upper hemisphere}} \mathbf{v} \cdot \hat{\mathbf{r}}\,da_1 + \int_{\text{circir with radius }R\text{ and z=0}} \mathbf{v} \cdot (-\hat{\mathbf{z}})\, da_2
$$
upper hemisphere 에 대한 surface 적분 $da_1 = r\sin\theta\, drd\theta d\phi$ with $r=R$ 이며. $z=0$ 에서의 $r=R$ 에 대한 surface 적분 $da_2 = rdrd\phi$ with $\theta=\pi/2$ 이다. 따라서,
$$
\begin{align*}
\int_{\mathcal{S}} \mathbf{v}\cdot d\mathbf{a}&=\int_0^{\pi/2} \int_0^{2\pi} R^3 \cos\theta \sin\theta\, d\theta d\phi - \int_0^R \int_0^{2\pi} (r \cos^2 \theta -r \sin^2 \theta )_{\theta = \pi/2} r drd\phi\\
&=\pi R^3 + \dfrac{2\pi}{3}R^3=\dfrac{5\pi}{3}R^3


\end{align*}
$$


<b>Problem 1.46 </b>

(a) 다음을 보이시오
$$
x \dfrac{d}{dx}(\delta(x))=-\delta (x)\;.
$$
(b) step function $\theta(x)$ 가 다음과 같다.
$$
\theta (x) \equiv \left\{\begin{array}{ll} 1\,, \qquad&\text{if } x>0 \\ 0\,, & \text{if } x\le 0\end{array}\right.
$$
이 때 $d\theta/dx = \delta(x)$ 임을 보이시오.

---

(a) Using integration by parts,
$$
\int_{-\infty}^\infty x\dfrac{d}{dx}(\delta (x)) \, dx = \left[x\delta(x)\right]_0^\infty - \int\delta(x)\, dx=-1 \\
\int_{-\infty}^\infty f(x) x\dfrac{d}{dx}(\delta(x)) \,dx= \left[xf(x)\delta(x)\right]_0^\infty - \int (f(x)+xf'(x))\delta(x)\,dx=-f(0)
$$
(b) If we integrate $f(x) \theta'(x) = f(x)d\theta/dx$, 
$$
\int_{-\infty}^\infty f(x)\theta'(x) = \int_{-\epsilon}^\epsilon f(x)\theta'(x)dx=[f(x)\theta(x)]_{-\epsilon}^\epsilon-\int_{-\epsilon}^\epsilon f'(x)\theta(x)dx=f(\epsilon)-\int_{0}^\epsilon f'(x)dx=f(0)
$$




<b>Problem 1.49 </b> 다음 적분을 계산하시오.
$$
J=\int_{\mathcal{V}} e^{-r}\left(\nabla \cdot \dfrac{\hat{\mathbf{r}}}{r^2}\right) d\tau
$$
 여기서 $\mathcal{V}$ 는 원점을 중심으로 반경 $R$ 인 구이다. 두가지 다른 방법으로 계산하시오.

---

(1) $\nabla \cdot  \left(\dfrac{\hat{\mathbf{r}}}{r^2} \right) = 4\pi \delta^3 (\mathbf{r})$ 이므로, $J=\displaystyle \int_{\mathcal{V}} e^{-r} \cdot (4\pi \delta (\mathbf{r}))\, d\tau = 4\pi$.

(2) $\nabla (f \mathbf{v})=\mathbf{v} \cdot (\nabla f)+ f(\nabla \cdot \mathbf{v})$  이며, $\nabla e^{-r}=-e^{-r} \hat{\mathbf{r}}$ 이므로,
$$
\begin{align*}
J&=\int_{\mathcal{V}} \nabla \cdot (e^{-r} \dfrac{\hat{\mathbf{r}}}{r^2})\, d\tau -\int_{\mathcal{V}}(-e^{-r} \hat{\mathbf{r}})\cdot \dfrac{\hat{\mathbf{r}}}{r^2} \, d\tau  \\
&= \int_{\mathcal{S}} \dfrac{e^{-r}}{r^2}  r^2\sin\theta \, d\theta d \phi  + \int_{\mathcal{V}} \dfrac{e^{-r}}{r^2} \sin\theta r^2 drd\theta d\phi \\
&= 4\pi e^{-R } +4\pi [-e^{-r}]_{r=0}^{r=R}=4\pi\,.

\end{align*}
$$




<b>Problem 1.51</b> Theorem 1 에서 (d) $\implies$ (a), (a) $\implies$ (c), (c) $\implies$ (b), (b) $\implies$ (c), (c)$\implies$ (a) 임을 보이시오.

---

Theorem 1 : 아래 네 명제는 equivalent 하다.

(a) $\nabla \times \mathbf{F}=0$,

(b) $\int_{\mathbf{a}}^{\mathbf{b}} \mathbf{F}\cdot d\mathbf{l}$ 은 임의의 end points 에 대해 path-independent 하다.

(c) $\oint \mathbf{F}\cdot d\mathbf{l}=0$, 

(d) $\mathbf{F}$ 는 어떤 scalar function $V$ 에 대해 $\mathbf{F}=-\nabla V$ 이다.

(1) (d)$\implies$(a) : see problem 1.28.

(2) (a)$\implies$(c) : From Stoke's theorem, $\oint \mathbf{F}\cdot d\mathbf{l}=\int (\nabla \times \mathbf{F} )\cdot d\mathbf{a}=0$ 

(3) (c)$\implies$(b) : Let's fix $\mathbf{a}$ and $\mathbf{b}$ and choose a path $\Gamma_1$ from $\mathbf{a}$ to $\mathbf{b}$. For any arbitrary path $\Gamma_2$ from $\mathbf{a}$ to $\mathbf{b}$,
$$
\int_{\Gamma_1} \mathbf{F}\cdot d\mathbf{l}-\int_{\Gamma_2}\mathbf{F}\cdot d\mathbf{l}=\oint_{\Gamma_1-\Gamma_2} \mathbf{F}\cdot d \mathbf{l}=0 \implies \int_{\Gamma_1} \mathbf{F}\cdot d\mathbf{l}=\int_{\Gamma_2}\mathbf{F}\cdot d\mathbf{l}
$$
(4) (b)$\implies$(c) : trivial

(5) (c)$\implies$(a) : Trivial from Stoke's theorem. 



<b>Problem 1.52</b> 

Theorem 2에서. (d)$\implies$(a), (a)$\implies$(c), (c)$\implies$(b), (b)$\implies$(c), (c)$\implies$(a) 를 보이시오.

---

Theorem 2: 아래 네 명제는 equivalent 하다.

(a) $\nabla \cdot \mathbf{F}=0$ everywhere.

(b) $\int \mathbf{F}\cdot d\mathbf{a}$ is independent of surface, for any given boundary line.

(c)  $\oint \mathbf{F}\cdot d\mathbf{a}=0$ for any closed surface.

(d)  $\mathbf{F}$ is the curl of some vector function : $\mathbf{F}=\nabla \times \mathbf{A}$.

(1) (d)$\implies$(a) : seel problem 1.27

(2) (a)$\implies$(c) : Divergence theorem, $\int_{\mathcal{V}} (\nabla \cdot \mathbf{F})=\int_{\mathcal{S}} \mathbf{F}\cdot d\mathbf{a}$, 

(3) (c)$\implies$(b) : boundary line을 경계로 하는 두 closed surface를 생각하라.

(4) (b)$\implies$(c) : 어떤 closed surface를 임의의 boundary line으로 이분할하는것을 생각하라

(5) (c)$\implies$(a) : divergende theorem





##  More Problems on Chapter I.

<b>Problem 1.61 </b>

Gradient, divergence, curl theorem으로 부터 몇가지 colloraries를 유도하라.

(a) $\int_{\mathcal{V}} (\nabla T)\, d\tau =\oint T d\mathbf{a}$ ,

(b) $\int_{\mathcal{V}} (\nabla \times \mathbf{v})d\tau = -\oint_{\mathcal{S}} \mathbf{v} \times d\mathbf{a}$, 

(c) $\int_{\mathcal{V}} [T\nabla^2 U+(\nabla T)\cdot (\nabla U)]\,d\tau = \oint_{\mathcal{S}} (T\nabla U)\cdot d\mathbf{a}$ , 

(d) $\int_{\mathcal{V}} (T\nabla^2 U-U\nabla^2 T)d\tau = \oint_{\mathcal{S}} (T\nabla U - U \nabla T)\cdot d\mathbf{a}$ ,

(e) $\int_\mathcal{S} \nabla T \times d\mathbf{a}=-\oint_{\mathcal{P}} T d\mathbf{l}$.

---

(a) Let $\mathbf{v} = \mathbf{c}T$ where $\mathbf{c}$ is a constant vector. Then,
$$
\int_{\mathcal{V}} \nabla\cdot (\mathbf{c}T)\,d\tau= \mathbf{c} \cdot\int_{\mathcal{V}} (\nabla T)\, d\tau
$$
From divergence theorem, 
$$
\int_{\mathcal{V}} \nabla \cdot (\mathbf{c}T)\,d\tau = \oint_{\mathcal{S}} T\mathbf{c}\cdot d\mathbf{a}=\mathbf{c} \cdot\oint_{\mathcal{S}} T\,d\mathbf{a}
$$
$\mathbf{c}$ 가 임의의 vector 이므로 (a)가 성립한다.

(b) From hint, let $\mathbf{c}$ be any constant vector. Then, 
$$
\nabla \cdot(\mathbf{v}\times \mathbf{c}) = \mathbf{c} \cdot (\nabla \times \mathbf{v})\,.
$$
이로부터, 양 변을 부피 $\mathcal{L}$ 에 대해 적분했을 때 
$$
\begin{align*}
\int_\mathcal{V} \nabla \cdot (\mathbf{v}\times \mathbf{c})\, d\tau &=\oint_{\mathcal{S}} (\mathbf{v}\times \mathbf{c})\cdot d\mathbf{a}=-\mathbf{c}\cdot\oint_\mathcal{S} \mathbf{v} \times d\mathbf{a}\,,\\
\end{align*}
$$
이며 우변은 $\displaystyle \mathbf{c} \cdot \int_\mathcal{V} (\nabla \times \mathbf{v})\, d\tau$ 이므로 증명 끝.

(c) 다음에 대해 divergence theorem을 적용하면 된다.
$$
\nabla\cdot(T \nabla U)=T \nabla^2 U+(\nabla T)\cdot (\nabla U)\;.
$$
(d) (c)의 식과 $\nabla \cdot (U\nabla T)=U \nabla^2 T + (\nabla T)\cdot (\nabla U)$ 를 이용하면 끝.

(e) 임의의 nonzero constant vector $\mathbf{c}$ 에 대해 $\mathbf{v} = \mathbf{c}T$ 라 하자. $\nabla \times (\mathbf{c}T)=-\mathbf{c} \times \nabla T$ 이므로,
$$
\begin{align*}
\int_\mathcal{S} \nabla \times (\mathbf{c}T)\cdot d\mathbf{a} &=\mathbf{c} \cdot\oint_{\mathcal{P}}  T\,d\mathbf{l}\qquad&\text{by Stoke's theorem,}\\
&=- \int_\mathcal{S} (\mathbf{c} \times\nabla T) \cdot d\mathbf{a} = -\mathbf{c} \cdot \int_\mathbf{S} \nabla T \times d\mathbf{a}\, &\text{From identity above,}

\end{align*}
$$




<b>Problem 1.62 </b> 다음 적분
$$
\mathbf{a} \equiv \int_\mathcal{S} d\mathbf{a}
$$
를 surface $\mathcal{S}$ 에 대한 **vector area** 라고 하기도 한다. 만약 $\mathcal{S}$ 가 평평하다면 $|\mathbf{a}|$ 는 우리가 통상적으로 말하는 area 이다.

(a) Hemispherical bowl of radius $R$ 에 대한 vector area를 구하라.

(b) 임의의 closed surface에 대해 $\mathbf{a}=0$ 임을 보여라.

(c) $\mathbf{a}$ 는 boundary를 공유하는 임의의 surface에 대해 동일함을 보여라.

(d)