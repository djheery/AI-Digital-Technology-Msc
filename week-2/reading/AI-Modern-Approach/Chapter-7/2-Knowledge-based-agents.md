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
- Third TELLS the knowledge base which action was chosen and returns the action so that it can be executed. 

The details of the representation language are bstracted into these three functions that implemnt the inference bbetween acutators and sensors on one side, and the core representation and reasoning system on the other. 

**Percept** is the input that an intelligent agent is perceiving at any given moment. 

A knowledge based agent can be built simply by telling it what it needs to know. 
Starting with 0 knowledge in the knowledge base, the agent designer can TELL the sentences systematically adding to the knowledge base so that the agent knows and understands how to operate in its environment. 

This is called a declaritive approach 

A procedural approach will encode the desired behaviours of the agent directly into the code.

A successful agent is often utilizes a combination of both procedural and declaritive elemnts in it's design. 





