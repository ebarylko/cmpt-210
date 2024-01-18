 ## Chapter 14
 
### Question 1
Since we always divide the number of possible numbers in half every time we ask 
a question, the minimum number of questions Q needed to be sure of the correct 
value is the amount where $\frac{1000}{2^Q} \leq 1$, meaning we have found the number Alice has guessed.
Since $log_2(1000) = 9.96$, this means we have to ask ten questions for our options to be restricted to one 
possible value.

### Question 2
The number of ways to answer the next chapter's problems is the product of all the possible 
ways to answer each of the three problems.

The number of ways to answer the first question is 16 since there are two possible answers for each of the four subquestions, with 
$2^4 = 16$ possible ways of answering them.

The number of ways to answer the second question is four since one out of four possible values must be chosen.

The number of ways to answer the third question is six since we can choose the integers between 15 and 20 inclusive as our answer.

Since each question can be answered independently of the other, the number of ways to 
answer the next chapter's problems is 16 * 4 * 6 = 384 possible ways.

### Question 3
To have a total function, we need every element in $A$ to map to an element in $B$. Since we are not given 
any constraints that the function has to be injective, this means that we can have multiple elements in $A$ mapping to the same element in $B$.
As a result, for every element in $A$, there are seven possible elements in $B$ which it can correspond to. Therefore, the number of total functions 
$f: A \rightarrow B$ are $7^3 = 343$.

### Question 4

#### part a
Since $x_1$ is in the set, what needs to be counted is the number of subsets containing the rest of the elements.
Since each subsequent element is in the subset or not, there are $2^5 = 32$ subsets containing $x_1$.

#### part b
Knowing we the subsets must contain $x_2$, $x_3$, and exclude $x_6$, we have to count the number of subsets
containing $x_4$, $x_5$, and $x_1$. There are 2^3 = 8 possible subsets fulfilling these constraints.

### Question 5

#### part a
Let $A$ be the set of all uppercase letters.

Let $D$ be the set of all digits.

Let $L$ be the set of all license plates.

Let $TLTD$ denote the set representing all the license plates with three letters followed by three digits in terms of $A$ and $D$.

Let $FL$ denote the set representing all the license plates with five letters in terms of $A$ and $D$.

Let $TC$ denote the set representing all the license plates with two characters (a number or a letter) in terms of $A$ and $D$.

$TLTD$ = $A^3 X D^3$

$FL$ = $A^5$

$TC$ = $(A \cup D)^2)$

Since there are three sets of license plates (three letters and three digits, five letters, two characters) and each set is disjoint with the other two sets, $L$ can be represented as the union of all these sets.

$L$ = $TLTD \cup FL \cup TC$

#### part b
Since $L$ is the union of disjoint sets, $|L|$ is the sum of each set within.

$|TLTD|$ = $|A|^3 * |D|^3$ = $26^3 * 10^3$ = 17576000

$|FL|$ = $|A|^5$ = $|26|^5$ = 11881376

$|TC|$ = $|36|^2$ = 1296
 
$|L|$ = $|TLTD| \cup |FL| \cup |TC|$ = 29458672


### Question 6

#### part a

How many of the integers from 1 to 1,000,000,000 contain the digit 1?

To construct a number which does not contain a 1, there are $9^9$ possible ways 
of making such a number.

999,999,999
To make a number which may or may not contain a zero, there are $10^9$ many ways 
of doing so. 

The total number of integers which contain a one is the difference between the number 
of all possible numbers and the number of integers which do not contain a one.
The total number is $10^9 - 9^9 + 1$, where the one is added to account for 
0 being removed in the difference.

Should it not be + 2 since I am adding a one for the 

#### part b
There are 20 books arranged in a row on a shelf. Describe a bijection between
ways of choosing 6 of these books so that no two adjacent books are selected and
15-bit strings with exactly 6 ones.

101010101010 00000000
the ones represent books. The zeroes represent 
0101010101010
111111
1 1 1 1 1