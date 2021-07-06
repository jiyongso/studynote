VIII. 삼차원 공간과 벡터의 외적
==



<u> 이 장에서의 공간은 $\mathbb{R}^3$ 를 의미한다</u>

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
\mathbf{v}_A&=\dfrac{1}{2} (\overrightarrow{DB}\times \overrightarrow {DC})\\
\mathbf{v}_B&=\dfrac{1}{2} (\overrightarrow{AD}\times \overrightarrow{AC})\\
\mathbf{v}_C&=\dfrac{1}{2} (\overrightarrow{BD}\times \overrightarrow{BA})\\
\mathbf{v}_D &=\dfrac{1}{2} (\overrightarrow{CB}\times \overrightarrow{CA})

\end{align}
$$

$$
\begin{align}
2(\mathbf{v}_A+\mathbf{v}_B+\mathbf{v}_C+\mathbf{v}_D) &= (\mathbf{b}-\mathbf{d})\times (\mathbf{c}-\mathbf{d})+(\mathbf{d}-\mathbf{a})\times (\mathbf{c}-\mathbf{a})+(\mathbf{d}-\mathbf{b})
\times (\mathbf{a}-\mathbf{b})+(\mathbf{b}-\mathbf{c})\times (\mathbf{a}-\mathbf{c})\\
&=\mathbf{b}\times \mathbf{c}-\mathbf{b}\times \mathbf{d}+\mathbf{c}\times \mathbf{d}-\mathbf{c} \times \mathbf{d} +\mathbf{a}\times \mathbf{d}-\mathbf{a}\times \mathbf{c} -\mathbf{a}\times \mathbf{d}+\mathbf{b}\times \mathbf{d}+\mathbf{a}\times \mathbf{b} -\mathbf{a}\times \mathbf{b}-\mathbf{b}\times \mathbf{c}+\mathbf{a}\times \mathbf{c}\\
&=0
\end{align}
$$



<b>12. </b> 일차독립인 벡터 $\mathbf{v}_1,\,\mathbf{v}_2$ 에 대하여 공간속의 두 직선
$$
A_i + t\mathbf{v}_i \qquad i=1,\,2
$$
사이의 최단거리는
$$
\left| (A_1-A_2) \cdot \dfrac{\mathbf{v}_1\times \mathbf{v}_2}{|\mathbf{v}_1 \times \mathbf{v}_2|} \right|
$$
임을 보이라.

---

직선 밖의 점 에서 직선까지의 최단거리는 그 점으로부터 직선까지 거린 수선에 의해 정해진다. 두 직선 사이 $l_1,\,l_2$ 의 최단거리를 생각하자. $l_1$ 의 임의의 점 $P_1$ 에서 $l_2$ 까치의 최단거리는 $P_1$ 에서 $l_2$ 에 내린 수선에 의해 정해지며 그 역도 마찬가지이다. 따라서 그 수선의 방향벡터는  $l_1,\,l_2$ 두 직선 각각에 수직이므로 $l_1, l_2$ 의 방향벡터에 수직이다. 문제에서 주어진 두 직선에서 최단거리를 포함하는 직선의 방향벡터는 단위벡터로 표현할 때
$$
\dfrac{\mathbf{v}_1\times \mathbf{v}_2}{|\mathbf{v}_1 \times \mathbf{v}_2|}
$$
이다. 직선상의 임의의 두 점은 $A_i+t_i \mathbf{v}_i\;(i=1,\,2)$ 이므로 한 직선의 임의의 한 점과 다른 직선의 임의의 한 점의 벡터는 
$$
A_2+t_2\mathbf{v}_1-A_1 -t_1\mathbf{v}_1
$$
으로 표현 할 수 있다. 그런데 이 벡터의 앞서 말한 수선방향으로의 정사영의 크기는 
$$
\left|(A_2-A_1)\cdot \dfrac{\mathbf{v}_1\times \mathbf{v}_2}{|\mathbf{v}_1\times \mathbf{v}_2|}\right|
$$
로 어떤 두 점에 대해서도 동일하다. 따라서 이 값이 두 직선 사이의 거리이다.



<b>13. </b> (**정사영**) 공간 속의 두 벡터 $\mathbf{a},\,\mathbf{b}$ 가 이루는 평행사변형을 한 평면에 정사영한 것의 넓이는 $\cos \theta$ 배임을 보이라. 여기서 $\theta$ 는 평행사변형과 주어진 평면이 이루는 각의 크기이다. 

