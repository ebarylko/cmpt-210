## Question 1

### Suppose that we have found that the word “Rolex” occurs in 250 of 2000 messages known to be spam and in 5 of 1000 messages known not to be spam. Estimate the probability that an incoming message containing the word “Rolex” is spam, assuming that it is equally likely that an incoming message is spam or not spam.

Let $S$ be the event that a message is spam. $Pr(S) = \frac{1}{2}$.

By this fact, $Pr(S^{\complement}) = \frac{1}{2}$.

Let $R$ be the event that a message contains the word Rolex.

$Pr(R|S) = \frac{250}{2000} = \frac{1}{8}$.

$Pr(R|S^{\complement}) = \frac{5}{1000} = \frac{1}{200}$.

I must calculate $Pr(S|R)$.

$Pr(S|R) = \frac{Pr(S \cap R)}{Pr(R)}$

I have to calculate the value of $Pr(R)$. Using the Law of Total Probability,
$Pr(R) = Pr(R|S)Pr(S) + Pr(R|S^{\complement})Pr(S^{\complement})$

Using the values of $Pr(R|S) = \frac{1}{8}$, $Pr(S) = Pr(S^{\complement}) = \frac{1}{2}$, and 
$Pr(R|S^{\complement}) = \frac{1}{200}$ in the expression above, $Pr(R)$ becomes

$Pr(R) = \frac{1}{8}\frac{1}{2} + \frac{1}{200}\frac{1}{2}$

$Pr(R) = \frac{1}{8}\frac{1}{2} + \frac{1}{200}\frac{1}{2}$

$Pr(R) = \frac{26}{400} = \frac{13}{200}$

Now, I only need to calculate the value of $Pr(S \cap R)$.

By using Bayes rule, $Pr(S|R) = \frac{Pr(R | S)Pr(S)}{Pr(R)}$

By using the values  of $Pr(R|S) = \frac{1}{8}$, $Pr(S) = \frac{1}{2}$, and $Pr(R) = \frac{13}{200}$,
$Pr(S|R)$ simplifies to $\frac{1}{16}\frac{200}{13}$

$Pr(R|S)  = \frac{25}{26}$