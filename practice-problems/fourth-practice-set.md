## Question one

### What is the probability that the total system functions

Let $C_i$ be the event that the ith component functions. $\forall i, Pr(C_i) = p$.

In order to find the probability that the total system functions, I can take the complement of the probability that
the total system fails.

Let $F$ be the event that the total system fails. $Pr(F) = Pr(\overline{C_1} \cap \overline{C_2} \cap ..... \overline{C_n})$.

Since each event is independent, I know that $Pr(F)$ is the product of the n components failing.

$Pr(F) = (1 - p)^n$.

Given $Pr(F)$, I can compute its complement and say that $Pr(\bar{F}) = 1 - (1 - p)^n$.

### 
