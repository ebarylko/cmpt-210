## Question 1 
Since there is an equal probability of buying any of the tickets, the probability of buying a ticket is equal 
to $\frac{1}{100}$.

Let $W$ be the event where we win after buying two tickets. 

Let $S$ be the set of all 100 lottery tickets.

Let $T_1$ be the event where the first ticket was the winning ticket, and $T_2$ the 
event where the second ticket was the winning ticket.

$W = T_1 \cup T_2$

$pr(W) = pr(T_1) + pr(T_2) - pr(T_1 \cap T_2)$

Since we can only have one winning ticket, we know that the events $T_1$ and $T_2$ are disjoint, implying that
$pr(T_1 \cap T_2) = 0$.

Since we have a uniform probability space, we know that $pr(W) = |W| * pr(T_1) = 2 * \frac{1}{100} = \frac{1}{50}$

The probability that you win is $\frac{1}{50}$.

Could I use exclusion inclusion theory or the properties of uniform probability spaces to solve this question?

## Question 2

You shuffle a deck of cards and deal your friend 5 cards.

### What is the probability that they have exactly one ace in their 5 cards?

If they have exactly one ace in their hand, this means that the remaining cards must be of any other denomination.

There are $\binom{4}{1}$ ways to pick an ace. 

There are $\binom{48}{4}$ ways to pick the remaining four cards which are not aces.

In total, there are
$\binom{4}{1}\binom{48}{4}$ ways to deal five cards such that the 
friend has exactly one ace in their 5 cards.

The number of ways of dealing five cards is $\binom{52}{5}$ many ways.

The probability that the friend has exactly one ace in their 5 cards is 
$\frac{\binom{4}{1}\binom{48}{4}}{\binom{52}{5}}$.

### What is the probability that they have the ace of spades in their 5 cards?

Since they must have the ace of spades, we must find the ways of dealing four cards from the remaining 51 cards.
There are $\binom{51}{4}$ ways of picking four cards from the remaining cards.

Using the number of ways of dealing five cards from the last sub question,
The probability that the friend has the ace of spades in their 5 cards is
$\frac{\binom{51}{4}}{\binom{52}{5}}$.
