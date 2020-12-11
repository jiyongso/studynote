IV. Sylow's Theorem and Direct Products
===



## 1. First Sylow's Theorem



#### Lemma 1.1

양의 정수 $n$, prime number $p$ 에 대해 $n=p^{\alpha}m$ 이고 $p^r \mid m$ and $p^{r+1} \nmid  m$ 이면 $p^r \mid \left(\begin{array}{c} p^\alpha m \\p^\alpha\end{array} \right)$  and  $p^{r+1} \nmid \left(\begin{array}{c} p^\alpha m \\p^\alpha\end{array} \right)$ 이다.

---

*(Proof)* (1)  $\left(\begin{array}{c} n \\k\end{array} \right) = \dfrac{n!}{k!(n-k!)}$ 이다. 이것은 $n$ 개의 집합에서 $k$개의 원소를 선택하는 가짓수이다. 그리고 다음이 성립한다.
$$
\left(\begin{array}{c} p^\alpha m \\p^\alpha\end{array} \right) = \dfrac{(p^{\alpha}m)!}{(p^{\alpha})! (p^{\alpha}m-p^{\alpha})!} = \dfrac{p^{\alpha}m (p^{\alpha}m-1)\cdots (p^{\alpha}m - p^\alpha+1)}{p^{\alpha} (p^{\alpha}-1)\cdots (p^{\alpha} - p^\alpha +1)} = m\cdot \left(\prod_{s=0}^{p^\alpha-1}\dfrac{p^\alpha m -s}{p^\alpha-s}\right)
$$
(2) 위 식의 우변에서 $p\nmid s$ 이면 $p\nmid (p^\alpha-s)$ and $p\nmid (p^{\alpha}m-s)$ 이다. $p^\beta |s$ for $\beta \le \alpha$ 이면 $p^\beta \mid (p^\alpha-s)$ and $p^\beta \mid (p^{\alpha}m-s)$ . 따라서 $p^r \mid \left(\begin{array}{c} p^\alpha m \\p^\alpha\end{array} \right)$  and  $p^{r+1} \nmid \left(\begin{array}{c} p^\alpha m \\p^\alpha\end{array} \right)$ 이다.



#### Theorem 1.2 (The 1st Sylow's theorem)

Prime number $p$, group $G$ 에 대해 $p^{\alpha}{\large \mid}|G|$ 이면 $G$ 는 order $p^{\alpha}$ subgroup을 가진다.

---

*(Proof)* Let  $|G|=p^{\alpha}m$ and $\mathcal{M} =\{ S\subset G : |S|=p^{\alpha} \}$. ($\mathcal{M}$ 은 $G$ 의 subset의 collection 이다.) $|\mathcal{M}|=\left(\begin{array}{c} p^\alpha m \\ p^\alpha \end{array}\right)$ 이다. $M_1,\,M_2 \in \mathcal{M}$ 이 어떤 $g\in G$ 에 대해 $M_1 = gM_2$ 이면 $M_1 \sim M_2$ 라 하자. $\sim$ 이 equivalence relation 임은 쉽게 알 수 있다. $p^r \mid m$ 이며 $p^{r+1}\nmid m$ 이라 하자.

(2) $\mathcal{M}$ 을 equivalence classes로 나누면 최소한 한 class의 원소의 갯수는 $p^{r+1}$ 로 나누어 지지 않는다. 모든 equivalence class의 원소의 갯수가 $p^{r+1}$ 로 나누어진다면 $p^{r+1}{\large \mid} |\mathcal{M}|$ 이며 이는 Lemma 1.1에 모순된다. 원소의 갯수가 $p^{r+1}$ 로 나누어지지 않는 equivalence class 를 $\{M_1,\ldots,\,M_n\}$ 이라 하자. 즉 $p^{r+1} \nmid n$ 이다.

(3) Equivalence class 의 정의에 의해 $M_j = g_j M_1$ 인 $g_j\in G$ for all $j = 1,\ldots,\,n$ 가 존재한다. $H=\{g\in G : gM_1 = M_1$} 이라 하면 $H \le G$ 임은 쉽게 보일 수 있다. 

(4) Group action of $G$ on $\{M_1,\ldots,\,M_n$} 을 생각하자. $H$ 는 stabilizer of $M_1$ 이며 $\{M_1,\ldots,\,M_n\}$ 은 orbit of $M_1$ on $G$ 이다. 따라서 counting principle 에 의해 $n|H|=|G|$  이다.

(5) $p^{r+\alpha} {\large \mid} |G|$, $p^{r+\alpha+1}{\large \nmid} |G|$ , $p^{r+1}\nmid n$ 이므로 $p^{\alpha} {\large \mid}|H|$ 이다. 즉 $|H|\ge p^\alpha$

(6) By the definition of $\mathcal{M}$, $|M_1|=p^{\alpha}$ . If $m_1 \in M_1$, $m_1 h \in M_1$ for all $h \in H$. 따라서 $|H|\le |M_1| =p^\alpha$. (5) 와 같이 생각하면 $|H|=p^{\alpha}$. $ \;\;\square$

  

#### Corollary 1.3 

$p^m {\large \mid}|G|$ 이고 $p^{m+1}{\large \nmid} |G|$ 이면 order $p^m$ subgroup of $G$ 가 존재한다.



#### Definition : Sylow $p$-subgroup

Group $G$, prime number $p$ 가 $p^m {\large \mid}|G|$ 이고 $p^{m+1} {\large \nmid} |G|$ 일 때 order $p^m$ subgroup을 **Sylow $p$-subgroup** of $G$ 라 한다. Group $G$ 의 모든 Sylow $p$-subgroups 의 집합을 $\text{Syl}_p (G)$ 라 한다.



#### The second proof of the 1st Sylow's theorem

<b>Outline : </b> Corollary 1.3을 induction을 이용해 먼저 증명한 후 이로부터 1st Sylow's theorem을 증명한다.

<b>1. </b>Prime $p$ 가 $p{\large \mid} |G|$ 이면 $G$ 의 Sylow $p$-subgroup은 항상 존재한다.

---

(1) $|G|=2$ 이면 관계된 prime number는 2 뿐이며 $G$ 자신이 Sylow $p$-subgroup 이다.

(2) $|G|$ 보다 작은 order 에서 위의 명제가 성립한다고 가정하자. 어떤 prime $p$, 양의 정수 $r$ 에 대해 $p^r {\large \mid}|G|$ and $p^{r+1}{\large \nmid}|G|$ 라 하자. 만약 어떤 $G$ 의 proper subgroup $H$ 에 대해 $p^r {\large \mid}|H|$ 이면 induction hypothesis에 의해 $G$ 의 Sylow $p$-subgroup이 존재한다. 

(3) 이제 $G$ 의 어떠한 proper subgroup도 그 order가 $p^r$ 로 나누어 떨어지지 않는다고 가정하자. 아래의 counting theorem을 다시 생각해 보자.
$$
|G| = |Z(G)| + {\textstyle \sum\limits_{a \not\in Z(G)}} \dfrac{|G|}{|N(a)|}\;.
$$
$Z(G)$ 와 $N(a)$ 는 모두 subgroup of $G$ 이므로 $p^r {\large \nmid}|Z(G)|$ and $p^r {\large \nmid} |N(a)|$ 이다. 따라서 $p \left| \left(\dfrac{|G|}{|N(a)|}\right) \right.$ for any $a \in G$ and $a \not\in Z(G)$ 이며,  $p \left| \left(\sum\limits_{a\not\in Z(G)} \dfrac{|G|}{|N(a)|} \right) \right.$ 이다. $p{\large \mid}|G|$ 이므로 $p{\large \mid}|Z(G)|$. 

(4) $p{\large \mid}|Z(G)|$ 이므로 $Z(G)$ 에는 order $p$ elements가 존재한다. 이를 $b$ 라 하고 $B= \langle b\rangle$ 이라 하자. $B\le Z(G)$ 이므로 모든 $g\in G$ 에 대해 $g^{-1}bg = b$ 이다. 따라서 $B\trianglelefteq G$ 이다.  $\overline{G}=G/B$ 라 하면 $|\overline{G}|=|G|/p$ 이므로 $p^{r-1}{\large \mid}|\overline{G}|$ 이고 $p^r {\large \nmid} |\overline{G}|$ 이다. 

