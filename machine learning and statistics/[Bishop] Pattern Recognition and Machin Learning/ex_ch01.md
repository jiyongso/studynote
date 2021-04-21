Exerciese in Chapter 1.
==



<b>1.1 </b> 식 (1.2) 의 sum-of-square error function 을 생각하자ㅣ $y(x,\,\mathbf{w})$ 는 식 (1.1) 의 다항식으로 주어졌다. Error function을 minimize 하는 coefficient $\mathbf{w} =\{w_i\}$ 는 다음 방정식의 해로부터 얻어질 수 있음을 보여라.
$$
\sum_{j=0}^M A_{ij}w_j = T_i\quad \text{where } A_{ij}=\sum_{n=1}^N (x_n)^{i+j},\quad T_i = \sum_{n=1}^N (x_n)^i t_n\;.
$$

---

$$
\begin{align}
y(x,\,\mathbf{w})&= \sum_{j=0}^M w_j x^j\\
E &=\dfrac{1}{2} \sum_{n=1}^N \left\{  y(x_n,\, \mathbf{w})-t_n\right\}^2\;. \\
&= \dfrac{1}{2}\sum_{n=1}^N \left[\sum_{j=0}^M w_j x_n^j-t_n\right]^2

\end{align}
$$

이므로,
$$
\begin{align}
&\dfrac{\partial E}{\partial w_i}=\sum_{n=1}^N x_n^i \left( \sum_{j=0}^M w_j x_n^j -t_n\right)=0  \\
\implies & \sum_{j=0} ^M (x_n) ^{i+j}w_j=\sum_{n=0}^N x_{n}^i t_n
\end{align}
$$


<b>1.2 </b> 





<b>1.3 </b> 3개의 색칠한 상자 $r$ (red), $b$ (blue), $g$ (green) 이 있다고 하자. 각 상자에 포함된 과일들의 갯수는 다음과 같다.

|      | 사과 | 오렌지 | 라임 |
| ---- | ---- | ------ | ---- |
| $r$  | 3    | 4      | 3    |
| $b$  | 1    | 1      | 0    |
| $g$  | 3    | 3      | 5    |






