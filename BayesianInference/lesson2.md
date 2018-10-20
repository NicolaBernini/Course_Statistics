---
title: Bayesian Inference and Computational Complexity 
tags: bayesian inference 
---

# Bayesian Inference and Computational Complexity 

Bayesian Inference is associated with computational complexity because of the need to compute integrals on a state space 

From a computational point of view, implementing an integral on a certain space means iterating over all the elements of that space, so $\int_{\mathcal{X}} f(\cdot) dx$ gets implemented (in Pseudo-CPP) as 


```cpp
for(int i=0; i<X.size(); ++i) f(X[i]); 
```
with 
- the $\mathcal{X}$ implemented as `vector<T> X` 
  - NOTE: the `vector<>` has been used as container because in order to compute the integral we only the need the space to be iterable 
- the $f(\cdot)$ implemented as `f()` and containing the element-specific logic 
- the $dx$ implemented as `T x[i]` element 


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



