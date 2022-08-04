## Overview
- A set of problems whose states must satisfy a number of constraints and limitations.
- Example include the famous **Map Colouring** problem
- More formally: 
	- A **state** is defined by a set of **variables** $V_i$ with values and **domain** $D_i$
	- The **constraints** are enforced by what we call **goal test**



## Example:
## Map Colouring
**![[Pasted image 20220419143622.png]]
## Cryptarithmetic
*![[Pasted image 20220419143533.png]]

## Solving Strategies for CSP
- **Backtracking** - Explore a branch of the tree until a solution or a dead end is found. If a dead end is found, backtrack back to the previous node and search a different branch. Basically what [[Depth-first Search]] does. 
	- This strategy can solve n-queens problem when n = 25![[Pasted image 20220430102227.png]]

## Optimisations and Heuristic strategies for solving CSP
- **Minimum Remaining Values Heuristic (MVR)** - Choose sucessor with fewest legal values. Select successor states that are more likely to result in failure (end as dead leaves of recursion tree)
- **Degree Heuristics** - Choose successor involved in the largest number of constraints on other potential successors. More constraints -> lower branching factor of recusion subtree.
- **Least constraining value Heuristic (prefers flexibility for the future)** - Given a variable, assign the value that makes the fewest choices of variables for neighbouring candidates illegal. This permits the maximum remaining flexibility for remaining variables, making it more likely to find a complete solution in future.Least constraining value  
	- Illustration ![[Pasted image 20220430110904.png]]
- **Minimum Conflicts Heuristic** (Very Good Heuristic) - Dictate how we pick value to assign by picking a value for some variable that produces the minimum number of conflicts.
	- ![[Pasted image 20220430103835.png]]
	- For example with the n-queens problem:
	- We can check for conflicts for each cell on the board (only vertical in this case): ![[Pasted image 20220430104543.png]]
	- We pick the smallest conflicting square, and we also check conflict cells for the next queen![[Pasted image 20220430104706.png]]
	- Go to the 0 conflict cell 
	- ![[Pasted image 20220430104855.png]]
	
- **AC-3 (Check for constraint consistency)** - Not a solving algorithm, but makes the problem alot easier to be solved for other solving strategies. **AC-3** will attempt to put the problem into a **arc-consistent state**. The **AC-3** algorithm enumerates all possible arcs in a queue Q and makes $X_i$ arc-consistent w.r.t $X_j$ by reducing the domains of variables accordingly.
	- Video walkthrough of algorithm: https://youtu.be/4cCS8rrYT14
	- ![[Pasted image 20220430112933.png]]
	- **Time Complexity of AC-3** to get a CSP tree into a consistent state:
		- $O(nD^2)$ where **$D$** is the domain size and n is the number of pairs connected in the graph. This is because you potentially can compare every possible value of each node to each other nodes, for every n pairs. 
- **Forward-Checking Strategy** - update a table of valid values for each variables at each assignment
	- Initial table before any assignment is made (From Map Colouring Problem)![[Pasted image 20220430103035.png]]
	- If we assign **red** to WA, the table will update with the new possible values each other variables can take on. ![[Pasted image 20220430103138.png]]
	- Suppose we choose to assign **green** to Q next, now we have: ![[Pasted image 20220430103255.png]]
	- Now we assign **blue** to V, we have ![[Pasted image 20220430103406.png]]
	- Notice here how **Forward-Checking** found a dead end, where SA cannot take on any values. Under **Backtracking Strategy**,  the algorithm will back track to find a better solution here.

![[Pasted image 20220430105203.png]]

## Real World CSPs
- Assignment Problems - who teaches what class
- Timetabling problems
- Hardware Configuration
- Spreadsheets
- Transportation Scheduling
- **A current example:**
	- Recomputing the flight routes for airplanes to go around Russia due to the Russia-Ukraine war
	- ![[Pasted image 20220419143808.png]]