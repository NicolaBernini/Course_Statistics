


# Bayesian Inference 

Bayesian Inference is essentially about solving an Inverse Problem which means inferring the state of something not directly observable using something directly observable which is connected to the former via some causal link 

One of the main concept related to the Bayesian Framework is that the act of observing is not the only way to acquire information about something 

In fact Bayesian Framework consists of 2 periods 

- The term **prior** indicates something related to the period **before** the observation 
- The term **posterior** indicates something related to the period **after** the observation 


The way information propagates from prior to posterior is regulated by the famous Bayes Formula 



## Basic 

Let's introduce from Bayesian Formula 

$$ P(H | O) = \frac{P(O | H) P(H)}{P(O)} $$

with 

- $H$ = Hypothesis 
- $O$ = Observation 
- $P(O|H)$ = Probability of an Observation given an Hypothesis 
- $P(H|O)$ = Probability of an Hypothesis given an Observation 


Here is an easy explanation of basic elements 

### Hypothesis 

Indicated by $H$

A term indicating something belonging to a Latent Space which can't be directly observed but which is connected by a cause-effect relationship to the Observable Soace 


### Observations 

Indicated by $O$

A term indicating something belonging to a directly Observable Space 


### Prior 

Indicated by $P(H)$

It represents prior knowledge about the latent element or hypothesis 



### Posterior 

Indicated by $P(H|O)$

It represents knowledge about the hypothesis after the observation or more precisely how the observation changed the prior 



### Likelihood 

Indicated by $P(O|H)$

It represents a sort of compatibility measure between a certain $H$ latent state and a certain $O$ observed state 



#### Notes 

- In order to be able to solve Bayesian Inference it is required to model Likelihood which typically means having a causal model linking the latent space to the observation space 
- Note this is expressed by the Likelihood Notation, as it expresses how **likely** is a certain observation **given** a certain hypothesis 
- Stated differently, that notations assumes a certain $H=h$ is true and with respect to this it associates a **likelyhood score** (which is NOT a probability) to a certain $O=o$ observation 
- Stated differently again, if we see $P(O=o|H=h)$ as a functions $f(x;\theta)$ then 
  - the $o \in \mathcal{D}$ is the function variable or input belonging to the $\mathcal{D}$ function domain and 
  - the $\theta \in \Theta$ is the function parameter belonging to the $\Theta$ function parameters space 
- Using an analogy with a Neural Network, which is in fact a function approximator, the $o=x \in \mathcal{D}$ (let's change the notation slightly for clarity sake) is the Network Input which because of the Network Inference process will lead to an associated $y \in \mathcal{C}$ Network Output in the Codmain while $\theta \in \Theta$ are the Network Parameters 









