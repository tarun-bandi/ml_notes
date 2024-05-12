## Information theory

- To transmit one bit is to reduce uncertainty by a factor of 2
- Suppose the weather has 8 states. When you find the weather out, you reduce uncertainty by a factor of 8.
- Uncertainty reduction is generally $\frac{1}{\mathbb{P}{[A]}}$
- $\log(\frac{1}{x}) = -\log(x)$
- Can use the above equation to get the uncertainty reduction when you find out an event with probability x is happening

#Entropy

- $H(p) = -\sum_{i} p_i \log_2 (p_i)$ 
- Entropy is the expected value of the information you get from a sample of a probability distribution
- It can be intuited as the unpredictability of the distribution/random variable

#Cross Entropy
- It is the average message length 
- Assuming each message has a uniform length $u$, the average message length will be $u$.
- However, if the cross entropy is below $u$, we can do better.
- Assume we create some unambigious code (Useful encoding - no messages are proper prefixes of other messages)
- The cross entropy is the expected value of the message lengths in bits
- $H(p, q) = -\sum_{i} p_i \log_2 (q_i)$ 
- p is the true distribution and q is the predicted distribution

#KL Divergence 
- $D_{KL} (p || q) = H(p, q) - H(p)$
- However much extra information is being sent out by the predicted prob distribution

#Cross Entropy for ML

- Suppose we have some supervised learning problem that outputs a distribution of classes (MNIST)
- For some one hot encoding (one class has probability 100%) the cross entropy is: $-\log(q_i)$ for an object of class $i$.