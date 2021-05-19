II. 멱급수와 수렴반경 #1
===



## 연습문제 2절



<b>1. </b> 등식 $\ln 3 = \displaystyle \sum _{n=0}^\infty \dfrac{1}{(2n+1)4^n}$ 을 보이라.

----

교재로 부터 $\displaystyle \ln 2 = \sum_{n=1}^{\infty} \dfrac{1}{n 2^n},\, \ln \dfrac{3}{2} = \sum_{n=1}^\infty \dfrac{(-1)^{n-1}}{n2^n}$  을 안다. 둘을 더하면 짝수차항이 없어지고 홀수차항만 남아 두배가 되므로 이로부터,
$$
\begin{align}
\ln 3 = \ln \dfrac{3}{2}+ \ln 2  &= \sum_{n=1}^\infty \dfrac{(-1)^{n-1}}{n 2^n}+ \sum_{n=1}^\infty \dfrac{1}{n2^n} = \sum_{n=1}^{\infty} \dfrac{2}{(2n+1)2^{2n+1}} = \sum_{n=1}^\infty  \dfrac{1}{(2n+1)4^n}
\end{align}
$$
<b>2. </b> 다음 급수가 수렴함을 보이고, 급수의 합을 구하라.

----

아래 문제를 푸는데 이용되는 식. $\dfrac{1}{1-x}$ 의 미분을 이용하여 다음을 얻는다.
$$
\begin{align}
\dfrac{1}{1-x} = \sum_{n=0}^\infty x^n &\implies \dfrac{1}{(1-x)^2} = \sum_{n=1}^\infty nx^{n-1} \\
&\implies \dfrac{2}{(1-x)^3} =\sum_{n=2}^\infty n(n-1)x^{n-2} \\
&\implies \dfrac{6}{(1-x)^4} = \sum_{n=3}^{\infty} n(n-1)(n-2) x^{n-3} 

\end{align}\tag{2.1}
$$
$\dfrac{1}{1-x}$ 의 적분을 이용하여 다음을 얻는다.
$$
\begin{align}
\dfrac{1}{1-x} =  \sum_{n=0}^\infty x^n &\implies -\ln (1-x)=\sum_{n=0}^\infty\dfrac{x^{n+1}}{n+1} = \sum_{n=1}^\infty \dfrac{x^n}{n} \\
&\implies x+(1-x)\ln (1-x) = \sum_{n=1}^\infty \dfrac{x^{n+1}}{n(n+1)}

\end{align}\tag{2.2}
$$


(1) $\sum \dfrac{n}{4^n}$ 

식 (2.1) 의 첫번째 줄을 이용한다. 
$$
\sum_{n=1}^\infty \dfrac{n}{4^n}= \dfrac{1}{4}\left(\sum_{n=1}^\infty \dfrac{n}{4^{n-1}}\right) = \dfrac{1}{4} \dfrac{1}{(1-1/4)^2}= \dfrac{1}{4} \dfrac{16}{9}=\dfrac{4}{9}
$$

(2) $\sum \dfrac{n(n-1)}{5^n}$ 

식 (2.1) 의 두전째 줄을 이용한다. $x=1/5$ 를 넣으면 
$$
\dfrac{10}{4^3}=\dfrac{5}{32}
$$
(3) $\sum \dfrac{(-1)^{n-1}}{n} \dfrac{1}{3^n}$ 

$|x|<1$ 에 대해 $\ln (1+x)= \displaystyle \sum_{n=1}^\infty \dfrac{(-1)^{n-1}x^n}{n}$ 이므로, $x=\dfrac{1}{3}$ 을 넣으면, $\ln \left(1+ \dfrac{1}{3} \right)=\ln \dfrac{4}{3}$. 



(4) $\sum \dfrac{n(n-1)(n-2)}{2^n}$ 

