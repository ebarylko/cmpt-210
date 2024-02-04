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

## Question 3
Suppose we made a loaded dice of 6 sides such that $Pr[1] = \frac{1}{16}, Pr[2] = Pr[3] = Pr[4] = Pr[5] = \frac{1}{8}$.
Calculate the probability of getting either a 1 or 3 or 6.


Let $S$ be the sample space of the possible dice rolls, where $S = (1, 2, 3, 4, 5, 6)$.

Let $R_i$ be the event where $i$ was rolled, $i \in S$.

We know that $Pr(S) = 1 = {\displaystyle\sum_{W \in S}^{} Pr(W)}$   

${\displaystyle\sum_{W \in S}^{} Pr(W)} = Pr(1) + Pr(2) +Pr(3) +Pr(4) +Pr(5) +Pr(6)$   

$Pr(1) + Pr(2) +Pr(3) +Pr(4) +Pr(5) +Pr(6) = \frac{1}{16} + 4\frac{1}{8} + Pr(6)$

$\frac{1}{16} + 4\frac{1}{8} + Pr(6) = 1$

$Pr(6) = 1 - \frac{9}{16} = \frac{7}{16}$

Since any subset of three events from $S$ is three ways disjoint (is there a proper term for three sets which are disjoint?)

Since we can only have one result after rolling the dice, we know that $Pr(R_1 \cup R_3 \cup R_6) = Pr(R_1) + Pr(R_3) + Pr(R_6)$ (using inclusion-exclusion theory)


$Pr(R_1 \cup R_3 \cup R_6) = \frac{1}{16} + \frac{1}{8} + \frac{7}{16} = \frac{10}{16} = \frac{5}{8}$

The probability of getting either a 1 or 3 or 6 is $\frac{5}{8}$.

## Question 4
An urn contains 10 white, 5 yellow, and 10 blue marbles. A marble is chosen at random.

### What is the probability it is yellow?
Since we are choosing randomly, this implies this is a uniform probability space. 

Let $S$ be the sample space consisting of all the balls in the urn.

This means that the probability of choosing a single marble is $\frac{1}{|S|} = \frac{1}{25}$.

Let $Y$ be the subset of all the yellow balls in the urn.

Pr(marble chosen is yellow) = $\frac{|Y|}{|S|} = \frac{5}{25} = \frac{1}{5}$

The probability that a yellow marble is chosen is $\frac{1}{5}$.

### We are told that the chosen marble is not blue. What is the probability it is yellow?
We must calculate Pr(chosen marble is yellow | chosen marble is not blue).

Let $M_y$ be the event that the chosen marble is yellow, and $M_b$ be the event that the chosen marble is not blue.

$Pr(M_y| M_b) = \frac{Pr(M_y \cap M_b)}{Pr(M_b)}$

$\frac{Pr(M_y \cap M_b)}{Pr(M_b)} = \frac{5}{25} * \frac{25}{15} = \frac{1}{3}$

Pr(chosen marble is yellow | chosen marble is not blue) = $\frac{1}{3}.

