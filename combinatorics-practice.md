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
Let us divide a unit square into sixteen points. For the first four points, the corners could be picked.
Considering the distance from each point to the other, the smallest possible distance is 1.

With the fifth point, either an adjacent point or one diagonal to the corner points will be picked.
The largest possible distance from a corner point to one of the neighbouring points is $\frac{\sqrt{2}}{3}$, which is less than 
$\frac{1}{\sqrt{2}}$. Therefore, no matter what set of five points we pick, there will always exist two 
which are less than $\frac{1}{\sqrt{2}}$ units apart.