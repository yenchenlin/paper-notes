## [Make It Happen](http://www.argmin.net/2018/01/29/taxonomy/)

The author motivates why RL is harder and more important than supervised and unsupervised learning. However, I don't fully agree with these arguments, see **My Two Cents** section at the bottom for my justification.

### Key Points

- Here is an approximated taxonomy of ML:

<img src="https://user-images.githubusercontent.com/7057863/43361654-58b1aed6-9307-11e8-8431-692880d1940d.png" alt="drawing" width="400px"/>

- Coincidentally, it turns out the field of Data Science also has terminology for this trichotomy:
  - **Descriptive Analytics**: summarizing data to make it more interpretable, similar to **Unsupervised Learning**.
  - **Predictive Analytics**: estimating outcomes from current data, similar to **Supervised Learning**.
  - **Prescriptive Analytics**: guiding actions to achieve the goal, similar to **Reinforcement Learning**.

<img src="https://user-images.githubusercontent.com/7057863/43361653-579f3e50-9307-11e8-944f-d62ca11c92b1.png" alt="drawing" width="400px"/>

- According to the figurer above, the author claims that:

  1. Unsupervised Searning is by far the easiest of the three types of ML problems because the stakes are low. There is no wrong answer for summarization.
  2. Supervised Learning is more challenging as we can evaluate accuracy in a principled manner on new data.
  3. RL is the hardest as it needs to deal with evolving environment and complicated feedback resulting from interaction.
  
- RL (prescriptive analytics) has the highest value among ML's trichotomy since it directly outputs actions with the promist that these actions will lead to valuable returns.
- RL is a great tool to conceptualize interaction in machine learning.

### My two cents

I think the author goes too far to motivate the value of RL by disdaining other ML regimes. 

Let's summon Yann Lecun's cake again:

<img src="https://user-images.githubusercontent.com/7057863/43362008-5a39a26c-9312-11e8-956e-f73df1c76dbd.jpg" alt="drawing" width="400px"/>

The rich information available to unsupervised learning has been proven to be very helpful for RL agent as auxialiary tasks [1]. In several Lecun's talks, he also emphasizes that:

> Good representation learnt by unsupervised learning is the key to solve RL's biggest deficiency: sample efficiency.

Besides learning good representation, unsupervised learning also enables generative modeling of the world, an essential component for agents that are not just reactive but able to perform planning in long horizon. The god father of Reinforcement Learning, Rich Sutton, once proposed an architecture called Dyna in which the main idea is to **try things in your head before acting**. He claimed that:

> The main idea of Dyna is the old, commonsense idea that planning is *trying things in your head* using an internal
model of the world. This suggests the existence of a more primitive process for trying things not in your head, but through direct
interaction with the world. Reinforcement learning is the name we use for this more primitive, direct kind of trying,
and Dyna is the extension of reinforcement learning to include a learned world model.

This is very intuitive, see this [funny birds video](https://www.youtube.com/watch?v=LI92DLRdKYE) for how helpful if you think before you act :)

Finally, from the perspective of Data Science [2]: 

> prescriptive analytics is about helping you see what the probable outcome relies on each decision. That helps you to decide what business decision to make.

According to this definition, it's clear that generative modeling lies at the heart of prescriptive analytics and directly classifying unsupervised learning as a whole into descriptive analytics is unfair.

In conclusion, I think it's inappropriate to argue that a) Unsupervised Learning has lower values compared to RL and b) there is an one-to-one connection between the three regimes in ML and Data Science. Different regimes in ML are actually complementary to each other in order to build **Prescriptive Analytics**.

What are some more inspirations we can draw from the field of Data Science? According to [3], expert recently postulated that **Automated Analytics** is a further extension to **Prescriptive Analytics**, eliminating the need for the human to make the final decision according to prescriptive analytics. In my opinion, as functions produced by machine learning algorithms gradually get used in important applications, their security and robustness becomes more crucial than ever before. More advances in ML safety would be essential for **Automated Analytics**.

### Reference

[1] [Reinforcement Learning with Unsupervised Auxiliary Tasks](https://arxiv.org/abs/1611.05397)
[2] [Why Prescriptive Analytics Is the Future of Big Data](https://www.linkedin.com/pulse/why-prescriptive-analytics-future-big-data-mark-van-rijmenam/)
[3] [Predictive Analytics - A Case For Private Equity?](https://www.forbes.com/sites/lutzfinger/2015/02/10/predictive-analytics-case-for-private-equity/#234d26097584)
