# Satisficing Search: Inadmissible Heuristics and Weighted A* 

A* search despite it's good qualites expands a lot of nodes. 

We can explore fewer nodes (taking up less time and space) if we are willing to accept solutions that are subboptimal but are "good enough"

This is what we call stisficing solutions. 

If we allow A* to use and inadmissibble heuristic (one that may overestimate) then we risk missing the optimal solution, but the heurisic can be potentially more accurate, thereby reducing the number of nodes expanded. 

"For example, road engineers know the concept of a detour index , which is a multiplier applied to the straight-line distance to account for the typical curvature of roads. A detour index of 1 . 3 means that if two cities are 10 miles apart in straight-line distance, a good estimate of the best path between them is 13 miles. For most localities, the detour index ranges between 1.2 and 1.6."

We can apply this idea to any problem with an approach called **weighted A\***

## Weighted A*

This is where we weight the heuristic value more heavily, giving us a new evaluation function: 

f(n) = g(n) + W * h(n)

View page 110 for a visual depiction of how this works 

Basically in regular A* many more nodes are expanded to find an optimal solution whereas in weighted A* finds a solution that is slightly less optimal but the search time is much faster. 

Weighted A* focus' on the contour of reached states that go towards the goal. 

If the optimal solution is C* 

Weighted A* will be somewhere bbetween C* and W * C* 

In practice it usually gets much closer to the C* than W * C* 

Weighted A* can be seen as a generalization of the others: 

A* Search:              g(n)+h(n)       (W=1)
Uniform-Cost Search:    g(n)            (W=0)
Greedy Best FS          h(n)            (W=∞)
Weighted A* :           g(n) + W * h(n) (1 < W < ∞)

