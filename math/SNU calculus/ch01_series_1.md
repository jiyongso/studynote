제 1 장 급수 #1
===



## 1. 수열과 급수



#### 자연상수 $e$

$$
e:= \lim_{n \to \infty} \left(1+\dfrac{1}{n}\right)^n\;.
$$



#### 정리 1.5.2 (일반항 판정법)

급수 $\sum a_n$ 이 수렴하면 $\displaystyle \lim_{n \to \infty} a_n =0$ 이다.

---

*(proof)* $s_n = \displaystyle \sum_{k=1}^n a_k$, $s=\displaystyle \sum_{k=1}^\infty a_n$ 이라 하자. $a_n = s_n-s_{n-1}$ 이다. 
$$
\lim_{ n\to \infty} a_n = \lim_{n \to \infty} (s_n-s_{n-1})=\lim_{n \to \infty}s_n - \lim_{n \to \infty}s_{n-1}=s-s=0
$$

## 연습문제 1.1

<b>1. </b> 피보나치수열 $(f_n)$ 에서 $f_{n+1}f_{n-1}-{f_n}^2=(-1)^n$ 임을 보여라.

---

Induciton 을 통해 증명한다. $n=1$ 일 때 $f_2f_0-{f_1}^2=3\times 0 -1=-1$. $n$ 일 때 성립함을 가정하면,
$$
\begin{align}
f_{n+2}f_{n}-{f_{n+1}}^2&=(f_{n+1}+f_n)(f_{n+1}-f_{n-1})-{f_{n+1}}^2=-f_{n}=f_{n+1}f_n-f_{n+1}f_{n-1}-f_nf_{n-1} \\
&=f_n (f_{n+1}-f_{n-1})-f_{n+1}f_{n-1}= {f_{n}}^2-f_{n+1}f_{n-1}=-(-1)^n =(-1)^{n+1}

\end{align}
$$


<b>2. </b> 다음 급수의 수렴 여부를 판정하라.

(1) $\displaystyle \sum \dfrac{n^2}{50n^2+1}$     (2) $\displaystyle  \sum \dfrac{2^n-2^{-n}}{2^n+2^{-n}}$   (3) $\displaystyle \sum n \sin \dfrac{1}{n}$ 

---

(1) $\displaystyle \lim_{n \to \infty} \dfrac{n^2}{50n^2+1}=\dfrac{1}{50}\ne 0$ . 발산

(2) $\displaystyle \lim_{n \to \infty}\dfrac{2^n-2^{-n}}{2^n+2^{-n}}=1$. 발산

(3) $\displaystyle \lim_{n \to \infty}n \sin \dfrac{1}{n} =\lim_{x\to 0}\dfrac{\sin x}{x}=1$. 발산. 



<b>3. </b> (Petersburg 파라독스) 동전을 던져서 처음에 앞면이 나오면 2원을 받고, 두번째에 비로소 앞면이 나오면 $2^2$ 원을 받고, 세번째에 비로소 앞면이 나오면 $2^3$ 원을 받기로 하였다고 하자. 이러한 놀이를 하였을 때 받는 기대값이 무한디임을 설명하라.

---

$$
[\text{expectation value}]=\sum_{k=1}^\infty 2^k \dfrac{1}{2^k}=\sum_{k=1}^\infty 1=\infty
$$



<b>4. </b> 급수 $\dfrac{1}{2}+\dfrac{1}{4} + \dfrac{1}{6}+ \dfrac{1}{8} + \dfrac{1}{10}+\cdots$ 의 수렴, 발산을 판정하라.

---

주어진 급수가 $l$ 로 수렴한다면,
$$
l=\dfrac{1}{2} \left(\sum_{k=1}^\infty\dfrac{1}{n}\right)
$$

이며 $(\cdots)$ 도 수렴해야 하지만 우리는 이것이 발산함을 알고 있다. 따라서 발산한다.



<b>5. </b> 다음 급수의 합을 구하여라.

---

