VIII. 삼차원 공간과 벡터의 외적
==



## 연습문제 : 제 8 장 1 절



<b>1. </b> ~ <b>7. </b> 까지는 단순계산이므로 생략



<b>8. </b> 삼차원 공간의 두 벡터 $\mathbf{a},\,\mathbf{b}$ 가 일차독립일 필요충분조건은 $\mathbf{a}\times \mathbf{b} \ne \mathbf{0}$ 임을 보이라.

---

$\mathbf{a},\,\mathbf{b}$ 가 일차종속일 필요충분조건이 $\mathbf{a}\times \mathbf{b}=0$ 임을 보이는것과 동치이다. 우선 $\mathbf{a}$ 혹은 $\mathbf{b}$ 가 일차종속임을 가정하자. 둘 중 하나가 $\mathbf{0}$  이면 $\mathbf{a} \times \mathbf{b}=0$ 이다. 이제 둘 다 $\mathbf{0}$ 이 아닌 벡터에 대해 생각하자. $\mathbf{a},\,\mathbf{b}$ 가 일차종속이면 어떤 scalar $c$ 에 대해 $\mathbf{a}=c\mathbf{b}$ 이며, 따라서 $\mathbf{a} \times \mathbf{b}=0$ 이다. 

이제 $\mathbf{a} \times \mathbf{b}=0$ 임을 가정하자. 둘 중 하나가 $\mathbf{0}$ 이면 일차종속이므로 둘 다 $\mathbf{0}$ 이 아닌 상태만 생각하면 된다. $|\mathbf{a}\times \mathbf{b}|=|\mathbf{a}||\mathbf{b}||\sin \theta|$ 이므로 $\theta = 0$ 이다. 두 벡터가 평행하므로 일차종속이다.



<b>9. </b> 삼차원 공간의 임의의 벡터 $\mathbf{a},\,\mathbf{b},\,\mathbf{c},\,\mathbf{d}$ 에 대하여 다음 식이 성립함음 보이라.

---

Levi-Civita 개념을 사용한다. google 검색..
$$
\begin{align}
(a)\qquad \qquad &(\mathbf{a}\times (\mathbf{b}\times \mathbf{c}))_i =\epsilon_{ijk}a_j(\epsilon_{klm}b_lc_m)=(\delta_{il}\delta_{jm}-\delta_{im}\delta_{jl})a_jb_lc_m = a_jb_ic_j-a_jb_jc_i=(\mathbf{a}\cdot \mathbf{c})b_i-(\mathbf{a}\cdot \mathbf{b})c_i\\
\implies &\mathbf{a} \times(\mathbf{b}\times \mathbf{c})=(\mathbf{a}\cdot \mathbf{c})\mathbf{b}-(\mathbf{a}\cdot \mathbf{b})\mathbf{c}\\
(b) \qquad \qquad & ((\mathbf{a}\times \mathbf{b})\times \mathbf{c})_i = \epsilon_{ijk}\epsilon_{jlm} a_lb_m c_k = (\delta_{kl}\delta_{im}-\delta_{km}\delta_{il})a_lb_mc_k = a_kb_ic_k-a_ib_kc_k = (\mathbf{a}\cdot \mathbf{c})b_i - (\mathbf{b}\cdot \mathbf{c})a_i \\
\implies & (\mathbf{a}\times \mathbf{b})\times \mathbf{c}=(\mathbf{a}\cdot \mathbf{c})\mathbf{b}-(\mathbf{b}\cdot \mathbf{c})\mathbf{a}\\
(c)\qquad \qquad & (\mathbf{a}\times \mathbf{b})\cdot (\mathbf{c \times \mathbf{d}}) = \epsilon_{ijk} a_jb_k  \epsilon_{ilm}c_ld_m = (\delta_{jl}\delta_{km}-\delta_{jm}\delta_{kl})a_jb_k c_ld_m = a_jb_k c_j d_k-a_jb_kc_kd_j \\
&=(\mathbf{a}\cdot \mathbf{c})(\mathbf{b}\cdot \mathbf{d})-(\mathbf{a}\cdot \mathbf{d})(\mathbf{b}\cdot \mathbf{c})\\
(d) \qquad \qquad & \mathbf{a}\times(\mathbf{b}\times \mathbf{c}) + \mathbf{b}\times (\mathbf{c}\times \mathbf{a}) +\mathbf{c}\times (\mathbf{a} \times \mathbf{b})=(\mathbf{a}\cdot \mathbf{c})\mathbf{b}-(\mathbf{a}\cdot \mathbf{b})\mathbf{c}+(\mathbf{b}\cdot \mathbf{a})\mathbf{c}-(\mathbf{b}\cdot \mathbf{c})\mathbf{a} + (\mathbf{c}\cdot \mathbf{b})\mathbf{a}-(\mathbf{c}\cdot \mathbf{a})\mathbf{b}=0
\end{align}
$$


