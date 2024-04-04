## Question 1

### Compute E[X] and Var[X].

Since $X$ and $Y$ denotes the number of ones and twos in $n$ rolls of a standard die, we know that each dice roll 
is independent and the probability of obtaining a particular value on a roll is $\frac{1}{6}$. Using this fact, 
we can model $X$ and $Y$ as binomial distributions. $X \sim Bin(n, \frac{1}{6}), Y \sim Bin(n, \frac{1}{6})$.

Using that the expectation of a binomially distributed r.v $R$ is $E[R] = np$, $E[X]$ can be calculated as
$E[X] = np = n * \frac{1}{6} = \frac{n}{6}$.

Using that the variance of a binomially distributed r.v $R$ is $Var[R] = np(1 - p)$, $Var[X]$ can be calculated as
$Var[X] = np(1 - p) = n * \frac{1}{6} * \frac{5}{6} = \frac{5n}{36}$.

### Are the random variables X and Y independent? Prove or give a counter-example.

If $X$ and $Y$ are independent, then $Pr(X = x, Y = y) = Pr(X = x)Pr(Y = y)$ must be true for each value of $x$ and $y$. 

I will disprove this relation for $x = n, y = n$.

$Pr(X = n, Y = n) = 0$ since if I obtain n heads, I cannot obtain n tails as well.
However,
$Pr(X = n)Pr(Y = n) = \binom{n}{n}{\frac{1}{6}}^n * \binom{n}{n}{\frac{1}{6}}^n = {\frac{1}{6}}^{2n}$.

Comparing the values of $Pr(X = n, Y = n)$ and $Pr(X = n)Pr(Y = n)$, we see they are not equal. Therefore, 
$X$ and $Y$ are not independent.

###  If Z = X + Y , compute E[Z] and Var[Z]

Since each roll is independent and the probability of obtaining a one or a two remains constant, I can model $Z$ by a binomial distribution. 
$Z \sim Bin(n, \frac{1}{3})$.

Using the fact $Z$ has a binomial distribution, $E[Z] = np = \frac{n}{3}$

Using the formula for variance on a binomial r.v. $X$, $Var[X] = np(1 - p)$, $Var[Z] = n * \frac{1}{3} * \frac{2}{3} = \frac{2n}{9}$.

### Use the above results to compute E[(X + Y )^2] and E[X Y ]

Using the formula $Var[Z] = E[Z^2] - {E[Z]}^2$ and knowing that 
$E[(X + Y)^2] = E[Z^2]$, we can rearrange the formula for $Var[Z]$ to 
obtain $E[Z^2] = Var[Z] + {E[Z]}^2$.

Substituting the values of $Var[Z] = \frac{2n}{9}$ and $(E[Z])^2 = \frac{n^2}{9}$ into
$E[Z^2] = Var[Z] + {E[Z]}^2$, we obtain that $E[Z^2] = \frac{2n}{9} + \frac{n^2}{9} = \frac{2n + n^2}{9}$

Expanding out $E[Z^2]$, we obtain $E[Z^2] = E[(X + Y)^2] = E[X^2 + Y^2 + 2XY]$.
Rearranging the expression, we obtain $E[XY] = E[Z^2]  - E[X^2] - E[Y^2]$.

Knowing that $X$ and $Y$ have the same distribution, finding the value of $E[X^2]$ will allow $E[Y^2]$ to be known.

Writing out $X$ as $X = X_1 + X_2 + X_3 + ..... X_n$, where each $X_i$ in an indicator r.v determining if 
a one has occurred on roll i. $X^2$ then becomes $(X_1 + X_2 + X_3 + ..... X_n)^2 = \displaystyle\sum_{i}^{} X_i^2 + 2 \displaystyle\sum_{i, j, i \neq j}^{} X_i X_j$. 
Applying linearity of expectation in $E[X^2]$, we obtain $E[X^2] = \displaystyle\sum_{i}^{} E[X_i^2] + 2 \displaystyle\sum_{i, j, i \neq j}^{} E[X_i X_j]$

Since $X_i$ is an indicator variable, $X_i^2 = X_i$. The above expression can be rewritten as
$E[X^2] = \displaystyle\sum_{i}^{} E[X_i] + 2 \displaystyle\sum_{i, j, i \neq j}^{} E[X_i X_j]$.
Recognizing the first term in the expression is equivalent to $E[X] = np = \frac{n}{6}$, the expression simplifies to
$E[X^2] = \frac{n}{6} + 2 \displaystyle\sum_{i, j, i \neq j}^{} E[X_i X_j]$
In the second term, the only case where any $X_i X_j$ pair outputs one is where both 
$X_i$ and $X_j$ are both one, which occurs with probability of $\frac{1}{36}$. Since there are
$\binom{n}{2} - n = \frac{n^2 - 3n}{2}$ many ways to obtain distinct $X_i X_j$ pairs, the expression above reduces to 
$E[X^2] = \frac{n}{6} + 2 * \frac{n^2 - 3n}{72} = \frac{n}{6} + \frac{n^2 - 3n}{36} = \frac{n^2 + 3n}{36}$.

