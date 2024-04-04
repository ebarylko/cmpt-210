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
a one has occurred on roll i. $X^2$ then becomes $(X_1 + X_2 + X_3 + ..... X_n)^2 = \sum_{i}^{} X_i^2 + 2\sum_{i, j, i \neq j}^{} X_i X_j$. 
Applying linearity of expectation in $E[X^2]$, we obtain $E[X^2] = \displaystyle\sum_{i}^{} E[X_i^2] + 2 \displaystyle\sum_{i, j, i \neq j}^{} E[X_i X_j]$