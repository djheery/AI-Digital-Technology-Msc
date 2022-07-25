# Fuzzy Expert Systems 

If there is an input of fuzzy values (values that are somewhat vague or exist in the excluded middle) then it is the responsibilitey of the inference engine to use fuzzy rules to output a fuzzy value.

This is the process of the inference engine: 

Rule base => Inference Engine <=========== Mamdani Inference 
              | |         | |         ||== TSK Inference 
               V           V
             Input        Output
            (crisp or fuzzy I/O)

## Crisp Relation as Rules 

Crip relation/input == input that is clear

Rules: 

- IF the colour is green 
    - THEN the maturity is unripe 
- IF the colour is yellow 
    - THEN the maturity is half-ripe 
- IF the colour is red 
    - THEN the maturity is ripe 

|         | Unripe    | Half-ripe     | Ripe      |
---------------------------------------------------
| green   |   1       |     0         |     0     |
| yellow  |   0       |     1         |     0     |
| red     |   0       |     0         |     1     |

## Fuzzy Rule as a Relation

Given the prior section a yellow tomato is some extent of ripe but not fully ripe.

|         | Unripe    | Half-ripe     | Ripe      |
---------------------------------------------------
| green   |   1       |     0.1       |     0     |
| yellow  |   0.1     |     1         |     0.8   |
| red     |   0       |     0.2       |     1     |

There is a line graph on the vle in the section of this title that represent where the colours ar placed using a fuzzy set