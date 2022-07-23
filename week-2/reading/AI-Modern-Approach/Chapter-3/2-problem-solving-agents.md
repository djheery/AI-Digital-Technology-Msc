# Problem Solving Agents 

The Section starts with an example in which you imagine you are in some city in another country, you have a set of goals such as improve your speaking of the language, see sights and avoid hangovers. 

You find yourself stuck somewhere in this country needing to get to another part of the country to catch a non-refundable flight. However, there are only 3 roads out of the city and none of the signs are say they are going to the city you need to be at. 

Thus, without any knowledge of the country/ roads you will not be able to know which road is the best to take to get you to your destination. I.e which one is going in the right direction/ leads to somewhere that will get you to the city. 

In this circumnstance where the agent (you) have not additional information - the environment is said to be **unknown**.

The best that can be done in this situation is to pick a road at random and execute it, doubling back after you have searched the path. 

For this chapter we will assume the agents **always** have access to the information about the world. 

Given this fact the agent will follow a **four-phase problem-solving process** 

1. Goal Formulation 
  - The agent will adopt goals, in this case the goal of trying to reach this other city. 
  - Goals are used to organize behavior and limit objectives to optimize the process of considering the next actions. 
2. Problem Formulation 
  - The agent will devise a description of the states and actions necassary to reach the goal.
    - As a result of this an abstract model will be produced of the relevant part of the world. 
    - In this scenario, the agent should consider the actions of travelling from one city to an adjacent city. This can be done by weighting the paths. 
  - The only state that will change as a result of an action is the current city. 
3. Search 
  - Before taking any action in the real world, the agent simulates sequences of actions in it's model. This is the agent simulating a search of the model, and it will keep doing this until it reaches the goal. 
    - A sequence reaching the goal is called a **solution**. 
    - The search process may produce many solutions or may produce none.
    - Each solution should be weighted and the most optimal should be chosen. 
4. Execution 
  - The agent will now execute the actions of the chosen solution, one at a time. 

### IMPORTANT 

In a fully observable, deterministic, known environment, the soltion to any problem is a fixed sequence of actions. 

This could be Drive from Luton to Nottingham, Nottigham to Sheffield, Sheffield to Leeds, Leeds to Newcastle. 

Assuming the model is correct, and the agent has found a solution, the agent can ignore other periferale steps (percepts) while it is executing its actions. 

In other words only consider the steps of the solution and none of the other steps that would have been considered in the sequenced simulated is the search phase. 

## Open Loop System

The process of ignoring the percepts once a solution has been found and chosen is called an **open loop system**. This name has been coined by **Control Theorists**. 

Ignoring the percepts breaks the loop between agent and the environment. 

If there is a chance that the model is incorrect or the environemnt is non-deterministic, then a **closed-loop** system would be a safer and more optimal choice. 

This is because it monitors the percepts. 

## Closed Loop 

In partially observable or nondeterministic environments, a solution would be a branching strategy that recommends different future actions depending on what percepts arrive. 

An example of this could be when an optimal solution is chosen and the agent starts the execution. As you are advancing city by city the agent gets to a city and the next path to take has a sign which says road close. In this circumstance the agent should re-evaluate it's options and consider an alternative solution by considering it's percepts. 




 