Inverse Function Theorem and Implicit Function Theorem
---

#### Notation.

For $\mathbf{x} \in \mathbb{R}^n$, $|\mathbf{x}| =  \max\{|x_1|,\,|x_2|,\ldots,\,|x_n|\}$ and $ \| \mathbf{x} \|  = \sqrt{x_1^2 + \cdots x_n^2}$ .

For a $n \times n$ matrix $A$ , $|A| = \max \{|A_{i,\,j}|\}$ .



#### Lemma 1.

$n \times m​$ 행렬 $A​$와 $m \times p​$ 행렬 B에 대해 $|A \cdot B| \le m |A||B|​$ 이다.



#### Theorem 2. (Mean value theorem for $\mathbb{R}^n$)

Let $A​$ be open in $\mathbb{R}^n​$ and $f :A \rightarrow \mathbb{R}​$ be differentiable on $A​$. 만약 $\mathbf{a}​$ 에서 $\mathbf{a}+\mathbf{h}​$ 로의 line segment가 $A​$에 포함된다면 어떤 $\mathbf{c} = \mathbf{a} + t_0\mathbf{h}​$ with $0 < t_0 < 1​$ 에서 $f(\mathbf{a}+\mathbf{h}) - f(\mathbf{a}) = D f(\mathbf{c}) \cdot \mathbf{h}​$ 이다.

---

*Proof is trivial*



**Comment** : $\mathbf{a} \in A​$ 를 중심으로 $A​$에 포함되는 open cube나 open ball 형태의 neighborhood $N_a​$를 잡으면 모든 $\mathbf{x},\,\mathbf{y} \in N_a​$를 잇는 line segment가 $N_a​$의 subset이므로 mean value theorem이 성립한다.



#### Lemma 3.

$A​$ is open in $\mathbb{R}^n​$, $f: A \rightarrow \mathbb{R}^n​$ is a $C^1​$ class function 이라 하자. $D f (\mathbf{a})​$ 가 non singular 이면 ${}^\exist \alpha >0​$ s.t $|f(\mathbf{x}_0) - f(\mathbf{x}_1) | \ge \alpha | \mathbf{x}_0 - \mathbf{x}_1|​$ holds for all $\mathbf{x}_0,\,\mathbf{x}_1​$ in some open cube $C(\mathbf{a}, \,\varepsilon)​$ centered at $\mathbf{a}​$. 즉 $f (\mathbf{x})​$ is injective in $C( \mathbf{a}, \,\varepsilon)​$. 

---

*Proof*

$E = Df(\mathbf{a})$ 라 하자. $|\mathbf{x}_0 - \mathbf{x}_1| = |E^{-1}\cdot E \cdot (\mathbf{x}_0 - \mathbf{x}_1)| \le n |E^{-1}|\cdot |E \cdot (\mathbf{x}_0 - \mathbf{x}_1)|$.

Let $2\alpha = 1/ (n|E^{-1}|)$, then $ |E \cdot (\mathbf{x}_0 - \mathbf{x}_1)| \ge 2 \alpha  | \mathbf{x}_0 - \mathbf{x}_1 |$ .

Consider function $H (\mathbf{x}) = f(\mathbf{x}) - E \cdot \mathbf{x}$ , then $DH(\mathbf{a}) = 0$.  $H$가 $C^1$ 함수이므로 $DH(\mathbf{x}) < \alpha /n$ for all $x \in C(\mathbf{a}, \,\varepsilon) =C$ 이 되도록 하는 $\varepsilon > 0$이 존재한다.  Mean value theorem에 의해 $\mathbf{x}_0,\, \mathbf{x}_1 \in C$ 이면 ${}^\exist \mathbf{c} \in C$ such that $|H_i (\mathbf{x}_0) - H_i (\mathbf{x}_1) |= |DH_i(\mathbf{c})\cdot (\mathbf{x}_0 - \mathbf{x}_1)| \le n (\alpha/n)|\mathbf{x}_0 - \mathbf{x}_1|$.

따라서, 모든 $\mathbf{x}_0,\, \mathbf{x}_1 \in C$ 에 대해

$$
\begin{aligned}
\alpha |\mathbf{x}_0 - \mathbf{x}_1 |&\ge |H(\mathbf{x}_0) - H(\mathbf{x}_1)|\\
& = |f(\mathbf{x}_0)- E\cdot \mathbf{x}_0 - f(\mathbf{x}_1) + E \cdot \mathbf{x}_1| \\
& \ge |E \cdot \mathbf{x}_1 - E \cdot \mathbf{x}_0| - |f(\mathbf{x}_1) - f(\mathbf{x}_0)| \\
& \ge 2 \alpha |\mathbf{x}_1 - \mathbf{x}_0| - |f(\mathbf{x}_1)- f(\mathbf{x}_0)|\;.
\end{aligned}
$$

