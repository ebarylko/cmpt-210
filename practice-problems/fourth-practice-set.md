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

## Question two

For finding the p where a five component system is better than a three component system, we need a p such that 
$\binom{5}{3}p^3(1-p)^2 + \binom{5}{4}p^4(1 - p) + \binom{5}{5}p^5 > \binom{3}{2}p^2(1 - p) + p^3$. 

Simplifying the above expression, it becomes
$10p^3(1-p)^2 + 5p^4(1 - p) + p^5 > 3p^2(1 - p) + p^3$. 

Noting that every term contains a factor of $p^2$, we can factor it out and obtain
$10p(1-p)^2 + 5p^2(1 - p) + p^3 > 3(1 - p) + p$, which is also equivalent to
$10p(1-p)^2 + 5p^2(1 - p) + p^3 > 3 - 2p$.

Moving over the $2p$ to the left and expanding the left hand side, we obtain
$6p^3 - 15p^2 + 12p > 3$, which is equivalent to
$2p^3 - 5p^2 + 4p > 1$.

If we move the one over to the left and solve the inequality, we will know what value p must take on.

Solving this inequality, $2p^3 - 5p^2 + 4p - 1 > 0$, we can use the root remainder theorem to find a possible 
root. Inputting the value $p = 1$ into the expression $2p^3 - 5p^2 + 4p - 1$, we obtain 0. As a consequence of this,
we know that $p -1$ is one of the factors of the expression.

Factoring $p -1$ out of $2p^3 - 5p^2 + 4p - 1$, we obtain $2p^3 -3p + 1$. Applying the root remainder theorem and 
using $p = 1$,  $2p^3 -3p + 1$ evaluates to zero. Therefore, we know that another root is $p -1$. Factoring $p -1$ 
out of the expression, we obtain $2p - 1$.

Using the work above, we can say that the inequality $2p^3 - 5p^2 + 4p - 1 > 0$ is equivalent to
$(1-p)^2(2p - 1) > 0$. Solving the inequality now, we find that $p > \frac{1}{2}$.

A five component system is better than a three component system when $p > \frac{1}{2}$.

## Question three

### Part 1

$PDF_X(3) = \frac{1}{6}$.

$PDF_X(5) = \frac{1}{6}$.

$PDF_X(7) = \frac{1}{6}$.

$PDF_X(9) = \frac{1}{6}$.

$PDF_X(11) = \frac{1}{6}$.

$PDF_X(13) = \frac{1}{6}$.

### Part 2

$PDF_X(0) = \frac{1}{2}$.

$PDF_X(1) = \frac{1}{6}$.

$PDF_X(2) = \frac{1}{6}$.

$PDF_X(3) = \frac{1}{6}$.

## Question four

Let $X$ be a random variable denoting the amount won.

$E[X] = 1,000,000 * \frac{4}{1,000,000} + 100,000 * \frac{5}{1,000,000} + 1000 * \frac{5000}{1,000,000}$

$E[X] = 4 + \frac{5}{10} + 5 = 9.5\$$.

## Question five 

### Part 1
$R \sim Bern(\frac{1}{2})$.

$E[R] = 1 * \frac{1}{2} + 0 * \frac{1}{2} = \frac{1}{2}$.

### Part 2

$R \sim Bin(10, \frac{1}{2})$.

$E[R] = np = 10 * \frac{1}{2} = 5$.

### Part 3
$R \sim Geo(\frac{1}{2})$.

$E[R] = \frac{1}{p} = \frac{1}{\frac{1}{2}} = 2$.

## Question six

$E[X] = 36 * \frac{36}{120} + 40 * \frac{40}{120} + 44 * \frac{44}{120}$

$E[X] = 36 * \frac{3}{10} = 40 * \frac{1}{3} + 44 * \frac{11}{30}$

