# UQ
	This model is used to examine how different Bayesian neural network perform on a toy dataset. <br/>
  Two models are compared for now: Bayes By Backprop and Laplace Approximation. Data we simulated is a gaussian process with lengthscale 0.1. <br/>
  Gaussian process is chosen due to its closed form predictive probability and lengthscale is chosen because this made the function more curved and thus not so trivial to converge. <br/>
  I found that BNN doesn't converge well, by examining the individual hidden unit weights and compare it to a regular NN that converge well to our data, I found that while both model have weights mean 0 and variance 1, the regular NN contains several hidden units that have particularly big weights like 8.0, which is statistically impossible for the BNN. Thus the next step is to examine how ensemble method with different priors work on this dataset.
