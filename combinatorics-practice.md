## Question 1
$B$ = {pancakes; bacon and eggs; bagel; Doritos}

$L$ = {burger and fries; garden salad; Doritos}

$D$ = {macaroni; pizza; frozen burrito; pasta; Doritos}

How many different daily diets are possible?

Since each choice for the breakfast, lunch, and dinner meal can be made independently of each other, there are 
$|B| * |L| * |D|$ possible choices for a diet.

There are 4 * 3 * 5 = 60 possible diets.

## Question 2

### How many ways could we construct an angry lineup of 3 students? 
To construct an angry lineup of three students, we need to find all the possible sequences of 
three students. Since it is a lineup, it implies that the ordering of the students matter. 

There are p(75, 3) = $\frac{75!}{72!}$ many sequences since you can only choose three students, having initially 75, then 74, the 73 possible options. 

### How many ways could we construct an angry mob of 3 students (the order does not matter)?
You could construct an angry mob of three students in $\binom{75}{3}$ many ways. 

## Question three

### How many ways can we choose a poker hand?
We can choose a hand in $\binom{52}{5}$ many ways.

### A 4-of-a-kind consists of a poker hand such that 4 of the cards have the same number but different suits. How many ways can we choose a 4-of-a-kind?
There are $2\binom{13}{2}\binom{4}{1}$
$\binom{13}{2}$ represents all the combinations of two values someone could have for a four of a kind.

$\binom{4}{1}$ represents the possible suits one could pick from for the fifth card

The 2 represents the act of swapping the values used in the four of a kind and the fifth card.

### A Full House is consists of a poker hand with three cards of one number and two cards of another number. How many ways can we choose a full house?
There are $\binom{13}{2}$ ways of picking two values to use in the hand.

There are $\binom{4}{3}$ ways of picking three cards from the four possible suits.

There are $\binom{4}{2}$ ways of choosing two cards out of four possible suits.

In total, there are $2\binom{13}{2}\binom{4}{3}\binom{4}{2}$ ways of drawing a full house, where the two represents the change of the values used for the three of a kind and the pair.

## Question four
Let us divide the square into four quadrants of equal size. Four points can be selected at the corners, and 
the farthest point from all four points is the center. Calculating the distance from the center, it is
$\frac{1}{\sqrt{2}}$. Since this distance is calculated with the farthest points not being in the interior of the square, 
the distance between the fifth point and any of the four previous points is less than $\frac{1}{\sqrt{2}}$.

## Question five
### What is the maximum possible number of edges if i) self-loops (edges of the form v1 → v1) are not permitted, ii) if self-loops are permitted?

#### self-loops not permitted
I have $\binom{n}{2}$ many possible edges since they count all the possible edges by considering every pair of two points.

#### self-loops permitted
I have $\binom{n}{2}$ many possible edges from the combinations of the unique vertices and $n$ edges since 
each vertex has an edge with itself. In total, I have $\binom{n}{2}$ + $n$ edges.

## Question six
Picking $n$ items out of a collection of $3n$ items is equivalent to partitioning the set into 
two collections of $n$ items and $2n$ items and picking n - r items from the set of $2n$ items and
r items from the set of $n$ items. For every selection of n - r and r elements from the set of $2n$ items and $n$ items, it maps
to a selection of n items from the set of $3n$ items. Similarily, every selection of $n$ items from
the collection of $3n$ elements can be mapped to a selection  of n - r and r elements from the set of $2n$ items and $n$ items.
Since we have a bijection between both ways of selecting the items, the number of ways of 
selecting $n$ items out of a collection of $3n$ items is equivalent to picking n - r items from the set of $2n$ items and r items from the set of $n$ items.

## Question seven
### How many positive integers not exceeding 1000 are divisible by 7 or 11?

Let $I_7$ be the set of positive integers smaller than 1000 divisible by 7.
Let $I_{11}$ be the set of positive integers smaller than 1000 divisible by 11.

$|I_7 \cup I_{11}| = |I_7| + |I_{11}| - |I_7 \cap I_{11}|$

$|I_7| = 142$
$|I_{11}| = 90$
$|I_7 \cap I_{11}|$ = 12

$|I_7 \cup I_{11}|$ = 142 + 90 -12 = 220

## Question eight
Using the binomial theorem, the sum can be expressed as $(1 - x)^{2n}$