식 (2.1) 의 세번째 줄을 이용한다. $x=1/2$ 를 넣으면,
$$
\dfrac{6}{(1-1/2)^4}=6\times 16=96.
$$
(5) $\sum \dfrac{n(n-1)(n-2)}{3^n}$

식 (2.1) 의 세번째 줄을 이용한다. $x=1/3$ 을 넣으면,
$$
\dfrac{6}{(1-1/3)^4}=\dfrac{6\times 3^4}{2^4}= \dfrac{243}{8}
$$


(6) $\sum \dfrac{1}{n(n+1)2^n}$ 

식 (2.2) 의 두번째 줄을 이용한다. $x=1/2$ 를 넣으면, 
$$
\sum_{n=1}^\infty \dfrac{1}{n(n+1)2^n} = 2 \cdot \sum_{n=1}^\infty \dfrac{1}{n(n+1)2^{n+1}} =2 \cdot \left( \dfrac{1}{2} + \dfrac{1}{2} \ln \dfrac{1}{2}\right)=1-\ln 2
$$
(7)  $\sum \dfrac{n^2}{2^n}$ 

$\displaystyle \sum_{n=2}^{\infty} \dfrac{n(n-1)}{2^n} = 4,\,\sum_{n=1}^{\infty}\dfrac{n}{2^n}=2$ 이므로 답은 $6$ 이다. 

(8) $\sum \dfrac{(-1)^n n^2}{2^n}$

from (2.1),
$$
\begin{align}
\dfrac{2}{(1+1/2)^3}=\dfrac{16}{27}&=\sum_{n=2}^\infty \dfrac{(-1)^n n(n-1)}{2^{n-2}}\,,\\
\dfrac{1}{(1+1/2)^2}=\dfrac{4}{9}&=\sum_{n=1}^\infty \dfrac{(-1)^{n-1} n}{2^{n-1}}
\end{align}
$$
따라서,
$$
\dfrac{1}{4}\times \dfrac{16}{27}+ \dfrac{-1}{2} \times\dfrac{4}{9} = -\dfrac{2}{27}=\sum_{n=0}^\infty \dfrac{(-1)^n n (n-1)}{2^n} + \sum_{n=0}^\infty\dfrac{(-1)^n n}{2^n}=\sum_{n=0}^\infty \dfrac{(-1)^n n^2}{2^n}
$$


<b>3. </b> 다음 급수가 수렴하는 $x$ 의 범위를 구하라. (이 문제에서도 $n\ge 1$ 이다.)

---

(1) $\displaystyle \sum \dfrac{x^n}{n^n}$ : $\displaystyle \lim_{n \to \infty} \dfrac{n^n}{(n+1)^{n+1}}=\lim_{n \to \infty}\dfrac{1}{n+1}\dfrac{1}{(1+1/n)^n} \le \lim_{n \to \infty} \dfrac{1}{en}=0$ 이므로 $x$ 는 모든 실수 에서 수렴한다.

(2) $\displaystyle \sum \dfrac{x^n}{\ln (n+2)}$ :  $\displaystyle \lim_{n \to \infty} \dfrac{\ln (n+2)}{\ln (n+3)}$ 을 구해보자. 우리는 $\ln$ 이 단조증가함수임을 알고 있다. 따라서 $ \dfrac{\ln (n+2)}{\ln (n+3)}\le 1$ 이다. 

