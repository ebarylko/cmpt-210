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

This is similar to the first part of the question, but we are now limiting the range of 
values that the first die can take on.

Instead of $Pr(X_1) + Pr(X_2) + ... Pr(X_{n - 1}) + Pr(X_n)$, we now have
$Pr(X_1) + Pr(X_2) + ... Pr(X_{m})$. 

I have two cases to analyze:
* m = n
* $m < n$

In the first case, $Pr(X_1) + Pr(X_2) + ... Pr(X_{m})$ becomes
$Pr(X_1) + Pr(X_2) + ... Pr(X_{m - 1})$ since $Pr(X_n) = 0$.

This expression is equivalent to what I solved in the earlier part, having a probability
of  $\frac{(n - 1)(n)}{2n^2}$.

In the second case, I must calculate $Pr(X_1) + Pr(X_2) + ... Pr(X_{m})$.

Knowing that $Pr(X_m) = \frac{n - m}{n^2}$, the expression $Pr(X_1) + Pr(X_2) + ... Pr(X_{m})$ 
is equivalent to $\frac{1}{n^2}(n -1 + n - 2 + .... n - m)$

Summing the values from [n - m, n - 1], it is $\frac{(2n - m -1)(m)}{2}$.

$Pr(X_1) + Pr(X_2) + ... Pr(X_{m})$ 

= $\frac{(2n - m -1)(m)}{2n^2}$


