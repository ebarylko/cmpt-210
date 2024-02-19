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

$Pr(S|R)  = \frac{25}{26}$

## Question two
### A plane is missing, and it is presumed that it was equally likely to have gone down in any of 3 possible regions. Let 1 − βi denote the probability that the plane will be found upon a search of region i when the plane is, in fact, in that region. What is the probability that the plane is in region i, given that a search in region 1 is unsuccessful?

Let $R_i$ be the event that a plane is in one of the i regions, $i \in (1, 2, 3)$. 
$Pr(R_1) = Pr(R_2) = Pr(R_3) = \frac{1}{3}$.

Let $S_i$ be the event that a search of the plane in region i successfully discovers the plane.

$Pr(S_i | R_i) = 1 - {\beta}_i$

I must calculate $Pr(R_i | {S_1}^{\complement})$.

Expanding out the above expression, it is 
$Pr(R_i | {S_1}^{\complement}) = \frac{Pr(R_i \cap {S_1}^{\complement})}{Pr({S_1}^{\complement})}$

I can calculate $Pr({S_1}^{\complement})$ by calculating $Pr(S_1)$ and then taking the complement.

Using the Law of Total Probability, $Pr(S_1) = Pr(S_1 | R_1)Pr(B_1) + Pr(S_1| {R_1}^{\complement})Pr({B_1}^{\complement})$ 

Using the fact that $Pr(S_1 | R_1) = 1 - {\beta}_1$, 
$Pr(S_1 | {R_1}^{\complement}) = 0$, $Pr(R_1) = \frac{1}{3}$, and that $Pr({R_1}^{\complement}) = 1 - Pr(R_1) = \frac{1}{3}$,
the above expression simplifies to 
$\frac{1 - {\beta}_1}{3}$.

As a result, $Pr({S_1}^{\complement}) = 1 - (\frac{1 - {\beta}_1}{3})$

$Pr({S_1}^{\complement}) = \frac{2 + {\beta}_1}{3}$

Using Bayes theorem, $Pr(R_i | {S_1}^{\complement})$ becomes  
$\frac{Pr({S_1}^{\complement} | R_i)Pr(R_i)}{Pr({S_1}^{\complement})}$

Let us now calculate the probabilities of
$\frac{Pr({S_1}^{\complement} | R_i)Pr(R_i)}{Pr({S_1}^{\complement})}$ for 
i = 1, 2, 3

#### i = 1

$\frac{Pr({S_1}^{\complement} | R_i)Pr(R_i)}{Pr({S_1}^{\complement})}$ 

Using $Pr({S_1}^{\complement}) = \frac{2 + {\beta}_1}{3}$, the above expression becomes

$\frac{Pr({S_1}^{\complement} | R_1)Pr(R_1)}{Pr({S_1}^{\complement})}$, which 
simplifies to ${\beta}_1\frac{1}{3}\frac{3}{2 + {\beta}_1}$.

The expression above further simplifies to $\frac{{\beta}_1}{2 + {\beta}_1}$

#### i = 2

$\frac{Pr({S_1}^{\complement} | R_i)Pr(R_i)}{Pr({S_1}^{\complement})}$  becomes

$\frac{Pr({S_1}^{\complement} | R_2)Pr(R_2)}{Pr({S_1}^{\complement})}$. Simplifying the expression 
by using $Pr({S_1}^{\complement} | R_2) = 1$, $Pr(R_2) = \frac{1}{3}$, and 
$Pr({S_1}^{\complement}) = \frac{2 + {\beta}_1}{3}$
we obtain

$\frac{1}{3}\frac{3}{2 + {\beta}_1} = \frac{1}{2 + {\beta}_1}$

#### i = 3

$\frac{Pr({S_1}^{\complement} | R_i)Pr(R_i)}{Pr({S_1}^{\complement})}$  becomes

$\frac{Pr({S_1}^{\complement} | R_3)Pr(R_3)}{Pr({S_1}^{\complement})}$. Simplifying the expression
by using $Pr({S_1}^{\complement} | R_3) = 1$, $Pr(R_3) = \frac{1}{3}$, and
$Pr({S_1}^{\complement}) = \frac{2 + {\beta}_1}{3}$
we obtain

$\frac{1}{3}\frac{3}{2 + {\beta}_1} = \frac{1}{2 + {\beta}_1}$

## Question three
Suppose that a standard deck of cards is shuffled and I pick 2 cards at random.

### What is the probability that exactly one of these cards is a spade card?

Since two cards are picked at random, I know I have a uniform probability space. 

Due to having a uniform probability space, $Pr(E) = \frac{|E|}{|S|}$, where $E$ is the event of 
interest and $S$ is the sample space.

Since $S$ is all the possible ways of picking pairs of cards, there are 
$\binom{52}{2}$ many ways of doing so. Therefore, $|S| = \binom{52}{2}$.

My event of interest is where only one of the two cards is a spade. Let $SP$ be a symbol denoting
this event.

In order to get the cardinality of $SP$, I must find all the ways of picking a single spade and 
any other card which is not a spade. There are 13 * 39 = 507 many pairs fulfilling these 
conditions, implying $|SP| = 507$.

Now that I have the cardinality of both $SP$ and $S$, I can solve for $Pr(SP)$.

Using the fact that $Pr(E) = \frac{|E|}{|S|}$, $Pr(SP) = \frac{|SP|}{|S|} = \frac{507}{\binom{52}{2}}$

### What is the probability that at least one of these cards is a spade card?

Let $MS$ be the event where at least one of the cards is a spade card.

To calculate $Pr(MS)$, I can calculate $Pr({MS}^{\complement})$ and then take its complement.

To calculate $Pr({MS}^{\complement})$, I must find all the ways of picking two cards which 
are not spades. There are $\binom{39}{2}$ many ways to do so. As a result of this, 
$|{MS}^{\complement}| = \binom{39}{2}$.

Using the properties of a uniform probability space, $Pr({MS}^{\complement}) = \frac{|{MS}^{\complement}|}{|S|}$

Using that $|{MS}^{\complement}| = \binom{39}{2}$ and $|S| = \binom{52}{2}$, the above expression
becomes $\frac{\binom{39}{2}}{\binom{52}{2}}$

Knowing the value of $Pr({MS}^{\complement})$, I can calculate $Pr(MS)$ by taking the 
complement of $Pr({MS}^{\complement})$, obtaining 1 -  $\frac{\binom{39}{2}}{\binom{52}{2}}$.

### If I know that at least one of the cards is a spade card, what is the probability that the other card is also a spade card.

$Let $BS$ be the event where both cards are spades.

I must calculate $Pr(BS | MS)$. Expanding this expression out, I obtain

$Pr(BS | MS) = \frac{Pr(BS \cap MS)}{Pr(MS)}$

$Pr(BS | MS) = \frac{\frac{\binom{13}{2}}{\binom{52}{2}}}{1 -  \frac{\binom{39}{2}}{\binom{52}{2}}}$

$Pr(BS | MS) = 0.13$
