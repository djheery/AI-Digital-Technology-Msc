# Conjunctive Normal Form 

The resolution rule applies only to clauses (that is, disjunctions of literals)/

Every sentence of propositional logic is logically equivalent to a conjunction of clauses. 

A sentence expressed as a conjunction of clauses is said to be in **conjunctive normal form** (CNF)

## Converting to CNF

Coverting to CNF

### Definitions

- **Conjunction**
  - A word or operator used to connect clauses. 
- **disjunction**
  - In logic it is the relation of 2 distinct alternatives
  - Often joined by a conjunction operator 
    - P V Q
    - Dan plays football **or** Conor plays Football
- **Conjunctive Normal Form** (CNF)
  - A sentence is said to be in CNF when it is expressed as a conjunction of clause.

The resolution rule only applies to clauses (disjunctions of literals).

A sentence in logic, expressed as a **conjunction** of clauses is said to be in **conjunctive normal form** or **CNF**

## Steps to Converting to CNF: 

1. Eliminate <=> replacing a <=> b with (a => b) ^ (B => a)
  - (B[1, 1] => (P[1, 2] V P[2, 1])) ^ ((P[1, 2], P[2, 1]) => B[1, 1])
2. Eliminate => replacing a => b with ¬α ∨ β 
  - (¬B[1, 1] V P[1, 2] V P[2, 1]) ^ (¬(P[1, 2] V P[2, 1]) V B[1, 1])
3. CNF rquires ¬ to only appear in literals. 
  - This means that we "move ¬ inwards" by repeating the application of equivilances: 
    - ¬(¬α) ≡ α 
    - ¬(α ^ β) ≡ (¬α ^ ¬β)
    - ¬(α V β) ≡ (¬α V ¬β)
  - For example if we apply this to the last rule: 
    - (¬B[1, 1] V P[1, 2] V P[2, 1]) ^ ((¬P[1, 2] V ¬P[2, 1]) V B[1, 1])
4. Now we have a sentence containing nested V and ^ operators applied to literal. 
    - We only need to apply the **distributivity law**: 
      - (¬B[1, 1] V P[1, 2] V P[2, 1]) ^ (¬(P[1, 2] V B[1, 1]) ^ (¬P[2, 1] V B[1, 1]))

This completes the original sentence and puts it into CNF 

However it is much harder to read. 
Although this may be the case, it can be used as input to a resolution procedure. 



## Definitions 

- Conjunctive Normal Form (CNF)
  - A sentence expressed as a conjunction of clauses via a conjunctive operator. 
- **distributivity law**
  - You can see this on page 241, however it is just a table of logical equivilance and how they map
