#UninformSearch
## Overview

- Uses a Queue Data Structure

## Example Steps

**What it looks like for our agent:**
- Say we want to go from a certain city in romania to another, the agent can use Breadth First Search to find a path towards a destination. Here's a different visual:

- **We start at the starting city, and traverse until the destination is reached, in which case we back track to the root of the tree to get the full route**

![[Pasted image 20220309160934.png]]

![[Pasted image 20220309160940.png]]

![[Pasted image 20220309160953.png]]

![[Pasted image 20220309161001.png]]

## Time Complexity: O($b^d$)
- where b is number of branch per level, and d is depth
- This is basically because we are exploring all nodes of the tree at every level. In a tree with *b* branches and *d* depth, there would be $b^d$ number of nodes to explore.

## Space Complexity: O($b^d$)
- This is because we keep every node in memory, and there are $b^d$ number of nodes.

## Optimal:
- Yes when cost at each step are all uniform.
- Doesn't take cost into account so will not be optimal if cost for different paths are different.
	- **So its technically not optimal in general**

## Completeness: Complete






Example Implementation:
![[Pasted image 20220318165627.png]]