이므로 Lemma가 성립한다.     $\square$.



#### Lemma 4.

Let $A$ be an open in $\mathbb{R}^n$ and $\phi : A \rightarrow \mathbb{R}$ be differentiable. 만약 $\phi$가 $\mathbf{x}_0 \in A$에서 local minimum을 가지면 $D \phi (\mathbf{x}_0) = 0$ 이다.

---

*Proof is trivial*



#### Theorem 5.

Let $A​$ be open in $\mathbb{R}^n​$,  $f: A \rightarrow \mathbb{R}^n​$ be of class $C^r​$, and $B=f(A)​$. 만약 $f​$가 one-to-one on $A​$ 이고 $Df(\mathbf{x})​$ 가 non singular for $\mathbf{x} \in A​$ 이면 $B​$는 open in $\mathbb{R}^n​$ 이며 $f^{-1}=g​$  는 $C^r​$ class 함수이다.

---

*Proof*

*(Step 1)* 우선 $B​$가 open 임을 보이자. 임의의 $\mathbf{b} \in B​$ 에 대해 open ball $B(\mathbf{b},\, \delta) \subset B​$가 존재함을 보이고자 한다. $\mathbf{a} = f^{-1}(\mathbf{b})​$ 를 내부에 포함하며 $A​$에 포함되는 closed rectangle $Q​$를 생각하자. ( $\mathbf{a} \in \text{int} (Q)​$ and $Q \subset A​$ ). $\text{Bd}(Q)​$는 compact set 이고  $f​$는 연속이므로 $f(\text{Bd}(Q))​$도 compact set 이다. $f​$가 injection 이므로 $\mathbf{b} \not \in \text{Bd}(Q)​$ 이다. $f (\text{Bd}(Q))​$가 closed set 이므로 이것과 disjoint 한 open ball around $\mathbf{b}​$, $B(\mathbf{b},\,2\delta)​$ 가 존재한다. 이제 임의의 $\mathbf{c} \in B(\mathbf{b}, \, \delta)​$에 대해  $\mathbf{c} = f(\mathbf{x})​$ for some $\mathbf{x} \in A​$ 임을 보이자. 

이를 위해  $C^r$ class 함수 $\phi (\mathbf{x}) = \| f(\mathbf{x}) - \mathbf{c} \|^2$ 를 생각하자. $Q$가 compact 하므로 $\phi$는 $Q$에서 최대값과 최소값을 가진다. $\mathbf{c} \in B(\mathbf{b}, \,\delta)$ 이므로  $\phi(\mathbf{a}) = \| f(\mathbf{a}) - \mathbf{c} \|^2 = \| \mathbf{b} -\mathbf{c}\|^2 < \delta^2$ 이다. 따라서  minimum value of $\phi$ on $Q$ 는 $\delta^2$ 보다 작아야 한다. 그런데 $\mathbf{y} \in \text{Bd}(Q)$ 이면 $f(\mathbf{y})$ 는 $B(\mathbf{b},\,2 \delta)$ 밖에 있으므로 $\phi (\mathbf{y}) \ge \delta^2$. 따라서 $\phi$를  minimum 이 되도록 하는 값 $\mathbf{x}$ 는 $\text{int}(Q)$에 존재한다. 

$f$ 는 $\mathbf{x} \in \text{int}(Q)$ 에서 local minimum을 가지므로 $D\phi (\mathbf{x}) = 0$. (Lemma 4.)  $D_j \phi (\mathbf{x}) = 0$ for all $j$. 
$ D_j \phi (\mathbf{x}) = \sum_{k=1}^n 2 \left( f_k (\mathbf{x}) - c_k\right)D_j f_k (\mathbf{x})$ 이므로 $D \phi (\mathbf{x})=0$ 을 행렬방정식으로 쓰면 
$$
2 Df(\mathbf{x}) \cdot \left[ \begin{array}{c} f_1(\mathbf{x})-c_1\\ \vdots \\ (f_n \mathbf{x})-c_n  \end{array} \right]  = 0
$$
이 된다. $D f(\mathbf{x})$가 non-singular 이므로 $f (\mathbf{x}) - \mathbf{c} = 0$인 $x$가 $B(\mathbf{b},\, \delta)$에 존재한다.

