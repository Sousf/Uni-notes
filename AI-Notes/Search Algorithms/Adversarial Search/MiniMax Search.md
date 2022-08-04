#AdversarialSearch

## Overview

- The MiniMax Search strategy is an adversarial search strategy whereby at a certain state, would try and maximise their own utility function in the game. Since we assume opponent is rational, they will try and pick moves that will minimise our utility, in this case it becomes a strategy where we try to maximise the minimal possible option the opponent can pick for us.
- Recursively compute the minimax value (the maximum minimum value that the opponent chose) for each state



![[Pasted image 20220324134903.png]]

## Pseudo Code:
- The MINIMAX-DECISION function returns the action that correspond with the minimax value, that is the maximal of the lowest scoring moves the opponent will choose for us.
- The MAX-VALUE function returns the minimax value of the given state
- The MIN-VALUE function returns the minimal value that the opponent can choose for us.

![[Pasted image 20220324135536.png]]

Another easier to understand version:
![[Pasted image 20220324140347.png]]



## Time Complexity: O($b^m$)
-  where b is number of branch per level, and m is maximum depth
- Terrible if the deepest path length $m$ is much bigger than the shallowest depth $d$
- Since MiniMax might explore the longest path. Worst case is to be exploring $b$ different branches on $m$ levels. which is $b^m$ number of nodes.
- Same Complexity as [[Depth-first Search]]

## Space Complexity: O($bm$)
- Same Space Complexity as [[Depth-first Search]], Since we only explore one long running branch at a time.

## Optimal:
- Yes, against an optimal opponent (rational).


## Completeness: 
- Yes, it is Complete only if tree is finite

## Minimax with Cutoff and Evaluation function instead of Utility function:
- We can have a cutoff test inside Minimax search where there is a depth limit to our search tree
- Evaluation function is different for different settings.
	- In Chess, typically evaluation function is a linear weighted sum of features
	- $Eval(s) = w_{1}f_{1}(s) + w_{2}f_{2}(s) + ... + w_{n}f_{n}(s)$ 


## Optimization:
- [[Alpha-Beta Pruning]] (Reduces **Time Complexity** to **$O(b^{m/2}))$** - Attempts to calculate the correct minimax decision without looking at every node of the game search tree. This is because there are many branches that could potentially be ignored (pruned). Two values are created during the search
	- **Alpha-value**: Associated with MAX nodes
	- **Beta-value**: Associated with MIN nodes

## Definition of Optimal Odering
- Basically for max level, the first node has the biggest value, for min level, the first node is the smallest.
- This is good for alpha beta pruning, as we can maximise the number of node prune. 



Example of minimax from Week 5 tute Q1:
![[Pasted image 20220401165219.png]]