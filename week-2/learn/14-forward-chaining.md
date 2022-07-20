# Forward Chaining 

There are two ways of inferences 

- Forward Chaning
  - Breadth First Search 
- Backward Chaining 
  - Depth First Search 

Forward chaining starts with the facts 
  - Data driven, bottom-up approach 
  - Many rules may be applicable at each stage and may be applied 

Forward chaining is said to be unconcious and not guided by a gaol
  - Computes all the facts that can be derived from the facts 
    - known as describing the situation based on the knowledge base. 
  
Forward chaining is suitable for 

- Planning 
- Monitoring 
- Control Applications 

### Typical Process 

1. Start with the facts in working memory, which represent the current situation 
2. Match the facts with the antecedents of rules 
3. Fire the matched rules (apply modus pones to derive new facts)
4. Add new facts into the working memory 
5. Based on the updated set of facts, repeat step 2 until no rules can be matched or the resource restriction is met

## Forward Chaining Example: 

FACT: AgentA Loses weapon 

      AgentA gets shot 
      AgentB is nearby 
      AgentB is friend 
      AgentB has plasma gun 

FIRE Rule1

losesWeapon(x) ^ getsShot(x) => rescue(x)

New fact AgenA needs rescue 

FIRE Rule2

needsRescue(x) ^ nearby(friend(y)) => fire

AgentB Fires 

FIRE Rule3 

fires(y) ^ plasmaGun(y) => killEnemy()

New Rule Agent B Kills enemy 


NOT SURE IF THE ABOVE ARE CORRECT 

