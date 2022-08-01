# Local Beam Search 

The local beam search algorithm keeps track of *k* states rather than jist one

At each step, alll successors of all k states are generated. If any one is a goal, the algorithm halts. Otherwise it selects the k best successors from the complete list and repeats. 

Local Beam search can suffer from alack of diversity among the k states. 

They can become clustered in the sam region of the state space.

There is a variant called stochaistic beam search in which the search chooses successors with probability proportional to the successor's value. 

