# Simulated Annealing

**Annealing** A heat treatment used from glass in which it is heated up to increase the maliablity of the material then cooled down and set to into the shape it has been changed into.

Hill climbing algorithms that never make downhill moves toward states a vunerable to getting stuck at a local maximum. 

The overall structure of the simulated-annealing algorithm (Figure 4.5) is similar to hill climbing. Instead of picking the best move, however, it picks a random move. If the move improves the situation, it is always accepted. Otherwise, the algorithm accepts the move with some probability less than 1. The probability decreases exponentially with the “badness” of the move— the amount ∆ E by which the evaluation is worsened. The probability also decreases as the “temperature” T goes down: “bad” moves are more likely to be allowed at the start when T is high, and they become more unlikely as T decreases. If the schedule lowers T to 0 slowly enough, then a property of the Boltzmann distribution, e ∆ E / T , is that all the probability is concentrated on the global maxima, which the algorithm will ﬁnd with probability approaching 1.
