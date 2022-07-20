# Inference Engine 

There are many ways of implementing an inference engine.

Typical examples encompasses the recognise-select-act cycle 

## Recognize 

Match the condition of rules against the facts in working memory. 
This is to identify the set of applicable rules to this problem domain. 

## Select 

If more than one rule is matched (Those that can be applied or fired), then use a conflict resolution strategy to solve the conflict; otherwise stop if no rules are matched 

## Act 

Apply the matched rules and update the working memory.
This will usually add new facts or delete old facts from working memory. 

## Stop 

Stop if the terminating condition is fulfilled;

Otherwise return to stage 1 and repeat the cyycle.

The termination condition can either be the reach of a goal state or by resource/time limitation. 

