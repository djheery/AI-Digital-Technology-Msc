# Propositional Logic 

There are multiple types of logic, but the two most relevant to the field of AI are: 

- Propositional Logic 
- First-Order Predicate Logic 

Based on Aristotles logic, propositonal logic and first-order predicate logic are known as 'two valued'. 

Two valued logic assumes everything is either true or false and there is no middle ground (Known as the excluded middle).

First we shall explore propositional logic

All variables in a proposition should be atomic for example: 

- It is dark 
- The street lights are on

From the above subjects a new proposition can be formed by connecting the two variables: 

- If it is dark, then the streetlights must be on. 

This proposition states that 'it is dark' and implies that due to this the streetlights are on. 

- In this statement you should use a logical operator known as an "Implication"

**An implication is a logical operator used to show one proposition variable implies another**

An implication logical operator looks like this: 

if it is dark => the streetlights are on. 

"=>" is the implication logical operator.

## Logical Operators 

- NOT :: ￢ 
  - Negation, this inverts the truth of the proposition 
- AND :: ∧
  - Conjunction, this required both conjored propositions to be true for the whole conjunction to be considered as true. 
- OR :: v
  - Disconjuntion, this requires one of the conjored propositions to be true for the whole disjunction to be true 
- IF :: => 
  - Implication, true if the antecedents are true while the consequent(s) are true, and is also true when the antecedents are false.
  - In other words P => Q means 
    - if P is true then Q is true. 
  - Otherwise no claim is made. 
  - If that is staisfied, then the implications are ture 
- IFF :: <=>
  - Equality, the two propositions are equivalent or 'if and only if' 

**Antecedent** ==> a thing that existed before or logically precedes another.

## The Truth Table 

You can list the binary values (True, False) of A and B on which the logic statements are derived: 

| A     | B     | (A)     | NOT A     | A ^ B   | A v B   | A => B    | A <=> B |
---------------------------------------------------------------------------------
| t     | t     | t       | f         | t       | t       | t         | t       |
---------------------------------------------------------------------------------
| t     | f     | t       | f         | f       | t       | f         | f       |
---------------------------------------------------------------------------------
| f     | t     | f       | t         | f       | t       | t         | f       |
---------------------------------------------------------------------------------
| f     | f     | f       | t         | f       | f       | t         | t       |
---------------------------------------------------------------------------------

## Propositions 

Propositions (statements) are only allowed to be true or false, they cannot be anything in between (The excluded middle).

The propositional calculus defines an argument as **a list of propositions** 

In a valid argument, it is a list of propositions, the last of which follows from - or is implied by - the rest of the premises. 

The simplest valid argument is known as **modus ponens** (method of affirming): 

1. P => Q
2. P
-------------------
∴ Q

Or: (P ⇒ Q) ∧ P ╞ Q

Breakdown of the above: 

This literally means: 'If P is true, Q is true'

In this circumstance P and Q are the propositions

╞ is read as 'therefore'

a final breakdown could be: 

if P is true then thefore Q is true. 

- Propositional logic can be used to derive knowledge which was previously unknown. This can be done in AI.
  - In AI knowledge is represented as propositions (aka facts). The existing knowledge forms the knowledge base (KB).
  - This means that you can gain knew knowledge from the KB 
    - More formally put: a Knowledge Base (KB) entails true if every model of KB is also a model of Q.
    - Or: Q follows from KB (KB ╞ Q)

  Propositional logic is widely employed in simple rule-based systems

## Limitations of Propositional Logic 

- Variables must be discrete
  - In otherwords they must be atomic or "individually separate and distinct"
- There is limited exprfession on logical connections or interrelationships between propositions
- Propositional logic does not support quantifiers
  - Quantifiers are words, expressions, or phrases that indicate the number of elements that a statement pertains to.
- Propositional logic only supports two-valued logic (true or false)
  - Law of the excluded logic 
  - Probabalistic logic can better handel random, unpredictable events and inputs 
  - Fuzzy logic can better deal with partial membership 
    - Partial membership is the state of being between true or false. 