(5) 따라서 induction hypothesis에 따라 $\overline{G}$ 는 order $p^{r-1}$ subgroup $\overline{P}$ 가 존재한다. $P=\{ x\in G : xB \in \overline{P}\}$ 라 하면 correspondence theorem에 의해 $P \le G$ 이며 $|P|= |\overline{P}|p=p^r$ 이다. 즉 $P$ 는 Sylow $p$-subgroup of $G$ 이다. $\;\;\square$



<b>2. </b>$|G|=p^r$ 이면 $G$ 는 모든 $p^n$ ($n=1,\ldots,\,r$) order subgroup을 가진다.

---

(1) $r=1$ 이면 자명하다. 모든  $m<n$ 에 대해  $|H|=p^m$ 일 때, 성립한다고 가정한다.

(2) $|Z(G)|=p^k$ for $0 <k \le n$ 이므로 $Z(G)$ 에는 order $p$ elements $a$ 가 존재한다. $\langle a \rangle = N \trianglelefteq G$ 이므로 $G/N$ 을 생각한다. $|G/N|=p^{n-1}$ 이므로 $0\le m \le n-1$ 에 대해 order $p^m$ subgroup이 존재한다. Let $M$ be the order $p^{\beta}$  subgroup of $G/N$.    

(3) $\phi \in \text{Hom}(G,\,G/N)$ defined by $\phi (g) = gN$ 을 생각하자. $M \le G/N$ 이므로 correspondence theorem에 의해 $\phi^{-1}(M) \le G$ 이며 $|\phi^{-1}(M)| = |M||N| = p^{\beta +1}$ 이다. $\;\;\square$





## 2. The third proof of the 1st Sylow's theorem

<b>Outline : </b> (1) 우선 prime number $p$ 에 대해, symmetric group $S_{p^r}$ 가 Sylow $p$-subgroup 을 가짐을 보인다. (2) $G\le M$ 이고 $M$ 이 Sylow $p$-subgroup을 가지면 $G$ 도 Sylow $p$-subgroup을 가짐을 보인다. (3) Cayley theorem 을 이용하여 충분히 큰 $k$ 에서 $S_{p^k}$ 가 $M$ 임을 보인다.



#### Lemma 2.1

 주어진 prime $p$ 와 자연수 $k$ 에 대해 $n(k)$ 를 $p^{n(k)}\mid (p^k)!$ and $p^{n(k)+1} \nmid (p^k)!$ 을 만족하는 정수로 정의한다. 이 때 $n(k) = 1+p+\cdots + p^{k-1}$ 이다.

---

*(Proof)*  $n(1) = 1$ 임은 자명하다.

$$
\begin{align*}
(p^k)! &= p[2p][3p] \cdots [(p-1)p] [p^2][2p^2]\cdots [p^{k-1}]\\
&\times [2p^{k-1}]\cdots [(p^{k-1}-1)p] [p^k=p^{k-1}p] \times [\text{integers not divided by }p] \\
&=[(p^{k-1})!]  \times [2p^{k-1}]\cdots [(p^{k-1}-1)p] [p^k=p^{k-1}p] \times [\text{integers not divided by }p]
\end{align*}
$$
을 생각하면 $n(k)= p^{k-1} + n(k-1)$ 임을 알 수 있다. 따라서 $n(k) = p^{k-1} + p^{k-2} + \cdots + p^1 + n(1)$. $\;\;\square$



#### Lemma 2.2

 $S_{p^k}$ 는 Sylow $p$ subgroup을 가진다.

---

*(Proof)* (1) Induction을 통해 증명한다. $k=1$ 인 경우, $(1,\ldots,\,p) \in S_p$ and the order of $(1,\ldots,\,p)$ 는 $p$ 이므로 성립.

(2) $S_{p^{k-1}}$ 이 Sylow $p$-subgroup 을 가진다고 가정하자. $\{ 1,\,2,\ldots,\,p^k \}$ 를 다음과 같이 분할하자. 
$$
\{1,\,2,\ldots,\,p^{k-1}\},\, \{p^{k-1}+1,\,p^{k-1}+2,\ldots,\,2p^{k-1}\},\ldots,\,\{(p-1)p^{k-1}+1,\ldots,\,p^k\}
$$
 각 부분집합을 $s_1,\,s_2,\ldots,\,s_p$ 라 하면 각 $s_i$ 는 $p^{k-1}$ 개의 원소를 포함한다. 

(3) Let $\sigma \in S_{p^k}$, $\sigma = (1,\,p^{k-1}+1,\,2p^{k-1}+1,\ldots,\,(p-1)p^{k-1}+1) \cdots $$ (j,\,p^{k-1}+j,\,2p^{k-1}+j ,$$\ldots, (p-1)p^{k-1}+j) $$\cdots$ $(p^{k-1},\,2p^{k-1},\ldots,\,p^k)$. Then $\sigma^p=e$. 

(4) Let $\tau \in S_{p^k}$ s.t. do not touch number larger than $p^{k-1}$. Then $\sigma\tau \sigma^{-1}$ touch only elements in $\{p^{k-1}+1, $$p^{k-1}+2,\ldots,\,2p^{k-1}\}$.  더 나아가 $\sigma^j \tau \sigma^{-j}$ touches only elements $\{jp^{k-1}+1,\,jp^{k-1}+2,\ldots,\,(j+1)p^{k-1}\}$. 

(5) Let $A = \{ \tau \in S_{p^k} : \tau (i) = i \text{ if } i > p^{k-1}\}$. Then $A \le S_{p^k}$ and $A \approx S_{p^{k-1}}$. Induction 에 의해 $A$ 는 order $p^{n(k-1)}$ Sylow $p$-subgroup을 가진다. 이를 $P_0$ 라 하자.

(6) Let $T=P_0 (\sigma P_0 \sigma^{-1})(\sigma^{-2} P_0 \sigma^2)\cdots (\sigma^{-(p-1)}P_0 \sigma^{p-1}) = P_0 P_1 \cdots P_{p-1}$ where $P_i = \sigma^{-i}P_0 \sigma^{i}$ 라 하자. 각각의 $P_i$ 는 $P_0$ 와 isomorphic 하므로 $|P_i|=p^{n(k-1)}$ 이다. $P_i \cap P_j = \{e\}$  for $i \ne j$ 이므로 $|T|= (p^{n(k-1)})^p = p^{p \cdot n(k-1)}$ 이다. $p \cdot n(k-1) = n(k)-1 \ne n(k)$ 이므로 $T$ 는 Sylow $p$ subgroup of $S_{p^k}$ 가 아님.    

(7) $\sigma^{i} T \sigma^{-i} = T$ for all $i \in \mathbb{N}$ 임은 쉽게 보일 수 있다. 이제 $P=\{\sigma^{j} t : t\in T,\,0 \le j \le p-1\}$ 라 정의하자. $\sigma \not\in T$ and $\sigma T \sigma^{-1} = T$ 이므로 $P \le S_{p^k}$ 이며 $|P|=p \cdot |T| = p\cdot p^{n(k)-1}=p^{n(k)}$ 임을 알 수 있다. 즉 $P$ is the Sylow $p$ subgroup of $S_{p^k}$. $\;\;\square$



<b>Note on 3rd proof : </b> 1st Sylow's theorem을 증명 했을 뿐만 아니라 Sylow $p$-subgroup을 얻는 한 방법을 제시했다.



#### Definition : Double Coset

$G$가 group 이고 $A,\,B$ 가 subgroup of $G$ 라 하자. $x,\,y \in G$ 가 어떤 $a\in A$, $b\in B$ 에 대해 $x=ayb$ 관계가 있을 때 $x \sim y$ 라 하자. 이 $\sim$ 은 equivalence relation 이다. $x\in G$ 에 대한 equivalence class $AxB = \{axb : a\in A,\,b\in B\}$ 를 **double coset** of $A$ and $B$ in $G$ 라 한다.

<b>Note : </b> $\displaystyle G=\bigcup_{x\in G} AxB$ 이며 $AxB=AyB$ or $(AxB) \cup (AyB)=\varnothing$ for all $x,\,y \in G$ .



#### Lemma 2.3

$\displaystyle |AxB| = \dfrac{|A||B|}{|A \cap xBx^{-1}|}$.

