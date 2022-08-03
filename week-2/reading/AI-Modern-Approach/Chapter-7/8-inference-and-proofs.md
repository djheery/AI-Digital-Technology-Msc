# Inference and Proofs 

**Inference ruules** can be applied to derive a **proof**.

Proof can be seen as a chain of conclusions that will lead towards a desired goal. 

The best known rul is **Modus Ponens** 

Modus Ponens -- Latin for mode that affirms it is writen: 

α => β, α / β 

In reality it looks like a fraction and the / symbol is the seperator between top line and bottomline.

This notation means that: 

Whenever any sentences of the form α => β and α are given. 
Then the sentence β can be inferred as true. 

For example: 

((WumpusAhead ^ WumpusAlive) =>  Shoot) ^ (WumpusAhead ^ WumpusAlive) / Shoot

Breakdown: 
  - If wumpus is ahead and the wumpus is alive this imples shoot 
  - And the Wumpus is ahead in the environment, and it is alive in the environment 
  - Then shoot can be inferred. 

## And-Elimination 

This says that from a conjunction any of the the individual conjuncts can be inferred: 

α ^ β / α 

For example, means that (WumpusAhead ^ WumpusAlive) then WumpusAlive can be inferred, or WumpusAhead can be inferred. 

**See page 241** for a list of logical equivilances. 

Not all inference rules work in both directions. 
For example we cannot run Modes Ponens in the opposite directions on the statement: 

α => β
β => α NOT TRUE 

## Applying Inference Rules and Equivilances to the Wumpus World: 

1. Apply biconditional elimination to R[2] to obtain: 
  - R[6]: (B[1, 1] => (P[1, 2] V P[2, 1]) ^ ((P[1, 2] V P[2, 1]) => B[1, 1]))
    - Breeze at 1, 1 infers there will be a pit at 2, 1 or 1, 2 
    - Pit at 1, 2 or 2, 1 infers there will be a breeze at 1, 1 
2. Apply And-Elimination to R[6]
  - R[7]: ((P[1, 2] V P[2, 1]) => B[1, 1])
    - Eliminated the and from R[6] to infer the 2nd result 
3. Logical Equivilance for **Contrapositives** gives: 
  - R8: (¬B[1, 1] => ¬(P[1, 2], P[2, 1]))
    - If there is not a breeze at 1, 1 then there cannot be a pit at 1, 2 or 2, 1
4. Apply Modes Monens with R8 and Percet R4 (i.e ¬B[1, 1])
  -R9: ¬(P[1, 2], P[2, 1])
  - Scroll up to read about Modus Ponens 
5. Apply De Morgans Rule
  - R10: ¬P[1, 2] ^ ¬P[2, 1]

## Definitions: 

- **Contrapositives** A proposition or theorem formed bby contradicting both the subject and predicate or both the hypothesis and the conclusion of a given proposition or theorem and interchanging them 
  - Basically inverting the a truth value to a not value and vis versa to prove the opposite;
- **Subject**: What a senetence is about 
- **Predicate**: Tells something about the subbject. 

Any of the search algorithms in Chapter 3 can be used to find a sequence of steps that constitutes a proof like the above inference rules and equivilances.

You define the problem as follows: 

- Initial State: The intial KB 
- Action: The actions consist of all the inference rules applied to all sentences that match the top half of inference rules 
- Result: the result of an action is to add the sentence in the bottom half of the inference rule 
- Goal: The state that contains the sentence we are trying to prove. 

## Monotonicity

Final property of logical system is monotonicity 
Monotonicity means that the set of entailed sentences can only increase as information is added to the KB. 

This can be represented as: 

KB |= α then 
  KB ^ β |= α

For example, suppose the KB contains the additional assertation β stating that there are 6 pits in the world. 
This knowledge might help the agent draw *additional* conclusions, but will not invalidate any conclusion α already infered. Such as that there is no pit [1, 2]

Monotonicity means that inference rules can be applied whenever suitable premises are found in the KB.
The conclusion of the rule must follow, regardless of what else is in the KB. 

