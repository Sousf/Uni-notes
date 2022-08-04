#UninformSearch
## Overview
* Expand deepest unexpanded node, basically traverse one path until the end is reach and traverse the next path.
* Uses a stack, LIFO


## Example Steps:

1. ![[Pasted image 20220310121220.png]]
2. ![[Pasted image 20220310121230.png]]
3. ![[Pasted image 20220310121237.png]]
4. ![[Pasted image 20220310121255.png]]


## Time Complexity: O($b^m$)
- where b is number of branch per level, and m is maximum depth
- Terrible if the deepest path length $m$ is much bigger than the shallowest depth $d$
- Since Depth First explores the longest paths first. Worst case is to be exploring $b$ different branches on $m$ levels. which is $b^m$ number of nodes.
## Space Complexity: O($bm$)
- Linear in space!
- This is because Depth First Search could traverse the longest path of the tree, which will have $b$ branches on $m$ levels, resulting in $bm$ space for this path. If a solution is not found, the memory can be cleared up to the next path that is going to be explored, which will require less memory than the longest running path, $bm$

## Optimal:
- Not Optimal. Depth First Search can get stuck to one long path that could eventually find a solution, but it might not be the optimal (fastest) solution available

## Completeness: 
- In spaces with infinite depth, Depth First Search can fail to halt and find the optimal solution. **Hence not complete in infinite space**
- **Depth First Search is complete in finite spaces.**





![[Pasted image 20220318165819.png]]