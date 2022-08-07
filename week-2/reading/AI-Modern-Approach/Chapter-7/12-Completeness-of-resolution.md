# Completeness of Resolution

We will now show why PL_RESOLUTION is Complete.

To do this, we introduce **Resolution Closure**. 
Resolution closure can be represented as: 

RC(S)

- S = a Set of clauses
  - These set of clauses are derivable by the repeated application of the **resolution rule** or their to clauses in S or their derivatives.

The resolution closure is what PL_RESOLUTION computes as the final value of the varriable *clauses* in the resolution algorithm in the previous section.

RC(S) must be finite. 

## Ground Resolution Theorem 

The completeness **Theorem** for resolution in propositional logic is called the: 

**Ground Resolution Theorem** 

This theorem is proved by demonstraiting its **contrapositive**.
For example:

(RC(S) !== {}) => S = true  

RC(S) does not equal an empty set then S is satisfiabble. 

We can construct a model for S with suitable truth values for P[1]... P[k]

The constructin procedure is as follows: 

For i from 1 to k 
   if *clause* in RC(S) contains the literal ¬P[i] and all its other literals are false under the assignment chosen for P[1]... P[i - 1 then assign false to P[i]
   else assign P[i] to true.

The assingment to P[1]...P[k] is a model of S

## Definitions 

- **Completeness** 
  - COmpleteness refers to the fact that a complete algorithm will offer at least one solution, which means it is garunteed to find a solution in a finite amount of time. 
- **Resolution Rule** 
  - A single valid inference rule that produces a new clause implied by two clauses containing complementary literals. 
- **Axiom**
  - A sentence that can be regarded as "given" or established. 
    - Self evidently true. 
- **Resolution Closure** 
  - 
- **Theorem** 
  - A truth established by means of accepted truths 
  - A proposition that is not an axiom but can be proved by a chain of reasoning 
  - A statement proved via reasoning and logical deduction rather than being self evident
- **Ground Resolution Theorem** 
  =
- **Contrapositive**
  - A proposition or theorem formed by contradicting both the subject and the predicate
    - If not-B then not-A
      - This is the contrapositive of if A then B (A => B)
      - In notation: 
        - ¬B => ¬A 
- **Predicate** 
  - Part of a clause that states something about a subject 
  - if A then B 
    - B would be the predicate 
    - A the subject 
  - Something confirmed or denied concerning an argument of a proposition. 
