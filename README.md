# Dijkstra’s in a Dungeon

## Project Overview
This project implements Dijkstra’s shortest path algorithm to solve a pathfinding problem within a maze. The program computes the path with minimal cost between two waypoints and extends the solution to find the cost to each reachable cell from an initial position. Additionally, a custom maze is created to test the implementation.

## Learning Objectives
- Revisit and apply Dijkstra’s shortest path algorithm.
- Practice dynamic graph construction.
- Utilize Python's high-level data structures such as lists and dictionaries.

## Features
1. **Adjacent Cells Calculation**:
   - The program calculates the adjacent cells for a given cell in the maze.
   - Supports movement in 8 directions (including diagonals).
   - Movement is restricted to open "spaces," with movement through "walls" disallowed.

2. **Dijkstra’s Shortest Path Algorithm**:
   - Returns the shortest path between a source and destination cell.
   - Stops once the destination is reached to avoid unnecessary exploration.
   - Handles cases where no path exists, returning appropriate responses (e.g., `None`).

3. **Cost Calculation to Reachable Cells**:
   - Modified Dijkstra's algorithm to compute the cost from an origin cell to all reachable cells.
   - Tested on a custom maze with varying costs for different grid cells.

## Maze Structure
The maze is defined in a text file with the following key:
- `X`: Impassable wall.
- `a, b, c, d, e`: Waypoints.
- `1, 2, 3`: Costs of moving through open spaces. Waypoints always have a cost of 1.

## Path Cost Computation
- Movement costs between cells are based on their respective costs and Euclidean distances for diagonal moves.
- Costs are higher for diagonal movement than horizontal or vertical movement.

## Support Functions
The provided `p1_support` module includes a `load_level` function, which loads the maze and returns a dictionary with:
- `walls`: Set of wall coordinates.
- `spaces`: Dictionary of open spaces with their corresponding costs.
- `waypoints`: Dictionary of waypoint names and coordinates.

## Example Level File (`example.txt`)
An example level file is provided for testing the algorithm. The file specifies walls, open spaces with movement costs, and waypoints.

## Project Files
1. **`path.py`**: The main Python file containing the Dijkstra’s algorithm implementation.
2. **`path_support.py`**: The helper Python file containing the Dijkstra’s algorithm implementation.
3. **`test_maze_path.txt`**: A text file showing the path between waypoints `a` and `d` in `test_maze.txt`.
4. **`my_maze.txt`**: A custom maze file created for testing. It contains at least four waypoints: `a`, `b`, `c`, and `d`.
5. **`my_maze_costs.csv`**: A CSV file containing the costs to all reachable cells from waypoint `a` in the custom maze.

## References
- [Dijkstra’s Algorithm](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm)
- [Python’s `heapq` module](https://docs.python.org/2/library/heapq.html)


