# Quantifiers 

Quantifiers are used to provide quantitive term to terms in a logic statement. 

## Universal Quantification 

Universal quantification asserts that a certain property holds for every element of a set.

Universal quantification is notated with a ∀

This allows one to capture statements such as 'for all' or 'for every' 

Examples:

- 'Everyone likes cake' || This could be written like:  
  -  ∀x likes(x, cake)
    - likes is the function, and x is the set with everyone, and cake is the second argument 
- 'All frogs are green' || This could be formally written as: 
  -  ∀x frog(x) ^ green(x)
    - all frogs are x and all x are green 
- 'All brown frogs are big'
  -  ∀x frog(x) ^ brown(x)=>big(x)
- 'Every mother is older than her child'
  -  ∀x older(mother(x), x)

 ∀ is a conjunction across all the elements in the set that it is applied to ('for this ^ this ^ this ^ this ....') thus is a shorthand for AND in these situations as it obeys the same rules. 

 ## Existential Quantification 

 An existential quantifier asserts that a property holds for **some** elements of the set. Therefore in plain language it is equivelant of: 

 'There exists one x such that ...Some statement is true...'

 Existential Quantification is written with an Ǝ

 Examples: 

 - 'Some people like cake' || Can be written 
  - Ǝx like(x, cake)
- Some frogs are green || Can be written 
  - Ǝx from(x)=>green(x)
- There is a brown frog which is big || Can be written
  - Ǝx frog(x) ^ brown(x) ^ big(x)
- There is a customer whom bob likes || Can be written
  - Ǝx customer(x) ^ likes(x, Bob)

Ǝ is a disjunction and is another usefule shorthand that obeys the rules of or v (or)

## Quantifiers 

There is a connection between Ǝ and ∀ via negation 

For example: 

- ∀x ¬likes(x, cake) is equivalent to ¬Ǝx likes(x, cake)
  - every person does not like cake 
  - There doesnt exist a person who likes cake
- ∀x likes(x, iceCream) is equivalent to ¬Ǝx ¬likes(x, iceCream)
  - There doesn't exist a person (x) who doesn't like icecream


Two quantifiers can be written at the same time: 

- There is something that everyone likes 
  - Ǝy ∀x  likes(y, x)
- There is someone who likes everything 
  - Ǝx ∀y likes(x, y)
- Everything is loved by someone 
  - ∀x Ǝy loved(x, y)

To review the robot gripper example: 

- ∃x ∃y position(gripper, x) ∧ position(target, y) ∧ (x < y)
  - if gripper in coordinate x and in position y and coordinate x is greater than y then target can be gripped ???? 
  
   