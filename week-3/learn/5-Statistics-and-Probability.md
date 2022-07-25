# Statistics and Probability 

A well-known and well-understood framework for dealing with randomness uncertainty is based on three simple axioms: 

**Axioms**: A statement or proposition which is regarded as accepted, established or self-evidently true.
  - A statement which is widely regarded as true or self-evident.

The three axioms are below: 

1. All Probablilities are between 0 & 1 
  - This can be represented by the following equation: 
    - 0 ≤ P(E) ≤ 1
      - ≤: This means less than or equal to 
      - P(E): 
        - P() = A probability function 
        - E = The event that the probability function will use as an argument 
    - This means that P(E) will be either less than or equal to zero and P(E) will be less than or equal to 1
    - P(E) = 0 only if the event will definitely not occur 
    - P(E) = 1 only if the event is certain to occur
2. The sum of all events that do not affect each other (Mutually exclusive) is 1
  - This can be represented iwht the following equation: 
    - P(E) + P(¬E) = 1
      - E = Event that is mutually exclusive
      - ¬E = Event that is not E
      - Thus: 
        - The probability of E occuring + the probability of an event that is not E occuring is 1
3. Conjuctive Probability of events E and E': 
  - P(E v E') = P(E) + P(E') - P(E' ^ E')
  - P(E v E') = P(E) + P(E')
    - When random events E and E' are mutually exclusive. 

**Mutually Exclusive**: 

In statistics and probability theory, two events are mutually exclusive if they cannot occur at the same time 
  - A simple example of a mutually exclusive event is a coin toss. Both heads and tails cannot occur at the same time, it is statistically impossible
    - Thus P(Heads) + P(Not Tails) = 1
      - P(E) + P(¬E) = 1 

 # Examples of Probbability 

 Toss a coin: What is the probability: 

 - 1/2

 When rolling a die with 6 faces, what is the probability of getting one dot: 

 - 1/6 

 What are the chances of getting two sixes when you roll two dice together: 

 - 1/6 * 1/6 
  - 1/36

What are the chances of getting no sixes when you roll two dices: 

5/6 * 5/6 
  - 25/36

What are the chances of getting at least one six when you roll two dice: 

- 1 - 5/6 * 5/6 = 11/36 or 
- 1/6 + 1/6 - 1/36 = 11/36
  - Axiom 3
    - P(E v E') = P(E) + P(E') - P(E' ^ E')
      - Not 100% on this should research some probability theory 