---

*(Proof)* (1) Consider mapping $T: AxB  \to AxBx^{-1}$ defined by $T(axb)= axbx^{-1}$. It is trivial that $T$ is bijection. 따라서 $|AxB|=|AxBx^{-1}|$. 

(2) $xBx^{-1} \le G$ and $|xBx^{-1}|= |B|$. 따라서 $\displaystyle |AxB|= |AxBx^{-1}| = \dfrac{|A||xBx^{-1}|}{|A \cap |xBx^{-1}|} = \dfrac{|A||B|}{|A \cap xBx^{-1}|}$ . $\;\;\square$



 #### Lemma 2.4

$G$ 가 finite group 이고 어떤 finite group $M$ 의 subgroup 이라 하자. $M$ 의 Sylow $p$-subgroup $Q$ 에 대해 $G\cap xQx^{-1}$ for some $x \in M$ 은 Sylow $p$ subgroup of $G$ 이다.

---

*(Proof)* (1) Let $|Q|=p^m$ and $|G|=p^nt$ for $p \nmid t$. $G \le M$ , $Q \le M$ 이므로 $\displaystyle M = \bigcup_{x \in M} G x Q$. By Lemma 2.1, $|GxQ|= |G||Q|/|G \cap xQx^{-1}|$.

(2) $G\cap xQx^{-1} \le xQx^{-1}$ 이므로 $|G \cap xQx^{-1}| = p^{m_x}$ for $m_x \le m$. We will show that $m_x = n$. 

(3) Suppose $m_x \ne n$. Then $m_x<n$. Then $|GxQ|= p^{m+n-m_x}t$. 따라서 $p^{m+1} {\large \mid} |GxQ|$ for all $x\in G$ 이므로 $p^{m+1}{\large \mid} |M|$. $M$ 의 Sylow $p$ subgroup $Q$ 의 order가 $p^m$ 임에 모순. 따라서 $m_x=n$ 이며 $|G\cap xQx^{-1}|=p^n$ 이므로 $G \cap xQx^{-1}$ 은 Sylow $p$-subgroup of $G$. $\;\;\square$

​    

#### Conclusion : 1st Sylow's theorem

---

Caley's theorem 에 의해 임의의 finite group $G$ with $|G|=n$ 은 $S_n$ 의 어떤 subgroup과 isomorphic 하다. $n<p^k$ 인 $k$ 를 선택하자. $S_{p_k}$ 는 Sylow $p$-subgroup을 가지며 $S_n \le S_{p_k}$ 이므로 $S_n$ 도 Sylow $p$ subgroup을 가지며 $G$ 도 Sylow $p$ subgroup을 가진다.



## 3. The 2nd and 3rd Sylow's theorem



#### Theorem 3.1 (Second Sylow's theorem)

$P_1,\, P_2 \in \text{Syl}_p (G)$ 이면 $P_1 = gP_2g^{-1}$ for some $g \in G$.

---

*(Proof)* (1) Let $P_1,\,P_2$ are distinct Sylow $p$-subgroup of $G$ and $|P_1|= |P_2|= p^m$.  Then $G=\bigcup_{x\in G}P_1 x P_2$ and $|P_1 xP_2| = |P_1||P_2|/|P_1 \cap xP_2x^{-1}| = p^{2m-n_x}$ for $n_x$ satisfying $|P_1 \cap xP_2 x|=p^{n_x} $. 

(2) If $xP_2x^{-1} \ne P_1$ for all $x \in G$, $n_x<m$ for all $x \in G$ .  $p^{m+1}{\large \mid} |P_1 xP_2|$ for every $x\in G$, and therefore $p^{m+1}{\large \mid} |G|$ , which is an contradiction. $\;\;\square$



#### Corollary 3.2

$|\text{Syl}_p (G)| = |G|/|N(P)|$  for $P$ is any Sylow $p$-subgroup of $G$.

---

Consider $N(H) = \{ x\in G : xHx^{-1} = H\}$. 



#### Theorem 3.2 (Third Sylow's theorem) 

$|\text{Syl}_p (G)| = 1 + kp$ for some $k \in \mathbb{N}$. 

---

*(Proof)* (1) Let $P \in \text{Syl}_p (G)$ with $|P|=p^n$ and consider $G= \bigcup PxP$. Then $|PxP|=|P|^2 /|P\cap xPx^{-1}|$.  

(2) If $xPx^{-1}=P$, $|PxP|=p^n$. Otherwise, $|PxP|=p^{n+m}$ for some $m > 0$.  

(3) $|G|=\sum\limits_{x \in N(P)} |PxP| + \sum\limits_{x \not\in N(P)} |PxP|$ and we can find that $|G|=|N(P)|+p^{n+1}t$ for some $t \in \mathbb{Z}_{+}$. $ | N(p)|{\large \mid} |G|$, $|N(P)| {\large \mid} p^{n+1}t$, and $p^{n+1}{\large \nmid} |N(P)|$ 이므로 $|G|/|N(P)| = |\text{Syl}_p (G)|= 1+ pk$. $\;\;\square$





#### Problems (p. 102 ~ 103)

 <b>2. </b> $x$ 가 양의 실수일 때 $[x]$ 를 $m\le x < m+1$ 인 정수 $m$ 으로 정의하자. $p$ 가 prime number 일 때 $p^l | n!$ 인 $l$ 은 다음 식으로 주어짐을 보이시오
$$
l=\left[ \dfrac{n}{p}\right] + \left[ \dfrac{n}{p^2}\right] + \cdots \left[ \dfrac{n}{p^r}\right] + \cdots
$$

---

(1) $\displaystyle \left[ \frac{n}{p^r} \right]$= number of positive integers less then or equal to p^r which are divisible by $p^r$.  



<b>3. </b> $S_{p^k}$ 의 Sylow $p$-subgroup을 구성하는 방법을 사용하여 $S_8$ 과 $S_9$ 의 generator를 구하시오

---

$S_8$ case

(1) $S_8=S_{2^3}$. $A =\{\tau \in S_8 : \tau (i) = i \text{ if } i>4 \} \approx S_{4}$ and $\sigma = (1, 5)(2, 6) (3, 7)(4, 8)$. $n(2)=1+2=3$. 

(2) $A$ has a subgroup of $2^3=8$, $P_0 = \{ e,\,(1,\,2,\,3,\,4), (1,\,3),\,(1,\,3)(2,\,4),\,(1,\,4,\,3,\,2),\, (2,\,4),\,(1,\,4)(2,\,3),$$\,(1,\,2)(3,\,4)\} = \langle (1,\,2,\,3,\,4),\,(1,\,3)\rangle$. $T= \langle (1,\,2,\,3,\,4),\,(1,\,3)\rangle\langle (5,\,6,\,7,\,8),\,(5,\,7)\rangle$. and $|T|=2^{2*3}= 2^6$.

(3) $P = \{\sigma^j t : t\in T,\, 0 \le j \le p-1\}$ is a Sylow $p$-subgroup of $S_8$. 

$S_9$ case

(1) $S_9 = S_{3^2}$. $A= \{ \tau \in S_9 : \tau(i) = i \text{ if } i > 3\} \approx S_3$ and $\sigma = (1, 4, 7)(2, 5, 8)(3, 6, 9)$. $n(1) = 1$       



<b>6. </b> Group $G$에서 $|G|=3^2 5^2$ 일 때, $3$-Sylow subgroups 와 $5$-Sylow subgroups 는 normal to $G$ 임을 보이시오.

---

(1) $|\operatorname{Syl}_5 (G)|=1+5m$. The only possible $m$ is $0$ and there is only one Sylow $5$-subgroup of $G$. Let it $M$. 

(2) $|\operatorname{Syl}_3 (G)|=1+3k$. $(1+3k)\mid 25$ for $k=0$ and $8$. If $|\operatorname{Syl}_3 (G)|=1$, It is normal to $G$. 



<b>7. </b> $G$가 order 30 group 이다.

(a) $G$의 어떤 Sylow 3-subgroup와  어떤 Sylow 5-subgroup 는 normal to $G$ 임을 보이시오.

(b) (a) 로 부터 모든 $G$의 Sylow 3-subgroups와 Sylow 5-subgroups는 normal to $G$ 임을 보이시오.

