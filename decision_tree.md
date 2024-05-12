# Decision tree

- Decision trees classify instances by sorting them down the tree from the root to leaves
- Each node consists of a decision where each branch coming out of them is an answer to said decision
- Suppose we have a dataset that has $n$ features. A decision is some criterion for $x_i \leq k$ for $i \in [1, n]$ and $\min(x_i) \le k \le \max(x_i)$
## Features
- A **Splitting Criterion** is a function that measures how good or useful splitting on a particular feature is for a specified dataset
- A general idea is make a greedy decision at each stage of the program - pick the best criteria.
- Let's first define a new entropy function
- For a set of values, we define a new entropy function 
## Entropy for Sets
- $H(S) = -\sum_{v \in V(s)} \frac{|S_v|}{|S|}\log_2\frac{|S_v|}{|S|}$
- $S_v$ is the set of values in S that are equal to v. $S$ is some set. 
- If all the elements are the same then, the entropy is 0.
- If it is half and half, the entropy is 1.
- We can use this to define mutual information
- $I(Y;X) = H(Y)- H(Y|X)$
- Generalized for sets: - $I(Y;x_d) = H(Y)- \sum _{v \in V(x_d)} (f_v)(H (Y_{x_d = v}))$
- Y is the labels, $V(X_d)$ is the unique values of $x_d$, $f_v$ is the fraction such that $x_d = v$, and $Y_{x_d = v}$ is the labels where $x_d = v$.
## Algorithm
- Pick the best criterion $x_d$. 
- For each value of $x_d$ recursively split the dataset. 
- Base case - If the set inputted is empty, all labels, or all features are the same
- Note that the best criterion is the one that maximizes the information gain.

## Pros and Cons
- We know which features we split on exactly
- Efficient cost wise for sure
- But it is greedy
- VERY liable to overfitting