<b>10. </b> 삼차원공간에서 양으로 향한 정규직교기저 $\mathbf{v}_1,\,\mathbf{v}_2,\,\mathbf{v}_3$ 에 대하여,
$$
\mathbf{a}=\sum_{i=1}^3 a_i\mathbf{v}_i,\qquad \mathbf{b}=\sum_{j=1}^n b_j \mathbf{v}_j
$$
일 때,
$$
\mathbf{a}\times \mathbf{b} =\sum_{i,j,k=1}^3 \epsilon_{ijk} a_ib_j \mathbf{v}_k
$$
임을 보이라.

---

$$
\mathbf{a}\times \mathbf{b}=\sum_{i}\sum_j a_ib_j (\mathbf{v}_i \times \mathbf{v}_j)=\sum_{i,j,k}a_ib_j\epsilon_{ijk} \mathbf{v}_k
$$



<b>11. </b> 공간속의 한 사면체 $ABCD$ 의 의 면 $BCD$ 에 대하여, 크기가 이 면의 넓이와 같고, 이 면에 수직이고, 방향은 사면체의 밖을 향하는 벡터 $\mathbf{v}_A$ 를 생각하자. 마찬가지로 각 면 $CDA,\,DAB,\,ABC$ 에 대하여 벡터 $\mathbf{v}_B,\,\mathbf{v}_C,\,\mathbf{v}_D$ 가 정의도었을 때,
$$
\mathbf{v}_A+\mathbf{v}_B+\mathbf{v}_C+\mathbf{v}_D=0
$$
임을 보이라.

---

사면체에서 $ABC$ 가 시계방향인지 반시계 방향인지, $\overrightarrow{AD}\cdot (\overrightarrow{BA}\times \overrightarrow{CA})$ 가 양수인지 음수인지 에 대해 각각의 $\mathbf{v}_{X}\;(X=A,\,B,\,C,\,D) $ 벡터를 표현하는  식이 달라진다. 

사면체의 꼭지점의 좌표가 주어지고 $\mathbf{v}_A,\,\mathbf{v}_B,\,\mathbf{v}_C,\,\mathbf{v}_D$ 를 계산했다고 하자. 우리는 그 꼭지점의 이름을 어떤 순서와 방향으로 붙이건 간에  $\mathbf{v}_A,\,\mathbf{v}_B,\,\mathbf{v}_C,\,\mathbf{v}_D$ 로 계산된 양이 각 면에 나타날 것이므로, 그 합은 꼭지점을 이름붙이는 순서와 상관 없음을 알 수 있다. 즉 편의대로 붙이면 된다.

$A,\,B,\,C$ 가 반시계 방향이고, $\overrightarrow{AD}\cdot(\overrightarrow{BA}\times \overrightarrow{CA})>0$ 이라고 하자. 그렇다면,
$$
\begin{align}
\mathbf{v}_A=-\dfrac{1}{2} 

\end{align}
$$
