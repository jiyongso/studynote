IV. 테일러 전개 #1
===



## 제 1 절. 코시의 평균값 정리



#### 1.0.1 기본연습문제

1. 평균값 정리를 이용하여 미분계수가 항등적으로 $0$ 인 함수는 상수함수임을 증명하라.
2. 미분가능한 함수 $f:[a,\,b]\to \mathbb{R}$ 에 대하여 점 $(a,\,f(a))$ 와 점 $(b,\,f(b))$ 를 지나는 직선의 방정식을 $y=l(x)$ 라 하자. 이 때 $|l(x)-f(x)|$ 가 최대가 되는 점 $c$ 에서 $f'(c)=\dfrac{f(b)-f(a)}{b-a}$ 임을 보이라. 만약 $f$ 가 이차함수이면 $c=\dfrac{a+b}{2}$ 임을 보이라.
3. 미분가능한 함수 $f:\mathbb{R}\to \mathbb{R}$ 이 $f(0)=1$ 이고, 임의의 $x$ 에 대하여 $f'(x)\le 0.2$ 이면 $f(5)\le 2$ 임을 보이라.
4. 현재 어떤 집값이 1억원이고, 앞으로 순간 물가 증가율이 $0.2$ (억원/년) 을 넘지 않는다면 5년 후에 이 집값은 2억원을 넘지 않음을 보이라.

---

1. 임의의 구간 $(a,\,b)$ 에 대해서 $f(b)\ne f(a)$ 라면 $0 \ne \dfrac{f(b)-f(a)}{b-a}=f'(c)$ 인 $c\in (a,\,b)$ 가 존재해야 한다. 이는 미분계수가 항등적으로 $0$ 이라는 가정에 위배된다. 따라서 $f$ 는 상수함수이다.
2. $l(x) = \dfrac{f(b)-f(a)}{b-a} (x-a)+f(a)$ 이다. $s(x)=|l(x)-f(x)|^2$ 라 하자.  $f$ 가 상수함수이면 자명하므로 $f$ 가 상수함수가 아닐 경우만 생각하자. $s(a)=s(b)=0$ 이며 $s(x)\ge 0$ 이므로,  $s (x)$ 가 최대가 되는 $c$ 에서 $s'(x)=0 \implies l(c)=f(c)$ or $l'(x)=f'(x)$ 이다. $l(c)=f(c)$ 이면 $s(c)=0$ 이므로 최대값이 아니다. $f'(c)=l'(c) = \dfrac{f(b)-f(a)}{b-a}$ 일 때 이다. 

3. $f(x)-f(0)=f'(c) (x-0) \le 0.2 x$ 이므로 $f(5)\le 2$ 이다.
4. 3. 에 의해 자명.



#### 연습문제 : 제 3장 2절

<b>1. </b> 다음 극한을 구하라.

---

(1)  $ \displaystyle \lim_{x \to 0}\dfrac{1-\cos x}{x^2}=\lim_{x \to 0}\dfrac{\sin x}{2x} = \lim_{x \to 0}\dfrac{\cos x}{2}=\dfrac{1}{2}$

(2) $\displaystyle \lim_{x \to 0}\dfrac{e^x-1-x}{x^2}=\lim_{x \to 0}\dfrac{e^x-1}{2x}=\lim_{x\to 0}\dfrac{e^x}{2}=\dfrac{1}{2}$

(3)  $\displaystyle \lim_{x\to 0} \dfrac{x-\tan x}{x-\sin x} = \lim_{x \to 0}\dfrac{1-\dfrac{1}{\cos^2 x}}{1-\cos x}= \lim_{x \to 0} \dfrac{-\dfrac{2 \sin x}{\cos^3 x}}{ \sin x}=-2$

(4) $\displaystyle \lim_{x \to 0} \dfrac{e^x-e^{-x}}{\sin x}=\lim_{x \to 0}\dfrac{e^x+e^{-x}}{\cos x}=2$ 

(5) $\displaystyle \lim_{x \to 0} \dfrac{e^x-1}{\ln (1+x)} = \lim_{x \to 0} e^x (1+x)=1$

