# Inference Using Full Joint Distributions 

**Probabilistic Inference** is the computation of posterior probabilities for **query** propositions given observed evidence 

We use the **Full Joint Distrubution** as the KB from which answers to all questions may be derived. 

We can begin with the example of Toothache, Cavity, Catch (Tool dentists use). 
These all have Boolean values, leaving 2X2X2 possibble worlds = 8 


you can see a table on page 413 

Remember all probabilites of the joint distribbution must sum up to 1
This is required by axioms of probability. 

To calculate the probability of a Cavity or Toothache using the table on 413 you add up all the probabilities to give you the overral probability of this query occuring. 

P(cavity V toothache) = prob1 + prob2 + ..... + prob[n]

A common task is to extract the distribution over some subset of variables or a single variable. 

Adding all entries of say cavity occuring in the given table is called the **Marginal Probability**

This process is called **Marginalization** or **summing out**

Because we sum up the probabilities for each possible value of the other variables, thereby taking them out of the equation.

This can be written: 

P ( Y ) = ∑[z] P( Y , Z = z ) 

∑[z] sums over all the possibble combinations of values for X 

We can abreviate the equation to: 

**P**(Y, z)

See page 414 for detailed breakdown of the calculation. 

Marginalization and conditioning are useful rules for all kinds of derivations involving probability expressions. 





## Definitions

- **Probabilistic Inference** 
  - The computation of **posterior probabilities** for query propositions given some observed evidence 
- **Postierier probibility**
  - Also known as conditional probability, it is the calculation of the probability of a given event based on some known information or evidence. 
- **Joint Distribution** 
  - The prediction of all combinations of particular values for example: 
  - For example weather has 4 values (snow, sun, rain) and cavity has 2 values (true or false) thus leaving 4 X 2 possible combinations (8) as shown on page 410
  - If we added toothache to that equation which has 2 values (true or false)
    - 4 X 2 X 2 = 16 possible worlds to consider
    - **P**(Weather, Cavity)
      - The probability of the weather having a cavity 
      - Table on page 410 
- **Full joint Distribbution** 
  - The probability model is determined completely by the **joint distribution** for all random variables, the results of which are known as the **Full joint distribution** 
    - For example, Cavity, Toothache, and Weather the full joint distrubution is: 
      - **P**(Weather, Cavity, Toothache)
        - This will generate a table with 16 entries.
- **Marginal Probability** 
  - Extracting the distribution of probabilities of some subset of variables or single variable 
    - Finding the probability of a cavity in the statement: 
      P(cavity)