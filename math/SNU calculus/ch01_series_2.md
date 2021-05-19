제 1 장 급수 #1
===


## 연습문제 1.5

<b>1.</b> 다음 급수가 수렴하는 $x$ 의 범위를 구하여라

(1) $\sum \dfrac{x^{2n}}{(2n)!}$   (2) $\sum \dfrac{x^{2n+1}}{(2n+1)!}$ 

---

(1) 
$$
1>\dfrac{a_{n+1}}{a_n}=\dfrac{x^{2(n+1)} (2n)!}{x^{2n}(2n+2)!}=\dfrac{x^2}{(2n+2)(2n+1)}
$$
이며 충분히 어떤 $N$ 에 대해 $n>N \implies \dfrac{a_{n+1}}{a_n}<1$ 이므로 모든 $x\in \mathbb{R}$ 에 대해 수렴한다.

(2) 
$$
1> \dfrac{a_{n+1}}{a_n}=\dfrac{(2n+1)! x^{2n+3}}{(2n+3)! x^{2n+1}}=\dfrac{x^2}{(2n+3)(2n+2)}
$$
이므로 (1)과 같은 이유로 모든 $x\in \mathbb{R}$ 에서 수렴한다.



<b>2. </b> Pell 의 수열은 점화식
$$
p_{n+2}=2p_{n+1}+p_n
$$
으로 주어진다. 이 때,
$$
\lim_{n \to \infty}\dfrac{p_{n+1}}{p_n}
$$
이 수렴함을 보이고, 그 극한값을 구하라. 또 이를 이용하여
$$
\sum\dfrac{1}{p_n}< \infty
$$
임을 보이라. 

<b>Note :  </b> 일단 $p_0=0$ $p_1=1$ 이라 가정한다.

---

우선 $q_n = \dfrac{p_{n+1}}{p_n}$ 이라 하자. 
$$
p_{n+2}=2p_{n+1}+p_n\implies  \dfrac{p_{n+2}}{p_{n+1}}=2 +\dfrac{p_n}{p_{n+1}} \implies q_{n+1}=2+\dfrac{1}{q_n}
$$
만약 $q_n$ 이 $q$ 로 수렴한다면 $q=2+1/q$ 를 만족하므로, $q=1\pm \sqrt{2}$ 이다. 일단 $(p_n)$ 이 양의 수열이라 가정하면 $q=1+\sqrt{2}$ 이다.
$$
q_{n+1}-q= 2+\dfrac{1}{q_n}-2-\dfrac{1}{q}=-\dfrac{q_n-q}{q_nq}
$$
$p_n>n$ for $n>1$ 이고 $q>1$ 이므로,
$$
|q_{n+1}-q|=\left|\dfrac{q_n-q}{qq_n}\right|<q|q_n-q|
$$
이며, 따라서 $\displaystyle \lim_{n \to \infty}q_n=0$ 이다. 비율판정법에 의해 $\sum \dfrac{1}{p_n}$ 은 수렴한다.





<b>3. </b> 다음 급수의 수렴 발산을 판정하라.

(1) $\sum \dfrac{2^nn!}{n^n}$    (2)$\sum \dfrac{n^2}{e^n}$     (3) $\sum \dfrac{2^n}{n^2}$   (4) $\sum \dfrac{2^n}{n^3}$ 

---

(1) 수렴한다.
$$
\dfrac{2^{n+1}(n+1)!(n)^{n}}{2^n n! (n+1)^{n+1}}=\dfrac{2(n+1) n^n}{(n+1)^{n+1}}=\dfrac{2n^n}{(n+1)^n} =2\left(1-\dfrac{1}{n+1}\right)^{n+1} \left(1-\dfrac{1}{n+1}\right)^{-1} \xrightarrow[]{n \to \infty}\dfrac{1}{e}<1
$$
(2) 수렴한다.
$$
\dfrac{(n+1)^2 e^n}{n^2e^{n+1}}=\dfrac{1}{e} \left(1+\dfrac{1}{n}\right)^2 \xrightarrow[]{n \to \infty} \dfrac{1}{e}<1
$$
(3) 발산한다.
$$
\dfrac{2^{n+1}n^2}{2^n (n+1)^2}=\dfrac{2 n^2}{(n+1)^2}\xrightarrow[]{n \to \infty}2 >1
$$
(4) 발산한다.
$$
\dfrac{2^{n+1}n^3}{2^n (n+1)^3}=\dfrac{2 n^3}{(n+1)^3} \xrightarrow[]{n \to \infty}2 >1
$$






## 연습문제 1.6

<b>1. </b> 급수 $\displaystyle \sum_{n\to \infty} \dfrac{1}{(2n+3)^s}$ 가 수렴하는 실수 $s$ 의 범위를 구하라. 

---

$s>1$ 



