# Facial-Emotion-Recognition
Facial Emotion Recognition or FER is an emerging classification task often utilized in the human-computer  interaction sphere To achieve FER, various techniques are employed : in this project :
The primary machine learning model for this Facial Emotion Recognition (FER) project is the InceptionV3 convolutional neural network (CNN), selected for its proven accuracy and versatility in visual 
classification tasks, as demonstrated in a study by Erlangga et al. [3]. Initially developed by Google, the 
Inception-V3 model is optimized for image classification and trained on the extensive ImageNet dataset, 
which contains over a million images across a thousand categories. The architecture integrates several 
innovations, such as factorized and asymmetric convolutions, enabling the model to capture complex 
patterns with fewer parameters. It employs inception modules, where layers with varying kernel sizes (e.g., 
1x1, 3x3, and 5x5) operate in parallel to capture details at multiple scales.
Our model is trained in two stages: in the first stage, only the new classification head is trained while all 
Inception-V3 layersremain frozen; in the second stage, the last 50% of the Inception-V3 layers are unfrozen 
and fine-tuned with a low learning rate to capture emotion-specific features while preserving foundational 
patterns. Since the FER2013 has two sets split into 80% training and 20% testing, we took the training set 
and split as 80-20 train-validation split, while the testing set remained untouched, ensuring that we achieve
similar splits to the original approach with our used dataset. We will evaluate the model’s performance 
using accuracy, precision, recall, and F1-score. We will be comparing our model against a baseline 
Inception-V3 model without fine-tuning and classification head. For hyperparameter tuning, we mainly 
focused on selecting an effective learning rate and number of epochs to ensure smooth convergence. We 
began with a higher learning rate to train the new classification head, then lowered it significantly for finetuning the Inception-V3 layers, which allowed us to preserve key pre-trained features while adapting the 
model to recognize emotions. Throughout training, we closely monitored both training and validation losses 
to track the model’s progress. Additionally, we applied dropout as a regularization technique to support 
stable learning.
