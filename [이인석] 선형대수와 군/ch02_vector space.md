제 2 장. 벡터공간
===

#### Notations

- Field $\mathbb{F}$ 에 대해 $\mathbb{F}^n$ 을 우리는 알고 있다. 이제 우리는 $\mathbb{F}^n=\mathfrak{M}_{n,\,1}(\mathbb{F})$ 으로 생각하기로 한다. 
- $X=(x_1,\ldots,\,x_n)^t\in \mathbb{F}^n$ 일 때 $x_i$ 를 $X$ 의 $i$-th coordinate 라 한다.
- Vector space $U,\,V$ 에 대해 $U$ 가 $V$ 의 subspace 일 때 $U\le V$ 라 쓰기로 한다.
- Fielf $\mathbb{F}$ 위에서의 vector space를 $\mathbb{F}$-vector space 라 한다. 
- Field $\mathbb{F}$ 위에서의 다항식 전체의 집합을 $\mathbb{F}[t]$ 라 한다. 
- $\mathcal{P}_n(\mathbb{F}) =\{f(t) \in \mathbb{F}[t] : \deg (f) \le n\}$ 





## 2.1 Vector Space



<b>연습문제 2.1.7. </b> $v,\,w \in V$ 일 때 다음을 보여라.

(가) $-(-v)=v$.

(나) $-(v+w)=-v-w$. 

(다) $-(v-w)=w-v$. 

---

(가) $(-v)-(-(v))=(-v)(1-1)=0$. 

(나) $(v+w)-v-w=0$.

(다) $(v-w)+(w-v)=0$. 



## 2.2 Subspace



 <b>연습문제 2.2.5.</b> (가) $\{(a,\,b,\,c)^t \in \mathbb{F}^3 : a^2+3b-c=0\}\le \mathbb{F}^3$ 인가?

(나) $\{(a,\,b,\,c)^t \in \mathbb{F}^3 : 2a+3b-1=0\}\le \mathbb{F}^3$ 인가?

(다) $\{ (a,\,b,\,c)^t \in \mathbb{F}^3 : 2a+3b-c=0\} \le \mathbb{F}^3$ 인가?

---

(가), (나), (다) 에서 기술된 집합을 $A$ 라 하자.

(가) $u=(1, 1, 4)\in A,\, v=(-1,\,1,\,4)\in A$ but $u+v=(0,\,1,\,4)\not\in A$. 따라서 No.

(나) $u=(-1,1,0) \in A,\, v=(2,\,-1,\,0)\in A$. $u+v=(1,0,0) \not \in A$. 따라서 No.

(다) $u=(u_1,\,u_2,\,u_3)\in A,\, v=(v_1,\,v_2,\,v_3)\in A$ 라 하자. $2u_1 + 3u_2 -u_3=2v_1+3v_2-v_3=0$ 이다. 이 때, $u+v=(u_1+v_1,\,u_2+v_2,\,u_3,\,v_3)$ 이며,
$$
2(u_1+v_1)+3(u_2+v_2)-(u_3+v_3)=(2u_1+3u_2-u_3)+(2v_2+3v_2-v_3)=0
$$
 이다. 또한 임의의 상수 $t$에 대해 $2(tu_1)+3(tu_2)-tu_3=t(2u_1+3u_2-u_3)=0$ 이므로 OK.



<b>연습문제 2.2.7.</b> (가) $I$ 가 non-empty set 이고, 만약 $[W_i \le V \text{ for all }i\in I]$ 이면 $\bigcap_{i\in I} W_i \le V$ 임을 보여라.

(나) $W_1,\ldots,\,W_k \subseteq V$ 일 때,
$$
\sum_{i=1}^k W_i = W_1 + \cdots +W_k = \{w_1+\cdots w_k \in V: w_1\in W_1,\ldots,\,w_k \in W_k \}
$$
 로 표기하고 $W_1,\ldots,\,W_k$ 의 합(sum) 이라고 부른다. 이제 $W_1,\ldots,\,W_k \le V$ 이면 $\sum_{i=1}^k W_i \le V$ 임을 보여라.

---

(가) Let $W=\bigcap_{i\in I} W_i$. 
$$
w_1,\,w_2\in W \implies \forall i\in I\, w_1,\,w_2 \in W_i \implies \forall i\in I\, w_1+w_2 \in W_i \implies w_1+w_2\in W\\
w \in W,\, c\in \mathbb{F} \implies \forall i\in I\, w\in W_i,\, cw\in W_i \implies cw\in W
$$


(나) Let $W=\displaystyle \sum_{i=1}^k W_i$  and $u_i\in W_i,\, v_i \in W_i$ for $i=1,\ldots,\,k$. Then $u_i+v_i \in W_i$ for all $i=1,\ldots,\,k$ and,
$$
u_1+\cdots +u_k+v_1+\cdots +v_k = (u_1+v_1)+ \cdots + (u_k+v_k) \in W,\\
$$


