Maze Pathfinding using Iterative Deepening Depth-First Search (IDDFS)

## Problem Overview

This program implements the **Iterative Deepening Depth-First Search (IDDFS)** algorithm to determine whether a valid path exists from a start cell to a target cell in a 2D grid representing a maze. The grid consists of empty spaces (denoted by `0`) and walls (denoted by `1`). The objective is to explore the maze and find a path from the start to the target while respecting the movement constraints (up, down, left, right), avoiding walls, and ensuring each cell is visited only once during a single exploration.

## Features

- **Grid Representation**: The maze is represented as a 2D list of integers, where `0` indicates an open path and `1` indicates a wall.
- **IDDFS Algorithm**: The solution uses the IDDFS technique, which performs depth-limited DFS iteratively with increasing depth limits until the target is found or the maximum depth is reached.
- **Traversal Order**: The program outputs the order in which the cells were visited during the traversal.
- **Handling Multiple Test Cases**: The program handles multiple test cases and reports the result for each case.

## Usage

### Input Format:
The input consists of:
1. The grid dimensions (rows and columns).
2. The grid itself, where `0` represents an open space and `1` represents a wall.
3. The starting position of the maze.
4. The target position.

Example input:

#### Case 1:

4 4
0 0 1 0
1 0 1 0
0 0 0 0
1 1 0 1
Start: 0 0
Target: 2 3


#### Case 2:

3 3
0 1 0
0 1 0
0 1 0
Start: 0 0
Target: 2 2


### Output Format:
The output will indicate whether a valid path exists and, if found, will display the traversal order of visited cells. If the path is not found, the program will report that the path is not found within the given maximum depth.

#### Case 1 Output:

Path found at depth 5 using IDDFS
Traversal Order: [(0,0), (1,0), (1,1), (0,1), (2,1), (2,2), (2,3)]


#### Case 2 Output:

Path not found at max depth 6 using IDDFS


## Code Explanation

1. **Input Parsing**: The input is read and processed to extract the grid, start and target positions.
2. **IDDFS Algorithm**: A function `iddfs` is used to perform the Iterative Deepening Depth-First Search. It uses DFS with depth-limited search and increases the depth limit iteratively until the target is found or the maximum depth is reached.
3. **DFS Function**: A helper DFS function is implemented to explore the maze from the current position to its neighbors while keeping track of the visited nodes to avoid revisiting them.
4. **Traversal Output**: The cells visited during the traversal are printed in order.

## Requirements

- Python 3.x
- No external libraries are required.

## How to Run

1. Clone the repository:
  
    git clone https://github.com/yourusername/iddfs-maze-solver.git
   
2. Navigate to the project directory:
  
    cd iddfs-maze-solver
  
3. Run the Python script:
  
    python iddfs_maze_solver.py


## Example Run

For Case 1:

Input:
4 4
0 0 1 0
1 0 1 0
0 0 0 0
1 1 0 1
Start: 0 0
Target: 2 3

Output:
Path found at depth 5 using IDDFS
Traversal Order: [(0,0), (1,0), (1,1), (0,1), (2,1), (2,2), (2,3)]


For Case 2:

Input:
3 3
0 1 0
0 1 0
0 1 0
Start: 0 0
Target: 2 2

Output:
Path not found at max depth 6 using IDDFS
