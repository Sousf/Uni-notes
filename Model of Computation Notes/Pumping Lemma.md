# Pumping Lemma for [[Regular Languages]]

For any [[Language]] A, 
A is *Regular* => $\exists$p $\geqslant$ 1, $\forall$ $s \epsilon A$ 
1) Length of $s \geqslant p$
2) $s = xyz$
3) $y$ is not empty
4) length $|xy| \leqslant p$
5) $x$$y^i$$z$ $\epsilon$ A $\forall i$


### Example of Pumping Lemma proving a [[Language]] is not Regular
*Prove the [[Language]] A = {$0^i1^j$ | 0 $\leqslant$ i $<$ j} is not a Regular [[Language]]*

1) Let the pumping length p $\leqslant$ 1.
2) Let $s = xyz$, where $x,y,z$ $\epsilon$ $\Sigma*$
3) Let $y$ not be empty
4) Let $|xy| \leqslant p$
5) Since $|xy| \leqslant p$, xy consists entirely of 0s.
6) By the Pumping Lemma, $x$$y^i$$z$ $\epsilon$ A $\forall i$ must exist, however, as we pump the value of $i$ up, the string no longer is recognised by A, hence Property 5 of the Pumping Lemma fails and A is not a Regular [[Language]]




# Pumping Lemma for [[Context Free Language]]
For any [[Language]] A, A is *Context Free* => $\exists$p $\geqslant$ 1, $\forall$ $s \epsilon A$ 
1) Length of $s \geqslant p$
2) $s = uvxyz$
3) $vy$ is not empty
4) length $|vxy| \leqslant p$
5) $u$$v^i$$x$$y^i$$z$ $\epsilon$ A $\forall i$


### Example of Pumping Lemma proving a [[Language]] is not Context Free

*Prove that A = { $a^ib^ja^ib^j$ | i $\geqslant$ 0 $\wedge$ j $\geqslant$ 0 }*

1) Suppose that A is Context Free, by the pumping lemma, there is some pumping length p $\geqslant$ 1
2) Let $s$ = $a^pb^pa^pb^p$, then $s$ $\epsilon$ A
3) |$s$| $\geqslant$ p
4) By the pumping lemma, there exist $uvxyz$ such that $s = uvxyz$, $|vxy| \leqslant p$, $vy$ is not empty, $u$$v^i$$x$$y^i$$z$ $\epsilon$ A $\forall i$
5) Since $|vxy| \leqslant p$, $vxy$ consist entirely of either $a$ or $b$ or $a$ and $b$
6) If we pump the value of i up to any other value, we can observe that in **all** cases of $vxy$, s will no longer belong to the set A. 
7) Hence A does not respect Pumping Lemma and hence A is not Context Free.