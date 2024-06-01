# Estimators 

## Introduction

- Statistics is generally taken such that we measure some data and then try to use 
inference to predict a property of the distribution underlying the data 

- We write $\hat{\theta}(X_1, X_2, ..., X_n)$ to indicate an $\textbf{estimator}$ of some unknown $\theta$.


## Sample mean

- **Sample Mean** is an estimator of $\mathbb{E}[X]$. 

    -  $M_n = \bar{X} = \frac{X_1 + X_2 + X_3 + ... + X_n}{n}$ 

- To rank the strength of the estimator, we can use biases. The bias $\textbf{B}(\hat\theta) = \mathbb{E}[\hat\theta] - \theta$
    - Objectively, we'd like our bias to be as close to zero as possible
- We can also use mean squared error to measure the spread of the estimator:
    - $\textbf{MSE} = \mathbb{E}[(\hat\theta - \theta)^2]$

- The final property is that we would like our estimators to become more accurate as the number of samples approach infinity, we wnat this property to hold: $\text{lim}_{n\to\infty} \mathbb{P} \{|\hat\theta_n - \theta| \ge \epsilon \} = 0 $
    - The estimators that do so are denoted as consistent


## Variance 

- There are two distinct cases to estimate variance.
    1. Mean is unknown
    2. Mean is known

- When the mean is known the estimator is:
$\frac{1}{n}\sum _{i = 1}^{n}(X_i - \mu)^2$

- If the mean is unknown this is slightly more tricky to handle

- We can try to replace $\mu$ with $\bar X$: 
    $\frac{1}{n}\sum _{i = 1}^{n}(X_i - \bar X)^2$
- However, we run into a slight issue here: the expected value is $\frac{n - 1}{n} \text{\textbf{Var}}(x)$.
- The solution is quite simple: multiply by $\frac{n}{n - 1}$.
- Now the estimator is $\frac{1}{n - 1}\sum _{i = 1}^{n}(X_i - \bar X)^2$