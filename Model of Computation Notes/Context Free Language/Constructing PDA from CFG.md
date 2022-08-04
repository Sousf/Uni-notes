# Converting PDA from [[Context Free Grammar|CFG]]
If we have this [[Context Free Grammar|CFG]]:
S--> aBc | ab
B--> SB | $\epsilon$

Construct a [[Pushdown Automata|PDA]] for this grammar

***Solution***
The way we construct the PDA for this ***or any*** [[Context Free Grammar|CFG]] is to do the following steps
1) Every PDA that we construct from a [[Context Free Grammar|CFG]] will have 4 main "base states" below
- ![[Pasted image 20211103195633.png]]
- The first transition we push a $ to signify the end of the stack
- The second transition we push S (Starting variable) into the stack
- The last transition we check if $ is ontop of the stack, if yes we can go to the accept state

2) The **q_loop** state is where the variations are at.
- For each terminal in this grammar, we create a self loop at **q_loop**, saying if we see this terminal at the top of the stack, pop it from the stack. (This is shown in the above picture ontop of q_loop)
3) For each of the variable inside the [[Context Free Grammar|CFG]], there will be a loop that goes from **q_loop** and back to **q_loop**, shown below
- ![[Pasted image 20211103200517.png]]
- The very left loop is for aBc in the first rule of S. Since its a stack we push everything from right to left. First we say
	- If there is an S ontop of the stack, pop it and push c
	- Then push B
	- Then push "a" and this takes us back to state **q_loop**
- The next loop (in the middle) is for the 'b' inside the first rule S
- Similarly the third one is for the variable B
- and last one for variable $\epsilon$


**Follow this algorithm to construct any PDA from [[Context Free Grammar|CFG]]**