(c) $G$가 order 15 normal subgroup을 가짐을 보이시오.

(d) (c)를 이용하여 $G$를 classify 하시오.

(e) Order 30 group중에 가능한 different nonisomorphic group은 몇가지인가?

---

(a) $30=2\cdot 3 \cdot 5$. $(1+3k)\mid 30$ for $k=0,\,3$ and $(1+5k)\mid 30$ for $k=0,\, 1$. Nontrivial 한 경우만 생각하자. $|\operatorname{Syl}_3(G)|=10$ 이라면 $G$는 최소한 20개의 order $3$ elements를 가진다. 게다가 order 2, order 5 elements를 가지므로 이것만 고려해도 $G$는 최소한 $2 \times 5 \times 20=200$ 개의 elements를 가져야 하므로 모순.

$|\operatorname{Syl}_5(G)|=6$ 이라 가정하면 $G$는 최소한 30개의 order 5 elements를 가져야 하므로 모순.

(b) (a)로부터 $|\operatorname{Syl}_3 (G)|=|\operatorname{Syl}_5 (G)|=1$ 

(c) $G$의 order 15 subgroup 이 있다면 $30=2\times 15$ 이므로 normal to $G$ 이다. $A$, $B$를 각각 order 3, 5 group of $G$ 라 하자. $AB=\{ab : a\in A,\, b\in B\}$ 라 하자. $a_1b_1 a_2b_2 = a_1 b_1 a_2 {b_1}^{-1}b_1 b_2 = a_1 (a_2)' b'\in AB$ 이며 $(ab)^{-1}= b^{-1}a^{-1}=b^{-1}a^{-1}bb^{-1}\in AB$ 이므로 $AB \le G$ 이다.

(d) 



<b>8. </b> $|G|=231$ 일 때 Sylow 11-subgroup은 $Z(G)$에 포함됨을 보이시오.

---

(1) $|G|=231=3 \cdot 7 \cdot 11$. $(1+11k)\mid 231$ 을 만족하는 $k$는 0 뿐이다. 따라서 $\operatorname{Syl}_{11}(G)$는 유일하다.

(2) $a\in G$, $a\not \in P\in \operatorname{Syl}_{11}(G)$ 라 하자. $x\in P$ 에 대해 $axa^{-1}=x^k$ 이며 $\mathcal{o}(a)=m$은 3 or 7 이다. 

$a^m xa^{-m}= x = x^{k^m}$ 이며 $k^m \equiv k \;(\operatorname{mod}\;m)$ 이므로 $k=1$ 이다. $ax=xa$ for all $a\in G, x\in P$ 이므로 $P\le Z(G)$ 이다. 



<b>9. </b> $|G|=385$ 일 때 Sylow 11-subgroup of $G$는 normal to $G$ 이며 Sylow 7-subgroup of $G$는 $Z(G)$에 포함됨을 보이시오.

---

(1) $|G|=385=5 \cdot 7 \cdot 11$. $(1+11k)\mid 385$ 를 만족하는 $k$ 는 0 뿐이므로 Sylow 11-Subgroup of $G$는 유일하다. 따라서 normal to $G$

(2) $(1+7m)\mid 385$를 만족하는 $m$은 $0$ 뿐이다. 따라서 normal to $G$. $a$가 order 5 elements 이고 $m$이 Sylow 7-subgroup $M$ 의 elements라 하자. $ama^{-1}=m^k$ for some $k\in \N$ 이며 $a^5ma^5=m=m^{k^5}$ 이며 $k^5 \equiv k \;(\operatorname{mod}\; 5)$ 이므로 $k=1$ 이다. $b$가 order 11 elements 라면 Sylow 11-subgroup $N$ 에 포함되며 $N\trianglelefteq G$ 이다. $MN =\{ mn : m\in N,\, n \in M\}$ 일 때 $NM\trianglelefteq G$ 임은 쉽게 보일 수 있다. $M\cap N = \{e\}$ 이다.

$mnm^{-1}n^{-1} =(mnm^{-1})n^{-1} \in N$ 이며 $mnm^{-1}n^{-1}=m(nm^{-1}n^{-1})\in M$ 이다. 따라서 $mnm^{-1}n^{-1}=e$ 이므로 $mn=nm$ 이다. 즉 $M \le Z(G)$ 이다.



<b>10. </b> $|G|=108$ 이면 $G$는 order $3^k$ where $k\ge 2$ 인 normal subgroup을 가짐을 보이시오.

---

(1) $|G|=108=2^2 \cdot 3^3$. $(1+3k)\mid 108$을 만족하는 $k=0,\,1$. $k=0$ 이면 $G$는 $3^3$ order normal subgroup을 가진다.

(2) $|\operatorname{Syl}_3 (G)|=4$ 이므로 $\operatorname{Syl}_3(G)=\{P_1,\,P_2,\,P_3,\,P_4\}$ 라 하자. 각각의 $P_i$는  2nd Sylow theorem 에 의해  normal subgroup 이 아니다.  $[G:P_i]=4$ 이며 $|G|=108$ 인데 $108 \not\mid 4!$ 이므로 $P_i$는 nontrivial normal subgroup of $G$를 포함한다. 한 $P_i$라도 order 9 normal subgroup을 가지면 O.K. 

(3) 이제 $P_i$의 non trivial normal subgroup of $G$는 order $3$ 뿐임을 가정하고 이 subgroup을 $N_i$ 라 하자. 어떤 $N_i \ne N_j$ 이면 $N_i \cap N_j =\{e\}$ 이므로 $N_iN_j \trianglelefteq G$ 이며 $|N_iN_j|=9$ 이다. 이제 $P_i\cap P_j = N$ for all $i,\,j$ and $|N|=3$ 인 경우만 고려하면 된다. $\operatorname{Syl}_3(G)$에 포함되는 모든 원소의 갯수는 $(27-3)\times 4+3=99$. 거기에 order $2^k$에 포함되는 원소의 갯수는 $4$ 이므로 최소한 $|G|\ge 99\times 4=396$ 이어야 하는데 이는 $|G|=108$ 임에 모순.



<b>11. </b> $|G|=pq$ and $p<q$ 이며 $p,\,q$는 prime 이다.

(a) $p \not\mid (q-1)$ 이면 $G$는 cyclic 임을 보이시오.

(b) $p\mid (q-1)$ 이면 $G$는 non-abelian group of order $pq$ 일 수 있으며 이 경우 $G$가  unique 함을 보이시오.

---

(a) $(1+kp)|pq$ 를 만족하는 $k$는 $0$, $(1+mq)|pq$를 만족하는 $m$도 $0$ 뿐이다. 즉 $|\operatorname{Syl}_p(G)|=|\operatorname{Syl}_q(G)|=1$ 이다. $G$의 order $p$ subgroup을 $P$, order $q$ subgroup을 $Q$ 라 하면 $G=PQ$ 이며 $P \cap Q=\{e\}$ 이므로 $G$는 cyclic 이다.

(b) 조건에 의해 $|\operatorname{Syl}_q(G)|=1$ 이며 $|\operatorname{Syl}_p (G)| >1$ 이다. Let $Q$ be the Sylow $q$-subgroup. Let $P_1,\,P_2 \in \operatorname{Syl}_p (G)$. Then $\exists g\in G$ s.t. $P_2 =xP_1 x^{-1}$. $P_1 \cap P_2 =\{e\}$ 이므로 $G$는 non abelian group 이다.

(c) --proof of uniqueness will be done--



<b>12. </b> $|G|=pqr$ with $p<q<r$ and $p,\,q,\,r$ are prime numbers.

(a) $G$의 Sylow $r$-subgroup은 normal to $G$ 임을 보이시오.

(b) $G$는 order $qr$ normal subgroup을 가짐을 보이시오.

(c) $q \not\mid (r-1)$ 이면 Sylow $q$-subgroup은 normal to $G$ 임을 보이시오.

---

(a) $|\operatorname{Syl}_r (G)|=1+kr$ and $(1+kr)\mid pqr$. 가능한 $k=0$ 뿐이므로  $G$의 Sylow $r$-subgroup은 normal to $G$

