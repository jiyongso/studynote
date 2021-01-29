IV. 선형 사상
===

#### Notation

1. $V\to W$ 인 모든 선형사상의 집합을 $\mathcal{L}(V,\,W)$ 라 쓴다. $V\to V$ 인 모든 선형사상의 집합은 $\mathcal{L}(V)$ 라 쓴다.
2. $L\in \mathcal{L}(V,\,W)$ 일 때 $v\in V$ 에 대해 $L(v)$ 를 $Lv$ 로, $S\subseteq V$ 에 대해 $L(S)$ 를 $LS$ 로 쓰기도 한다.







## 4.1 Linear map



<b>관찰 4.1.6.</b> $L\in \mathcal{L}(V,\,W)$ 이면 $\ker L\le V$ 이고 $\operatorname{im} L \le W$ 이다.

---

(1) 우선 $\ker L$ 은 vector space 임을 보이자. $\ker L \subseteq V$ 이며, $L(0)=0$ 이므로 $\ker L \ne \varnothing$. $v_1,\,v_2\in \ker V$ 이고 $c\in \mathbb{F}$ 일 때,
$$
L(v_1+v_2)=L(v_1)+L(v_2)=0+0=0\,,\\
L(cv_1)=cL(v_1)=c\cdot 0=0\;.
$$
이다. 따라서 $\ker L\le V$ 이다. (관찰 2.2.2)

(2) 이제 $\operatorname{im}L\le W$ 임을 보이자. $0\in \operatorname{im}L$ 이므로 $\operatorname{im}L \ne \varnothing$ 이다. $w_1,\,w_2\in W,\, c\in \mathbb{F}$ 라 하면 $L(v_1)=w_1,\,L(v_2)=w_2$ 인 $v_1,\,v_2\in V$ 가 존재한다.
$$
w_1+w_2 = L(v_1)+L(v_2)=L(v_1+v_2) \in W\,,\\
cw_1= cL(v_1)=L(cv_1)\in W
$$
이므로 $\operatorname{im}L\le W$. $\quad\square$



<b>연습문제 4.1.10.</b> $L \in \mathcal{L}(V,\,W)$ 이고 $S \subseteq W$ 일 때 다음을 증명하라.

(가) $V=\langle S\rangle$ 이면, $\operatorname{im}L=\langle L(S)\rangle$.

(나) $L$ 이 epimorphism(surjective linear map) 이기 위한 필요충분조건은 [$L$ 은 ($V$ 의) **generating set** 을 ($W$ 의) generating set 으로 옮기는 것] 이다.

---

(가) $V=\langle S \rangle$ 이므로 $v\in V$ 는 $v=\sum_{i} a_i s_i$ for $s_i\in S$ 이다. 
$$
\begin{align*}
w\in \operatorname{im}L &\iff \exist v\in V \text{ s.t. }w=L(v) \\
&\iff w=L\left(\sum_{i} a_i s_i \right)=\sum_i a_iL(s_i) \quad\text{where }a_i\in \mathbb{F},\, s_i \in S\\
&\iff w\in \langle L(S)\rangle

\end{align*}
$$
따라서 $\operatorname {im} L = \langle L(S) \rangle$. 

(나) $L$ 이 epimorphism 이면 $W=\operatorname{im}L$ 이므로 [...] 는 (가) 에 의해 trivial 하다. [...] 를 가정하면 $V=\langle S\rangle$ 에 대해 $\langle L(S)\rangle = W$ 이다. 그런데 (가)  에서 $\operatorname{im}L = \langle L(S)\rangle$ 임을 보였으므로 $\operatorname{im} L =W$ 이다. 따라서 $L$ 은 epimorphsim 이다.





<b>연습문제 4.1.11.</b> $L \in \mathcal{L}(V,\,W)$ 이고 $S\subset V$, $\mathcal{B}$ 는 $V$ 의 기저일 때 다음을 증명하라.

(가) $S$ 가 일차독립이고 $L$ 이 monomorphism(injective linear map) 이면 $L(S)$ 도 일차독립이다.

