# Components of Expert Systems in AI 

The three main components in an AI system are: 

1. The Knowledge Base 
2. The Inference Engine 
3. The Interface

## Knowledge Base 

A knowledge base aims to capture the knowledge of an expert of domain-specific knowledge.

It is usually comprised of a set of production rules which can be seen as IF-Then logic.
Remember that IF logic is essentialy logical implications (IF=>).

Each rule has a condition (or atencedents or premises) and an action (conclusion or consequence).

Atencedents::: a thing that existed before or logically precedes another.

Both can use logical connectors such as ^ (And) v OR and NOT. 

Condition represents what must be true for the rule to fire, while Action indicates what happens when the condition is not met. 

For example: Outlook(sunny) ^ temp(high) goingOut=> takeWater

The implication of the rule forms the action to be taken. 

## Inference Engine 

An inference engine is a procedure or algorithm that decides how to trigger the rules (representing th eexisting knowledge)
This is a basically a repeated application of modus ponens (method for putting in place).

There are two common methods to do this: 

1. Forward chaining (Forward Reasoning)
  - This deduces new facts which derives new information from available data using inference rules 
    - It is known as the breadth-first search stratergy
2. Backword Chaining (Backward Reasoning)
  - Demonstrates the validity of some facts and starts from the hypothesis and works backwards from the consequent to the atecedent
    - This is to see if th efacts suppor the consequence 
      - This is known as the depth-first search strategy 
  

## The Interface 

There are two Interfaces 

1. Knowledge Aquisiton 
  - Encodes knowledge in computer readable language, this is the major bottle neck in producining applicable expert systems. 
    - There are two approaches 
      - Translating human expert knowledge 
      - learning from data using machine learning approaches 
2. Explanation 
  - Convinces the end user that the reasoning is substantially correct and convincess the knowledge engineer that the system is working properly

