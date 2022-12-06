1. What is one-hot encoding? Why is this important and how do you implement it in keras?
	- One-hot encoding is a method used in data preprocessing that converts categorical variables to numerical data.
	- In keras, we can perform one-hot encoding by calling keras.utils.to_categorical() function
2. What is dropout and how does it help overfitting?
	- Dropout is a regularization technique that helps prevent neural network from overfitting. 
	- By applying dropout, the neural network randomly "turns off" neurons during training. The "off" neurons do not contribute or learn information and forces other "on" neurons to adapt and learn robust useful features. It also temporarily alters the network structure to form an ensemble of subnetworks, which will average the effects of overfitting in different networks.

3. How does ReLU differ from the sigmoid activation function?
	- Sigmoid function is a non-linear activation function that transforms an input value to an output value anywhere between 0 and 1. The ouput saturates around 0 and 1 and the midpoint is very sensitive to change. When using sigmoid activation to train large nueral networks, it become inefficient and difficult for the weights to adapt. Sigmoid also can cause the neural networks to suffer from "vanishing gradient"
	- ReLU takes inspiration from biological neurons and ouputs a value of 1 if input is positive and 0 if negative. ReLU activation function is half linear and half non-linear, which eliminates vanishing gradient problem while also allowing for degrees of model complexity. ReLU also requires less computation and is generally more efficient
	
4. Why is the softmax function necessary in the output layer?
	- The softmax activation function transforms the output of the neural network into a vector of probabilities by 
squashing the values into a set of number between 0 and 1 whose sum is 1. Softmax shows us probability distribution, which is useful in predicting output in multi-class classification.

5. This is a more practical calculation. Consider the following convolution network:
(a) Input image dimensions = 100x100x1
(b) Convolution layer with filters=16 and kernel size=(5,5)
(c) MaxPooling layer with pool size = (2,2) 
What are the dimensions of the outputs of the convolution and max pooling layers?
	- convolution layer output dimension: 96x96x16
	- Max pooling layer output dimension: 48x48x16

6. My choice of architecture is inspired by the classic LeNet-5 architecture. I've also added dropout to reduce overfitting. I was able to achieve an accuracy score of 93.39% on the test dataset.



