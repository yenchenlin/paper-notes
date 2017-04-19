## [Model-Agnostic Meta-Learning for Fast Adaptation of Deep Networks](https://arxiv.org/abs/1703.03400)

The authors propose an algorithm for meta-learning that is compatible with any model trained with gradient descent, and show that it works on various domain including supervised learning and reinforcement learning. This is done by explicitly train the network such that a small number of gradient steps with a small amount of training data from a new task will produce good generalization performance on that task.

### Key Points

- MAML is actually finding a good **initialization** of model parameters for several tasks.
- Good initialization of parameters means that it can achieve good performance on several tasks with small number of gradient steps.

### Method
- Simultaneously optimize the **initialization** of model parameters of different meta-training tasks, hoping that it can quickly adapt to new meta-testing tasks.

![](https://cloud.githubusercontent.com/assets/7057863/25161911/46f2721e-24f1-11e7-9fba-8bc2f0782204.png)

- Training procedure:

![](https://cloud.githubusercontent.com/assets/7057863/25161749/8d00902a-24f0-11e7-93a8-6a9b74386f55.png)



### Exp

- It acheived performance that is comparable to the state-of-the-art on classification/regression/reinforcement learning tasks.

### Thought
I think the experiments are thorough since they proved that this technique can be applied to both supervised and reinforcement learning. However, the method is not novel provided that [Optimization a A Midel For Few-shot Learning](https://openreview.net/pdf?id=rJY0-Kcll) already proposed to learn initialization of parameters.
