멱급수와 수렴반경 #2
===



#### 3.1.1. 기본연습문제

등식
$$
\dfrac{1}{e}=\dfrac{1}{2!}-\dfrac{1}{3!}+ \dfrac{1}{4!}-\dfrac{1}{5!}+ \cdots
$$
임을 보이고, 이를 이용하여 $e$ 가 무리수임을 증명하라.

---

(1) $\displaystyle \exp (x) = \sum_{n=0}^\infty \dfrac{x}{n!}$ 에 $x=-1$ 을 대입하면 위 식을 얻는다.

(2) $1/e$ 가 유리수라고 하면 어떤 자연수 $p$ 를 $1/e$ 에 곱하면 자연수가 된다. 따라서,
$$
\dfrac{p!}{e} = \dfrac{p!}{2!}-\dfrac{p!}{3!}+ \cdots + (-1)^p \dfrac{p!}{p!}+ \sum_{k=p+1}^\infty (-1)^k \dfrac{p!}{k!}
$$
에서 $\displaystyle \sum_{k=p+1}^\infty (-1)^k \dfrac{p!}{k!}$ 도 자연수 이어야 한다. 그런데,
$$
\begin{align}
\left|\sum_{k=p+1}^\infty (-1)^{k}\dfrac{p!}{k!}\right|< \sum_{k=p+1}^\infty \dfrac{p!}{k!} \le 1
\end{align}
$$
이므로 $\dfrac{1}{e}$ 가 유리수가 되려면 $\displaystyle \sum_{k=p+1}^\infty (-1)^k \dfrac{p!}{k!}=0$ 이어야 한다. 즉 $\displaystyle\dfrac{1}{(p+1)!}= \sum_{n=1}^\infty (-1)^{n+1}\dfrac{1}{(p+n+1)!}$ 이어야 한다. 그러나, 양변에 $(p+1)!$ 을 곱하여 전개시켜주면, 
$$
\begin{align}
1=\left|\sum_{n=1}^\infty (-1)^{n+1} \dfrac{(p+1)!}{(p+n+1)!}\right| & < \sum_{n=1}^{\infty} \dfrac{(p+1)!}{(p+n+1)!} \\
&= \dfrac{1}{p+2} + \dfrac{1}{(p+2)(p+3)} + \dfrac{1}{(p+2)(p+3)(p+4)}+\cdots\\
&< \dfrac{1}{p+2}+ \dfrac{1}{(p+2)^2}+ \dfrac{1}{(p+3)^2} +\cdots \\
&= \dfrac{1/(p+2)}{1-1/(p+2)} = \dfrac{1}{p+2-1}=\dfrac{1}{p+1}

\end{align}
$$
이 되므로 모순. 즉 $1/e$ 는 유리수가 아니다.

#### 3.2.1 기본연습문제

<b>1. </b> 다음을 보이라.

---

(1) $\displaystyle \lim_{x \to \infty} \dfrac{x^2}{2^x}=0$ : $2^x = e^{x \ln 2}$ 이다. 즉 $2^x=e^{x \ln 2}= 1+ x\ln 2 + \dfrac{(x\ln 2)^2}{2}+ \dfrac{(x\ln 2)^3}{3!}+\cdots $  이므로, 임의의 자연수 $n$ 에 대하여 $2^x > \dfrac{(x\ln 2)^n}{n!}$ 이다. $x>\dfrac{4!}{(\ln 2)^4}$ 이라 하면 
$$
2^x> \dfrac{x^4 (\ln 2)^4}{4!}=\dfrac{x(\ln 2)^4}{4!}x^3>x^3
$$
이므로 $\dfrac{x^2}{2^x} < \dfrac{1}{x}$ for sufficiently large $x$. 따라서 극한이 $0$ 이다. 

(2) $\displaystyle \lim_{x\to \infty}\dfrac{x^3}{3^x} = 0$ : $0<\dfrac{x^3}{3^x} < \dfrac{x^3}{e^x}$ 이며 $x>5!=120$ 이면 $e^x>x^4$ 이므로 $ \dfrac{x^3}{3^x}< \dfrac{1}{x}$ 이다. 따라서 극한이 $0$ 이다. 



<b>2. </b> 주어진 자연수 $n$ 에 대하여,
$$
x\gg 1 \implies \ln x < \sqrt[n]{x}
$$
임을 보여라.

---

$e^x$ 가 단조증가 함수이므로 $\ln x< \sqrt[n]{x} \implies e^{\ln x}< e^{\sqrt[n]{x}}$ 이다. 즉 $x \gg 1 \implies x< e^{\sqrt[n]{x}}$ 임을 보이면 된다. 
$$
e^{\sqrt[n]{x}}=e^{x^{1/n}}= \sum_{k=0}^\infty \dfrac{x^{k/n}}{k!}
$$
이다. 이로부터 우리는 임의의 자연수 $k$ 에 대해 $e^{\sqrt[n]{x}}> \dfrac{x^{k/n}}{k!}$ 임을 안다. $k=2n$ 으로 놓드면 $e^{\sqrt[n]{x}}> \dfrac{x^2}{k!}$ 이며, $x>k!=(2n)!$ 일 때,
$$
e^{\sqrt[n]{x}}> \dfrac{x^2}{(2n)!}=\dfrac{x}{(2n)!}x >x
$$
이다. 

<b>3. </b> trivial



<b>4. </b> trivial





## 연습문제 2장 3절.

<b>1. </b> 지수함수 $\exp (x)$ 는 어떤 멱급수 함수 $u(x)$ 에 대하여
$$
\exp (x) = 1+ x + \dfrac{x^2}{2} u(x)
$$
로 표현됨을 보여라.

---

$$
\exp (x) = \sum_{k=0}^\infty \dfrac{x^k}{k!}= 1+x+\sum_{k=0}^\infty \dfrac{x^{k+2}}{(k+2)!}=1+x+\dfrac{x^2}{2} \left(\sum_{k=0}^\infty \dfrac{2}{(k+2)!} x^k \right)
$$



<b>2. </b> 다음 극한값을 구하라.
$$
\displaystyle \lim_{x \to 0} \dfrac{e^x-1-x}{x^2}
$$

---

$$
\dfrac{e^x-1-x}{x^2}= \sum_{k=0}^\infty \dfrac{x^k}{(k+2)!}
$$

이므로 극한값은 $1/2$. 



<b>3. </b> 베르누이 함수
$$
B(x) = \dfrac{x}{e^x-1}
$$
의 멱급수 전개를 구하여 보자. 이 함수는 원점에서 값을 
$$
B(0)= \lim_{x\to 0} \dfrac{x}{e^x-1}=1
$$
로 정의한다.

(1) 우선 $e^x-1 = x+\dfrac{1}{2}x + \dfrac{1}{3!}x^3 + \cdots $ 에서
$$
\begin{align}
B(x)& = \dfrac{x}{x+ \dfrac{1}{2}x^2 + \dfrac{1}{3!}x^3 + \cdots} = \dfrac{1}{1+ \dfrac{1}{2}x + \dfrac{1}{3!}x^2 + \cdots }\\
&= 1-\left(\dfrac{1}{2}x + \dfrac{1}{3!}x^2 + \cdots \right) + \left(\dfrac{1}{2}x + \dfrac{1}{3!}x^2 + \cdots \right)^2 + \cdots \\
&= 1 - \dfrac{1}{2}x + \dfrac{1}{12}x^2 + \cdots


\end{align}
$$
임을 보이라. 

