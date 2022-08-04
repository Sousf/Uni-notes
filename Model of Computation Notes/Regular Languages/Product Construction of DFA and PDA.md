---
aliases: [Product DFA]
---

# Steps to Perform Product Construction of 2 [[DFA]]
- Construct a [[DFA]] for $L_1$ and $L_2$ using the produce construction
1) Make a [[DFA]] for $L_1$ and $L_2$
	- ![[Pasted image 20211104120900.png]]
	- The Product [[DFA]] $L_1$ and $L_2$ will be have num of states in $L_1$ x num of states in $L_2$, in this case 2 x 3 = 6

2) Construct all states that is going to be in the product [[DFA]]
	- ![[Pasted image 20211104121328.png]]
	- Each state in Product DFA is a pair of states from $L_1$ and $L_2$
3) Construct the links between the states
	- We pick a state from the Product DFA, in this case $q_0r_0$, we see that on input 1, $q_0$ goes to $q_1$, and $r_0$ goes to $r_1$. Hence   $q_0r_0$ goes to  $q_1r_1$. We repeat this kind of logic for all the states in the Product DFA to obtain the graph below:
	- ![[Pasted image 20211104122354.png]]



# Product Construction Can Be Used To Construct Union and Intersection [[DFA]]
- Let $L_1$ and $L_2$ Be 2 languages with there own DFA.
- The Product DFA of these 2 languages can be used to construct the **Union** and **Intersection** DFA.
1) Constructing Union DFA from Product DFA
	- To do this, simply make any states in the Product DFA that contains 1 accept state from **either** DFA<sub>1</sub> or  DFA<sub>2<sub>
2) Constructing Intersection DFA from Product DFA
	- To do this, simply make any states in the Product DFA that contains 1 accept state from **both** DFA<sub>1</sub> and  DFA<sub>2<sub>
	
	
	
# Product Construction between a PDA and a DFA
- Can be used to Prove that CFL $\cap$ Regular Language is also a CFL
