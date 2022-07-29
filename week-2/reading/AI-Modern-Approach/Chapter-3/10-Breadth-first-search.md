# Breadth First Search 

When all actions have the same cost, an appropriate stratergy is Breadth First Search.

In this approach the root node is expanded first, then each of the successor nodes are expanded systematically, then their successors and so on. 

For example the initial state is A this has 2 frontier successor nodes of B and C. The algorithm will first expand A, then B then C. If state B has 2 successors D and E and C has F and G then it will expand D first then E and so on. 

This means that on infinite state spaces it is regarded as complete 

A first in first out queue will be faster than a priorty queue and give as the correct order of nodes. 

Reached can also be sa set of states rather than a mapping from states to nodes, because once we have reached that state we can never find a better path. 

This means that you can do an *early goal test* checking whether a node is a solution as soon as it's generated. 

Breadth-ﬁrst search always ﬁnds a solution with a minimal number of actions, because when it is generating nodes at depth d , it has already generated all the nodes at depth d − 1, so if one of them were a solution, it would have been found. That means it is cost-optimal

**check page 95 for psuedo code of the alogorithm**
