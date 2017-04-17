## [Synthesizing the preferred inputs for neurons in neural networks via deep generator networks](https://www.google.com.tw/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&ved=0ahUKEwj_jOqc6dvQAhWKfbwKHaG3B8YQFggaMAA&url=https%3A%2F%2Farxiv.org%2Fabs%2F1605.09304&usg=AFQjCNFSkaNfiK04_LFwaUwo5l4yD4sfcw&sig2=52CYBnpnwFlgjs5s3ov-bw)

This paper performs activation maximization (AM) using Deep Generator Network (DGN), which served as a learned natural iamge prior, to synthesize realistic images as inputs and feed it into the DNN we want to understand.
By visualizing synthesized images that highly activate particular neurons in the DNN, we can interpret what each of neurons in the DNN learned to detect.

### Key Points

- DGN (natural image prior) generates more coherent images when optimizing fully-connected layer codes instead of low-level codes. However, previous studies showed that low-level features results in better reconstructions beacuse it contains more image details. The difference is that here DGN-AM is trying to synthesize an entire layer code from scratch. Features in low-level only has a small, local receptive field so that the optimization process has to independently tune image without knowing the global structure. Also, the code space at a convolutional layer is much more high-dimensional, making it harder to optimize.

- The learned prior trained on ImageNet can also generalize to Places.
- It doesn't generalize well if architecture of the encoder trained with DGN is different with the DNN we wish to inspect.
- The learned prior also generalizes to visualize hidden neurons, producing more realistic textures/colors.
- When visualizing hidden neurons, DGN-AM trained on ImageNet also generalize to Places and produce similar results as [1].
- The synthesized images are showed to teach us what neurons in DNN we wish to inspect prefer instead of what prior prefer.

### Model

![](https://cloud.githubusercontent.com/assets/7057863/21002626/b094d7ae-bd61-11e6-8c95-fd4931648426.png)

### Thought
Solid paper with diverse visualizations and thorough analysis.

### Reference
[1] Object Detectors Emerge In Deep Scene CNNs, B.Zhou et. al.
