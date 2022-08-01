# Wumpus World 

We explore the ability of logical agents through a wumpus world 

- It is a cave consisting of rooms connected via passageways 
- Somewhere inside is a wumpus (monster) that will eat anyone who enters it's room 
- Room contain bottomless pits that will trap anyone who falls in 
  - Except the wumpus as it is too large 
- The agent can kill the wumpus 
  - But the agent is armed with only one array 
- The reason for being there is that there is a pot of gold for someone to find 

## Preformance Measure

- +1000 for climbing out of the cave with gold 
- -1000 for falling into a pit 
- -1000 for being eaten by the wumpus 
- -1 for each action taken 
- -1- for using the arrow 

The gam ends when the agent dies or climbs out of the cave. 

## Environment 

- 4X4 grid of rooms with walls surrounding the grid 
- Agent always starts in square with coordinates [1, 1]
  - The agent is always facing to the east 
- The locations of the gold are random 
- The location of the wumpus is random 
- The wumpus and the gold have uniform distribution from squares other than the start square 
- Each square other than the start can be a pit 
  - the probbability is 0.2 

## Actuators 

- The agent can move: 
  - Forward 
  - Turn left 90deg 
  - Turn right 90deg 
- The agent dies if it enters a square containing the wumpus 
- The agent dies if it enters a square with a pit 
- The agent will be blocked from moving if the direction it is moving is into a wall 
- Actions 
  - Grab: used to pick up gold 
  - Shoot: To fire an arrow in the direction it is facing 
    - The arrow continues until it either: 
      - Hits a wall
      - Kills the wumpus 
  - Climb used to climb out of the cave 
    - Only can be used from the start position [1, 1]

## Sensors 

- The agent has 5 sensors: 
  - Squares directly (not diagonally) from the wumpus will percieve stench 
  - The squares adjacent to a pit will percieve breeze 
  - A square when the gold is will percieve glitter 
  - Walking into a wall will percieve bumb 
  - If a wumpus is killed a scream will be emmited which can be percieved anywhere in the cave. 

The percepts will be given to the agent program in the form of five symbols;

For example if there is a:
  - Stench
  - Breeze 
  - But no glitter, bump, or scream 

Program will get these percepts: 

[Stench, Breeze, None, None, None]

## Enviroment Characteristics 

- Deterministic 
- Discrete 
- Static 
- Single Agent 
- Sequential 
  - Because rewards will come only after many actions are taken 
- Partially observable 
  - Some aspects of the state are not directly perceivable 
    - The agents location, 
    - Wumpus state of health
    - Arrow availability 
- Unobserved state: 
  - Wumpus location 
  - Pit Locations 

Transition model could be known or unknown 
  - The agent doesn't know which actions are fatal (unknown)
  - Finding the locations of pits completes the agent's knowledge of the state (known)

"Note that in each case for which the agent draws a conclusion from the available information, that conclusion is guaranteed to be correct if the available information is correct."