(1)
$$
\sum \left(\dfrac{1}{\sqrt{n+1}}-\dfrac{1}{\sqrt{n+3}}\right)=\lim_{n \to \infty} \left(\dfrac{1}{\sqrt{2}}+\dfrac{1}{\sqrt{3}}-\dfrac{1}{\sqrt{n+2}}-\dfrac{1}{\sqrt{n+3}}\right)=\dfrac{1}{\sqrt{2}}+\dfrac{1}{\sqrt{3}}\,.
$$
(2)
$$
\sum \dfrac{1}{n^2+2n}=\sum \dfrac{1}{2}\left(\dfrac{1}{n}-\dfrac{1}{n+2}\right)=\dfrac{1}{2}\left(1+\dfrac{1}{2}\right)=\dfrac{3}{4}\,.
$$

<b>6.</b> (1) $\displaystyle \lim_{n \to \infty} (\ln (n+1)-\ln n)=0$ 을 보이라.

(2) 급수 $\displaystyle \sum \left(\ln (n+1) - \ln n \right)$ 은 수렴하는가?

(3) 급수 $\displaystyle \sum \left( \ln \ln (n+1)- \ln \ln n \right)$ 은 수렴하는가?

---

(1) 
$$
\lim_{n \to \infty} \left(\ln (n+1)-\ln n\right)=\lim_{n\to \infty} \ln \left(1+\dfrac{1}{n}\right)=\ln 1 =0\,.
$$
(2)
$$
\sum \left( \ln (n+1)-\ln n\right)=\lim_{n \to \infty} \ln (n+1)=\infty \;.
$$


(3)
$$
\sum_{n \ge 2} (\ln \ln (n+1)-\ln \ln n)=\lim_{n \to \infty} \ln \ln (n+1)-\ln\ln 2 = \infty\;.
$$

## 연습문제 1.2

<b>1. </b> $0<\epsilon<1$ 일 때 다음을 보이라.
$$
\left|\dfrac{1}{1+\epsilon}-(1-\epsilon+\epsilon^2)\right|<\epsilon^3
$$

---

$$
\dfrac{1}{1+\epsilon}-(1-\epsilon+\epsilon^2)=\dfrac{1-(1-\epsilon+\epsilon^2)-(\epsilon-\epsilon^2+\epsilon^3)}{1+\epsilon} =\dfrac{\epsilon^3}{1+\epsilon} < \epsilon^3
$$



## 연습문제 1.3

<b>1. </b> 임의의 양수 $a$ 에 대하여 조화급수 $\displaystyle \sum_{n=1}^\infty \dfrac{1}{n+a}$ 는 항상 발산함을 보여라.

---

$N<a,\, N+1\ge a$ 를 만족하는 자연수 $N$ 은 항상 존재한다. 
$$
\sum_{n=1}^\infty \dfrac{1}{n+a} \ge\sum_{n=1}^N \dfrac{1}{n+a}+\sum_{n=N+1}^\infty \dfrac{1}{n+n}=\sum_{n=1}^N \dfrac{1}{n+a}+\sum_{n=N+1}^\infty \dfrac{1}{2n} = +\infty
$$


<b>2. </b> 모든 조화급수는 발산함을 보여라. 즉 주어진 실수 $a,\,b$ 에 대하여 $a$ 가 $-d$ 의 자연수의배수가 아니면 급수
$$
\sum_{n=1}^\infty \dfrac{1}{a+nd}
$$
는 발산함을 보여라.

---

$\dfrac{1}{a+nd}=\dfrac{1}{d} \dfrac{1}{n+a/d}$ . 연습문제 1을 참고.



<b>3. </b> 다음 급수의 수렴 여부를 판정하라.

(1) $\displaystyle \sum \dfrac{1}{\ln (n+1)}$  (2) $\displaystyle \sum \sin^2 \dfrac{\pi}{n}$  (3) $\displaystyle \sum \dfrac{3n^2+4n+5}{n^3+1}$  (4) $\displaystyle \sum 2^{-n^2}$

