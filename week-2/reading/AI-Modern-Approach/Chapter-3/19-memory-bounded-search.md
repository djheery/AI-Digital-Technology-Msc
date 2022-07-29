# Memory Bounded Search 

The main issue with A* is it's use if memory. 

Your memory will be split between: 

- Frontier 
- Reached States 

Best first search saves the state in two places

- A node on the frontier 
- An entry in the table of reached states 

You could keep the state in only one of two places, saving memory 

Another possiblity is you could remove staes from reached when we can prove they are no longer needed. 

You could also keep a reference count of the number of times a state has been reached and then remove that state from reached when there are no more ways to reach the stae. 

## Algorithms to Conserve Memory 

Below are some algorithms that are designed to save memory

### Beam Search 

Beam search limtes the size of the frontier. 

The easiest approach is to only keep k nodes with the best f-scoures (eval function scores) discarding other expanded nodes. 
This does make the search incomplete and suboptima.
 
But k can be chosen to make good use of availabble memory
Fast exectution because it executes of fewer nodes. 

For many problems it can find good near-optimal solutions. 

An alternative version of beam search doesn't keep a strict limit on the size of the frontier.
Instead it keeps every node whose f-score is within a certain amount. 

That way when there are a few strong-scoring nodes only a few will be kept, bbut if there are no strong nodes then more will be kept until a strong one emerges. 

### Iterative-deepening A* search (IDA*)

This is the equivelant of the iterative deepening search for A. 
It removes staes in memory beyond a certain pooint at the cost of visiting some states multiple times. 
Then expands if the solution is not found.

It is a very important, commanly used algorithm for problems that do not fit in memory. 

In IDA* the cutoff is the f-cost(g+h)

### Recursive Best First Search 

Mimcs the operation of a standard Best-FS but using only linear space. RBFS resembles a recursive depth-first-search, but rather than continuing indefinitely down the current path, it uses the f_limit variable to keep track of the f-value of the best alternavtive path available from any ancestor of the current node. 

If the current node exceeds this limit, the recursion unwinds back to the alternative path.
As the recursion unwinds, RBFS replaces the f-value of each node along the path with a backed up value.

"In this way, RBFS remembers the f -value of the best leaf in the forgotten subtree and can therefore decide whether it’s worth reexpanding the subtree at some later time."



