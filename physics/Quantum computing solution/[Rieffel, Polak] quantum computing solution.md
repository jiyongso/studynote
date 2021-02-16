Quantum Computing - Rieffel and Polak
==



## Chapter 2. Single cubit quantum systems



<b>2.9</b>  BB84 protocol에서 Eve 의 존재를 90% 확률로 감지하기 위해서 Alice 와 Bob이 비교해야 하는 비트수는 얼마인가?

---

Eve 가 중간에 도청한 다고 가정할 경우 한 비트에 대해 오류가 날 확률은 25% , 오류가 나지 않을 확률은 75%. 따라서 $(3/4)^n <0.1$ 인 $n$ 값을 구하면 된다. $n=8$ 일 때 $0.1001$, $n=9$ 일 때 $0.075$ 이므로 9개의 비트를 비교하면 된다.



<b>2.10</b> Eve가 두 basis 중 어떤 것을 선택했는지 모르고 random 하게 선택 했을 때 eve의 도청 성공을 BB84 protocol 에서 분석하자

(a) Alice와 Bob의 public channel을 도청 한 후 이브가 final key를 알게 될 평균적인 확률은 얼마인가?

(b) Eve 가 가진 string이 올바를 확률은 평균적으로 얼마인가?

(c) Eve의 존재를 90% 확률로 확인하기 위해서 Alice와 Bob이 비교해야 하는 bit 수는 얼마인가?

---

(a) 

