# Predicate Logic 

Propositional logic does not have the expressive power to capture these statements: 

- Every Bird can Fly 
- A Penguin is a bird 
- The deduction would likely be that penguins can fly which is not true 

This is an example of logical interference .

Another example of expresiveness about the positional relationship between a robot gripper and it's target object. 

Should you list all the coordinates for comparison between the object and the gripper? Surely not as this may be an infinite number of propositions. 

Predicate logic would be used to represent this task and it would look something like this: 

- ∃x ∃y position(gripper, x) ∧ position(target, y) ∧ (x < y)

Propositional logic works on the assumption that the world contains facts (propositions). 

Predicates on the other hand are used to descibe certain properties or relationships between individuals or objects. 

First-order predicate logic assumes the world contains: 

- Objects (Also known as **Terms**)
  - People, houses, numbers, colors, games, countries are examples of these terms (objects)
- Relations and functions 
  - Red, round, prime, brother of, parents of, mortal enemy of, shorter than, fatter than, outside of. 

A predicate is a proposition whose truth depends on the value of one or more variables.

Variables are the placeholders for constants, like programming languages they are fixed value things such as someones name, a number, a password, so on. 

An example of this could be: 'x' is a prime number. 
The above predicates truth is entirely dependent on the value of x.

A function like notation is used to denote a predicate supplied with specific variables. 

To show this: 

- Prime_number(7) 
  - this would be true 
- Prime_number(9) 
  - this would be false 

Prime_number is the function name. 
