# Turing Accept Problem

### Is the Acceptance of Any [[Turing Machine]] Decidable
- It is undecidable

***Proof: By contradiction***
Let A<sub>TM</sub> = { [[String Representation of TM|<M]],[[String Representation of TM|w>]] : M is a TM, w $\epsilon$ L(M) }

- Assumes there is a H that decides Let A<sub>TM</sub> 
- Pseudocode for H:
	- On input x:
		- if x not in correct format of <M,w>, reject.
		- if M accept, accepts
		- otherwise reject

- Now we have a theoretical machine H that can decide whether another TM accept an input, but we have to prove that H exist now.

- Build another decider D that does 2 things:
	1) Run H on <M,$<M>$>
	2) Output the opposite

- Now if we give <M> to D:
	1) D will accept if H reject
	2) D will reject if H accept
	
- This also mean that
	1) D will accept if M reject <M>
	2) D will reject if M accept <M>
	
- Everything is fine so far, now since D is the decider, D must correctly answer for all TMs, including itself.
- But when we give <D> to D we get:
	1) D will accept if D reject <D>
	2) D will reject if D accept <D>
	***The above are contradictions***
	
***Hence*** D cannot exist $=>$ H cannot exist which means Let A<sub>TM</sub> is not decidable
	
## Note:
- Because D has to be able to exist if H exist, since we proved that D is a contradiction and hence cannot exist if we want it to. H cannot exist.


# Turing Halting Problem

### Is the Halting of Any [[Turing Machine]] Decidable
- It is undecidable

***Proof: By contradiction***
Let Halt<sub>TM</sub> = { [[String Representation of TM|<M]],[[String Representation of TM|w>]] : M is a TM, M halts when run on w }
- Let H be another TM (taken from  Turing Accept Problem)
- Let the machine below be Z
- On input x:
	- if x is not in correct <M,w> form, reject
	- if H accept x, accept
	- else reject

- Since H also halt on all input, the above machine also halt. From [[Turing Accept Problem]], we know that there exist cannot exist a D for Z since if we do decide to create a D, it is impossible due to contradiction. Hence Z cannot exist
	
	
# Turing Emptiness Problem
E<sub>TM</sub> = { <M> | M is a TM and L(M) = $\emptyset$ }
The Problem of knowing if the Language of A Turing Machine is empty is **undecideable**

We can use the A<sub>TM</sub> to help prove this question is undecidable

What if we have a TM M'
- M' Language is the language of M (which is $\emptyset$) and some string w

Then M' would work like this
On input x:
1) if x is w, accept
2) if x is not w, reject
	
This is exactly the hypothetical decider for A<sub>TM</sub>
	
Now the decider for E<sub>TM</sub> would look like this:
On input x:
1) if M' accept, reject
2) otherwise, accept
	
**Ofcourse we know that A<sub>TM</sub> does not exist, hence  E<sub>TM</sub> cannot also exist. **

	
# Turing Equivalence Problem
EQ<sub>TM</sub> = { <M1,M2> | M1, M2 are TMs and L(M1) = L(M2) }
The equivalence of 2 Turing Machines is **undecidable**

This problem of EQ<sub>TM</sub> is reducible from E<sub>TM</sub>
	
Proof Approach:
- To Prove that EQ<sub>TM</sub> is undecidable, we reduce E<sub>TM</sub> to this problem
- Assume that R = Decider for EQ<sub>TM</sub>
- Assume that S = Decider for E<sub>TM</sub>

S will decide whether L(M) = $\emptyset$

This is how R is going work:
On input <M>:
1) Construct a TM M<sub>$\emptyset$</sub> which rejects all input
2) Run S on <<M,>,<M<sub>$\emptyset$</sub>>>
3) if S accepts, accept; if it rejects, reject.