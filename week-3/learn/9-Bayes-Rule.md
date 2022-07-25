# Bayes Rule 

Bayes' Theorem can be used in expert systems to manage randomness and uncertainty 
Think about some events being considered 'Hidden Causes'
  - They are not necessarily directly observed, such as a tooth cavity due to eating too many sweets. 

If you model how likely an observable effect is given a hidden cause then Bayes rule allows you to use your model to calculate and infer the likelyhood that hidden cause will occur. 

For example the likelyhood of toothache given that there is a tooth cavity. 

This can be expressed like this: 

P(*cause* | *effect*) = P(*effect* | *cause*)P(cause) / P(effect)

P(effect | cause) is often available in real domains, such as medical diagnosis. 

Remember that you can see this as: 

(P(effect | cause) * P(cause)) / P(effect)

## Meningitis example: 

Suppose Meningitis causes a still neck in 50% of all cases.

This means that P(s | m) = 0.5 

Alongside this it is also known that the probability in the general population of someone having a stiff neck at any one time is 1/20

This means P(s) = 0.05

Also the incidence of meningitis in the population is one in 50,000 

This means p(m) = 0.00002

Thus 

(0.5 * 0.00002) / 0.05

This equals 0.00002 = 1/5000

Bayes inference is a type of diagnostic or evidential reasoning where the prior probability hypothesis is already known.

The prior Probability being known: P(Hi)
The conditional probability: P(Ej | Hi) 

To Compute the posterior probability: 

P(Hi | Ej) 

A chain of references implement probabilistic reasoning. 

Research: 

Posterior Probability
Probability theory some more
Bayes Theorem 
Do some Practice questions.

