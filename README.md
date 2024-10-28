# MNIST Neural Network from Scratch

## Overview
This project implements a neural network built from scratch to classify handwritten digits using the MNIST dataset. Built entirely with numpy for matrix operations and pandas for data handling, the model achieves approximately 94% accuracy on a 10,000-image test set. This hands-on approach allowed me to deepen my understanding of both linear algebra and neural network theory.

## Model Architecture
The neural network is structured as follows:

Input Layer: Accepts flattened 28x28 images. <br/> 
Hidden Layers: Configurable fully-connected layers with ReLU activation. <br/> 
Output Layer: Softmax layer classifying digits from 0 to 9. <br/> 

## Mathematical Foundations

### Forward Propagation

#### Linear Transformation

For each layer \( l \), the linear transformation is computed as:

$$
Z^{[l]} = A^{[l-1]} W^{[l]} + b^{[l]}
$$

- \( Z^{[l]} \): Linear output of layer \( l \).
- \( A^{[l-1]} \): Activations from the previous layer (or input data \( X \) for the first layer).
- \( W^{[l]} \): Weights matrix for layer \( l \).
- \( b^{[l]} \): Bias vector for layer \( l \).

#### Activation Functions

- **ReLU Activation**:

  $$
  A^{[l]} = \text{ReLU}(Z^{[l]}) = \max(0, Z^{[l]})
  $$

  Applies to all hidden layers to introduce non-linearity.

- **Softmax Activation (Output Layer)**:

  $$
  A^{[L]}_i = \frac{ e^{ Z^{[L]}_i } }{ \sum_{j=1}^{K} e^{ Z^{[L]}_j } }
  $$

  - \( A^{[L]}_i \): Probability of class \( i \).
  - \( K \): Total number of classes (10 for MNIST).

### Loss Function

The model minimizes the **Cross-Entropy Loss**, defined as:

$$
\mathcal{L} = -\frac{1}{m} \sum_{i=1}^{m} \sum_{k=1}^{K} y_{i,k} \log(A^{[L]}_{i,k})
$$

- \( m \): Number of examples.
- \( y_{i,k} \): True label (one-hot encoded) for example \( i \) and class \( k \).
- \( A^{[L]}_{i,k} \): Predicted probability for example \( i \) and class \( k \).

## Results
The model achieved approximately 94% accuracy on the MNIST test set, showcasing its capacity to generalize well on unseen data.

## Credits
A huge thank you to Samson Zhang for his educational videos that were instrumental in guiding this project.
