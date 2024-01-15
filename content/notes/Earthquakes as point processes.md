---
tags: seismology, statistics
---
[[statistical seismology]]

Firstly, earthquake sequences are [point processes](https://en.wikipedia.org/wiki/Point_process).
# Gaussian process
Gaussian distribution or normal distribution
$$f(x) = \frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{1}{2}(\frac{x-\mu}{\sigma})^2}$$
- $\mu$ is the mean and $\sigma$ is the standard deviation
- The moment of a probability density function

## the central limit theorem
Under some not-too-strict mathematical conditions, the theorem states that the average of a large number of random variables tends to follow a Gaussian distribution

It is bad practice to estimate qualities of a population using individuals or very small samples.

# Bayes theorem
- How often A happens given that B happens?
$$P(A|B) = \frac{P(B\cap A)}{P(B)} =\frac{P(B|A)P(A)}{P(B)}$$

# Markov chain and Markov process
- Hidden Markov Model
  A  [statistical](https://en.wikipedia.org/wiki/Statistical_model)   [Markov model](https://en.wikipedia.org/wiki/Markov_model)  in which the system being modeled is assumed to be a  [Markov process](https://en.wikipedia.org/wiki/Markov_process)  with unobservable (i.e. *hidden*) states.
- [Particle filter]() or “sequential Monte Carlo” is used to solve HMM problems.

- Renewal process
    * This make sense if earthquake repeats on the same segment according to elastic rebound and never interact or break into other segments.
    * The point process analog of Markov Chains.

[Fractal dimension](https://en.wikipedia.org/wiki/Fractal_dimension)

[Weibull distribution](https://en.wikipedia.org/wiki/Weibull_distribution)

# Declustering
- @Mizrahi2021

## Statistical terms
- Independent and identically distributed : iid

---
See also [[ETAS]]