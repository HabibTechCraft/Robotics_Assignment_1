# Dynamic Wall Maze Solution Using VEX VR
This project aims to program a robot using the VEX VR environment to navigate through a maze, find the quickest escape route, map the maze, and return to its starting position. The robot is programmed in Python and implements various algorithms to achieve its tasks.

## Objectives
1) Maze Navigation: Move along the maze corridors without straying past the walls.
2) Maze Mapping: Create a representation of the maze while navigating through it.
3) Fastest Escape Route: Determine the quickest way out of the maze.
4) Return Home: Successfully navigate back to the starting position after escaping.

## Tasks Attempted
1) Maze Navigation:
The primary goal of maze navigation is to ensure the robot can move through the maze corridors without colliding with walls. To achieve this, the robot is equipped with eye sensors that detect obstacles ahead. The programming logic (Wall Following Algorithm) allows the robot to make real-time decisions based on sensor input. For example, if the front sensor detects a wall, the robot will turn left or right to navigate around it. This task involves implementing movement functions, such as move_forward, turn_left, and turn_right, which enable the robot to traverse the maze while keeping track of its movements.

2) Return Home Functionality:
This feature enables robot to return to its starting position after escaping the maze. The return_home function facilitates this by retracing the robot’s steps based on the recorded movements from the navigation phase. By interpreting the logged actions in reverse order, the robot can accurately backtrack to its starting point. This functionality ensures that the robot not only escapes the maze but can also navigate back safely, completing its mission.

4) Maze Mapping:
Maze mapping involves creating a representation of the maze as the robot navigates through it. The whole maze is divided into small cells (25mm) to get the coordinates of each cell for navigation. The BFS_MAP function utilizes a breadth-first search algorithm to systematically explore the maze. As the robot moves, it logs each cell it visits into a list, called visited_cells, which helps track the areas already explored. This mapping process is crucial for understanding the maze layout, allowing the robot to make informed navigation decisions and effectively plan its escape route.

5) Finding The Quickest Route:
After successfully mapping the maze, the next task is to determine the fastest escape route. The find_shortest_path function is responsible for this, utilizing pathfinding algorithms to evaluate the maze layout and identify the quickest route to the exit. By employing a queue to explore potential paths, the function records movements until it locates the end position. Once the optimal escape route is identified, the robot can follow the calculated path to exit the maze efficiently.

## Code Explanation
The code is structured into several key sections:

1) Configuration:
The robot’s setup using the VEX VR API, defining sensors (like distance and eye sensors) and motors.

2) Movement Functions: 
Functions to control the robot’s movement, including move_forward, turn_left, and turn_right, while logging its path.

3) Maze Escape Logic:
The Escape_maze function guides the robot through the maze by checking for walls and making turns.

4) Return Home Logic:
The return_home function allows the robot to backtrack to its starting position based on the recorded moves.

5) Maze Mapping:
The BFS_MAP function employs a breadth-first search algorithm to explore and log visited cells in the maze.

6) Finding the Shortest Path: The find_shortest_path function computes the quickest route from the starting position to the exit.

## Documentation

The code is documented with comments to explain each function’s purpose and logic. For detailed understanding, refer to the inline comments throughout the code.

## References:
Maze Exploration Algorithm for Small Mobile Platforms: https://www.researchgate.net/publication/315969093_Maze_Exploration_Algorithm_for_Small_Mobile_Platforms
VEX VR Documentation: https://api.vex.com/vr/home/playgrounds/dynamic_wall_maze.html
All You Need to Know About Breadth-First Search Algorithm: https://www.simplilearn.com/tutorials/data-structure-tutorial/bfs-algorithm
