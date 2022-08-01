# Local Search and Optimization Problems 

Sometimes we care only about the final state and not the path needed to get there. 

## Local Search Algorithims 

Local search algorithms search from the start state to neighboring states without keeping track of the paths.

They also do not store which states have been reached/ visited. 

This means they are not systematic. 

2 key advantages: 

- Use very little memory 
- They often find reasonable solutions in large or infinite statte spaces 
  - Where systematic algorithms are unsuitable. 

Local search algorithms can also solve optimization problems, in which the aim is to find the best state according to some objective function (A function with an objective)

## Hill-Climbing Search

"The hill-climbing search algorithm is shown in Figure 4.2. It keeps track of one current state and on each iteration moves to the neighboring state with highest value— that is, it heads in the direction that provides the steepest ascent . It terminates when it reaches a “peak” where no neighbor has a higher value. Hill climbing does not look ahead beyond the immediate neighbors of the current state."

There is a description of this search on page 130 using the 8-queens proble,. 

**Complete-state-formulation**: Means that every state has all the components of a solution, but they may not all be in the right place. 

Hill climbings is sometmimes called a greedy local search this is because it grabs a good neighbour without thinking ahead to har. 

- Local Maxima: A peak that is higher than each of its neighboring states but lower than the global maximum. 
- Ridge: A ridge results in a sequence of local maxima, this is very difficult for greedy algorithms to navigate. 
- Plateaus: A plateau is a flate area of the state-space landscape, it can be a flat local maximum or a **shoulder**, from which progress is possible. 
- A hill climbings search can get lost wandering on a plateu 

In each case the algorithm reaches a point at which no progress is being made. 

"The hill-climbing search algorithm is shown in Figure 4.2. It keeps track of one current state and on each iteration moves to the neighboring state with highest value— that is, it heads in the direction that provides the steepest ascent . It terminates when it reaches a “peak” where no neighbor has a higher value. Hill climbing does not look ahead beyond the immediate neighbors of the current state."

## How to Solve More Problems 

- We could allow a sideways move, in thge hope that the plteau is really a shoulder. 
  - We would need to limit the number of consecutive sideways moves after stopping, this way we would hopefully keep climbing a shoulder but not wander a plateu forever 
  - This increases the success of this algorithm from 14% to 94%. 
    - There is a cost, a success averages 21 steps however a failure averages 64 steps. 

**Stochaistic**: Random Probability 

Varients of Hill Climbings 

- Stochastic Hill Climbing 
  - CHooses at random among uphill moves 
  - The probability of selection can vary with te steepness of the uphill move. 
- First Choice Hill vlimbings 
  - Implements Stochastic Hill Climbing by generation successors randomly until one is generated that is better than the current state. 
  - Good stratergy when a state has many successors (sometimes thousands)
- Random Restart Hill Climbing 
  - Searches from randomly generated intial states until a goal is found 