(2) 함수 
$$
B(x) - \left(1- \dfrac{1}{2} x \right)
$$
는 $x$ 대신에 $-x$ 를 넣어도 변하지 않는 **짝함수** 임을 보이고, 이로부터 이 함수의 멱급수 전개는 모두 짝수차항으로만 이루어져 있음을 밝히라.

(3) 베르누이수 $B_1,\,B_2,\,B_3,\ldots$ 는 등식
$$
\dfrac{x}{e^x-1} = 1 - \dfrac{x}{2}- \sum_{n=1}^\infty (-1)^n \dfrac{B_n}{(2n)!} x^{2n}
$$
을 만족시키는 수이다. 이 때 
$$
B_1= \dfrac{1}{6},\qquad B_2= \dfrac{1}{30}
$$
임을 보이라.

---

(1) $|y|<1$ 일 때, $\dfrac{1}{1+y}=1-y+y^2-y^3+\cdots +(-1)^n y^n + \cdots $ 이다. 따라서 $\left|\dfrac{1}{2}x+\dfrac{1}{3!}x^2 + \cdots \,\right|<1$ 이면 위의 식이 성립하는데.. $>1$ 일 때는? 

(2) $f(x) = B(x)-\left(1-\dfrac{1}{2}x\right)$ 하면, 
$$
\begin{align}
f(-x)=B(-x)-1-\dfrac{1}{2}x &= \dfrac{-x}{e^{-x}-1}-1-\dfrac{1}{2}x \\
&=\dfrac{1}{e^x-1}\left(xe^x-(e^x-1)-\dfrac{1}{2}x(e^x-1) \right) \\
&=\dfrac{1}{e^x-1} \left( xe^x-e^x+1- \dfrac{1}{2}xe^x+\dfrac{1}{2}x\right) \\
&=\dfrac{x}{e^x-1} +\dfrac{1}{e^x-1} \left(\dfrac{1}{2}xe^x-e^x+1-\dfrac{1}{2}x\right) \\
&=\dfrac{x}{e^x-1}-1+\dfrac{1}{2}x \\
&=f(x)

\end{align}
$$
$\displaystyle g(x) = \sum_{n=0}^\infty a_n x^n$ 이며 양함수라 하자. $g(x)=g(-x)$ 이므로 $\displaystyle g(x) = \dfrac{g(x)+g(-x)}{2}=\sum_{n=0}^\infty a_{2n}x^{2n}$ 이므로 $g$ 의 멱급수 전개는 짝수차항으로 이루어졌다. (일단 uniqueness of power series 는 가정한다)



(3) $B(x)$ 를 4차항까지 전개하며 홀수차항의 계수가 $0$ 이므로 홀수차항은 생각하지 않는다. 
$$
\begin{align}
B(x)-(1-\dfrac{1}{2}x)&= - \left(\dfrac{1}{6}x^2 + \dfrac{1}{24}x^3 + \dfrac{1}{120}x^4 + \cdots\right) \\
&\qquad+   \left(\dfrac{1}{2}x +\dfrac{1}{6}x^2 + \dfrac{1}{24}x^3 + \dfrac{1}{120}x^4 + \cdots\right)^2 \\ 
&\qquad -  \left(\dfrac{1}{2}x +\dfrac{1}{6}x^2 + \dfrac{1}{24}x^3 + \dfrac{1}{120}x^4 + \cdots\right) ^3 \\
&\qquad +  \left(\dfrac{1}{2}x +\dfrac{1}{6}x^2 + \dfrac{1}{24}x^3 + \dfrac{1}{120}x^4 + \cdots\right) ^4 + \cdots \\
&= \left(-\dfrac{1}{6} + \dfrac{1}{4} \right)x^2 + \left(-\dfrac{1}{120}+ \dfrac{1}{36}+\dfrac{1}{24} -\dfrac{1}{8} + \dfrac{1}{16}\right) x^4 + \cdots\\
&=\dfrac{1}{12}x^2 + \dfrac{-6+20+30-90+45}{720}x^4+ \cdots\\
&=\dfrac{1}{12} x^2 - \dfrac{1}{120}x^4 + \cdots

\end{align}
$$
이므로 $B_1=\dfrac{1}{6},\, B_2= \dfrac{1}{30}$ 이다.



<b>4. (이항전개) </b> 주어진 자연수 $r$ 에 대하여 미지수 $x$ 에 대한 다항식 $(1+x)^r$ dmf wjsrogkaus $n$ 차항 $x^n$ 의 계수는
$$
\begin{pmatrix} r\\n \end{pmatrix} := {}_rC_n = \dfrac{r(r-1)\cdots (r-n+1)}{1\cdot 2 \cdots n} = \dfrac{r!}{n! (r-n)!}
$$
 로 주어진다. 
$$
(1+x)^r = \sum_{n=0}^r \begin{pmatrix} r\\n \end{pmatrix} x^n
$$
 이제 이항전개의 개수 $\begin{pmatrix} r\\n\end{pmatrix}$ 을 $r$ 이 임의의 실수일 때 도 의미가 있도록 다음과 같이
$$
\begin{pmatrix} r\\n \end{pmatrix} := \dfrac{r(r-1)\cdots (r-n+1)}{1 \cdot 2 \cdots n }
$$
로 정의한다.



만약 $r$ 이 자연수가 아닌 실수이면 멱급수
$$
f(x):=\sum_{n=0}^\infty \begin{pmatrix} r\\n \end{pmatrix}x^n = 1+rx+\dfrac{r(r-1)}{2} x^2+ \cdots
$$
의 수렴반경이 $1$ 임을 보이고, $f(x)$ 는 미분방정식
$$
(1+x) f'(x) = rf(x) \qquad (|x|<1)
$$
을 만족시킴을 보이라. 이로부터
$$
(1+x)^r= \sum_{n=0}^\infty \begin{pmatrix} r\\n\end{pmatrix} x^n \qquad (|x|<1)
$$
을 보이라. 또 $|x|<1$ 일 때 다음을 보이라.
$$
\begin{align}
\sqrt{1+x}&=1+\dfrac{1}{2}x- \dfrac{1}{8}x^2 + \dfrac{1}{16}x^3 + \cdots\\
\sqrt[3]{1+x}&=1+\dfrac{1}{3}x-\dfrac{1}{9}x^2 + \dfrac{5}{81}x^3 + \cdots

\end{align}
$$

---

(1) $r$ 이 정수일 때는 다항식으로 전개되므로 $r$ 이 정수가 아닐 때를 생각한다. 우선 수렴반경을 보이자. 
$$
\lim_{n\to \infty} \dfrac{a_{n+1}}{a_n}=\lim_{n\to \infty} \dfrac{r(r-1)\cdots (r-n)\times 1\cdot 2 \cdots n}{r(r-1)\cdots (r-n+1) \times 1 \cdot 2 \cdots (n+1) }=\lim_{n \to \infty} \dfrac{(r-n+1)}{(n+1)}=-1
$$
이다. 따라서 수렴반경은 $1$ 이다.