---

(1) $\ln (n+1)\le n+1\,,\forall n\in \mathbb{N}$. 발산.

(2) $\sin^2 x> \dfrac{2}{\pi}x$ for $0<x<\pi/2 \approx 1.57$. 발산.

(3) $\dfrac{3n^2+4n+5}{n^3+1} \ge \dfrac{3n^2}{n^3+1}\ge \dfrac{3n^2}{2n^3}$. 발산.

(4) $2^{-n^2}<2^{-n}$ . 수렴. 



<b>4. </b> 양의 수열 $(a_n)$ 과 $(b_n)$ 에 대하여
$$
\displaystyle \lim_{n \to \infty} \dfrac{a_n}{b_n}=1
$$
이라 하자. 이 때 $\sum a_n$ 이 수렴할 필요충분조건은 $\sum b_n$ 이 수렴하는 것임을 보여라. 만악 위 식의 우항이 $1$ 이 아니고 $2$ 인 경우는 어떠한가?

---

(1) 우선 $\displaystyle \lim_{n \to \infty}a_n =0 \iff \lim_{n \to \infty}b_n =0$ 임을 보이자. 임의의 $\epsilon >0$ 에 대해 어떤 큰 $N_1\in \mathbb{N}$ 이 존재하여 $n>N_1 \implies \left| \dfrac{a_n}{b_n}-1\right|<\epsilon$ 이다.  임의의 $0<\epsilon<1$ 을 생각하자. $(a_n),\,(b_n)$ 이 양의 수열이므로 $\left||a_n|-|b_n|\right|<|a_n -b_n|<\epsilon b_n$ for $n > N_1$ 이다.  즉 
$$
n>N_1 \implies 0<(1-\epsilon)b_n < a_n < (1+\epsilon)b_n \tag{1}
$$
이로부터 $\displaystyle \lim_{n \to \infty} a_n =0 \iff \lim_{n \to \infty}b_n=0$ 임을 알 수 있다. 

(2) 또한 (1) 로 부터 충분히 큰 $N$ 에 대해 $\displaystyle \sum_{k=N}^\infty a_n < (1+\epsilon) \sum_{k=N}^\infty b_n$ 이며 $\displaystyle \sum_{k=N}^\infty b_n < \dfrac{1}{1-\epsilon}\sum_{k=N}^\infty a_n$ 이므로 증명 끝. 



<b>5. </b> $1$ 보다 작은 양수 $a$ 에 대해
$$
\sum a^{\sqrt{n}}<\infty
$$
 임을 다음과 같은 방법으로 보이자.

(1) $n \gg 1 \implies a^{2^{n/2}} <3^{-n}$. 

(2) $\sum 2^n a^{2^{n/2}} < \infty$. 

(3) $\displaystyle \sum_{n \ge 1} a^{\sqrt{n}} \le \sum_{n \ge 0} 2^n a^{2^{n/2}} <\infty$

----

(1) $\ln a^{2^{n/2}}=2^{n/2} \ln a$ 이며 $\ln 3^{-n}=-n\ln 3$ 이다. $\ln a<0$ 이며 $\dfrac{2^{n/2}}{n}$ 는 단조증가함수이다.  $\dfrac{2^{n/2}}{n} > - \dfrac{\ln 3}{\ln a}$ 이라면 $2^{n/2}\ln a < -n \ln 3$ 이므로 $a^{2^{n/2}} <3^{-n}$ 이다. 

(2) $N \gg 1$ 이면,
$$
\sum_{n>N} 2^n a^{2^{n/2}} < \sum_{n>N} 2^n 3^{-n }=\dfrac{(2/3)^{N+1}}{1-2/3}=\dfrac{2^{N+1}}{3^N}<\infty\;.
$$

