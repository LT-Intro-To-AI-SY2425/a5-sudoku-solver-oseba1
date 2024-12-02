# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. How do the performance and efficiency of the Depth-First Search (DFS) and Breadth-First Search (BFS) algorithms compare when solving Sudoku puzzles? In what scenarios might one approach be preferable over the other?

DFS has a higher variance in its effciency on solving the puzzles. Still the average result of DFS were better than BFS. I think because the nature of sudoku restricts a lot of the possible numbers it makes it faster for DFS rather than BFS. It might be beneficial to use DFS when the tree is very deep and not very wide. Likewise it might be better to use BFS if the node tree is wider rather than deeper.

2. How did the choice of data structures (like the Stack for DFS and Queue for BFS) impact the implementation and functionality of the algorithms? Are there alternative data structures or design patterns that could have been used to achieve the same objectives?

The choice of a stack for DFS and a queue for BFS is important in defining the behavior of the algorithms. A stack in DFS makes it so that the most recent decision is explored first which supports the algorithm's depth-first nature of going forward deeper into the search tree before backtracking. In contrast a queue used in BFS ensures that all nodes at the current level of the search are explored before moving on to deeper levels. Alternative data structures like priority queues or  deques could modify the search strategy for specific problem types.

3. Considering the current implementation, how might the Sudoku solver be adapted or extended for larger puzzles or different types of grid-based logic games? How can the lessons learned from this assignment be applied to real-world problem-solving or optimization challenges?

To solve bigger Sudoku puzzles you can use the same basic approach, but you might need to make some changes to handle the extra size or difficulty. Using things like parallel processing could help speed up the process. The main ideas from solving Sudoku like using rules to narrow down choices cutting out bad options early and making decisions with incomplete information can be used for other real world problems too. Tasks like scheduling managing resources or AI for games all involve finding the best solution quickly. The methods used for Sudoku puzzles can be adapted to solve these types of problems as well.