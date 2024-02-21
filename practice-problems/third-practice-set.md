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

Revise this question.

$Let $BS$ be the event where both cards are spades.

I must calculate $Pr(BS | MS)$. Expanding this expression out, I obtain

$Pr(BS | MS) = \frac{Pr(BS \cap MS)}{Pr(MS)}$

$Pr(BS | MS) = \frac{\frac{\binom{13}{2}}{\binom{52}{2}}}{1 -  \frac{\binom{39}{2}}{\binom{52}{2}}}$

$Pr(BS | MS) = 0.13$

## Question four

Prove that if $E_1$ and $E_2$ are independent, so are ${E_1}^{\complement} and {E_2}^{\complement}$

Since $E_1$ and $E_2$ are independent, this implies that $Pr(E_1E_2) = Pr(E_1)Pr(E_2)$.


$Pr({E_1}^{\complement}{E_2}^{\complement}) = \overline{Pr(E_1 \cup E_2)}$ (by De Morgan)

$Pr({E_1}^{\complement}{E_2}^{\complement}) = \overline{Pr(E_1 \cup E_2)}$

Expanding out $\overline{Pr(E_1 \cup E_2)}$, we obtain $\overline{Pr(E_1) + Pr(E_2) - Pr(E_1 \cap E_2)}$,
which is equivalent to  $1 - Pr(E_1) - Pr(E_2) + Pr(E_1 \cap E_2)$.

We now have that
$Pr({E_1}^{\complement}{E_2}^{\complement})  = 1 - Pr(E_1) - Pr(E_2) + Pr(E_1 \cap E_2)$

We can rewrite the expression as
$Pr({E_1}^{\complement}{E_2}^{\complement})  = (1 - Pr(E_1))(1 - Pr(E_2))$, which is 
equivalent to  
$Pr({E_1}^{\complement}{E_2}^{\complement})  = Pr({E_1}^{\complement})Pr({E_2}^{\complement})$.

The above statement proves that $E_1$ and $E_2$ being independent implies the 
independence of ${E_1}^{\complement}$ and ${E_2}^{\complement}$.

## Question five

Suppose that we flip three fair, mutually-independent coins. Define the following events: E1 is the event
that coin 1 matches coin 2, E2 is the event that coin 2 matches coin 3 and E3 is the event that coin 3
matches coin 1.

### Are E1, E2 and E3 pairwise independent?

If $E_1, E_2,$ and $E_3$ are pairwise independent, then it means that for every pair of events 
$E_i, E_j, i, j \in (1, 2, 3), Pr(E_iE_j) = Pr(E_i)Pr(E_j)$

No matter what pair of events are picked, I am always checking whether $Pr(\text{coin i matches coin j})$ 
influences $Pr(\text{coin i matches coin k})$, for $i, j, k \in (1, 2, 3)$, where i, j, k take on 
one of the values in (1, 2, 3). 

Regardless of if coins i and j match, I will still have a 50% chance of coins i and k 
matching or not matching. This comes from the fact that the coins are mutually independent.

Therefore, events $E_1, E_2$, and $E_3$ are pairwise independent.

### Are E1, E2 and E3 mutually independent?

If $E_1, E_2,$ and $E_3$ are mutually independent, then that means that all the events are 
independent. As a consequence of this, $Pr(E_1 \cap E_2 \cap E_3) = Pr(E_1)Pr(E_2)Pr(E_3)$

However, if $E_1$ and/or $E_2$ occur or do not occur, then that affects the probabilities of
$E_3$ occurring. 

If coins one and two match, and coins two and three match, then coins three and one must match.
Similarly, if coins one and two match, but coins two and three do not match, then coins one and
three will not match.

Since the results of the first two events decide the outcome of the third event, these set of 
events in not mutually independent.

## Question six
### Prove that CDF is an increasing function i.e. if a ≤ b, then CDF[a] ≤ CDF[b].

We know that by definition CDF(a) is equivalent to $Pr(X \le a)$.

Since $a \le b$, then $CDF(b)$ is equivalent to $CDF(a)$ + 
${\displaystyle\sum_{a < i \le b}^{}} Pr(X = i)$  

For the expression ${\displaystyle\sum_{a < i \le b}^{}} Pr(X = i)$, it takes on a 
non-negative value. Therefore,
${\displaystyle\sum_{a < i \le b}^{}} Pr(X = i) + CDF(a) \ge CDF(a)$.

Since ${\displaystyle\sum_{a < i \le b}^{}} Pr(X = i) = CDF(b)$, we can say that 
$CDF(b) \ge CDF(a)$.


## Question seven
 Three balls are to be randomly selected (without replacement) from an urn containing 20 balls numbered 1 through 20. The random variable M is the maximal value on the selected balls.

### Calculate Pr[M = 5]?

If I randomly select three balls, this means the probability of selecting one triplet is the 
same as selecting a distinct triplet. Therefore, I have a uniform probability space.

For $Pr(M = 5)$, this evaluates to $\frac{|\text{set of all triplets where five is the maximum value}|}{|S|}$,
where $|S|$ is the sample space consisting of all possible triplets.

$|S| = \binom{20}{3}$.

Let $M5$ be the event where a selected triplet has five as the maximum value. To count 
the cardinality of this event, I must find all the ways of generating a triplet where 
five is the largest value.

To do this, I can select five as one of the balls and then choose 2 balls from (1, 2, 3, 4).
I can do this in $\binom{4}{2}$ many ways. Therefore, $|M5| = \binom{4}{2}$

Now that I have calculated $|M5|$, I can obtain the value of $Pr(M5)$.

Using the fact that I am within a uniform probability space, $Pr(M5) = \frac{|M5|}{|S|}$.

$Pr(M5) = \frac{\binom{4}{2}}{\binom{20}{3}}$.

### Completely specify the PDF(M)

${PDF}_M(x) = \frac{\binom{x - 1}{2}}{\binom{20}{3}}, 0 < x \le 20$. 

### Completely specify the CDF(M)?

${CDF}_M(x) = {\displaystyle\sum_{i = 1}^{x}} \frac{\binom{x - 1}{2}}{\binom{20}{3}}, 0 < x \le 20$. 



