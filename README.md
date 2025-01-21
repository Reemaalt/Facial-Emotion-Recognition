# Facial-Emotion-Recognition
This project utilizes the Inception-V3 CNN for Facial Emotion Recognition (FER), leveraging its proven performance in visual classification tasks. The model is fine-tuned in two stages using the FER2013 dataset:

Stage 1: Train a custom classification head with Inception-V3 layers frozen.
Stage 2: Fine-tune the last 50% of Inception-V3 layers with a low learning rate.
Performance is evaluated on accuracy, precision, recall, and F1-score, with comparisons to a baseline model. Hyperparameters were tuned for optimal convergence, and dropout was applied for regularization.
