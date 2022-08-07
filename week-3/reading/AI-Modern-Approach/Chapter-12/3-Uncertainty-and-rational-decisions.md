# Uncertainty and Rational Decisions 

Consider an automated car trying to take a journey to the airport. The passenger must arrive at the airport in the next 90 minutes to catch their flight (A[90]). 

Making a rational decision revolves around the importance of reaching various goal state.

If there is a 97% chace of reaching the airport on time is this a rational choice? 
Not necissarly. The choice made by the agent is dependent on the importance of the goal, there are other options that may result in a higher likelyhood of catching the flight. For example if you left 3 hours early (A[180]) there would be a higher probability of reaching the airport in time. 

But by this logic you could also leave 24 hours in advance (A[1440]), this is also not a good choice. Thus a good agent must be able to have **preferences** among the different possible **outcomes**. Leaving enough time to reach the airport in time, but not having a massive wait time. 

**Utility theory** is used to represent preferences and reason quantitiatively with them 

**Utility** is the quality of being useful. Utilities are considered by agent when finding the most rational descision it should take in uncertain environments. 

Utility states are relative to the agent, in chess the black checkmating the white will be high for the agent playing white but low for the agent playing black. 

We also cannot go by a one size fits all for agents. A novice player (Agent A) may be thrilled to draw against a professional chess master (Agent B) thus Agent A's preference for a draw would be exponentially higher than for the oppisite in Agent B which would be catasrophic. 

A **utility function** is used to accounjt for the preferences of an agent 

Preferences (expressed by utilities) are combined with probabilites in the general theory of rational decisions. 
This is called **Decision Theory**

Decision Theory can be represented like this: 

Descision Theory = probability theory + utility theory

**"An agent is considered rational, if and only if it chooses the action that yields the highest expected utility, averaged over all the possible outcomes of an action"**

The above statement is a principle called **Maximum Expected Utility** (MEU)

You can see pseudo code of such an alogorithm on page 406 


## Definitions 

- **Utility Theory** 
  - Used to represent preferences and reason quantitivatively with the prefrenece. 
  - Says that every state has a degree of usefulness, or utility, to an agent.
- **Utility Function**
  - Used to account for preferences of an agent
- **Decision Theory**
  - Used to account for both preferences and probability theory 
  - Probability theory is added with Utility theory to given an indication of what the agents next action should be 
- **Maximum Expected Utitlity**
  - A principle which is used by agents to choose the action that yeilds the highest expected utility when averaging all possible outcomes of an action. 



 