(6) $\displaystyle \lim_{x \to 0} (e^x+x)^{1/x}=\lim_{x \to 0} e^{\frac{1}{x}{\ln (e^x+x)}}=\lim_{x \to 0} \exp \left(\dfrac{e^x+1}{e^x+x}\right)=e^2$ 

(7) $\displaystyle \lim_{x \to 0} \left(\dfrac{1}{\sin x}-\dfrac{1}{x}\right) = \lim_{x \to 0} \dfrac{x-\sin x}{x\sin x}= \lim_{x \to 0}\dfrac{1-\cos x}{\sin x +x\cos x}=\lim_{x \to 0}\dfrac{\sin x}{\cos x -x\sin x+\cos x}=0$

(8) $\displaystyle \lim_{x \to 0} \dfrac{\tan x-\sin x}{x^3}= \lim_{x \to 0}\dfrac{\sin x - \sin x \cos x}{x^3 \cos x} = \lim_{x\to 0}\dfrac{\cos x-\cos^2 x+ \sin ^2 x}{3x^2 \cos x - x^3 \sin x}= \cdots =\lim_{x \to 0} \dfrac{-\sin x + 4 \sin x \cos x}{6 \cos x + x(\cdots)}=\dfrac{1}{2}$

(9) $\displaystyle \lim_{x \searrow 0} \sin x \ln x= \lim_{x \searrow 0 } \dfrac{\ln x}{1/\sin x}= \lim_{x \searrow 0}\dfrac{1/x}{\cos x/\sin^2 x}= \lim_{x \searrow 0}\dfrac{\sin ^2 x}{x\cos x}= \lim_{x \searrow 0 }\dfrac{2\sin x \cos x}{\cos x+x\sin x}=0$ 

(10) $\displaystyle \lim_{x \searrow 0} \sqrt{x}\ln x = \lim_{x \searrow 0}\dfrac{\ln x}{1/\sqrt{x}}=\lim_{x \searrow 0} \dfrac{1/x}{-1/2x^{3/2}} = \lim_{x \searrow 0}\left[-2\sqrt{x}\right]=0$ 

(11)  $\displaystyle \lim_{x \searrow 0} x^a \ln x\;(a>0)= \lim_{x \searrow 0}\dfrac{\ln x}{x^{-a}}=\lim_{x \searrow 0} \dfrac{x^{-1}}{-ax^{-a-1}}=\lim_{x\searrow 0}\dfrac{1}{-a} x^a=0$

(12) $\displaystyle \lim_{x \searrow 0} x^x = \lim_{x \searrow 0} e^{x \ln x} = \lim_{x \searrow 0} \exp \left(\dfrac{1/x}{-1/x^2}\right) = \lim_{x \searrow 0}e^{-x}=1$  

(13) $\displaystyle \lim_{x \searrow 0} x^{\sin x}= \lim_{x \searrow 0 } \exp \left(\sin x \ln x\right)=1$ (see (9))

(14) $ \displaystyle \lim_{x \searrow 0} \dfrac{\sqrt{x}}{\sqrt{x} + \sin \sqrt{x}}= \lim_{x \searrow 0} =\dfrac{1/\sqrt{x}}{1/\sqrt{x} +1/\sqrt{x} \cos \sqrt{x}}=\dfrac{1}{2}$



