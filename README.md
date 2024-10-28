# MNIST Neural Network from Scratch

## Overview

This project implements a neural network built from scratch to classify handwritten digits using the MNIST dataset. Built entirely with numpy for matrix operations and pandas for data handling, the model achieves approximately 94% accuracy on a 10,000-image test set. This hands-on approach allowed me to deepen my understanding of both linear algebra and neural network theory.

## Model Architecture
The neural network is structured as follows:

Input Layer: Accepts flattened 28x28 images. <br/> 
Hidden Layers: Configurable fully-connected layers with ReLU activation. <br/> 
Output Layer: Softmax layer classifying digits from 0 to 9. <br/> 

## Forward Propagation Equations
The core calculations in the network include:

**1.Linear Transformation:**

𝑍 = 𝑋 ⋅ 𝑊 + 𝐵 <br/> 
where: <br/> 
 - 𝑋 is the input data matrix <br/> 
 - 𝑊 is the weight matrix for each layer <br/> 
 - 𝐵 is the bias vector <br/> 


**2. Activation (ReLU):** <br/> 

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

##Loss Function
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
        
## Results
The model achieved approximately 94% accuracy on the MNIST test set, showcasing its capacity to generalize well on unseen data.

## Credits
A huge thank you to Samson Zhang for his educational videos that were instrumental in guiding this project.
