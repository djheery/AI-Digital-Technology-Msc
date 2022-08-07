# The Language of Propositions in Probability Assertions 

Possible worlds are u8sually written in notation that combines elements of propositional logic and constraint satisfaction notation. 

This is called **Factored Representation**. 
A more expressive **Structured Notation** is also possible (Represented in Chapter 18)

**Random Variables** Are variables in probability notation, and their names begin with an uppercase letter. 

Every random variable is a function that maps from the domain of possible worlds Ω to some **range**

Names for values are always lowercase. 
You may write to sum over the values of X: 

∑[x] P (X = x)

Value a = true is simple written as: 

a

Value a = false is written as

¬a

Variables can have infinite ranges, either discrete (like integers) or continuous (like reals)

“The probability that the patient has a cavity, given that she is a teenager with no toothache, is 0.1” can be expressed: 

P(cavity | ¬toothache ^ teenager) = 0.1; 

It is common to use a comma for conjunction in probability notation (like arguments to methods in programming)

P(cavity | ¬toothache, teenager) 

Sometimes we may want to write out all the given probbabilites of possibble values for a random variable.
Rather than writting it like this: 

P(Weather=sun) = 0.68
P(Weather=rain) = 0.2
P(Weather=cloud) = 0.01
P(Weather=snow) = 0.01

We can write it out as an abbriviation: 

**P**(Weather) = {0.68, 0.2, 0.01, 0.01}

When **P** is bold this indicates a **vector** of numbers.
It is said that the **P** statements defines the probability distribution for the random variable Weather.


For continuous variables it is not possible to write out the entire distribbution as a vector 
This is because there may bbe an infinite amount of values. 

Instead we can define the probbability that a random variable takes on some value x as a parameterized function of x. 

This is usually done using a **Probability destiny function**: 

P(NoonTemp=x) = Uniform(x;18C, 26C)

This represents that the temperature at noon is distrubbuted uniformly between 18 and 26 celsius. 
The temperature will be within the bounds of 18C and 26C at noon and it may be anywhere inbetween these numbers at any given instance. 

**Go back to page 410 to read about Joint proabability Distribution** 

## Definitions 

- **Factored Representation**
  - When a possible world is represented by a set of variable/value pairs
  - A mixture or propositional logic and constraint satisfaction notation
- **Random Variables** 
  - The name of variables in proability notation, represented with an uppercase letter: 
    - *Total=11*
    - *Die=5*
- **Range** 
  - The set of possibble values that a possible world can take on 
    - The range of Die[1] is {1,....,6}
    - The total for two dice is {2...12}
    - A boolean random variable has a range of {true, false}
- **Probability Vector**
  - In probability a vector is a matrix of non-negative numbers which sum up to 1 to give the proportional representation of each possibbility occuring for a given Random variable. 
- **Catogorical Distribution** 
  - A finite, **discrete** range of probbability distributions.
    - **Discrete** in mathmatice means objects that can only assume distinct, separate values 
    - **Discrete mathmatics** is the study of mathematical structures that are countable or otherwise distinct or serable 
      - Graphs
      - Combinations 
      - Logical statements 
- **Probability Destiny Function** 
  - A parameterized function that works out the probability of some coninuous random variable with a value of x, will fall somewhere in the bounds of a uniformed function between 2 or more arguments 
    - See Line 58 



 


