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

