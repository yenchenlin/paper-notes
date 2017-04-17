## [InforGAN: Interpretable Representation Learning by Information Maximizing Generative Adversarial Nets]()

### Preliminaries
Mutual information `I(X;Y)`, measures the **amount of information** learned from knowledge of random variable Y about the other random variable X. 

It can be expressed as the difference of two entropies terms:
```
I(X;Y) = H(X) - H(X|Y) = H(Y) - H(Y|X)
```

### Problem

Normal GANs use a simple factored continuous input noise vector z, while imposing no restrictions on the manner in which the generator may use this noise. As a result, it is possible that the noise will be used by the generator in a highly entangled way, causing the individual dimensions of z to not correspond to semantic features of the data.

### Key Points



### Model


### Exp


### Thought

### Questions
- What does it mean by "even though it is easy to construct perfect generative models with arbitrarily bad representations"?

### References 
http://www.inference.vc/infogan-variational-bound-on-mutual-information-twice
