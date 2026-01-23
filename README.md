# Image-Classification-GenAI-task

GARBAGE CLASSIFICATION

Model Architectures:

For this task, I implemented and compared the result of a custom CNN model and ResNet (pre-trained) model via augmented and non-augmented (simple) transformations of the garbage dataset.

1) Custom CNN (Scratch):
     Implemented a 3-layer Convolutional Neural Network designed to learn spatial features from the garbage dataset.
     It includes Conv2d layers to scan the images for edges and shapes.
     MaxPool2d to shrink the images and focus on the most important features
     Fully Connected layers for the final 6-class classification.

2) ResNet-18 (Transfer Learning):
     I utilized a pre-trained ResNet-18 model
     Pre-trained weights: It already knows how to recognize objects because it was trained on 1 million images (ImageNet).
     Freezing: kept the early layers "frozen" so it does not loses the pre-trained knowledge.
     Match 6-category garbage: replaced the very last layer with a new one that specifically looks for our 6 types of garbage.


Final Results: 

I conducted four experimental trials to determine the most robust and reliable model.

Case	                                     Accuracy	                 Reliability
Scratch + No Augmentation	                  98.76%	              Low (Overfitting)
Scratch + Augmentation	                    77.02%	                    Medium
ResNet-18 + No Augmentation	                84.84%	                     High
ResNet-18 + Augmentation	                  79.35%	          Highest (Best Generalization)


