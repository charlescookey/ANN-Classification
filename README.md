# Fitting a model using Fully connected Layers

Hidden Layer 1: The idea is to extract broad features from the input. This allows the model capture patterns such as shape, edges, and textures. 100 neurons were used as the allows the model capture a wide variety of low level features from the image.
A ReLU activation was the applied as this help retain non-linearity and mitigates vanishing gradient issues

Hidden Layer 2: This reduced the feature space but retains learned patters. 50 neurons were chosen as this would aloow the model discard irrelevant information and focus on the object parts and texture clusters. This also helps prevent overfiting, as the model would not learn the noise. A ReLU activation was also applied here

Hidden layer 3: The nerons were reduced to 25, this prevents overfitting as too many layers would cause the model to memorize data rather then generalize well , this also ensures that only the most discriminative features remain before classification. The reduction improves computational efficiency.

Output Layer: 4 nerons, which translate to the class labels. 


## Result 

Train Epoch: 20 [560/601 (92%)]	Loss: 0.195941 <br>
Train Epoch: 20 [601/601 (100%)]	Loss: 0.195941 <br>
Epoch: 20, Training Accuracy: 93.18% <br>
Epoch: 20, Validation Accuracy: 76.92% <br>
Epoch: 20, Testing Accuracy: 88.46% <br>
Training and evaluation finished in: 18.905198097229004 sec. <br>
Final Training Loss (Last Epoch): 0.216405 <br>


### Final Evaluation Metrics: <br>
Precision: 74.54%, Recall: 74.81%, F1-Score: 74.31% <br>
Confusion Matrix: <br>
[[254   4  39  43] <br>
 [ 81 205   9  85] <br>
 [ 18   3 397   2] <br>
 [ 24  78   7 311]] <br>
Class 0 Accuracy: 74.71% <br>
Class 1 Accuracy: 53.95% <br>
Class 2 Accuracy: 94.52% <br>
Class 3 Accuracy: 74.05% <br>
