# Search Problesm and Solutions 

Below is a formal definition of a **Search Problem** 

- A set of possible states that the environment could be in 
  - Known as **state space**
- The initial state of the agent. 
  - For example, the starting city of the agent
- A set of one or more **goal states** for the agent to acheive
  - In this case the city to get to, but there could be many more goal states which would be considered a solution to the search problem. 
- Any **actions** that are available to the agent
- A **Transaction Model** 
  - This is the result that occurs because of each action 
  - RESULT(Luton, toNottingham) = Nottighamn
    - RESULT is the function 
      - Luton, Nottingham are the subjects (propositions) 
      - the Deduction is Nottingham which is the result of the Propositions. 
  - The transation Model is all of the results of each action
- An **Action Cost Function** 
  - This is a mathematical equation associated with each action, of from which the result is the cost. Hence the Action Cost function 
  - This can also be Denoted as: 
    - ACTION-COST(s, a, s**1) 
      - a: the applied action 
      - s: the state 
      - s**1: the state to be reached as a result of the action taken
  - A problem-solving agent has to use a cost function that reflects on it's own performance to choose the most optimal solution
    - This a cost could be the amount of miles between one path and another. 

## Path 

A path is considered a sequence of actions from one state to antoher state 

## Solution 

A solution is considered the path from the intial state a to the goal state g. 

Costs are considered addititve. 
The total cost of a path is the sum of each individual action cost. 

## Optimal Soltuin 

The optimal solution is considered the path from initial state to goal states which results in the lowest cost when compared to other paths (if there are any) which achieve the same goal. 

For example an optimal solution would be going from Luton to Newcastle via the M1 when compared to going first to birmingham, then up to the M62 only to rejoin the A1 which would have a miuch higher cost. 

