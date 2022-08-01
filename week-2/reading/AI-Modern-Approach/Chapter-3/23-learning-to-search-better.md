# Learning to Search Better 

Agents can learn how to search better. 

The method rests on a concept known as **meta-level state space**.

Each state in a metal level state pace captures the internal state of the program that is performing the search in an ordinary state space. This ordinary state space could be the map of england. 

For example, in A* the internal state space consists of the current search tree. 

Each action in the metalevel state space is a computation step that alters the internal state. 

Every time a leaf nod is expanded and adds successors to a tree the metalevel state space will change.

A **metalevel learning algorithm** can learn from choices that do not help reach a goal state to avoid expoliring unpromising subtrees. 


