## [Model-Agnostic Meta-Learning for Fast Adaptation of Deep Networks](https://arxiv.org/abs/1703.03400)

The authors propose an algorithm for meta-learning that is compatible with any model trained with gradient descent, and show that it works on various domain including supervised learning and reinforcement learning. This is done by explicitly train the network such that a small number of gradient steps with a small amount of training data from a new task will produce good generalization performance on that task.

### Key Points

- MAML is actually finding a good *initialization* of model parameters for several tasks.
- Good initialization of parameters means that it can achieve good performance on several tasks with small number of gradient steps.

### Model
- .


### Exp

- 

### Thought
I think the method is useful and the experiments are thorough. However, the method is not novel provided that Ravi & Hugo et al. already propose to learn parameters initialization.

### Questions
