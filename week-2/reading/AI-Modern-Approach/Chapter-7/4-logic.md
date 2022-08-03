# Logic 

A logic must define the semantics of sentences. (Semantics = meaning)
The semantics defines the truth of each sentence with respect to each possible environment/ world. 

For example 

x + y = 3

This is true in an envrionment where:

x = 1;
y = 3; 

(or visa versa)

but not in an envrionment where: 

x = 5;
y = 2;

In standard logic every sentence must either be true or false

## Models 

Models are mathematical abstractions of a "possible world". 
Each model has a fixed truth value for every relevant sentence the agent percievs. 

α = sentence 

If a sentence (α) is true in model m It is said that:

 m satisfies α 

Or sometimes it may be said:

that m is a model of α

This can be notated as: 

M(α)

## Logical Entailment 

Logical entailment is the idea that a sentence follows logically from another sentence. 
In mathmatical notation this is: 

α ╞ β

This means directly 

sentence α is true therefore sentence β is true 

α ╞ β if and only if M (α) ⊆ M ( β ) 

⊆ = Is a subset of 

The direction of ⊆ means that α is stronger than β (This rules out more possible worlds)

In understanding entailment and inference, it migh thelp to think of the set of all consequences of KB as a haystack and of each sentence as a needs. 

Entailment is like the needle being in the haystack, inference is like finding it. 

If an inference algorithm i can derive some sentence from the KB it is notated like this: 

KB |- i α,

|- is not the proper representation. check the top of page 234 to see it. 

## Soundness/ truth Preserving

An inference algorithm that derives only entailed sentences is called sound or truth preserving. This is a highly desirable property of an inference algorithm. 

Model checking is a sound procedure. Only applicable when the space is finite (world is of a fixed size, such as the wumpus world.)

## Completeness

Completness is also desirable, an inference algorithm is complete if it caqn derive any sentence that is entailed (any needle that exists in a haystack).

Completeness is an issue in infinite knowledge bases.


## Grounding 

Grounding is the connection between the logical reaasoning process of the agent and the real environment in which the agent exists. 

"How do we know that KB is true is in the real world"


## Knowledge Base 

The Knowledge base can be thought of as a set of sentences.
Or a single sentence that asserts all individual sentences. 

The KB is false in models that contradict what the agent knows. 







