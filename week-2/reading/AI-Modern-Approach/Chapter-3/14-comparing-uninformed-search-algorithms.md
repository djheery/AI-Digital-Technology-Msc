# Comparing Uninformed Search Algorithms

| Criterion       | BFS     | Unifrom-Cost      |DFS      | D-Limited-S     | Interative Deepening    | BiDirectional     |
---------------------------------------------------------------------------------------------------------------------------
| Complete        | Yes^1   | Yes^1,2           | No      | No              | Yes^1                   | Yes^1,4           |  
| Optimal Cost?   | Yes^3   | Yes               | No      | No              | Yes^3                   | Yes^3, 4          |         
| Time            | O(b^d)  | O(b^1+[c*/e])     | O(b^m)  | O(b^l)          | O(b^d)                  | O(b^d / 2)        |
| Space           | O(b^d)  | O(b^1+[c*/e])     | O(b*m)  | O(bl)           | O(bd)                   | O(b^d / 2)        |

b = branching factor
m = maximum depth of search tree 
d = is depth of shalowest solution or m where no solution 
l = Depth limit

1 complete if b is ﬁnite, and the state space either has a solution or is ﬁnite. 
2 complete if all action costs are ≥ > 0; 
3 cost-optimal if action costs are all identical; 
4 if both directions are breadth-ﬁrst or uniform-cost.