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

Using linearity of expectation, $E[Z] = E[X] + E[Y]$. Using the fact that $X$ and $Y$ both have the same distribution, which is binomial,
$E[X] = E[Y] = np$. Using the fact that $p = \frac{1}{6}$, the value of $E[Z]$ is $E[Z] = 2 * \frac{n}{6} = \frac{n}{3}$.

Using the formula for variance on a r.v. $X$, $Var[X] = E[X^2] - (E[X])^2$, $Var[Z] = E[(X + y)^2] - (E[X + Y])$