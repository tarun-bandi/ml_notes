## Introduction

Maximum a Posteriori(MAP) estimators are estimators that make use of some a priori information.

Just like ML estimators, they aim to estimate some parameter $\theta$, however, they start with a distribution $\Theta$ on the possible values of $\theta$

## Example

You are given a coin which either has probability 0.4 or 0.6 of being heads. 

You flip the coin 9 times, and based on that make a decision:

$\mathbb{P}\{X = x | p = 0.6\} = {9 \choose x} (0.4)^x (0.6)^{9 - x}$

$\mathbb{P}\{X = x | p = 0.4\} = {9 \choose x} (0.6)^x (0.4)^{9 - x}$

Based on the value of x, we pick the one that is larger.

## Formal definition

**MAP** - $\hat{P}_{\text{map}}(X) = \underset{\theta}{\text{argmax  }} \mathbb{P}\{\Theta = \theta | X = x\}$  

Where $\Theta$ is some distribution on the possible values from $\theta$

We can further specify the definition. 

When $\Theta$ is a discrete RV: 

$\hat{\Theta}_{\text{map}}(X =x) = \begin{cases}
\underset{\theta}{\text{argmax  }} \mathbb{P}\{ X = x | \Theta = \theta\} \cdot \mathbb{P}\{\Theta = \theta\} & \text{X is discrete }
\\
f_{ X = x | \Theta = \theta}(x) \cdot \mathbb{P}\{\Theta = \theta\} 
\end{cases}$

If $\Theta$ is continuous it is analgous