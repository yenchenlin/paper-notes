## [World Models](https://arxiv.org/abs/1803.10122)

The author proposed a model-based method to learn policy. Specifically, the system consists of three components:

1. Encoder (V)
2. Future predictor (M)
3. Controller (C)

<img src="https://user-images.githubusercontent.com/7057863/44424238-81e77400-a556-11e8-88b1-7bab14386569.png" width="400px"/)

The author shows that it's possible to train a controller in a simulated environment.

### Key Points

- By keeping model capacity of V and M large, we can learn a compact feature space (i.e., dimension 32) for C and thus being able to apply ES to get good policy.



### Method

1. Randomly collect trajectories in the environment.
2. Train a VAE for every states.
3. Use the encoder of VAE, V, to encode the states z = V(s). Then, train a predictive model, P(z_t+1 | z_t, h_t, a_t).
4. Use ES to evolve a controller which takes [z_t h_t] as input and outputs an action a_t.

If we want to train the agent to entirely in **dream**, we can use the predictive model as a simulator and 


### Exp

The author performs the experiments in two domains:

- Racing Car
- Vizdoom

In Racing Car, the author shows that World Models achieve state of the art performance against RL methods such as PPO.

In Vizdoom, the authore went one step further to train an agent entirely in its **dream** and then apply the controller back to real world environment. It turns out it can score even higher score in real environments compared to imperfect simulated environment by M.

### Thought

I think the paper is well-presented and shows lots of cool findings. However, it's obvious that unsupervised learning of V and M cannot learn really compact features for the downstream specific task that C is addressing since there is no reward. If we can backprop the reward signal back to both V and M then this issue is solved but then the problem is not simplified compared to deep learning anyway.

### Questions

- Why we can't use RL for C?
