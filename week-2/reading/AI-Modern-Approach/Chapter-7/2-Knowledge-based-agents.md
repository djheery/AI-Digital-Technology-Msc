# Knowledge Based Agents 

The **Knowledge Base** KB is a set of **sentences**

**Sentences**: Not described? 

Each sentence is expressed in a language called **knowledge representation language** 

These sentences represent some form of assertion in the real world. 

If a sentence is taken as a given and notd derived from other sentences then  it is known as an **axiom**. 

You must have a way to query you knowledge base 
You also must have a way to add knowledge to the KB 

The standard names for these operations are: 

- TELL (Add)
- ASK (Query)

Both of these operations may involve **inference** -- Deriving new sentence from old. 

Inference must obey the requirement that when one querys a the KB the answer should be a result/ follow on from what has been added to the KB previously 

like other agents it takes a percept as an input and returns an action. 

The agenty maintains a KB iwhich may initially contain some domain knowledge. 

Each time the agent program is 

- First Tells the knowldge base what it percieves 
- Second ASKs the knolefge base what action it should perform in the process of answering this query 
- TELLS the knowledge base which action was chosen and returns the action so that it can be executed. 

The details of the representation language 

**Percept** is the input that an intelligent agent is perceiving at any given moment. 





