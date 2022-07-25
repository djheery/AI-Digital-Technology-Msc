# Bayesian Networks

An example Bayesian Network:

                Pr(A)
            ------A--------
            |             |
            |             |
            v             v
   Pr(B|A)  B             C  Pr(C|A)
            |             |
            |             |
            ----->D<-------
              Pr(D | B, C)

A Baysian network is an acyclic graph where the variables of interest are represented as nodes.

Directions in the graph represent the relations amongst variables. 

A conditional probability table is attached to each node and represents the relations strength.

In the above graph is labelled from A to D.
Arrows go from nod A to nodes B and C, which go to D.

Attached to Node A is a probability table Pr(A)
Attached to Node B is a Probability table Pr(B | A)
Attached to Node C is a Probability table Pr(C | A)
Attached to Node D is a Probability table Pr(D | C, B)


      