(2) $(1+x)f'(x) = rf(x)$ 를 보이자. 
$$
\begin{align}
(1+x)f'(x) &= (1+x) \sum_{n=0}^\infty \begin{pmatrix} r\\n \end{pmatrix}nx^{n-1} \\
&=\sum_{n=1}^\infty \begin{pmatrix}r\\n\end{pmatrix} (nx^{n-1}+nx^{n}) \\
&= r+ \sum_{n=2}^\infty \begin{pmatrix} r\\n\end{pmatrix} nx^{n-1} + \sum_{n=1}^\infty \begin{pmatrix} r\\n\end{pmatrix}nx^n \\
&=r+\sum_{n=1}^\infty \left[\begin{pmatrix} r\\ n+1\end{pmatrix}(n+1)+\begin{pmatrix}r\\n\end{pmatrix} n\right ] x^n \\
&=r+ \sum_{n=1}^\infty \left(\dfrac{r(r-1)\cdots (r-n)}{1\cdot 2 \cdots n} + \dfrac{r(r-1)\cdots (r-n+1)}{1\cdot 2\cdots (n-1)}\right)x^n \\
&=r+ \sum_{n=1}^\infty \left(\dfrac{r(r-1)\cdots (r-n+1)\cdot  (r-n) + r(r-1)\cdots (r-n+1) n}{1\cdot 2 \cdots n}\right) x^n \\
&=r+ \sum_{n=1}^\infty r\dfrac{r (r-1)\cdots (r-n+1)}{1\cdot 2 \cdots n}x^n = rf(x)

\end{align}
$$
(3) 
$$
\dfrac{d}{dx}\dfrac{f(x)}{(1+x)r}=\dfrac{f'(x)}{(1+x)^r}-\dfrac{rf(x)}{(1+x)^{r+1}}=\dfrac{(1+x)f'(x)-rf(x)}{(1+x)^{r+1}}=0
$$
이므로 $f(x)= c (1+x)^r$ for $c=\text{const.}$ 이다. $x=0$ 을 넣으면 $c=1$ 임을 알 수 있다. 따라서 $f(x)=(1+x)^r$



(4) $\sqrt{1+x}$ 에는 $r=1/2$, $\sqrt[3]{1+x}$ 눈 $x=1/3$ 을 넣어 계산해보면 된다.



## 연습문제 2장 4절.

<b>1. </b> $\cos 0.1$ 의 값을 오차의 범위가 $10^{-3}$ 이하가 되도록 구하라.

---

$\displaystyle \cos x = \sum_{n=0}^\infty \dfrac{(-1)^n}{(2n)!}x^{2n}$ 이다. 멱급수 전개를 이용하면,
$$
\cos 0.1=1-0.005+4.166\times 10^{-6} + \cdots
$$
이며 $n$ 번째 항 $ \dfrac{(-1)^n}{(2n)!}x^{2n}$ 의 절대값이 계속 감소하는 교대수열이므로 $3$ 번째 항 이하가 $10^{-3}$ 보다 커질 수 없다. 따라서 $\cos 0.1 \approx 0.995$ 이다. 



<b>2. </b> 탄젠트 함수 $\tan x$ 의 멱급수 전개는
$$
\tan x = x +\dfrac{x^3}{3}+ \dfrac{2}{15}x^5 + \cdots
$$
임을 보이라. (물론 의미있는 구간은 $\left(-\dfrac{\pi}{2},\, \dfrac{\pi}{2}\right)$ 이다. )

---

$\tan x = \dfrac{\sin x}{\cos x}$ 이므로 $\tan (-x)= -\tan x$ 인 odd function 이다. $\tan x=\sum a_n x^n$ 이라 하자. odd function 이므로,
$$
\tan x = \dfrac{\tan x- (\tan (-x))}{2}= \sum_{n=0}^\infty a_{2n+1}x^{2n+1}
$$
이다. 즉 $\tan x$ 의 멱급수 전개에서는 홀수차 항만 생각하면 된다.

$a_n = \left(\dfrac{d^n}{dx^n}\tan x\right)(0)$ 이라 하면, $ a_1=1,\,a_3=2,\,a_5=16$ 이므로,
$$
\tan x = x + \dfrac{2}{3!}x^3+ \dfrac{16}{5!}x^5 + \cdots = x+\dfrac{1}{3}x^3+ \dfrac{2}{15}x^5+\cdots
$$




<b>3. </b> 어떤 멱급수 함수 $u(x),\, v(x)$ 에 대하여 다음이 성립함을 보이라.
$$
\sin x = x-\dfrac{x^3}{6}u(x),\qquad \cos x =1-\dfrac{x^2}{2}+\dfrac{x^4}{24}v(x);.
$$

---

교재에 주어진 멱급수전개로부터,
$$
\begin{align}
u(x) &=\sum_{n=1}^\infty (-1)^{n+1} \dfrac{3!}{(2n+1)!}x^{2n-2}\,,\\
v(x) &= \sum_{n=1}^\infty (-1)^{n+1} \dfrac{4!}{(2n+2)!} x^{2n-2}

\end{align}
$$
를 얻는다.



<b>4. </b> 다음 극한값을 구하라.

skip



<b>5. </b> 피타고라스의 소리에 관한 이론에 의하면, 길이가 $1/2$ 인 현 $S_{1/2}$ 이 내는 소리는 길이가 $1$ 인 현 $S_1$ 이 내는 소리보다 한 옥타브 높은 소리가 난다. $1$ 과 $2$ 의 조화평균인 $\dfrac{1}{\dfrac{1}{2} \left(\dfrac{1}{1}+\dfrac{1}{1/2}\right)}=\dfrac{2}{3}$ 를 길이로 가지는 현 $S_{2/3}$ 은 기본현 $S_1$ 보다 장오도 높은 소리를 낸다. 즉 기본현이 다($C$)음을 내면, 길이가 $2/3$ 인 현은 사($G$) 음을 내고, 길이가 $1/2$ 인 현은 높은 다($c$) 음을 낸다. 이러한 소리들은 모두 사인곡선으로 표현되는데, 현들 $S_1,\, S_{2/3},\, S_{1/2}$ 이 같은 크기로 내는 소리는 다음 곡선에 대응한다.
$$
S_1 (x) = \sin x,\qquad S_{2/3}(x) = \sin \dfrac{3}{2}x ,\qquad S_{1/2}(x) = \sin 2x\;.
$$
이제 $C,\,G,\,c$ 음을 동시에 울릴 때 생기는 아름다운 소리
$$
\sin x + \sin \dfrac{3}{2}x  + \sin 2x
$$
의 멱급수 전개를 구하여라.
$$
\begin{align}
\sin x + \sin \dfrac{3}{2} x + \sin 2x = \sum_{n=0}^\infty (-1)^{n}\left(1+ \dfrac{3^{2n}}{2^{2n+1}}+2^{2n+1}\right)\dfrac{x^{2n+1}}{(2n+1)!}

\end{align}
$$


<b>6. </b> $\cos 1$ 과 $\sin 1$ 이 모두 무리수임을 보이라.

---

$\displaystyle \cos 1 = \sum_{n=0}^\infty \dfrac{(-1)^n}{(2n)!}$ 이다. $\cos 1$ 이 유리수라면 곱하여 자연수가되는 어떤 자연수 $p$ 가 존재한다. $N\in \mathbb{N}$ 이 $2N\le p$  이고 $2(N+1)>p$ 를 만족한다고 하자. (이런 $N$ 은 항상 존재한다.) 그렇다면,
$$
p!\cdot \cos 1 = p! -\dfrac{p!}{2!}+ \dfrac{p!}{4!} + \cdots (-1)^N\dfrac{p!}{(2N)!} + \sum_{n=N+1}^\infty (-1)^n\dfrac{p!}{(2n)!}
$$
이다 $p! - \cdots+(-1)^N\dfrac{p!}{(2N)!}$ 는 자연수이므로 $\sum$ 으로 묶여 있는 term 도 정수 이어야 한다. $2(N+1)\ge p+1$ 을 이용하면,그런데..
$$
\left|\sum_{n=N+1}^\infty (-1)^n\dfrac{p!}{(2n!)}\right| \le \sum_{n=N+1}^\infty \dfrac{p!}{(2n)!} <\dfrac{1}{p+1} + \dfrac{1}{(p+1)^3}+ \dfrac{1}{(p+1)^5}+\cdots = \dfrac{1/(p+1)}{1-1/(p+1)^2}=\dfrac{p+1}{(p^2+2p)}<\dfrac{1}{p+1}<1 
$$
이므로 이를 만족하는 정수는 $0$ 뿐이다. $a_n = \dfrac{p!}{(2n!)}$ 이라 하면 $\sum [\cdots]$ 부분의 합은 ($a_{N+1}>0$ 으로 놓아도 no loss of generality!),
$$
s=a_{N+1}-a_{N+2}+ (a_{N+3}-a_{N+4})+ \cdots >a_{{N+1}}-a_{N+2}
$$
 이다. 그런데 $a_{N+1}-a_{N+2}>0$ 이므로 $\sum[\cdots]>0$ 이다. 따라서 $\cos 1$ 은 무리수이다.