Knowing the value of $E[X^2]$ and further aware that $E[X^2] = E[Y^2]$, I can now calculate $E[XY]$.
Using the values of
$E[X^2] = \frac{n^2 + 3n}{36}, E[Z^2] = \frac{2n + n^2}{9}$ in the expression $E[XY] = E[Z^2]  - E[X^2] - E[Y^2]$, 
I obtain $E[XY] = \frac{2n + n^2}{9} - 2 * \frac{n^2 + 3n}{36} = \frac{2n + n^2}{9} -\frac{n^2 + 3n}{18}  = \frac{4n + 2n^2 - n^2 - 3n}{18} = \frac{n^2 + n}{18}$.

### Use the above results to compute Cov[X, Y ]
Using the formula for covariance, $Cov[X, Y] = E[XY] - E[X]E[Y]$, I have that
$Cov[X, Y]  = \frac{n^2 + n}{18} - \frac{n^2}{36} = \frac{n^2 + 2n}{36}$.

### Use the above results to compute Corr[X, Y ]. Are X and Y positively or negatively correlated?

Using the formula for $Corr[X, Y] = \frac{Cov[X, Y]}{\sqrt{Var[X]Var[Y]}}$, I obtain that the correlation coefficient is
$\frac{\frac{n^2 + 2n}{36}}{\sqrt{(\frac{5n}{36})^2}} = \frac{n^2 + 2n}{36} * \frac{36}{5n} = \frac{n^2 + 2n}{5n}$. Since this 
value is positive for all values of n $\in \mathbb{Z^{+}}$, I conclude that $X$ and $Y$ are positively correlated.

## Question 2

### Calculate E[X] and Var[X]

We can decompose $X$ as $X = X_1 + X_2 + X_3 + .... X_n$, where each $X_i$ represents an indicator r.v signifying that the 
ith turn was a winning turn. Applying linearity of expectation to $E[X]$, we obtain $E[X] = E[X_1] + E[X_2] + ... E[X_n]$.

$\forall X_i, Pr(X_i = 1) = p^i$. Applying this to $E[X]$ above, we obtain that $E[X] = p + p^2 + ... p^n$. Recognizing this
as a geometric series, we know that $\displaystyle\sum_{i = 1}^{n} p^i = \frac{p}{1 - p}$. Therefore, 
$E[X] = \frac{p}{1 - p}$.

For calculating $Var[X]$, I can exploit the fact that for an indicator r.v $Y$, $Var[Y] = p(1 - p) = p - p^2$. Furthermore, 
since all the flips are mutually independent of each other, I can assume that the results of one game have no influence on the
outcome of the other games. Utilizing this information in calculating $Var[X]$, I have that 
$Var[X] = \displaystyle\sum_{i = 1}^{n} p^i - p^{2i}$. Expanding out the first few terms of the summation, I have 
$p - p^2, p^2 - p^4, p^3 - p^6$, and  $p^4 - p^8$. Seeing that some of the terms would be cancelled out when summing them up, 
adding more terms from the summation would cancel out every term except the $p$ term. 

I can simplify $Var[X] = \displaystyle\sum_{i = 1}^{n} p^i - p^{2i}$ to become $Var[X] = p$.

Ask TA if this is correct.

### Calculate E[Y] and Var[Y]

I can compose $Y$ as a collection of $Y_i$ where each $Y_i$ is an indicator variable r.v signifying if the ith turn 
is a winning turn. Applying linearity of expectation, $E[Y] = E[Y_1 + Y_2 + Y_3 + .... Y_n] = E[Y_1] + E[Y_2] + ... E[Y_n]$.

If I need at least one heads in order to have a winning turn, then on turn j I would have probability $1 - (1 - p)^j$ 
of obtaining at least one heads. Since this happens for each turn, the expression $E[Y]$ can be modified as 
$E[Y] = \displaystyle\sum_{j = 1}^{n} 1 - (1 - p)^j$. Breaking apart the summation, I obtain
$E[Y] = \displaystyle\sum_{j = 1}^{n} 1  - \displaystyle\sum_{j = 1}^{n}(1 - p)^j$, which simplifies to
$E[Y] = n - \displaystyle\sum_{j = 1}^{n}(1 - p)^j$. Recognizing the second term is a geometric sum, I can 
use the formula for a geometric sum ($S_n = \frac{a}{1 -r}$) to reduce the expression above into
$E[Y] = n - \frac{1 - p}{1 - (1 - p)} = n - \frac{1 - p}{p}$.

The expression above simplifies to
$E[Y] = \frac{np + p - 1}{p}$.


### Var[Y]

Using the fact that each of turn result is independent of the other turns, I can calculate 
$Var[Y]$ as $Var[Y] = \displaystyle\sum_{i = 1}^{n} Var[Y_i]$. 

Knowing that $Var[T] = p(1 - p)$ for an indicator r.v $T$, I can apply it with $Y$ to 
obtain $Var[Y] = \displaystyle\sum_{i = 1}^{n} p_i(1 - p_i)$. Substituting the 
value of $p_i$ with $1 - (1 - p)^i$, the expression becomes
$Var[Y] = \displaystyle\sum_{i = 1}^{n} (1 - (1 - p)^i) (1 - (1 - (1 - p)^i)) = \displaystyle\sum_{i = 1}^{n} (1 - (1 - p)^i) (1 - p)^i$.

Noting that many of the terms in the summation cancel out, we can simplify the summation to become $Var[Y] = 1 - p$.

Ask TA about this.  




