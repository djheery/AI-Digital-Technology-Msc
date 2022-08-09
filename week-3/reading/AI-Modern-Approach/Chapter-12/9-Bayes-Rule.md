# Bayes Rule and Its Use 

**Product Rule** can be written in two forms: 

- P(a ^ b) = P(a|b)P(b) 
- P(a ^ b) = P(b|a)P(a)

Equating the two right hand sides and dividing by P(a) we get: 

P(b|a) = p(a|b)P(b) / P(a)

This equation is known as bayes rule or bayes theorem 
Bayes Theorem underlies most modern AI systems for probabilistic inference. 

The more general case of Bayes rule for multivalued variables can be written in **P** notation as follows: 

**P**(Y | X) = P(X | Y)P(Y)/ P(X)

We also have occasion to use a more general version conditionalized on some background evidence **e**

**P**(Y | X, **e**) = P(X | Y, **e**)P(Y | **e**)/ P(X | **e**)

Bayes rule is useful as in practice there are many cases where we have good probbability estimates for these three numbers when computing P(b | a): 

P(a | b), P(b), P(a)

OFten we percieve as evidence the effect of some unknown cause and we would like to determine that cause: 

In this case bayes rule becomes: 

P(cause | effect) = P(effect | cause)P(cause) / P(effect)

P(effect | cause) quantifies the relationship given some cause in a **casual direction**

P(cause | effect) describbes a **diagnostic** relationship

In medicine this could be: 

P(symptoms | disease) could be used to find: 

P(disease | symptoms)

Take the Meningitis Example: 

The doctor knows: 

- Meningits patients have a *stiff neck* (S) 70% of the time
- Probability of meningitis in a patient is 1/50,000
- Prior probability that any patioent has a stiff neck is 1%.

s = the proposition that the patient has a stiff neck 
m = the proposition that the patient has meningitis: 

P(s | m) = 0.7
P(m) = 1/50,000
P(s) = 0.01

P(m | s) = (P(s | m)P(m) / P(s)) 
P(m | s) = (0.7 * 1 / 50,000) / 0.01) = 0.0014

This means that only 0.14% of patients with a stiff neck to have meningitis. 

One can avoid assessing the prior probability of the evidence (in this case P(s)) by instead computing the posterior probability for each value of the query (here, m and ¬m) and then normalizing the results: 

P(M | s) = α {P ( s | m )P( m ) , P ( s | ¬ m )P ( ¬ m )} .


The general form of bayes rule with normalization is: 

P ( Y | X ) = α P(X|Y)P(Y)

α = normalization constant needed to make the entries in P(Y|X) sum to 1. 

## Using Payes Rule: Combining Evidence 

P  420 blazin 