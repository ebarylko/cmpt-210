## Question one

### What is the probability that he breaks exactly 2 out of the 5 boards that are placed before him?
Since each board is independent and the probability he breaks each board is the same, I can model the 
number of boards broken by a binomial distribution.

Let $B$ be the number of boards broken. $B \sim Bin(5, 0.8)$.

$Pr(B = 2) = \binom{5}{2}(0.8)^2(0.2)^3 = 0.0512$.

### What is the probability that he breaks at least 3 out of the 5 boards that are placed before him
To calculate $Pr(B \ge 3)$, this is equivalent to finding the value of $1 - Pr(B \le 2)$.

I already have $Pr(B = 2)$ from the question above, and I must find the values of $Pr(B = 1)$ and 
$Pr(B = 0)$.

Calculating $Pr(B = 1)$ and $Pr(B = 0)$, I find them to be $\binom{5}{1}(0.8)(0.2)^4$ and $\binom{5}{0}(0.2)^5$ respectively.

Summing up $Pr(B = 2), Pr(B = 1),$ and $Pr(B = 0)$, I have that $Pr(B \le 2) = 0.05792$.

Using this value, I have that $Pr(B \ge 3) = 1 - Pr(B \le 2) = 0.94208$.

### If 10 boards are placed before him, what is the expected number of boards that he will break?
Using the fact that the expectation for a binomally distributed R.V. is np, I can calculate 
$E[B]$ as $E[B] = 10 * \frac{4}{5} = 8$.

The expected number of boards that Bruce will break is eight.

### In order to challenge Bruce Lee, he now has to break the bricks placed before him until he fails. He can break a brick with probability 0.2. He starts breaking the bricks one by one, but as soon as he fails, the challenge is over. On average, how many bricks will he attempt to break before the challenge is over
Given that Bruce breaks each brick with probability $\frac{1}{5}$ and we are wishing to find the number of bricks he will break 
before his last attempt fails, we can model this situation with a geometric distribution.

Let $F$ be the r.v. denoting the number of bricks that Bruce attempted to break, where the last brick could not be broken.
$F \sim Geo(\frac{1}{5})$.

Using the fact that for any geometrically distributed r.v. X, $E[X] = \frac{1}{p}$, we can calculate the expected value of 
F to be $\frac{1}{\frac{1}{5}} = 5$.

Bruce will break an average of five blocks before he fails to break the next block. 

## Question two

### Fully specify the PDF for X

From the $CDF$, we can see that the $PDF$ has non-zero probabilities for $x \in \set{0, 1, 2, 3}$.

Given the value of $F(0)$, we know that it is equivalent to $Pr(X = 0)$ since there is no other element smaller than 
zero with a non-zero probability. Therefore, $Pr(X = 0) = \frac{1}{2}$.

Using the value of $F(0)$, I can calculate $Pr(X = 1)$ by calculating $F(1) - F(0)$, which is equivalent to $Pr(x \le 1) - Pr(x \le 0)$. 
Doing this, I have that $Pr(x = 1) = \frac{2}{3} - \frac{1}{2} = \frac{1}{6}$.

Repeating the process above with $F(1)$ and $F(2)$ to calculate $Pr(X = 2)$, I obtain that $Pr(X = 2) = \frac{11}{12} - \frac{2}{3} = \frac{3}{12} = \frac{1}{4}$.

In order to find $Pr(X = 3)$, I can calculate it by doing $F(3) - F(2) = 1 - \frac{11}{12} = \frac{1}{12}$.

Using the values I calculated above, I can fully specify the PDF.

$Pr(X = 0) = \frac{1}{2}$.

$Pr(X = 1) = \frac{1}{6}$.

$Pr(X = 2) = \frac{1}{4}$.

$Pr(X = 3) = \frac{1}{12}$.

### Calculate Pr[X ≤ 2]
I know that $Pr(X \le 2) = F(2)$. Reading off the value of $F(2)$, I have that
$Pr(X \le 2) = \frac{11}{12}$.

