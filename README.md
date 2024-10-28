# MNIST Neural Network from Scratch

# Overview

This project demonstrates a neural network built from scratch to classify handwritten digits using the MNIST dataset. Developed solely with numpy for matrix operations and pandas for data handling, this model achieves an impressive 94% accuracy on the 10,000-image test set. Building this network without deep learning libraries provided hands-on experience in linear algebra, matrix math, and neural network theory.

**Project Goals**
Master Linear Algebra: Practice matrix math by implementing neural network components without frameworks like TensorFlow or PyTorch.
Deepen Neural Network Theory: Develop and train each network component manually to gain practical insights into their mechanics.

**Key Features**
Custom Neural Network Architecture: Flexible network with adjustable layers and activation functions.
Batch Training and Gradient Descent: Implements efficient matrix-based calculations.
Strong Performance: Achieves ~94% accuracy on MNIST, demonstrating its reliability.

**Model Architecture**
The neural network is structured as follows:

Input Layer: Accepts flattened 28x28 images.
Hidden Layers: Configurable fully-connected layers with ReLU activation.
Output Layer: Softmax layer classifying digits from 0 to 9.

**Forward Propagation Equations**
The core calculations in the network include:

1.Linear Transformation:

𝑍 = 𝑋 ⋅ 𝑊 + 𝐵
where:

 - 𝑋 is the input data matrix
 - 𝑊 is the weight matrix for each layer
 - 𝐵 is the bias vector


2. Activation (ReLU):

 A = ReLU(𝑍) = max(0,𝑍)
⁡

3. Softmax Output:

Softmax(𝑍)= 
∑e 
Z
e 
Z
 
​
This transforms the outputs into probabilities, summing to 1 for classification.

**Loss Function**
The model minimizes cross-entropy loss:

Loss
=
−
1
𝑚
∑
𝑖
=
1
𝑚
𝑦
𝑖
⋅
log
⁡
(
𝑦
^
𝑖
)
Loss=− 
m
1
​
  
i=1
∑
m
​
 y 
i
​
 ⋅log( 
y
^
​
  
i
​
 )
where:

𝑚
m is the number of samples
𝑦
𝑖
y 
i
​
  is the true label
𝑦
^
𝑖
y
^
​
  
i
​
  is the predicted probability for the true class
        
Results
The model achieved approximately 94% accuracy on the MNIST test set, showcasing its capacity to generalize well on unseen data.

Credits
A huge thank you to Samson Zhang for his educational videos that were instrumental in guiding this project.