<b>2. </b> 적분판정법을 이용하여 다음을 보이라.

(1)  $\displaystyle \sum_{n=1}^\infty \dfrac{1}{n} = \infty$    (2) $\displaystyle \sum_{n=2}^\infty \dfrac{1}{n \ln n}= \infty$  (3) $\epsilon>0 \implies \displaystyle \sum_{n=2}^\infty \dfrac{1}{n(\ln n)^{1+\epsilon}}<\infty$  (4) $\displaystyle \sum_{n=3}^\infty \dfrac{1}{n \cdot \ln n \cdot \ln \ln n}=\infty$ 

---

(1)
$$
\int_{1}^\infty \dfrac{1}{x}dx =\left[\ln x\right]_{1}^\infty = \infty
$$
(2) 
$$
\int_{2}^\infty \dfrac{1}{x\ln x}\,dx=\left[\ln \ln x\right]_2^\infty = \infty
$$
(3) 
$$
\int_2^{\infty} \dfrac{1}{x (\ln x)^{1+\epsilon}}\,dx= \left[-\dfrac{1}{\epsilon} (\ln x)^{-\epsilon} \right]_2^\infty = \dfrac{1}{\epsilon (\ln 2)^\epsilon}<\infty 
$$
(4)
$$
\int_3^\infty \dfrac{1}{x\ln x \ln \ln x}\,dx= \left[\ln \ln \ln x\right]_3^\infty=\infty
$$


<b>3. </b> 다음을 보이라.

(1) $\displaystyle \int_1^\infty \sin \dfrac{1}{x} \,dx =\infty$,    (2) $\displaystyle \int_1^\infty \dfrac{1}{x} \sin \dfrac{1}{x} \,dx < \infty$.

---

(1) $\displaystyle \sum_{n=1}^\infty \sin \dfrac{1}{n}$ 이 발산함을 알고 있다. 따라서 발산한다.

(2) 우리는 $x>0$ 일 때, $\sin x<x$ 임을 알고 있다. 따라서, 
$$
\sum_{n=1}^\infty \dfrac{1}{n}\sin \dfrac{1}{n} < \sum_{n=1}^\infty \dfrac{1}{n^2}<\infty
$$


<b>4.</b>  여러가지 판정법중에서 편리한 것을 이용하여 다음 급수의 수렴, 발산을 판정하라.

---

(1) $\sum \dfrac{-2}{n\sqrt{n}}$
$$
\int_1^\infty \dfrac{1}{x^{3/2}}\,dx= \left[-\dfrac{1}{2\sqrt{x}} \right]_1^\infty = \dfrac{1}{2}<\infty
$$
(2)  $\displaystyle \sum_{n=3}^\infty \dfrac{\ln n}{n} > \sum_{n=3}^\infty \dfrac{1}{n} =\infty$ 

(3) $\displaystyle \sum_{n=3}^\infty \dfrac{\ln n}{\sqrt{n}}>\sum_{n=3}^\infty \dfrac{1}{n}=\infty$ 

(4) $\sum \dfrac{2^n}{n+1} =\infty$ because $\displaystyle \lim_{n \to \infty} \dfrac{2^n}{n+1}=\infty$ and $\left(\dfrac{2^n}{n+1}\right)$ is a positive sequence. 

(5) $\sum \dfrac{1}{\sqrt{n}(\sqrt{n}+1)}> \sum \dfrac{1}{\sqrt{n}{(\sqrt{n}+\sqrt{n})}}=\sum \dfrac{1}{2n}=\infty$

(6) $\sum \dfrac{\sqrt{n}}{\ln (n+1)}>\sum \dfrac{\sqrt{n}}{n+1} > \sum \dfrac{1}{2\sqrt{n}} > \sum \dfrac{1}{2n}=\infty$ 

(7) $\sum \left(1+\dfrac{1}{n}\right)^n=\infty$ because $\displaystyle \lim_{n \to \infty}\left(1+\dfrac{1}{n}\right)^n = e \ne 0$. 

(8) $\sum \dfrac{1}{(\ln 2)^n}$ 에서 $0<\ln 2<1$ 이다. 멱근판정법으로부터 발산함을 알 수 있다.

(9) $\sum \dfrac{1}{(\ln 3)^n}$ 에서 $\ln 3>1$ 이므로 멱근판정법으로부터 수렴함을 알 수 있다.

(10) $\sum n \tan \dfrac{1}{n}= \sum n \dfrac{\sin 1/n}{\cos 1/n}> \sum n \sin \dfrac{1}{n}> \sum \dfrac{2}{\pi} \to \infty$  (page 21 에서 $\sin \dfrac{1}{n}> \dfrac{2}{\pi n }$ 임을 안다. )



<b>5. </b> 급수 $\sum \dfrac{\ln n}{n^p}$ 이 수렴하는 실수 $p$ 의 범위를 구하시오.

