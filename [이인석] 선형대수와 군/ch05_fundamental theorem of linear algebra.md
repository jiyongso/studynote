제 5 장 기본정리
====



## 5.1 Vector Space of Linear Map.



<b>연습문제 5.1.2.</b> $L,\,L'\in \mathcal{L}(V,\,W)$, $M,\,M'\in \mathcal{L}(W,\,U)$, $N\in \mathcal{L}(U,\,U')$, $r\in \mathbb{F}$ 일 때 다음 '기본' 규칙들이 성립함을 보여라.

(가) $(N \circ M) \circ L = N\circ(M \circ L)$. 

(나) $L \circ I_V = L$, $I_W \circ L = L$. 

(다) $(M+M')\circ L = M \circ L + M'\circ L$, $M\circ (L+L')=M \circ L + M \circ L'$. 

(라) $(rM) \circ L = r (M \circ L)= M \circ (rL)$. 



(가) $v\in V$ 에 대해 $L(v)=w$, $M(w)=u$ 라 하면,
$$
((N \circ M)\circ L)(v)=(N\circ M)(L(v)))=(N\circ M)(w)= N(M(w))=N(u)\,,\\
(N\circ (M \circ L))(v)=N((M\circ L)(v))=N(M(w))=N(u)\,.
$$
(나) $(L\circ I_V)(v)=L(I_V (v))=L(v)$, $(I_W\circ L)(v)=I_W (L(v))=L(v)$. 

(다) $v,\, v'\in V$ 에 대해 $L(v)=w,\, L(v')=w'$ 이라 하면,
$$
((M+M')\circ L)(v)=(M+M')(w)=M(w)+M'(w) = (M\circ L)(w)+(M'\circ L)(w)\,,\\
(M\circ(L+L'))(v)=M(w+w')=M(w)+M(w')=(M\circ L)(w) + (M\circ L')(w) \,.
$$
 (라) $v\in V$ 에 대해 $L(v)=w$ 라 하면,
$$
\begin{align*}
((rM)\circ L)(w)& = rM(w)=r(M(w))=r(M\circ L )(v)\,,\\
&=rM(w)=M(rw)=M(rL(v))=(M\circ(rL))(v) \,.

\end{align*}
$$


<b>연습문제 5.1.3.</b> $L,\,M \in \mathcal{L}(V,\,W)$ 일 때ㅔ, 다음을 보여라.

(가) $(L+I)\circ (L-I)=L^2-I$.

(나) $(L+M)^2=L^2+L\circ M + M \circ L + M^2$.

(다) $(L-I)\circ(L^m + L^{m-1}+\cdots + L+I)=L^{m+1}-I$.

---

(가) $(L+I)\circ (L-I)=(L+I)\circ L - (L+I)\circ I = L^2+L - L -I = L^2-I$. 

(나) $(L+M)^2= (L+M)\circ (L+M)=(L+M)\circ L + (L+M)\circ M=L^2+M \circ L + L \circ M +M^2$. 

(다) 
$$
\begin{align*}
(L-I)\circ (L^m+L^{m-1}+ \cdots +L+I) &=L(L^m+L^{m-1}+ \cdots +L+I)-(L^m+L^{m-1}+ \cdots + L+I)\\
&=L^{m+1}+ L^m+\cdots +L^2+L -(L^m+L^{m-1}+L+I)\\
&=L^{m+1}-I
\end{align*}
$$
<b>연습문제 5.1.4.</b> [$L^r=0$ for some $r\ge 1$] 인 linear operator $L\in \mathcal{L}(V,\,W)$ 를 **nilpotent operator** 라고 부른다. 만약 $L,\,M\in \mathcal{L}(V,\,V)$ 가 nilpotent 이고 $L\circ M = M \circ L$ 이면 $(L+M)$ 도 nilpotent 임을 보여라.

---

$L^r=0$, $M^s=0$ 이며 $n=\max (r,\,s)$ 라 하자.
$$
(L+M)^{2n} =\sum_{k=1}^{2n} \begin{pmatrix} 2n \\ k \end{pmatrix} L^kM^{2n-k}
$$
이다.  $k\ge n$ 이면 $L^k=0$, $k\le n$ 이면 $L^{2n-k}=0$ 이므로 위 식은 $0$ 이 된다.



<b>연습문제 5.1.5. </b> $L\in \mathcal{L}(V,\,V)$ 이고
$$
f(t) = a_n t^n + \cdots + a_1 t+a_0, \qquad (\text{단 }, a_n,\ldots,\,a_1,\,a_0\in \mathbb{F})
$$
가 $\mathbb{F}[t]$ 의 polynomial 일 때,
$$
f(L)=a_nL^n +\cdots + a_1L+a_0 I
$$
로 표기하는 것은 매우 자연스럽다. 우리는 $f(L)$ 을 [**evaluation** of $f(t)$ at $L$ ]이라고 부른다. 이제 $f(t),\,g(t) \in \mathbb{F}[t]$ , $c\in \mathbb{F}$ 일 때, 다음을 보여라.

(가) $(f+g)(L)=f(L)+g(L)$. 

(나) $(cf)(L)=cf(L)$. 

(다) $fg(L)=f(L) \circ g(L)$. 

---

귀찮고.. 지겹고.. 당연하고..



<b>연습문제 5.1.8.</b> $V$ 가 **f.d.v.s.** 일 때 $\psi : V \to V^{**}$ 를
$$
\psi (v)(f)=f(v)\,, \qquad (v\in V,\, f\in V^*)
$$
로 정의 할 때, 다음을 보여라.

(가) $v\in V$ 이면, $\psi (v)$ 는 linear. 즉 $\psi (v) \in V^{**}$. 

(나) $\psi : V \to V^{**}$ 는 isomorphism.

(다) $\{v_i\}$ 가 $V$ 의 기저일 때, $v_i^{**}=(v_i^*)^*$ 로 표기하면, $\psi(v_i)=v_i^{**}$. 

---

(가) $v,\,v'\in V,\, c\in \mathbb{F}$ 라 하자. 
$$
\begin{align*}
\psi (v+v')(f) &=f(v+v')=f(v)+f(v')=\psi(v)(f)+\psi(v')(f)\,,\\
\psi (cv)(f)&=f(cv)=cf(v)=c(\psi(v)(f))\;.

\end{align*}
$$
(나) $0=\psi(v)(f)=f(v) \implies v=0$. $\dim V^{**} =\dim V^* = \dim V$ 이므로 $\psi$ 는 isomorphism 이다.

(다) $\{v_i\}$ 가 $V$ 의 기저이면 $\{v^*_i\}$ 는 $V^*$ 의 기저이고 $\{v_i^{**}\}$ 는 $V^{**}$ 의 기저이다. 따라서,
$$
\psi(v_i)(v_j^*)=v_j^*(v_i)=\delta_{ij}
$$
이므로 $v_i^{**}=\psi(v_i)$ .



<b>연습문제 5.1.19. </b> $V$ 와 $W_1,\ldots,\,W_k$ 가 벡터공간일 때, 다음을 보여라.

(가) $\mathcal{L}(V,\, \prod_{i=1}^k W_i)\approx\prod_{i=1}^k \mathcal{L}(V,\,W_i)$.

(나) $\mathcal{L}(\prod_{i=1}^k W_i,\,V)\approx \prod_{i=1}^k \mathcal{L}(W_i,\,V)$.

---

$\{v_i\}$ 를 $V$ 의 기저, $\{w_{p_j}^{(j)}\}$ 를 $W_j$ 의 기저라 하자. 그렇다면 $\{(w_{p_1}^{(1)},\ldots,\, w_{p_k}^{(k)})  \}$ 는 $\prod_{j=1}^k W_j$ 의 기저가 된다. 

이제 $\mathcal{L}(V,\,W_1)\times \mathcal{L}(V,\, W_2)$ 을 어떻게 정의할까? $\phi_1\in \mathcal{L}(V,\,W_1),\, \phi_2 \in \mathcal{L}(V,\,W_2)$ 라 하자.  $v\in V$ 에 대해 $(\phi_1,\,\phi_2) (v)=(\phi_1(v),\,\phi_2(v))$ 라 하면 $(\phi_1,\,\phi_2)$ 는 vector 의 direct product의 정의에도 맞고, 자체로 $V \to W_1 \times W_2$ linear map 이다. (이건 쉽게 보일 수 있으므로 생략한다.) 이제 우리는 $\prod_{i=1}^k \mathcal{L}(V,\,W_i)$ 을 잘 정의하게 되었다. 

(가) $\phi_{j,\,p_1,\,p_2,\ldots,\,p_k}(v_i)=\delta_{ij}\left( w^{(1)}_{p_1},\ldots,\, w^{(k)}_{p_k} \right)$ 는 $\mathcal{L}(V,\, \prod_{i=1}^k W_i)$ 의 basis 이다. $\phi^{(p)}_{j,\,p_l}(v_i)=\delta_{ij} w^{(p)}_{p_l}$ 라 하자. 그렇다면 $\prod_{i=1}^k \mathcal{l}(V,\,W_i)$ 의 basis 는 $\left( \phi_{j_1,\,p_1}^{(1)},\ldots,\, \phi_{j_k,\,p_k}^{(k)} \right) $ 이다.  그런데 $\left( \phi_{j_1,\,p_1}^{(1)},\ldots,\, \phi_{j_k,\,p_k}^{(k)} \right)(v_i)=\delta_{i,\,j_1}\cdots \delta_{i,\,j_k}\left( w^{(1)}_{p_1},\ldots,\,w^{(k)}_{p_k}\right)$ 이다. $\psi_{j_1,\ldots,\,j_k,\,p_1,\ldots,\,p_k}=  \left( \phi_{j_1,\,p_1}^{(1)},\ldots,\, \phi_{j_k,\,p_k}^{(k)} \right)$ 로 정의하면 $\phi_{j,\,p_1,\,p_2,\ldots,\,p_k}(v_i)=\delta_{j,\,j_1}\cdots \delta_{j,\,j_p}\psi_{j_1,\ldots,\,j_k,\,p_1,\ldots,\,p_k}=\psi_{j,\cdots,\,j,\,p_1,\ldots,\,p_k}$ 이므로 (가) 의 관계가 성립함을 알 수 있다.

(나) (가) 와 같은 논리로 증명 할 수 있다.



## 5.2 기본정리 : 표준기저의 경우



<b> 표기법 5.2.1</b> 이 절에서는 다음과 같은 notation을 사용한다.

- $V=\mathbb{F}^n$  : $\dim V=n$, 	[ $\mathbb{F}^n$ 의 표준기저 ] $=\mathcal{E}=\{\mathbf{e}_1,\ldots,\,\mathbf{e}_n\}$.  
- $W=\mathbb{F}^m$ : $\dim W=m$,  [ $\mathbb{F}^m$ 의 표준기저 ] $=\mathcal{F}=\{\mathbf{f}_1,\ldots,\,\mathbf{f}_m \}$. 
- $U=\mathbb{F}^r$   : $\dim U=r$,     [ $\mathbb{F}^r$ 의 표준기저 ] $=\mathcal{G}=\{\mathbf{g}_1,\ldots,\,\mathbf{g}_r\}$. 



#### Notation

- $L\in \mathcal{L}(\mathbb{F}^n,\,\mathbb{F}^m)$ 일 때 $[L]^\mathcal{E}_{\mathcal{F}}$ 는 $L$ 을 표준기저 $\mathcal{E}$ 와 $\mathcal{F}$ 에서 기술한 행렬표현을 의미한다. 즉 $\displaystyle L(\mathbf{e}_j)=\sum_{i=1}^m a_{ij}\mathbf{f}_i$ 이다.



#### 선형대수학의 기본정리

$\Phi^\mathcal{E}_{\mathcal{F}}=\Phi : \mathfrak{M}_{m,\,n}(\mathbb{F})\to \mathcal{L}(\mathbb{F}^n,\,\mathbb{F}^m)$ 를 다음과 같이 정의한다.
$$
\Phi^{\mathcal{E}}_\mathcal{F} (A)= \Phi(A)=L_A\,.\qquad (A\in \mathfrak{M}_{m,\,n}(\mathbb{F}))
$$
 또, $\Psi^\mathcal{E}_\mathcal{F}=\Psi :\mathcal{L}(\mathbb{F}^n,\,\mathbb{F}^m) \to \mathfrak{M}_{m,\,n}$ 을 다음과 같이 정의한다.
$$
\Psi^\mathcal{E}_\mathcal{F}(L)=\Psi(L)=[L]=[L]^\mathcal{E}_{\mathcal{F}}\,. \qquad (L \in \mathcal{L}(\mathbb{F}^n,\,\mathbb{F}^m))
$$
이 때 다음이 성랍힌다.

(가) $\Phi^\mathcal{E}_\mathcal{F}$ 와 $\Psi^\mathcal{E}_{\mathcal{F}}$ 는 isomorphism 이고 $\left( \Phi^\mathcal{E}_\mathcal{F}\right)^{-1}=\Psi^\mathcal{E}_{\mathcal{F}}$ 이다. 

(나) $B\in \mathfrak{M}_{m,\,n}(\mathbb{F})$ 이고 $A\in \mathfrak{M}_{m,\,n}(\mathbb{F})$ 이면,
$$
\Phi^\mathcal{F}_\mathcal{G}(B)\circ \Phi^\mathcal{E}_\mathcal{F}(A)=\Phi^\mathcal{E}_\mathcal{G}(BA), \quad \text{i. e.} \quad L_B \circ L_A=L_{BA}
$$
가 성립한다. 또 $L\in \mathcal{L}(\mathbb{F}^n,\,\mathbb{F}^m)$ 이고 $M\in \mathcal{L}(\mathbb{F}^m,\, \mathbb{F}^r)$ 이면,
$$
\Psi^\mathcal{F}_\mathcal{G}(M)\circ \Psi^\mathcal{E}_\mathcal{F}(L)=\Psi^\mathcal{E}_\mathcal{G}*(M \circ L),\quad\text{i. e. } \quad \left[M\right]^\mathcal{F}_\mathcal{G}\cdot \left[L\right]^\mathcal{E}_\mathcal{F} =\left[M \circ L\right]^\mathcal{E}_\mathcal{G}
$$
가 성립한다.

----

*(proof)* (가-1) 우선 $\Phi^\mathcal{E}_\mathcal{F}=\Phi$ 가 linear map임을 보이자. 임의의 $c\in \mathbb{F},\, X\in \mathbb{F}^n$ 와 $A,\,B\in \mathfrak{M}_{m,\,n}$  에 대해,
$$
\begin{align*}
\Phi (A+B) X&=L(A+B)X=AX+BX=(\Phi(A)+\Phi(B))X\,,\\
\Phi(cA) X&=L(cA)X=(cA)X=c(AX)=c\Phi(A)X\,.
\end{align*}
$$
따라서 $\Phi^\mathcal{E}_\mathcal{F}$ 는 linear map 이다. isomorphism 임은 쉽게 보일 수 있다.

(가-2) 이제 $\Psi^\mathcal{E}_\mathcal{F}=\Psi$ 가 linear map 임을 보이자. 임으의 $c\in \mathbb{F},\, X\in \mathbb{F}^n$ 과 $L,\,M \in \mathcal{L}(\mathbb{F}^n,\,\mathbb{F}^m)$ 에 대해,
$$
\begin{align*}
\Psi(L+M)&= [L+M]^\mathcal{E}_{\mathcal{F}}=[L]^\mathcal{E}_\mathcal{F}+[M]^\mathcal{E}_\mathcal{F}=\Psi(L)+\Psi(M)\,,\\
\Psi(cL)&=[cL]^\mathcal{E}_{\mathcal{F}}=c[L]^\mathcal{E}_\mathcal{F}=c\Psi(L)\,.

\end{align*}
$$
 따라서 $\Psi^\mathcal{E}_\mathcal{F}$ 는 linear map 이다. isomorphism 임은 쉽게 보일 수 있다.

(가-3) $\Psi\circ \Phi : \mathfrak{M}_{m,\,n} \to \mathfrak{M}_{m,\,n}$ 를 생각하자.  $A\in \mathfrak{M}_{m,\,n},\, \mathbf{e}_i \in \mathcal{E}$ 에 대해,
$$
(\Psi \circ \Phi )(A)\mathbf{e}_i = \Psi(L_A)\mathbf{e}_i=[L_A]^\mathcal{E}_\mathcal{F}\mathbf{e}_i=[A]^{i}=A\mathbf{e}_i
$$
이다. 따라서 $\Psi \circ \Phi = I$ 이다. 

(가-4) $\Phi \circ \Psi : \mathcal{L}(\mathbb{F}^n,\,\mathbb{F}^m) \to \mathcal{L}(\mathbb{F}^n,\,\mathbb{F}^m)$ 을 생각하자. $L \in\mathcal{L}(\mathbb{F}^n,\,\mathbb{F}^n),\, \mathbf{e}_i\in \mathcal{E}$ 에 대해, $L\mathbf{e}_i = \sum_{j=1}^m c_{ji} \mathbf{f}_j$ 라 하자. 
$$
\Phi\circ \Psi (L)\mathbf{e}_i= \Phi\left( [L]^\mathcal{E}_\mathcal{F} \right)\mathbf{e}_i= [L]^\mathcal{E}_\mathcal{F} \mathbf{e}_i =
$$
