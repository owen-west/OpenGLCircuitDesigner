# CP411 Project: OpenGL Circuit Designer

Author: Owen West

Date: 2024-11-23


## Introduction

This project will be focused on creatingan interactive tool for designing and visualizing basic logic circuits using OpenGL. The tool will allow users to place, connect, and simulate gates like AND, OR, and NOT, within a 2D grid interface. Combining computer graphics and computational logic, this tool aims to provide users with an environment for exploring digital circuit design.

The main goal is to help users visualize the flow of logic through their created circuits and understand how gates interact. The tool simulates the values that flow through the circuit while ensuring a responsive and visually appealing user experience. Another goal is to lay the foundation for expanding this project in the future to support more complex circuits.
 
## Problem solving and algorithms

The major problem with this project is designing a system where users can intuitively draw circuits, place gates, and connect them in a logical manner, all while maintaining real-time logical accuracy.

The algorithm will contain a few key parts:
- Logic evaluation will be crucial to ensure this tool can support any combination of gates. Using proper data structures and search algorithms will be important. BFS can be used to evaluate all logic values at each step through the circuit.
- Grid snap interaction will be crucial to ensure all circuits are aligned on the world grid. There are a few ways to handle this, such as clicking within a predetermined radius of a corner to place a wire, or the center of a grid square for a gate. Keeping track of mouse movements will make this possible.
- Rendering the gates and wires will likely be one of the more simpler tasks of this project. I will just need to keep track of the coordinates of each item, such as a wire and gate, and then use OpenGL to display all objects in 2D.
- Collision detection will be important to ensure wires and gates do not overlap, as that can cause confusion and a poor user experience. A simple algorithm to ensure coordinates are not occupied will need to be implemented.


## Design consideration 

1. System Design
There will be 3 main components for the system.
One will be the logic engine. This will keep track of all connections within the circuit, as well as handling the computational logic whenever changes are made to the circuit.
Another component will be the rendering system. This will handle our window and it's components such as rendering the grid, gates, wires, and input/output systems.
The final component will be the input component. This will capture and process all user input, and mapping these actions to whatever actions are available such as drawing, placing, and selecting.

2. Architecture
For the MVC, we have:
Model will represent the logical state of the circuit, gates, wires, input/outputs.
View will display the circuits and grid using OpenGL, and handling visual feedback for the user.
Controller will manage user input and update the Model or View accordingly.


## Milestones & schedule
| Task ID | Description   |  Due date |  
| :----:  | :------------ | :-----:   |
|  1      | Project research | Day 7 of week 10 | 
|  2      | Project proposal | Day 7 of week 10 |
|  3      | Project check point  | Day 3 of week 11 |
|  4      | Project check point  | Day 7 of Week 11  |
|  5      | Project demonstration | Day 3 of week 12 |
|  6      | Project submission | Day 3 of week 12 |



## References

- CP411 Lecture Notes
- https://learnopengl.com/