---

(1) 임의의 양수 $\varepsilon>0$ 와 충분히 큰 $x>0$ 에 대해 $x^{\varepsilon} > \ln x$ 임을 안다. (미분을 이용해 증명 할 수 있는데..) 문제의 소지가 있는 것은 $\epsilon<1$ 일 대 이므로 $x=e^{1/\varepsilon}$ 으로 놓으면 $x^\varepsilon - \ln x=e-\dfrac{1}{\epsilon}>0$  
$$
\sum \dfrac{\ln n}{n^p}< \sum \dfrac{n^{\epsilon}}{n^p}=\sum n^{-p+\epsilon}
$$
이므로 $p>1$ 이면, 수렴한다.  

(2) $p \le 0$ 이면 $\sum \dfrac{\ln n}{n^p}\ge \sum \ln n =\infty$ 이다. 

(3) $0<p\le 1$ 이면 $\sum \dfrac{\ln n}{n^p}> \sum \dfrac{1}{n^p}\ge \sum \dfrac{1}{n}=\infty$ 



<b>6.  </b> 다음 특이적분이 수렴하는 지를 밝히라.
$$
\int_1^\infty \dfrac{x^2}{1+x^5}\, dx
$$

---

$$
\sum\dfrac{n^2}{1+n^5}< \sum \dfrac{1}{2}\dfrac{1}{n^3}<\infty.
$$



## 연습문제 1.7

<b>1.  </b> 다음 급수의 수렴여부를 판정하고, 또 절대수렴하는지를 알아보라.

---

(1) $\sum (-1)^n \dfrac{\sqrt{n}+1}{n+1}$  : $\displaystyle \lim_{n \to \infty} \dfrac{\sqrt{n}+1}{n+1}=0$ 이므로 수렴한다. 절대수렴은 No

(2) $\sum \dfrac{\cos n \pi}{n}= \sum (-1)^{n}\dfrac{1}{n}$ : 수렴 Yes, 절대수렴 No.

(3) $\sum (-1)^{n}ne^{-n}$ : $\displaystyle \lim_{n\to \infty} ne^{-n}=0$ 이므로 수렴 Yes. $\sum ne^n$ 에서 비율판정법을 사용하면, $\displaystyle \lim_{n \to \infty} \dfrac{a_{n+1}}{a_n}=\lim_{n \to\infty}\dfrac{(n+1)}{en}=\dfrac{1}{e}<1$  이므로 절대수렴.

(4) $\sum (-1)^n \sin \dfrac{1}{n}$ : $\displaystyle \lim_{n \to \infty}\sin \dfrac{1}{n}=0$ 이므로 수렴. 절대수렴 하지 않는것은 이미 안다.

(5) $\sum \dfrac{(-1)^{n+1}}{n^{3/2}}$ : 절대수렴하는것을 안다. 따라서 수렴한다.

(6) $\sum (-1)^n \left(\dfrac{n}{10}\right)^n$ : 수렴 No. 절대수렴 No

(7) $\sum (-1)^n  \dfrac{10^n}{n^{10}}$ : 
$$
\dfrac{a_{n+1}}{a_n}=\dfrac{10^{n+1} (n+1)^{10}}{10^n n^{10}}= 10 \left(1+\dfrac{1}{n}\right)^{10}>10
$$
발산. 절대수렴 No

(8)  $\sum (-1)^n \dfrac{\ln n}{n}$ : $n\to \infty$ 일 때 $0$ 으로 수렴하는 교대수열이므로 수렴. 절대수렴 No

(9) $\sum (-1)^n \ln \left(1+\dfrac{1}{n}\right)$ : $n \to \infty$ 에서 $0$ 으로 수렴하는 교대수열의 합이므로 수렴. 절대수렴 하는것은 쉽게 보일 수 있다.

(10) $\sum_{n\ge 2} \dfrac{(-1)^n}{\ln n}$ : 수렴 Yes, 절대수렴 No



<b>2. </b> 생략



<b>3. </b> 교대급수 $\sum a_n$ 에서 모든 $n$ 에 대하여 $|a_n| \ge |a_{n+1}|$ 이고 $\displaystyle \lim_{n \to \infty} a_n =0$ 일 때, 급수 $\sum a_n$ 과 $n$ 항까지의 합의 차는 $|a_{n+1}|$ 을 넘지 않음을 보여라.

---

$s_n = \displaystyle \sum_{k=1}^n a_k,\, s=\lim_{n \to \infty}s_n$ 이라 하자. 즉 $|s-s_n|\le|a_{n+1}|$ 을 보이면 된다.

