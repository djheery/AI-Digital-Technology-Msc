# Measuring Performance 

To choose the optimal algoithm you must measure their performance by considering a select criteria 

- Completeness 
  - Is the algorithm guaranteed to find a solution when there is one 
  - Will it correctly report a failure if the solution is not found 
- Cost complexity 
  - Does it find a solution with the lowest path cost of all the solutions 
- Time Complexity 
  - How long does it take to find a solution 
  - This can be measured in seconds or more abstractly by the number of states and actions considered 
- Space complexity 
  - How much memory is needed to perform the search? 

A search algorithm must be systematic in the way it explores an infinite statespace, to ensure that it can eventually reach any state that is connected to the initial state 

An example could be on an infinite grid, a systematic search could be a spiral path around the intial state s before performing another spiral path s + 1 steps away. 