우리는 이미 $(1+1/n)^{n+1}$ 단조감소 수열로 $e$ 로 수렴함을 알고 있다. 따라서,
$$
\left(1+\dfrac{1}{n+2}\right)^{n+3}=\left(\dfrac{n+3}{n+2}\right)^{n+3}\ge e \implies (n+3)\ge e^{1/(n+3)}(n+2) \implies (n+2) \le (n+3)^{e^{-(1/(n+3))}}
$$
를 이용하면,
$$
\dfrac{\ln (n+2)}{\ln (n+3)} \le \dfrac{-\dfrac{1}{n+3}+ \ln (n+3)}{\ln (n+3)}=1-\dfrac{1}{(n+3)\ln (n+3)}
$$
를 얻는다. 양변에 $n \to \infty$ 극한을 취하면 $\displaystyle \lim_{n \to \infty} \dfrac{\ln (n+2)}{\ln (n+3)}=1$ 을 얻는다. 따라서 $|x|<1$ 이면 수렴한다. $x=1$ 일 때는 발산함을 알고 있다. $x=-1$ 일 때는 교대급수정리로부터 수렴함을 알고 있다. 따라서 수렴구간은 $[-1,\,1)$ 이다. 

(3)  $\sum \dfrac{nx^n}{6^n}$ : $\displaystyle \lim_{n \to \infty}\dfrac{(n+1)6^n}{n6^{n+1}}=\lim_{n \to \infty} \dfrac{n+1}{6n}=\dfrac{1}{6}$ 이므로 $|x|<6$ 에서는 수렴한다. $x=\pm 6$ 일때는 발한산다. 

(4) $\sum \dfrac{n^2x^n}{1+n^2}$ : $\displaystyle \lim_{n \to \infty} \dfrac{(n+1)^2 (1+n^2)}{ n^2 (1+(n+1)^2)}=1$ 이므로 일단 $|x|<1$ 에서는 수렴한다. $x=1$ 에서는 $\sum \dfrac{n^2}{n^2+1}$ 이므로 발산한다. 같은 이유로 $x=-1$ 에서도 발산한다. 따라서 수렴구간은 $(-1,\,1)$ 이다.

(5) $\sum \dfrac{7^nx^n}{n!}$ : $\displaystyle \lim_{n \to \infty} \dfrac{7^{n+1}n!}{7^n (n+1)!}=\lim_{n \to \infty} \dfrac{7}{n+1}=0$  이므로 모든 실수에서 수렴한다.

(6) $\sum \dfrac{(-1)^n (x-2)^n}{n^n}$ : $\displaystyle \lim_{n \to \infty} \dfrac{n^n}{(n+1)^{n+1}}= \lim \dfrac{1}{n+1} \dfrac{1}{(1+1/n)^n}=0$ 이므로 모든 실수에서 수렴한다.

(7) $\sum x^n \ln n$  : $\displaystyle \lim_{n \to \infty} \dfrac{\ln (n+1)}{\ln n}=1$ 이므로 (see (2)) $|x|<1$ 에서 수렴한다. $x=\pm 1$ 에서 발산함은 쉽게 보일 수 있다.

(8) $\sum \dfrac{(x-1)^n}{(\ln (n+1))^n}$ : $\displaystyle \lim_{n \to \infty} \dfrac{(\ln (n+1))^{n}}{(\ln (n+2))^{n+1}}$ 을 구한다. 우리는 $\left(1+\dfrac{1}{n+1}\right)^{n+1}<e<\left(1+\dfrac{1}{n+1}\right)^{n+2}$ 이며 앞과 뒤의 수열은 각각 단조증가, 단조감소임을 알고 있다. 이 부등식으로부터 다음을 얻는다. 
$$
e^{1/(n+2)}<\dfrac{n+2}{n+1}<e^{1/(n+1)} \implies (n+1)e^{1/(n+2)}<n+2 <(n+1)e^{1/(n+1)}
$$
이로부터,
$$
\begin{align}
& \dfrac{(\ln (n+1))^n}{(\ln (e^{1/(n+1)} (n+1)))^{n+1}} \le \dfrac{(\ln (n+1))^{n}}{(\ln (n+2))^{n+1}} \le \dfrac{(\ln (n+1))^n}{(\ln (e^{1/(n+2)} (n+1)))^{n+1}} \\
\implies & \dfrac{1}{\left(\dfrac{1}{n+1} + \ln (n+1)\right)} \dfrac{1}{\left(\dfrac{1}{(n+1)\ln (n+1)}+1\right)^{n}} \le \dfrac{(\ln (n+1))^{n}}{(\ln (n+2))^{n+1}}  \le\dfrac{1}{\left(\dfrac{1}{n+2} + \ln (n+1)\right)} \dfrac{1}{\left(\dfrac{1}{(n+2)\ln (n+1)}+1\right)^{n}}


