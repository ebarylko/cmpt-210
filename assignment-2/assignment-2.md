## Question 1

### Prove that the probability that exactly one of the events A or B occurs is equal to Pr[A] + Pr[B] − 2 Pr[A ∩ B].

$Pr(A) = Pr(A - B) + Pr(A \cap B)$

$Pr(A - B) =  Pr(A) - Pr(A \cap B)$

$Pr(B) = Pr(B - A) + Pr(A \cap B)$

$Pr(B - A) =  Pr(B) - Pr(A \cap B)$

The probability that exactly one of the events A or B occurs is $Pr((A - B) \cup (B - A))$.

Since (B - A) and (A - B) are disjoint, $Pr((A - B) \cup (B - A)) = Pr(A - B) + Pr(B - A)$

$Pr((A - B) \cup (B - A)) =  Pr(A) - Pr(A \cap B) + Pr(B) - Pr(A \cap B)$ 

= $Pr(A) + Pr(B) - 2Pr(A \cap B)$

