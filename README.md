# 15-Puzzle-AI-Based-Game

## Solver Algorithms

**UCS**
--------------
Uniform cost search is the general version of breadth-first search where only the cost of each node is considered with the heuristic function h(n) evaluating to 0 at every node. For the 15 Puzzle game, since each operation takes an atomic step, the weight of every edge in the game tree is always 1. In this case, uniform cost search simply equals breadth-first search. In our program, in order to make all algorithms as general as possible, we implemented uniform cost search simply.

**Iterative deepening DFS**
-------------------------------
The iterative deepening algorithm has the advantage to combine the time complexity of DFS and the minimal property of the solution. It uses a DFS algorithm with a limited depth search. The limit is incremented until a solution is found.

**A***
---------------
The A* algorithm has given the best results so far. The heuristic used is the sum of each Manhattan distance between a tile's position to the position it should be. The heuristic is admissible and therefore, provides the shortest sequence of actions.


**Bonus**
------------

# h3 Heuristic
---------------
We proposed a new h3 heuristic. Unlike Manhattan distance heuristic, h3 first considers all
possible diagonal movements and remaining vertical/horizontal movements later. This
function provides a higher value estimated cost which still does not exceed the real cost.
While this heuristic is still not better than h2 in few random generated inputs in different
depths, we observed it is better than the h1 and h2 overall. Especially in larger depth
solutions.