\end{align}
$$
여기서,
$$
\dfrac{1}{\left(\dfrac{1}{(n+1)\ln (n+1)}+1\right)^{n}} \ge \dfrac{1}{\left(\dfrac{1}{n+1}+1\right)^n} \ge \dfrac{1}{\left(\dfrac{1}{n+1}+1\right)^{n+1}}\ge \dfrac{1}{e}
$$
이며,
$$
\dfrac{1}{\left(\dfrac{1}{(n+2)\ln (n+1)}+1\right)^{n}} \le \dfrac{1}{\left(\dfrac{1}{(n+2)^2}+1\right)^n} \le 1
$$


따라서, 
$$
\dfrac{1}{e}\dfrac{1}{\left(\dfrac{1}{n+1} + \ln (n+1)\right)} \le \dfrac{(\ln (n+1))^{n}}{(\ln (n+2))^{n+1}}  \le\dfrac{1}{\left(\dfrac{1}{n+2} + \ln (n+1)\right)} 
$$
이므로 양변에 $n \to \infty$ 극한을 취하면 $0$ 이된다. 따라서 모든 실수 구간에서 수렴한다.



(9) $\sum \dfrac{n(n+1)(n+2)}{3^n}x^n$ : $\displaystyle \lim_{n \to \infty} \dfrac{(n+1)(n+2)(n+3)3^n}{n(n+1)(n+2)3^{n+1}}= \lim_{n \to \infty} \dfrac{n+3}{3n}=\dfrac{1}{3}$ 이므로 수렴반경은 $3$ 이다. $x=1$ 일때와 $x=-1$ 일 때 발산함은 쉽게 알 수 있다. 따라서 $x$ 의 수렴구간은 $(-3,\,3)$ 이다.



(10) $\sum \dfrac{x^n}{2^{^n+(-1)^n}}$ : $\displaystyle \lim_{n \to \infty} \dfrac{2^{n+(-1)^{n}}}{2^{n+1+(-1)^{n+1}}} = \lim_{n \to \infty} 2^{-1}=\dfrac{1}{2}$ 이므로 수렴반경은 $2$ 이다. $x=\pm 2$ 일 때는 발산함은 쉽게 알 수 있다. 



(11) $\sum \dfrac{\sin (n\pi /2)}{2^n}x^n$ : $\displaystyle \sum_{n=1}^\infty \sin \dfrac{n\pi}{2} \left(\dfrac{x}{2}\right)^n=\sum \left(\dfrac{x}{2}\right)^{4n-3} -\left(\dfrac{x}{2}\right)^{4n-1} $ 

교대급수이므로 $|x|<2$ 이면 수렴한다. $x= \pm 2$ 이면 발산함은 자명하다.



(12) $\sum \dfrac{\cos n\pi}{n} x^n = \sum \dfrac{(-1)^{n+1}}{n}x^n$ : 당연히 $x=1$ 에서는 수렴, $x=-1$ 에서는 발산. $|x|<1$ 에서는 수렴. 따라서 수렴구간은 $(-1,\, 1]$ 



(13) $\sum \left(n \sin \dfrac{1}{n}\right) x^n$ :  우리는 $\displaystyle \lim_{x \to 0} \dfrac{\sin x}{x}=1$ 임을 안다. 따라서, $\displaystyle \lim_{n\to \infty}\dfrac{(n+1)\sin \dfrac{1}{n+1}}{n \sin \dfrac{1}{n}}=1$. 즉 수렴반경은 ${1}$ 이다. $x=\pm 1$ 일 때는 당연이 발산. 따라서 수렴구간은 $(-1,\,1)$. 



