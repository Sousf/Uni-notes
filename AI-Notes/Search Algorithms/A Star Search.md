#InformSearch #HeuristicSearch

## Overview

- Popular informed search algorithm
- It evaluates nodes by combining $g(n)$, the cost to reach the node, and $h(n)$, the cost to get from the node to the goal. The full evaluation function is $f(n) = g(n) + h(n)$
- The algorithm is identical to [[Uniform-cost search]] except that A∗ uses $g + h$ instead of $g$


## Example:

![[Pasted image 20220316175432.png]]

- An Example of A* Search starting from the city of Arad and is looking for the shortest path to Bucharest. Nodes are labelled with $f = g + h$.


## Time Complexity: 
- Exponential in (relative error in $h$ x length of solution)
## Space Complexity: O($bm$)
- Keep all nodes in memory

## Optimal: 
- Yes, but only if the graph is locally finite.

## Completeness: 
- https://cs.stanford.edu/people/eroberts/courses/soco/projects/2003-04/intelligent-search/astar.html
- Yes, but only if the graph is locally finite, the heuristic is [[Admissible]] and [[Monotonic]]. 
- How does [[Monotonic]] affect A*'s search Completeness?
	- Because A* is monotonic, the path cost increases as the node gets further from the root. **Contours can be drawn to show areas where the estimated path cost, the f(n), for the nodes inside the areas are lower than or equal to the path cost for the outer bounds of the contours**. These contours can be drawn as larger and larger areas that increase outwards as the f(n) for the outer bound of these contours increases. The first solution found is optimal since it is the first band where the f(n) for the contour is equal to the path cost for the goal. All the contours outside of this solution will have a higher f cost.
	- ![[Pasted image 20220325153840.png]]


**A* search is complete and optimal, but is prohibitive in memory.**

![[Pasted image 20220325170304.png]]
