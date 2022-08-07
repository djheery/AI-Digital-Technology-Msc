# Quantifying Uncertainty 

Agents in the world need to handle uncertainty. 

Uncertainty could be caused by: 

- Partial Observability 
- Nondetrerminism 
- Adversaries 

An agent may never know for sure what state it is in now or where it will end up after a sequence of actions. 

Problem solving agents keep track of a **belief state** and generating a contingency plan that handles every possible eventuality that its ensors may report during execution. 

This process only works on simple problems. 

The drawbacks of this process are as follows: 

- The belief-state can grow large and can be full of unlikely possiblities 
- A contingent plan can grow arbitraliy large and must consider many unlikely contingencies 
- Sometimes there is no plan that is gauranteed to achieve a goal yet the agent must act 
  - It must have some way to comare the merits of plans that are not garunteed.

Situations where there are contingencies cannot be deduced/ planned (Such as a metorite hitting the road for an automated taxi drive) for is called a **logical qualification problem**

To handel these issues the agent must make a **rational descision**

## Definitions 

- **Belief State** 
  - A representation of all possible world states that it might be located in
- **Logical Qualification Problem** 
  - Situations in which contingencies cannot be accurately deduced 
    - Will an automated taxi have a crash, will a metorite hit the road, will there be road closures
    - In the situation the taxi must arrive in a location in a specific time period.
- **Rational Decision** 
  - The agent must consider the relative importance of various goals and the likelihood, and degree to which they will be achieved