편의를 위해 $a_{2n}<0,\, a_{2n+1}>0,\, b_n=|a_n|$  이라 하자. 그렇다면 $s-s_{2n}=(b_{2n+1}-b_{2n+2})+(b_{2n+3}-b_{2n+4})+\cdots >0$ 이며 같은 이유로 $s-s_{2n+1}<0$ 임을 알 수 있다. 그렇다면,
$$
\begin{align}
0<s-s_{2n}&=b_{2n+1}-(b_{2n+2}-b_{2n+3})-(b_{2n+4}+b_{2n+5})+\cdots <b_{2n+1}\\
0>s-s_{2n+1}&=-b_{2n+2}+(b_{2n+3}-b_{2n+4})+(b_{2n+5}-b_{2n+6})+ \cdots >-b_{2n+2}


\end{align}
$$
이므로 증명 끝.



<b>4. </b> 특이적분 $\displaystyle \int_0^\infty \dfrac{\sin x}{x}\,dx$ 이 수렴함을 보이라.

---

Define $a_n = \displaystyle \int_{(n-1)\pi}^{n \pi} \dfrac{\sin x}{x}\,dx$ 라 하면 적분 영역 내에서 함수의 부호는 변하지 않으므로 $a_n$ 이 교대급수임을 알 수 있다. 또한 $\lim_{x\to 0}\dfrac{\sin x}{x}=1$ 이므로 모든 영역에서 적분이 잘 정의된다. $a_n$ 의 적분 영역 내에서 $\dfrac{1}{x} < \dfrac{1}{(n-1)\pi}$ 이며,
$$
|a_n| = \left|\int_{(n-1)\pi}^{n\pi }\dfrac{\sin x}{x}\,dx \right| \le \dfrac{1}{(n-1)\pi} \left|\int_{(n-1)\pi}^{n\pi} \sin x \, dx\right|= \dfrac{2}{\pi(n-1)}
$$
이므로 $\lim_{n \to \infty}a_n=0$ 이다. 또한 $|a_{n}|\ge |a_{n+1}|$ 임은 잘 알고 있다. 따라서 이 적분은 수렴한다. 





## 연습문제 1.8



<b>1. </b> 수열 $(n^{1/n}: n=3,\,4,\ldots)$ 는 순감소 수열임을 보여라.

---

<u>a. 미분을 이용한 증명</u> $n^{1/n}$ 이 순감소이면 이것에 $\ln n^{1/n}=\dfrac{1}{n}\ln n$ 도 순감소 수열이다. $f(x) = \dfrac{\ln x}{x}$ for $x>3$ 에 대해 미분을 취하면,
$$
f'(x)=-\dfrac{\ln x}{x^2}+\dfrac{1}{x^2}=-\dfrac{\ln x-1}{x^2}<0
$$
 <u>b. 쉬운 증명</u> $n^{1/n}> (n+1)^{1/(n+1)}$ 임을 보이면 된다. 양변의 $n(n+1)$ 승을 취하면 $n^{n+1}>(n+1)^n$ 임을 보이면 된다. 우리는 $\left(1+\dfrac{1}{n}\right)^n<3$ 임을 알고 있다. 즉 $(n+1)^n <3 n^n$ 이다. 그런ㄷ $n>3$ 일 경우는
$$
(n+1)^n<3n^n <n \cdot n^{n}=n^{n+1}
$$
 이다.



<b>2. </b> 일반항이 다음과 같이 주어진 수열의 유계성과 증가-감소를 판정하라.

---

(1) $\dfrac{(-1)^n}{n}$ : 유계, 교대수열.

(2) $\sqrt{n}$ : 유계 아님. 단조증가.

(3) $\dfrac{n^2}{n+1}$ : 유계 아님. $\dfrac{a_{n+1}}{a_n}=\dfrac{(n+1)^2(n+1)}{n^2(n+2)}=\dfrac{n^3+3n^2+3n+1}{n^3+2n^2}>1$ 이므로 단조증가.

(4) $\ln \dfrac{2n}{n+1}$ : 위로 유계. $a_n=\dfrac{2n}{n+1}$ 이라 하자. $\dfrac{a_{n+1}}{a_n}=\dfrac{(n+1)(n+1)}{n(n+2)}=\dfrac{n^2+2n+1}{n^2+2n}>1$ 이므로 단조증가.

(5) $\dfrac{(-2)^n}{n^{10}}$ : 위 아래로 유계, 교대수열.



<b>3. </b> 임의의 두 양수 $a,\,b$ 에 대하여 수열 
$$
(a^n+b^n)^{1/n} \qquad n=1,\,2,\,3,\ldots
$$
은 유계인 단조수열임을 보이라. 이 수열의 극한값을 구하라. 

---

 $a>b$ 라 가정해도 no loss of generality. 그렇다면 $(a^n+b^n) I ^{1/n}=a(1+x^n)^{1/n}$ where $x=b/a<1$ 이다. 이제  $0<x<1$ 인 $x$ 에 대해 $x_n=(1+x^n)^{1/n}$ 이  감소수열임을 보이자. 