---

$\mathbf{a},\,\mathbf{b}$ 에 의해 정의되는 평면의 방향벡터는 (이 평면에 수직인) $\mathbf{a}\times \mathbf{b}$ 이다.  주어진 평면의 방향벡터의 단위벡터를 $\mathbf{n}$ 이라 하자. $\mathbf{a}\times \mathbf{n}$ 은 $\mathbf{n}$ 에 수직이며 그 크기가 $\mathbf{a}$ 의 평면에 대한 정사영의 크기와 같고 그 방향은 $\mathbf{a}$ 의 평면으로의 정사영에 대하여 $\pi/2$ 만큼 회전한 벡터이다. 그 회전방향은 $\mathbf{n}$ 과 $\mathbf{a}$ 의 방향에 따라 시계방향 혹은 반시계방향일 수 있다. $\mathbf{b}\times \mathbf{n}$ 도 마찬가지. 

$\mathbf{a}\cdot \mathbf{n}>0$ 일 때 $\mathbf{a}$ 의 평면에 대한 정사영에 대해 $\mathbf{a}\times \mathbf{n}$ 의 회전방향을 $+$ 로 잡자. $\mathbf{b}\cdot \mathbf{n}$ 이 양수이든 음수이든 평행사변형의 면적은 변화가 없다. 즉 정사영의 평행사변의 면적 $S$ 는
$$
S=|(\mathbf{a}\times\mathbf{n}) \times (\mathbf{b} \times \mathbf{n})|=|((\mathbf{a} \times \mathbf{n})\cdot \mathbf{n})\mathbf{b} -((\mathbf{a\times \mathbf{b}}) \cdot \mathbf{n})\mathbf{n}| = |(\mathbf{a}\times \mathbf{b})\cdot \mathbf{n}|=|\mathbf{a}\times \mathbf{b}|\cos \theta
$$
이다. 



<b>14. </b> 공간에서 벡터 $\mathbf{a}\ne \mathbf{0}$ 에 대한 벡터 $\mathbf{b}$ 의 정사영을 $p_{\mathbf{a}}(\mathbf{b})$ 라 하자. 이 때,
$$
\mathbf{b}-p_{\mathbf{a}}(\mathbf{b})=\dfrac{(\mathbf{a}\times \mathbf{b})\times \mathbf{a}}{\mathbf{a}\cdot \mathbf{a}}
$$
임을 보여라.

---

정리 3.1.1 로부터 $p_{\mathbf{a}}(\mathbf{b})= \dfrac{\mathbf{a}\cdot \mathbf{b}}{\mathbf{a}\cdot \mathbf{a}}\mathbf{a}$ 임을 안다. 여기서,
$$
(\mathbf{a}\times\mathbf{b})\times \mathbf{a}= (\mathbf{a}\cdot \mathbf{a})\mathbf{b}-(\mathbf{a}\cdot \mathbf{b})\mathbf{a}
$$
이므로,
$$
p_{\mathbf{a}}(\mathbf{b})=\dfrac{(\mathbf{a}\cdot \mathbf{a})\mathbf{b}-(\mathbf{a}\times \mathbf{b})\times \mathbf{a}}{\mathbf{a} \cdot \mathbf{a}}=\mathbf{b}-\dfrac{(\mathbf{a}\times \mathbf{b})\times \mathbf{a}}{\mathbf{a} \cdot \mathbf{a}}
$$
이다. 





<b>15. </b> 공간에서 벡터 $\mathbf{a},\,\mathbf{b},\, \mathbf{c}$ 가 일차독립이면, 임의의 벡터 $\mathbf{v}$ 에 대하여,
$$
\mathbf{v} = \dfrac{\det (\mathbf{v},\,\mathbf{b},\,\mathbf{c})}{\det(\mathbf{a},\,\mathbf{b},\,\mathbf{c})}\mathbf{a} + 
\dfrac{\det (\mathbf{a},\,\mathbf{v},\,\mathbf{c})}{\det(\mathbf{a},\,\mathbf{b},\,\mathbf{c})}\mathbf{b} 
+\dfrac{\det (\mathbf{a},\,\mathbf{b},\,\mathbf{v})}{\det(\mathbf{a},\,\mathbf{b},\,\mathbf{c})}\mathbf{c}
$$
임을 보이라.

