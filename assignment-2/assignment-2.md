## Question 1

### Prove that the probability that exactly one of the events A or B occurs is equal to Pr[A] + Pr[B] − 2 Pr[A ∩ B].

$Pr(A) = Pr(A - B) + Pr(A \cap B)$

$Pr(A - B) =  Pr(A) - Pr(A \cap B)$

$Pr(B) = Pr(B - A) + Pr(A \cap B)$

$Pr(B - A) =  Pr(B) - Pr(A \cap B)$

The probability that exactly one of the events A or B occurs is $Pr((A - B) \cup (B - A))$.

Since (B - A) and (A - B) are disjoint, $Pr((A - B) \cup (B - A)) = Pr(A - B) + Pr(B - A)$

$Pr((A - B) \cup (B - A)) =  Pr(A) - Pr(A \cap B) + Pr(B) - Pr(A \cap B)$ 

= $Pr(A) + Pr(B) - 2Pr(A \cap B)$

## Question 2

A pair of n-sided fair dice are rolled (there is equal probability of rolling each number
from {1, 2, . . . , n})

### What is the probability that the second dice lands on a higher value than does the first?
The probability of obtaining the pair (a, b), where $a, b \in [1, n]$, is $\frac{1}{n^2}$.
Let $S = {(a, b) | a, b \in [1, n]}$

Let $P(x)$ be the probability of rolling a higher value given that we obtained x on the first 
roll, where $x \in [1, n]$. Since we have a uniform probability space, we know that $P(x)$ =
$\frac{|\{a | a > x \wedge a \in S\}|}{|S|}$ = $|{a | a > x \wedge a \in S}| * \frac{1}{n^2}$.

$P(1) = \frac{n - 1}{n^2}$

$P(2) = \frac{n - 2}{n^2}$

$P(3) = \frac{n - 3}{n^2}$

$P(x) = \frac{n - x}{n^2}$


To calculate the probability that the second die has a higher value than the first,
we must consider all the possible values for the first die where a larger value
can be rolled from the second die. Our range of values is limited to [1, n - 1]. 