$$
\begin{align}
\left(\dfrac{x_{n+1}}{x_n}\right)^{n+1}= \dfrac{(1+x^{n+1})}{(1+x^n)^{(n+1)/n}}= \dfrac{1+x^{n+1}}{1+x^n} \cdot \dfrac{1}{(1+x^n)^{1/n}}

\end{align}
$$
 이다. 그런다 $0<x<1$ 에서 $ x^{n+1}<x^n$ 이므로  $\dfrac{(1+x^{n+1})}{1+x^n}<1$ 이다. 또한 $(1+x^n)^{1/n}>1$ 이므로 $1/(1+x^n)^{1/n}<1$ 이다. 따라서,
$$
\left(\dfrac{x_{n+1}}{x_n}\right)^{n+1}<1 \implies x_{n+1}<x_n 
$$
이므로 주어진 수열은 감소수열이다.



<b>4.</b> 다음 집합의 상한과 하한을 구하여라.

---

(1) $\left\{ \left(1+\dfrac{1}{n}\right)^n : n=1,\,2,\,3,\ldots \right\}$ : 우리는 이 수열이 증가하는 위로 유계인 수열임을 안다. 따라서 하한은  $2$ 이며 상한은  $e$ 이다.

(2) $\left\{ \left(1+\dfrac{1}{n}\right)^{n+1} : n=1,\,2,\,3,\ldots\right\}$ : 이 수열이 감소수열임을 보이자. $a_n = \left(1+\dfrac{1}{n}\right)^{n+1}$ 이라 할 때, 
$$
\dfrac{a_{n}}{a_{n+1}}=\dfrac{\left(1+\dfrac{1}{n}\right)^{n+1}}{\left(1+\dfrac{1}{n+1}\right)^{n+2}} = \left(\dfrac{1+\dfrac{1}{n}}{1+\dfrac{1}{(n+1)}}\right)^{n+1} \dfrac{1}{1+\dfrac{1}{n+1}}=\left(1+\dfrac{1}{n^2+2n}\right)^{n+1} \dfrac{1}{1+\dfrac{1}{n+1}}
$$
이다. 우리는  $a>0,\,m>0$ 에 대해 $(1+a)^m \ge 1+am$ 임을 안다. 따라서,
$$
\left(1+\dfrac{1}{n^2+2n}\right)^{n+1}\ge 1+ \dfrac{n+1}{n^2+2n}>1+\dfrac{n+1}{n^2+2n+1}=1+\dfrac{1}{n+1}
$$
이므로 $\dfrac{a_n}{a_{n+1}}>1$ 이다. 븍 $a_n$  은 감소수열이다. 따라서 이 수열의 상한은 $n=1$ 일 때의  $4$ 이며 이 수열은 $e$ 로 수렴하므로 하한은  $e$ 이다.

(3) $\left\{\dfrac{1}{n} \sin \dfrac{1}{n} : n=1,\,2,\,3,\ldots\right\}$ : $0<\dfrac{1}{n}<\pi$ for $n\in \mathbb{Z}$ 이므로 이 수열은 양의 수열이다. 또한 $\displaystyle \lim_{n\to \infty } \dfrac{1}{n}\sin \dfrac{1}{n}=0$ 이므로 하한은 $0$ 이다. 또한 이 수열이 감소수열임은 쉽게 보일 수 있다. 따라서 상한은 $\sin 1$ 이다.



<b>5. </b> 다음 함수 $f(x)$ 는 유계이지만 그 도함수 $f'(x)$ 는 유계가 아님을 보여라.

---

(1) $f(x)=x\sin \dfrac{1}{x}$ : $f'(x) = \sin \dfrac{1}{x}-\dfrac{1}{x} \sin \dfrac{1}{x}$ . $-1 \le \sin \dfrac{1}{x}  \le 1$ 이므로 도함수는 유계가 아니다. 

(2) $f(x)= \sin x^2$ : $f'(x) =2x\sin x^2$ 유계가 아님이 자명하다.



<b>6. </b>(**오일러 상수**) 임의의 자연수 $n$ 에 대하여
$$
\dfrac{1}{2}+ \dfrac{1}{3} + \cdots + \dfrac{1}{n} < \ln n < 1+\dfrac{1}{2} + \dfrac{1}{3}+\cdots + \dfrac{1}{n-1}
$$
임을 보이라. 이로부터 극한값 
$$
\lim_{n \to \infty} \left(\sum_{k=1}^n \dfrac{1}{k}-\ln n\right)
$$
이 존재함을 보이라.

----

(1) 부등식이 성립함은 $\dfrac{1}{n}$ 에 대한 구분구적법을 생각하면 자명하다. 

