# Bayseian Theorem 

Given event A has happened, the conditional probability of a hypothesis event B, P(B | A) follows the following bayes theorem: 

- P(B|A) = P(A|B) P(B) / P(A)

Consider the dice example: 

Roll one white die and one dark blue die together
Find out the probability of the white die bbeing 5 given that the sum of dots is 11: 

- B: the white die is 5 
- A: the sum of all dots is 11
- B|A: the probability the white die is 5 given that the sume is 11
- A|B: the sum of all dots is 11, given that the white die is 5 

P(whiteDie5 | sum11) = P(sum11 | whiteDie5) P(whiteDie5) / P(sum11)

## Bayesian Theorem Example:

Again consider this example:

Roll one white die and one dark blue die together
Find out the probability of the white die bbeing 5 given that the sum of dots is 11: 

Given the above lets break down the calculations: 

B: the white die being 5
P(B) = 6/36 = 1/6

A: the sum of dots is 11
P(A) = 2/36 = 1/18

A|B = the sume is 11, given that the white die is five
P(A|B) = 1/6

B|A: the white die is 5, given that the sum of dots is 11 
P(B|A): 1/2

## Related Bayesian Theorem Question

Roll one white die and one dark blue die together.
Find out the probability of the sum of dots is 11, given that the white die is 5:

A|B: a sum of 11 dots given that the white die is 5 
P(A|B): 1/6

B|A: the white die is 5 given that the sum of all dots is 11
P(B|A): 1/2 

B: the probability that the white die is 5: 
P(B) = 1/6

A: the sum of all dots is 11
P(A) = 2/36 = 1/18

P(A|B) = P(B|A) P(A) / P(B): 
  - (1/2 * 1/18) / (1/6) = 1/6

Note that P(B|A) P(A) is bracket notation in which could really be seen as (P(B | A) * P(A)) / P(B)






