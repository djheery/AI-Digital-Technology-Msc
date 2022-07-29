# Search Algorithms 

A Search Algorithm will take an assigned search problem and find a solution to that problem.
If no solution is found, a failure should be indicated. 

## Search Tree 

A search tree superimposes a tree like structure of the state space graph (The nodes to be considered and how they are lonked)

- Each node corresponds to a state 
- The search tree edges coresspond to an action.
- The search tree may have multiple paths and thus multiple nodes for any given state
- The root of the tree coressponds to the intial state.  

It is important to understand the different between the state space and the search tree 

## Difference between State and State Space

- The state space describes a possibly infinite number of possible states in the world
- It also describes the actions that allow transitions from one state to anothe r

- The search tree describes the pathes bbetween these states 
  - These paths should "reach toward the goal"
- The search tree may have multiple paths too and thus multiple nodes for any given state. 
- Each node has a unique path back to the root. 

## Search Process 

The act of expanding the root node and checking for available actions is done using a Result function. 
The result function is used to see where those results lead too.

For each of the results a new node will be **generated**. 
These new nodes are known as **child nodes** or **sucessor nodes** 
Each of these child nodes will have a parent node which will be the node that they have come from.

A group of unexpanded nodes is known as the **frontier** of the search tree. 
Any state that has been generated for the frontier is said to have been **reached**

## Best First Serach 

Below is some sudo code describing how to perform a best-first-seach: 

```````````````````````````````````````````````````````````````````````````````
function BEST_FIRST_SEARCH(problem, f) returns a solution node or failuer;

  node <-- NODE(STATE=problem.initial)
  frontier <--- A priority queue ordered by f, with node as an element 
  reached <---- A looku table, with one entry with key problem.INITIAL and value node 

    while not IS_EMPTY(frontier) do 
      node <--- POP(frontier)
      if problem.IS_GOAL(node.STATE) then return node;

      for each child in EXPAND(problem, node) do 
        s <--- child.STATE 
        if s is not in *reached* or child.PATH_COST < *reached[s]*.PATH_COST then
          reached[s] <--- child 
          add child to frontier;

  return failure 

function EXPAND(problem, node) yields nodes 
  s <-- node.STATE
  for each action in problem.ACTIONS(s) do 
    s 1<--problem.RESULT(s, action)
    cost <-- node.PATH_COST + problem.ACTION_COST(s, action, s1)
    yield NODE(STATE=s1, PARENT=node, ACTION=action, PATH_COST=cost)

```````````````````````````````````````````````````````````````````````````````

Summary of Best_First_Search 

- Choose a node (n) with minimum value of some evaluation function f(n)
- On each interation chose a node on the frontier with the minimum f(n)
- return if its stae is a goal state 
- otherwise expand to generate child nodes. 
- Each child node is added to the frontier if it has not been reached before 
- It is re0added if it is now being reached with apath that has lower path cost than any previous path
- The alogorithm returns either an indication of failure or the node that represents the path goal. 

## Search Data Structures 

Search Algorithms requre a data structure to keep track of the search tree. 

### Node in the Tree

A node in the tree is represented by a data structure with four components: 

- node.STATE: The state that the node coressponds too 
- node.PARENT: the node in the tree that generated this node 
- node.ACTION: the action that was applied to the parent state to generate this node.
- node.PATH_COST: the total cost of the path from the initial state to this node 
    - Mathmatical formulas use g(node) as a synonym for PATH_COST. 

### Frontier 

The ideal data structure for the frontier is a **queue**

**Write some notes on queues** 

This is because the operations that the frontier requires are: 

- IS_EMPTY(frontier) returns true if there are no nodes in the frontier
- POP(frontier) removes the top node from the frontier and returns to it 
- TOP(frontier) returns (but does not remove) the top node of the frontier 
- ADD(node, frontier) inserts node into its proper place in the queue 

There are 3 kinds of queues used in search algorithims

- Priority Queue: 
  - First pops the node with the minimum cost according to some evaluation function, f
    - This is used in BEST_FIRST_SEARCH 
- FIFO queue: 
  - First in first out queue, first pops the node  that was added to the queue first
    - Breadth first search 
- LIFO queue 
  - Last in first out queue (aka a stack). Pops the first most recent node
    - This is used in depth first search 


## Handling Redundant paths 

Search trees can have redundant paths, such as in the path search from Luton to Leeds there may be a path from Luton to nottingham, then as we expand into this node, the tree may have a path from nottingham to luton. 

This path would known as redundant.
Also a **loopy path** or **cycle** in this particular instance as we could cycle these paths infinitely 

In a 10 X 10 grid the agent may be able to reach for any of the 8 paths available (providing there are no obstacles).

This means that the agent could reach any of 100 the squares in 9 moves or fewer. 
But the number of the paths of length 9 is almost 8^9 (a bit less because of the edges of the grid).

That amounts to more than 100 million. 

This means that the average cell could be reached more than a million different ways. 

This is why we should eliminate redundant paths as the search algorithm would perform roughly a million times faster. 

Saying: 

**algorithms that cannot remember the past are doomed to repeat it**

There are 3 approaches to this issue: 

- Remember all previously visited states 
  - This allows detection of redundant paths, as we will not vist previous paths 
  - This is appropriate when there are many redundant paths 
    - Appropriate providing all the states will fit in memory
  
- Second: Do not worry about repeating the past 
  - In search problems where it is impossible for two paths to reach the same state this may be appropriate 
  - An example would be an assembly problem where each action adds a part to an evolving assemblage, and there is an ordering of parts 
    - This could be so A could be added then B, but not B then back to A .

- Third: check for cycles (infinite loops such as luton to nottingham then nottingham back to luton) 
  - In this case we don't chack for redundant paths 
  - You do this byt following up the chain of paents to see if the state at the end of the path has appeared earlier 
  
## Graph search vs tree search 

A search algorithm is a

- Graph search 
  - If it checks for redundant path
- Tree search if it does not 






