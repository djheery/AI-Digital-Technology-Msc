# The Semantics of Bayesian Networks 

The syntax of a Bayesian Network consists of a directed **Acyclic Graph** with some local probability information attached to each node. 

The semantics defines how te syntax corresponds to a joint distribution over the variables of the network. 

Example: 

- Bayes net contains *n* variables from *X[1],....,X[n]* 
  - A generic entry in the joint distribution is then: 
    - P(X[1] = x[1] ^ ... ^ X[n] = x[n])
    - Each entry in a Bayes net is defined as follows:  
      - **Top Page 433**
      - Page  433 For full calculation example

Bayesian Networks can be used in much the same manner as a **full joint distribution**. They can be used to answer any query about the domain. 

This is done by summing all relvant joint probability values. 
Each of the joint probability values is calculated by multiplying probabilities from the local conditional distributions. 

**Page 434**

## Definitions 

- **Acyclic**
  - Not displaying or forming a cycle.
  - Not occurring in periods or cycles 
  - **Acyclic Graph**
    - There are no cycles within this type of graph 
    - Where nodes in a graph are in one direction 