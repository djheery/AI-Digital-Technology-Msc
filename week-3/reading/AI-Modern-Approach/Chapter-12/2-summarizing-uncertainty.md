# Summarising Uncertainty 

Uncertainty can occur in alot of scenarios 

Consider diagnosing a dental patient's tooth ache.

Toothache => Cavity 

This is wrong. It could be one of a wide range of issues: 

Toothache => Cavity V Abcess V WisdomTeeth V GumIssue.......

There could be an infinite list of probable causes, thus the resolvent cannot be exposed. 

We could invert the rule to: 

Cavity => Toothache.

But this is not necissaryly true either, as not all cavities cause toothache. 

trying to use logic to cope with a domain like this fails for three main reasons: 

- Laziness 
  - There is too much work to list the complete set of **antecedents** or consequents 
- Theoretical Ignorance 
  - Medical science has not complete theory for the domain 
- Practical ignorance 
  - Even if we know all the rules, we might bbe uncertain about an individual patient as we do not ahve the necessary tests to understand the individuals needs/ history. 

To summarize the connection between the antecedent and the consequent or visa versa is not a strict logical consequence in either direction. 

This is fairly typical in a medical domain as well as others (law, business, car repair etc).

The agent can only provide a **degree of belief**

The **Onotological Commitments** of logic and probability theory are the same
But the **Epistemological commitemnts** are different 

This means that probability theory provides a way of summarising uncertainty in a domain that comes from some form of ignorance (be it practical or theoretical) or laziness (too many contingencies to plan for). 

Rather than giving a bbinary result, instead it will return the probabbilistic likelyhood of a cause to a problem, whether that be in a medical domain or otherwise. 

For example, based on a patients dental records, or more wide ranging data in it's KB an agent that can handle uncertainty may be able to deduce that there is an 80% (0.8) likelyhood that the toothache is caused by a cavity, which gives the domain expert a useful insite. 

Probbabilistic statements are made with respect to the Knowledge state, to with respect to the real world. 
For example, a patient either has or does not have a cavity, there is no inbetween.
But given the knowledge state of the agent and the current percepts it can give a result which is a suggestion for some domain expert to act upon/ gain evidence that a patient is likely too or unlikely too have a cavity. 



## Definitions: 

- **Antecedents** 
  - Causes/ subjects of a sentences
  - Something that exists before or logically preceeds another 
  - A => B 
    - A is the Antecedent 
    - B is the consequent 
- **Degree of Belief** 
  - A probabalistic likelyhood to the consequent/ antecedent of some consequent/ antecedent 
- **Otological Commitments** 
  - Thye world is composed of facts that do or do not hold in any particular case
- **Epistemological Commitments** 
  - These differ between logical and probabalistic agents 
    - A logicl agents bbelieves each sentence to be binary (true or false) or it has no opinion 
    - A probabilistic agent believes that each sentence may have a numrical degree of belief between 0 and 1. 