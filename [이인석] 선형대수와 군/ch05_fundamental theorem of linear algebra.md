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

$\{v_i\}$ 를 $V$ 의 기저, $\{w_k^{(j)}\}$ 를 $W_j$ 의 기저라 하자. 그렇다면 $\{(w_{k_1}^{(1)},\, w_{k_2}^{(2)},\ldots)  \}$ 는 $\prod_{j=1}^k W_j$ 의 기저가 된다. 

(가) $E_{j,\,k_1,\,k_2,\,k_3,\ldots}(v_i)=\delta_{ij} (w_{k_1}^{(1)},\, w_{k_2}^{(2)},\ldots)$  는 $\mathcal{L}(V,\, \prod_{k=1} W_k)$ 의 basis 이며, $\mathcal{L}(V,\,W_k)$ 의 basis 는 $E_{jk_p}(v_i)=\delta_{ij}w^{(k)}_{k_p}$ 이므로, 



$\varphi : \mathcal{L}(V,\, \prod_{i=1}^k W_i)\to\prod_{i=1}^k \mathcal{L}(V,\,W_i)$ defined by $