---

벡터 $\mathbf{a},\,\mathbf{b},\,\mathbf{c}$ 가 일차독립이므로, $\det(\mathbf{a},\,\mathbf{b},\,\mathbf{c})=(\mathbf{a}\times \mathbf{b})\cdot \mathbf{c} \ne 0$ 이며, $\mathbf{v}=a\mathbf{a}+b\mathbf{b}+c\mathbf{c}$ 일 때 scalar $a,\,b,\,c$ 가 유일하게 결정된다. 
$$
\begin{align}
\det (\mathbf{v},\,\mathbf{b},\,\mathbf{c})\mathbf{a} + 
\det (\mathbf{a},\,\mathbf{v},\,\mathbf{c})\mathbf{b} 
+\det (\mathbf{a},\,\mathbf{b},\,\mathbf{v})\mathbf{c}
&= ((\mathbf{v}\times \mathbf{b})\cdot \mathbf{c})\mathbf{a}+((\mathbf{a} \times \mathbf{v})\cdot\mathbf{c}) \mathbf{b} + ((\mathbf{a} \times \mathbf{b})\cdot \mathbf{v})\mathbf{c} \\
\end{align}
$$
인데,
$$
\begin{align}
((\mathbf{v}\times \mathbf{b})\cdot \mathbf{c}) &= (a\mathbf{a}\times \mathbf{b}+c\mathbf{c}\times \mathbf{b})\cdot \mathbf{c}=a\det(\mathbf{a},\,\mathbf{b},\,\mathbf{c})\\
((\mathbf{a}\times \mathbf{v})\cdot \mathbf{c}) &= (b \mathbf{a} \times \mathbf{b}+c \mathbf{a} \times \mathbf{c})\cdot \mathbf{c}=b \det (\mathbf{a},\,\mathbf{b},\,\mathbf{c}) \\
((\mathbf{a}\times \mathbf{b})\cdot \mathbf{v})&=(\mathbf{a}\times \mathbf{b})\cdot(a\mathbf{a}+b\mathbf{b}+c\mathbf{c})=c\det (\mathbf{a},\,\mathbf{b},\,\mathbf{c})
\end{align}
$$
이므로 
$$
\dfrac{\det (\mathbf{v},\,\mathbf{b},\,\mathbf{c})}{\det(\mathbf{a},\,\mathbf{b},\,\mathbf{c})}\mathbf{a} + 
\dfrac{\det (\mathbf{a},\,\mathbf{v},\,\mathbf{c})}{\det(\mathbf{a},\,\mathbf{b},\,\mathbf{c})}\mathbf{b} 
+\dfrac{\det (\mathbf{a},\,\mathbf{b},\,\mathbf{v})}{\det(\mathbf{a},\,\mathbf{b},\,\mathbf{c})}\mathbf{c} = a\mathbf{a}+b\mathbf{b}+c\mathbf{c}=\mathbf{v}
$$
이다.



<b>16. </b> 좌표공간속의 정사면체 $OABC$ 에 내접하는 구의 중심을 $P$ 라고 두자. 이때 $\overrightarrow{OP}$ 를 $\overrightarrow{OA},\,\overrightarrow{OB},\, \overrightarrow{OC}$ 의 일차결합으로 표현하라.

---

일단 $OABC$ 가 정사면체가 되려면 $\overrightarrow{OA},\,\overrightarrow{OB},\, \overrightarrow{OC}$ 이 일차독립이어야 한다. 따라서 $\overrightarrow{OP}$ 는 $\overrightarrow{OA},\,\overrightarrow{OB},\, \overrightarrow{OC}$ 의 일차결합으로 표현된다. 편의를 위해 $\overrightarrow{OA}=\mathbf{a},\,\overrightarrow{OB}=\mathbf{b},\,\overrightarrow{OC}=\mathbf{c},\,\overrightarrow{OP}=\mathbf{p}$ 라 하자. 이제 $\mathbf{p}=a\mathbf{a}+b\mathbf{b}+c\mathbf{c}$ 이다. 