$\displaystyle \sin 1 = \sum_{n}^\infty \dfrac{(-1)^{n}}{(2n+1)!}$ 도 같은 방법으로 보일 수 있다.



<b>7. </b> 다음 등식을 보이라.
$$
\begin{align}
\sum (-1)^n \dfrac{x^{2n+1}}{(2n+1)!} &= - \sum (-1)^n \dfrac{\left(x+\dfrac{\pi}{2}\right)^{2n}}{(2n)!} \\
&= -\sum (-1)^n \dfrac{(x+\pi)^{2n+1}}{(2n+1)!} \\
&= \sum (-1)^n \dfrac{\left(x+\dfrac{3\pi}{2}\right)^{2n}}{(2n)!} \\
&= \sum (-1)^n \dfrac{(x+2\pi)^{2n+1}}{(2n+1)!}
\end{align}
$$

---

$\sin x = -\cos \left(x+\dfrac{\pi}{2}\right)=- \sin (x+\pi)=\cos\left(x+\dfrac{3\pi}{2}\right) = \sin (x+2\pi)$ 



<b>8. </b> 두번 미분 가능한 함수 $f:\mathbb{R} \to \mathbb{R}$ 이 미분방정식
$$
f''(x)=-f(x),\qquad f(0)=a,\qquad f'(0)=b
$$
를 만족시킨다고 하자. (여기에서 $a$ 와 $b$ 는 주어진 실수이다.)

