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



## 4.2 Linear Map의 보기



<b>연습문제 4.2.6.</b> 앞 보기 4.2.5 에서, $\mathcal{B}_i$ 를 f.d.v.s. $V_i$ 의 basis라고 표기할 때, 다음을 보여라.

(가) $i_1 (\mathcal{B}_1)\cup \cdots \cup i_n(\mathcal{B}_n)$ 은 $V_1 \times \cdots \times V_n$ 의 basis.

(나) $\dim (V_1 \times \cdots \times V_n)=\dim V_1 + \cdots +\dim V_n$. 

---

Let $V=V_1 \times \cdots \times V_n$. 

(가) $v\in \mathcal{B}_i$ 일 때 $i_j(\mathcal{B}_i)=\delta_{ij}(0,\ldots,0,\,v,\,0,\ldots,\,0)$, $i=j$ 일 경우 $j$-th component가 $v$ 이고 나머지 component 는 $0$ 이다. $\mathcal{B}_i = \{v_1^{(i)},\,v_2^{(i)},\ldots,\, v_{N_i}^{(i)}\}$ Where $N_i = \dim V_i$ 라 하자. $v^{(i)}\in V_i$ 는 $v=\sum_{j=1}^{N_i} c_j^{(i)} v_j^{(i)}$ for $c_j^{(i)}\in \mathbb{F}$ 이다. 또한,

$$
i_1 (\mathcal{B}_1)\cup \cdots \cup i_n(\mathcal{B}_n) =\{(v_{j_1}^{(1)},\ldots,\,v_{j_n}^{(n)}) : v_{j_k}^{(k)} \in \mathcal{B}_k,\, j_k=1,\ldots,\,N_k\}
$$
이므로 $i_1 (\mathcal{B}_1)\cup \cdots \cup i_n(\mathcal{B}_n)$ 은 $V_1 \times \cdots \times V_n$ 의 basis 임은 쉽게 알 수 있다.

(나) $\dim(V_1 \times \cdots \times V_n) =\left|\{(v_{j_1}^{(1)},\ldots,\,v_{j_n}^{(n)}) : v_{j_k}^{(k)} \in \mathcal{B}_k,\, j_k=1,\ldots,\,N_k\}\right|=\dim V_1+ \dots + \dim V_n$.



 <b>연습문제 4.2.8.</b> $L,\,M \in \mathcal{L}(V,\,W)$ 일 때, [$L$ 과 $M$ 의 합]과 [$L$ 과 scalar $a\in \mathbb{F}$ 의 상수곱]을 각각
$$
(L+M)(v)=L(v)+M(v),\quad (aL)(v)=aL(v)\,\quad (v\in V)
$$
로 정의하면 $(L+M)$과 $(aL)$ 도 linear map 임을 보여라.

---

