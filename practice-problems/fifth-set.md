## Question 1

### Calculate the expected payoff for each game
**Game A**:


Let $P_A$ be the r.v denoting the payoff for game $A$. Using the formula for expectation,
$E[P_A] = 2 * \frac{2}{3} -1 * \frac{1}{3} = 1$.

Using the formula for variance, 
$Var[P_A] = 4 * \frac{2}{3} + 1 * \frac{1}{3} = 3$.

**Game B**:

Let $P_B$ be the r.v denoting the payoff for game $B$. Using the formula for expectation,
$E[P_B] = 1002 * \frac{2}{3} -2001 * \frac{1}{3} = 1$.

Using the formula for variance,
$Var[P_B] = (1002)^2 * \frac{2}{3} + (2001)^2 * \frac{1}{3} = 2004002$.


## Question 2

### We throw a standard dice, and define a random variable R which is equal to 1 if we get an even number and 0 otherwise. What is Var[R]?
Since the die is fair, implying the probability of getting an even number is $\frac{1}{2}$, and that we only have 
one trial, it seems that a Bernoulli distribution best models $R$. $R \sim Bern(\frac{1}{2})$.

Using the formula for variance, $Var[R] = E[R^2] - (E[R])^2$. Using the fact that $R$ is a Bernoulli distribution,
$R^2 = R$ for all the possible values $R$ can take on. Using that, the expression above becomes
$Var[R] = E[R] - (E[R])^2 = p - p^2 = p(1 - p)$.

### We repeatedly and independently throw the dice until we get an even number. We define a random variable S equal to the number of throws we need to get an even number. What is Var[S]? 
Since we continuously throw the dice until an even number is obtained, a geometric distribution seems to model $S$ the best.
$S \sim Geo(\frac{1}{2})$.

Using the formula for variance, $Var[S] = E[S^2] - (E[S])^2 = \frac{2 - p}{p^2} - \frac{1}{p^2} = \frac{1 - p}{p^2}$.

## Question three
    
$E[\frac{X - \mu}{\sigma}] = E[\frac{X}{\sigma} - \frac{\mu}{\sigma}] = \frac{\mu}{\sigma} - \frac{\mu}{\sigma} = 0$. 

$Var[\frac{X - \mu}{\sigma}] = Var[\frac{X}{\sigma} - \frac{\mu}{\sigma}] = \frac{\sigma^2}{\sigma^2} = 1$. 

## Question four