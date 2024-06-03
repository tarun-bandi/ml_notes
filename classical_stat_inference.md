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

1. Define $\hat\theta_{ml} (X = x) = \text{argmax}_{\theta} \mathbb{P} \{X = x | \theta\}$

2. Convert x into X$

Let us use an example to illustrate this:

For the jelly bean example: suppose initially 3 jelly beans are shown from the batch of 20. Let's find the MLE for this. 

$\mathbb{P} \{X = 3 | \theta\} = {20 \choose3} \cdot (\frac{\theta}{1000})^3 \cdot (1 - \frac{\theta}{1000})^{17}$

The theta that maximizes this is 150.

Let's do this with a generic example

$\mathbb{P} \{X = x | \theta\} = {n \choose x} \cdot (\frac{\theta}{1000})^x \cdot (1 - \frac{\theta}{1000})^{(n - x)}$

We can take the derivative of this function with respect to theta, which will give us $\frac{1000x}{n}$ as the value that maximizes the likelihood

## Log likelihood

- Rather than maximizing the likelihood function, sometimes we can maximize the log of the likelihood 

## Continuous

Define $\hat\theta_{ml} (X_1 = x_1) = \text{argmax}_{\theta} f _{X_1| \theta}(x_1)$

Let's take an example: students taking a class expect to spend a uniform amount of time on their homework.

More precisely, for some student let the random variable $X \sim U(0, b)$ denote the time that the student will spend on their homework.

Let's find what the parameter b is using MLE.

Say that we have three point samples.

We now must solve this expression:

$\underset{b}{\operatorname{argmax}} f_{X_1, X_2, X_3 | b}(x_1, x_2, x_3)$

$f_{X_1, X_2, X_3 | b}(x_1, x_2, x_3) = \begin{cases}
    \frac{1}{b^3},& \text{if } x_1, x_2, x_3 \leq b\\
    0,              & \text{otherwise}
\end{cases}$

Clearly, this wil reach the optimal value when $b = max(x_1, x_2, x_3)$

However, it is not unbiased!. It is left as an excercise to the reader to show that the expected value is not b.

## Mutliple parameters 

This can be accomplished by simply taking the partial derivatives.

Suppose we need to find the standard deviation and the mean of a Normal Distribution.

$g(\mu, \sigma) = f_{X_1, X_2, ..., X_n | \mu, \sigma}$


