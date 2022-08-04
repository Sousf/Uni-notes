#AdversarialSearch

## Overview:
- Remove nodes that do not need to be searched

## Example Steps:

The Min of the current branch is 3, so if we search other branches, we only care about ones with a minimum bigger than 3.
![[Pasted image 20220324144158.png]]

The Min here is 2 or less for this branch, hence we can skip the last 2 nodes since min is not bigger than 3
![[Pasted image 20220324144213.png]]

The min here is potentially 14 or smaller, so we keep searching
![[Pasted image 20220324144349.png]]

We found a new min for this branch which is 5. 5 is still bigger than 3 so we keep searching.
![[Pasted image 20220324144422.png]]

The final branch is 2, which is the new min for this sub branch. Since we had 3 as the min of the first sub branch, we traverse along the very right branch.
![[Pasted image 20220324144457.png]]



## Proof of  **$O(b^{m/2}))$ Time Complexity