(b) Let $R$ be the Sylow $r$-subgroup and $Q$ be a Sylow $q$-subgroup. $R \trianglelefteq G$ 이므로 $G/R$ is a order $pq$ group and it has order $q$ subgroup $Q'$. $Q' \trianglelefteq G/R$ 임은 자명하다. $\phi \in \operatorname{Hom}(G,\,G/R)$ defined by $\phi (x)=xR$ 을 생각하면 $\phi^{-1}(Q')$ 은 normal subgroup of $G$ 이다. $|Q'|=q$ 이므로  $Q'$은 cyclic group 이며 따라서 $Q=\phi^{-1}(Q')$ 은 order $qr$ normal subgroup of $G$ 이다.

(c) $|\operatorname{Syl}_q (G)| = 1+mq$ 이며 $(1+mq)|pqr$ 이다. For $m>0$ 에 대해 $(1+mq)\not\mid p$, $(1+mq)\not \mid q$ 임은 자명하다. $q\not\mid (r-1)$ 이므로 $(1+mq)\not\mid r$ for $m>0$. 따라서 $|\operatorname{Syl}_q(G)|=1$. 



<b>13. </b> $|G|=p^2q$ 이고 $p,\,q$가 prime 이면 $G$가 nontrivial normal subgroup을 가짐을 보이시오.

---

(1) $p>q$ 이면 $(1+kp)\mid q$ 는 $k=0$ 일 때 뿐이므로 $G$의 유일한 Sylow $p$ subgroup이 normal to $G$ 이다.

(2) $q > p$ 이면 $(1+mq)\mid p^2$ 는  $1+mq =p^2$ 이거나 $m=0$ 일 때 뿐이다. $m=0$ 이면 $G$의 Sylow $q$-subgroup은 유일하며 normal to $G$ 이다. $1+mq=p^2$ 라 하자. $mq=p^2-1=(p-1)(p+1)$ 이며 $q>p$ 이므로 $q=p+1$ 일 때 뿐이다. 이때는 $p=2,\,q=3$ 이며 $(1+2k)\mid 3$ for $k=0,\,1$ 이므로 $|\operatorname{Syl}_2 (G)|=3$ and $|\operatorname{Syl}_3 (G)|=4$ 이고 $|G|=12$ 이다. $P\in \operatorname{Syl}_2 (G)$ 이면 $[G:P]=6$ 이므로 $|G| {\large \not\mid}[G:P]!$ 이다. 따라서 $P$는 nontrivial normal subgroup of $G$를 포함하는데 $|P|=2$ 이므로 이는 자기 자신일 수 밖에 없다.



<b>14. </b> $|G|=p^2q$ 이고 $p,\,q$가 prime 이면 Sylow $p$-subgroup 혹은  $q$- subgroup은 normal to $G$ 이다.

---

Problem 13에서 다 보였다. 



<b>15. </b> $G$가 모든 $a,\,b\in G$  와 어떤 prime $p$ which divide $|G|$ 에 대해 $(ab)^p=a^pb^p$ 라 하자.

(a) $G$의 Sylow $p$-subgroup은 normal to $G$ 이다.

(b) $P$가 Sylow $p$-subgroup 이면 어떤 normal subgroup of $G$인 $N$ 이 존재하여 $P \cap N =\{e\}$ 이며 $G=PN$ 이다.

(c) $G$는 nontrivial center 를 가진다.

---

(a) 우선 $(ab)^p=a^pb^p$ 이면 $(ab)^{p^m}=a^{p^m}b^{p^m}$ for positive integer $m$ 임을 보이자. 모든 $n<m$ 인 자연수 $n$에 대해 $(ab)^{p^n}=a^{p^n}b^{p^n}$ 임을 가정하자.
$$
(ab)^{p^m}=\left[(ab)^{p^{m-1}}\right]^p=\left[a^{p^{m-1}}b^{p^{m-1}}\right]^p = a^{p^m}b^{p^m}\;.
$$
$p^r {\large \mid}|G|$ 이며 $p^{r+1}{\large \not\mid }|G|$ 라 하자. $S=\{x\in G : x^{p^m}=e,\,\text{for some}\; m\in \mathbb{Z_+}\}$ 라 정의한다. $S\trianglelefteq G$ 임은 Herstein problem 2.6.20에서 증명했다. $S$는 모든 $p^m$ type order elements of $G$를 모은 것이며 $S\le G$ 이므로 $p^r{\large \mid}|S|$ 이고 $p^{r+1}{\large \not \mid }|S|$ 이다. 따라서 $S$ 는 Sylow $p$-subgroup of $G$ 이며 normal to $G$ 이다.

(b) Let $|G|=p^r m$ with $p \nmid m$. $\gcd (p,\,m)=1$ 이므로 Euler's $\phi$ function을 생각하면 $p^{\phi(m)}\equiv 1 \; (\operatorname{mod}\;m)$ 이며 임의의 양의 정수 $k$ 에 대해서도 $p^{k\phi (m)}\equiv 1 \;(\operatorname{mod}\; m)$ 이다. $s>r$ 이며 $p^s \equiv 1 (\operatorname{mod}\;m)$ 인 $s$를 선택하자. 

Consider a map $\psi : G \to G$ defined by $\psi(x)=x^{p^s}$. From (a), $\psi \in \operatorname{Hom}(G,\,G)$ and $P=\ker \psi$. Let $N = \operatorname{Im}(\psi)=\{\psi(x) : x\in G\}$. $e\in N$ 이며 $n_1,\,n_2 \in N$ 이면 $n_1 = (x_1)^{p^s},\, n_2 = (x_2)^{p^s}$ for some $x_1,\,x_2\in G$ 이고 $n_1n_2 = (x_1x_2)^{p^s}$ 이므로 $N$ 은 closed under operation 이며 $n\in N$ 이면 $n^{-1}\in N$ 임을 알고 있다. 따라서 $N\le G$ 이다. $n\in N,\, g\in g$ 일 때 $n=(x)^{p^s}$ for some $x\in S$ 이며 $gng^{-1}=(gxg)^{p^s}\in N$ 이므로 $N \trianglelefteq G$ 이다. 

$N \cap P=\{e\}$ 임은 자명하다. $N\approx G/P$ 이므로 $|G|=|N|\cdot |P|$ 이며 $NP\le G$ 이므로 $G=NP$ 이다. 

(c) $G=PN$ 이라 하자. $pnp^{-1}n^{-1}=pnp^{-1}n^{-1}=n'n^{-1}\in N$ 이며 $pnp^{-1}n^{-1}=p(np^{-1}n^{-1})=pp'\in P$ 이므로 $pnp^{-1}n^{-1}=e$ 이다. 즉 $pn=np$ 이다. $P$ 가 $p^r$ order를 가지므로 $Z(P)$ 는 nontrivial 이며 $Z(P)=Z(G)$ 임은 자명하다. 따라서 $G$는 nontrivial center를 가진다. 



<b>16. </b> $G$가 finite group 이고 Sylow $p$-subgroup of $G$가 $Z(G)$ 에 포함된다면 어떤 normal subgroup $N$ of $G$ 가 존재하여 $P \cap N=\{e\}$ 이며  $PN=G$ 임을 보이시오.

---

(1) Let $P \in \operatorname{Syl}_p (G)$. If $P \subset Z(G)$, $xPx^{-1}=P$ for all $x\in G$. 따라서 $P \trianglelefteq G$ 이며 $|\operatorname{Syl}_p (G)|=1$ 이다. 

(2) Let $|G|=p^rm$ for prime $p$. Then $|P|=p^r$. Problem 15 (b)의 증명과정에서 에서 보였듯이. $\gcd (p,\,m)=1$  이므로 $p^s \equiv 1 \;(\operatorname{mod}\;m)$ 인 $s>r$ 이 존재한다. $\psi :G \to G$ defined by $\psi (x) = x^{p^s}$, $N=\operatorname{Im}(\psi)$ 라 하면 $N \trianglelefteq G$, $P \cap N = \{e\}$ 이며 $\ker \psi = P$ 이므로 $N \approx G/P$ 이다. $NP \le G$ 이므로 $G=NP=PN$ 이다.



<b>17. </b> $H \le G$ 일 때 $N(H)=\{x\in G : xHx^{-1}=H\}$ 를 생각하자. $P\in \operatorname{Syl}_p (G)$ 이면 $N(N(P))=N(P)$ 임을 보이시오.

---

