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

Pr(chosen marble is yellow | chosen marble is not blue) = $\frac{1}{3}$.

## Question five

### Two integers are simultaneously chosen at random from {1, 2, 3, . . . , 100}. What is the probability that we chose {3, 5}?

Does the order of the numbers drawn matter? Is {3, 5} equivalent to {5, 3}

Assuming the order of the numbers does not matter.

Let $S$ be the sample space of pairs of numbers from the set of natural numbers from 1 to 100.

Since we draw two integers at random, this implies that $S$ is a uniform probability space. 

Pr(a pair is picked) = $\frac{1}{|S|} = \frac{1}{\binom{100}{2}}$.

Let $E$ be the event that the pair {3, 5} is picked. 

$Pr(E) = |E|\frac{1}{\binom{100}{2}} = \frac{1}{\binom{100}{2}}$

The probability that we chose {3, 5} is $\frac{1}{\binom{100}{2}}$.

##  Question six

### Two integers are chosen at random from {1, 2, 3, . . . , 100}, one after the other without putting the first back. What is the probability that we chose {3, 5}?

If we pick the first integer and then the second one afterwards, then it is the same as what we did above.

Ask professor if you are thinking about it wrong.

## Question seven

### Two teams A and B are asked to separately design a new product within a month. From past experience we know that, (a) The probability that team A is successful is 2/3, (b) The probability that team B is successful is 1/2, (c) The probability that at least one team is successful is 3/4. Assuming that exactly one successful design is produced, what is the probability that it was designed by team B.

If the teams separately design the products, then the success/failure of one team does not affect the other team in any way.

Let $A$ be the event that team A succeeds. $Pr(A) = \frac{2}{3}$.

Let $B$ be the event that team B succeeds. $Pr(B) = \frac{1}{2}$.

$Pr(B \cup A) = \frac{3}{4}$

Let $C$ be the event that only one team made a successful design.

$C = (A \cap \overline{B}) \cup (B \cap \overline{A})$

Calculate: Pr(B | C)

$Pr(B | C) = \frac{Pr(B \cap C)}{Pr(C)}$

$Pr(C) = Pr((A \cap \overline{B}) \cup (B \cap \overline{A}))  = Pr(A \cap \overline{B}) + Pr((B \cap \overline{A})) - Pr((A \cap \overline{B}) \cap (B \cap \overline{A}))$ (exclusion-inclusion theory)

Since $C$ is pairwise disjoint, this implies $Pr((A \cap \overline{B}) \cap (B \cap \overline{A})) = 0$

$Pr(C) =  Pr(A \cap \overline{B}) + Pr((B \cap \overline{A}))$

$Pr(C) = \frac{2}{3}\frac{1}{2} + \frac{1}{2}\frac{1}{3} = \frac{1}{2}$

$Pr(B \cap C) = Pr(B \cap ((A \cap \overline{B}) \cup (B \cap \overline{A})))$

$Pr(B \cap C) = Pr((B \cap A \cap \overline{B}) \cup (B \cap \overline{A}))$

$Pr(B \cap C) = Pr(\emptyset \cup (B \cap \overline{A}))$

$Pr(B \cap C) = Pr(B \cap \overline{A})$

$Pr(B \cap C) = \frac{1}{2}{1}{3} = \frac{1}{6}$

$Pr(B | C) = \frac{Pr(B \cap C)}{Pr(C)}$

$Pr(B | C) = \frac{1}{3}$

The probability that exactly one successful design is produced by team B is $\frac{1}{3}$

## Question eight
### Two players take turns flipping a fair coin. Whoever flips heads first is declared the winner. What is the probability that the first player wins?

Since we have a fair coin, the probability of obtaining a heads is equal to the probability of getting a tails, which is $\frac{1}{2}$.

Let $O$ represent the set of odd natural numbers.

Let $P_i$ represent the event that the first player wins on the ith turn, $i \in O$.

$P_1$ = \frac{1}{2}$.

$P_3$ = \frac{1}{2}\frac{1}{2}\frac{1}{2} = \frac{1}{8}$.

$P_5$ = \frac{1}{2}\frac{1}{2}\frac{1}{2}\frac{1}{2} \frac{1}{2}  = \frac{1}{32}$.

$P_i = 2^{-i}$.

To account for the probability of the first player always winning, I must sum the probabilites of winning under every 
possible turn.

When calculating $Pr(P_1 \cup P_2 + ..... P_n)$, Since each event is disjoint from the others, I know that
$Pr(P_1 \cup P_2 + ..... P_n) =  Pr(P_1) + Pr(P_2) + ..... Pr(P_n).

I end up with $\frac{1}{2} + \frac{1}{8} + \frac{1}{32} + ..... \frac{1}{2^n}$. Since this is a geometric series, 
with $r = \frac{1}{4}, a = \frac{1}{2}$.

$Pr(P_1 \cup P_2 + ..... P_n) = \frac{\frac{1}{2}}{1 - \frac{1}{4}} = \frac{2}{3}$

The probability that the first player wins is $\frac{2}{3}$.