<b>17. </b>  공간에서 $\triangle ABC$ 와 원점 $O$ 에 대하여 $\mathbf{a}=\overrightarrow{OA},\,\mathbf{b}=\overrightarrow{OB},\, \mathbf{c}=\overrightarrow{OC}$ 로 두면 $(\mathbf{a}\times \mathbf{b})+(\mathbf{b} \times \mathbf{c})+(\mathbf{c}\times \mathbf{a})$ 는 $\triangle ABC$ 에 수직임을 보이라.

---

$\mathbf{p}=(\mathbf{a}\times \mathbf{b})+(\mathbf{b} \times \mathbf{c})+(\mathbf{c}\times \mathbf{a})$ 라 두면 $\mathbf{p}\cdot (\mathbf{b}-\mathbf{a})=0$ 이고 $\mathbf{p}\cdot (\mathbf{c}-\mathbf{a})=0$ 임을 보이면 된다. 
$$
\begin{align}
\mathbf{p}\cdot (\mathbf{b}-\mathbf{a}) &= (\mathbf{c}\times \mathbf{a})\cdot \mathbf{b}-(\mathbf{b}\times \mathbf{c})\cdot \mathbf{a}=0 \\
\mathbf{p}\cdot (\mathbf{c}-\mathbf{a}) &=(\mathbf{a} \times \mathbf{b} )\cdot \mathbf{c} -(\mathbf{b}\times \mathbf{c})\cdot \mathbf{a} =0

\end{align}
$$


<b>18. </b> 벡터 $\mathbf{a},\,\mathbf{b},\,\mathbf{c}\in \mathbb{R}^3$ 에 대하여,
$$
(\mathbf{a}\times \mathbf{b})\cdot (\mathbf{b}\times \mathbf{c}) \times (\mathbf{c}\times \mathbf{a})=(\mathbf{a}\cdot \mathbf{b} \times \mathbf{c})^2
$$
임을 보이라.

---

$$
\begin{align}
(\mathbf{a}\times \mathbf{b})\cdot (\mathbf{b}\times \mathbf{c}) \times (\mathbf{c}\times \mathbf{a}) &=(\mathbf{a}\times \mathbf{b})\cdot \left[((\mathbf{b}\times \mathbf{c})\cdot \mathbf{a})\mathbf{c} - ((\mathbf{b}\times \mathbf{c})\cdot \mathbf{c})\mathbf{a}\right] = ((\mathbf{b}\times \mathbf{c} )\cdot \mathbf{a})((\mathbf{a} \times \mathbf{b})\cdot \mathbf{c})=(\mathbf{a} \cdot \mathbf{b} \times \mathbf{c})^2
\end{align}
$$



<b>19</b> 평행사변형을 $xy$-평면, $yz$-평면, $zx$-평면으로 정사영한것의 넓이가 각각 $1,\,1,\,2$ 이면 처음 평행사변형의 넓이는 얼마인가?

---

평행사변형의 면적을 $S$ 라 하고 평행사변형을 포함하는 평면의 방향벡터의 단위벡터를 $\mathbf{n}$ 이라 하자. 그렇다면
$$
S\mathbf{n}\cdot (0,\,0,\,1)=1,\qquad S\mathbf{n} \cdot (1,\,0,\,0)=1,\qquad S\mathbf{n}\cdot (0,\,1,\,0)=2
$$
이므로 $S=\sqrt{1^2+1^2+2^2}=\sqrt{6}$. 



<b>20. </b> $\mathbb{R}^3$ 속의 세 백터 $\mathbf{x},\,\mathbf{y},\,\mathbf{z}$ 가 이루는 **평행육면체**
$$
\{r\mathbf{x}+s\mathbf{y}+t\mathbf{z} : 0 \le r,\,s,\,t \le 1\}
$$
의 부피는 $|\det (\mathbf{x},\,\mathbf{y},\,\mathbf{z})|$ 임을 보이라.

---

$\mathbf{x},\,\mathbf{y}$ 의 면적은 $|\mathbf{x}\times \mathbf{y}|$ 이다. $\mathbf{x},\,\mathbf{y}$ 에 의해 정해지는 평면의 방향벡터의 단위벡터는  $\mathbf{n}=\dfrac{\mathbf{x}\times  \mathbf{y}}{|\mathbf{x}\times \mathbf{y}|}$ 이며 이 평면과 $\mathbf{z}$ 사이의 거리는 $\mathbf{n}\cdot \mathbf{z}$ 로 주어진다. 따라서,
$$
V=|\mathbf{x} \times \mathbf{y}| \, |\mathbf{n}\cdot \mathbf{z}|=|\mathbf{x}\times \mathbf{y}| \left| \dfrac{(\mathbf{x}\times \mathbf{y})\cdot \mathbf{z}}{|\mathbf{x} \times \mathbf{y}|}\right|=|\det (\mathbf{x},\,\mathbf{y},\,\mathbf{z})|
$$