<b>2. </b> 구간 $I$ 에서 두번 미분 가능한 함수 $f$ 에 대하여
$$
f''(x) = 2\lim_{h \to 0} \dfrac{f(x+h) -f(x) - f'(x)h}{h^2}\,,\qquad x\in I
$$
이 성립함을 보이라.

---

$$
\begin{align}
\lim_{h \to 0} \dfrac{f(x+h) -f(x) - f'(x)h}{h^2} &=\lim_{h \to 0}\dfrac{f'(x+h)-f'(x)}{2h}=\dfrac{f''(x)}{2}
\end{align}
$$



<b>3. </b> 열린 구간 $I$ 에서 두 번 미분가능한 함수 $f(x)$ 를 생각하자. 이 때 $x=a\in I$ 가 $f(x)$ 의 임계점(critical point), 즉 $f'(a)=0$ 이라고 하자.

(1) 만약 $f''(a)>0$ 이면 $x=a$ 는 $f(x)$ 의 극소점 임을 보여라.

(2) 만약 $f''(a)<0$ 이면 $x=a$ 는 $f(x)$ 의 극대점 임을 보여라.

---

(1) $f''(a)>0$ 이면 $a$ 를 포함하는 어떤 열린 구간 $I_a$ 에 대해 $x\in I_a \implies f''(x)>0$ 임을 생각 할 수 있다. $x_1,\,x_2 \in I_a$ 이고 $x_1<x_2$ 이면 $f'(x_1) < f'(x_2)$ 이다. $x\in I_a$ 에 대해 $x>a$ 라 하자.  평균값정리에 의해 다음을 만족하는 $y\in (a,\,x)$ 가 존재한다. 
$$
f(x)-f(a)=(x-a)f'(y)
$$
여기서 $f'(y)-f'(a)=f'(y)=(y-a)f''(z)$ 를 만족하는 $z\in (a,\,y)$ 가 존재하므로 $f'(y) = (y-a)f''(z)>0$ 이며 $(x-a)>0$ 이므로 이 구간 $I_a$  에서의 임의의 $x>a$ 에 대해 $f(x)-f(a)>0$ 이다.

$x<a$ 일 경우도 마찬가지로 $f(x)-f(a)>0$ 임을 보일 수 있다. 따라서 $x=a$ 는 $f(x)$ 의 극소점이다.



(2) (1) 의 방법대로 하면 쉽게 보일 수 있다.



<b>4. </b> (**로피탈의 정리**) 구간 $(a,\,\infty)$ 에서 정의된 두 미분가능한 함수 $f,\,g$ 에 대하여 극한값 $l:=\displaystyle \lim_{x \to \infty} \dfrac{f'(x)}{g'(x)}$ 이 존재한다고 하자. 이제 

(i) $\displaystyle \lim_{x \to \infty} f(x) = \lim_{x \to \infty} g(x) =0$ 

이거나, 또는

(ii) $\displaystyle \lim_{x \to \infty} f(x) = \lim_{x \to \infty} g(x) = \infty$

이면,
$$
\lim_{x \to \infty} \dfrac{f(x)}{g(x)}= \lim_{x \to \infty} \dfrac{f'(x)}{g'(x)}
$$
임을 보이라.

---

$y=1/x$ 라 놓으면 $\displaystyle \lim_{x \to \infty}f(x)=\lim_{y \searrow 0}f(1/y)$ 임을 안다. 
$$
\lim_{x \to \infty} \dfrac{f(x)}{g(x)}= \lim_{y\searrow 0} \dfrac{f(1/y)}{g(1/y)} = \lim_{y\searrow 0} \dfrac{(-1/y^2)f'(1/y)}{(-1/y^2)g'(1/y)}=\lim_{y \searrow 0} \dfrac{f'(1/y)}{g'(1/y)}=l
$$


<b>5. </b> 로피탈의 정리를 이용하여 $\displaystyle \lim_{n \to \infty} n^{1/n}=1$ 임을 보이라.
$$
\lim_{n \to \infty} n ^{1/n}=\lim_{n \to \infty} e^{\frac{1}{n} \ln n}=\lim_{n \to \infty}e^{1/n}=1
$$




<b>6. </b> 로피탈의 정리를 이용하여 다음을 보이라.
$$
\lim_{x \to \infty} \dfrac{x}{e^x}=0\,,\qquad \lim_{x \to \infty}\dfrac{x^2}{e^x}=0\;.
$$
일반적으로 임의의 다항식 $p(x)$ 에 대하여
$$
\lim_{x \to \infty} \dfrac{p(x)}{e^x}=0
$$
임을 보이라.

----

$$
\begin{align}
\lim_{x \to \infty} \dfrac{x}{e^x} = \lim_{x \to \infty} \dfrac{1}{e^x}=0\,,\\
\lim_{x \to \infty} \dfrac{x^2}{e^x} = \lim_{x \to \infty}\dfrac{2x}{e^x }=0\,.

\end{align}
$$

$p(x)$ 가 $n$ 차 다항식일 때 분자 분모를 각각 $n+1$ 번 미분하면 $\lim_{x \to \infty} \dfrac{0}{e^x}$ 꼴이 되므로 그 극한이 $0$ 이다.



<b>7. </b> 다음을 보이라.
$$
\lim_{x \to \infty} \dfrac{\ln x}{x}=0,\qquad \lim_{x \to\infty}\dfrac{\ln x}{\sqrt{x}}=0\;.
$$
일반적으로 임의의 자연수 $n$ 에 대하여 $\displaystyle \lim_{x \to \infty} \dfrac{\ln x}{\sqrt[n]{x}} =0$ 임을 보이라.

---


$$
\begin{align}
\lim_{x \to \infty}\dfrac{\ln x}{x} &= \lim_{x \to \infty}\dfrac{1/x}{1}=0\;.\\
\lim_{x \to \infty}\dfrac{\ln x}{\sqrt{x}} &= \lim_{x \to \infty} \dfrac{1/x}{(1/2)x^{-1/2}}=\lim_{x \to \infty}\dfrac{2}{\sqrt{x}}=0\;,\\
\lim_{x \to \infty}\dfrac{\ln x}{x^{1/n}} &= \lim_{x\to \infty}\dfrac{1/x}{(1/n)x^{(1/n-1)}} = \lim_{x \to \infty} \dfrac{n}{x^{1/n}}=0\;.

\end{align}
$$


<b>8. </b> $0$ 이상인 임의의 실수 $a,\,b,\,c$ 에 대하여

(1) $\displaystyle \lim_{n \to \infty} \left( \dfrac{a^{1/n}+b^{1/n}}2{}\right)^{n}=\sqrt{ab}$

(2) $\displaystyle \lim_{n\to \infty} \left(\dfrac{a^{1/n}+b^{1/n}+c^{1/n}}{3}\right)^n = \sqrt[3]{abc}$

이 성립함을 보이라.

---

(1) 좌변에 log를 취하면, $\displaystyle \ln \left[\left(\dfrac{a^{1/n}+b^{1/n}}{2}\right)^n\right] =n  \ln\left(\dfrac{a^{1/n}+b^{1/n}}{2}\right)= \dfrac{\ln(a^{1/n}+b^{1/n})-\ln{2}}{1/n}$
$$
\lim_{n \to \infty}\dfrac{\ln(a^{1/n}+b^{1/n})-\ln{2}}{1/n}= \lim_{n \to \infty}  \dfrac{1/n^2 (\ln a+\ln b) \dfrac{1}{a^{1/n}+b^{1/n}}}{1/n^2} = \dfrac{\ln (ab)}{2}=\ln \sqrt{ab}
$$


(2) 역시 좌변에 log 를 취하면 (1) 과 같은 방법으로 쉽게 구할 수 있다.



<b>9. </b> 자연수 $n$ 에 대하여, 구간 $I$ 에서 정의된 $n$ 번 미분 가능한 함수 $f(x)$ 에 대하여
$$
\dfrac{f^{(n)}(x)}{n!}=\lim_{h \to 0}\dfrac{\displaystyle f(x+h)-\sum_{k=0}^{n-1}\dfrac{f^{(k)}(x)}{k!} h^k}{h^n}\,,\qquad \forall x \in I
$$
을 보이라.

---

좌번의 $h \to 0$ 극한에서 분자와 분모가 모두 $0$ 으로 수렴한다. 분자 분모를 모두 $h$ 에 대하여 $n$ 번 미분하면, 분모의 $\displaystyle \sum_{k=0} ^{n-1}\cdots$ 은 $h$ 의 $n-1$ 차 다항식이므로 $n$ 번 미분에 사라진다. 따라서,  
$$
\lim_{h \to 0}\dfrac{\displaystyle f(x+h)-\sum_{k=0}^{n-1}\dfrac{f^{(k)}(x)}{k!} h^k}{h^n} = \lim_{h \to 0} \dfrac{f^{(n)}(x+h)}{n!} = \dfrac{f^{(n)}(x)}{n!}
$$
이다.



<b>10. </b> 다음 극한을 구하라.

---

(1) $\displaystyle \lim_{n \to \infty} \dfrac{1}{\sqrt{n}} \left(1+\dfrac{1}{2}+ \cdots +\dfrac{1}{2n-1}+\dfrac{1}{2n}\right)$ 

우리는 $\dfrac{1}{2}+\dfrac{1}{3} + \cdots+ \dfrac{1}{n} <\ln n < 1+\dfrac{1}{2}+ \cdots + \dfrac{1}{n}$ 임을 알고 있다. 따라서 $\left(1+\dfrac{1}{2}+ \cdots +\dfrac{1}{2n-1}+\dfrac{1}{2n}\right) > \ln (2n+1)$ 이다.
$$
0\le \displaystyle \lim_{n \to \infty} \dfrac{1}{\sqrt{n}} \left(1+\dfrac{1}{2}+ \cdots +\dfrac{1}{2n-1}+\dfrac{1}{2n}\right) \le \lim _{n \to \infty}\dfrac{\ln (2n+1)}{\sqrt{n}} = \lim_{n \to \infty} \dfrac{2/(2n+1)}{\dfrac{1}{2\sqrt{n}} }=\lim_{n \to \infty} \dfrac{4\sqrt{n}}{2n+1}=0\;.
$$
이므로 극한값은 $0$ 이다. 

(2) $\displaystyle \lim_{n \to \infty} \dfrac{1}{n} \left(1+\dfrac{1}{2} + \cdots + \dfrac{1}{3n-1}+\dfrac{1}{3n}\right)^2$ 

역시 $\left(1+\dfrac{1}{2} + \cdots + \dfrac{1}{3n-1}+\dfrac{1}{3n}\right) > \ln (3n+1)$ 이므로,
$$
\lim_{n \to \infty} \dfrac{1}{n} \left(1+\dfrac{1}{2} + \cdots + \dfrac{1}{3n-1}+\dfrac{1}{3n}\right)^2 \le \lim_{n \to \infty}\dfrac{(\ln (3n+1))^2}{n} = \lim_{n \to \infty} \dfrac{6 \cdot \ln (3n+1)}{3n+1}=0
$$


(3) $\displaystyle \lim_{n \to \infty} \dfrac{1}{n}\left(1+\dfrac{1}{2} + \cdots + \dfrac{1}{4n-1}+\dfrac{1}{4n}\right)^5$ 

역시 $\left(1+\dfrac{1}{2} + \cdots + \dfrac{1}{4n-1}+\dfrac{1}{4n}\right) > \ln (4n+1)$ 이므로,
$$
\begin{align}
\lim_{n \to \infty} \dfrac{1}{n} \left(1+\dfrac{1}{2} + \cdots + \dfrac{1}{4n-1}+\dfrac{1}{4n}\right)^5  
&\le \lim_{n \to \infty}\dfrac{(\ln (4n+1))^5}{n}  \\
&= \lim_{n \to \infty} \dfrac{20 \cdot (\ln (4n+1))^4}{4n+1} \\
&=\lim_{n \to\infty} \dfrac{20 \cdot 4 \cdot 4 (\ln (4n+1))^3}{4(4n+1)}=\lim_{n\to \infty} \dfrac{80 (\ln (4n+1))^3}{4n+1} \\
&=\lim_{n \to\infty} \dfrac{80 \cdot 4 \cdot 3 (\ln (4n+1))^2}{4\cdot (4n+1)}= \lim_{n \to \infty} \dfrac{240 \cdot (\ln (4n+1))^2}{4n+1} \\
&= \lim_{n \to \infty} \dfrac{240 \cdot 4 \cdot 2 (\ln (4n+1))}{4\cdot(4n+1)} = \lim_{n \to \infty}\dfrac{ 480 \cdot \ln (4n+1)}{4n+1}=0\;.


\end{align}
$$


