---
title: Bayesian Inference and Computational Complexity 
tags: bayesian inference 
---

# Bayesian Inference and Computational Complexity 

Bayesian Inference is associated with computational complexity because of the need to compute integrals on a state space 

Typical examples includes 

1. Normalization 

It is the necessary step to transform Likelihood in Posterior in fact 

$$ P(X | Y) = \frac{P(Y | X)P(X)}{P(Y)} $$

which is equivalent to 

$$ P(X | Y) = \frac{ P(Y | X) P(X) }{ \int_{\mathcal{X}} P(Y | X) dP(X) } $$

and the denominator integral, leading to the normalization constant, scales $O(N)$ with $\mathcal{X}$ dimensionality 



2. Marginalization 

The Marginalization consists of integrating over a full subspace in the PDF Domain so to obtain a new PDF / Scalar 

For example let's decompose the $\mathcal{X}$ PDF Domain so that $\mathcal{X} = \mathcal{X'} \cup \mathcal{Z}$ so the marginalization over $\mathcal{Z}$ is defined as 

$$ P(X') = \int_{\mathcal{Z}} P(X',Z) dP(Z) $$

Also this integral is $O(N)$ with $\mathcal{Z}$ dimensionality 





3. Estimation 

Given a certain $P(X)$ Probability Space or $P(X|Y)$ Conditional Probability Space, computing an estimation for a certain function $f(x)$ over the state space means computing the following integral 

$$ E_{[P(X|Y)]}(f(x)) = \int_{\mathcal{X}} f(x)dP(X|Y) = \int_{\mathcal{X}} f(x)P(X|Y)dx $$

which again scales $O(N)$ with the $\mathcal{X}$ dimensionality 

