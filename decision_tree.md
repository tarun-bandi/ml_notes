## Trees

- Decision trees classify instances by sorting them down the tree from the root to leaves
- Each node consists of a decision where each branch coming out of them is an answer to said decision
- Suppose we have a dataset that has $n$ features. A decision is some criterion for $x_i \leq k$ for $i \in [1, n]$ and $\min(x_i) \le k \le \max(x_i)$
- A **Splitting Criterion** is a function that measures how good or useful splitting on a particular feature is for a specified dataset
- A general idea is make a greedy decision at each stage of the program - pick the best criteria.