## [Graph Networks as Learnable Physics Engines for Inference and Control](https://arxiv.org/abs/1806.01242)

This paper introduced GN-based forward and inference models, and demonstrate their usage with MPC to solve control tasks.

### Key Points
- GN is an object-based representation of the physics system and hence leads to combinatorial generalization.
- Inference model can be used to perform "implicit" system identification, which in turn improves forward model's accuracy.

### Exp
- They demonstrate results on DeepMind control suite.

### Thought
- Object-based model-based RL looks promising.

### Questions

- How to solve forward model's compound error? (maybe a simple bi-directional solution may help)