Let $w_i \in W_i$ for $i=1,\ldots,\,k$ and $c\in \mathbb{F}$. Then, $cw_i \in W_i$ and
$$
c(w_1+\cdots+w_k)=cw_1+\cdots +cw_k \in W
$$
따라서 $W=\displaystyle \sum_{i=1}^k W_i \le V$. 



## 2.3. Vector Space의 보기.

<b>연습문제 2.3.3</b> 한 개의 원소만을 갖는 벡터공간은 모두 사실상 같은 벡터공간임을 설명하라. 이를 우리는 (the) **zero space** 라고 부르고 $0$ 으로 표기한다. 즉, $0=\{0\}$. 

---

trivial 한데 임의의 $c\in \mathbb{F}$ 에 대해 $c0=0$ 임을 알면 쉽게 이해 할 수 있다.



<b>연습문제 2.3.5.</b> (가) $\C$ 를 $\R$-vector space로 볼 수 있음을 설명하라.

(나) $\R$ 은 $\R$-vector space $\C$ 의 $\R$-subspace 인가?

(다) $\R$ 은 $\C$-vector space $\C$ 의 $\C$-subspace 인가?

---

(가) 우리는 field $\mathbb{F}$ 가 $\mathbb{F}$-vector space임을 보기 2.3.4에서 배웠다.  $x+iy \in \C$, $c\in \mathbb{F}$ 에 대해 $c(x+iy)=cx+icy\in \C$ 이므로 $\C$ 는 $\R$-vector space 이다.

(나) Yes

(나) No



<b>Exercise 2.3.6.</b> (가) $\mathbb{F}^3$ 의 subspace $W=\{(a,\,b,\,c)^t\in \mathbb{F}^3 : c=0 \}$ 은 $\mathbb{F}^2$ 와 사실상 같은 vector space 임을 설명하라.

(나) $U=\{(a,\,b,\,c)^t \in \mathbb{F}^3: b=c\}$ 는 $\mathbb{F}^3$ 의 subspace 임을 보이고, $U$ 도 $\mathbb{F}$ 와 사실상 같은 vector space 임을 설명하라.

(다) $U$ 와 $W$ 는 사실상 같은 vector space 임을 설명하라.

(라) $U \cap W$ 는 $\mathbb{F}$ 와 사실상 같은 vector space 임을 설명하라.

(마) $U+W =\mathbb{F}^3$ 임을 보여라.

---

(가) $(a,\,b,\,0)^t\in W$ 와 $(a,\,b)^t\in \mathbb{F}^2$ 를 생각하면 $(a,\,b,\,0)^t \longleftrightarrow (a,\,b)$ 사이에 bijection이 존재하며 서로 대응하는 벡터의 합과, 임의의 $c\in \mathbb{F}$ 에 대한 곱도 대응한다.

(나) $(a,\,b,\,b)^t\in W$ 와 $(a,\,b)^t\in \mathbb{F}$ 사이에서도 (가) 와 같은 관계가 성립한다.

(다) (가), (나) 로 부터 자명하다.

(라) $U\cap W = \{(a,\,0,\,0)^t \} $ 임을 알면 trivial 하다.

(마) $U+W=\{(a+a',\, b+b',\, b)^t: (a,\,b,\,b)^t\in U,\, (a',\,b',\,0)^t\in W\}$ 이다. 임의의 $(x,\,y,\,z)^t\in \mathbb{F}^3$ 에 대해 $a+a'=x,\, b+b'=y,\, b=z$ 가 되도록 정할 수 있으므로 $\mathbb{F}^3 \le U+W$ 이다. 또한 $U \le \mathbb{F}^3$, $V\le \mathbb{F}^3$ 이므로 $U+V \le \mathbb{F}^3$ 이다. 따라서 $U+V=\mathbb{F}^3$ 이다.



<b>연습문제 2.3.8.</b> $U,\,V,\,W$ 가 vector space 일 때,

(가) $V\times W$ 는 $W \times V$ 와 사실상 같은 벡터공간임을 보여라.

(나) $(U \times V) \times W$ 와 $(U \times V)\times W$, 그리고 $U \times V\times W$ 는 사실상 같은 벡터공간임을 보여라.

---

그냥 isomorphism 개념을 쓴다.

(가) Define $\phi : V \times W \to W \times V$ by $\phi ((v,\,w))=(w,\,v)$. $\phi$ 가 bijection 임은 자명하다. $v,\,v'\in V,\, w,\,w'\in W$ 에 대해,
$$
\phi (v,\,w)+\phi (v',\,w')=(w,\,v)+(w',\,v')=(w+w',\,v+v')=\phi(v+v',\,w+w')
$$
이며 $v\in V,\, w\in W,\, c\in \mathbb{F}$ 에 대해,
$$
 c\phi (v,\,w)=c(w,\,v)=(cw,\,cv)=\phi(cv,\,cw)
