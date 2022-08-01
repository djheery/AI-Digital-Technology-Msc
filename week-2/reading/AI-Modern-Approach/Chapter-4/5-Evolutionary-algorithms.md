# Evolutionary Alogorithms

Evolutionary Algorithms can be seen as variants of stochaistic beam search. 

They are motivated by the metaphor of natural selection in biology 

- Survival of the fittest 
  - Where an individual represents a state 
  - The fittest represents the state with the highest value. 
  - These individuals produce offsring in the form of successors. 
  - Then populate the next generation (**recombination**)

## Variety in Evolutionary Algorithms 

There are endless forms of evolutionary algorithims, they vary in the following ways: 

- The Size of a Population 
- The representation of each individual 
  - In Genetic algorithms each individual is a string over a finite alphabet 
  - Evolutions strategies, an idividual is a sequence of real numbers in genetic programming. 
- The Mixing number (p)
  - This is the number of parents that come together to form offspring 
    - Most common p = 2
    - 2 parents combine their genes (parts of their representation) to form offspring 
    - When p = 1 we have stochastic beam search (asexual)
    - p > 2 only rarely occurs in nature but can be simulated. 
- Selection 
  - Process of selecting individuals who will become parents of the next generation 
  - One way is to select from individuals with probability proportional to their fitness score 
  - Another: Randomly select n individuals (n > p) and then select p most fit ones as parents 

- **Mutation Rate** 
  - Determins how often offspring have random mutations to their representation 
  - Once an offspring has been generated, every bit in its composition is flipped with probability equal to mutation rate 
- The makeup of the next generation 
  - This can be just newly formed offspring
  - Can include a few top-scopring parents from previous **elitism** 
  - The practice of **culling** in which all individuals below a given fitness threshold are discarded. 

  **read about the combination function on page 135** 

  **See a psuedo-code for a genetic algorithm on page 137** 

