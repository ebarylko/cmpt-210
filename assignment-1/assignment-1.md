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

The number of possible sequences are r^n, meaning there are r^n number of
total functions.

### If r > n, what is the number of injective functions f : A → B?
For a function to be injective, each element in $A$

### If r ≤ n, what is the number of injective functions f : A → B?

### If r = n, what is the number of bijective functions f : A → B?

### If r < n, what is the number of bijective functions f : A → B?