Topology in Metric Space
=====================
 대체적으로  Rudin을 따른다.
## Definitions
아래의 모든 집합은  metric space $X$의 subset 이다.
1. $B_{\varepsilon}(p) = \{x \in X : d(x, p) < \varepsilon\; \textrm{for some} \;\varepsilon > 0\}$ 을 p에 대한 **$\varepsilon$-neighbor** 라 한다.
2. $p$의 모든 $\varepsilon$-neighbor가 집합 $E \subset X$의 원소를 포함하면 $p$를 $E$의 **limit point** 라 한다. $E$의 모든 limit point의 집합을 $E'$라 쓴다. $\overline{E} = E \cup E'$를 **closure** of $E$라 한다.
3. $p\in E$가 $E$의 limit point가 아니면 $p$를 **isolated point** of $E$라 한다.
4. $E$의 모든 limit points가 $E$에 포함되면 $E$를 **closed set** 이라 한다.
5. $p\in E$의 어떤 $\varepsilon$-neighboor가 $E$에 포함되면 $p$는 $E$의 **interior point**라 한다. $E$의 모든 interior point의 집합을 $int(E)$라 쓴다.
6. $E = int(E)$ 일 때 $E$를 **open set** 이라 한다.
7. $E$가 $x$를 포함하는 open set일 경우 $E$ is a **neighborhood** of $x$라 한다.
8. $E = \overline{E}$ 일 때 $E$를 **perfec set** 이라 한다.
9.  모든 $x \in X$가 $E$의 limit point 이면 $E$를 **dense** in X 라 한다.


## Properties

1. 모든 $\varepsilon$-neighbor of $x \in X$는 open in $X$ 이다.
2. $E$ is open iff $X-E$ is closed. $F$ is closed iff $X-F$ is open.
3. Union of open sets is an open set. Finite intersection of open sets is an open set. Finite union of closed sets is a closed set. Intersection of closed sets is a closed set.
4. $\overline{E}$는 closed set이다. $E = \overline{E}$ iff $E$ is closed. $F$가 $E$를 포함하는 closed set 이면 $\overline{E} \subset F$ 이다. 