(3) 
$$
\begin{align}
\sum_{n\ge 1} a^{\sqrt{n}}&= a+a^{\sqrt{2}} + a^{\sqrt{3}} + a^{\sqrt 4}+ \cdots \\
&\le a+ (a^{\sqrt 2} + a^{\sqrt{2}}) + (a^{\sqrt{4}}+ a^{\sqrt{4}}+ a^{\sqrt{4}}+ a^{\sqrt{4}} )+ \cdots \\
&=a+2a^{\sqrt{2}} + 2^2 a^{\sqrt{4}}+ 2^3 a^{\sqrt{8}} + 2^4 a^{\sqrt{16}}+ \cdots \\
&=a+ 2a^{2^{1/2}} + 2^2 a^{2^{2/2}} + 2^3 a^{2^{3/2}}+ 2^4 a^{2^{4/2}}+ \cdots\\
&= \sum_{n=0}^\infty 2^n a^{2^{n/2}}

\end{align}
$$



## 연습문제 1.4

<b>1. </b> (1) 급수 $\sum \dfrac{2^n}{n^n}$ 의 수렴 여부를 판정하라.

(2) 극한 $\displaystyle \lim_{n \to \infty} n^{1/n}=1$ 을 이용하여 급수 $\sum \dfrac{2^n}{n^3}$ 의 수렴 여부를 판정하라.

---

(1) $\displaystyle \lim_{n \to \infty} \sqrt[n]{\dfrac{2^n}{n^n}}=\lim_{n \to \infty} \dfrac{2}{n}=0<1$.

(2)  $\displaystyle \lim_{n\to \infty}\sqrt[n]{\dfrac{2^n}{n^3}}=\lim_{n \to \infty} \dfrac{2^n}{n^{3/n}}=\lim_{n \to \infty} \dfrac{2^n}{(n/3)^{3/n}}3^{3/n}=\lim_{n \to \infty} 2^n=\infty$ .



<b>Note : </b> $\displaystyle \lim_{n \to \infty}n^{1/n}=1$ 임을 보이자.  


$$
(1+\varepsilon)^n = \sum_{k=0}^n\begin{pmatrix}n \\ k\end{pmatrix} \varepsilon^k \ge 1+ n\varepsilon + \dfrac{1}{2} n (n-1)\varepsilon^2
$$
 이다. $n$ 을 충분히 크게 잡아 $(n-1)> \dfrac{2}{\varepsilon^2}$ 이면 우변이 $n$ 보다 크며, 따라서 $(1+\varepsilon)^n \ge n$ 이다. 즉 $(1+\varepsilon)\ge n^{1/n}\ge 1$ 이다. 여기서 $\varepsilon$ 이 임의의 양수이므로 $\displaystyle \lim_{n \to \infty} n^{1/n}=1$ 이다.  



<b>2. </b> 다음 급수의 수렴 여부를 판정하라. 이때 멱근판정법이 유용한지를 살펴보라.

(1) $\displaystyle \sum \left(1- \dfrac{1}{n}\right)^{n}$    (2) $\displaystyle \sum \left(1-\dfrac{1}{\sqrt{n}}\right)^n$

---

(1) 
$$
\left(1-\dfrac{1}{n}\right)^n =  \left(\dfrac{n-1}{n}\right)^n = \dfrac{1}{\left(\dfrac{n}{n-1}\right)^n} = \dfrac{1}{\left(1+ \dfrac{1}{n-1}\right)^n} = \left(1-\dfrac{1}{n-1}\right) \dfrac{1}{\left(1+\dfrac{1}{n-1}\right)^{n-1}}
$$
이므로 $\displaystyle \lim_{n \to \infty} \left(1-\dfrac{1}{n}\right)^n = \dfrac{1}{e} >0$ 이므로 발산한다. 멱근 극한이 $1$ 이므로 유용하지 않다.

(2) $\displaystyle \lim_{n \to \infty} \left(1-\dfrac{1}{\sqrt{n}}\right)^\sqrt{n}=\dfrac{1}{e}$ 이다. 따라서 충분히 큰 $N$ 에 대해 $n>N \implies \left(1-\dfrac{1}{\sqrt{n}}\right)^{\sqrt{n}} < \dfrac{1}{e-0.01}=\alpha$ with $\alpha<1$ 이다.   

