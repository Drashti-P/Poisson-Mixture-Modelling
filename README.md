# Poisson-Mixture-Modelling
Poisson Mixture Modelling to uncover hidden Limit Order Executions

A Limit Order instructs a broker to buy or sell stocks, shares, or bonds at a specified price. The flow of limit orders can be modelled using a Poisson process, a probability distribution for counting events in a set timeframe . The arrival of different types of limit orders—such as submissions, executions, or deletions—introduces heterogeneity, posing a clustering problem.

A Poisson mixture model addresses this heterogeneity by combining Poisson distributions, each representing a different rate. While the distinct Poisson rates are visible in each cluster of the Poisson Mixture Model plot, the hidden variable is the weighting of each data point to a particular cluster. For example, in a two-cluster Poisson Mixture Model, we cannot directly observe the probability of a point arising from one of the clusters. This hidden weighting, the latent variable, along with the Poisson rates, can be approximated using the Expectation-Maximization (EM) algorithm, an iterative optimization algorithm that alternates between estimating the weighting and maximizing the likelihood to determine the model parameters.

I implemented the Expectation-Maximization Algorithm to build a Two-Cluster Poisson Mixture Model for the flow of visible and hidden limit order executions. Using inter-arrival times of Google Stock from the LOBSTER dataset, the Poisson rates were determined to be λ₁ = 21 and λ₂ = 6, respectively.
