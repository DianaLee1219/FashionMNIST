# Fashion MNIST Classification with MLP
What is Fashion MNIST?
Fashion MNIST is a widely used benchmark dataset for machine learning, designed as a more challenging alternative to the original MNIST digit dataset. It consists of 70,000 grayscale images (60,000 for training, 10,000 for testing), each sized 28x28 pixels and labeled as one of 10 clothing categories:

![image](https://github.com/user-attachments/assets/5d0d0702-d6f1-4c18-8d76-04a77378d089)

| Lable | Type |
| 0	| T-shirt/top |
| 1	| Trouser |
| 2	| Pullover |
| 3	| Dress |
| 4	| Coat |
| 5	| Sandal |
| 6	| Shirt | 
| 7 |	Sneaker |
| 8	| Bag | 
| 9 |	Ankle boot |

The dataset is commonly used for benchmarking image classification models and is included in standard ML libraries like Keras and TensorFlow.

## Project Workflow
This project implements a simple Multi-Layer Perceptron (MLP) to classify Fashion MNIST images. The main steps are:

1. Data Loading & Preprocessing

Load the Fashion MNIST dataset using Keras.

Normalize pixel values to the range for stable training.

Flatten each 28x28 image into a 784-dimensional vector for the MLP input.

2. Model Building

Define a simple MLP with one or two hidden dense layers, using ReLU or swish activations.

The output layer uses softmax activation to predict probabilities for each of the 10 classes.

3. Training

Compile the model with a suitable optimizer (e.g., SGD with momentum or Adam), categorical cross-entropy loss, and accuracy metric.

Train the model on the training set, monitoring validation accuracy to avoid overfitting.

4. Evaluation

Evaluate the trained model on the test set to measure generalization performance.

Achieved test accuracy is typically in the 87–91% range for a well-tuned MLP.

5. Prediction

Implement a prediction function that takes a single image and returns the predicted class label.

6. Model Saving

Save the trained model in .h5 format for future use or deployment.

## Results
The MLP model achieved a test accuracy of approximately 89–91%, depending on architecture and hyperparameters.

Validation accuracy and loss curves were plotted to monitor training progress.

The model can accurately classify most clothing items, though some classes (e.g., shirt vs. T-shirt/top) are more challenging and may be confused more often.


## Experiments to improve the validation accuracy 
1. Enhanced Model Architecture did not improve the validation accuracy

I asked perplexity how to increase the validation accuracy, and it recommended to enhance the model architecture.
However, the accuracy dropped as below.

Changes:

- Increased layer sizes (512 → 256 → 128) for better feature extraction.

- Swish activation (x⋅σ(x)x⋅σ(x)) instead of ReLU for smoother gradients.

- Added L2 regularization (λ=0.001) to prevent overfitting.

- Batch normalization after each dense layer for stable training.

- Higher dropout rate (0.5) to enforce robust learning.

Before:
![image](https://github.com/user-attachments/assets/938b9117-baf8-4d7c-ba32-313e64fe79a2)
![image](https://github.com/user-attachments/assets/d117db86-5b34-4135-a376-d28d2e5d32cb)

After:
![image](https://github.com/user-attachments/assets/381ef769-c2fb-44ba-87d4-c560c871bcf1)
![image](https://github.com/user-attachments/assets/94c8b7af-0aad-45dc-92c0-23d52763e21e)

## 
