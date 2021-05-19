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





## 연습문제 3절

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
B(0)= \lim_{x\to 0} \dfrac{x}{e^x}=1
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

