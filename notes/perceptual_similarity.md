## [Generating Images with Perceptual Similarity based on Deep Networks]()

This paper proposed a class of loss functions applicable to image generation that are based on distance in feature spaces:

![](https://cloud.githubusercontent.com/assets/7057863/21340329/b809b78a-c6c0-11e6-8e41-2aa264dc84a0.png)

### Key Points
- Using only l2 loss in image space yields over-smoothed results since it leads to averaging all likely locations of details.
- L_feat measures the distance in suitable feature space and therefore preserves distribution of fine details instead of exact locations.
- Using only L_feat yields bad results since feature representations are contractive. Many non-natural images also mapped to the same feature vector.
- By introducing a natural image prior - GAN, we can make sure that samples lie on the natural image manifold.

### Model

![](https://cloud.githubusercontent.com/assets/7057863/21340508/0644aa58-c6c2-11e6-8d8d-5338b88a10ce.png)

### Exp
- Training Autoencoder
- Generate images using VAE
- Invert feature

### Thought
I think the experiment section is a little complicated to comprehend. However, the proposed loss seems really promising and can be applied to many tasks related to image generation.

### Questions
- Section 4.2 & 4.3 are hard to follow for me, need to pay more attention in the future
