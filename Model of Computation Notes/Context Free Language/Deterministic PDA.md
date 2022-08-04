- A PDA is called *deterministic* iff from any configuration, there is at most one transition you can take.
- This means that a *determinstic* PDA will never find itself in a position where it can make two different transition steps.
- More formally:
	- |$\delta(q,v,a)$| + |$\delta(q,\epsilon,a)$| + |$\delta(q,v,\epsilon)$| + |$\delta(q,\epsilon,\epsilon)$| $\leqslant$ 1

- ![[Pasted image 20211102160637.png]]