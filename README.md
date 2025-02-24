# Maze Solver (Using DFS and BFS search Algorithms)

This project is a maze solver that uses Breadth-First Search (BFS) and Depth-First Search (DFS) algorithms to find a path from the start point `A` to the goal point `B` in a given maze.

## Files

- `maze.py`: The main Python script that contains the implementation of the maze solver.
- `maze.txt`: A text file representing the maze layout.

## Requirements

- Python 3.x
- Pillow library for image generation(optional you can also see solution in terminal)

You can install the Pillow library using pip:

```sh
pip install pillow
```
## Usage
To run the maze solver, use the following command:
```sh 
python maze.py maze.txt
```

The script will prompt you to select a search algorithm:

- BFS (Breadth-First Search)
- DFS (Depth-First Search)

Enter your choice (1 or 2) and the script will solve the maze, print the solution, and generate an image maze.png showing the solution path.

## Classes:  
  
## Node
### Represents a node in the search tree.

#### state: 
The current state (position) of the node.
#### parent: 
The parent node.
#### action: 
The action taken to reach this node.
#### StackFrontier
Implements a stack-based frontier for DFS.

#### add(node): 
Adds a node to the frontier.
#### contains_state(state): 
Checks if the frontier contains a given state.
#### empty(): 
Checks if the frontier is empty.
#### remove(): 
Removes and returns the last node from the frontier.

## QueueFrontier
Inherits from StackFrontier and implements a queue-based frontier for BFS.

#### remove(): 
Removes and returns the first node from the frontier.

## Maze
Represents the maze and contains methods to solve it.

### __init__(filename): Initializes the maze from a file.
#### print(): 
Prints the maze with the solution path.
#### neighbors(state): 
Returns the neighboring states of a given state.
#### solve(): 
Solves the maze using the selected search algorithm.
#### output_image(filename, show_solution=True, show_explored=True): 
Generates an image of the maze with the solution path.

## License
This project is licensed under the MIT License.