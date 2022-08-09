# Probabilistic Reasoning 

This chapter will introduce: 

- Bayesian Networks 
- Syntax and Semantics of Bayesian Networks 
- How probabilistic inference can be done efficiently 
- Approximate inference agorithms

## Representing Knowledge in an Uncertain Domain 

**Bayesian Networks** can:
  - Be used to represent dependencies amongst variables.
  - Represent any full joint probability distribution 
    - In many cases concisely 

A Bayesian Network is a directed graph.
In this directed graph each node is annotated 
The annotations include quantitative probability information. 

Full Bayesian Network Specification: 

1. Each node corresponds to a random variable 
  - Remember random variables can be Discrete or continuous 
2. Directed links connect pairs of nodes 
  - Can be seen as arrows 
  - If an arrow from node X to node Y exists. X is said to be the parent of node Y. 
3.  Each node X[i] has associated probability information 
  - This information quantifies the effect of the parents on the node using a finite number of parameters. 

The nature of the graph with X being a parent of Y suggests that causes (X) should be the parents of effects (Y).

Page 431 for an example of how Bayesian networks represent relationships between conditionally independent variables and root. 

You can represent the logical probability attached to each node with a **conditional probability table** also known as **CPT** 

Each node has a **Conditioning Case** associated with it. 

Each row must sum up to 1. 
For boolean variables, once you know the probability of a true value (p) then the value of a false must be:

1 - p 

Thus the false value is often ommited. 

In general a table for a Boolean variable with k Boolean parents contains:

2^k independently specifiable probabilities. 

A node with no parents has only one row representing the **prior probabilities** of each possible value of the variable. 



## Definitions

- **Conditional Probability Table** (**CPT**) 
  - A way to represent the local probability information attached to each node in a Bayesian Network. 
    - View the top of page 432 for an example. 
- **Conditioning Case** 
  - This is the conditional probability of each node value for a node in a Bayesian networks CPT. 
  - A possible combination of values for the parent nodes 
    - A miniature world. 
  - Each row must sum up to 1