(2) $\displaystyle a_n = \sum_{k=1}^n \dfrac{1}{k}-\ln n$ 이라 하자. 이 수열이 유계인 단조감소수열임을 보이고자 한다.  $a_{n+1}-a_n<0$ 임을 보이기 위해  $(n+1)(a_{n+1}-a_n)$ 을 생각하면, 
$$
\begin{align}
(n+1)(a_{n+1}-a_n)&=(n+1)\left(\sum_{k=1}^{n+1} \dfrac{1}{k}-\ln (n+1) - \sum_{k=1}^n \dfrac{1}{k}+\ln n\right) \\
&= (n+1) \left[\dfrac{1}{n+1}-\ln \left(\dfrac{n+1}{n}\right)\right]=1-\ln \left(1+\dfrac{1}{n}\right)^{n+1}<0

\end{align}
$$
이다. 따라서 $a_n$ 은 단조감소수열이다. 

(3) 아래로부터 우리는 $a_n>0$ 임을 알 수 있다. 
$$
\ln n <1+\dfrac{1}{2}+ \cdots + \dfrac{1}{n-1} <\sum_{k=1}^n \dfrac{1}{k}
$$
따라서   극한값이 존재한다.



<b>7. </b> 오일러 상수
$$
\gamma :=\lim_{n \to \infty} \left(1+\dfrac{1}{2}+\cdots + \dfrac{1}{n}-\ln n\right) \approx 0.5772156649
$$
를 이용하여,
$$
\ln 2 = 1-\dfrac{1}{2}+\dfrac{1}{3}-\dfrac{1}{4} + \cdots
$$
임을 보이라.

---

$\displaystyle a_n = \sum_{k=1}^n \dfrac{1}{k}-\ln n$, $\displaystyle s_n = \sum_{k=1}^n \dfrac{(-1)^{n+1}}{k}$ 라 하자. 
$$
\begin{align}
s_{2n}&= \left( 1+ \dfrac{1}{2}+ \cdots + \dfrac{1}{2n}\right)-2\left(\dfrac{1}{2}+\dfrac{1}{4}+ \dfrac{1}{6} +\cdots + \dfrac{1}{2n}\right)\\
&= a_{2n}+\ln (2n)-(a_n +\ln n) = a_{2n}-a_n +\ln 2

\end{align}
$$
이므로 $\displaystyle \lim_{n \to \infty}s_{2n}=\ln 2$. 



<b>8.  </b> 수열 $(a_n)$ 이 수렴하면 수열 $(a_{2n})$ 도 수렴함을 설명하라. 또 수열 $(a_{3n})$ 도 수렴함을 설명하라.

---

$\epsilon -\delta$ 를 이용하면 쉽게 설명 할 수 있는데...



<b>9. </b> 급수 $\sum \dfrac{1}{(2n-1)(2n)}$ 의 합을 구하라. 

---

See problem 7. 
$$
\sum_{k=1}^n \dfrac{1}{(2k-1)(2k)}= \sum_{k=1}^n \dfrac{1}{2k-1}-\sum_{k=1}^n \dfrac{1}{2k}= \ln 2.
$$


<b>10. </b> **(특이적분)** 구간  $(a,\,b]$ 에서 정의된 연속함수 $f(x)$ 에 대하여
$$
\int_{a}^b f(x) \,dx:=\lim_{c \searrow a } \int_c^b f(x)\,dx
$$
로 정의한다. 이제
$$
\int_{0}^1 \dfrac{dx}{x^2+\sqrt{x}}
$$
가 수렴함을 보여라.

---

 $1/t=x$ 로 치환 하면 알 수 있는데.. 이걸 원하는 건가?



## 탐구문제

<b>1. </b> 수열 $\mathbf{a}$ 로 부터 얻은 급수를  $S(\mathbf{a})$ 라고 하면, $S$ 는 수열 전체의 집합에서 정의된 자기사상이 된다. 이 사상이 전단사 사상임을 보이라. 도 두 수열 $\mathbf{a},\, \mathbf{b}$ 의 합을 설명하고
$$
S(\mathbf{a}+\mathbf{b})=S(\mathbf{a})+S(\mathbf{b})
$$
임을 보이라. 실수  $t$ 에 대하여 수열 $\mathbf{a}$ 의 실수배 $t\mathbf{a}$ 를 설명하고,
$$
S(t\mathbf{a})=tS(\mathbf{a})
$$
임을 보이라.

---

(1) $A$ 를 수열 전체의 집합이라고 하면 $\mathbf{a}\in A$ 이며 $ S(\mathbf{a})\in A$ 임은 자명하다. $\mathbf{a}=(a_n:n=1,\,2,\ldots)$ 이라 하자. 임의의 $ (s_n )\in A$ 에 대해,
$$
a_1=s_1,\quad a_n = s_{n}-s_{n-1} \text{ for }n>1
$$
이라 하면 $(a_n)\in A$ 이다. 즉 $S: A\to A$ 는  surjection 이다.

