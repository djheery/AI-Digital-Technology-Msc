# Example Problems 

The probelem solving approach ahs been applied to a vast array of task environments.

Below are some of the best known, distinguising between standadized and real world problems. 

## Standardized Problems 

A **Grid World** Problem is:

- two-dimensional
- rectangular array of square cells 
- agents can move from cell to cell known as traveral.
  - Horizontally
  - Vertically 
  - Sometimes Diagonally 
- Cells can conain objects 
  - These objects can be acted upon by the agent 
    - Picked up 
    - Pulled 
    - Pushed 
    - Etc. 
  - There could be a wall or a blocker in a cell which would mean that this cell is impassable for the agent and would prevent the agent from moving to that cell 

Sokaban could be an example of a grid world probem: 

- The game operates on a two dimensional grid or square cells 
- An agent can move hoizontally or vertically 
- Some cells contain boxes and can be moved to a goal position
- Some cells contain walls which are impassable and boxes cannot be pushed onto them 
- The goal state is of such that all the boxes must be on one of the goal positions 
- Each action will cost 1, with the optimal solution being the least amounts of moves taken to move every box to a goal position. 
- Transaction model returns the state occured by a previous action, such as incrementing the move count by one, and dictating the new positions of the agent and maybe a box moved by the agent. 

A World has 

n: non-obstacle cells 
b: boxes 

this means there are 

n * n! / (b!(n - b)!) states 

For example on an 8*8 grid there would be 200 trillion states. 

! states apply all of the numbers down to 1 from the current number in algebra. This means factorial. 

https://www.mathsisfun.com/numbers/factorial.html: This is a good site for explaining factorial. 


for example: 

8 * 8! means: 

8 * 8 * 7 * 6 * 5 * 4 * 3 * 2 * 1 

which means the above calculation would be : 

8 * (8 * 7 * 6 * 5 * 4 * 3 * 2 * 1) /
  ((5 * 4 * 3 * 2 * 1) * ((8 - 5) * 3 * 2 * 1))