(나) $L$ 이 monomorphism일 필요충분조건은 $L(\mathcal{B})$ 가 일차독립인 것이다.

(다) $L(\mathcal{B})$ 가 $W$ 의 기저이면 $L$ 은 isomorphism 이다.

---

(가) $\{s_1,\ldots,\,s_n\}\in S$ 에 에 대해 $0=L\left(\sum_i c_i s_i\right)=\sum_i c_i L(s_i)$ 라 하면 $L$ 이 monomorphism 이므로 $\sum_{i}c_i s_i=0$ 이어야 하며 $S$ 가 일차독립이므로 $c_1=\cdots =c_n=0$ 이다. 따라서 $L(S)$ 도 일차독립이다.

(나) $\mathcal{B}=\{u_1,\,u_2,\ldots\}$ 라 하자. $L$ 이 monomorphism 이면 $L(\mathcal{B})$ 가 일차독립임은 (가)에 의해 자명하다. $L$ 이 monomorphsim 이 아니라면 $v\ne 0,\, L(v)=0$ 인 $v\in V$ 가 존재하며 이 때 $v=\sum_i a_i v_i$ 라 하자. $0=\sum_i a_i L(v_i)$ 이므로 $L(\mathcal{B})$ 는 일차독립이 아니다.

(다) $L(\mathcal{B})$ 가 $W$ 의 기저이면 (나)에 의해 $L$ 은 monomophism 이며, 연습문제 4.1.10 (나) 에 의해 $L$ 은 epimorphism 이므로 $L$ 은 isomorphism 이다.



<b>연습문제 4.1.14.</b> $\varphi \in \mathcal{L}(V,\,\mathbb{F}^n)$ 이 isomorphism 이면, $\varphi = \alpha_{\mathcal{B}}$ 인 $V$ 의 기저 $\mathcal{B}$ 가 존재함을 보여라.

---

관찰 4.1.4 에서 $\varphi^{-1}$ 도 isomorphism 이다. $\mathbb{F}^n$ 의 standare basis  $\{\mathbf{e}_i: i=1,\ldots,\,n\}$ 에 대해 $v_i = \varphi^{-1}(\mathbf{e}_i)$ 라 하면 $\{v_1,\ldots,\,v_n\}$ 은 basis of $V$ 이며 $\varphi \left(\sum_{i=1}^n a_i v_i\right)=\sum_{i=1}^n a_i \mathbf{e}_i$ 이므로 $\mathcal{B}=\{\varphi^{-1}(\mathbf{e}_1),\ldots,\, \varphi^{-1}(\mathbf{e}_n)\}$  이다.



<b>연습문제 4.1.17.</b> $L \in \mathcal{L}(V,\,W)$ 이고 $Lv=w\in \operatorname{im}L$ 일 때 다음을 보여라.

(가) $L^{-1}(w) = v+\ker L$. 

(나) $L^{-1} (w)$ 와 $\ker L=L^{-1}(0)$ 사이에는 bijection이 존재.

---

(가) $v_0 \in \ker L$ 에 대해 $L(v+v_0)=w$ 이므로 $v+\ker L \subset L^{-1}(w)$ 이다. $v_1 \not\in \ker L$ 에 대해 $L(v+v_1)=L(v)+L(v_1)\ne w$ 이다.  

(나) Define $f_v : L^{-1}(w) \to \ker L$ by $f_v (x) = x-v$. $x\in L^{-1}(w)$ 이면 $L(f_v(x))=L(x-v)=w-w=0$ 이므로 well defined 되어 있다. 

$z \in \ker L$ 에 대해 $L(z+v)=L(v)=w$ 이므로 $z+v\in L^{-1}(w)$ 이다. 따라서 $f_v$ 는 surjection 이다. 

$f_v(x_1)=f_v (x_2) \implies x_1-v = x_2=v \implies x_1=x_2$. 따라서 $f_v$ 는 injection 이므로 윗줄과 더불어 $f_v$ 는 bijection이다.



