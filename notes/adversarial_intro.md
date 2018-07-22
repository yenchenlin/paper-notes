## [A Brief Introduction to Adversarial Examples](http://people.csail.mit.edu/madry/lab/blog/adversarial/2018/07/06/adversarial_intro/)

The authors briefly introduce the definitoin of adversarial examples and **why it's really a thing**.

### Key Points

- Beyond security, studying adversarial examples can provide us insight on a) robustness of ML-based system, b) difference between ML-based system and human esp. when lots of papers are claiming surpassing-human performance these days.
- Adversarial examples are beyond image classification. They also appear in other important applications such as speech recognition, question answering system, ... etc.

### Method
- Simultaneously optimize the **initialization** of model parameters of different meta-training tasks, hoping that it can quickly adapt to new meta-testing tasks.

![](https://cloud.githubusercontent.com/assets/7057863/25161911/46f2721e-24f1-11e7-9fba-8bc2f0782204.png)

- Training procedure:

![](https://cloud.githubusercontent.com/assets/7057863/25161749/8d00902a-24f0-11e7-93a8-6a9b74386f55.png)



### Exp

- It acheived performance that is comparable to the state-of-the-art on classification/regression/reinforcement learning tasks.

### Thought
I think the experiments are thorough since they proved that this technique can be applied to both supervised and reinforcement learning. However, the method is not novel provided that [Optimization a A Midel For Few-shot Learning](https://openreview.net/pdf?id=rJY0-Kcll) already proposed to learn initialization of parameters.