따라서 $ \left(1-\dfrac{1}{\sqrt{n}}\right)^n <\alpha^\sqrt{n}$ 이며 연습문제 1.3.5 에 의해 수렴한다. 멱근판정법이 유용하지 않다.



<b>3. </b> 멱근판정법을 $r>1$ 일 때 증명하라.

---

$\displaystyle \lim_{n \to \infty} \sqrt[n]{a_n}=r>1$ 이라 하자. $t=\dfrac{1+r}{2}<r$ 이라 하면 충분히 큰 $N$ 에 대해 $n>N \implies \sqrt[n]{a_n}>t$ 이며 $a_n > t^n >1$ 이다. 따라서 $(a_n)$ 은 발산한다.





##  참고

$$
e=\lim_{n \to \infty} \dfrac{n}{\sqrt[n]{n!}}
$$

임을 보이자.

---

(1)  $a_n = \left(1+\dfrac{1}{n}\right)^n$, $b_n = \left(1+\dfrac{1}{n}\right)^{n+1}$ 라 하자.

(2) $a_n$ 이 증가수열임을 보이자. 

<b>method 1. </b>
$$
\begin{align}
\dfrac{a_{n+1}}{a_n}&=\dfrac{\left(\dfrac{n+2}{n+1}\right)^{n+1}}{\left(\dfrac{n+1}{n}\right)^n}=\left(1+\dfrac{1}{n+1}\right) \cdot \left(\dfrac{n^2+2n}{n^2+2n+1}\right)^n\\
&=\left(1+\dfrac{1}{n+1}\right) \cdot \left(1-\dfrac{1}{(n+1)^2}\right)^n\\
\end{align}
$$
이다. 우리는 $0<x<1$ 일 때,  $(1-x)^n \ge 1-nx$ 임을 induction을 이용해 증명 할 수 있다.

$n=1$ 일 때는 자명하다. $n$ 일 때 성립함을 가정하면,
$$
(1-x)^{n+1}=(1-x)(1-x)^n\ge (1-x)(1-nx)=1-(n+1)x+nx^2>1-(n+1)x
$$
따라서 다음을 알 수 있다. 
$$
\dfrac{a_{n+1}}{a_n} \ge \left(1+\dfrac{1}{n+1}\right) \cdot\left(1-\dfrac{n}{(n+1)^2}\right)=\left(1+\dfrac{1}{n+1}\right) \cdot \left(\dfrac{n^2+n+1}{(n+1)^2}\right) \tag{1}
$$


또한,
$$
\begin{align}
(n+2)(n^2+n+1)=(n+2)\left((n+1)^2−n\right)≥(n+1)^3
\end{align}
$$
이므로,
$$
\begin{align}
\left(\dfrac{n^2+n+1}{(n+1)^2}\right)  \ge \left(\dfrac{(n+1)^3}{(n+2)(n+1)^2}\right)= \left(\dfrac{n+1}{n+2}\right) =\left(\dfrac{1}{1+\dfrac{1}{n+1}}\right)

\end{align}
$$
이다. 이것을 식 (1) 에 대입하면,
$$
\dfrac{a_{n+1}}{a_n}\ge \left(1+\dfrac{1}{n+1}\right) \cdot \left(\dfrac{1}{1+\dfrac{1}{n+1}}\right)=1
$$
 이다. 즉 $\left(1+\dfrac{1}{n}\right)^n$ 은 단조증가수열이며 이에대한 $n\to \infty$ 극한이 $e$ 이므로 $\left(1+\dfrac{1}{n}\right)^n <e$ 이다.

<b>method 2</b>

