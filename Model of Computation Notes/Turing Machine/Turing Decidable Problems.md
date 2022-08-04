# Acceptance of DFA and NFA

Let A<sub>DFA</sub> = { [[String Representation of TM|<M]],[[String Representation of TM|w>]] : M is a DFA and w $\epsilon$ L(M) }

We can show A<sub>DFA</sub> is decidable if a Turing Machine M can simulate the DFA of the string A<sub>DFA</sub>
![[Pasted image 20211103154203.png]]
The above is a representation of [[String Representation of TM|<M]],[[String Representation of TM|w>]]

Let H be a new machine that decides the ***Acceptance of DFA***
On input [[String Representation of TM|<M]],[[String Representation of TM|w>]]
1) H checks the first 5 components of DFA, if not valid, rejects.
2) H simulates the moves of M, keeping track of states and current position by writing after $ (at the end) 
3) When the last symbol in w is process, check if M is in a state in F, reject otherwise.

**Similarly A<sub>NFA</sub> is also decidable by converting NFA to DFA**


# Acceptance of CFG

Let A<sub>CFG</sub> = { [[String Representation of TM|<M]],[[String Representation of TM|w>]] : M is a CFG and w $\epsilon$ L(M) }

High level overview:
1) Convert The CFG to ***Chomky's Normal Form***
2) For all grammars in Chomky's Form, if a string w can be derived, then its derivation takes 2|w| - 1 steps
3) So to decide Let A<sub>CFG</sub>, we can simply try all derivation of that length, in finite time and see if one generates w.


# Emptiness of DFA
### Is it decidable that a DFA will recognise nothing?

Let E<sub>DFA</sub> = { <D,>: D is a DFA}

A representation of <D,> can be
![[Pasted image 20211103155939.png]]

On input <D,>
1) Go to transition part and remove all non reachable states
2) If there are no accept states left, accept otherwise reject.

***This is finite since both steps are finite, step 1 will end once all non reachable states are gone, or if there are no reachable states. Step 2 is a simple check that runs over all accept states once.***


# Emptiness of CFG
To test whether a CFG can generate a string, we can test for a simpler problem, see if any variables within CFG can generate a string.

The idea of the algorithm is to basically mark all terminals symbols in the ***rules*** of G. Then after that loop through each variable within the rules, and mark any variables that has its RHS all marked.

On input <G,> where G is a CFG:
1) Mark all terminal symbols of G
2) Repeat until no new variable get marked:
	- Mark any variable A where G has a rule A --> abc...def... and each symbol abc...def... has already been marked

3) If the start symbol of G is not marked, accept; otherwise reject.

***Note:***
If the start symbol of G is not marked, then G can't produce any strings, and L(G) = $\emptyset$



# Acceptance of CFL
For a CFL A and string w, does w belong to A? is there a CFG G such that w $\epsilon$ L(G)?

We can convert any CFG A into Chomky's Normal Form and produces all derivations of length 2|w| - 1, then we check if w is among the derived strings.