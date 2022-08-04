# Defintion
- Closure of a relation is the smallest relation with a particular property that contains the original

### Transitive Closure
Let X = {a,b,c,d}, and R = { (a,b), (b,c), (c,d) }

To Close R under transitivity, we need to have the original set in the new set, and new elements to satisfy the property of [[Properties of Relations#Transitive]]:
- Let R<sup>2</sup> = {(a,c), (b,d)} (By transitivity (a,b), (b,c) --> (a,c)...etc.)
- The new set that is R closed under **transitivity** is:
	- R $\cup$ R<sup>2</sup> =  { a,b), (b,c), (c,d), (a,c), (b,d) }


### Symmetric Closure
Let X = {a,b,c,d}, and R = { (a,c), (c,a), (c,b), (d,a), (d,d) }

To Close R under symmetry, we need to have the original set in the new set, and new elements to satisfy the property of [[Properties of Relations#Symmetric]]:
- Let R<sup>-1</sup> = { (c,a), (a,c), (b,c), (a,d), (d,d) }
- The new set that is R closed under *symmetry* is:
	- R $\cup$ R<sup>-1</sup> =  { (a,c), (c,a), (c,b), (d,a), (d,d), (c,a), (a,c), (b,c), (a,d), (d,d)  }

### Reflexive Closure
Let X = {a,b,c,d}, and R = { (a,c), (c,a), (c,b), (d,a), (d,d) }

To Close R under reflexiveness, we need to have the original set in the new set, and new elements to satisfy the property of [[Properties of Relations#Reflexive]]:
- Let $\Delta$ = { (a,a), (b,b), (c,c), (d,d) } 
- The new set that is R closed under **reflexiveness** is:
	- R $\cup$ $\Delta$ = { (a,c), (c,a), (c,b), (d,a), (d,d), (a,a), (b,b), (c,c), (d,d) }


### Symmetric Transitive Closure
- A **symmetric transitive** closure is a set that is closed under both [[Closures on a relation#Symmetric Closure]] and [[Closures on a relation#Transitive Closure]].



### Preservation of Closure Properties
![[Pasted image 20211105110153.png]]