# MNIST Neural Network from Scratch

Overview
This project implements a neural network from scratch to classify handwritten digits from the MNIST dataset. Built entirely with numpy for matrix operations and pandas for data handling, the model achieves approximately 94% accuracy on a 10,000-image test set. This hands-on approach allowed me to deepen my understanding of both linear algebra and neural network theory.

Project Goals
Enhance Linear Algebra Skills: Built without frameworks like TensorFlow or PyTorch, this project emphasizes matrix math fundamentals.
Understand Neural Network Theory: By coding each component from scratch, I gained insights into the inner workings of neural networks.
Key Features
Customizable Neural Network Architecture: Easily adjustable layers and activation functions.
Batch Training with Gradient Descent: Efficiently trains with matrix-based gradient calculations.
Performance: Achieved ~94% accuracy on MNIST’s test set, demonstrating the network’s generalizability.
Model Architecture
The neural network consists of:

Input Layer: Accepts flattened 28x28 pixel images.
Hidden Layers: Configurable fully-connected layers with ReLU activation.
Output Layer: Softmax layer to classify images into one of 10 digits.
Code Snippets
Forward Pass
python
Copy code
# Example of the forward pass
def forward(X):
    Z1 = np.dot(X, W1) + B1
    A1 = np.maximum(0, Z1)  # ReLU activation
    Z2 = np.dot(A1, W2) + B2
    A2 = np.exp(Z2) / np.sum(np.exp(Z2), axis=1, keepdims=True)  # Softmax
    return A2
Training Loop
python
Copy code
# Example of the training loop
for epoch in range(epochs):
    for batch in range(num_batches):
        X_batch, y_batch = get_batch(X_train, y_train)
        y_pred = forward(X_batch)
        gradients = compute_gradients(y_pred, y_batch)
        update_parameters(gradients)
Results
Trained on MNIST with approximately 94% accuracy on the test set, the network demonstrates robust performance in digit classification.

Credits
Special thanks to Samson Zhang for his insightful videos that helped guide me through building this project.
