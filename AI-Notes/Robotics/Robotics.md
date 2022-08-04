## Key Terms
- Degree of Freedom: The number of configurations a robot might have
	- ![[Pasted image 20220601202139.png]]
- Non-holonomic robots: Robots that have more degrees of freedom than controls
	- Example: **Non-Holonomic Drive**
		- If the controllable degree of freedom is less than the total degrees of freedom, then it is known as non-Holonomic drive. A car has three degrees of freedom; i.e. its position in two axes and its orientation. However, there are only two controllable degrees of freedom which are acceleration (or braking) and turning angle of steering wheel. This makes it difficult for the driver to turn the car in any direction (unless the car skids or slides).


## Localization
- The technique that robots/hardware use to identify where they are in terms of their surroundings.
	- ![[Pasted image 20220601210543.png]]
	- ![[Pasted image 20220601210554.png]]
	- ![[Pasted image 20220601210609.png]]



![[Pasted image 20220601221610.png]]

![[Pasted image 20220601221634.png]]

- **Downside of cell decomposition**:  what to do with cells that is part obstacle?
	- The granularity might not be small enough and we could be blocked by cells that are part obstacle
	- Could lose out on important details due to granularity not small enough, can be solved by a recursive approach that is represented by an octomap.

## Skeletonization
- ![[Pasted image 20220601211814.png]]
- **Down side of skeletonization equidistance**: Not optimal since we could be taking a longer path as the path has to be in the middle
- **Potentially expensive in computation**
- ![[Pasted image 20220601211822.png]]