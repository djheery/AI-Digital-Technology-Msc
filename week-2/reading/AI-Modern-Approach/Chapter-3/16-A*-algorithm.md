# A* Search Alogorithm 

A* Search is the most common informed search algorithm. 

It uses this evaluation function: 

f(n) = g(n) + h(n)

g(n) = path cost from initial state to node n 
h(n) = estimated cost of the shortest path from n to a goal state

This means that

f(n) = The estimated cost fo the best path that continues from n to goal

**page 105 for visual deptiction**

A* is complete.
Whether A* is cost-optimal or not depends on certain properties of the heuristic.

A Key property is **Admissibility**

**Admissible heuristic**: One that never overestimates the cost to reach the goal (therefore it is optimistic)

Suppose the optimal path has cost C*.
The algorithm then returns a path with cost C > C*.

This means there must be some node n which is on the optimal path and is unexpanded.

So uing notation g*(n) to mean the cost of the optimal path from the start to n.
And h*(n) to mean the cost of the optimal path from n to the nearest goal we have: 

f(n) > C* (otherwise n would have been expanded)
f(n) = g(n) + h(n) (by definitaion)
f(n) = g*(n) + h(n) (because n is an optinal path)
f(n) <= g*(n) + h*(n) (because of admissibility, h(n) <= h*(n))
f(n) <= C* (by definition, C* = g*(n) + h*(n))

"The ﬁrst and last lines form a contradiction, so the supposition that the algorithm could return a suboptimal path must be wrong— it must be that A ∗ returns only cost-optimal paths."


## Consistency

A slightly stronger property is called **consistency. 
A heuristic h(n) is consistent if for every node n and every successor n^1 of n generated by an action a, we have 

h(n) <= c(n, a, n^1) + h(n^1)

This is a form of **Triangle Inequality**
Triangle Inequality stipulates that a side of a triangle cannot be longer than the sum of the other two sides.

Every consistnd hueristic is admissable
Every admissable heuristic is not consistent

This means that with a consistent heuristic A* is const optimal. 

In addtion, with a consistent heuristc, the first time we reach a state it will be on an optimal path, so we never have to re-add a state to the frontier, and never have to change an entry in reached. 

However, with an inconsistent heuristic we may end up with multiple paths reaching the same state. 
If each new path has a lower path cost than the previous one then we will end up with multiple nodes for that stae in the frontier, costing us both time and space. 

Because of that, some implementations of A* take care to only enter a state into the frontier once, and if a better path to the state is found, all the succssors of the state are updated.

This requires nodes to have child pointers as well as parent pointers. 

"With an inadmissible heuristic, A ∗ may or may not be cost-optimal. Here are two cases where it is:

- First, if there is even one cost-optimal path on which h ( n ) is admissible for all nodes n on the path, then that path will be found, no matter what the heuristic says for states off the path.
- Second, if the optimal solution has cost C ∗ , and the second-best has cost C 2 , and if h ( n ) overestimates some costs, but never by more than C − C ∗ , then A ∗ 2 is guaranteed to return cost-optimal solutions."


