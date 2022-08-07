# Proof By Resolution 

Proof by resolution is using prior knowledge in the KB to infer a **resolvent** that resolves new rules. 
Take this example: 

R11: ¬B[1, 1]
R12: B[1, 2] <=> (P[1, 1] V P[2, 2] V P[1, 3])

Above are two propositions, due to R10 earlier we can now utilize the KB to solve R12.

R13: ¬P[2, 2]
R14: ¬P[1, 3]

Remember there is no Pit at [1, 1] and the KB knows this as it is our starting position

We can then apply biconditional (if and only if) elimination to R3, followed by Modes Ponens (if the implied sentence is true) with R5  to obtain the fact that there is a pit in [1, 1]. [2, 2] or [3, 1]

R15: P[1, 1] V P[2, 2] V P[3, 1]

this is the fires application of Resolution rule, R13 resolves with the literal in R15 P[2, 2] to give the resolvent: 

R16: P[1, 1] V P[3, 1]

Similarly the literal R1 ¬P[1, 1] will resolve with the Literal in R16: 

R17: P[3, 1]

THis defines that there is a Pit in 3, 1

In plain English: 

If there is a pit in 1, 1 or 3, 1 and it is not in 1, 1 then it must be in 3, 1


**Go back and look at complementary literals**