<b>21. </b> 생략



<b>22. </b> 3차원 좌표공간 속의 세 벡터 $\mathbf{x},\,\mathbf{y},\,\mathbf{z}$ 가 이루는 평행육면체의 부피를 $\operatorname{Vol}(\mathbf{x},\,\mathbf{y},\,\mathbf{z})$ 라 고 두었을 때, 3차 정사각행렬 $A$ 에 대하여
$$
\operatorname{Vol}(L_A(\mathbf{x}),\,L_A(\mathbf{y}),\,L_A(\mathbf{z}))=|\det A| \operatorname{Vol}(\mathbf{x},\,\mathbf{y},\,\mathbf{z})
$$
임을 보이라.

---

앞의 20번 문제에서 부터 $\operatorname{Vol}(\mathbf{x},\,\mathbf{y},\mathbf{z})=|\det(\mathbf{x},\,\mathbf{y},\,\mathbf{z})|$  임을 보였다. 정리 3.0.6으로부터, 
$$
\det(A\mathbf{x},\,A\mathbf{y},\,A\mathbf{z}) = (\det A ) (\det (\mathbf{x},\,\mathbf{y},\,\mathbf{z}))
$$
이므로 증명 끝.



## 연습문제 : 제 8 장 2 절

<b>1. </b> 모든 정사각행렬은 대칭행렬과 왜대칭행렬의 합으로 표현됨을 보여라.

---

$$
\begin{align}
(A+A^t)_{ij}-(A+A^t)_{ji}&=A_{ij}+(A^{t})_{ij} -A_{ji}-(A^t)_{ji}=A_{ij}+A_{ji}-A_{ji}-A_{ij}=0\\
(A-A^t)_{ij}+(A-A^t)_{ji}&=A_{ij}-A_{ji}+A_{ji}-A_{ij}=0
\end{align}
$$

이므로 $A+A^t$ 는 대칭행렬이고 $A-A^t$ 는 왜대칭행렬이다. $\dfrac{1}{2}(A+A^t)$ 는 대칭행렬이고 $\dfrac{1}{2}(A-A^t)$ 는 왜대칭행렬이며,
$$
A=\dfrac{1}{2}(A+A^t)+\dfrac{1}{2}(A-A^t)
$$
이다.



<b>2. </b> 왜대칭행렬의 합은 왜대칭행렬임을 보이라. 또 왜대칭행렬의 상수배도 왜대칭임을 보이라.

---

trivial. 




<b>3. </b> 차수가 같은 두 정사각행렬 $M,\,N$ 에 대하여
$$
[M,\,N]:=MN-NM
$$
으로 정의하자. 이 때 삼차원 공간의 임의의 벡터 $\mathbf{a},\,\mathbf{b}$ 에 대하여
$$
M_{\mathbf{a}\times \mathbf{b}}=[M_\mathbf{a},\,M_\mathbf{b}]
$$
가 성립함을 보이라. 또
$$
[M_1,\,M_2]=M-3,\quad [M_2,\,M_3]=M_1,\quad [M_3,\,M_1]=M_2
$$
임을 보이라.

---

임의의 $\mathbf{x}\in \mathbb{R}^3$ 를 생각하자. 연습문제 8.1.9(d) 의 $ \mathbf{a}\times(\mathbf{b}\times \mathbf{c}) + \mathbf{b}\times (\mathbf{c}\times \mathbf{a}) +\mathbf{c}\times (\mathbf{a} \times \mathbf{b})=0$ 을 이용하면, 
$$
(M_{\mathbf{a}}M_{\mathbf{b}}-M_{\mathbf{b}}M_{\mathbf{a}})\mathbf{x}=\mathbf{a} \times (\mathbf{b}\times \mathbf{x})-\mathbf{b}\times (\mathbf{a}\times \mathbf{x})= \mathbf{a}\times (\mathbf{b}\times \mathbf{x})+\mathbf{b}\times (\mathbf{x}\times \mathbf{a})=(\mathbf{a}\times \mathbf{b})\times\mathbf{x} =M_{\mathbf{a}\times \mathbf{b}}\mathbf{x}
$$




