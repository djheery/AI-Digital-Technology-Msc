# Computational Intelligence Problem Examples 

This section introduces some Computational Intelligence (CI) problems.

The Problems Introduced are below: 

- The Travelling Salesman Problem 
- The N-Queens Problem 
- The Hill Climbing Search 
- The Simulated Annealing Search 

The above problems are appropriate for Computational Intelligence as normal analytics approaches cannot provide an optimal solution, while CI can find an optimal Solution. 

## The Travelling Salesman Problem 

In this problem: 

- There are a list of cities 
  - There are distances between each pair of cities 
- A salesman starts from a chosen city 
- You are then asked to identify the shortest possible route
  - The route must visit each city only once and then return to the original cities 

## The N-Queens Problem 

In this problem: 

- You must move a queen on a chessboard so that it reduces the number of conflicts 

I should learn a little more about this problem 
  - The lecture does not say much. 

## Hill-Climbing Search 

The hill-climbing search is a gradient based search. 
It is often described as like climbing Everest in thick fog with amnesia. 

The Algorithm steps are as follows: 

1. Expand the Current State 
  - Generate All neighbours 
2. Move to the one with the highest evaluation.
3. Decide the direction with the biggest gradient 
4. Decide what is the pace you should take until the evaluation goes down.

The lecture states that the issue with this algorithm is that you may get stuck in "local maxima" 

This is because the algorithm stops as soon as it reaches the top of the hill, despite the fact that it should be aiming for the top of the mountain. 

Varients on the Hill-Climbing Process include: 

- Repeating the Process multiple times with different starting points and using the one with the best result 
- Using multiple agents to do the search at the same time 
  - With different start points and then choosing the agent landing at the highest peak 
- Doing a simulated annealing search. 

Annealing is the process used to harden metals and glass by heating them to a high temperature and then gradually cooling them.

A Simmulated Annealing is allowing the agent to escape local maxima by allowing some 'bad' moves but gradually decreasing their frequency.

If the annealing process happens slowly enough then the annealing search will find the global optimum.

This approach is widley used in VLSI layout, airline scheduling and so on. 

## Practice 

Google hill-climbing process 

maybe try and create a basic algorithm like this. 




