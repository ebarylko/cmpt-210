## Question 2

Set $A$ has r elements and set $B$ has n elements

### What is the number of possible total functions f : A → B?

For a function f to be a total function, each element in $A$ must map to 
and element in $B$. Since each element in $A$ can map to n elements in $B$, and there are
no further constraints on the function being injective or surjective, we have
n possible outputs for each element in $A$. 

We can define a bijection between counting the number of total functions and
counting the number of sequences in the set $(n_1, n_2, n_3, .... n_n)^r$, where 
each element in the ith position represents the value in $B$ that the ith element in 
$A$ maps to.

For any sequence of the form described above, we can map it to a function where
$f(r_1) = n_1, f(r_2) = n_2, ..... f(r_n) = n_n$. Similarly, we can map any
function to a sequence which describes the output of the ith element in $A$.

Since we have a bijection, we know that counting the number of sequences
in the set $(n_1, n_2, n_3, .... n_n)^r$ is equivalent to counting
the number of possible total functions.

The number of possible sequences are $r^n$, meaning there are $r^n$ number of
total functions.

### If r > n, what is the number of injective functions f : A → B?
For a function to be injective, each element in $A$ must map to a unique 
element in b. If $|A| > |B|$, then there exists two elements in $A$ which map
to the same element in $B$ by the pigeonhole principle.

Since two elements in $A$ mapping to the same element in $B$ disqualifies f from 
being a injective function, there exist no injective functions when r > n.

### If r ≤ n, what is the number of injective functions f : A → B?
For a function to be injective, each element in $A$ must map to a unique
element in b. Since $|A| \le |B|$, we can select r elements from $B$ to use 
as the values that each element in $A$ maps to.

We can define a bijection between the number of injective functions and 
the number of ways we can form a string of size r using the values from 1 
to n, where the element in the ith position in the string represents the value
in $B$ that $f(r_i)$ maps to. 

For every string of the form described above, we can map it to a function 
that maps the values of $r_i$ to their corresponding value in $B$. For every 
injective function, we can map it to a string which describes the value 
that $r_i$ maps to.

Since we have a bijection, we know that counting the number of ways we
can form a string of size r using the values from 1 to n is equivalent to 
counting the number of injective functions.

The number of ways we can form a string of size r using the values from 1
to n is $\binom{n}{r} * r!$.

Therefore, the number of injective functions is $\binom{n}{r} * r!$.

### If r = n, what is the number of bijective functions f : A → B?
For a function to be bijective, it must be injective and surjective. This means
that every element in $B$ is mapped to by a unique element in $A$.

We can define a bijection between the number of bijective functions and
the number of ways to permute a string of n elements, where the element in the
ith position is the value that $f(r_i)$ maps to. For any string of the 
form described recently, it can be mapped to a function that maps $r_i$ to 
the values in the sequence. Any function can be mapped to a string which
describes the value that the ith element of $A$ maps to. 

The number of ways to permute a string of n elements is $n!$.

Therefore, the number of bijective functions is $n!$.

### If r < n, what is the number of bijective functions f : A → B?
For a bijective function, $|A| = |B|$. Since this condition is not satisfied,
there exists no possible bijective function considering the condition that r < n.


### We have 5 identical black balls and 1 ball each of 5 colors {red, green, blue, yellow, violet}. In how many different ways can we choose 5 balls?

Since the black balls are identical, I know that the sequences of the form
$(black_1, black_2, red, green, blue)$ is equivalent to 
$(black_4, black_5, red, green, blue)$. Since I would be double counting by
not considering these types of cases, I know that what matters is the number
of black balls. Therefore, I must focus on counting the cardinality of 
the power set of the five non-black colors. With every subset, if there are
less than five balls in the set, I add the black balls to the set. This way, 
I avoid overcounting by only adding black balls to the unique subsets.

The number different ways we can we choose 5 balls is $|\mathcal{P}({red, green, blue, yellow, violet})|$ 

= $2^{|{red, green, blue, yellow, violet}|}$ 

= 32.

There are 32 different ways we can we choose 5 balls. 

## Question four
Let P be the set of all possible plates, L = {A, B, . . . , Z} 
be the set of upper-case letters, and D = {0, 1, . . . , 9} be
the set of digits.

### Express P in terms of L, D using the set union ∪ and product × operations 

Let $L_{3l3d}$ be the set of all licence plates where three letters are followed
by three digits.

$L_{3l3d} = L \times L \times L \times D \times D \times D$

Let $L_{5l}$ be the set of all licence plates where there are five letters.

$L_{5l} = L \times L \times L \times L \times L$

Let $L_{2c}$ be the set of all licence plates with two characters.

Let $C = L \cup D$.

$L_{2c} = C \times C$

$P = L_{3l3d} \cup L_{5l} \cup L_{2c}$ 

$P = (L \times L \times L \times D \times D \times D) \cup (L \times L \times L \times L \times L) \cup (C \times C)$


### Using the sum rule and the product rule, compute |P|

Since $P$ is pairwise disjoint, $|P| = |L_{3l3d}| \cup |L_{5l}| \cup |L_{2c}|$.