(2) $s_n = t_n$ 이면  $S^{-1}(s_n)= S^{-1}(t_n)$ 이므로 $S$ 는  injection 이다. 따라서  $S$ 는  bijection 이다.



<b>2. <b>





<b>3. </b> 급수
$$
1+ \dfrac{1}{3}-\dfrac{1}{2}+ \dfrac{1}{5}+ \dfrac{1}{7}-\dfrac{1}{4} + \cdots + \left(\dfrac{1}{2^n+1}+ \dfrac{1}{2^n+3}+\cdots + \dfrac{1}{2^{n+1}-1} -\dfrac{1}{2^n}\right) + \cdots
$$
는 발산함을 보여라.

---

$\displaystyle a_n = \sum_{k=1}^{2^{n-1}} \dfrac{1}{2^n+(2k-1)} -\dfrac{1}{2^n}$ 이라 하면 위 식은 $ \sum a_n$ 이다. 
$$
a_n = \sum_{k=1}^{2^{n-1}} \dfrac{1}{2^n+2k-1}-\dfrac{1}{2^n} >\sum_{k=1}^{2^{n-1}} \dfrac{1}{2^{n+1}-1} - \dfrac{1}{2^n} =\dfrac{2^{n-1}}{2^{n+1}-1}-\dfrac{1}{2^n}
$$
이므로,
$$
\lim_{n \to \infty} a_n \ge \dfrac{1}{4}
$$
이다. 따라서 주어진 급수는 발산한다.



<b>4. </b> 등비급수의 합의 식
$$
1+r+r^2+\cdots = \dfrac{1}{1-r}  \quad(|r|<1)
$$
은  $r$ 이 복소수 일 때에도 참임을 설명하라.

---

$$
(1-r)(1+r+r^2+\cdots +r^{N-1})=1-r^N\quad \text{for }N\in \mathbb{N}
$$

은  $r\in\mathbb{C}$ 에서도 성립한다. 따라서,
$$
1+r+r^2 + \cdots +r^{N-1}=\dfrac{1-r^N}{1-r}
$$
이다.  $r=x+iy\in \mathbb{C}$ where $x,\, y \in \mathbb{R}$ 이며  $|r|=\sqrt{x^2+y^2}<1$ 이라 하면  $\displaystyle \lim_{N \to \infty} r^N=0$ 이므로 성립한다.



<b>5. </b> **(급수의 재배열)** 전단사함수 $r: \mathbb{N}\to \mathbb{N}$ 에 대하여 급수 $\sum a_n$ 의 재배열은
$$
r\left(\sum_n a_n\right) :=\sum _n a_{r(n)} =a_{r(1)}+a_{r(2)}+ a_{r(3)}+ \cdots
$$
로 주어진다. 주어진 급수 $\sum a_n$ 이 절대수렴하면, 이 급수의 재배열도 절대수렴함을 보이라. 

---

(1) $\sum a_n$ 이 절대수렴함을 가정하자. 이제 $\sum a_n= a, \sum |a_n|=b$ 라 하자.  임의의 $\varepsilon >0$ 에 대해 어떤 $N\in \mathbb{N}$ 이 존재하여,
$$
\left|\sum_{n=1}^{N} |a_n| -b \,\right|<\varepsilon \iff \sum_{n=N+1}^\infty|a_n|<\varepsilon
$$
임을 안다. 

(2) 재배열된 수열 $(a_{r(n)})$ 에서 $r$ 은 전단사 함수이다.  어떤  $M\in \mathbb{N}$ 이 존재하여 $n>M \implies r(n)>N$ 이 성립함을 알 수 있다. 만약 모든 $ n\in \N$ 에 대하여 $r(n)\le N$ 이면 전단사 함수임에 위배된다. 또한 $M\ge N$ 임은 자명하다. 즉,
$$
\sum_{n=M+1}^\infty |a_{r(n)}|<\sum_{n=N+1}^\infty |a_n|<\varepsilon \iff 0\le \sum_{n=1}^M |a_{r(n)}|-a<\varepsilon
$$
  이다.





<b>6. </b> 자연수 $n$ 에 대하 $n$ 의 분할수(partition number) 란 자연수들을 더하여 $n$  을 얻는 방법의 가짓수를 뜻한다. 이 분할수를 $p(n)$ 으로 나타내기로 하자. 보기를 들면,
$$
\begin{align}
2&=1+1\,,\\
3&=2+1 = 1+1+1\,,\\
4&=3+1 = 2+2 = 2+1+1 = 1+1+1+1\,.
\end{align}
$$
이므로 $p(2)=1,\, p(2)=2,\, p(3)=3,\, p(4)=5$ 이다. 이제 급수
$$
\sum \dfrac{1}{p(n)}
$$
이 수렴하는지 판정하라.

---

