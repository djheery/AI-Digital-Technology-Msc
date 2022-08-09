# Naive Bayes Model 

This is how the **full joint distribution** can be written mathematically 

P (Cause,Effect 1 ,..., Effect n ) = 
  P(Cause)∏{i}P(Effect[i]|Cause)

∏  = The product over a set of terms 

Such probbability distribution is known as **Naive Bayes** model

Naive, because it is often used in cases where the "effect" variables are not strictly independent given the cause variable. 

Naive Bayes model is sometimes called a **Bayesian Classifier** 

"To use a naive Bayes model, we can apply Equation (12.20) to obtain the probability of the cause given some observed effects. Call the observed effects E = e , while the remaining effect variables Y are unobserved. Then the standard method for inference from the joint distribution (Equation (12.9)) can be applied:"

P ( Cause | e ) = α ∑ P ( Cause , e , y )
P ( Cause | e ) = α ∑{y} P(y | cause)(∏{j} P(e[j] | cause))
                = α P(cause)(∏{j} P(e[j] | cause)) ∑{y} P(y | cause)
                = α P(cause) ∏{j} P(e[j] | Cause)

Reinterpreting this equation in words: for each possible cause, multiply the prior probability of the cause by the product of the conditional probabilities of the observed effects given the cause; then normalize the result.

Naive Bayes models are widely used for language determination, document retrieval, spam filtering and other classification tasks. 

For medical tasks, where actual values of the posterior probabilities matter a more sophisticated model is needed (as described in the next chapter)