I implemented an algorithm to solve the **n×n puzzle** using the **A\*** algorithm, which is highly effective in finding optimal solutions due to its combination of informed search and accumulated cost. The puzzle consists of a grid of variable size (e.g., 3x3, 4x4) with numbered tiles and a blank space, where the goal is to rearrange the tiles into numerical order by moving the blank.

### Design Choices:
1. **Grid Representation**: I used a **list of lists** to represent the puzzle state, making it easy to manipulate tiles and generate new configurations during the search process.

2. **Heuristic**: I employed the **Manhattan distance** as the heuristic function. It's admissible and consistent, ensuring that it never overestimates the minimum moves required to reach the goal, thus guaranteeing that A\* finds the optimal solution.

3. **Tracking States**: To efficiently track visited states and reconstruct the solution path, I convert the grid into a **hashable string**. This approach optimizes both memory usage and lookup speed compared to nested tuples.

The code is designed to handle grids of any size `n×n` , but as `n` increases, the computational time grows exponentially. It performs well for sizes up to `3x3`, but larger grids significantly increase the solution time due to the combinatorial complexity.
