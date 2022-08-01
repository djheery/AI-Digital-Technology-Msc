# Search Contours

The book says that a useful way to visualize a search is to draw contours in the state space. 

Like the contours on a topographic map.

**Topographic Map**: The distinctive characteristic of a topographic map is the use of elevation contour lines to show the shape of the Earth's surface.(The Maps that show the elevation of hills via contour lines)

You can see a visual depiction on page 108 

In the diagram on this page there is a contour labled 400
This means all inside this contour have a heuristic of <= 400.

this means: 

f(n) = g(n) + h(n) <= 400

Then because A* expands the frontier of the lowest f-cost, we can see that an A* search fans out from the start node, adding node concentric bands and increasing th f-cost

In uniform cost search we have contours only for g-cost not of g+h cost (g-cost is the cost from initial state to node n)

It should be clear that g-costs are *monotonic*.

Monotonic means that the path cost always increases as you go along the path as action costs are always positive. 

We say that A* with a consistent heuristic (**go back and look at this**) is **optimally efficient** 

A* is efficient because it prunes away search tree nodes that are not necessary for finding the optimal solution. 

For example the path from luton to leeds. 

There is a path from luton to birmingham of 490, there is a path from luton to london of 600. These paths would be pruned as a path will already be found from luton to nottingham with an action cost of 300 

A* does have downsdes 

Tyhe fact that the number of nodes expanded can be exponential in the length of the solution.