(1) $P \trianglelefteq N(P)$ 이므로 $P$는 unique Sylow $p$-subgroup of $N(P)$ 이다. 

(2) $x\in N(N(P))$ 이면 $xN(P)x^{-1} = N(P)$ 이다. $P \ne N(P)$ 이므로 $xPx^{-1}\le N(P)$ 이며 $P$가 unique Sylow $p$-subgroup of $N(P)$ 이므로 $xPx^{-1}=P$ 이다. 즉 $x\in N(P)$ 이므로 $N(N(P))\le N(P)$ 이다.

(3) $N(P)\le N(N(P))$ by definition of normalizer 이므로 $N(P)=N(N(P))$ 이다.



<b>18. </b> $P$가 group $G$의 Sylow $p$-subgroup 이며 $a,\,b \in Z(P)$ 라 하자. $a=xbx^{-1}$ for some $x\in G$ 일 때 $\exists y\in N(P)$ s.t. $a=yby^{-1}$ 임을 보이시오.

---

(1) For every $ g \in P$, $ga=ag$ and $gb=bg$. 따라서 $P \le N(a)$ and $P\le N(b)$.

(2) $xPx^{-1} \le xN(b)x^{-1}=N(xbx^{-1})=N(a)$. 따라서  모든 Sylow $p$-subgroup은 $N(a)$의 subgroup 이고 $N(b)$ 의 subgroup 이다. $N(a)\le G$ 이므로 모든 Sylow $p$-subgroup of $G$는 $N(a)$의 subgroup 이다. 

(3) 따라서 $P=z(xPx^{-1})z^{-1}$을 만족하는 $z\in N(a)$가 존재한다. $P=(zx)P(zx)^{-1}$ 이므로 $zx\in N(P)$ 이다. 

$(zx)b(zx)^{-1}=z(xbx^{-1})z^{-1}=zaz^{-1}=a$ 이므로 $y=zx$. 



<b>19. </b> $G$가 finite group 이고 $\phi \in \operatorname{Aut}(G)$ s.t. $\phi^3 = I$. 또한 $\phi (x)=x \implies x=e$ 라 하자. 이 경우 모든 prime $p$ s.t. $p {\large \mid}|G|$ 에 대해 Sylow $p$-subgroup은 normal to $G$ 임을 보이시오.

---

---to be done--





## 4. Direct Products



#### Definition : External direct product of groups

$A,\,B$가 group 일 때 $A\times B=\{ (a,\,b) : a\in A,\, b\in B\}$ 를 생각하자. $A \times B$에서의 연산을 
$$
(a_1,\,b_1)(a_2,\,b_2)= (a_1a_2,\,b_1b_2)
$$

와 같이 정의하면 $A\times B$의 unit elements는 $(1_A,\,1_B)$ 이며 $(a,\,b)^{-1}=(a^{-1},\,b^{-1})$ 인 group임을 쉽게 알 수 있다.   이것은 임의의 수의 groups로 확장 될 수 있으며 이렇게 주어진 groups로 새로운 group을 만드는 것을 **external direct product** 라 한다.



#### Lemma 4.1

$\overline{A}=\{(a,\,1_B) : a\in A\}$ where $e_B$ is a unit element of $B$ 라 하면 $\overline{A} \trianglelefteq A\times B$ 이며 $\overline{A} \approx A$ 이다. 

----

*proof is trivial*



#### Theorem 4.2

Group $A,\,B$ 에 대해 $\overline{A}=\{ (a,\,1_B): a\in A\}$ 와 $\overline{B}=\{(1_A,\,b): b\in B\}$ 를 생각 하자. $G=A \times B$ 라 하면  $G=\overline{A}\overline{B}$ 이다.

----

*(proof)*  $\overline{A}\trianglelefteq G$, $\overline{B}\trianglelefteq G$, and $\overline{A} \cap \overline{B} = e_G=(1_A,\,1_B)$ . 이 대 $\overline{A}\overline{B} \le G$ 이며 $|\overline{A}||\overline{B}|=|G|$ 이므로 $G=\overline{A}\overline{B}$. $\square$ 



#### corollary 4.3

모든 $g\in G$ 에 대해 어떤 $\overline{a}\in \overline{A}$, $\overline{b}\in \overline{B}$ 가 존재하여 $g=\overline{a}\overline{b}$ 이다.

---



#### Definition : Internal direct product

$G$가 group 이고 $N_1,\ldots,\,N_m$ 이 각각 normal to $G$ 이며 다음을 만족한다고 하자.

1. $G=N_1\cdots N_m$.
2. $g\in G$ 이면 $g=n_1\cdots n_m$ for $n_i \in N_i$ 로 unique 하게 결정된다.

이 때 $G$를 **internal direct product** of $N_1,\ldots,\,N_m$ 이라 한다.



#### Lemma 4.4

$G$ 가 internal direct product of $N_1,\ldots,\,N_m$ 이면 각각의 $i\ne j$ 에 대해 $N_i \cap N_j = \{e\}$ 이며 $a\in N_i,\,b \in N_j$ 에 대해 $ab=ba$ 이다.

---

*(proof)* (1) $x\in N_i \cap N_j$ 이면 $x=e_1\cdots e_{i-1}xe_{i+1}\cdots e_m$ and $x=e_1 \cdots e_{j-1}x e_{j+1}\cdots e_m$ where $e_k$ is the unit element of $N_k$. By definition of internal direct product, $x=e_i=e_j$. 따라서 $N_i \cap N_j =\{e\}$ for $i\ne j$.

(2) Let $a\in N_i,\,b\in N_j$ and $i\ne j$. $aba^{-1}b^{-1}=(aba^{-1})b^{-1}\in N_j$ and $aba^{-1}b^{-1}=a(ba^{-1}b^{-1})\in N_i$. 

$aba^{-1}b^{-1}\in N_i \cap N_j$ 이므로 $aba^{-1}b^{-1}=e$ 이며 따라서 $ab=ba$ $\qquad \square$



<b>Note : </b> $K_1,\ldots,\,K_m$ 이 각각 normal subgroup of $G$ 이고 $G=K_1 \cdots K_m$ 이며 for each $i \ne j$ 에 대해 $K_i \cap K_j = \{e\}$  이더라도 $G$ 가 internal product of $K_1,\ldots,\,K_m$ 일 수 있다. 이것은 problem 8, 9 를 참고하라. 



#### Theorem 4.5

$G$가 internal direct product of $N_1,\ldots,\,N_m$ 이며 $G'=N_1 \times \cdots \times N_m$ 일 때 $G \approx G'$ 이다.

----

*(proof)* (1) Define a map $\phi : G' \to G$ by $\phi(n_1,\ldots,\,n_m) = n_1 \cdots n_m$ where $n_i \in N_i$. It is clear that $\phi$ is surjective. It is also clear that $\phi$ is injective since $G$ is the internal product of $N_1,\ldots,\,N_m$. 

