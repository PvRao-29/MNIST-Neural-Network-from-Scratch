# MNIST Neural Network from Scratch

## Overview
This project implements a neural network built from scratch to classify handwritten digits using the MNIST dataset. Built entirely with numpy for matrix operations and pandas for data handling, the model achieves approximately 94% accuracy on a 10,000-image test set. This hands-on approach allowed me to deepen my understanding of both linear algebra and neural network theory.

## Model Architecture
The neural network is structured as follows:

Input Layer: Accepts flattened 28x28 images. <br/> 
Hidden Layers: Configurable fully-connected layers with ReLU activation. <br/> 
Output Layer: Softmax layer classifying digits from 0 to 9. <br/> 

## Forward Propagation Equations
Linear Transformation:

Each layer’s output Z is computed as:
Z = X * W + B
Where:
X is the input data matrix.
W is the weight matrix for the layer.
B is the bias vector.
Activation (ReLU):

The ReLU activation function is applied to Z to introduce non-linearity:
A = max(0, Z)
This sets all negative values in Z to zero.
Softmax Output:

The final layer uses Softmax to convert outputs into probabilities:
Softmax(Z) = exp(Z) / sum(exp(Z))
This ensures that all output values sum to 1, making them interpretable as probabilities for classification.

## Loss Function
The model minimizes cross-entropy loss during training, defined as:
Loss = -1/m * sum(y * log(ŷ))
Where:
m is the number of samples.
y is the true label vector.
ŷ is the predicted probability vector for the true class.
        
## Results
The model achieved approximately 94% accuracy on the MNIST test set, showcasing its capacity to generalize well on unseen data.

## Credits
A huge thank you to Samson Zhang for his educational videos that were instrumental in guiding this project.
