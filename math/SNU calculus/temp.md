<b>22. </b> 삼차원 좌표공간에서 단위벡터 $\mathbf{v}=(v_1,\,v_2,\,v_3)$ 가 만드는 축의 주위로 $\theta$ 만큼 회전이동하는 변환의 행렬 $R_{\mathbf{v}}(\theta)$ 는
$$
\begin{pmatrix}
v_1^2 (1-\cos \theta) +\cos \theta & v_1v_2(1-\cos \theta)-v_3\sin \theta  & v_1v_3 (1-\cos \theta)+ v_2\sin \theta \\
v_1v_2(1-\cos\theta)+v_3 \sin \theta & v_2^2 (1-\cos \theta) + \cos \theta & v_2v_3 (1-\cos \theta) - v_1 \sin \theta \\
v_1v_3 (1-\cos \theta) - v_2 \sin \theta & v_2v_3 (1-\cos \theta)+v_1\sin \theta & v_3^2(1-\cos \theta) + \cos \theta


\end{pmatrix}
$$
임을 보이라. 또,
$$
\cos \theta = \dfrac{1}{2} \left(\operatorname{tr} R_{\mathbf{v}}(\theta)-1\right)
$$
임을 보이라.

---



지겨운데..



<b>23. </b> 정사각행렬 $A$ 에 대하여 $|A|<1$ 이면 급수
$$
I+A+A^2+A^3+\cdots
$$
가 수렴하고 이 때
$$
(I-A)(I+A+A^2+A^3+\cdots )=I
$$
임을 보이라.

---

$A$ 를 $n \times n$ 행렬이라 하자. 우리는 $|A_{ij}|<1 \;\forall 1\le i,\,j \le n$ 이며 $|A^k|\le |A|^k$ 임을 안다. (정리 3.3.2) 즉 $|A_{ij}|=r<1$ 이면 $|A^k|\le r^k$ 이므로 모든 $A^k$ 의 성분은 $r^k$ 보다 작다. 따라서, $\displaystyle \lim_{k=\infty}A^k=0$ 이며, $B_k=I+A+A^2+\cdots +A^k $ 라 하면, 
$$
|(B_k)_{ij}|<1+r+r^2+\cdots +r^{k}<\dfrac{1}{1-r}
$$
이므로 $(B_k)_{ij}$ 는 절대수렴한다. $I+A+A^2+\cdots = B$ 이므로 양변에 $A$ 를 곱하면 $B-I=AB$ 임을 안다. 따라서,
$$
(I-A)(I+A+A^2+\cdots)=B-AB=I
$$
이다.



<b>24. </b> 수렴반경이 $r>0$ 인 멱급수 $\displaystyle f(x)=\sum_{k=0}^\infty b_k x^k$ 를 생각하자. 이 때 $A$ 가 $|A|<r$ 인 정사각행렬이면 급수
$$
f(A):=\sum_{k=0}^\infty b_k A^k
$$
가 수렴함을 보이라.

---

우리는 $|A^k|<|A|^k<r^k$ 임을 알며 $|(A^k)_{ij}|<|A^k|<r^k$ 임을 안다. 따라서,
$$
|f(A)_{ij}| = \left|\sum_{k=0}^\infty b_k (A^k)_{ij}\right|\le \sum_{k=0}^\infty \left|b_k (A^k)_{ij}\right| \le \sum_{k=0}^{\infty} b_k r^k
$$
이므로 절대수렴한다. 