<b>4. </b> 단위벡터 $\mathbf{a}\in \mathbb{R}^3$ 에 대하여 선형변환
$$
\mathbf{x}\mapsto \mathbf{a} \times \mathbf{x} \qquad (\mathbf{x}\in \mathbb{R}^3)
$$
은 $\mathbf{a}$ 방향의 벡터는 $0$ 으로 보내고, $\mathbf{a}$ 에 수직인 방향의 벡터는 $\mathbf{a}$ 를 회전축으로 $90^\circ$ 회전시키는 변환임을 설명하라.

---

$\mathbf{x}$ 는 $\mathbf{a}$ 방향의 벡터와 $\mathbf{a}$ 에 수직인 방향의 벡터로 분해 할 수 있다. $\mathbf{x}$ 의 $\mathbf{a}$ 방향 벡터는 $(\mathbf{x}\cdot \mathbf{a})\mathbf{a}$ 이므로,  $\mathbf{x}_{\perp}= \mathbf{x}-(\mathbf{a}\cdot \mathbf{x})\mathbf{a}$  라 하면,  $\mathbf{x}_{\perp}$ 는 $\mathbf{x}$ 의 $\mathbf{a}$ 에 수직인 방향의 벡터임을 알 수 있다. 
$$
\begin{align}
\mathbf{x}_{\perp} \cdot \mathbf{a} &= \mathbf{x}\cdot \mathbf{a} -(\mathbf{a}\cdot \mathbf{x})(\mathbf{a} \cdot \mathbf{a})=0\\
\mathbf{x}_{\perp }\times \mathbf{a} &=\mathbf{x}\times \mathbf{a} -(\mathbf{a}\cdot \mathbf{x})(\mathbf{a}\times \mathbf{a})=\mathbf{x} \times \mathbf{a}
\end{align}
$$
그런데, 
$$
(\mathbf{a}\times \mathbf{x})\cdot \mathbf{x}_{\perp} = (\mathbf{a}\times \mathbf{x}_\perp) \cdot \mathbf{x}_{\perp}=0
$$
이므로 $\mathbf{a}\times \mathbf{x}$ 는 $\mathbf{x}_{\perp}$ 수직이며. 또한 당연히 $\mathbf{a}\cdot (\mathbf{a}\times\mathbf{x})=0$ 이므로 $\mathbf{a}$ 와도 수직이다. 
$$
|\mathbf{a}\times \mathbf{x}|=|\mathbf{x}_{\perp}|
$$
이므로 $\mathbf{a}\times \mathbf{x}$ 는 $\mathbf{x}$ 의 $\mathbf{a}$ 에 수직인 성분벡터를 $\mathbf{a}$ 를 회전축으로 $90^\circ$ 회전시키는 변환임을 알 수 있다.



<b>5. </b> 공간에서 벡터 $\mathbf{a},\,\mathbf{b}_0$ 에 대하여,
$$
\mathbf{b}_{n+1}=\mathbf{a}\times \mathbf{b}_n,\qquad (n=0,\,1,\ldots)
$$
으로 두자. 이 때 $\mathbf{b}_n$ 이 어떻게 변하는 지를 설명하라. 또 $\mathbf{a}=(1,\,2,\,2)/3,\, \mathbf{b}_0=(0,\,1,\,2)$ 일 때 $\mathbf{b}_{2000}$ 을 구하라.

---

앞의 4. 의 결과를 알면 쉽다.  $|\mathbf{a}|=1$ 이므로 $\mathbf{b}_1$ 은 $\mathbf{b}_0$ 의 $\mathbf{a}$ 에 대해 수직인 방향의 성분을 $90^\circ$ 회전시키 것이다.  $\mathbf{b}_1$ 은 이제 $\mathbf{a}$  에 수직이므로 $n\ge 1$ 에 대해 $\mathbf{b}_{n+1}$ 은 $\mathbf{b}_n$ 을(이제 $\mathbf{b}_n$ 은 $\mathbf{a}$ 에 수직이다) $\mathbf{a}$ 를 회전축으로 $90^\circ$ 만큼 회전시것이다.  $\mathbf{b}_0$ 의 $\mathbf{a}$ 에 수직인 성분을 $\mathbf{b}_{\perp}$ 라 하면,
$$
\mathbf{b}_{\perp}=\mathbf{b}_0-(\mathbf{a}\cdot \mathbf{b_0})\mathbf{a}=(-2, -1, 2)/3
$$
이며, $\mathbf{b}_n$ 은 $\mathbf{b}_\perp$ 를 $n$ 번 $90^\circ$ 회전시킨 것이므로 $\mathbf{b}_{2000}=\mathbf{b}_\perp$ 이다.



