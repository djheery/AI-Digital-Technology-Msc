# Basic Probability Notation

Probbability notation is used to represent probabilistic information. 

## What are Probabilities about

Probabilistic assertions, like logical assertions are possible outcomes in universes of discourse. 

Logical assertions strictly rule out possible worlds (all those which the assertion is false) and operate of binary information. 

Probabilistic assertions reason how probable various worlds/ outcomes are.

A set of all possible worlds is called a **sample space** 

Two possible worlds cannot both bbe the case 
And one possible world must be the case 

This means that possibble worlds are considered, **mutually exclusive** and **exhaustive**

Ω: Refers to the **sample space** 
ω: Refers to the elements of Ω
∑: The sum of 

A fully specified **probability model** associates a numerical proability P(ω) with each possible world.

An axiom of probability theory says that: 

*Every possible world has a possibility between 0 and 1*

And 

*The total probability of the set of possible worlds is 1* 

(1 world will definitley occur in a set of possibble worlds)

This is represented with the following equation: 

0 ≤ P ( ω ) ≤ 1 for every ω and ∑ P ( ω ) = 1

**Plain Text**

The probability of each possible world is ≤ (less than or equal to) 0 and  ≤ (less than or equal to 1) 1 for every possibble world.

And the sum of (∑) is 1 as any number of these possible worlds could occur

It is worth noting in the book underneath the Some of quantifier there is this: 

ω ∈ Ω

∈: a subset of the predicate (is an element of..., has set membership to...) 
ω is a subset of Ω

**Events** in probability theory are the sets that are used in probabilistc assertions 
Probabilistic assertions and queries are not usually abbout particular possible worlds but rather about sets of them. 

The probability associated with a proposition is deﬁned to be the sum of the probabilities of the worlds in which it holds:

For any proposition φ, P ( φ ) = ∑ P ( ω )

φ = a predicate variable 
φ a prooposition that may occur such as that two dice will add up to 11, the probabilities that doubles will be rolled and so on. 

**Plain text**

The sum of the proability ω will occur is equals the sum of probabilities of the worlds in which it holds.

For example, when rolling fair dice, we have P ( Total = 11 ) = P (( 5 , 6 )) + P (( 6 , 5 )) = 1 / 36 + 1 / 36 = 1 / 18.


**Uncoditional** or **Prior** Probbabilites refer to degrees of belief in proportions in absence of other information. 

These could be P(Total=11) or P(Doubles) when 2 dice a rolled
P(Total=11) = the probbability that the total number after a roll is 11 
P(Doubles) = the Probability that two die are the same (2, 2) or (5, 5) etc 

Most of the time we have some information usually called evidence. 
In this case we are not interested in the uncoditional probability rather the **conditional** probability or **positerior probability**

| = Given that 

P(total=11 | Die[1]=6)



## Defintions 

- **Sample Space** 
  - A set of all possible worlds
- **Mututally Exclusive**
  - Being related in a way (such that) one excludes/ precudes the other
    - 2 distict events are mutually exclusive if they cannot occur at the same time 
    - **precludes** 
      - Prevent something from happening
        - The secret nature of his work precluded his official recognition 
          - His work could not be recognized because it was secretive. 
- **Exhaustive** 
  - Considering all elements or aspects of a situation/ possible worlds in the case of AI 
- **Probability Model** 
  - A mathmatical abstraction of some real world representation used by an agent in which the probability of possible worlds occuring based on actions is calculated. 
  - A probability model assigns a numerical value to the probability of a possible world occuring via: 
    - P(ω)
    - ω represents the elements located within each world. 
- **Unconditional Probabilites**/ **Prior Probabilities**
  - Probbabilites which refer the the degree of belief in proportions in the absence of other information. 
- **Conditional Probbability**/ **Posterior Probability** 
  - Probability of some event occuring based on knowledge we already have 
    - For example the probbability of the total=11 when two dies are rolled given the first is a 5
      - Written: P(total=11 | die[1] = 5)
        - | means "given that" 
        - Probability that the total is 11 given that Die 1 is equal to 5