$E[X] = 36 * \frac{9}{30} = 40 * \frac{10}{30} + 44 * \frac{11}{30} = \frac{1208}{30} = \frac{604}{15} \approx 40.27$

## Question seven

### Case 1

Let $X$ be the number of cards which have been guessed correctly, and $X_i$ be the event that the ith guess was correct.

Since we are guessing the value of each of the n cards, we can say that $X = X_1 + X_2 + ..... + X_n$.

Using linearity of expectation, $E[X]$ becomes $E(X_1) + E(X_2) + ... + E(X_n)$. In order to calculate this 
expression, we must find the expected value for each guess.

For each guess, we either guess it correctly with probability $\frac{1}{n}$ or guess it incorrectly with probability 
$\frac{n - 1}{n}$ since we select a card at random from a full deck.

We can then say that $\forall X_i, X_i \sim Bern(\frac{1}{n})$.

As a consequence of the above, we know that $\forall X_i, E[X_i] = \frac{1}{n}$.

Taking our expression for $E[X]$ and substituting the corresponding values for each $E[X_i]$, we obtain that
$E(X_1) + E(X_2) + ... + E(X_n) = n * \frac{1}{n} = 1$.

This means that the expected number of correct guesses is 1.

### Case 2

For each guess, remembering the cards played allows us to narrow down our guess. $\forall i \in [1, 52],$ Pr(ith card was guessed correctly) 
= $\frac{1}{52 - (i - 1)}$, where $i - 1$ denotes the cards we have seen at the ith guess.

Applying linearity of expectation on the expression $E[X] = (X_1) + E(X_2) + ... + E(X_n)$, we obtain that 
$E[X] = \frac{1}{52} + {1}{51} + .... + \frac{1}{1}$.

Noting that the values for the expectation of X are a subset of the harmonic numbers and that
${\int_{1}^{n} \frac{1}{n}dx} = ln(n)$, we can bound the expected value of correct cards by $ln(n)$.


## Question 8

### Part 1
Let B be the random variable counting the number of blue-eyed offspring excluding the eldest child.

Since the eldest child has blue eyes, this means that each parent has the gene for brown and blue eyes.

Furthermore, each child has a probability of $\frac{1}{2}$ to receive either gene. In order for a child to have blue 
eyes, they must contain two blue genes, which occurs with a probability of $\frac{1}{4}$.

Using the information above, $Pr(B = 2) = \binom{4}{2}(\frac{1}{2})^2(\frac{3}{4})^2 = \frac{27}{128}$.

Ask professor about the independence of each child's eye color. Are they not independent since the knowledge that 
one of them has blue eyes affects the probability that the other has brown eyes?

### Part 2

Let Br be the random variable counting the number of brown-eyed offspring in the additional five children.

Assuming the children's eye colors are independent of each other (are they really?), I can say that 
$Br \sim Bin(5, \frac{3}{4})$. 

Using the fact that for a variable V with a binomial distribution, $E[V] = np$, I can calculate $E[Br] = 5 * \frac{3}{4} = \frac{15}{4}$.

The expected number of children with brown eyes are $\frac{15}{4}$.

## Question nine

Calculating $E[I_E]$, we know that it is $1 * Pr(I_E = 1) + 0 * Pr(I_E = 0) = Pr(I_E = 1)$.

Let $D_i$ be the change on day i. We can say that $Pr(I_E) = Pr(D_1 = 1 \cap D_2 = 2 \cap D_3 = 0)$.

Since each of these random variables are independent, $Pr(D_1 = 1 \cap D_2 = 2 \cap D_3 = 0)$ becomes 
$Pr(D_1 = 1)Pr(D_2 = 2)Pr(D_3 = 0)$.

Using the values of $Pr(D_1 = 1) = 0.2, Pr(D_2 = 2) = 0.1,$ and $Pr(D_3 = 0) = 0.3$, 
$Pr(I_E)$ can be calculated as $0.3 * 0.2 * 0.1$. 








