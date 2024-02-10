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

Let $X_i$ be the probability of rolling a higher value given that we obtained i on the first 
roll, where $i \in [1, n]$. Since we have a uniform probability space, we know that $Pr(X_i)$ =
$\frac{|\{a | a > i \wedge a \in S\}|}{|S|}$ = $|{a | a > i \wedge a \in S}| * \frac{1}{n^2}$.

$Pr(X_1) = \frac{n - 1}{n^2}$

$P(X_2) = \frac{n - 2}{n^2}$

$P(X_3) = \frac{n - 3}{n^2}$

$P(X_x) = \frac{n - x}{n^2}$


To calculate the probability that the second die has a higher value than the first,
we must consider all the possible values for the first die where a larger value
can be rolled for the second die. Our range of values for the first die 
is limited to [1, n]. 

When summing all the probabilities, $Pr(X_1 + X_2 + ... X_n)$, we notice that the events 
are disjoint and the expression $Pr(X_1 + X_2 + ... X_{n})$ simplifies to 
$Pr(X_1) + Pr(X_2) + ... Pr(X_{n - 1}) + Pr(X_n)$.

Note: Pr(X_n) is zero since there is no larger value that the second die can be.

We can factor out the $\frac{1}{n^2}$ term from the summation, and we are left with 
$\frac{1}{n^2}(n -1 + n -2 + .... 1)$.

Using the fact that the summation of the numbers from 1 to n is $\frac{n(n + 1)}{2}$, 
the summation from 1 to n - 1 is $\frac{(n - 1)(n)}{2}$.

$\frac{1}{n^2}(n -1 + n -2 + .... 1)$

= $\frac{(n - 1)(n)}{2n^2}$

### Given that the first dice is between 1 and m (for m ≤ n), what is the probability that the second dice lands on a higher value than does the first? 

In this case, I must calculate $Pr(X_1) + Pr(X_2) + ... Pr(X_{m})$.

Knowing that $Pr(X_m) = \frac{n - m}{n^2}$, the expression $Pr(X_1) + Pr(X_2) + ... Pr(X_{m})$ 
is equivalent to $\frac{1}{n^2}(n -1 + n - 2 + .... n - m)$

Summing the values from [n - m, n - 1], it is $\frac{(2n - m -1)(m)}{2}$.

$Pr(X_1) + Pr(X_2) + ... Pr(X_{m})$ 

= $\frac{(2n - m -1)(m)}{2n^2}$

The probability that the second dice lands on a higher value than the first is

$\frac{(2n - m -1)(m)}{2n^2}$.


## Question three
Suppose that an insurance company classifies people into one of three classes – good risks, average risks, and bad risks. Their records indicate that the probabilities that good, average, and bad risk persons will be involved in an accident over a 1-year span are, respectively, 0.05, 0.15, and 0.30. If 20% percent of the population are good risk, 50% percent are average risk and 30% percent are bad risk,

### What is the probability that a person has an accident in a fixed year? 
Let G, A, and B be the events where a person has good, average, and bad risk respectively.

$Pr(G) = 0.2$

$Pr(A) = 0.5$

$Pr(B) = 0.3$

Let AC be the event where someone is involved in an accident. 

$Pr(AC | G) = 0.05$

$Pr(AC | A) = 0.15$

$Pr(AC | B) = 0.30$

Using the law of total probability, $Pr(AC) = Pr(AC | G)Pr(G) + Pr(AC | A)Pr(A) + Pr(AC | B)Pr(B)$

$Pr(AC) = 0.05 * 0.2 + 0.5 * 0.15 + 0.3 * 0.3$

$Pr(AC) = 0.175$

### If a policy holder had no accidents in the 1-year span, what is the probability that they are good risk?

Calculate $Pr(G | AC^{\complement})$

$Pr(G | AC^{\complement}) = \frac{Pr(G \cap AC^{\complement})}{Pr(AC^{\complement})}$

$Pr(AC^{\complement}) = 1 - Pr(AC)  = 0.825 $

Pr(G | AC^{\complement}) = \frac{G \cap AC^{\complement}}{Pr(AC^{\complement})}

$Pr(AC | G) = \frac{Pr(AC \cap G)}{Pr(G)}$

$Pr(AC \cap G) = Pr(AC | G)Pr(G)$

$Pr(G | AC) = \frac{Pr(AC \cap G)}{Pr(AC)}$

$Pr(G | AC) = \frac{Pr(AC | G)Pr(G)}{Pr(AC)}$

$Pr(G | AC) =\frac{0.01}{0.175} \approx 0.0571$

$Pr(G \cap AC^{\complement}) = 1 - $Pr(G | AC)$

$Pr(G \cap AC^{\complement}) = 0.94$