Let $v_1,\,v_2\in V$ and $c\in \mathbb{F}$.
$$
\begin{align*}
(L+M)(v_1+v_2)&=L(v_1+v_2)+M(v_1+v_2)=L(v_1)+L(v_2)+M(v_1)+M(v_2)\\
&= (L+M)(v_1)+(L+M)(v_2)\,,\\
(aL)(cv_1)&=a(L(cv_1)=acL(v_1)=c(aL(v_1))

\end{align*}
$$
이므로 증명 끝.



<b>연습문제 4.2.9. </b> 위 보기 4.2.9 에서, 다음과 같은 그럴듯한 식들이 성립하는 것을 보여라.

(가) $\pi_i \circ i_j=\delta_{ij}\cdot I_{V_j}$ (단 $1 \le i,\, j \le n$.)

(나) $i_1 \circ \pi_1 + \cdots +i_n \circ \pi_n = I_{V_1 \times \cdots \times V_n}$.

---

(가) $V=V_1\times \cdots \times V_n$ 이라 하자. $\pi_i \circ i_j (v_j)=\pi_i (0,\ldots,\,v_j,\ldots,\,0)=\delta_{ij}v_j$. 

(나) Let $v=(v_1,\ldots,\,v_n)$. Then, 
$$
\sum_{i=1}^n (i_i \circ \pi _i)(v)=\sum_{i=1}^n i_i (v_i)=\sum_{i=1}^n(0,\ldots,\,v_i,\ldots,\,0) =v.
$$


<b>연습문제 4.2.11.</b> $f:\mathbb{F}^2\to \mathbb{F}^2$ 를 $f((x,\,y)^t)=(x+y+1,\,x^2+y^3)^t$ 로 정의하면, $f$ 는 linear map 인가?

---

No. $f((0,\,1)^t)=(2,\,1)^t$, $f((1,\,0)^t)=(2,\,1)^t$, $f((1,\,1)^t)=(3,\,2)^t \ne f((1,\,0)^t)+f((0,\,1)^t)$. 



<b>연습문제 4.2.13.</b> $A\in \mathfrak{M}_{m,\,n}(\mathbb{F})$ 일 때, 다음을 보여라.

(가) $\ker L_A$ = [$(*) \, AX=0$ 의 solution space].

(나) $\ker L_A=0$ (즉, $L_A$ 는 injective) 일 필요충분조건은 $(*)\, AX=0$ 가 trivial solution 만을 갖는 것이다.

---

(가) 동어반복.

(나) 관찰 4.1.8.



<b>연습문제 4.2.14.</b> $A\in \mathfrak{M}_{m,\,n}(\mathbb{F})$ 일 때, 다음을 보여라.

(가) $B\in \mathbb{F}^m$ 이면 $(L_A)^{-1}(B)=[\,(**)\,AX=B$ 의 해집합 $]$. 

(나) $L_A$ 가 surjective 일 필요충분조건은 임의의 $B\in \mathbb{F}^m$ 에 대해 $(**)\, AX=B$ 가 solution을 갖는 것이다.

(다) $L_A$ 가 bijective 일 필요충분조건은 임의의 $B\in \mathbb{F}^m$ 에 대해 $(**) AX=B$ 가 unique solution을 갖는 것이다.

---

(가) $Y \in (L_A)^{-1}(B) \iff AY=B \iff Y\in [\cdots]$ .

(나) trivial.

(다) $L_A$ 가 injective 이고 $AX=B$ 를 만족시키는 $X$ 가 존재한다면 유일하다. (Injective의 정의이다.) 따라서 $L_A$ 가 bijective 이면 $AX=B$ 는 unique solution을 갖는다. 

$B\in \mathbb{F}^m$ 에 대해 $AX=B$ 가 unique solution을 가진다고 가정하자. 일단 solution이 존재하므로 $L_A$ 는 surjection이다. $L_A(X)=AX=0$ 을 만족하는 $X$ 는 $0$ 뿐이므로 $L_A$ 는 injective 이다. 따라서 $L_A$ 는 bijective.



<b>연습문제 4.2.15. </b> $A\in \mathfrak{M}_{m,\,n}(\mathbb{F})$ 일 때, 다음을 보여라.

(가) $L_A$ 는 injective $\iff$ $\{[A]^1,\ldots,\,[A]^n\} \subset \mathbb{F}^m$ 은 일차독립.

(나) $L_A$ 는 surjective $\iff$ $\langle [A]^1,\ldots,\,[A]^n\rangle = \mathbb{F}^m$. 

(다) $L_A$ 는 bijective $\iff$ $\{[A]^1,\ldots,\,[A]^n\}$ 은 $\mathbb{F}^m$ 의 기저.

---

(가), (나) 를 증명하면 (다) 는 자동적이다.

(가) $\{\mathbf{e}_1,\ldots,\,\mathbf{e}_n\}$ 를 $\mathbb{F}^n$ 의 standard basis라 하자. $L_A(\mathbf{e}_i)=[A]^i$ 임을 알고 있다. $0=\sum_i c_i[A]^i=L_A(\sum_i c_i \mathbf{e}_i)$ 이다. 따라서,

$L_A$ is injective $\iff \ker L_A=0 \iff c_1=\cdots =c_n=0 \iff$ $\{[A]^1,\ldots,\,[A]^n\} \subset \mathbb{F}^m$ 은 일차독립.

(나) trivial.



<b>연습문제 4.2.16.</b> $A$ 가 square matrix 일 때, 연습문제 3.5.14 에 다음 동치조건

(사) $L_A$ 는 bijective.

(아) $L_A$ 는 surjective.

(자) $L_A$ 는 injective.

을 추가할 수 있음을 설명하라.

---

연습문제 4.2.15 와 3.5.14를 보면,

(가) $\left\{ [A]^1,\ldots,\,[A]^n\right\}$ 은 $\mathbb{F}^n$ 의 basis $\iff$ (사) $L_A$ 는 bijective.

(다) $\left\{ [A]^1,\ldots,\,[A]^n\right\}$ 은 일차독립.$\iff$ (자) $L_A$ 는 injective.

(나) $\left\langle [A]^1,\ldots,\,[A]^n\right\rangle=\mathbb{F}^n$. $\iff$ (아)  $L_A$ 는 surjective.

이다. 



<b>연습문제 4.2.17.</b> $X_0\in \mathbb{F}^n$ 이 연립방정식 $(**)\, AX=B$ 의 한 solution 이면 $(**)$ 의 해집합은
$$
(L_A)^{-1}(B)=X_0+\ker L_A
$$
임을 보여라.

---

(1) 임의의 $Z\in \ker L_A$ 에 대해 $L_A (X_0 +Z)=AX_0 +AZ=B$ 이므로 $X_0 + \ker L_A \subset (L_A)^{-1}(B)$ 이다. 

(2) 이제 $Y \in (L_A)^{-1}(B)$ 라 하자. $Y\ne X_0 +Z$ for any $Z\in \ker L_A$ 이면 $Y-X_0 \not \in \ker L_A$ 이므로 $L_A(Y-X_0)=B'\ne 0$ 이다. $L_AX_0=B$ 이므로 $L_A Y =B'+B\ne B $ 이므로 $Y\in (L_A)^{-1}(B)$ 라는 가정에 모순. 따라서 $Y \in X_0 = \ker L_A$ 이어야 하므로 $(L_A)^{-1}(B) \subset (X_0 + \ker L_A)$ 이다.

(3) From (1) and (2), $ (L_A)^{-1}(B)=X_0+\ker L_A$. 



<b>연습문제 4.2.19. </b> 는 생략.



<b>연습문제 4.2.21.</b> $A\in \mathfrak{M}_{m,\,m}(\mathbb{F})$ 일 때, 함수 $\lambda : \mathfrak{M}_{m,\,n}(\mathbb{F})\to \mathfrak{M}_{m,\,n}(\mathbb{F})$ 를
$$
\lambda_A (B) =AB,\qquad (B\in \mathfrak{M}_{m,\,n}(\mathbb{F}))
$$
로 정의하자.

(가) $\lambda : \mathfrak{M}_{m,\,n}(\mathbb{F})\to \mathfrak{M}_{m,\,n}(\mathbb{F})$ 는 linear operator 임을 보여라.

(나) $E\in \mathfrak{M}_{m,\,m}(\mathbb{F})$ 가 elementary matrix 이면 operator $\lambda_E$ 의 'operation'은 elementary row operation과 같음을 설명하라.

---

(가) $B_1,\,B_2\in \mathfrak{M}_{m,\,n}(\mathbb{F}),\, c\in \mathbb{F}$ 에 대해,
$$
\lambda_A(B_1+B_2)=A(B_1+B_2)=AB_1+AB_2 = \lambda_A (B_1)+\lambda_A(B_2)\,,\\
\lambda_A (cB_1)=A(cB_1)=cAB_1=c\lambda_A(B_1)\,.
$$
이므로 $\lambda$ 는 linear operator 이다.

(나) trivial.



<b>연습문제 4.2.22</b> (가) $\mathcal{D,\,I} : C^\infty(\R)\to C^\infty (\R)$ 을
$$
(\mathcal{D}f)(x) = f'(x),\quad (\mathcal{I}f)(x)= \int_0^x f(u)\,du,\quad (f(x) \in C^\infty(\R),\, x\in \R)
$$
로 정의하면 differential operator $\mathcal{D}$ 와 intetral operator $\mathcal{I}$ 는 linear 임을 보여라.

(나) Differential operator $\mathcal{D}: \mathbb{F}[t]\to \mathbb{F}[t]$ 와 integral operator $\mathcal{I}:\mathbb{F}[t]\to \mathbb{F}[t]$ 를 정의하라.

---

(가) trivial.

(나) trivial.



## 4.3 Linear Extention Theorem



<b>연습문제 4.3.5.</b> $\R^2$ 에서, 원점을 중심으로 (시계 반대 방향으로) $\theta$ 만큼 회전하는 $\R^2$ 의 회전변환 $R_\theta : \R^2 \to \R^2$ 를 생각해 보자.

(가) $R_\theta$ 가 왜 선형사상인지 그림으로 설명해보라.

(나) 따라서, $R_\theta$ 는 표준단위벡터 $\mathbf{e}_1$ 과 $\mathbf{e}_2$ 를 어디로 보내는지에 의해 결정되므로, $A=\begin{bmatrix} \cos \theta & -\sin \theta \\ \sin \theta & \cos \theta \end{bmatrix}$ 라고 할 때, $R_\theta = L_A$ 임을 보여라.

(다) $\theta,\, \eta\in \R,\, r \ge 0$ 일 때, 실제로,
$$
R_\theta \begin{bmatrix} r \cos \eta \\ r \sin \eta \end{bmatrix} =\begin{bmatrix} \cos \theta & -\sin \theta \\ \sin \theta & \cos \theta \end{bmatrix}\begin{bmatrix} r \cos \eta \\ r \sin \eta \end{bmatrix}  = \begin{bmatrix} r \cos (\theta+\eta) \\ r \sin (\theta+\eta) \end{bmatrix} 
$$
인 것을 확인하라.

(라) 삼각함수의 덧셈정리는 $R_\theta \circ R_\eta = R_{\theta+\eta}$ 라는 사실과 동치임을 보여라.

(마) $R_\theta$ 는 invertible(isomorphism) 이고, $(R_\theta)^{-1}=R_{-\theta}$ 임을 보여라.

---

--- to be done ---





<b>연습문제 4.3.9.</b> $V,\,W$ 가 f.d.v.s. 일 때, 다음을 보여라.

(가) Monomorphism $\varphi : V \to W$ 가 존재할 필요충분조건은 $\dim V \le \dim W$.

(나) Epimorphism $\varphi :V \to W$ 가 존재할 필요충분조건은 $\dim V \ge \dim W$. 

---

(가) $\varphi \in \mathcal{L}(V,\,W)$ 가 monomorphism 이면 (즉 injective 이면), $V \approx \operatorname{im} \varphi \le W $ 이므로 $\dim V \le \dim W$ 이다. 

$\dim V\le \dim W$ 일 때 $V$ 의 기저 $\mathcal{B}_V= \{v_1,\ldots,\,v_n\}$ 과 $W$ 의 기저 $\{w_1,\ldots,\,w_m\}$ 에 대해 $n \le m$ 임을 안다. $\varphi (v_i)=w_i$ for $i=1,\ldots,\,n$ 인 $\varphi\in \mathcal{L}(V,\,W)$ 를 생각 할 수 있으며  monomorphism 이다. 

(나) $\varphi (V,\,W)$ 가 epimorphism 이면 (즉 surjective 이면) $\dim V \ge \dim W$ 임은 관찰 4.1.15 에서 보았다. 이제 $\dim V \ge \dim W$ 일 때, $V$ 의 기저 $\mathcal{B}_V= \{v_1,\ldots,\,v_n\}$ 과 $W$ 의 기저 $\{w_1,\ldots,\,w_m\}$ 에 대해 $n \ge m$ 임을 안다. $\varphi(v_i)=w_i$ For $i=1,\ldots,\,m$ 이라 하면 $\varphi$ 는 epimorphism 이다.



## 4.4. Dimension Theorem



<b>연습문제 4.4.2.</b> [$\ker L$ 의 기저와 $\operatorname{im}L$ 의 기저]로부터 $V$ 의 기저를 construct 하는 방법으로 dimension theorem을 다시 증명하라.

----

(1) $L\in \mathcal{L}(V,\,W)$ 이며 $V$가 f.d.v.s. 이다. $\{v_1,\ldots,\,v_n\}$ 을 $\ker L$ 의 기저라 하고, $\{w_1,\ldots,\,w_m\}$ 를 $\operatorname{im}L$ 의 기저라 하자.  

(2)$L^{-1}(w_i)$ 중에 하나를 골라 $u_i$ 라 하자. (각각의 $w_i$ 에 대해 $L^{-1}(w_i)\ne \varnothing$ 인것은 자명하다). 이 때 $\{u_1,\ldots,\,u_m\}$ 은 선형독립임을 보이자. $a_1 u_1+\cdots + a_m u_m=0$ 이라 할 때 
$$
L(a_1u_1 + \cdots + a_m u_m )=a_1w_1+\cdots + a_m w_m =0 \implies a_1=\cdots =a_m=0\,
$$
이므로 선형독립이다. 

이제 $\{v_1,\ldots,\,v_n,\,u_1,\ldots,\,u_m\}$ 은 선형독립임을 보이자 $v=\sum_{i=1}^n a_i v_i + \sum_{j=1}^m b_j u_j \in V$ 라 하면 
$$
v=0 \implies L(v)=0 \implies \sum_{j=1}^m b_j w_j=0 \implies b_1=\cdots=b_m=0
$$
이다. 그렇다면 $v=0 \implies \sum_{i=1}^n a_i v_i=0 \implies a_1=\cdots=a_n=0$ 이므로 $\{v_1,\ldots,\,v_n,\,u_1,\ldots,\,u_m\}$ 는 선형독립이다.

(3) 이제 $\langle v_1,\ldots,\,v_n,\,u_1,\ldots,\,u_m \rangle=V$ 임을 보이자. $\langle v_1,\ldots,\,v_n,\,u_1,\ldots,\,u_m \rangle\le V$ 임은 자명하다. 이제 $v'\in V$ 이며 $v'\notin \langle v_1,\ldots,\,v_n,\,u_1,\ldots,\,u_m \rangle$ 라 가정하자.  $L(v')\in \operatorname{im}(L) $ 이므로,  $L(v')=\sum_{i=1}c_i w_i=L\left(\sum_{i=1}c_i u_i\right)\in \operatorname{im} L$ 이어야 한다. 그렇다면 $v'\in \sum_{i}c_i u_i + \ker V \in  \langle v_1,\ldots,\,v_n,\,u_1,\ldots,\,u_m \rangle$ 이므로 모순. 따라서  $\langle v_1,\ldots,\,v_n,\,u_1,\ldots,\,u_m \rangle= V$ 이며 $n=\dim \ker L$, $m=\dim \operatorname{im}L$, $m+n=\dim V$ 이므로 dimension theorem이 성립한다.



<b>연습문제 4.4.5.</b> [따름정리 3.5.12 에서 $V=\mathbb{F}^n$ 인 경우] 와 [따름정리 4.4.4 에서 $L=L_A : \mathbb{F}^n \to \mathbb{F}^n$ 인 경우] 는 동치임을 설명해보라.

---

(1) 따름정리 3.5.12 에서  : $S=\{v_1,\;\ldots,\,v_n\}\subseteq \mathbb{F}^n$ 일 때 다음  조건은 동치이다.

​	(가) $S$ 는 $\mathbb{F}^n$ 의 기저.

​	(나) $S$ 는 일차독립.

​	(다) $\langle S \rangle=\mathbb{F}^n$. 

(2) 따름정리 4.4.4 에서 $L=L_A:\mathbb{F}^n \to \mathbb{F}^n$ 인 경우  다음 조건은 동치이다.

​	(가) $L$ 은 isomorphism.

​	(나) $L$ 은 monomorphism.

​	(다) $L$ 은 epimorphism.

(3) $S=\{v_1,\ldots,\,v_n\}$ 이며 $u_i = L_A(v_i)=Av_i$ , $S' =\{u_1,\ldots,\,u_n\}\subseteq{F}^n$ 이라 하자. 

--- to be done--



<b>연습문제 4.4.8. </b>$V_1,\ldots,\,V_k$ 가 f.d.v.s. 일 때, (첫번째 좌표료의) natural projection $\pi_1 : \prod_{i=1}^k V_i \to V_1$ 을 생각하고 (보기 4.2.5), 다음을 보여라.

(가) $\ker \pi_1 \approx V_2 \times \cdots \times V_k$. 

(나) $\dim \left( \prod_{i=1}^k  V_i \right)=\sum_{i=1}^k \dim V_i$.

---

(가) $V=V_1 \times \cdots \times V_k$ 라 하자.  $v= (v_1,\ldots,\,v_k)\in V$ 일 때 $\pi_1 (v)=0 \iff v_1=0$ 이므로 $\dim (\ker \pi_1)= \dim (V_2 \times \cdots \times V_k)$ 이다. 따라서 주어진 식이 성립한다. 

(나) 수학적 귀납법으로 증명한다. $k=1$ 일 경우는 자명하다. $k = n$ 일 때 성립함을 가정하자. $k=n+1$ 일 때 $\pi_1 : \prod_{i=1}^{n+1}V_i \to V_1$ 을 생각한다. $\dim (\operatorname{im} \pi_1) = \dim V_1$ 이며, 귀납적 가정에 의해 $\dim (\ker \pi_1)= \dim (V_2 \times \cdots \times V_{n+1}) = \sum_{i=2}^{n+1} \dim V_i$ 이므로 주어진 식이 성립한다.



<b>연습문제 4.4.10. </b> $\mathbb{F}$-위의 polynomial space $\mathbb{F}[t]$ 의 부분집합 $S=\{t^i : i \ge 1\}$ 을 생각하자. 그리고 선형사상 $\varphi : \mathbb{F}[t]\to \mathbb{F}[t]$ 를 
$$
\varphi (f(t))=tf(t) \,, \qquad(f(t) \in \mathbb{F}[t])
$$


로 정의하자.

(가) $S$ 는 일차독립이고, $|S|=\dim \mathbb{F}[t]$ 이지만, $S$ 는 $\mathbb{F}[t]$ 전체를 생성하지 못하는 것을 보여라.

(나) $\varphi : \mathbb{F}[t]\to \mathbb{F}[t]$ 는 monomorphism 이지만 epimorphism이 아님을 보여라.

(다) Epimorphism 이지만 monomorphism이 아닌 선형사상 $\psi :\mathbb{F}[t]\to \mathbb{F}[t]$ 를 찾아라.

---

(가) $S$ 는 일차독립임은 자명. $|S|=|\N|=\dim \mathbb{F}[t]$. $t+1 \in \mathbb{F}[t]$ but $t+1 \not\in \langle S\rangle$. 

(나) $t + 1 \in \mathbb{F}[t]$.  $\varphi (f(t))=tf(t)=t+1$ 을 만족하는 $f(t)\in \mathbb{F}[t]$ 는 존재하지 않으므로 surjection은 아님. $\varphi (f(t))=\varphi (g(t))$ 이면 $tf(t)=t(g(t))$ 이며 $f(t)=g(t)$ 이다. 따라서 $\varphi$ 는 injection 임.

$f,\,g \in \mathbb{F}[t],\, c\in \mathbb{F}$ 에 대해 $\varphi (f(t)+g(t))=t(f(t)+g(t))=tf(t)+tg(t) = \varphi (f(t))+\varphi (g(t))$. $\varphi (cf(t))=t(cf(t))=ctf(t) = c\varphi (f(t))$ 이므로 $\varphi$ 는 linear map. 

(다) Differential operator $\mathcal{D}$. 



## 4.5 Rank Theorem.



<b>연습문제 4.5.7. </b> $A,\,B \in \mathfrak{M}_{m,\,n}(\mathbb{F})$ 일 때, 다음을 증명하라.

(가) $A \sim_r B$ 또는 $A \sim^c B$ 이면 $\operatorname{rk}(A)=\operatorname{rk}(B)$. 

(나) $A$ 가 가역이면 (물론 $m=n$ ), $A$ 는 full rank 를 갖는다. 즉, $\operatorname{rk}(A)=n$. 

---

(가) 따름정리 4.5.6 (가) 의 동어반복. 

(나) $A \in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 라 하자. $A$ 가 가역면 $A \sim_r I_n$ 이며 $\operatorname{rk}(I_n)=n=\operatorname{rk}(A)$. 



<b>연습문제 4.5.8.</b>  $A\in \mathfrak{M}_{m,\,n}(\mathbb{F})$ 일 때 다음을 증명하여라.

(가) $Q\in \mathfrak{M}_{m,\,m}(\mathbb{F})$ 가 가역이면 $\operatorname{rk}(QA)=\operatorname{rk}(A)$. 

(나) $P\in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 가 가역이면 $\operatorname{rk}(AP)=\operatorname{rk}(A)$. 

(다) $Q\in \mathfrak{M}_{m,\,m}(\mathbb{F})$ 와 $P\in \mathfrak{M}_{n,\,n}(\mathbb{F})$ 가 가역이면 $\operatorname{rk}(QAP)=\operatorname{rk}(A)$. 

---

(가) $QA\sim_r I_mA=A$.

(나) $AP \sim^c AI_n=A$. 

(다) $QAP\sim_r AP \sim_c A$.