### Calculate Pr[2 < X ≤ 4].

Taking the expression $Pr(2 < x \le 4)$, we can convert it to the equivalent expression $Pr(3 \le x \le 4)$ since we are 
looking at a discrete distribution.

Noting that my distribution only contains non-zero probabilities for $x \in \set{0, 1, 2, 3}$,
$Pr(3 \le x \le 4)$ can be also be represented as $Pr(3 \le x \le 3) = Pr(X = 3)$.

Using the values of the $PDF$ computed in the last question, $Pr(X = 3) = Pr(2 < x \le 4) = \frac{1}{12}$.

### Calculate E[X], E[X^2], Var[X]

Using the formula of $E[X] = {\displaystyle\sum_{x \in X}^{}} x * Pr(X = x)$, the value of $E[X]$ can be calculated 
as $0 * \frac{1}{2} + 1 * \frac{1}{6} + 2 * \frac{1}{4} + 3 * \frac{1}{12} = \frac{11}{12}$.

Using the formula of $E[g(X)] = {\displaystyle\sum_{x \in X}^{}} g(x) * Pr(X = x)$ with $g(x) = x^2$,
the value of $E[X^2]$ can be calculated as $0 * \frac{1}{2} + 1 * \frac{1}{6} + 4 * \frac{1}{4} + 9 * \frac{1}{12} = \frac{23}{12}$.

Using the fact that $Var[X] = E[X^2] - (E[X])^2$ and that $E[X] = \frac{11}{12}$ and $E[X^2] = \frac{23}{12}$, 
the value of $Var[X]$ is $\frac{23}{12} - \frac{121}{144} = \frac{155}{144}$.

### Calculate Pr[X = 2|X ≥ 2]