이항정리로부터,
$$
\begin{align}
\left(1+\dfrac{1}{n}\right)^n &= \sum_{k=0}^n \dfrac{n!}{k!(n-k)!} \left(\dfrac{1}{n}\right)^k \\
&= 2+\sum_{k=2}^n \dfrac{1}{k!} \prod_{m=1}^{k-1} \left( 1-\dfrac{m}{n}\right)
\end{align}
$$
임을 안다. 따라서,
$$
\begin{align}
\left(1+\dfrac{1}{n+1}\right)^{n+1} &= 2 + \sum_{k=2}^{n+1}\dfrac{1}{k!}\prod_{m=1}^{k-1}\left(1-\dfrac{m}{n+1}\right)  \\
&= 2+ \sum_{k=1}^{n} \dfrac{1}{k!}\prod_{m=1}^{k-1}\left(1-\dfrac{m}{n+1}\right) +\dfrac{1}{(n+1)!} \prod_{m=1}^n  \left(1-\dfrac{m}{n+1}\right)\\
\end{align}
$$
이다 그런데 $\left( 1-\dfrac{m}{n+1}\right)> \left(1-\dfrac{m}{n}\right)$ 이므로,
$$
\begin{align}
\left(1+\dfrac{1}{n+1}\right)^{n+1} &> 2+\sum_{k=1}^{n} \dfrac{1}{k!}\prod_{m=1}^{k-1}\left(1-\dfrac{m}{n}\right) +\dfrac{1}{(n+1)!} \prod_{m=1}^n  \left(1-\dfrac{m}{n+1}\right) \\
&>\left(1+\dfrac{1}{n}\right)^n+ \dfrac{1}{(n+1)!} \prod_{m=1}^n  \left(1-\dfrac{m}{n+1}\right) \\
&>\left(1+\dfrac{1}{n}\right)^n
\end{align}
$$
이므로  $(a_n)$ 은 단조증가수열이다. 

(3) $(b_n)$ 이 단조감소수열임을 보이자. 
$$
\dfrac{a_{n}}{a_{n+1}}=\dfrac{\left(1+\dfrac{1}{n}\right)^{n+1}}{\left(1+\dfrac{1}{n+1}\right)^{n+2}} = \left(\dfrac{1+\dfrac{1}{n}}{1+\dfrac{1}{(n+1)}}\right)^{n+1} \dfrac{1}{1+\dfrac{1}{n+1}}=\left(1+\dfrac{1}{n^2+2n}\right)^{n+1} \dfrac{1}{1+\dfrac{1}{n+1}}
$$
여기서,
$$
\left(1+\dfrac{1}{n^2+2n}\right)^{n+1}\ge 1+ \dfrac{n+1}{n^2+2n} > 1+\dfrac{n+1}{(n+1)^2}=1+\dfrac{1}{(n+1)}
$$
이므로 $a_n>a_{n+1}$ 이다. 따라서 $(b_n)$ 은 단조감소수열이다.

(4) $\displaystyle \lim_{n \to \infty} \left(1+\dfrac{1}{n}\right)^{n+1}=e$ 임은 쉽게 보일 수 있다. 따라서,
$$
\left(1+\dfrac{1}{n}\right)^n < e < \left(1+\dfrac{1}{n}\right)^{n+1}
$$
 이다. 위 식을 $n=1$ 부터 $n$ 까지 곱하면,
$$
\begin{align}
&\left(\dfrac{2}{1}\right) \left(\dfrac{3}{2}\right)^2 \cdots \left(\dfrac{n+1}{n}\right)^n < e^n <\left(\dfrac{2}{1}\right)^{2} \left(\dfrac{3}{2}\right)^{3} \cdots \left(\dfrac{n+1}{n}\right)^{n+1}\\
\implies& \dfrac{(n+1)^n}{n!}<e^n < \dfrac{(n+1)^{n+1}}{n!} \\
\implies &\left(\dfrac{n+1}{e}\right)^n <n! < (n+1)\left(\dfrac{n+1}{e}\right)^n \\
\implies & \dfrac{(n+1)}{\sqrt[n]{n!}}<e<\sqrt[n]{n+1} \dfrac{(n+1)}{\sqrt[n]{n!}}

\end{align}
$$
이다. 

 