# 🧩 Maze Solver

![Maze Solving Animation](https://d18l82el6cdm1i.cloudfront.net/uploads/mf7THWHAbL-mazegif.gif)

## 📖 Overview

This project implements a maze solver using a depth-first search (DFS) algorithm. It takes a maze represented as a text file and finds a path from the start point (A) to the goal point (B).

## 🔑 Key Features

- Solves mazes using DFS algorithm
- Supports custom maze inputs
- Visualizes the solution path
- Generates PNG output of solved mazes

## 🧱 Maze Format

Mazes are represented in text files using the following symbols:

| Symbol | Meaning |
|--------|---------|
| `A`    | Start   |
| `B`    | Goal    |
| `#`    | Wall    |
| ` `    | Path    |

Example:
```
#####B#
##### #
####  #
#### ##
     ##
A######
```

## 🚀 Usage

Run the solver with:

```bash
python maze.py maze.txt
```

Replace `maze.txt` with your maze file path.

## 📊 Example Runs

### Maze 1

<details>
<summary>Click to expand</summary>

#### Console Output
![Console Output of maze1](https://raw.githubusercontent.com/nawaz0x1/AI-Lab/refs/heads/main/Search%20Algorithms/screenshots/maze_1_run.png)

#### Solution Visualization
![Visual Output of maze1](https://raw.githubusercontent.com/nawaz0x1/AI-Lab/refs/heads/main/Search%20Algorithms/screenshots/maze_1_solve.png)

#### Original Maze
```
#####B#
##### #
####  #
#### ##
     ##
A######
```
</details>

### Maze 2

<details>
<summary>Click to expand</summary>

#### Console Output
![Console Output of maze2](https://raw.githubusercontent.com/nawaz0x1/AI-Lab/refs/heads/main/Search%20Algorithms/screenshots/maze_2_run.png)

#### Solution Visualization
![Visual Output of maze2](https://raw.githubusercontent.com/nawaz0x1/AI-Lab/refs/heads/main/Search%20Algorithms/screenshots/maze_2_solve.png)

#### Original Maze
```
###                 #########
#   ###################   # #
# ####                # # # #
# ################### # # # #
#                     # # # #
##################### # # # #
#   ##                # # # #
# # ## ### ## ######### # # #
# #    #   ##B#         # # #
# # ## ################ # # #
### ##             #### # # #
### ############## ## # # # #
###             ##    # # # #
###### ######## ####### # # #
###### ####             #   #
A      ######################
```
</details>

## 🛠 Implementation Details

The project consists of a single Python file `maze.py` with the following key components:

1. `Node` class: Represents a state in the maze.
2. `StackFrontier` class: Implements a stack for DFS.
3. `QueueFrontier` class: Available for BFS (unused in current implementation).
4. `Maze` class: Handles maze parsing, solving, and visualization.

## 🧮 Solving Algorithm (DFS)

1. Initialize frontier with start position
2. While frontier is not empty:
   - Remove a node from frontier
   - If node is goal, solution found
   - Mark node as explored
   - Add unexplored neighbors to frontier
3. If frontier empties, no solution exists

## 🖼 Output

The program generates:
1. Text representation of the maze and solution
2. Number of explored states
3. PNG image (`maze.png`) showing:
   - 🔴 Start point
   - 🟢 Goal point
   - 🟡 Solution path
   - 🟠 Explored states
   - ⚪ Unexplored paths
   - ⚫ Walls

## 📋 Requirements

- Python 3.x
- Pillow library

## 💻 Installation

1. Install Python 3.x
2. Install required library:
   ```bash
   pip install -r requirements.txt
   ```

