# Conjunctive Normal Form 

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
