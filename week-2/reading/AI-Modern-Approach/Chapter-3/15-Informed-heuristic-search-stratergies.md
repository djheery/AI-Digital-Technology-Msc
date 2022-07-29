# Informed Heuristic Search Stratergies 

This section shows how an informed search strategy can find solutions more efficiently than an uninformed strategy.
Informed means that there will be hints in the form of domain specific knowledge about where the goal may be located. 

Hints come in the form of a heuristic function. 

This is notated as h(n)

h(n) = Estimated cost of the cheapest path from the state at node n to goal state. 

For example, in route-ﬁnding problems, we can estimate the distance from the current state to a goal by computing the straight-line distance on the map between the two points.

## Greedy Best-First Search 

"Greedy best-ﬁrst search is a form of best-ﬁrst search that expands ﬁrst the node with the lowest h ( n ) value— the node that appears to be closest to the goal— on the grounds that this is likely to lead to a solution quickly. So the evaluation function f ( n ) = h ( n )

Let us see how this works for route-ﬁnding problems in Romania; we use the straightline distance heuristic, which we will call h SLD . If the goal is Bucharest, we need to know the straight-line distances to Bucharest, which are shown in Figure 3.16. For example, h SLD ( Arad ) = 366. Notice that the values of h SLD cannot be computed from the problem description itself (that is, the A CTIONS and R ESULT functions). Moreover, it takes a certain amount of world knowledge to know that h SLD is correlated with actual road distances and is, therefore, a useful heuristic."

On each iteration it tries to get as close to a goal as it can, this is why it is known as "greedy" but greediness can lead to worse results than being careful.

Greedy best-ﬁrst graph search is complete in ﬁnite state spaces, but not in inﬁnite ones. The worst-case time and space complexity is O ( | V | ) . With a good heuristic function, however, the complexity can be reduced substantially, on certain problems reaching O ( bm )