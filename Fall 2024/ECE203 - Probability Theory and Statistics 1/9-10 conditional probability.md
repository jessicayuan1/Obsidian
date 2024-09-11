Conditional probability is one of the most important concepts in this course
* it is a tool to compute probability
* it lets us update probabilities when partial information is revealed

Ex. Say we toss 2 dice. What is the prob that sum = 9?

F = {(3,6), (6,3), (4,5), (5,4)}
P[E] = |E| / |S| = 4/36 = 1/9

Ex. Say I roll 1st die (but not the second) and get a 4. What is prob that sum will be 9 given this new information
1/6
All possible outcomes 
F = {(4,1), (4,2) (4,3) (4,4) (4,5) (4.6)}
The 30 other cases are inconsistent with this information. They have prob = 0 
The 6 cases in F had some prob before first die was rolled 
They should have same prob after outcome of 1st die roll is revealed to be 4
Each has prob 1/6

We say probability of E given has occurred is 1/6
P[E | F] = 1/6 (Prob of E given F)


Ex. A coin is flipped twice -- what is prob of 2 heads if ii) at least one flip is heads
F = {ht, th, hh}
P[E|F] = P[EF] / P[F]
		= 1/4 / 3/4 = 1/3 
P[EF] = hh intersection F is 1/4 chance 

Ex. Two 4-sided die are rolled. Let 
E={max of both rolls = 3}
F = {min of both rolls = 2}
S = 16
Find P[E|F]

E = { (1,3) , (2,3) , (3,3) (3,2) (3,1)}
F = {(2,3) (3,2) (4,2) (2,2) (2,4)}

P[E|F] = P[EF] / P[F] = P{(2,3) (3,2)}/P[F] =  2/16  / 5/16 = 2/5


Conditional probability satisfies the axioms of prob: For fixed F with P[F] > 0. the function P[. |F] satisfies all the same axioms as P[.].



[A1] P[E|F] = P[EF]/P[F] > 0 since P[F] > 0 and P[EF] >= 0
		P[E|F] = P[EF]/P[F] <= 1 (at most 1) since P[E|F] <= P[EF]/P[F] since EF contained in F
[A2] P[S|F] = P[SF] / P[F] = P[F] / P[F] = 1

[A3] Let E1 Intersection E2 = 0/ (null set)

Multiplication rule 
![[Pasted image 20240910111117.png]]


Ex. 3 grad and 12undergrad students are randomly divided into 3 groups of 5. WHat is prob that each group has exactly 1 grad student?