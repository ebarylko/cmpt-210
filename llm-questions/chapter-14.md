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