(14) $\sum \left(n \tan \dfrac{1}{n} \right)x^n$ : $\displaystyle \lim_{x \to 0} \dfrac{\tan x}{x}=1$ 임을 안다. 따라서 13. 과 같은 이유로 수렴반경은 $1$ 이다. $\tan \dfrac{1}{n} > \sin \dfrac{1}{n}$ 이므로 $x=\pm 1$ 에서는 당연히 발산. 따라서 수렴구간은 $(-1,\,1)$. 



(15) $\sum \left(\sin \dfrac{1}{n} \right) x^n$ :  $\displaystyle \lim_{n \to \infty} \sin \dfrac{1}{n}=0$ 이며, $\displaystyle \lim_{n \to \infty} \dfrac{\sin \dfrac{1}{n+1}}{\sin \dfrac{1}{n}} = \lim_{n\to \infty} \dfrac{(n+1) \sin \dfrac{1}{n+1}}{n \sin \dfrac{1}{n}}\cdot \dfrac{n}{n+1}=1$ 이므로 $|x|<1$ 에서 수렴한다. $x=1$ 일 경우 $\sum \sin \dfrac{1}{n} > \sum \dfrac{2}{\pi n}$ 이므로 발산한다.  $x=-1$ 일 경우 절대값이 감소하며 $0$ 으로 수렴하는 교대수열이므로 수렴한다. 따라서 수렴구간은 $[-1,\, 1)$ 이다. 



(16) $\sum \left(\tan \dfrac{1}{n} \right) x^n$ : 15와 같다.



(17)  $\sum \left( \dfrac{1}{n} \tan \dfrac{1}{n}\right)x^n$ : $\displaystyle \lim_{n \to \infty} \dfrac{1}{n} \tan \dfrac{1}{n}=0$ 이며, $\displaystyle \lim_{n \to \infty} \dfrac{\dfrac{1}{n+1} \tan\dfrac{1}{n+1}}{\dfrac{1}{n}\tan \dfrac{1}{n}}= \lim_{n \to \infty} \dfrac{(n+1)\tan \dfrac{1}{n+1}}{n \tan \dfrac{1}{n}} \cdot \dfrac{n^2}{(n+1)^2}=1$ 이므로 $|x|<1$ 에서 수렴한다. $x=1$ 이면 $\sum \dfrac{1}{n} \tan \dfrac{1}{n}=\sum \dfrac{1}{n^2} \cdot \left(n \tan \dfrac{1}{n}\right)$   이다. 충분히 큰 $n$ 에서 $n \tan \dfrac{1}{n} \approx 1$ 이므로 $n \tan \dfrac{1}{n}<2$ 이다.  따라서 수렴한다. 

$x=-1$ 에서도 수렴함은 쉽게 알 수 있다. 따라서 수렴구간은 $[-1,\,1]$ 이다.



(18) $\sum \dfrac{x^n}{\ln (n+1)}$ : $\displaystyle \lim_{n \to \infty} \dfrac{1}{\ln (n+1)}=0$ 이며, $\displaystyle \lim_{n \to \infty} \dfrac{\ln (n+1)}{\ln n} $ 을 구해야 한다.
$$
\dfrac{\ln (n+1)}{\ln n}= \dfrac{\ln n \left(1+\dfrac{1}{n}\right)}{\ln n}= 1+ \dfrac{\ln \left(1+1/n\right)}{\ln n}= 1+ \dfrac{\ln (1+1/n)^n}{n \ln n}
$$
 이므로 양변에 $n \to \infty$ 극한을 취하면 분자의 $\ln$ 의 인수가 $e$ 로 수렴하고, 분모는 $\to \infty$ 이므로 $n \to \infty $ 극한에서 $1$ 이 된다. 따라서 $|x|<1$ 에서 수렴한다. $x=1$ 에서는 발산하고 $x=-1$ 에서는 수렴함은 쉽게 보일 수 있다.



