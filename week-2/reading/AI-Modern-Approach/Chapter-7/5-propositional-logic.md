# Propositional Logic

Propositional logic is used to implement the semantic (domain knowledge) notion of entailment. 

## Syntax

- Atomic sentences consist of a single propositions symbol. 
- Each symbol stands for a specific proposition. 
- Each proposition is either true or false. 
- Symbols start with an uppercase letter and may contain other letters or subscripts
- Examples of symbols: 
  - P, Q, R, W [1, 3], FacingEast
    - [1, 3] = small sub letters 
  - Names are arbitry
  - W [1, 3] can stand for WUmpus in these coordinates 
  - 2 propositions symbols
    - True is always-true proposition
    - False is the always-false proposition.  
- Complex sentences are constructed from simpler sentences. , using parenthese and operators
  - These are called logical connectives

## Logical Connectives: 

- ¬: Not 
- ∧: And 
- ∨: Or
- =>: Implication 
- <=>: If and only if

## Book Example: 

Sentence → AtomicSentence | ComplexSentence
AtomicSentence → True | False | P | Q | R | . . .
ComplexSentence → ( Sentence ) 
                | ¬ Sentence 
                | Sentence ∧ Sentence
                | Sentence ∨ Sentence
                | Sentence ⇒Sentence 
                | Sentence ⇔Sentence 

OPERATOR PRECEDENCE : ¬ , ∧ , ∨ , ⇒ , ⇔

## Semantics 

Semantics define the rules for determining the truth of a sentence in respect to a particular model

In propositional logic, a model sets a truth value (true/ false) for every symbol. 

For example, if the KB makes use of propsition symbols P[1, 2], P[ 1, 4]

One possible model is: 

m[1] = {P[1, 2]= *false*, P[1, 4]=*true*}

with 3 proposition sumbols there are 2^3 = 8 models. 

Models are purely mathamatical, with no connection to the wumpus world. 

P[1,2 ] could mean there's a pit or I'm in portugal tomorrow and today. 

## Rules for Complex Sentences

iff == if and only if <=>

- ¬ P is true iff P is false in m . 
- P ∧ Q is true iff both P and Q are true in m  
- P ∨ Q is true iff either P or Q is true in m . 
- P ⇒ Q is true unless P is true and Q is false in m . 
- P ⇔ Q is true iff P and Q are both true or both false in m


This can be expressed with truth tables (example on page 237)

