## [Practical Black-Box Attacks against Deep Learning Systems using Adversarial Examples](https://arxiv.org/abs/1602.02697)


### Key Points
- This paper attacks against black-box DNN classifiers without knowledge of the classifier training data or model.
- The black-box attack evades defenses proposed in the literature because the substitute trained by the adversary is unaffected by defenses deployed on
the targeted oracle model to reduce its vulnerability

### Method
Since adversarial examples transfer between architectures, we can 

1. Substitute Model Training: learn a substitute DNN approximating the target using a dataset constructed with synthetic inputs and labels observed from the oracle
2. Adversarial Sample Crafting: craft adversarial example using the substitute trained by first step

Generally, the goal of the adversary is to produce a **minimally** altered, i.e., imperceptible, version of input which will be misclassifyed by target model.

### Exp


### Thought


### Questions
