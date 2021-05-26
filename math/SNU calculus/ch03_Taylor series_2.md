IV. 테일러 전개 #2
===



## 연습문제 : 제 3 장 3 절



<b>1. </b> 원점 근방에서 정의된 함수 $f(x)$ 와 $g(x)$ 가 모두 $o(x^k)$ 이면 $f(x)+g(x)$ 도 $o(x^k)$ 임을 보이라. 또 임의의 실수 $c$ 에 대하여 $cf(x)$ 오 $o(x^k)$ 임을 보이라.

---

$f^{(n)}(0)=g^{(n)}(0)=0$ for $n=0,\ldots,\,n$ 이므로 $(cf+g)^{(n)}(0)=0$ for any constant $c$. 



<b>2. </b> 두 일차 다항삼수 $l_1(x)$ 와 $l_2(x)$ 의 차가 $o(x)$ 이면 $l_1(x)=l_2(x)$ 임을 보이라.

---

let $l_1(x) = a_1 x +b_1,\, l_2(x) = a_2 x+b_2$. $l_1(x)-l_2 (x)=o(x)$ 이므로 $l_1 (0)=l_2 (0)\implies b_1=b_2$, ${l_1}'(0)={l_2}'(0)=0 \implies a_1=a_2$. 



<b>3. </b> 두 $n$ 차 다항함수 $p_1(x)$ 와 $p_2(x)$ 의 차가 $o(x^n)$ 이면 $p_1(x)=p_2(x)$ 임을 보이라.

---

Let $p_1 (x) =a_0 + a_1x + \cdots + a_n x^n$ and $p_2(x) =b_0+b_1 x+ \cdots + b_n x^n$. Then, 
$$
p_1(x)-p_2(x) = (a_0-b_0)+(a_1-b_1)x +\cdots + (a_n-b_n)x^n= o(x^n)
$$

 $(p_1-p_2)^{(k)}(0)=0 \implies a_k = b_k$ for $k=0,\ldots,\,n$ 따라서 $p_1=p_2$



<b>4. </b> 다음 함수의 원점에서의 3차 근사 다항식을 구하라.

---

(1) $f(x) = e^x \sin x$
$$
\begin{align}
f(0)&=0\,,\\
f'(0) &=(e^x\sin x + e^x \cos x)(0)=1\,,\\
f''(x) &= (e^x \sin x + e^x \cos x + e^x  \cos x -e^x \sin x)(0)=(2e^x \cos x)(0)=2\,,\\
f^{(3)}(x) &= (2e^x \cos x - 2e^x\sin x )(0)=2\,,\\
f(x)&\approx 0+x+x^2 + \dfrac{1}{3} x^3 

\end{align}
$$
(2) $f(x) = x\ln (1+x)$ 
$$
\begin{align}
f(0)&=0\,,\\
f'(0) &= \left( \ln (1+x) + \dfrac{x}{1+x} \right) (0)=0\,,\\
f''(0) &=\left(\dfrac{2}{1+x}-\dfrac{x}{(1+x)^2}\right)(0)=2\,,\\
f^{(3)}(0) &= \left(\dfrac{-2}{(1+x)^2} -\dfrac{1}{(1+x)^2}+ \dfrac{2x}{(1+x)^3}\right)(0)=-3\;. \\
f(x) &\approx x^2-\dfrac{1}{2}x^3\;.

\end{align}
$$
(3) $f(x) = e^{-x^2}$
$$
\begin{align}
f(0)&=1\,, \\
f'(0) &= \left(-2xe^{-x^2}\right)(0)=0\,,\\
f''(0) &=\left(-2e^{-x^2} +4x^2e^{-x^2}\right)(0)=-2\,,\\
f^{(3)}(0) &= \left(4xe^{-x^2} + 8xe^{-x^2} -8x^3e^{-x^2}\right)(0)=0\,.\\
f(x) &\approx 1-x^2

