## Question one

### What is the probability that he breaks exactly 2 out of the 5 boards that are placed before him?
Since each board is independent and the probability he breaks each board is the same, I can model the 
number of boards broken by a binomial distribution.

Let $B$ be the number of boards broken. $B \sim Bin(5, 0.8)$.

$Pr(B = 2) = \binom{5}{2}(0.8)^2(0.2)^3 = 0.0512$.

### What is the probability that he breaks at least 3 out of the 5 boards that are placed before him
To calculate $Pr(B \ge 3)$, this is equivalent to finding the value of $1 - Pr(B \le 2)$.

I already have $Pr(B = 2)$ from the question above, and I must find the values of $Pr(B = 1)$ and 
$Pr(B = 0)$.

Calculating $Pr(B = 1)$ and $Pr(B = 0)$, I find them to be $\binom{5}{1}(0.8)(0.2)^4$ and $\binom{5}{0}(0.2)^5$ respectively.

Summing up $Pr(B = 2), Pr(B = 1),$ and $Pr(B = 0)$, I have that $Pr(B \le 2) = 0.05792$.

Using this value, I have that $Pr(B \ge 3) = 1 - Pr(B \le 2) = 0.94208$.