(1) $g(x):=(f(x)-a\cos x - b\sin x)^2+ (f'(x)+ a\sin x - b \cos x)^2$ 로 두면 
$$
g'(x)=0,\qquad g(0)=0
$$
임을 보이라.

(2) $f(x) = a \cos x + b \sin y$ 임을 보이라. 

(3) 다음을 보이라.
$$
\cos (x+y)= \cos x \cos y - \sin x \sin y,\qquad \sin (x+y)=\sin x \cos y - \cos x \sin y
$$

---

(1) 우선 $g'(x)=0$ for all $x$ 임을 보이자. 
$$
\begin{align}
g'(x) &=2(f'(x) + a \sin x - b \cos x)(f(x)-a\cos x - b \sin x)\\
& \qquad + 2(f''(x)+a \cos x + b \sin x)(f'(x) + a \sin x - b \cos x)\\
&= 0

\end{align}
$$

$$
g(0)=(a-a)^2+(b-b)^2=0
$$
(2) $g'(x)=0$ 이므로 $g(x)$ 는 상수함수이며 $g(0)=0$ 이므로 $g(x)=0$ for all $x\in \mathbb{R}$ 이다. 따라서 $f(x)=a\cos x + b \sin y$ 이며 $f'(x)= - a \sin x + b \cos x$ 이어야 한다. $f(x)$ 를 미분하면 정확히 나오므로 $f(x) = a \cos x + b \sin y$ 이다.

(3) $h(x) := (f(x) - \cos (x+y))^2 + (f'(x)+\sin (x+y))^2$ 이라 하자. 
$$
h'(x) = 2(f'(x)+\sin (x+y))(f(x)-\cos (x+y))+2(f''(x)+\cos (x+y))(f'(x)+ \sin (x+y))=0
$$
이며 $h(0)=(\cos y - \cos y)^2 + (-\sin y + \sin y )^2=0$ 이다. 따라서 $h(x) =0$ for all $x\in \mathbb{R}$ 이다.

즉 $f(x) = \cos (x+y)=\cos x \cos y - \sin x  \sin y$, $- f'(x) = \sin (x+y)=\sin x \cos y + \cos x \sin y$ 이다.



## 연습문제 2 장 5절.



<b>1. </b> 쌍곡 삼각함수 $\cosh x$ 와 $\sinh x$ 는 모두 미분방정식
$$
f''(x)=f(x)
$$
를 만족시킴을 보여라.

----

$$
\begin{align}
(\cosh x)'' &= (\sinh x)' = \cosh x\,,\\
(\sinh x)'' &=(\cosh x)' = \sinh x\;.

\end{align}
$$



<b>2. </b> 쌍곡 탄젠트 함수
$$
\tanh x := \dfrac{\sinh x}{\cosh x}
$$
로 정의한다. 이때
$$
\tanh'x = 1-\tanh^2x = \dfrac{1}{\cosh^2 x}
$$
임을 보이라. 또 쌍곡탄젠트 함수의 그래프를 그리라.

또
$$
\tanh =x - \dfrac{x^3}{3}+ \dfrac{2}{15}x^5 + \cdots
$$
임을 보이라.

----

(1)
$$
\tanh'x = 1-\dfrac{\sinh^2 x}{\cosh^2 x}=\dfrac{1}{\cosh^2 x}
$$
(2) $\displaystyle f(x) = \sum_{n=0}^\infty \dfrac{f^{(n)}(0)}{n!} x^n$ 을 이용한다. $f(0)=0,\, f'(0)=1,\, f''(0)=0,\, f^{(3)}(0)=-2,\,f^{(4)}(0)=0,\,f^{(5)}(0)=16$ 이므로,
$$
\tanh x = x - \dfrac{1}{3}x^3 + \dfrac{2}{15}x^5+\cdots
$$


<b>3. </b> 다음 등식을 보이라.

---

$$
\begin{align}
\sinh x \cosh y + \cosh x \sinh y &=\dfrac{1}{4}\left[(e^x-e^{-x})(e^y+e^{-y})+(e^x+e^{-x})(e^{y}-e^{-y})\right] \\
&=\dfrac{1}{4} \left(e^{x+y}+e^{x-y}-e^{-x+y}-e^{-x-y}+e^{x+y}-e^{x-y}+e^{-x+y}-e^{-x-y}\right)\\
&=\dfrac{1}{4}(2e^{x+y}-2e^{-(x+y)})=\sinh(x+y) \;, \\
\cosh x \cosh y + \sinh x \sinh y &=\dfrac{1}{4} \left[(e^x+e^{-x})(e^{y}+e^{-y}) + (e^x-e^{-x})(e^{y}-e^{-y})\right] \\
&=\dfrac{1}{4} (e^{x+y} + e^{-x+y}+ e^{x-y}+e^{-x-y} + e^{x+y} -e^{x-y}-e^{-x+y}+e^{-x-y})\\
&=\dfrac{1}{4}(2e^{x+y}+2e^{-(x+y)})= \cosh (x+y)\,, \\
\dfrac{\tanh x + \tanh y}{1+\tanh x \tanh y} &= \dfrac{\sinh x \cosh y + \cosh x \sinh y}{ \cosh x \cosh y + \sinh x \sinh y }=\dfrac{\sinh (x+y)}{\cosh (x+h)}=\tanh(x+y)\,,\\
\cosh ^2 x&=\left(\dfrac{e^x+e^{-x}}{2}\right)^2=\dfrac{1}{4} (e^{2x}+e^{-2x}) +1 = \dfrac{1}{2}\cosh 2x +1\,,\\
\sinh^2 x &=\left(\dfrac{e^{x}-e^{-x}}{2}\right)^2 = \dfrac{1}{4} (e^{2x}+e^{-2x})-1 = \dfrac{1}{2}\cosh 2x -1\;.
\end{align}
$$



<b>4. </b> 실수 전체에서 정의된 함수 $f:\mathbb{R}\to \mathbb{R}$ 은 짝함수와 홀함수의 합으로 나타남을 보여라.

---

함수 $f:\mathbb{R}\to \mathbb{R}$ 에 대해 $f_e:\mathbb{R}\to \mathbb{R}$ 와 $f_o: \mathbb{R}\to \mathbb{R}$ 를 다음과 같이 정의한다.
$$
f_e (x):=\dfrac{f(x)+f(-x)}{2},\qquad f_o (x):= \dfrac{f(x)-f(-x)}{2}
$$
이 때 $f_e(-x)=f_e(x)$, $f_o(-x)=-f_o(x)$ 임을 알 수 있다. 이제 $f(x) = f_e(x)+f_o(x)$ 이다. 



<b>5. </b> 홀함수의 도함수는 짝함수이고, 짝함수의 도함수는 홀함수임을 보여라.

---

$$
f_e'(-x)= \lim_{h \to 0} \dfrac{f_e(-x+h)-f_e(-x)}{h} = \lim_{h\to 0} \dfrac{f_e(x-h)-f_e(x)}{h}=-\lim_{h \to 0} \dfrac{f_{e}(x-h)-f_e(x)}{-h}=-f_e'(x)
$$

$$
f_o'(-x) = \lim_{h \to 0}\dfrac{f_o (-x+h)-f_o(-x)}{h}=  \lim_{h \to 0}\dfrac{f_o(x-h)-f_o(x)}{-h}=f'(x)
$$



<b>6. </b> 멱급수 $\mathbf{f}(x) = \sum f_n x^n $ 에서

(i) $\mathbf{f}(x) = \mathbf{f}(-x)$ 이면 
$$
\forall n,\quad f_{2n+1}=0
$$
 을 보이라.

(ii) $\mathbf{f}(x) = - \mathbf{f}(-x)$ 이면
$$
\forall n,\quad f_{2n}=0
$$
임을 보이라.

---

(i) $\mathbf{f}(x) = \dfrac{\mathbf{f}(x)+\mathbf{f}(-x)}{2} = \dfrac{1}{2}\sum f_n (x^n +(-x)^n)=\sum f_{2n}x^{2n}\,.$ 

(ii) $\mathbf{f}(x) = \dfrac{\mathbf{f}(x)-\mathbf{f}(-x)}{2}= \dfrac{1}{2}\sum f_n (x^n - (-x)^n)= \sum f_{2n+1}x^{2n+1}$ 



<b>7. </b> 다음을 보이라.
$$
\begin{align}
A(x) &= \dfrac{x}{\sinh x} = 1 -\dfrac{1}{6}x^2 + \dfrac{7}{360}x^4 + \cdots \\
B(x) &= \dfrac{x}{\tanh x}= 1 + \dfrac{1}{3} x^2 = \dfrac{1}{45}x^4 + \cdots
\end{align}
$$

---

$\displaystyle f(x) = \sum_{n=0}^\infty \dfrac{f^{(n)}(0)}{n!}x^n$ 을 이용한다. 교재에 나온 대로 분모가 $0$ 일 경우는 $0$ 으로 향하는 극한을 취하여 도함수값으로 사용한다.

$A(0)=1,\, A'(0)=0,\,A^{(2)}(0)=\dfrac{1}{3},\, A^{(3)}(0)=0,\,A^{(4)}=\dfrac{1}{15}$

$B(0)=1,\,B'(0)=0,\, B^{(2)}(0)=\dfrac{2}{3},\, B^{(3)}(0)=0,\, B^{(4)}(0)=-\dfrac{8}{15}$ 



<b>8. </b> 좌표평면의 제일사분면에서, 원점과 점 $P=(\cosh t,\, \sinh t)$ 를 잇는 직선의 아래 쪽과 쌍곡선 $x^2-y^2=1$ 의 왼쪽의 공통부분의 넓이는 $t/2$ 임을 보여라.

---

$\cosh^2 t-\sinh^2 t =1$ 을 이용한다.  또한 $2\cosh t \cdot \sinh t= \sinh 2t$ 를 이용한다. $x=\cosh t,\, y=\sinh t$ 에 대해 $y=\sqrt{x^2-1}$ 이므로,
$$
\begin{align}
[\text{Area}]&=\dfrac{1}{2} x\sqrt{x^2-1}-\int_1^x \sqrt{s^2-1}\, ds \\
&\overset{z=\coth s}{=}\dfrac{1}{2}x\sqrt{x^2-1}-\int_0^{\cosh^{-1}x} \sinh^2 z \,dz\\
&= \dfrac{1}{2} \cosh t \cdot \sinh t- \dfrac{1}{2} \int_0^{\cosh^{-1}x} \cosh 2z\, dz +\dfrac{1}{2}\cosh^{-1}x\\
&= \dfrac{1}{2}\cosh t \cdot  \sinh t - \dfrac{1}{4} \left[\sinh 2z\right]_{0}^{\cosh^{-1}x} +\dfrac{1}{2}t\\
&= \dfrac{1}{2}{t}

\end{align}
$$


#### 기본연습문제 6.1.5.

<b>2. </b> 구간 $-1<x<1$ 에서
$$
\dfrac{d}{dx} \arcsin x = \dfrac{1}{\sqrt{1-x^2}}
$$
임을 보이라. 또 $y=\arcsin x$ 의 그래프에서 $x=1/3$ 일 때의 접선의 기울기를 구하라.

---

$y=\arcsin x$ 라 하면 $0 <y <\pi$ 이다. $x=\sin y$ 이며 $\dfrac{dx}{dy}= \cos y$ 이므로 $\dfrac{dy}{dx}=\dfrac{1}{\cos y}=\dfrac{1}{\sqrt{1-x^2}}$ 이다



## 연습문제 2장 6절.

<b>1. </b> $ad-bc\ne 0$ 일 때 함수 $f(x) =\dfrac{ax+b}{cx+d}$ 의 역함수를 구하라.

---

$$
y=\dfrac{ax+b}{cx+d}\implies (cy-a)x=b-dy \implies f^{-1}(x) =\dfrac{b-dx}{cx-a}
$$



<b>2. </b> 단사함수와 그 역함수의 그래프는 직선 $y=x$ 에 대칭임을 보여라.

---

$ (s,\,t)\in \mathbb{R}^2$  일 때 $y=x$ 에 대한 대칭점이 $(t,\,s)$ 임을 보이자. 이 두 점의 중점은 $\left(\dfrac{s+t}{2},\, \dfrac{s+t}{2}\right)$ 이므로 $y=x$ 위에 있다. 또한 점을 잇는 직선의 기울기는 $\dfrac{t-s}{s-t}=-1$ 로 $y=x$ 에 대해 수직이다. 따라서 $(s,\,t)$ 와 $(t,\,x)$ sms $y=x$ 에 서로 대칭이다. 

역함수에 성질에 따라 $(x,\,y)\in f \iff (y,\,x)\in f^{-1}$ 이다.  따라서 함수와 그 역함수의 그래프는 $y=x$ 에 대칭이다. 



<b>3. </b> 단사함수 $y=f(x)$ 와 그 역함수의 그래프가 점 $(x_0,\,y_0)$ 에서 만나면
$$
f(f(x_0))=x_0
$$
임을 보이라.

---

$y_0=f(x_0)$ 이며 $f^{-1}(x_0)=y_0$ 이다. 따라서 $x_0=f(y_0)$ 이다. 즉 $f(f(x_0))=f(y_0)=x_0$. 



<b>4. </b> $\cos x$ 의 정의역을 구간 $[0,\,\pi]$ 에서 제한하면, $\cos x$ 는 순감소 함수이고, 다라서 역함수를 가진다. 이 역함수를 **역코사인 함수** 라고 부르고 $\arccos$ 또는 $\cos^{-1}$ 로 나타낸다. 이 대 $\arccos$ 의 정의역은 $[-1,\,1]$ 이고, $-1<y<1$ 일 때,
$$
\dfrac{d}{dy} (\arccos y) = -\dfrac{1}{\sqrt{1-y^2}}
$$
임을 보이라.

---

$$
x=\arccos y \implies y=\cos x \implies \dfrac{dy}{dx}=-\sin x \implies \dfrac{dx}{dy}=-\dfrac{1}{\sin x} = -\dfrac{1}{\sqrt{1-y^2}}
$$

 

<b>5. </b> 등식
$$
\arccos y = \dfrac{\pi}{2}-\arcsin y \qquad (-1\le y\le 1)
$$
를 보이라.

---

Let $\theta = \arccos y$ and $\phi = \arcsin y$. $y=\cos \theta = \sin \phi$ 인데 우리는 $\sin \phi = \cos \left(\dfrac{\pi}{2}-\phi\right)$ 임을 알고 있으며 따라서 $\theta = \dfrac{\pi}{2}-\phi$ 이다. 



<b>6. </b> 두 집합 $A,\,B$ 사이에 정의된 함수 $f:A\to B$ 와 $g:B \to A$ 에 대하여, 이 두 함수가 서로의 역함수일 필요충분조건은
$$
g \circ f = \operatorname{id}_A,\,\qquad f \circ g = \operatorname{id}_B
$$

임을 보여라. 여기에서 $\operatorname{id}_A:A \to A$ 와 $\operatorname{id}_B:B \to B$ 는 모두 항등사상을 나타낸다.

---

(1) $f^{-1}=g$ 임을 가정하자. 임의의 $a\in A$ 에 대해 $f(a)=b$ 이면 $g(b)=a$ 이므로 $(g \circ f)(a)=g(b)=a$ 이므로 $g\circ f=\operatorname{id}_A$ 이다. 임의의 $b\in B$ 에 대해 $g(b)=a$ 이면 $g^{-1}(a)=f(a)=b$ 이므로 $(f \circ g)(b) = f(a)=b$ 이다. 즉 $f \circ b=\operatorname{id}_B$ 이다.

(2) $g \circ f=\operatorname{id}_A,\, f\circ g= \operatorname{id}_B$ 임을 가정한다. 우선 $f,\,g$ 가 단사임을 보이자. $a_1\in A,\,a_2\in A,\, a_1 \ne a_2$ 에 대해 $f(a_1)=f(a_2) =b$ 라 하자. 그렇다면, 
$$
a_1 = \operatorname{id}_A(a_1 )=(g \circ f)(a_1)=g(b)=(g \circ f)(a_2)=\operatorname{id}_A (a_2)=a_2
$$
이므로 $a_1 \ne a_2$ 라는 가정에 모순. 따라서 $a_1 \ne a_2 \implies f(a_1)\ne f(a_2)$ 이므로 $f$ 는 단사이다. 같은 방법으로 $g$ 가 단사임을 보일 수 있다.

$f$ 가 전사임을 보이자. $f$ 가 전사가 아니라면 어떤 $b\in B$ 에 대하여 $f(a)=b$ 인 $a\in A$ 가 존재하지 않는다. $g(b)=c$ 라 하자. $(f \circ g)(b) = f(c) =b$  이므로 모순. 따라서 $f$ 가 전사이다. 같은 방법으로 $g$ 가 전사임을 보일 수 있다. 결론적으로 $f,\,g$ 는 모두 전단사이다.

$f(a) =b$ 일 때 $g(b) = (g \circ f)(a) = a$ 이다. 또한 $g(d)=c$ 일 때 $(f \circ g)(d)=d=f(c)$ 이다. 즉 $f$ 와 $g$ 는 서로 역함수이다.



<b>7. </b> 임의의 실수 $x$ 에 대하여 등식 $\tan (\arctan x)=x$ 가 성립함을 보이라. 또 $\arctan (\tan x)$ 가 성립하는 구간을 논하라.

---

$\arctan : \mathbb{R} \to \left(-\dfrac{\pi}{2},\, \dfrac{\pi}{2}\right)$ 는 $\tan$ 함수의 역함수 이므로 $\tan (\arctan x)=x$ 이다. $\arctan (\tan x)$ 가 성립하는 구간은 $\left(-\dfrac{\pi}{2},\, \dfrac{\pi}{2}\right) $ 이다. 



<b>8. </b> trivial



<b>9. </b> 쌍곡 사인함수 $y=\sinh x$ 의 역함수는 
$$
x=\sinh^{-1}y = \ln (y+\sqrt{y^2+1})
$$
임을 보이고,
$$
\dfrac{dx}{dy}=\dfrac{1}{\sqrt{y^2+1}}
$$
임을 보이라.

---

$y=\sinh x=\dfrac{e^x-e^{-x}}{2}$ 이며 $e^x=t$ 라 하면,
$$
2y=t-\dfrac{1}{t} \implies t^2-2yt-1=0 \implies t=y \pm \sqrt{y^2+1}
$$
인데 정의상 $t>0$ 이므로 $e^x = t = y+\sqrt{y^2+1}$ 이므로 $x=\ln (y +\sqrt{y^2+1})$ 이다. 또한,
$$
\dfrac{dx}{dy}= \dfrac{1+\dfrac{y}{\sqrt{y^2+1}}}{y+\sqrt{y^2+1}}= \dfrac{1}{\sqrt{y^2+1}}
$$
이다. 



<b>10. </b> 구간 $x>0$ 에서 쌍곡코사인 함수 $y=\cosh x$ 의 역함수는 
$$
x=\cosh^{-1}x = \ln (y+\sqrt{y^2-1})
$$
임을 보이고
$$
\dfrac{dx}{dy}=\dfrac{1}{\sqrt{y^2-1}}
$$
임을 보이라.

---

$y=\cosh x = \dfrac{e^x+e^{-x}}{2}$ 이며 $e^x=t$ 라 하면, 구간 $x>0$ 에서 생각하므로 $t>1$ 이어야 한다.
$$
2y= t+\dfrac{1}{t} \implies t^2 -2yt+1=0 \implies t=y\pm \sqrt{y^2-1}
$$
이다.  $y\ge 1$ 이므로 $-2y+2\le 0$ 이다. $y-\sqrt{y^2-1}\le y-\sqrt{y^2-1-2y+2}=y-(y-1)=1$ 이므로 $t>1$ 조건에 위배된다. 따라서 $t=y +\sqrt{y^2-1} = e^x$ 이므로 $x=\ln (y+\sqrt{y^2-1})$ 이다. 또한,
$$
\dfrac{dx}{dy}= \dfrac{1+\dfrac{y}{\sqrt{y^2-1}}}{y+\sqrt{y^2-1}}=\dfrac{1}{\sqrt{y^2-1}}
$$
이다.



<b>11. </b> 다음 등식을 보이라.
$$
\begin{align}
\sinh (\cosh ^{-1} x) &= \sqrt{x^2-1} \qquad (x>1)\\
\cosh(\sinh^{-1}y) &= \sqrt{1+y^2}
\end{align}
$$

---

$$
\begin{align}
\sinh (\cosh^{-1}x) &= \dfrac{x+\sqrt{x^2-1} - \dfrac{1}{x+\sqrt{x^2-1}}}{2} \\
=&\dfrac{x^2+x^2-1+2x\sqrt{x^2-1}-1}{2(x+\sqrt{x^2-1})}\\
&=\dfrac{x^2+x\sqrt{x^2-1}-1}{x+\sqrt{x^2-1}}\\
&=x-\dfrac{1}{x+\sqrt{x^2-1}}=x-(x-\sqrt{x^2-1})=\sqrt{x^2-1}\\
\cosh (\sinh^{-1}y) &= \dfrac{y+\sqrt{y^2+1}+\dfrac{1}{y+\sqrt{y^2+1}}}{2} \\
&=\dfrac{y^2+y^2+1+2y\sqrt{y^2+1}+1}{2(y+\sqrt{y^2+1})}\\
&= \dfrac{y^2+1 + y\sqrt{y^2+1}}{y+\sqrt{y^2+1}} \\
&=y+\dfrac{1}{y+\sqrt{y^2+1}}=y+(\sqrt{y^2+1}-y)=\sqrt{y^2+1}

\end{align}
$$



<b>12. </b> 다음 극한을 구하라.
$$
\lim_{x \to 0} \dfrac{\sin x - \arctan x}{x^2 \ln (1+x)}
$$


---

분자와 분모를 각각 우리가 아는 멱급수로 전개를 하면,
$$
\begin{align}
\sin x - \arctan x &= \left(x-\dfrac{1}{3!}x^3 +\dfrac{1}{5!}x^5 +\cdots\right)-\left(x-\dfrac{1}{3}x+\dfrac{1}{5}x^3 + \cdots\right)=\dfrac{1}{6}x^3-\dfrac{23}{120}x^5 + \cdots\\
x^2 \ln (1+x) & = x^3- \dfrac{1}{2}x^4 + \dfrac{1}{3}x^5 + \cdots
\end{align}
$$
이다. 따라서 $\sin x -\arctan x= \dfrac{1}{6}x^3 u(x)$ 를 만족하는 멱급수 $u(x)$ 가 존재하며 $u(0)=1$ 이다. 또한 $x^2\ln(1+x)=x^3 v(x)$ 를 만족하는 멱급수 $v(x)$ 가 존재하며 $v(0)$=1$ 이다. 따라서,
$$
\lim_{x \to 0} \dfrac{\sin x - \arctan x}{x^2 \ln (1+x)}=\lim_{x \to 0}\dfrac{u(x)}{6 v(x)}=\dfrac{1}{6}
$$
이다.



<b>13. </b> 연속함수 $f$ 가 모든 실수 $x$ 에 대하여
$$
(\exp x -1)f(x) = x
$$
를 만족시킬 때 다음 물음에 답하라.

(1) $f(0)$ 의 값을 구하라.

(2) 미분계수 $f'(0)$ 의 값을 구하라.

(3) $f$ 는 일대일 함수임을 밝히라.

(4) 함수 $f$ 의 역함수를 $g$ 라고 할 때, 미분계수 $g'(1)$ 의 값을 구하라.

---

(1) $f$ 가 연속함수 이므로 $\displaystyle f(0)= \lim_{x \to 0}\dfrac{x}{\exp x-1}=1$ 이다. 

(2)  $\exp x = e^x$ 라 쓴다. $f(x) = \dfrac{x}{e^x-1}$ 이며, 
$$
\begin{align}
f'(0) &= \lim_{h \to 0} \dfrac{f(h)-f(0)}{h}=\lim_{h \to 0} \dfrac{\dfrac{h}{e^h-1}-1}{h} =\lim_{h \to 0} \dfrac{h-e^h+1}{h(e^h-1)}

\end{align}
$$
이다. $e^h = 1 + h + \dfrac{h^2}{2} u(h)$ , $u(0)=1$ 이므로,
$$
f'(0)=\lim_{h \to 0} \dfrac{-h^2 u(h)}{2h(h+\dfrac{h^2}{2} u(h))}=\lim_{h \to 0}\dfrac{-u(h)}{2+hu(h)}=-\dfrac{1}{2}
$$
(3) $f'(x)$ 를 구하면,
$$
f'(x) = \dfrac{1}{e^x-1}-\dfrac{xe^x}{(e^x-1)^2}=\dfrac{e^x-1-xe^x}{(e^x-1)^2}
$$
이다. 이 때 분자를 $g(x)$ 라 하면 $g(x)=e^x-1-xe^x$ 이다. $g'(x) = e^x-e^x-xe^x=-xe^x$ 이므로 $x=0$ 일 대 극값을 갖는다. $g(0)= 0$ 이며 $\displaystyle \lim_{x \to -\infty}g(x)=-1,\,\lim_{x \to \infty} g(x)=-\infty$ 이므로 최대값이 $0$ 이고 따라서 $g(x)\le 0$ and $g(x)=0 \iff x=0$ 이다. 따라서 $f'(x)\le 0 \iff x=0$ 이다. 즉 $f(x)$ 는 단조감소함수이며 $x=0$ 일 때에만 극값을 가진다. 따라서 $f$ 는 일대일 함수이다.

(4) $\dfrac{dg}{dy}=\dfrac{1}{df/dx}$ 이며 $g(1)=f^{-1}(1)=0$ 이므로 $g'(1)=-2$ 이다. 



<b>14. </b> 함수 $f(x)=3x+\cos x$ 는 모든 실수 $y$ 에 대하여 역함수 $g(y)$ 가 정의됨을 설명하고, 이 대 미분계수 $g'(1)$ 과 $g''(1)$ 을 구하라. 

---

(1) $f'(x)= 3-\sin x >0$ 이므로 $f$ 는 단조증가 함수. $\displaystyle \lim_{x \to \infty} f(x)=-\infty,\,\lim_{x \to \infty} f(x)=\infty$ 이므로 $f$ 는 실수 전체에서 정의된 전단사함수이다. 따라서 모든 실수 $y$ 에 대해 역함수 $g(y)$ 가 정의된다.

(2) $f'(x)=3-\sin x,\,f(0)=1$  이다. $g'(1)=\dfrac{1}{f'(0)}=\dfrac{1}{3}$ , 

(3) 합성함수의 미분을 생각하자. $x=g(f(x))$ 이므로 $1=f'(x)g'(f(x))$ 이며,
$$
0=f''(x)g'(f(x))+(f'(x))^2g''(f(x))
$$
이므로,
$$
0=f''(0)g'(f(0))+(f'(0))g''(f(0))=-\dfrac{1}{3}+9 g''(1) \implies g''(1)=\dfrac{1}{27}
$$


<b>15. </b> 열린 구간 $I_1$ 과 $I_2$ 사이으 전단사 함수 $f: I_1 \to I_2$ 가 두번 미분 가능하고, 모든 $x\in I_1$ 에 대하여 $f'(x)\ne 0$ 이라고 하자. 이 때 $y=f(x)$ 의 역함수 $x=g(y)$ 도 두번 미분 가능하고 
$$
g''(y)=-\dfrac{f''(x)}{(f'(x))^3}
$$
임을 보이라. 또 $f(x)$ 가 세번 미분 가능하면 역함수 $g(y)$ 도 세번 미분 가능하고,
$$
g'''(y) = \dfrac{3(f''(x))^2-f'''(x) f'(x)}{(f'(x))^5}
$$
임을 보이라. 일반적으로 $f(x)$ 가 $n$ 번 미분 가능하면 $g(y)$ 도 $n$ 번 미분 가능함을 보이라.

---

(1) 14. 에서 보았듯이 $g''(y)=-\dfrac{f''(x) g'(f(x))}{(f'(x))^2}= \dfrac{f''(x)}{(f'(x))^3}$ because $g'(f(x))=\dfrac{1}{f'(x)}$ . 

(2) 14. 의 풀이 (3) 의 식을 다시 한번 미분하면,
$$
\begin{align}
0&=f'''(x)g'(f(x))+f''(x)f'(x)g''(f(x))+2f''(x)f(x)g''(f(x))+(f'(x))^3g'''(f(x))\\
&=f'''(x)g'(f(x))+3f'(x)f''(x)g''(f(x))+(f'(x))^3 g'''(f(x))

\end{align}
$$
 이므로,
$$
\begin{align}
g'''(x)=-\dfrac{1}{(f'(x))^3} \left(\dfrac{f'''(x)}{f'(x)}-\dfrac{3(f''(x))^2}{(f'(x))^2}\right)=\dfrac{ 3(f''(x))^2- f'(x)f'''(x)}{(f'(x))^5}

\end{align}
$$
(3) $f$ 가 $n$ 번 미분 가능하고 $m\le n$ 인 모든 자연수 $m$ 에 대하여 $f^{(m)}(x) \ne 0$ 이라 하자. $f$ 의 역함수 $g$ 를 생각 할 때 $g^{(n)}(y)$ 가 $f,\,f',\cdots,\, f^{(n)}$ 의 합과 곱으로 이루어진 함수를 $(f'(x))^{2n+1}$ 으로 나눈 함수임을 보이자. 즉, $F(f,\,f',\ldots,\,f^{(n)})$ 을 $f,\,f',\ldots,\,f^{(n)}$ 의 임의의 합과 곱으로 이루어진 함수라고 하면 $\dfrac{dF}{dx}$ 는 $f,\,f',\ldots,\,f^{(n+1)}$ 의 합과 곱으로 이루어진 함수이다. 이를 $G(f,\,\ldots,\,f^{(n+1)})$ 이라 하자. 
$$
\begin{align}
g^{(n)}(f(x)) &= \dfrac{F(f(x),\,f'(x),\ldots,\,f^{(n)})}{(f'(x))^{2n+1}}\\
\implies f'(x)g^{(n+1)}(x) &=\dfrac{f'(x)F(f(x),\ldots,\,f^{(n)}) -(2n+1)G(f,\ldots,\,f^{(n+1)})}{(f'(x))^{2n+2}} \\
\implies g'^{(n+1)}(x) &= \dfrac{f'(x)F(f(x),\ldots,\,f^{(n)}) -(2n+1)G(f,\ldots,\,f^{(n+1)})}{(f'(x))^{2n+3}} 
\end{align}
$$


<b>16. </b> 함수 $f(x)=e^x +\ln x$ 의 역함수를 $g(y)$ 라고 할 때 $y=e$ 에서의 미분계수 $g'(e)$ 를 구하라. 또 이계미분계수 $g''(e)$ 를 구하라.

---

$f'(x) = e^x+\dfrac{1}{x}>0$ 이므로 $f'(x)$ 는 단조증가함수이다. 따라서 역함수가 존재한다. $f(1)=e$ 이므로,
$$
g'(e) = \dfrac{1}{f'(1)}=\dfrac{1}{e+1}
$$
$f''(x) = e^x-\dfrac{1}{x^2}$ 이므로 $f''(1) =e-1>0$ 이다. 따라서,
$$
g''(e) = -\dfrac{f''(1)}{(f'(1))^3}=-\dfrac{e-1}{(e+1)^3}
$$


<b>17. </b> 최근 10년간의 통계자료를 분석하여 보았더니 어떤 곡물의 연간 생산량 $y$ 와 경작과정에서 사용하는 비료의 양 $x$ 가 다음 관계가 있다는 것을 알았다. : $y=2x^3+3x^2+4x+4$. 이 곡물의 금년 생산량이 $40$ 이라 하자. 내년에 생산량을 $1%$ 증가시키려면 금년보다 비료를 몇 % 정도 더 많이 사용하여야 하는가?

---

$y'=6x^2+6x+4$ 이며 $y'>0$ 임은 쉽게 보일 수 있다. 따라서 $y$ 는 단조증가함수이다. $y=40$ 를 만족하는 $x=2$ 이다. 
$$
\Delta y = \dfrac{dy}{dx}\Delta x \implies 0.4=40\times \Delta x \implies \Delta x =0.01
$$

$$
\% = \dfrac{2.01-2}{2}\times 100 = 0.5 \%
$$



<b>18. </b> 구간 $\left[-\dfrac{1}{2},\, \dfrac{1}{2}\right]$ 에서 연속인 함수 $f(x)$ 가 식
$$
\arcsin 2x = xf(x)
$$
를 만족시킬 때 $f(0)$ 를 구하라.

---

양변을 $x$ 에 대해 미분하면,
$$
\dfrac{2}{\sqrt{1-4x^2}}=f(x)+xf'(x)
$$
이로 $2=f(0)$. 



<b>19. </b> 함수 $y=\tanh x$ 의 역함수를 $x=\tanh^{-1}y$ 로 두었을 때,
$$
\tanh^{-1}y=\dfrac{1}{2}\ln \left(\dfrac{1+y}{1-y}\right) = y+\dfrac{y^3}{3}+\dfrac{y^5}{5} + \cdots \qquad(|y|<1)
$$
임을 보이라. 이 식에서
$$
\dfrac{d}{dy}\left(\tanh^{-1} y\right) = \dfrac{1}{1-y^2} \tag{2.4}
$$
 임을 보이라. 또
$$
\dfrac{d}{dx}\tanh x = 1-\tanh^2 x
$$
을 이용하여 (2.4) 를 보이라.

----

(1) $y=\tanh x = \dfrac{e^x-e^{-x}}{e^x+e^{-x}}$ 이다. $(e^{2x}+1)y=e^{2x}-1$ 이므로 $(y-1)e^{2x}=-(y+1) \implies x= \dfrac{1}{2}\ln \left(\dfrac{1+y}{1-y}\right)$ 이다. 

연습문제 2.2.4 에서 $\displaystyle \ln \left(\dfrac{1+y}{1-y}\right)= \sum_{n=1}^\infty \dfrac{y^{2n-1}}{2n-1}$ 임을 보았다. 

(2)  이로부터,
$$
\dfrac{d}{dy} \left(\tanh^{-1} y\right)= \sum_{n=1}^\infty y^{2n-2}=\dfrac{1}{1-y^2}
$$
(3) 
$$
\dfrac{d \tanh^{-1}y}{dy}=\dfrac{1}{\dfrac{d}{dx}\tanh x}=\dfrac{1}{1-\tanh^2x}=\dfrac{1}{1-y^2}
$$
