# Depth First Search 

Depth first search will always expand to the deepest node in the frontier first.

It could be implemented as a call to Best-First-Search where the evaluation function f is the negative of the depth. 

However it is usually implemented as a tree-like seach.

Remember tree-like search means that it does not keep track of the states. 

An example initial state A will expand into B and C then it will choose to keep expanding B and then D and E the say D has 2 nodes H J it will see H is the end, then check J, it will see that J is the end then go back up to E then expand what ever nodes are successors to E and only when it has exhausted these paths will it then go back and repeat the process on C.

Depth first search is not optimal as it will return the first solution even if it is not the cheapest cost. 

For finite state space that are trees it is efficient and complete 

For acyclic state space it may end up expanding the same state space many times via different paths. 

It can get stuck in cyclic state spaces therefore some implementations check each new node for cycles. 

It does not work in infinite state space. 

## Why would you consider it? 

For finite spaces where a tree-like search is feasable it has much smaller memory requirements. 

" a depth-ﬁrst tree-like search takes time proportional to the number of states, and has memory complexity of only O ( bm ) , where b is the branching factor and m is the maximum depth of the tree.
"

## Depth Limited and Interative Deepening Search 

To stop depth first search going down an infinite path we can use a **depth-limited serach**

In a depth limited seearch a depth limit is a applied and the algorithm will know once it has reached a certain depth that it will treat this node as if it had no sucessors. 

IF we make a poor choice for the limit of the algorithm it will fail to reach the solution making it incomplete. 

## Diameter 

The diameter acts as the most efficient depth limit. For example in a map probblem with 20 places to visit and one goal state we could set the depth limit to 19; However this would be inefficient, upon reviewing the number of cities we find that you can visit any city in 9 actions. 

Thefore the diameter is 9 and the depth limit should be equal to the diameter (9)

### Iterative Deepening Search 

"Iterative deepening search solves the problem of picking a good value for by trying all values: ﬁrst 0, then 1, then 2, and so on— until either a solution is found, or the depthlimited search returns the failure value rather than the cutoff value. The algorithm is shown in Figure 3.12. Iterative deepening combines many of the beneﬁts of depth-ﬁrst and breadth-ﬁrst search. Like depth-ﬁrst search, its memory requirements are modest: O ( bd ) when there is a solution, or O ( bm ) on ﬁnite state spaces with no solution. Like breadth-ﬁrst search, iterative deepening is optimal for problems where all actions have the same cost, and is complete on ﬁnite acyclic state spaces, or on any ﬁnite state space when we check nodes for cycles all the way up the path. "

Iterative deepening search may seem wasteful because states near the top of the search tree are re-generated multiple times. But for many state spaces, most of the nodes are in the bottom level, so it does not matter much that the upper levels are repeated. In an iterative deepening search, the nodes on the bottom level (depth d ) are generated once, those on the next-to-bottom level are generated twice, and so on, up to the children of the root, which are generated d times. So the total number of nodes generated in the worst case is N ( IDS ) = ( d ) b N ( IDS ) N ( BFS ) = = 1 + ( d − 1 ) b 2 + ( d − 2 ) b 3 · · · + b d , which gives a time complexity of O ( b d ) —asymptotically the same as breadth-ﬁrst search. For example, if b = 10 and d = 5, the numbers are 50 + 400 + 3 , 000 + 20 , 000 + 100 , 000 = 123 , 450 10 + 100 + 1 , 000 + 10 , 000 + 100 , 000 = 111 , 110 .

