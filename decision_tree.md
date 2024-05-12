## Trees

- Decision trees classify instances by sorting them down the tree from the root to leaves
- Each node consists of a decision where each branch coming out of them is an answer to said decision
- Suppose we have a dataset that has $n$ features. A decision is some criterion for $x_i \leq k$ for $i \in [1, n]$ and $\min(x_i) \le k \le \max(x_i)$
- A **Splitting Criterion** is a function that measures how good or useful splitting on a particular feature is for a specified dataset
- A general idea is make a greedy decision at each stage of the program - pick the best criteria.
- Let's first define a new entropy function
- For some set of values: we define a new entropy function $H(S) = -\sum_{v \in V(s)} \frac{|S_v|}{|S|}\log_2\frac{|S_v|}{|S|}$
- $S_v$ is the set of values in S that are equal to v $S$ is some set. 
- If all the elements are the same then, the entropy is 0.
- If it is half and half, the entropy is 1.
