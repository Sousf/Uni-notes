### Overview
- A feature engineering/dimensionality reduction technique
- Creates new features from existing features.
- Work by taking the different linear combinations of all the features within the dataset


### How it works
- Lets say we want to compute 3 new features, called p1, p2 and p3
- We will compute them as follow
	- p1 = $a_1v_1 + a_2v_2 + ... + a_nv_n$
	- p2 = $b_1v_1 + b_2v_2 + ... + b_nv_n$
	- p3 = $c_1v_1 + c_2v_2 + ... + c_nv_n$
- Here $v_n$ are the original features, and we can see that p1, p2, p3 are just linear combinations of all original features.
- We will have to compute $a_n, b_n, c_n$ such that they maximises the variance of the new feature and that each feature is orthogonal to the previous feature, p2 is orthogonal to p1, p3 is orthogonal to p2.




