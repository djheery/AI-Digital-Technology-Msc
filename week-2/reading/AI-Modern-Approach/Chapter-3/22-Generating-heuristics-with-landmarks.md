# Generating Heuristics with Landmarks 

How can services such as google maps generate driving directions in miliseconds when the search algorithms considered so far are about a million times slower? 

There are many answers, but the most imporant is the **precomputation** of some optimal path costs. 

Whist precomputation is time consumiong, it need only be done once. Then the time spent will be amortized over billions of usre search requests. 

It would be possible to generate a perfect heuristic by precomputing and sotring hte cost of the optimal path between every pair of vertices. 

that would take O(|V|^2) space, and O(|E|)^3 time.

This may be practical for 10,000 graphs but not 10,million. 


A better approach is to choose a few **landmark points** from theis vertices. 

For each landmark L and for each other Vertex v in the graph, we compute and store C*(v, L) the exact cost from the vertices to the landmark. 

Given the stored C* tables, we can easily create an efficient (although inadmissible heuristic): the minimuym over all landmarks of the cost of getting fronm the current node to the landmark and then to the goal. 

Hl(n) = min L ∈ Landmarks C ∗ ( n , L ) + C ∗ ( L , goal )

If the optimal path happens to geo through a landmark, this heuristic will be exact, if not it will be inadmissible. 

Some route-ﬁnding algorithms save even more time by adding **shortcuts** —artiﬁcial edges in the graph that deﬁne an optimal multi-action path. 

For example, if there were shortcuts predeﬁned between all the 100 biggest cities in the U.S., and we were trying to navigate from the Berkeley campus in California to NYU in New York, we could take the shortcut between Sacramento and Manhattan and cover 90% of the path in one action. 

h L ( n ) is efﬁcient but not admissible.

 But with a bit more care, we can come up with a heuristic that is both efﬁcient and admissible: 

h DH ( n ) = max L ∈ Landmarks | C ∗ ( n , L ) − C ∗ ( goal , L ) |

This is called a **differential heuristic** 

differential - dissimilarity, difference, Of or relating to the state or relation of being different

Difference or the amount of difference between two things that are different such as cost, state, rate etc. 

A differetial heuristic could be considered a landmark that is somewhere out beyond the goal. 

If the goal happens to be on the optimal path from n to the landmark, then this is saying:

**"consider the entire path from n to L, then subtract off the last part of that path, from a goal L, giving us the exact cost of the path from n to goal**

Picking landmarks should be done selectively so they a spaced far enough apart. Landmarks coul dbe picks from logs or requests from previous users. 