<b>6.  </b> 벡터 $\mathbf{a}\in \mathbb{R}^3$ 의 절대값을 $a$ 라 하였을 때
$$
M_{\mathbf{a}}^3+a^2M_{\mathbf{a}}=O
$$
임을 보이라. 이를 이용하여 $M_{\mathbf{a}}^{2002}$ 를 간단히하라.

----

$M_\mathbf{a} \mathbf{x} =\mathbf{a}\times\mathbf{x}$ 이므로,
$$
\begin{align}
\mathbf{a}\times (\mathbf{a} \times (\mathbf{a}\times \mathbf{x}))+a^2 \mathbf{a}\times \mathbf{x} &= \mathbf{a} \times \big((\mathbf{a} \cdot \mathbf{x}) \mathbf{a}-a^2\mathbf{x}\big)+a^2\mathbf{a}\times \mathbf{x}=  -a^2\mathbf{a} \times \mathbf{x}+a^2\mathbf{a}\times\mathbf{x}=0
\end{align}
$$
이다. 따라서 $M_{\mathbf{a}}^{3}=-a^2M_{\mathbf{a}}$ 이므로 (쓰기 편하게 $M_{\mathbf{a}}=M$ 이라 하자. 
$$
\begin{align}
M^{10}&=(M^3)^3M=-a^6M^2 \\
M^{100} &= a^{60}M^{20}=a^{72}M^4=-a^{74}M^2 \\
M^{1000}&= a^{740} M^{20}=a^{752}M^4 = -a^{754}M^2 \\
M^{2002}&= a^{1508}M^4=-a^{1510}M^2
\end{align}
$$




## 연습문제 : 제 8장 3절

<b>1. </b> 일반적으로 삼차원 공간의 점 $P_1,\ldots,\,P_k$ 와 각 점 $P_i$ 에 작용하는 힘 $\mathbf{f}_i$ 에 대하여 기준점 $Q$ 에 대한 이들의 회전력을
$$
\sum_{i=1}^k \overrightarrow{QP_i} \times \mathbf{f}_i
$$
로 정의한다. 만약
$$
\sum_{i=1}^k \mathbf{f}_i=0
$$
이면, 회전력은 기준점 $Q$ 를 달리하더라도 변화가 없음을 보이라.

---

$$
\sum_{i=1}^k \overrightarrow{Q'P_i} \times \mathbf{f}_i = \sum_{i=1}^k \left(\overrightarrow{Q'Q}+\overrightarrow{QP_i}\right) \times \mathbf{f}_i = \sum_{i=1}^k \overrightarrow{Q'Q}\times \mathbf{f}_i +\sum_{i=1}^k \overrightarrow{QP_i}\times \mathbf{f}_i = \overrightarrow{Q'Q}\times \left(\sum_{i=1}^k \mathbf{f}_i\right)+\sum_{i=1}^k\overrightarrow{QP_i}\times\mathbf{f}_i = \sum_{i=1}^k\overrightarrow{QP_i}\times\mathbf{f}_i
$$





<b>2. </b> 한쪽 긑은 $A=(0,\,0,\,0)$, 또 다른 한쪽 끝은 $B=(1,\,1,\,1)$ 에 위치한 곧은 막대에 힘 $(0,\,1,\,2)$ 가 $A$ 에 작용하고, 또 힘 $(1,\,2,\,3)$ 이 $B$ 에 작용한다고 하자. 이 때 막대의 어느붑ㄴ에 얼마만큼의 힘이 작용하면, 막대가 움직이지 않을까?

---

