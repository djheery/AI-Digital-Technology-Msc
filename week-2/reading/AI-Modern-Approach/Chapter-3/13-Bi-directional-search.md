# Bidirectional Search 

Bidirectional Search simultaneously searchs forward from the initial state and backwards from the goal state. hoping that the two staes will meet. 

You can see the sudocode for the algorithm on **page 101**

For this to work we need to keep track of the two frontiers and two tables of reached staets. 
We also need to be able to reason backwards. 

There are many different versions of Bidirectional search in this part we only cover best-first bidrectional search. 

Although there are two separate frontiers, the node to be expanded next is always one with a minimum value of the evaluation function, across either frontier. When the evaluation function is the path cost, we get bidirectional uniform-cost search, and if the cost of the optimal path is C ∗ ∗ , then no node with cost > C 2 will be expanded. This can result in a considerable speedup.

