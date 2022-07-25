# Real World Problems

We have already seen how the route finding problem is defined in terms of specified locations and transitions along edges between them. 

Route finding algorithms are used in a variety of applications including: 

- Web Sites 
- In care Systems 
- Google maps 
- Routing video streams in computer networks
- Military operations planning 
- Airline travel planning 

Consider airline travel we will breakdown the probelm solving formulation: 

- **States**
- Each state includes a: 
  - Location 
  - Current Time 
    - Must record historical states to dictate what a new state may be for a flight
      - Previous flight segments 
      - Fares 
      - Domestic or international travel 
- **Intial State** 
- The User's home/ selected airport 
- **Actions** 
- Take any flight from the current location (current state)
- In any seat class 
- Leaving the airport after the current time 
- Leaving enough tme for within-airport transfer if necessary 
- Leaving enough time for Baggage checkin 
- **Transaction Model** 
- The state resulting from taking a flight will have the flight's destination as the new location and the flight's arrival time as the new time 
- **Goal State** 
- A destination city. Sometimes the goal can be more complex such as arrive at the destination with no stopovers/ arrive at the destination by a certain time. 
- **Action Cost** 
- A combination of:
  - monetary cost
  - Waiting time 
  - Flight time 
  - Customs
  - Immigration procedures 
  - Seat quality 
  - time of day 
  - Type of Airplane 
  - Weather 
- All of these will be used to compute the action cost .

## Different Probelms: 

## Touring Problems 

A Touring problem descibes a set of locations that must be visited, rather than a single goal destination. 

The traveling salesman probelm is an example of a touring problem.

## Traveling Salesman Problem (TSP)

Every city on a map myst be visted 
The aim is to find a tour with cost < C with c being a designated target cost. This could also be optimized with the lowest possible cost. 

## VLSI Layout Problem 

The VLSI layout problem requires positioning millions of compennents and connections on a chip to minimize area, minimize circuit delays, minimize stray capacitances, and maximize manufacturer yeilding. 

The layout problem comes after the logical design phase and is usually split into two parts: 

- Cell layout 
- Channel Routing 

### Cell Layout 

- Cell Layout the primitaive components of the ciruits are grouped into cells, each of which will provide some function. 
- Each cell will have a footprint or size/ shape.
- Each cell will require a fixed ammount of connections to other cells 
- The aim is to place the cells on the chip so they do not overlap and so there is enough room for the connecting wires.

### Channel Routing 

- This phase finds routing for each of the connection wires between each of the cells which have been laid out 

## Robot Navigation 

- Generalization of the route-finding problem described earlier. 

Rather than following distinct path, a robot can roam and forge it's own paths. 

For a circular robot moving on a flat surface the space is essentially 2D. 

When the robot has arms and legs that must be controlled more complexity is added as the problem becomes 3D/ Many dimensional. 

## Automatic Assembelly Sequencing 

Automatic assembely sequencing is the assembley of complex objects such as engines/ computers by a robot. 

Algorithms will find feasable solutions to assemble the object, then work to optimize the process. 

This minimizes manual human labour which will save times, and save production cost in the long term after funding these robots. 