(19) $\sum \dfrac{x^n}{n2^n}$ : $|x|<2$ 에서는 수렴. 나머지는 발산. 따라서 수렴범위는 $(-2,\,2)$ 이다. 



<b>4. </b> $|x|<1$ 이면
$$
\ln \dfrac{1+x}{1-x}=2\sum_{n=1}^\infty \dfrac{x^{2n-1}}{2n-1}
$$
임을 또 보이라. 또 $|x|>1$ 이면
$$
\ln \dfrac{x}{x-1}=\sum\dfrac{1}{nx^n},\qquad \ln \dfrac{x}{x+1}=\sum \dfrac{(-1)^n}{nx^n}
$$
임을 보이라.

---

From text p. 63,
$$
\begin{align}
\ln \dfrac{1+x}{1-x} &= \ln (1+x)-\ln (1-x)=\sum_{n=1}^\infty \dfrac{(-1)^{n-1}x^n}{n} + \sum_{n=1}^\infty \dfrac{x^n}{n}=\sum_{n=1}^\infty \dfrac{x^{2n-1}}{2n-1}\;.
\end{align}
$$
$y=1/x$ 라 하면 $|y|=1$ 이며,
$$
\begin{align}
\ln \dfrac{x}{x-1}&=\ln \dfrac{1/y}{1/y-1}=-\ln (1-y)= \sum_{n=1}^\infty \dfrac{y^n}{n}=\sum_{n=1}^\infty \dfrac{1}{nx^n}\,,\\
\ln\dfrac{x}{x+1}&=\ln \dfrac{1/y}{1/y+1}=-\ln (1+y)= -\sum_{n=1}^\infty \dfrac{(-1)^{n-1}y^n}{n}=\sum_{n=1}^\infty \dfrac{(-1)^n}{nx^n}\;.

\end{align}
$$


<b>5. </b> 갑과 을 두 사람이 '가위-바위-보' 를 하여 진 사람이 이긴 사람에게 100원을 주기로 하였다. 이 놀이를 갑이 이길 때까지 하고 종료한다고 하면, 갑이 얻게 되는 기대값은 얼마인가?

---

$$
M=\sum_{n=1}^\infty (100-100(n-1)) \times \left(\dfrac{1}{2}\right)^n= \sum_{n=1}^n (200-100n)\times \left(\dfrac{1}{2} \right)^n = 200-200=0
$$



<b>6. </b> 주어진 임의의 자연수 $N$ 에 대하여 다음 멱급수의 수렴반경이 모두 같음을 보이시오.
$$
\sum_n a_n x^n \,, \qquad \sum_{n\ge N} a_n x^n \,, \qquad \sum_n a_n x^{n+N}
$$

---

(1) $|x|=r$ 에서 $\sum a_n x^n$ 이 수렴한다고 가정하자. 그렇다면 $\displaystyle \sum_{n\ge N} a_n x^n = \sum_n a_n x_n-\sum_{n=1}^{N-1} a_n x^n$  이며 $-\sum$ term은 유한한 수이므로 $\sum_{n\ge N}a_n x^n$ 이 수렴한다. 

(2) $|x|=r$ 에서 $\displaystyle \sum_{n \ge N} a_n x^n$ 이 수렴함을 가정하자. $x^N$ 을 곱해도 수렴하며 $\displaystyle \sum_{n} a_n x^{n+N}=x^N \left(\sum_{n\ge N} x^n\right)- x^N \left(\sum_{n=1}^{N-1} a_n x^n\right)$ 이며 second term은 유한한 term $\sum_n a_n x^{n+N}$ 도 수렴한다.

