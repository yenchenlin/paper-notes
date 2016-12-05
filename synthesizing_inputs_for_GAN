## [SoundNet: Learning Sound Representations from Unlabeled Video](http://web.mit.edu/vondrick/soundnet.pdf)

This paper developed a semantically rich representation for natural sound using unlabeled videos as a bridge to 
transfer discriminative visual knowledge from well-established visual recognition models into the sound modality.
The learned sound representation yields significant performance improvements on standard benchmarks for acoustic 
scene classification task.

### Key Points

- The natural synchronization between vision and sound can be leveraged as a supervision signal for each other.
- Cross-modal learning can overcome overfitting if the target modal have much fewer data than other modals, which is essential for deep networks to work well.

### Model
- The authors proposed a student-teacher training procedure to transfer discriminative visual knowledge from visual recognition models 
trained on ImageNet and Places into the SoundNet by minimizing KL divergence between their predictions.
![](https://cloud.githubusercontent.com/assets/7057863/20856609/05fe12d6-b94e-11e6-8c92-995ee84fe0d7.png)
- Two reasons to use CNN for sound: 1. invariant to translations; 2. stacking layers to detect higher-level concepts.
- **???** To handle variable-temporal-length of input sound, this model uses a fully convolutional network and produces an output over multiple timesteps in video.
- ***???*** Not clear about the data augmentation technique used in training.

### Exp

- Adding a linear SVM upon representation learned from SoundNet outperforms other existing methods 10%.
- Using lots of unlabeled videos as supervision signals enable the deeper SoundNet to work, or otherwise the 8-layer networks 
performs poorly due to overfitting.
- Simultaneous Using Places and ImageNet as supervision beats using only one of them 3%.
- Multi-modal recognition models use visual and sound data together yields 2% gain in classification accuracy.

### Thought
I think this paper is really complete since it contains good intuition, ablation analysis, representation visualization, hidden unit visualization, and significent performance imporvements.
