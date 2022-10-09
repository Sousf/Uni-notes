### Overview
- MCMC is a very widely-used technique for simulating samples from the posterior distribution.
- The basic idea is to simulate a Markov chain, whose stationary distribution is the posterior distribution. By simulating the Markov chain for long enough, one obtains samples that are “approximately” from the posterior distribution.

### Why MCMC?
- For an average [[Rejection Method]], each individual random instance sampled is indepedent from one another. This in essence can be very inefficient as the algorithm can be sampling many "rubbish instances" that are not part of the true distribution $f(x)$.
- By leveraging Markov-Chains, MCMC algorithms create new instances that are dependent on one another. The MCMC algorithm will calculate the probability of the newest sampled point and compare it to the probability of the previous, and pick the one with the highest probability. This works well as in cases where MCMC sampled a point near a peak , it will know to stay there and sample for awhile, rather than randomly generating new coordinates without regards for the probability.


### Example MCMC Algorithms
- [[Gibbs Sampling]]
- [[Metropolis–Hastings Algorithm]]