\end{align}
$$
(4) $f(x) = \sin \exp(x)$ 
$$
\begin{align}
f(0)&=\sin 1\,,\\
f'(0) & = (e^x \cos e^x)(0)=\cos 1\,,\\
f''(0)&= (e^x \cos e^x -e^{2x } \sin e^x)(0)=\cos 1-\sin 1\\
f'''(0) &=(e^x \cos e^x -e^x \sin e^x-2e^{2x}\sin e^x-e^{3x}\cos e^x)(0)=\cos 1-\sin 1-\sin 1 -\cos 1=-2\sin 1\,,\\
f(x)&\approx (\sin 1)+ (\cos 1) x + \dfrac{\cos 1-\sin 1}{2}x^2 -\dfrac{2\sin 1}{6} x^3\;

\end{align}
$$

(5) $f(x) = x-\cos x$
$$
\begin{align}
f(0)&=-1\,,\\
f'(0)&=(1+\sin x)(0)=1\,,\\
f''(0) &=(\cos x)(0)=1\,,\\
f^{(3)}(0) &=(-\sin x)(0)=0\,,\\
f(x)&\approx  -1+x+\dfrac{1}{2}x^2\,.

\end{align}
$$


(6) $f(x)=2^x = e^{x \ln 2}$ 
$$
\begin{align}
f(0)&=1\,,\\
f'(0)& = (\ln 2 e^{x\ln 2})(0)=\ln 2\,,\\
f''(0) &= ((\ln 2)^2 e^{x\ln 2})(0)=(\ln 2)^2\,,\\
f^{(3)}(0) &= ((\ln 2)^3 e^{x \ln 2})(0)= (\ln 2)^3\,,\\
f(x)&\approx 1 + \ln 2 x + \dfrac{(\ln 2)^2}{2}x^2 + \dfrac{(\ln 2)^3}{3!}x^3\,.
\end{align}
$$


(7) $f(x) = \sqrt{1+x}$ 
$$
\begin{align}
f(0)&=1\,,\\
f'(0)&= \left( \dfrac{1}{2\sqrt{1+x}}\right)(0)=\dfrac{1}{2}\,,\\
f''(0)&=\left(-\dfrac{1}{4} \dfrac{1}{(1+x)^{3/2}}\right)(0)=-\dfrac{1}{4}\,,\\
f^{(3)}(0)&=\left(\dfrac{3}{8} \dfrac{1}{(1+x)^{5/2}}\right)(0) =\dfrac{3}{8}\,,\\
f(x) &\approx 1+\dfrac{1}{2}x -\dfrac{1}{8}x^2 + \dfrac{1}{16}x^3\,.

\end{align}
$$


(8) $f(x) = (1+x)^{-1}$
$$
\begin{align}
f(0)&=1\,,\\
f'(0) &= \left(-(1+x)^{-2}\right)(0)=-1\,,\\
f''(0) &=\left(2(x+1)^{-3}\right)(0)=2\,,\\
f^{(3)}(0) &= (-6(x+1)^{-4})(0)=-6\,,\\
f(x) &\approx 1-x+x^2 -x^3\,.

\end{align}
$$


<b>5. </b> 다음을 보이라.

---

(1) $\cosh x = \cos x + o(x)$

$f(x)=\cosh x - \cos x$ 라 놓으면 $f(0)=(\cosh x -\cos x)(0)=0$, $f'(0)= (\sinh x + \sin x)(0)=0$ 이므로 $f(x)=o(x)$ .



(2) $\sinh x = \sin x +o(x^2)$ 

$f(x) = \sinh x - \sin x$ 라 놓으면 $f(0)=0$, $f'(x) = (\cosh x - \cos x)(0)=0$, $f''(x) = (\sin h x + \sin x)(0)=0$ 이므로 $f(x) = o(x^2)$ 이다.



(3) $\tanh x = \arctan x + o(x^4)$ 

멱급수 전개를 보면,
$$
\begin{align}
\tanh x &=  x-\dfrac{1}{3}x^3 + O(x^4)\,,\\
\arctan x &= x-\dfrac{1}{3}x^3 +O(x^4)\,,\\
\tanh x-\arctan x &=O(x^4)
\end{align}
$$


<b>6.</b> 원점 근방에서 정의된 연속 함수 $f(x)$ 가 $o(x^n)$ 이면 적분함수 $\displaystyle F(x):= \int_0^x f(t)\, dt$ 는 $o(x^{n+1})$ 임을 보여라.

---

$F'(x) = f(x),\, F^{(n)}(x)=f^{(n-1)}(x)$ 이므로 trivial 하다.



<b>7. </b> 원점 근방에서 정의된 $n$ 번 미분가능 함수 $f(x)$ 가 $o(x^n)$ 이면 도함수 $f'(x)$ 는 $o(x^{n-1})$ 임을 보여라.

---

trivial



<b>8. </b> 정육면체의 모서리의 길이를 각각 1% 씩 증가시키면 부피는 3% 정도 증가함을 보여라.

---

$f(x) =V(L+x)=(L+x)^3=L^3 +3L^2x +3Lx^2 +x^3$.   $x=\dfrac{1}{100}L$ 라 하면,
$$
\dfrac{f(x)-f(0)}{f(0)}=\dfrac{1}{L^3} \left(\dfrac{3}{100}L^3 +\dfrac{3L^3}{10,000}+ \dfrac{L^3}{1,000,000} \right) \approx 0.03
$$


나머지는 생략..



## 연습문제 : 제 3장 4절



<b>1. </b> 지수함수 $\exp x$ 의 테일러 전개에서 $n$ 차 잉여항 $R_n (x)$ 가
$$
\left| R_n (x)\right| \le \dfrac{|x|^{n+1}}{(n+1)!} \max\{e^x,\,1\}
$$
임을 보이고, 이로부터 $e$ 의 값을 오차의 범위가 0.001 이하가 되도록 구하라.

---

$$
|R_n(x) | = |e^x-T_n(x)|=\left| \dfrac{e^y x^n}{(n+1)!} \right|
$$

여기서 $y$ 는 $0$ 과 $x$ 사이에서 $e^x-T_n (x) = e^yx^n/(n+1)!$ 을 만족하는 값이다. $x<0$ 이면 $ -\infty <y <0$ 이므로 $e^y<1$ 이며 $x>0$ 이면 $0<y<x$ 이므로 $e^y < e^x$ 이다. 따라서 $0<e^y \le \max\{e^x,\,1\}$ 이며, 주어진 식이 증명되었다. 그런데 우리는 $e^1$ 의 정확한 값을 모른다고 가정해야 한다. 다만 $0<e<3$ 임을 안다(고 가정하자). 

$e=e^1$ 이므로 $\left| R_n (1)\right| < \dfrac{3}{(n+1)!} $ 이다. $R_5(1)<0.0042, R_6(1)<0.0006$ 이므로 6차항 까지 계산하면 된다. 
$$
e^1 \approx 1+1+\dfrac{1}{2} + \dfrac{1}{3!} + \dfrac{1}{4!}+\dfrac{1}{5!}+\dfrac{1}{6}=2.7180\dot5
$$


<b>2. </b> $e^{0.1}$ 의 근사값을 오차가 $10^{-3}$ 이내가 되도록 구하라.

---

$1<e^{0.1}<2$ 이므로$R_n (0.1) \le  \left|\dfrac{(0.2)^n}{(n+1)!}\right|$ $R_1(0.1)\le 0.1,\, R_2(0.1)= 0.00\dot{6},\, R_3(0.1)\le 0.000\dot{3}$ 이므로 $3$ 차항 까지만 구하면 된다.
$$
e^{0.1}\approx 1+0.1+ \dfrac{(0.1)^2}{2}+ \dfrac{(0.1)^3}{3!}=1.105\;.
$$


<b>3.  </b> 생략



<b>4. </b> 원점을 포함하는 구간에서 정의된 $n$ 번 미분 가능한 함수 $f(x)$ 의 $n-1$ 차 나머지항 $R_{n-1}(x)$ 에 대하여
$$
\lim_{x \to 0} \dfrac{R_{n-1}(x)}{x^n} = \dfrac{f^{(n)}(0)}{n!}
$$
임을 보이라.

---

$\displaystyle F_n (x) = \sum_{k=0}^n \dfrac{f^{(k)}(0)}{k!} x^n$ 은 $f(x)$ 의 $n$ 차항 까지의 테일러 전개이다. $R_{n-1}(x) = f(x) - F_{n-1} (x)$ 이므로,
$$
\begin{align}
\lim_{x \to 0}\dfrac{R_{n-1}(x)}{x^n}= \lim_{x \to 0}\dfrac{f(x)-F_{n-1}(x)}{x^n}=\lim_{x\to 0}\dfrac{f'(x)-F'_{n-1}(x)}{nx^{n-1}} = \cdots = \lim_{x\to 0}\dfrac{f^{(n-1)}(x)-f^{(n-1)}(0)}{n!x} =\lim_{x \to 0}\dfrac{f^{(n)} (x)}{n!}=\dfrac{f^{n}(0)}{n!}

\end{align}
$$
 



<b>5. </b> 무한급함수 $f(x)$ 의 한 임계점 $x_0$ 에서 $f''(x_0)=0$ 일 때 $f'''(x_0)\ne 0$ 이면 $x_0$ 는 극소점도 아니고 극대점도 아님을 보이라.

---

$x_0=0$ 으로 놓아도 no loss of generality. 

$f(x)=f(0)+\dfrac{f'''(0)}{6}x^3 +R_{3}(x)$. $0$ 을 포함하는 어떤 열린구간 $I_0$ 에서 $f(x)-f(0) \approx ax^3$ for some constant $a$ 인데 $(f(x)-f(0))(f(-x)-f(0))<0$ 이므로 $0$ 은 극소점도 극대점도 아니다.



<b>6. </b> 원점을 포함하는 구간에서 정의된 $n$ 급 함수 $f(x)$ 에 대하여,
$$
B_n f(x) : = \max\{|f^{(n)}(t)-f^{(n)}(0)|: t\in [0,\,x]\}
$$
로 두면, $f(x)$ 의 $n$ 차 테일러 나머지항 $R_n f(x)$ 는 부등식
$$
|R_n f(x)|\le B_n f(x) \dfrac{|x|^n}{n!}
$$
을 만족시킴을 보여라.

---