막대가 움직이지 않으려면 힘의 총합도 $0$ 이며 회전력의 총합도 $0$ 이어야 한다. 따라서 힘 $(-1, -3, -5)$ 가 작용해야 한다. 문제 $1$ 에 의해 회전력의 총합은 기준점의 영향을 받지 않으므로 $A$ 를 기준으로 하기로 하자. 막대이므로 세번째 힘이 작용하는 위치는 $(t,\,t,\,t)$ 라 하자. 그렇다면 회전력의 총합이 $0$ 이 되어야 하므로,
$$
0=(1,\,1,\,1)\times (0,\,1,\,2)+(t,\,t,\,t)\times (-1,\,-3,\,-5)=(1,\,-2,\,1)+(-2t,\, 4t,\, -2t)
$$
이며, 따라서 $t=1/2$ 인 (1/2, 1/2, 1/2) 에 작용해야 한다.



<b>3. </b> 생략



## 탐구문제



<b>1. </b> $i=1,\,2,\,3$ 에 대하여
$$
\exp tM_i = R_i (t) \qquad t\in \mathbb{R}
$$
임을 보이라. ($R_i$ 는 기본 연습문제 2.0.1 에서 정의하였다.)

---

우선 $M_1$ 을 보자. 
$$
\begin{align}
M_1 &= \left(\begin{array}{rr} 0 & 0 & 0 \\ 0 & 0 & -1 \\ 0 & 1 & 0 \end{array}\right)\\
M_1^2 &=\left(\begin{array}{rr} 0 & 0 & 0 \\ 0 &-1 & 0 \\ 0 & 0 & -1\end{array}\right)\\
M_1^3 &=\left(\begin{array}{rr} 0 &  0 & 0 \\ 0 & 0 & 1 \\ 0 & -1 & 0\end{array}\right) = -M_1\\ 
M_1^4 &=-M_1^2 \\
M_1^5 &= M_1
\end{align}
$$
이다.
$$
\begin{align}
{\big (}\exp (tM_1){\big)}_{22} &=  \left(\sum_{k=0}^\infty t^k \left( M_1 \right)^k\right)_{22} = \sum_{k=0}^\infty \dfrac{1}{(2k)!} t^{2k}(-1)^{k} =\cos t  \\
{\big (}\exp (tM_1){\big)}_{23} &= \left(\sum_{k=0}^\infty t^k \left( M_1 \right)^k\right)_{23} = \sum_{k=0}^\infty \dfrac{1}{(2k+1)!}t^{2k+1} (-1)^{k+1} = -\sin t\\
{\big (}\exp (tM_1){\big)}_{32} &= -{\big (}\exp (tM_1){\big)}_{23} = \sin t \\
{\big (}\exp (tM_1){\big)}_{33} &= {\big (}\exp (tM_1){\big)}_{22}= \cos t

\end{align}
$$
이므로 $\exp tM_1 = R_1 (t)$ 이다. 

$M_2,\,M_3$ 에 대해서도 같은 방법으로 보일 수 있다.





<b>2. </b> 단위벡터 $\mathbb{a}\in \mathbb{R}^3$ 에 대하여 선형변환
$$
\mathbf{x} \mapsto \mathbf{a}\times\mathbf{x} \qquad (\mathbf{x}\in \mathbb{R}^3)
$$
대응되는 행렬 $M_{\mathbf{a}}$ 와 실수 $t$ 에 대하여 $\exp tM_{\mathbf{a}}$ 는 $\mathbf{a}$ 축을 회전축으로 하고 회전각이 $t^{\text{rad}}$ 인 회전변환에 대응되는 행렬임을 보이라. 또 임의의 $\mathbf{x}\in \mathbb{R}^3$ 에 대하여
$$
\left.\dfrac{d}{dt}\right|_{0} \left( \exp tM_{\mathbf{a}}\right)\mathbf{x}=\mathbf{a}\times \mathbf{x}
$$
임을 보여라.

---

$\mathbf{a}=(a_1,\,a_2,\,a_3)$ 라 하면,
$$
M_{\mathbf{a}}=\begin{pmatrix} 0 & -a_3 & a_2 \\ a_3 & 0 & -a_1 \\ -a_2 & a_1& 0\end{pmatrix} = a_1M_1+a_2M_2+a_3M_3
$$
이다. 





정사각 행렬 $A,\,B$ 와 실수 $a,\,b$ 에 대하여,
$$
\exp (aA+bB)=\sum_{k=0}^\infty \dfrac{1}{k!} (aA+bB)^k= \sum_{k=0}^\infty \dfrac{1}{k!}\sum_{n=0}^k \dfrac{k!}{}
$$
