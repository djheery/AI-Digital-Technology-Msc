# Backward Chaining 

Backward Chaining is goal driven 

1. IT begins with a desired goal 
2. You must then match the goal with the consequence of the rules in the rule base and find the matched rules to fire. 
  - If no rule can be matched, terminate the algorithm 
3. Check workin gmemory to see if th eatecedents are true. If yes, terminate the backward search and a solution has been found so progress to final step. 
  - If no take the missing antecedents as the sub-goals and recursively go back to the first step 
4. based on the solution path, work forward to output the solution 

Backward chaining has a clear goal and terminates as soon as the goal is reached. 
  - It is a top down approach 
  - Depth first search stratergy 

Backward chaining is suitable for diagnostic, prescription and debugging applications. 

It has a finite number of conclusions 

A backward chaining model. There is a box labelled Facts which contains A, B, C, E, G, H … … There is a cylinder labelled Knowledge base that contains B AND F => Z and C AND D => F and A => D. Dotted arrows from these lines of text point to the following three statements, respectively: B AND F => Z, C AND D => F and A => D. These sit above a query line which is represented by four chevrons that read in turn, Goal Z, Need F, Need D and Found a solution. This series of chevrons leads to A => D, C AND D => F and finally B AND F => Z which finishes in an output. 