## Question one

### What is the probability that the total system functions

Let $C_i$ be the event that the ith component functions. $\forall i, Pr(C_i) = p$.

In order to find the probability that the total system functions, I can take the complement of the probability that
the total system fails.

Let $F$ be the event that the total system fails. $Pr(F) = Pr(\overline{C_1} \cap \overline{C_2} \cap ..... \overline{C_n})$.

Since each event is independent, I know that $Pr(F)$ is the product of the n components failing.

$Pr(F) = (1 - p)^n$.

Given $Pr(F)$, I can compute its complement and say that $Pr(\bar{F}) = 1 - (1 - p)^n$.

The probability that the total system functions is  $1 - (1 - p)^n$.

### The total system will be able to operate effectively if at least 3 of its 5 components function. What is the probability that the total system functions?

Let $T$ be the event the total system functions.

Let $CM_3, CM_4,$ and $CM_5$ be the events that three, four, and five components are functioning.

Since $CM_3, CM_4,$ and $CM_5$ are disjoint events and that Pr(T) = $Pr(CM_3 \cup CM_4 \cup CM_5)$, I can say that
$Pr(T) = Pr(CM_3) + Pr(CM_4) + Pr(CM_5)$.

Calculating the values for $Pr(CM_3), Pr(CM_4)$, and  $Pr(CM_5)$, they are 
$\binom{5}{3}p^3(1-p)^2, \binom{5}{4}p^4(1 - p),$ and $\binom{5}{5}p^5$ respectively.

Summing up these values, we have that $Pr(T) =  \binom{5}{3}p^3(1-p)^2 + \binom{5}{4}p^4(1 - p) + p^5$. 

