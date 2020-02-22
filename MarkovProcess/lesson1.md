

# Markov Models 

Let's consider a stochastic process $S_{t}$ : a time indexed list of random variables related to some domain 

This may represent a time-evolving system which evolves according to some non deterministic dynamic 

Let's now approach the problem of defining a **model** for such a system 

An interesting class of models for this goal is the Markov Models class which indentifies a set of models relying on the **Markov Property Assumption** which consists of assuming the stochastic process is without memory so 

$$ P(S_{t+\Delta t} | {S_{\tau}}) = P(S_{t+\Delta t} | S_{t}) \quad \tau \in [1,t] $$

The following types of Markov Models exist 

![Markov Models](https://i.imgur.com/4c8LnGH.png)

*Courtesy of [Wikipedia](https://en.wikipedia.org/wiki/Markov_model)*



## Markov Chain 

The Markov Chain is the simplest type of Markov Model, consisting of the following Category (in the sense of [Category Theory](https://en.wikipedia.org/wiki/Category_theory)): 
- $\mathcal{S}$ : Objects Space or State Space which contains all the possible states for the system $S \in \mathcal{S}$
- $P(S_{t + \Delta t} | S_{t})$ : Stochastic Morphism Space defininig a probabilistic connction between 2 elements in the State Space 



# Hidden Markov Model 

The Hidden Markov Model introduces a decoupling between the State Space or Latent Space and Observation Space 

![HMM1](https://upload.wikimedia.org/wikipedia/commons/8/83/Hmm_temporal_bayesian_net.svg)



The HMM backbone is a Markov Chain defining an evolution in the Latent Space, but the latent - observable space decoupling, introduces 2 additional elements 
- $\mathcal{Z}$ : Observable Space so that $Z \in \mathcal{Z}$ 
- $P(Z|S)$ : Likelihood (according to Bayesian Framework terminology) which acts as Pseudo-Functor or Cross Category Mapping as it defines a probabilistic relationship between the Latent Space (belonging to State Category) and the Observable Space (belonging to Observation Category)

In order to estimate Latent State from Observations an **Inference** needs to be performed and the following types are possible 
- Filtering : $P(S_{t} | \{Z_{\tau}\}_{\tau = t_{0}:t})$ which is focused on estimating only the most recent state from the available knowledge 
- Smoothing : $P(\{S_{\tau}\}_{\tau = t_{0}:t} | \{Z_{\tau}\}_{\tau = t_{0}:t})$ which is focused on estimating the last states in the $[t_{0}, t]$ timeframe from the available knowledge 
- Prediction : $P(\{S_{_{\tau}}\}_{\tau = t:t_{1}} | \{Z_{\tau}\}_{\tau = t_{0}:t})$ which is focused on estimating the future states in the $[t, t_{1}]$ timeframe from the available knowledge 




To be continued 




