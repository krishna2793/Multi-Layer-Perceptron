# Multi-Layer-Perceptron
A very simple implementation of Multi Layer Perceptron Neural Network.
Classification tasks tend to create class boundaries that divides the data in feature space into multiple classes.
An SVM or a Linear Discriminant methods create a Linear class boundaries.
When the optimal class boundary is non linear, it is difficult to construct a model.
Multi Layer Perceptron Neural Networks act as Non-linear classifiers which learn from the data.

## Linear Perceptron:
Basic unit that takes n inputs and 1 output. The output is weighted sum of the inputs.
o = w1*i1 + w2*i2 + ... + wn*in

## Activation Function:
The non linearity of the MLP is achieved by the existance of activation function.
Thus output from Linear perceptron is passed to a function like ReLU or tanh to get output
o = act(w1*i1 + w2*i2 + ... + wn*in)

## Learning:
The weights w1,w2..wn are guessed randomly at start.
On each iteration, the values of the weights are adjusted to be a better approximation.
This process of updating weights and other parameters is called learning.

## Forward:
The outputs from each perceptron is fed to another perceptron forming a network.
When features are fed to input layer, the ouputs are calculated for each perceptron and fed as input to successors.
This process ends when the outputs(class predictions) are fetched from output layer

## BackPropogation:
For training data, we already know the class the datapoint belongs to.
We compare the predicted output with the class labels and the error is calculated based on the difference.
The errors for the preceding nodes are clculated by reversing the forward process.
Based on the error, the weights are adjusted 

## Bias:
When the weights are updated, the slope of the activation changes.
Sometimes that is not enough for proper learning. 
So we introduce a bias which shifts the curve to left or right.
The perceptron equation becomes
o = act(w1*i1 + w2*i2 + ... + wn*in + b)

## Learning Rate:
The learning rate determines how much a perceptron is rewarded or penalized for making a right or wrong prediction.
A higher learning rate means huge updates to the weights and bias and vice versa.

## Loss Function:
The error between prediction and the ground truth can be measured by several distance metrics.
Some famous metrics are Mean Square Error(MSE), Cross Entropy, etc..
The choice of Loss function depends on the domain.

