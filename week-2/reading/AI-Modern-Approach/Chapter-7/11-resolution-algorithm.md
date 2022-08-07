# A Resolution Algorithm 

Inference procedures based on coming to a resolution work by using the principle of **proof by contradiction**

## Resolution Algorithm Code Example: 

function PL_RESOLUTION(KB, α) RETURNS true or false 
  inputs: 
    - KB (The knowledge Base)
    - α: A sentence in propositional logic 
    - The Query 
  
  *clauses* <==== The set of clauses in the CNF representation of KB ^ ¬α
  *new* <==== {}

  while true do 
    for each pair of clauses C[i], C[j] in *clauses* do
      *resolvents* <==== PL_RESOLVE(C[i], C[j])
      if *resolvents* contains empty clause then return true 
        *new* <==== *new* ∪ *resolvents*
      if *new* ⊆ *clauses* then return false 
        *clauses* <==*clauses* ∪ *new*

## Code Explanation: 

PL_RESOLVE: returns the set of all possible clauses obtained by resolving the two inputs 

The resolution rul is applied to the resulting clauses. 
Each pair that contains complementary literals is resolved to produce a new clause
This is then added to the set, if it is not already present. 

The process will continue until one of two things happens: 

- There are no new clauses that can be added, in whcih KB does not entail α
- Two clauses resolve to yield an empty clause, in which case KB entails α

The empty clause— a disjunction of no disjuncts— is equivalent to False because a disjunction is true only if at least one of its disjuncts is true. Moreover, the empty clause arises only from"

Any clause in which two complementary literals appear can be discarded as it is the equivilant of deducing: 

True is True. 

Read more on page 246 

## Definitions 

- **Proof by contradiction** 
  - This can be represented like this: 
    - If KB |= a then (KB ^ ¬a) is unsatisfiable.
    - It is used to prove contradicction 
- **∪**
  - The union operator 
  - A union between set A and Set B 
  - Above it represents a Union between New (an empty set) and resolvents (the resolved clauses)
- **⊆**
  - Means is the left operand a subset of the right operand for example: 
    - Is set A a subset of set B ≡ A ⊆ B