$Pr(X = 2 | X \ge 2) = \frac{Pr(X = 2 \cap X \ge 2)}{Pr(X \ge 2} = \frac{Pr(X = 2}{Pr(X \ge 2)}$.

Using the value for $Pr(X = 2) = \frac{1}{4}$ from part one of the question and that $Pr(X \ge 2) = F(3) - F(1) = 1 - \frac{2}{3} = \frac{1}{3}$,
I can calculate the value of the expression above.

$Pr(X = 2 | X \ge 2)  = \frac{\frac{1}{4}}{\frac{1}{3}} = \frac{3}{4}$ .

### Calculate E[X|X ≥ 2]

Using the formula for conditional expectation $E[X | A]  = {\displaystyle\sum_{x \in X}^{}} x * Pr(X = x| A)$, $E[X | X \ge 2]$ 
can be calculated as $0 * Pr(X = 0 | X \ge 2) + 1 * Pr(X = 1| X \ge 2) + 2 * Pr(X = 2 | X \ge 2) + 3 * Pr(X = 3 | X \ge 2)$.

Since $Pr(X = x | X \ge 2)$ only has non-zero probability for $x \ge 2$, the first two terms in the expectation disappear.

To evaluate what remains of the expectation, I must calculate the value of $Pr(X = 3 | X \ge 2)$.

Expanding out the expression, I obtain that it is equivalent to $\frac{Pr(X = 3)}{Pr(X \ge 2)} = \frac{\frac{1}{12}}{\frac{1}{3}} = \frac{1}{4}$.

Using the values of $Pr(X = 2 | X \ge 2) = \frac{3}{4}$ and $Pr(X = 3 | X \ge 2) = \frac{1}{4}$, the value of the 
conditional expectation is $2 * \frac{3}{4} + 3 * \frac{1}{4} = \frac{9}{4}$.

## Question three

### Part 1

I will now prove that
${\displaystyle\sum_{k = 0}^{n}k \binom{n}{k}x^k y^{n - k}} = nx(x + y)^{n - 1}$.

Start of proof:

${\displaystyle\sum_{k = 0}^{n}k \binom{n}{k}x^k y^{n - k}} = {\displaystyle\sum_{k = 0}^{n}k \frac{n!}{k!(n - k)!}x^k y^{n - k}}$.

Dividing by a factor of $k$ on the numerator and denominator, we obtain
${\displaystyle\sum_{k = 1}^{n} \frac{n!}{(k - 1)!(n - k)!}x^k y^{n - k}}$.

We can then take out a factor of n and x from the expression, resulting in 
$nx{\displaystyle\sum_{k = 1}^{n - 1} \frac{(n - 1)!}{(k - 1)!(n - k)!}x^{k - 1} y^{n - k}}$.

We can simplify the expression above by defining $t$ to be $t = k -1$, resulting in $k = t + 1$. Substituting in the 
value of t in the expression above, we obtain 
$nx{\displaystyle\sum_{t = 0}^{n - 1} \frac{(n - 1)!}{(t)!(n - t - 1)!}x^{t} y^{n - t - 1}}$, which is equivalent to
$nx{\displaystyle\sum_{t = 0}^{n - 1} \binom{n - 1}{t}x^{t} y^{n - t - 1}},$ which is 
equivalent to $nx(x + y)^{n - 1}$.

End of proof.

### Part 2

Since I derived $E[X] = nx(x + y)^{n - 1}$ from
${\displaystyle\sum_{k = 0}^{n}k \binom{n}{k}x^k y^{n - k}} = nx(x + y)^{n - 1}$, I know that 
for a binomially distributed r.v, x represents p and $y$ represents $1 - p$. Subbing in $x = p$ and 
$y = 1 - p$ into the expression $E[X] = nx(x + y)^{n - 1}$, I obtain 
$E[X] = np(p + (1 - p))^{n - 1} = np(1)^{n - 1} = np$

## Question four

### Prove Pr[X = i] = Pr[X ≥ i] − Pr[X ≥ i + 1] 
$Pr(X \ge i) = {\displaystyle\sum_{t \ge i}^{}} Pr(X = t)$

$Pr(X \ge i + i) = {\displaystyle\sum_{t \ge i + i}^{}} Pr(X = t)$

Taking the difference between $Pr(X \ge i)$ and $Pr(X \ge i + 1)$, I have that the only term that does not 
cancel out is $Pr(X = i)$.

Therefore, $Pr[X = i] = Pr[X ≥ i] − Pr[X ≥ i + 1]$.

### Part 2
Using the formula for expectation, it is  ${\displaystyle\sum_{x \in X}^{}} x * Pr(X = x)$.
Substituting the value for $Pr(X = x)$ I have from the question above, the expression becomes
${\displaystyle\sum_{x \in X}^{}} x * (Pr(X \ge i) - Pr(X \ge i + i))$.

Distributing the x in the expression above, we obtain
${\displaystyle\sum_{x \ge 1}^{}} xPr(X \ge x) -  {\displaystyle\sum_{x \ge 1}^{}}xPr(X \ge x + 1)$.

To simplify the above expression, let us define $k$ such that $k = x + 1$. Using the value of $k$ in the  
second summation above with $x = k -1$ resulting as a consequence of the definition, the expression becomes 
${\displaystyle\sum_{x \ge 1}^{}} xPr(X \ge x) -  {\displaystyle\sum_{k \ge 2}^{}}(k - 1)Pr(X \ge k)$.

Expanding out the expression, we obtain
${\displaystyle\sum_{x \ge 1}^{}} xPr(X \ge x) -  {\displaystyle\sum_{k \ge 2}^{}}kPr(X \ge k) + {\displaystyle\sum_{k \ge 2}^{}}Pr(X \ge k)$. 

We can note that for $x$ and $k$ greater than or equal to two,  ${\displaystyle\sum_{x}^{}} xPr(X \ge x) -  {\displaystyle\sum_{k}^{}}kPr(X \ge k)$
will cancel out, leaving the original expression as ${\displaystyle\sum_{x = 1}^{1}} xPr(X \ge x) + {\displaystyle\sum_{k \ge 2}^{}}Pr(X \ge k)$.
Substituting the value of $x = 1$ into the first expression, we obtain $1*Pr(X \ge 1) + {\displaystyle\sum_{k \ge 2}^{}}Pr(X \ge k)$.

Summing together these expressions, we obtain that they are equivalent to ${\displaystyle\sum_{k \ge 1}^{}}Pr(X \ge k)$

Therefore, we have proven that $E[X] = {\displaystyle\sum_{k \ge 1}^{}}Pr(X \ge k)$.

### Part 3

Using the value of $E[X]$ obtained above for computing $E[R]$, we obtain
$E[R] = {\displaystyle\sum_{k \ge 1}^{}}Pr(R \ge k)$

For $Pr(R \ge 1)$, this evaluates to 1 since I will always need at least one attempt of whatever I am doing in order to gain a success 
immediately or after some n - 1 failures. 

For the remaining terms in ${\displaystyle\sum_{k \ge 2}^{}}Pr(R \ge k)$, I can always factor out a $(1 - p)^{k - 1}$ 
term since if $R \ge k$, this means that I have at least $k - 1$ failures before I must account for all the combinations of 
successes and failures that can occur in the following events. 

I can then think of the summation in two different parts, one part in which is the probability of the minimum amount of 
failures and the other part which is the probability of every possible event that can occur after the minimum amount of 
failures occurring. By doing this, I can think of $Pr(R \ge k)$ as $Pr(X, Y)$, where $X$ indicates the number of 
minimum failures and $Y$ is the set of all events that can follow after the minimum amount of failures.

I can then change ${\displaystyle\sum_{k \ge 2}^{}}Pr(R \ge k)$ to ${\displaystyle\sum_{\forall x \ge 1}{} Pr(X)Pr(Y| X)}$.

After summing over all the possible events $y \in Y$, my expression above becomes
${\displaystyle\sum_{\forall x \ge 1}{} Pr(X)}$. I know this expression is equivalent to 
${\displaystyle\sum_{i \ge 1}{} (1- p)^{i}}$.

Summing this expression with the value obtained for $Pr(R \ge 1)$, I have that the summation becomes
${\displaystyle\sum_{i \ge 0}{} (1- p)^{i}}$.

Using the geometric sum formula with a = 1 and r = 1 - p, the summation of this series becomes $\frac{1}{1 - (1 - p)}$, which 
is $\frac{1}{p}$ after simplifying the expression.

Since we obtained this value by manipulating the expression $E[R]$, we can conclude that $E[R] = \frac{1}{p}$.

## Question five

### Part 1
Since there are n audience members voting where each member has the same probability of voting for Adele and 
each audience member's vote is independent of the others, the distribution of $X_{Adele}$ can be 
modeled as a binomial distribution. 

$X_{Adele} \sim Bin(n, p_{Adele})$.

Since $X_{Adele}$ is binomally distributed, we know that $E[X_{Adele}] = np = np_{Adele}$.

### Part 2

The joint PDF is $PDF_{i, j, k} = \binom{n}{i, k, k}p_{Adele}^i p_{Lizzo}^j p_{Taylor}^k$

### Part 3

Given that $n = 8, p_{Adele} = 0.5, p_{Lizzo} = 0.3$, and $p_{Taylor} = 0.2$, the value of 
$PDF_{4, 2, 2} = \frac{8!}{4!(2!)^2}(0.5)^4 (0.3)^2 (0.2)^2 = 0.095$

### Part 4
Since I only wish to compute the probabilities that Adele receives three votes, this is the same as 
taking the joint pdf and then summing over the possible values that j and k can take on, obtaining 
$X_{Adele}$ as the result. 

For calculating the probability that Adele receives three votes, it is the same as $Pr(X_{Adele} = 3) = \binom{8}{3}(0.5)^3(0.5)^5 = 0.219$.

### Part 5

If Adele receives three votes, Lizzo receives three votes, and Taylor receives two votes, the probability 
of this occurring is $Pr(\text{Lizzo and Taylor receive 3 and 2 votes}| \text{Adele received three votes})$, which 
is equivalent to $\frac{PDF_{3, 3, 2}}{Pr(X_{Adele} = 3}$ using the definition of conditional probability.

Taking the joint $PDF_{i, j, k}$ for $i = 3, j = 3, k = 2$, we obtain 
$\binom{8}{3, 3, 2} (0.5)^3 * (0.3)^3 * (0.2)^2 = 0.0756$.

Using the value of $Pr(X_{Adele} = 3) = 0.219$ from the previous question, we can expand 
$Pr(PDF_{3,3, 2} | X_{Adele} = 3) = \frac{PDF_{3,3, 2}}{ Pr(X_{Adele} = 3)} = 0.35$

## Question six

### Part 1
Since the bullets are placed randomly in any of the chambers, the probability that a bullet is in any specific chamber is 
$\frac{1}{6}$. 

Let $S$ be the event that the hero is shot the first time. We know that $S$ occurs if the 
chamber landed after spinning the cylinder contains the first bullet or the second bullet.

Let $FB$ and $SB$ be the event that the chamber landed on contains the first bullet and second bullet respectively.

We can then say that $S = (S \cap FB) \cup (S \cap SB)$. Since these events are disjoint, this means that 
$Pr(S) = Pr(S \cap FB) + Pr(S \cap SB)$. 

Since we wish to sum up the probabilities that we landed on the first or second chamber and it is known that 
the bullets are distributed uniformly (meaning that Pr(bullet is in a specific chamber) = $\frac{1}{6}$), 
$Pr(S) = 2 * \frac{1}{6} = \frac{1}{3}$.

### Part 2

Let $SS$ be the event that the hero is shot on the second attempt and $M$ be the event the gangster misses on the first attempt.

We want to calculate $Pr(SS | M)$, which is equivalent to $\frac{Pr(SS \cap M)}{Pr(M)}$.

To calculate $Pr(SS \cap M)$, we must count all the ways in which the hero can get shot on the second attempt.
Given that the first attempt failed and the second attempt succeeded, we know that one bullet must be in the chamber adjacent to 
the one used on the first attempt and that another bullet can be in any of the four remaining chambers. This means there 
are four possible location combinations which result in the hero getting shot. Since this number only considers the case where the first 
bullet is the one used when shooting the hero, we add four additional cases to account for when the second bullet is used for 
shooting the hero. Since we have a uniform probability space and there are $\binom{6}{2} * 2$ ways to place two bullets in 
the six chambers, we can calculate $Pr(SS \cap M) = \frac{|SS \cap M|}{|S|}$,  where $S$ is the sample space. This expression simplifies to
$\frac{8}{30} = \frac{4}{15}$.

Now, we nee to calculate $Pr(M)$ in order to obtain the value of $Pr(SS | M)$. We can calculate $Pr(M)$ by taking the 
complement of $Pr(S)$ (using the value of $Pr(S)$ defined in the previous question) , having that $Pr(M) = 1 - Pr(S) = 1 - \frac{1}{3} = \frac{2}{3}$.

Using the values of $Pr(SS \cap M) = \frac{4}{15}$ and $Pr(M) = \frac{2}{3}$, we can calculate
$\frac{Pr(SS \cap M)}{Pr(M)}$ to be $\frac{4}{15} * \frac{3}{2} = \frac{2}{5}$.

### Part 3
Since the gangster spins the cylinder, it is equally probable that we land on any chamber. Since the bullets continue to 
be randomly distributed after spinning the cylinder once more, the probability the hero gets shot on the third 
attempt is the probability of landing on the first or second chamber which contains a bullet.

Let $TS$ be the event that the hero is shot on the third attempt. Using the fact that Pr(bullet is in chamber i) = $\frac{1}{6}$, we can 
calculate Pr(TS) as Pr(TS) = Pr(bullet lands on chamber with bullet 1) + Pr(bullet lands on chamber with bullet 2) = $\frac{1}{6} * 2 = \frac{1}{3}$.

### Part 4

The expression $Pr(S > i + 1| S > i)$ means the probability that I need more than i + 1 shots given that I missed the i shots.
This can only occur if I missed the (i + 1)th shot. 
Let $M_{i}$ be the event that the villain misses on the ith shot. 

I then need to calculate $Pr(M_{i + 1} | M_i)$. Since I started out with four chambers which were empty, 
I know that missing the first i shots will leave me with $4 - i$ empty chambers and $6 - i$ unused chambers.
Using the fact that this is a uniform probability space, I know that 
$Pr(M_i) = \frac{|\set{\text{All empty chambers at the ith shot}}|}{|\set{\text{All unused chambers}}|}$. 

Since $Pr(M_{i + 1} | M_i)$ is asking for the probability that we miss the (i + 1)th shot given we miss the first 
i shots, I know that the number of empty chambers is $4 - i$, and the number of unused chambers is $6 - i$. 
Therefore, $Pr(M{i + 1} | M_i) = Pr(S > i  + 1| S > i) = \frac{4 - i}{6 - i}$.

### Part 5

My inductive hypothesis is $\forall i \in \set{1, 2, 3, 4}, Pr(S > i) = \frac{(6 - i)(5 - i)}{30}$.

I will now prove the base case for $i = 1$:

$Pr(S > 1) = 1 - Pr(S = 1) = 1 - \frac{1}{3} = \frac{2}{3}$.

Calculating the value of $\frac{(6 - i)(5 - i)}{30}$ when $i = 1$, we obtain 
$\frac{20}{30} = \frac{2}{3}$.

Seeing that $Pr(S > 1) = \frac{(6 - i)(5 - i)}{30}$ when i = 1, this hypothesis holds true for when $i = 1$.

My inductive step will be proving that for $i = 5$, $Pr(S  > 5) = \frac{(6 - (i + 1))(5 - (i + 1))}{30}$.

To start, I note that $Pr(S > i + 1 | S > i) = \frac{Pr(S > i + 1)}{Pr(S > i)}$, meaning that 
$Pr(S > i + 1) = Pr(S > i + 1 | S > i)Pr(S > i)$.

Using the values of $Pr(S > i + 1 | S > i) = \frac{4 - i}{6 - i}$ and $Pr(S > i) = \frac{(6 - i)(5 - i)}{30}$ (from the inductive hypothesis) in 
the expression above, $Pr(S > i + 1)$ becomes $\frac{(4 - i)(6 - i)(5 - i)}{30(6 - i)}$, which simplifies to $\frac{(4 - i)(5 - i)}{30}$. 

We can modify the expression above to be equivalent to $\frac{(5 - (i + 1))(6 - (i + 1))}{30}$, which is 
the value we wished to obtain.

Since we were able to show that $Pr(S > i + 1) = \frac{(6 - (i + 1))(5 - (i + 1))}{30}$ for $i = 5$, we have proved that 
the inductive hypothesis is true for $i \in \set{1, 2, 3, 4, 5}$.


### Part 6

Using the value of $Pr(S > 5) = 0$ from the subquestion above, I know this is equivalent to $Pr(S = 6) = 0$.

For the value of $Pr(S = 5)$ I can calculate $Pr(S > 4) = Pr(S = 5) + Pr(S = 6)$.

Knowing that $Pr(S = 6) = 0$ and that $Pr(S > 4) = \frac{1}{15}$, I can substitute these values above to 
obtain $\frac{1}{15} = Pr(S = 5)$.

To calculate $Pr(S = 4)$, I can use the value of $Pr(S > 3) = Pr(S = 4) + Pr(S = 5) + Pr(S = 6)$.

Utilizing that $Pr(S = 6) = 0, Pr(S = 5) = \frac{1}{15}, Pr(S > 3) = \frac{1}{5}$ in the expression above, substituting 
these values allow us to obtain $\frac{1}{3} = Pr(S = 4) + \frac{1}{15}$, which can be rearranged to obtain 
$Pr(S = 4) = \frac{1}{5} - \frac{1}{15} = \frac{2}{15}$.

The value of $Pr(S = 3)$ can be obtained by using $Pr(S > 2) = Pr(S = 3) + Pr(S = 4) + Pr(S = 5) + Pr(S = 6)$.
Utilizing that $Pr(S = 6) = 0, Pr(S = 5) = \frac{1}{15}, Pr(S = 4) = \frac{2}{15}, Pr(S > 2) = \frac{2}{5}$, the 
expression above changes to $\frac{2}{5} = Pr(S = 3) + \frac{2}{15} + \frac{1}{15}$. Rearranging 
the terms, we obtain that $Pr(S = 3) = \frac{1}{5}$.


The value of $Pr(S = 2)$ can be obtained by using $Pr(S > 1) = Pr(S = 2) + Pr(S = 3) + Pr(S = 4) + Pr(S = 5) + Pr(S = 6)$.
Utilizing that $Pr(S = 6) = 0, Pr(S = 5) = \frac{1}{15}, Pr(S = 4) = \frac{2}{15}, Pr(S = 3) = \frac{1}{5}, Pr(S > 1) = \frac{2}{3}$, the
expression above changes to $\frac{2}{3} = Pr(S = 2) + \frac{1}{5} + \frac{2}{15} + \frac{1}{15}$. Rearranging
the terms, we obtain that $Pr(S = 2) = \frac{4}{15}$.

The value of $Pr(S = 1)$ can be obtained by noting that $1 = Pr(S = 1) + Pr(S = 2) + Pr(S = 3) + Pr(S = 4) + Pr(S = 5) + Pr(S = 6)$.
Utilizing that $Pr(S = 6) = 0, Pr(S = 5) = \frac{1}{15}, Pr(S = 4) = \frac{2}{15}, Pr(S = 3) = \frac{1}{5}, Pr(S = 2) = \frac{4}{15}$,
the expression above changes to $Pr(S = 1) = 1 - \frac{1}{15} - \frac{2}{15} - \frac{1}{5} - \frac{4}{15}$. Simplifying this,
we obtain that $Pr(S = 1) = \frac{1}{3}$.

## Question seven


### Part 1

Assuming the balls are drawn randomly from the urn, we have a uniform probability space where the probability of 
picking any set of n balls from the urn is $\frac{1}{\binom{N}{n}}$.

Let U be the event that there are $k$ white balls in the $n$ balls selected from the urn. We need to calculate all the 
ways to select the k white balls and the $n - k$ non-balls in the n balls we pick from the urn.

Since we want to calculate all the ways of picking k white balls from the set of w balls, this can be done in 
$\binom{w}{k}$ many ways.

We also need to count the number of ways to pick the non-white balls in the urn. Since there are $N - w$ non-white 
balls and we want to pick $n - k$ non-white balls, there are $\binom{N - w}{n - k}$ 
many ways to pick the non-white balls.

Using the fact we have a uniform probability space, $Pr(U) = \frac{|U|}{|S|}$, where $S$ is the sample space of all 
possible ways to select n balls from the urn. Knowing that $|S| = \binom{N}{n}$ and $|U| = \binom{n}{k}$, $Pr(U)$ 
can be calculated as $\frac{\binom{w}{k} \binom{N - k}{n - k}}{\binom{N}{n}}$

### Part 2
The domain of $X$ would be $[0, n]$ since we could draw no white balls in the worst case and then have that all the balls
selected are white.

### Part 3
Let $X_i$ be the indicator r.v denoting whether the ith ball in the n balls selected from the urn is white. We can 
decompose $X$ as $X_1 + X_2 + ... X_n$. As a result, we have that $E[X] = E[X_1] + E[X_2] + .... E[X_n]$.

Since every $X_i$ is an indicator variable, we know that $E[X_i] = Pr(X_i = 1)$. Since we draw all the 
balls simultaneously at once, each ball has the same probability of being a white ball. Since this is a uniform 
probability space and there are $w$ white balls in the total number of $N$ balls in the urn, we know that 
$Pr(W) = \frac{w}{N}$, where $W$ is the event that a white ball was picked. Since we select each ball with a probability of $\frac{w}{N}$ and we 
do this for each of the n balls selected, $E[X]$ simplifies to $n * \frac{w}{N} = \frac{nw}{N}$. 

### Part 4

Since we draw n balls where the probability of drawing a white ball for each ball is constant and each 
ball is independent of the others, a binomial distribution seems suitable for modelling $Y$.

$Y \sim Bin(n, \frac{w}{N})$.

Given that $Y$ is a binomial r.v, we know that $E[Y] = np = n * \frac{w}{N} = \frac{nw}{N}$.

## Question eight

### Part 1
We can partition $R$ into the events that occurred after obtaining a six on the first throw and the events that 
occurred after not obtaining a six on the first throw. As a result, we have that $E[R]$ becomes equivalent to
$E[R] = E[R | {O6}^{\complement}]Pr({O6}^{\complement}) + E[R | O6]Pr(O6)$, where $O6$ is the event that a six was obtained 
on the first throw.

Expanding out the expression $E[R | {O6}^{\complement}]$, it is equivalent to 
$\displaystyle\sum_{i = 1}^{\infty} i Pr(R = i | {O6}^{\complement})$.

For counting the number of rolls needed, I know that I will need at least one due 
to the first roll not being a six. After that roll, I must calculate how many rolls I need until 
I obtain two sixes, which is equivalent to $E[R]$. Summing up these values, I know that
$E[R | {O6}^{\complement}] = (1 + E[R])$.

### Part 2

Expanding out $E[R | O6]$, it is equivalent to
$\displaystyle\sum_{i = 1}^{\infty} i Pr(R = i | O6)$.

We can separate the summation into two cases:

**Case 1**: The first two rolls are both sixes
In this case, the probability of this occurring is 2p, owing from the fact that we roll a six with probability $p$ 
and this occurs on the second term in the summation.

**Case 2**: The first two rolls are not both sixes
In this case, the first two rolls are misses and I need to calculate how many rolls I need after 
failing the first two rolls. This is equivalent to (2 + E[R]) many rolls. This case could only occur after 
missing the second roll, which happens with probability $Pr({O6}^{\complement})$. Therefore, we have
$(2 + E[R])* Pr({O6}^{\complement})$ for this case, where $x = (2 + E[R]), Pr(R = x) = Pr({O6}^{\complement})$.

Since these cases are separate, I can sum them to obtain $2p + (2 + E[R])* Pr({O6}^{\complement})$. Since 
this value was obtained from splitting two different portions in $E[R | O6]$, we can say that 
$E[R | O6] = 2p + (2 + E[R])* Pr({O6}^{\complement})$.

### Part 3

Using value of $E[R] = (E[R] + 1)(1 - p) + p(2p + (E[R] + 2)(1 - p))$, it can be simplified to 
$E[R] = E[R] - pE[R] + 1 - p + p(2p + E[R] - E[R]p + 2 - 2p)$, which can be further reduced to
$E[R] = E[R] - pE[R] + 1 - p + p(E[R] - E[R]p + 2)$.

We can rearrange the terms to obtain $0 = -pE[R] + 1 - p + pE[R] - p^2E[R] + 2p$, which becomes 
$p^2E[R] = 1 + p$. Dividing by $p^2$, we obtain $E[R] = \frac{1 + p}{p^2}$.
