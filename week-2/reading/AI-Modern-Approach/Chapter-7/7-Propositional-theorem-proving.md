# Propositional Theorem Proving 

**Model Checking**: Enumarating the possible mathmatical abstractions of the world (models) and showing that a sentence will hold in all of the enumarated models. 

Entailment can be done by **theorem proving** 
 **Theorem Proving** is applying the rules of inference directly to the sentences in our KB to construct a proof of the desired sentence without consulting models. 

 ## Logical Equivilance 

 Logical Equivilance is when sentences α and β are logically equivilant. 
 This means that they are true in the same set of models. 

 This can be written as: 

 α ≡ β.

 Note that ≡ is used to make claims about a sentence, whereaas <=> is used as part of a sentence.

 An example could be that: 

(P ∧ Q) ≡ (Q ∧ P)

Another scenario:

α ≡ β if and only if α |= β and β |= α

In plain english means, sentence α  is logically equivilant ≡ to β if and only if |= each sentence entails the other. 

## Validity 

A sentence is valid if it is true in all models 

Valid sentences are known as **tautologies** (They are necessarily true)

**dedution theorem**

For any sentences α and β , α |= β if and only if the sentence ( α ⇒ β ) is valid.

This means that we can imply a entails b if a implies b 

## Satifiability 

A sentence is said to bbe satifiable if it is true in (or satisfied by) , some model. 

Satifiability can be checked by enumerating the possible models until one is found that satisfies the sentence.

