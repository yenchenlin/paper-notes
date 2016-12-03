## [SoundNet: Learning Sound Representations from Unlabeled Video](http://web.mit.edu/vondrick/soundnet.pdf)

This paper developed a semantically rich representation for natural sound using unlabeled videos as a bridge to 
transfer discriminative visual knowledge from well-established visual recognition models into the sound modality.
The learned sound representation yields significant performance improvements on standard benchmarks for acoustic 
scene classification task.

### Key Points

- The natural synchronization between vision and sound can be leveraged as a supervision signal for each other.
- The authors proposed a student-teacher training procedure to transfer discriminative visual knowledge from visual recognition models 
trained on ImageNet and Places into the SoundNet by minimizing KL divergence between their predictions.
![](https://cloud.githubusercontent.com/assets/7057863/20856609/05fe12d6-b94e-11e6-8c92-995ee84fe0d7.png)

- 
- 

### Notes

- This work reminds of of Highway Networks, with an additional constraint to make the gates sparse to save computation.
- It's surprising to me that the authors didn't evaluate using different architectures for each experts network. That would've been the first use case that comes to my mind. They mention this possibility in the paper but I would've loved to see experiments for this.
- `We used the Adam optimizer (Kingma & Ba, 2015). The learning rate was
increased linearly for the first 200 training steps, held constant for the next 200 steps, and decreased
after that so as to be proportional to the inverse square root of the step number.` - Hmmm.... :)
