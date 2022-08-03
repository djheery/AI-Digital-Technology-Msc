# Simple Knowledge base 

First we should focus on the immutable aspects of the wumpus world: 

P[x, y] is true if there is a pit in [x, y]
W[x, y] is true if there is a wumpus in [x, y] dead or alive 
B[x, y] is true if there is a Breeze in [x, y]
S[x, y] is true if there is a stench in [x, y]
L[x, y] is true if the agent is in location [x, y]

We can then make inferences based on these immutable aspects 

One inference we can make: 

- ¬P[1, 1]: as there is no pit on the starting position;

we label each sentence with R[i] so that we can refer to them: 

- R[1] : ¬P[1, 1]

A pit is only in a neighbouring square if there is a breeze on the current square:

- R[2] : B[1, 1] <=> (P[1, 2] V P[2, 1]);
- R[3] : B[2, 1] <=> (P[1, 1] V P[2, 2] V [3, 1])
  - However, as the KB should contain the details that there is no pit in P[1, 1] (As this is our starting positiion) the agent should gather that there is not a pit at P[1, 1] and only consider P[2, 2] or P[3, 1] as potentially containing a pit. 