$$
5=4+1=3+2=3+1+1=2+2+1=2+1+1+1=1+1+1+1+1
$$

이므로 $p(5)=6$, 
$$
\begin{align}
6&=5+1\\
&=4+2 = 4+1+1\\
&=3+3=3+2+1=3+1+1+1 \\
&=2+2+2=2+2+1+1=2+1+1+1+1+1\\
&=1+1+1+1+1+1
\end{align}
$$
이므로  $p(6)=10$ 이다. 





--- to be done



<b>7. </b> 명제

> 공집합이 아닌 위로 유계인 집합은 상한을 가진다

는 실수의 완비성과 동치임을 보이라.

---

(1) 실수의 완비성을 가정하자. 즉 증가하는 수열의 각 항이 일정한 실수보다 작으면, 그 수열은 수렴한다고 가정한다. $(a_n)$ 이 증가하는 수열이며 $a$ 로 수렴한다고 가정하자. $(a_n)$ 은 공집합이 아니다. $a_n<a$  for all $n\in \mathbb{N}$ 임을 보이자. 만약 어떤 $N$ 에서 $a_N\ge a$ 이면 $n>N+1 \implies a_n >a$ 이므로 $(a_n)$ 은 $a$ 로 수렴하지 않는다. 따라서 모든 $a_n<a$ 이다. $b<a$ 에 대해 $b$ 가 $(a_n)$ 의 상계이면 모든 $n$ 에 대해 $|a_n -a|> \dfrac{a-b}{2}$ 이므로 $(a_n)$ 은 $a$ 로 수렴하지 않는다. 따라서 $a$ 는 $(a_n)$ 의 상한이다.

(2) 공집합이 아닌 위로 유계인 집합은 상한을 가짐을 가정한다. $(a_n)$ 가 증가하는 수열이며  $b\in \mathbb{R}$ 보다 작다면 $(a_n)$ 은 공집합이 아닌 위로 유계인 집합이므로 상한 $a$ 를 갖는다. 이제 이 수열 $(a_n)$ 이 $a$ 로 수렴함을 보이자. 임의의 $\varepsilon>0$ 에 대해 $a-\varepsilon <a_n <a$ 인 $n$ 이 존재한다. 만약 존재하지 않는다면 $a-\varepsilon$ 이 $(a_n)$ 의 상계이므로 $a$ 가 상한이라는 가정에 위배된다. 이 $n$ 에 대해 $k>n$ 이면 $a-\varepsilon<a_n <a_k <a$ 이다. 따라서 $(a_n)$ 은 $a$ 로 수렴한다.



<b>8. </b>  수열 
$$
a_1=1,\quad a_{n+1}=\sqrt{1+a_n}
$$
은 수렴함을 보이라. 황금비 $\phi = \dfrac{1+\sqrt{3}}{2}$ 는 방정식 $\phi =\sqrt{1+\phi}$ 를 만족시킨다. 이 식에서 
$$
\phi = \sqrt{1+\sqrt{1+\phi}}
$$
를 보이라. 또,
$$
\phi = \sqrt{1+\sqrt{1+\sqrt{1+\cdots}}}
$$
을 설명하라.

---

(1) $a_n> 1$ 이면 $a_{n+1} >\sqrt{2}$ 이다. $a_1=1$ 이므로 $a_2 >1$ 이고 $a_n>1$ for $n>1$ 이다.

(2)  $x>0$ 에 대해 $\sqrt{1+x}>x$ 를 풀어보면 $ x<\dfrac{1+\sqrt{5}}{2} =\phi$ 가 나온다. 즉 $a_1=1<\dfrac{1+\sqrt{5}}{2}$ 이므로 $a_2<\phi$ 이며 따라서 $a_3,\, a_4,\ldots <\phi$ 이다. 또한 $a_{n+1}>a_n$ 이므로 단조증가수열이고 유계이므로 수렴한다. 

(3) 나머지는 easy!



<b>9. </b> 수열
$$
a_1=1,\quad a_{n+1}=1+\dfrac{1}{a_n}
$$
이 수렴함을 보이라. 또 황금비 $\phi=1+\dfrac{1}{\phi}$ 를 만족시키는 것으로부터
$$
\phi =1+\dfrac{1}{1+\dfrac{1}{1+\dfrac{1}{1+\cdots}}}
$$
임을 설명하라.

---

(1) 일단 $a_1>1$ 이므로 $a_{n+1}>1$ 임은 쉽게 알 수 있다. 

(2) $x<1+\dfrac{1}{x}$ 를 만족시키는 $x$ 는 $\dfrac{1-\sqrt{5}}{2}<x<\dfrac{1+\sqrt{5}}{2}$ 이다. 따라서 $(a_n)$ 은 단조증가수열이지만 유계이다. 다라서 수렴한다.

(3) 나머지는 easy!