*(Step 2)* 이제 $g=f^{-1}$이 연속임을 보이자. $g$가 연속인 것은 임의의 open $U \subset A$에 대해 $f (U)$가 open in $B$ 임을 보이면 되는데 이는 step 1에서 보인것이다. 따라서 $g = f^{-1}$는 연속이다.

*(Step 3)* $g$ 가 임의의 $\mathbf{b} \in B$에서 differentiable 임을 보이자. $\mathbf{a} = g(\mathbf{b})$ 이고 $E=Df(\mathbf{a})$ 라 하자. $N_0 = \{ \mathbf{x} \in A : 0 < \|x\|<r, \text{for some $r$ } \}$ 라 하면 $N_0$ 는  open in $A$ 이다. $G : N_0 \rightarrow B$ 를 다음과 같이 정의한다.
$$
G (\mathbf{k}) = \frac{\left[g(\mathbf{b}+ \mathbf{k}) - g(\mathbf{b}) - E^{-1} \cdot \mathbf{k}\right]}{|\mathbf{k}|}\;.
$$
$g$ 는 $\mathbf{b}$ 에서 미분가능하며 $D g(\mathbf{b}) = E^{-1}$ 이다. $\Delta (\mathbf{k}) = g(\mathbf{b}+\mathbf{k})-g(\mathbf{b})$ 라 정의한다. 

Lemma 3 으로부터 $\mathbf{a}$의  cubic neighborhood $C$와 $\alpha >0$ such that $|f(\mathbf{x}_0) - f(\mathbf{x}_1)  \ge \alpha |\mathbf{x}_0 - \mathbf{x}_1|$ for all $\mathbf{x}_0,\,\mathbf{x}_1 \in C$  이 존재함을 알고 있다. $f(C)$가 $\mathbf{b}$의 neighborhood 이다. $|\mathbf{k}| < \varepsilon$ 일 때 $f (\mathbf{b} + \mathbf{k}) \in f(C)$ 이도록 $\varepsilon$을 작게 잡자. 그렇다면 $g(\mathbf{b}+\mathbf{k}) = \mathbf{x}_0$, $g(\mathbf{b}) = \mathbf{x}_1$ 가 되도록 할 수 있으며 다음이 성립한다.
$$
|(\mathbf{b} + \mathbf{k})-\mathbf{b}| \ge \alpha | g(\mathbf{b}+\mathbf{k}) - g(\mathbf{b})|\;.
$$
따라서 $1/\alpha \ge |\Delta (\mathbf{k})|/|\mathbf{k}|$ 이다. 즉 우리는 $\Delta (\mathbf{k})|/|\mathbf{k}|$ 가 bounded 되도록 하는 $|\mathbf{k}|<\varepsilon$을 생각 할 수 있다.

이제 $\mathbf{k} \rightarrow 0$ implies $G(\mathbf{k}) \rightarrow 0$ 임을 보이자. Let $0 < \mathbf{k} < \varepsilon$ 이라 하자. $g$ 가 injection 이므로 $\mathbf{k} \ne 0$ 이면 $\Delta(\mathbf{k}) \ne 0$ 임을 이용하면 
$$
G(\mathbf{k}) = \dfrac{\Delta (\mathbf{k}) - E^{-1}\cdot \mathbf{x}}{|\mathbf{k}|} = -E \cdot \left[ \dfrac{\mathbf{k}-E \cdot \Delta (\mathbf{k})}{|\Delta (\mathbf{k})|}\right] \cdot \dfrac{|\Delta (\mathbf{k})|}{|\mathbf{k}|} \;.
$$
$E^{-1}$는 constant, $| \Delta(\mathbf{k})|/|\mathbf{k}|$ 는 bounded 이다. 위 식의 $[ \; ]$  부분이  $\mathbf{k} \rightarrow 0$ 일 때 $0$에 접근함을 보이자. $\mathbf{b}+\mathbf{k}$ $= f(g(\mathbf{b} + \mathbf{k}))$ $= f(g(\mathbf{b}) + \Delta (\mathbf{k}))$ $= f(\mathbf{a} + \Delta (\mathbf{k}))$ 이므로, 위 식의 $[\;]$ 부분은 다음과 같다.
$$
\dfrac{f(\mathbf{a} + \Delta (\mathbf{k}))- f(\mathbf{a}) - E\cdot \Delta (\mathbf{k})}{|\Delta (\mathbf{k})|}
$$
$\mathbf{k}\rightarrow 0 ​$ implies $\Delta (\mathbf{k}) \rightarrow 0​$ because $g​$ is continuous. 따라서 $f​$는 $\mathbf{a}​$ 에서 미분가능 하며 그 derivative는 $E​$ 이다.

 