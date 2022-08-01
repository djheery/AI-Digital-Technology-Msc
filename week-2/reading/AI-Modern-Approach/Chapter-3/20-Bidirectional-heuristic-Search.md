# Bidirectional Heuristic Search

With bidirectional best-first-search there is no garuntee the f(n) = g(n) + h(n) will lead to an optimal solution. Even with an admissible heuristic. 

This is because in bidirectional search, it is not singluar nodes but pairs of nodes that must be weighted together to prove the efficiency of the path. 

Ff(n) = Gf() + Hf(n) 

This is the function for the forward direction frontier 

Fb(n) = Gb(n) + Hb(n) 

This is the calculation for the backward direcytion frontier 

Althought both forward and backward direction are solving the same problems, they need different evaluation functions. 

This is because the heuristics will be different if you a striving from the goal from the initial state or the goal state. 


This function defines the lower bound cost: 

lb(m,n) = max(Gf(m) + Gb(n), Ff(m), Fb(n))

lb = lower bound cost of solution.
m = forward path from initial state 
n = backward path from goal to n 


In other words, the cost of such a path must be atleast as large as he sum of the path costs of the two parts. 

The cost must also be at least as much as the estimated fcost 

given that the theorem is that for any pair of nodes m,n with a lower bound lb(m, n)  cost of less than the C*, we must expand wither  or n, because the path that goes through both of them is a potential optimal solution. 

There is no garuntee that this is optimally efficient as we don't know for sure which is the best node to expand. 

**Go Back and read a bit more of this section.