$$
이다. 

(나) 는 쉽다.





<b>연습문제 2.3.9.</b> 생략



<b>연습문제 2.3.10.</b> 생략



<b>연습문제 2.3.11. </b> 생략



<b>연습문제 2.3.12. </b> 앞으로 우리는
$$
\mathcal{P}_n (\mathbb{F})=\{ f(t) \in \mathbb{F}[t] : \deg(f)\le n \}
$$
의 notation을 사용할 것이다. 우선, $\mathcal{P}_n(\mathbb{F})$ 은 $\mathbb{F}[t]$ 의 $\mathbb{F}$-subspace 임을 보이고, $\mathcal{P}_n(\mathbb{F})$ 는 $\mathbb{F}^{n+1}$ 과 사실상 같은 $\mathbb{F}$-vector space 임을 보이시오.

---

$\mathcal{P}_n(\mathbb{F}) \le \mathbb{F}[t]$ 임을 보이는 것은 쉽다. $f(t)=a_n t^b + \cdots a_1t+a_0$ 와 $(a_n,\,\ldots,\,a_0 )\in \mathbb{F}^{n+1}$ 을 대응시키면 bijection 이며 벡터의 합과 스칼라곱도 대응함을 쉽게 보일 수 있다.



<b>연습문제 2.3.13</b> $A$ 가 square matrix 이고 $f(t)\in \mathbb{F}[t] $ 가
$$
f(t) =a_nt^n + \cdots a_1t +a_0
$$
일 때,
$$
f(A) = a_n A^n + \cdots a_1 A + a_0 I
$$
로 표기하는 것은 매우 자연스럽다. 이 때 우리는 $f(A)$ 를  [ **evaluation** of $f(t)$ at $A$ ] 라고 부른다. 이제 $f(t),\, g(t) \in \mathbb{F}[t]$, $c\in \mathbb{F}$ 일 때, 다음을 보여라.

(가) $(f+g)(A)= f(A)+g(A)$.

(나) $(cf)(A)=cf(A)$.

(다) $(fg)(A)=f(A)g(A)$. 

---

Trivial but boring.



## 2.4 Isomorpism



<b>연습문제 2.4.5.</b> (가) **항등사상 (identity map)** $I_V =I : V \to V$ 를
$$
I_V (v) = I(v) = v,\quad (v\in V)
$$
로 정의 하면 $I_V$ 는 isomorphism 임을 보여라.

(나) 또 isomorphism $\varphi : V \to W$ 의 **역사상 (inverse map)** $\varphi^{-1}:W \to V$ 도 isomorphism 임을 보여라.

(다) 두개의 isomorphism $\psi : U \to V$ 와 $\varphi : V \to W$ 의 **합성 (composition)**  $\varphi \circ \psi :U \to W$ 도 isomorphism 임을 보여라.

---

(가) $I_V$ 가 bijection 임은 자명하다. $v_1,\,v_2\in V$ 에 대해 $I_V (v_1+v_2) = v_1+v_2=I_V (v_1)+I_V(v_2)$, $v\in V,\, c\in \mathbb{F}$ 에 대해 $I_V (cv)=cv=cI_V(v)$ 이므로 $I_V$ 는 isomorphism 이다.

(나) $\varphi$ 가 isomorphism 이므로 $\varphi^{-1}$ 은 bijection 이다. $\varphi(v_1)=w_1,\,\varphi(v_2)=w_2$ 라 하자.  $c \in \mathbb{F}$ 에 대해, 
$$
\varphi^{-1}(w_1+w_2)=v_1+v_2 = \varphi^{-1}(v_1)+\varphi^{-1}(v_2)\,,\\
\varphi^{-1}(cw_1 )=cv_1 = c\varphi^{-1}(v_1)
$$
이므로 $\varphi^{-1}$ 도 bijection 이다.

(나) $\psi (u_1)=v_1,\,\psi (u_2)=v_2$, $\varphi(v_1)=w_1,\,\varphi (v_2)=w_2$, $c\in \mathbb{F}$ 라 하자. $\varphi \circ \psi$ 가 bijection 임은 쉽게 보일 수 있으므로,
$$
(\varphi \circ\psi) (u_1+u_2)=\varphi (\psi(u_1)+\psi (u_1))=\varphi (v_1+v_2)=w_1+w_2=\varphi(v_1)+\varphi (v_2)= (\varphi \circ \psi) (u_1)+ (\varphi \circ \psi) (u_2)\,,\\
(\varphi \circ \psi )(cu_1)=\varphi(cv_1)=cw_1=c(\varphi \circ \psi)(u_1) 
$$
이므로 $\varphi \circ \psi$ 도 isomorphism 이다.