(3) $|x|=r$ 에서 $\displaystyle \sum_n a_n x^{n+N}$ 이 수렴함을 가정하자. $r=0$ 일 때는 위 수열 $\displaystyle \sum_n a_n x^n=0$ 이므로 수렴한다. $r\ne 0$ 일 때는 $\displaystyle \sum_n a_n x^n = (x^N)^{-1}\left(\sum_n a_n x^{n+N}\right)$ 이므로 수렴한다.

(4) 따라서 세 급수의 수렴조건이 동등하므로 수렴반경은 같다.



<b>7. </b> 임의의 자연수 $k$ 와 $|x|<1$ 에 대하여
$$
\dfrac{x^k}{(1-x)^{k+1}}=\dfrac{1}{k!}\sum_{n=k}^{\infty} n (n-1)\cdots (n-k+1)x^n
$$
임을 보이라.

---

$\displaystyle \dfrac{1}{1-x}=\sum_{n=0}^\infty x^n$ 을 $k$ 번 미분하면,
$$
\dfrac{k!}{(1-k)^{k+1}} = \sum_{n=k}^\infty n (n-1) \cdots (n-k+1)x^{n-k}
$$
이다. 양변을 $k!$ 로 나누고 $x^k$ 를 곱하면 주어진 식을 얻는다.



<b>8. </b> 멱급수 $\sum a_n x^n$ 의 수렴반경과 멱급수 $\sum a_n x^{2n}$ 의 수렴반경 사이의 관계를 구하라.

---

$\sum a_n x^{2n}=\sum a_n (x^2)^n$ 이다. $|x|=r$ 일 때 $\sum a_n x^n$ 이 수렴한다면 $|x|=\sqrt{r}$ 일 때 $\sum a_n x^{2n}$ 에서 수렴한다. $|x|=s$ 일 때 $\sum a_n x^{2n}$ 에서 수렴한다면, $|x|=s^2$ 일 때 $\sum a_n x^{n}$ 에서 수렴한다.



<b>9. </b> 구간 $|x|<1$ 에서
$$
\operatorname{li_2}(x) :=\sum_{n=1}^\infty \dfrac{x^n}{n^2}
$$
으로 정의하였을 때,
$$
\operatorname{li_2}(x) = - \int_{0}^x \dfrac{\ln (1-t)}{t} dt
$$
를 보이라.

---

$\displaystyle \ln (1-t)=- \sum_{n=1}^\infty \dfrac{t^n}{n}$ 이므로,
$$
-\int_0^x \dfrac{\ln (1-t)}{t}\,dt = \sum_{n=1}^\infty \int_0^x \dfrac{t^{n-1}}{n}dt=\sum_{n=1}^\infty \dfrac{x^n}{n^2}
$$
이다.





<b>10. </b>

trivla



<b>11. </b> 피보나치수열 $(f_n)$ 에 대해 멱급수 
$$
f(x) = \sum f_n x^n
$$
의 수렴반경을 구하고, 이때 $f(1/2)$ 의 값을 구하라.

---

피보나치수열 $f_n$ 에 대해 $r_n = \dfrac{f_{n}}{f_{n+1}}$ 이 $\dfrac{-1+\sqrt{5}}{2}$ 로 수렴함을 안다. 즉 피보나치수열의 수렴반경은 $\dfrac{-1+\sqrt{5}}{2}$ 이다. 
$$
\begin{align}
f(x) &= x+x^2 + \sum_{n=3}^\infty (f_{n-1}x^n + f_{n-2}x^n) \\
&= x+x^2+x\sum_{n=3}^\infty f_{n-1}x^{n-1}+x^2 \sum_{n=3}f_{n-2}x^{n-2} \\
&=x+x^2 +x(f(x)-x) +x^2f(x)\\
&=x+xf(x)+x^2f(x)
\end{align}
$$
이다. $f(1/2)=1/2+1/2f(1/2)+1/4f(1/2)$ 이므로 $f(1/2)=2$ 이다. 