(2) 이제 $\phi \in \operatorname{Hom}(G',\,G)$ 를 보이면 된다. $n_i,\,n'_i \in N_i$ for $i=1,\ldots,\,m$ 이라 하자.
$$
\begin{align*}
\phi((n_1,\ldots,\,n_m)(n'_1,\ldots,,n'_m)) &= \phi(n_1n_1',\ldots,n_m n_m')\\
&= n_1n_1'\cdots n_mn_m'\\
&=n_1m_mn_1'\cdots n'_m \qquad\qquad\qquad & \text{; From lemma 4.4}\\
&=n_1\cdots n_m n'_1 \cdots n'_m \\
&=\phi(n_1,\ldots,\,n_m)\phi(n_1',\ldots,\,n'_m)

\end{align*}
$$


따라서 $G \approx G'$. $\qquad\square$



#### Direct product of group

$G \approx G_1 \times \cdots \times G_m$ 이면 $G$ 는  $\overline{G}_1,\ldots,\,\overline{G}_m$ 의 internal direct product 이며 $G_i \approx \overline{G}_i$ 이 때 $G$를 **direct product** of $G_i$ (or $\overline{G}_i$) 라 한다. 



#### Problem (p. 108 ~ 109)

<b>1. </b> $A,\,B$ 가 group 일 때 $A \times B \approx B \times A$ 임을 보이시오.

---

Define $\phi (a,\,b)=(b,\,a)$. Then,

$$
\phi((a_1,\,b_1)(a_2,\,b_2)) = \phi (a_1a_2,\,b_1b_2)= (b_1b_2,\,a_1a_2)=(b_1,\,a_1)(b_2,\,a_2)=\phi(a_1,\,b_1)\phi(a_2,\,b_2)
$$

It is easy to show that $\phi$ is a bijection.



<b>2. </b> $G_1,\,G_2,\,G_3$ 가 groups 일 때 $(G_1 \times G_2)\times G_3 \approx G_1 \times G_2 \times G_3$ 임을 보이시오. 이것을 일반화 할 수 있는가?

---

Define $\phi : (G_1\times G_2)\times G_3 \to G_1 \times G_2 \times G_3$ by $\phi ((g_1,\,g_2),\,g_3)=(g_1,\,g_2,\,g_3)$. It is easy to show that $\phi $ is bijective and it is also easy to show that $\phi$ is an homomorphism. 



<b>3. </b> $T=G_1 \times \cdots \times G_m$  일 때 $\phi_i \in \operatorname{Hom}(T,\,G_i)$ for all $i=1,\ldots,\,m$ 이 존재함을 보이시오. 이 때 $\ker \phi_i$ 를 구하시오.

---

Define a map $\phi_i: T \to G_i$ by $\phi_i (g_1,\ldots,\,g_i,\ldots,\,g_m)=g_i$. Then,
$$
\begin{align*}
\phi_i((g_1,\ldots,\,g_i,\,\ldots,\,g_m)(g'_1,\ldots,\,g'_i,\ldots,\,g'_m)) &= \phi_i (g_1g'_1,\ldots,\,g_ig'_i,\ldots,\,g_mg'_m)\\
&= g_ig'_i \\
&=\phi_i(g_1,\ldots,\,g_i,\ldots,\,g_m)\phi_i (g'_1,\ldots,\,g'_i,\,\ldots,\,g'_m)\;.

\end{align*}
$$
Then $\ker \phi_i = G_1 \times \cdots \times G_{i-1} \times \{e\}\times G_{i+1}\times \cdots \times G_m$



<b>4. </b>  $G$가 group 이며 $T=G\times G$ 라 하자.

(a) $D=\{(g,\,g) \in G \times G: g\in G\}$ 는 $G$와 isomorphic 한 group 임을 보이시오.

(b) 다음을 증명하시오. : $D \trianglelefteq T \iff G$ is abelian. 

---

(a) Define a map $\phi : G \to T$ by $\phi (g) = (g,\,g)$. Then $\operatorname{Im}(\phi)=D$. It is easy to show that $\phi \in \operatorname{Hom}(G,\,T)$ and $\phi$ is injective. 따라서 $D \approx G$.

(b) Suppose $G$ is abelian. Then $(a,\,b)(g,\,g)(a^{-1}b^{-1})=(g,\,g)\in D$. $D \trianglelefteq T$. 

Suppose $D \trianglelefteq T$.  For any $(a,\,b)\in T$, $(a,\,b)(g,\,g)(a^{-1},\,b^{-1}) = (g',\,g')\in D$. $aga^{-1}=bgb^{-1}$ for any $a,\,b \in G$. Let $a=e$ then, $g=bgb^{-1}\implies bg=bg$ for any $b,\,g\in G$. 따라서 $G$ is abelian.



<b>5. </b> $G$가 finite abelian group 이면 $G$는 isomorphic to the direct product of $G$'s Sylow subgroups 임을 보이시오.

---

(1) $G$가 abelian 이므로 $p{\large\mid}|G|$ 인 모든 prime $p$ 에 대해  $G$의 Sylow $p$ subgroup은 유일하며 normal to $G$ 이다. 이 prime numbers를 $p_1,\ldots,\,p_m$ 이라 하고 이에 대한 Sylow $p_i$-subgroup을 $P_1,\ldots,\,P_m$ 이라 하면 $P_i \trianglelefteq G$ 이며 $P_i \cap P_j =\{e\}$ 임은 자명하다. 

(2) Define a map $\phi : P_1 \times \cdots \times P_m \to G$ defined by $\phi (x_1,\ldots,\,x_m)=x_1\cdots x_m$. It is easy to show that for any $X,\,Y \in P_1 \times \cdots \times P_m$, $\phi (XY)=\phi (X)\phi (Y)$. Therefore $\phi$ is an homomorphism.

$|P_1 \times \cdots \times P_m|=G$ 임은 자명하다. $\ker \phi =\{e\}$ 이므로 $G \approx P_1 \times \cdots \times P_m$ 



<b>6.</b> $A,\,B$ 가 각각 order $m,\,n$ cyclic group 일 때 다음을 보이시오.
$$
A \times B \text{ is cyclic} \iff \gcd (m,\,n)=1\;.
$$

---

(1) $A=\langle a\rangle$, $B=\langle b\rangle$ 이라 하자. 

(2) Suppose $\gcd (m,\,n)=1$. Then, $(a,\,b)^k=e$ 를 만족하는 최소의 $k=mn$ 이므로 $A\times B=\langle(a,\,b)\rangle$ 이며 cyclic. 

(3) Suppose $\gcd (m,\,n)=l\ne 1$. Then, $(a,\,b)^k=e$를 만족하는 최소의 $k =l$ 이며 $|A \times B|=mn$ 이지만 $|\langle (a^r,\,b^s)\rangle|=l$ for any $r$ and $s$ 이므로 $A \times B$는 cyclic 이 아니다.



<b>7. </b> Problem 6의 결과를 이용하여 중국인 나머지 정리를 증명한다. 즉 $m,\,n$ 이 relatively prime integer 이고 $u,\,v$가 임의의 정수일 때 $x\equiv u\; (\operatorname{mod}\; m)$ and $x\equiv v\;(\operatorname{mod}\; n)$ 인 $x\in \N$이 존재함을 보이시오.

---

(1) $\mathbb{Z}_m^{+}$ 과 $\mathbb{Z}_n^{+}$ 를 생각하면 $\mathbb{Z}_m^+ \times \mathbb{Z}_m^{+}$ 는 problem 6에 의하면 cyclic 이므로 성립한다.



<b>8. </b> $N_1,\ldots,\,N_m$ 이 각각 normal subgroup of $G$ 이며 $G=N_1\cdots N_m$ 이고 $N_i \cap N_j =\{1\}$ for every $i\ne j$  이더라도 $G$가 internal direct product of $N_1,\ldots,\,N_m$ 이 아닌 예를 드시오.

---

Consider Klein 4 group $F=\{1,\,a,\,b,\,ab\}$ which satisfying $a^2=b^2=1$ and $ab=ba$. Let $N_1=(1,\,a)$, $N_2=(1,\,b)$, $N_3=(1,\,ab)$. Then each $N_i \trianglelefteq F$. However, $ab= 1 \cdot 1 \cdot ab=a \cdot b \cdot 1$. The representation is not unique.



<b>9. </b> $N_1,\ldots,\,N_m$ 이 각각 normal to $G$ 일 때 다음 두 statements가 동치임을 보이시오.

1. $G$ is an internal direct product of $N_1,\ldots,\,N_m$.
2. $G=N_1\cdots N_m$ and $N_k \cap (N_1N_2 \cdots N_{k-1}N_{k+1}\cdots N_m)=\{e\}$ for each $k=1,\ldots,\,m$. 

---

(1) Suppose $G$ is an internal direct product of $N_1,\ldots,\,N_m$. Let $M_k = N_1N_2 \cdots N_{k-1}N_{k+1}\cdots N_m$ and $x\in N_k \cap M_k$. 만약 $x = n_1 \cdots n_m$ 이며 $n_k \in N_k \cap M_k$ 이면 $n_k = n'_1 \cdots n'_{k-1}n'_{k+1}\cdots n'_m$ 이므로 $x=(n_1n'_1)\cdots (n_{k-1}n'_{k-1})e (n_{k+1}n'_{k+1})\cdots (n_m n'_m)$ 이므로 unique representation 이 아니다. 따라서 $N_k \cap M_k =\{e\}$ 이어야 한다.

(2) Suppose $G=N_1 \cdots N_m$ and $N_k \cap M_k = \{e\}$. $N_i$ for $i\ne k$ 는 $M_k$ 의 subset 이므로 $N_i \cap N_k=\{e\}$ for every $i\ne j$ 이다. $N_i \cap N_k = \{e\}$ 이고 $N_i \trianglelefteq G$, $N_k \trianglelefteq G$ 일 때 $a \in N_i,\, b \in N_k$ 라 하자. $aba^{-1}b^{-1}=(aba^{-1})b\in N_k$ 이며 $aba^{-1}b^{-1}=a(bab^{-1})\in N_i$ 이므로 $aba^{-1}b^{-1}=$ 이다. 따라서 $ab=ba$ 이다. $x= n_1 \cdots n_m = n'_1 \cdots n'_m$ for some $n_k \ne n'_k$ 라 하자. 그렇다면 $x=n_k m_k = n'_k m'_k$ 이며 $n_k (n'_k)^{-1}=m'_k (m_k)^{-1}=e$ 이므로 $n_k=n_k'$ 이어야 한다. 이는 조건에 모순. 따라서 $x$가 uniquely represent 되므로 $G$는 internal direct product of $N_1,\ldots,\,N_m$ 이다.



<b>10. </b> $K_1,\ldots,\,K_m$ 이 group $G$의 normal subgroup 이며  $K_1 \cap\cdots \cap  K_m =  \{e\}$ 라 하자. $V_i = G/K_i$ 라면 $G$ 와 $V_1 \times \cdots \times V_m$ 사이의 injective homomorphism이 존재함을 보이시오.

---

Define a map $\phi : G \to V_1 \times \cdots \times V_m $ by  $\phi (g)=(gK_1,\ldots,\,gK_m)$. Then,
$$
\begin{align*}
\phi (g_1g_2)&= (g_1g_2K_1,\ldots,\,g_1g_2K_m) =(g_1K_1,\ldots,\,g_1K_m)(g_2K_1,\ldots,\,g_2K_m)=\phi (g_1)\phi(g_2)
\end{align*}
$$
따라서  $\phi \in \operatorname{Hom}(G,\,V_1\times \cdots \times V_m)$. 

$x\in \ker \phi$ 이면 $g\in K_1 \cap \cdots \cap K_m$ 이므로 $x=e$. 따라서 $\ker \phi =\{e\}$ 이며 $\phi$는 injection 이다. 



<b>11. </b> $G$는 finite abelian group이며 어떤 nontrivial subgroup $H_0$ 가 존재하여 $H\le G$ 이면 $H_0 \le H$ 이다. $G$가 cyclic 임을 보이시오. $|G|$ 에 대해 더 알아낼 수 있는 것은 무엇인가?

----

(1) $G$가 cyclic이 아니면 어떤 $a_1,\ldots,\,a_m$ 이 존재하여 $\langle a_i \rangle \cap \langle a_j \rangle =\{e\}$ for each $i\ne j$ 이다. 따라서 $G$는 cyclic. 

(2) 어떤 prime $p,\,q$ with $p\ne q$ 에 대해 $p{\large \mid}|G|$, $q{\large \mid}|G|$ 라 하자. $G$가 finite abelian 이므로 각각 유일한 Sylow $p$-, $q$- subgroup $P,\,Q$ 가 존재하며 $P \cap Q=\{e\}$ 임은 자명하다. 따라서 $G$는 $p$-group 이다. 

(3) $|G|=p^m$ 이고 $G=\langle g\rangle$ 이라 하자. $\langle g^{p^{m-1}}\rangle$ 은 order $p$ subgroup of $G$ 이다. $\gcd(r,\,p)=1$ 인 $r\in \N$ 에 대해 $\langle g^r\rangle = G$ 이다. $\langle g^{p^k}\rangle$ where $k<m-1$ 인 경우는 $(g^{p^k})^{p^{m-1-k}}=g^{p^{m-1}}$이므로 $\langle g^{p^{m-1}}\rangle$ 을 포함한다. 

$p^k \mid r,\, p^{k+1}\not\mid r$ 에 대한 $\langle g^r\rangle$ 인 경우 $\mu r + \lambda p^{m}=p^k$ 인 정수 $\mu,\,\lambda$ 가 존재하며 이 때 $g^{p^k}\in \langle g^r\rangle$ 이므로 $\langle g^{p^{m1}}\rangle$ 을 포함한다.

즉 $G$가 어떤 prime $p$ , 양의정수 $m$ 에 대해 $|G|=p^m$ order 이면 된다.



<b>12. </b> $G$가 finite abelian group 일 때 $G$는 finite number of finite cyclic group의 direct product의 어떤 subgroup과 isomorphic 함을 보이시오.

---

(1) $|G|={p_1}^{\alpha_1}\cdots {p_m}^{\alpha_m}$ 이며 $p_i$'s는 각각 distinct prime numbers 이고 $\alpha_i$는 양의 정수라 하자. $P_i$를 $G$의 Sylow $p_i$-subgroup 이라 하자. $G$가 abelian 이므로 $P_i \trianglelefteq G$ 이며 $P_i \cap P_j =\{e\}$ 임은 자명하다. 우리는 problem 5. 에서 $G\approx P_1 \times \cdots \times P_m$ 임을 보았다. 

(2) 이제 각각의 $P_i$가 어떤 finite number of finite cyclic group의 direct product의 subgroup과 isomorphic 함을 보이면 된다. 

---to be done--



<b>13. </b> 어떤 finite non-abelian group $G$의 어떤 nontrivial subgroup $H_0$는 $G$의 모든 nontrivial subgroup에 포함된다. 그 예를 드시오.

---

Consider Quarternion group $Q=\{1,\,-1,\,i,\,j,\,k,\,-i,\,-j,\,-k\}$ with $i^2=j^2=k^2=-1$, $ij=k$, $jk=i$, $ki=j$, and $(-1)^2=1$. $H_0=\{1,\,-1\}$ is a subgroup of $G$. It can be shown that for every nontrivial subgroup of $G$, $H_0=\{1,\,-1\}$ is included.



<b>15.  </b> $A$ 가 order $p$ cyclic group 일 때 $G=A \times A$ 라 하자. $|\operatorname{Aut}(G)|$ 는 무엇인가?

----





<b>16. </b> $G=K_1 \times \cdots \times K_m$ 일 때 $K_i$의 center를 이용하여 $G$의 center를 기술하시오.

---

(1) Let $Z_i$ be the center of $K_i$ and $Z$ be the center of $G$. 

(2) let $z_i \in Z_i$ and $a_i \in K_i$. $(a_1,\ldots,\,a_m)(z_1,\ldots,\,z_m)=(a_1z_1,\ldots,\,a_m z_m)= (z_1,\ldots,\,z_m)(a_1,\ldots,\,a_m)$. 따라서 $Z_1 \times \cdots \times Z_m =Z$. 



<b>17.</b> $G=K_1 \times \cdots \times K_m$ 이고 $g\in G$ 일 때  $N(g)=\{x\in G : xg=gx\}$ 를 구하시오.

---

Let $g=(g_1,\ldots,\,g_m)$. Define $N_i (g)=\{x\in K_i : xg=gx\}$. Then $N(g) = N_1(g_1)\times \cdots \times N_m(g_m)$.



<b>18. </b> $N_1,\ldots,\,N_m$ 이 각각 normal to $G$ 라 하자. $G=N_1 \cdots N_m$ 이며 $|G|=|N_1|\cdots |N_m|$ 일 때 $G$는 direct product of $N_1,\ldots,\,N_m$ 임을 보이시오.

----

$N\trianglelefteq G,\, M\trianglelefteq G$ 이면, $MN\trianglelefteq G$ 이며 $NM/M \approx N/(N \cap M)$ 이다. $M_i = N_1 \cdots N_{i-1}N_{i+1}\cdots N_m$ 이라 하면 $M_i \trianglelefteq G$ 이다. $ N_i \cap M_i \ne \{1\}$ 이면 $|N_iM_i|<|N_i||M_i|\le |N_1|\cdots |N_m|$ 이므로 $G=N_1\cdots N_m$ 임에 모순. 따라서 $|G|=|N_1|\cdots |N_m|$ 이면 $N_i \cap M_i =\{1\}$ 이므로 problems 11에 의해 $G$는 direct product of $N_1,\ldots,\,N_m$. 











