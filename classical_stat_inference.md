# Towards more general estimators

Let's start with a small example:

- Suppose we have a jar of 1000 jelly beans. We take out 20 and we want to estimate
the number of pink jelly beans in the jar. 

- To estimate $\theta$ we can try to do this: $\frac{X}{n}* 1000$ where X = the number
of beans in theta that were pink

# How to get any kind of estimator

- Wouldn't it be powerful if we could come up with a way to derive any estimator?

- **maximum likelihood estimation (MLE)** is a methodolgy to derive any estimator using the following question: "What is the value of $\theta$ that maximizes the likelihood of seeing X = x"

Algorithm: 

1. Define $\hat\theta_{ml} (X = x) = \text{argmax}_{theta} \mathbb{P} \{X = x | \theta\}

2. Convert x into X$

Let us use an example to illustrate this:

For the jelly bean example: suppose initially 3 jelly beans are shown from the batch of 20. Let's find the MLE for this. 

$\mathbb{P} \{X = 3 | \theta\} = {20 \choose3} \cdot (\frac{\theta}{1000})^3 \cdot (1 - \frac{\theta}{1000})^{17}$